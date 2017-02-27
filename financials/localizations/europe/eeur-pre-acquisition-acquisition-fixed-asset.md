---
title: Post the pre-acquisition of a fixed asset
description: This topic explains how to set up and post fixed asset pre-acquisitions.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-19 19 - 43 - 14
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.custom: 264704
ms.assetid: 89218666-7c5e-45ca-aead-a87853d05928
ms.search.region: Czech Republic, Hungary
ms.author: epopov
ms.dyn365.ops.intro: 01-11-2016
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 79252321f41cd14f84ab40df34c6c9eca64374f2
ms.lasthandoff: 02/22/2017


---

# <a name="post-the-pre-acquisition-of-a-fixed-asset"></a>Post the pre-acquisition of a fixed asset

This topic explains how to set up and post fixed asset pre-acquisitions.

**Note:** The functionality for posting fixed asset pre-acquisitions is available only for legal entities that have their primary address in Hungary or the Czech Republic. A pre-acquisition of a fixed asset isn't depreciable, and it doesn't affect the acquisition costs or the net book value of the fixed asset. When you post a pre-acquisition, the status of the fixed asset is changed to **Acquired**. A fixed asset that has the **Acquired** status isn't depreciable. By contrast, when you post an acquisition, the status is changed to **Open**, and the fixed asset is depreciable.

## <a name="set-up-preacquisitions"></a>Set up preacquisitions
Before you can post a pre-acquisition, you must complete the following setup:

-   On the **Fixed assets parameters** page, set the **Allow pre-acquisitions** option to **Yes**.
-   On the **Fixed asset posting profiles** page, set up a fixed asset posting profile for the pre-acquisition posting type.

## <a name="post-a-preacquisition-of-a-fixed-asset"></a>Post a preacquisition of a fixed asset
1.  On the **Fixed assets** page, create a new journal, and enter all applicable information, as required.
2.  For the journal that you just created, click **Lines** to open the **Journal voucher** page.
3.  Click **New** to create a line.
4.  In the **Transaction type** field, select a transaction that has the **Pre-Acquisition** transaction type.
5.  Enter values for the remaining fields as required.
6.  Click **Validate** to validate the journal lines.
7.  Click **Proposals** &gt; **Pre-acquisition proposal**.
8.  Click **Select** to set up the selection criteria, and then click **OK**.
9.  Click **OK** to close the **Pre-acquisition proposal** page.
10. Click **Post** &gt; **Post** to post the pre-acquisition transaction. On the **Books** page, the status of the fixed asset should now be **Acquired**.



