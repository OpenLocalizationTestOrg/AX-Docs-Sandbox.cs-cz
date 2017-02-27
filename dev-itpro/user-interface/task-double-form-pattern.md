---
title: Task Double form pattern
description: This article provides information about the Task Double form pattern. This pattern was previously used to present a parent and child entity in the same form.
author: jasongre
manager: AnnBe
ms.date: 2015-12-02 23 - 42 - 59
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations
ms.custom: 14651
ms.assetid: 9f28e5f9-efec-48c5-aaa6-b68a505c4df3
ms.search.region: Global
ms.author: jasongre
ms.dyn365.ops.intro: 01-02-2016
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 3094438cdbf34a900c0a7550513a2e97dde45bb5
ms.lasthandoff: 02/22/2017


---

# <a name="task-double-form-pattern"></a>Task Double form pattern

This article provides information about the Task Double form pattern. This pattern was previously used to present a parent and child entity in the same form.

<a name="usage"></a>Usage
-----

This type of form has previously been used when you wanted to present parent/child entities in the same form. This isn't a recommended pattern for new forms. No new forms should be created that use this pattern. This pattern will provide structure and stability for legacy forms, and will also provide a migration path to more modern form patterns.

## <a name="wireframe"></a>Wireframe
[![patternTaskDouble](./media/patterntaskdouble.png)](./media/patterntaskdouble.png)[](./media/taskdouble1.png)

## <a name="pattern-changes"></a>Pattern changes
Here are the main changes to this pattern since Microsoft Dynamics AX 2012:

-   The form opens in view mode.
-   The top ActionPane strip control has been converted to a standard ActionPane.
-   The **Overview** label on the parent tab has been changed to **List**.
-   The contents of the tab container use dynamic columns for a responsive layout.
-   The label for the child tab’s list should be **&lt;x&gt; list**, where **&lt;x&gt;** is replaced by an appropriate string, based on the entity. For example, if the child entity is usually called Charges, the label for the tab should be **Charges list**.
    -   Exception: If the child entity is “lines” of some sort, the word “list” should not be added to the end.

## <a name="model"></a>Model
### <a name="high-level-structure"></a>High-level structure

Design

ActionPane (Action Pane)

*CustomFilter (Group) \[Optional\]*

ParentTab (Tab)

ParentList (TabPage) – **Note:** The Toolbar and List subpattern is used.

General (TabPage repeats 0..N)

*ParentFooterGroup (Group) \[Optional\]*

HSplitter (Group)

*ChildToolbar (ActionPane) \[Optional\]*

ChildTab (Tab)

ChildList (TabPage) – **Note:** The Toolbar and List subpattern is used.

General (TabPage, repeats 0..N)

*ChildFooterGroup (Group) \[Optional\]*

### <a name="core-components"></a>Core components

1.  Apply the Task Double pattern on **Form.Design**.
2.  Address BP Warnings:
    1.  **Design.Caption** isn't empty.
    2.  The form must be referenced by at least one menu item.
    3.  **TabPage.Caption** isn't empty.
    4.  **TabPage.DataSource** isn't empty.
    5.  **StaticText.Text** isn't empty.

### <a name="related-patterns"></a>Related patterns

-   [Task Single](task-single-form-pattern.md)

### <a name="commonly-used-subpatterns"></a>Commonly used subpatterns

-   [Custom Filter Group](custom-filter-group-subpattern.md)
-   [Fields and Field Groups](fields-field-groups-subpattern.md)
-   [Toolbar and List](toolbar-list-subpattern.md)
-   [Toolbar and Fields](toolbar-fields-subpattern.md)

## <a name="ux-guidelines"></a>UX guidelines
The verification checklist shows the steps for manually verifying that the form complies with UX guidelines. This checklist doesn't include any guidelines that will be enforced automatically through the development environment. Open the form in the browser, and walk through these steps.

**Standard form guidelines:**

-   Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md)document.

**Task Double guidelines:**

-   The **Overview** tab is the first tab and is active when the form is opened.
-   The first tab on a child tab control should be called **Lines list** or an appropriate variation.
-   Selection in the parent grid will update content in the child grid.

## <a name="example"></a>Example
Form: **HRMAbsenceTableHistory** [![Task Double example](./media/taskdouble2-1024x639.png)](./media/taskdouble2.png)

## <a name="appendix"></a>Appendix
### <a name="frequently-asked-questions"></a>Frequently asked questions

This section will have answers to frequently asked questions that are related to this guideline/pattern.

### <a name="open-issues"></a>Open issues

-   None

### <a name="ax-2012-content"></a>AX 2012 content

[![AX 2012 visual example](./media/taskdouble3.png)](./media/taskdouble3.png)

