---
title: Fixed assets depreciation methods for the Czech Republic
description: This topic provides information about fixed assets depreciation for legal entities in the Czech Republic.
author: ShylaThompson
manager: AnnBe
ms.date: 2016-12-16 21 - 23 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationGroup_W
audience: Application User
ms.search.scope: AX 7.0.0, Operations
ms.custom: 264314
ms.assetid: 185cc4ce-d1b2-429a-9b1b-6b9c4b865da0
ms.search.region: Czech Republic
ms.author: v-elgolu
ms.dyn365.ops.intro: 01-05-2016
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: b97d17ceabfd25c52c5f0c1e96a123bae6941c5a
ms.openlocfilehash: 8362692c1a9c9e13a44b53827c4276283b6ffdf8
ms.lasthandoff: 02/22/2017


---

# <a name="fixed-assets-depreciation-methods-for-the-czech-republic"></a>Fixed assets depreciation methods for the Czech Republic

This topic provides information about fixed assets depreciation for legal entities in the Czech Republic. 

Fixed assets depreciation for the legal requirements in the Czech Republic include:

-   Depreciation percentages
-   Depreciation methods that are specific to the Czech Republic

## <a name="depreciation-percentages-and-coefficients"></a>Depreciation percentages and coefficients
Per Czech Republic legislation, fixed assets are grouped in depreciation groups. For each depreciation group, legislation has defined specific values for the depreciation rate for the first year, a depreciation rate for subsequent years, and an adjusted acquisition price. To meet the legal requirements in the Czech Republic, different values of the depreciation rate for the first year, for next years, and for the adjusted acquisition price must be set up in different depreciation groups. The **Depreciation groups** page contains the following options.

|                                          |                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                                | **Description**                                                                                                                                                                                                                                                                                                                                                               |
| **Start date**                           | Enter the date when the depreciate group will start.                                                                                                                                                                                                                                                                                                                          |
| **Depreciation rate for the first year** | Enter the depreciation percentage for the regular CZ depreciation method or the depreciation coefficient for the accelerated CZ depreciation method used in the first depreciation year of this group.                                                                                                                                                                        |
| **Depreciation rate for next years**     | Enter the depreciation percentage for the regular CZ depreciation method or the depreciation coefficient for the accelerated CZ depreciation method for depreciation in years following the year of acquisition.                                                                                                                                                              |
| **Adjusted acquisition price**           | Enter the depreciation percentage for the regular CZ depreciation method or the depreciation coefficient for the accelerated CZ depreciation method that is extended by an acquisition adjustment. This percentage or coefficient is valid from the year of the acquisition adjustment. All positive and negative adjustments are included in the adjusted acquisition price. |

## <a name="czech-republicspecific-depreciation-methods"></a>Czech Republicspecific depreciation methods
For users in legal entities in Czech Republic, there are additional depreciation methods available. Additional rules and settings are used to meet specific fixed asset accounting requirements. Per Czech Republic regulations, the following depreciation methods are applied in the Czech Republic:

-   Regular CZ
-   Accelerated CZ

For more information about depreciation methods, see [Fixed asset depreciation](fixed-asset-depreciation.md).

### <a name="regular-cz-depreciation-method"></a>Regular CZ depreciation method

The regular CZ depreciation method calculates depreciation using the following formulas:

-   Depreciation amount in the first year = Acquisition value \* Depreciation percentage for the first year
-   Depreciation amount in the next years = Acquisition value \* Depreciation percentage for the next years
-   Depreciation amount after acquisition adjustment = (Acquisition value + Acquisition adjustment) \* Depreciation percentage after acquisition adjustment

The following example shows the regular CZ method of depreciation calculation.

|                                                      |                     |
|------------------------------------------------------|---------------------|
| **Field**                                            | **Value**           |
| Acquisition value                                    | 100 000             |
| Acquisition adjustment                               | 50 000 (in 3d year) |
| Depreciation percentage for the first year           | 14.2%               |
| Depreciation percentage for the next years           | 28.6%               |
| Depreciation percentage after acquisition adjustment | 25.0%               |

This example shows depreciation calculated using the regular CZ method of depreciation.

|                     |                           |
|---------------------|---------------------------|
| **Number of years** | **Calculation**           |
| 1                   | 100 000 \* 14.2% = 14 200 |
| 2                   | 100 000 \* 28.6% = 28 600 |
| 3                   | 150 000 \* 25% = 37 500   |
| 4                   | 150 000 \* 25% = 37 500   |

### <a name="accelerated-cz-depreciation-method"></a>Accelerated CZ depreciation method

The accelerated CZ method of deprecation uses coefficients to calculate the depreciation using the following formulas:

-   Depreciation amount in the first year = Acquisition value / Depreciation coefficient for the first year,
-   Depreciation amount in the next years = (2 \* Net book value) / (Depreciation coefficient for next years - Already depreciated periods)
-   Depreciation amount after acquisition adjustment = (2 \* Net book value) / (Depreciation coefficient after acquisition adjustment - Already depreciated periods after certain acquisition adjustment)

The following example shows the accelerated CZ method of depreciation calculation.

|                                                       |           |
|-------------------------------------------------------|-----------|
| **Field**                                             | **Value** |
| Acquisition value                                     | 100 000   |
| Acquisition adjustment (in 3 year)                    | 50 000    |
| Acquisition adjustment (in 5 year)                    | 60 000    |
| Depreciation coefficient for the first year           | 4         |
| Depreciation coefficient for the next years           | 5         |
| Depreciation coefficient after acquisition adjustment | 4         |

This example shows depreciation calculated using the accelerated CZ method of depreciation.

|                     |                                  |
|---------------------|----------------------------------|
| **Number of years** | **Calculation**                  |
| 1                   | 100 000 /4 = 25 000              |
| 2                   | (2 \* 75 000) / (5 - 1) = 37 500 |
| 3                   | (2 \* 87 500) / (4 - 0) = 43 750 |
| 4                   | (2\* 43750) / (4 - 1) = 29 167   |
| 5                   | (2\* 74583) / (4 - 0) = 37 292   |
| 6                   | (2\* 37292) / (4 - 1) = 24 861   |
| 7                   | (2\* 12431) / (4 - 2) = 12 430   |

 

