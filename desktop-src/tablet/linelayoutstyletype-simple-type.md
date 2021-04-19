---
description: Définit les valeurs valides pour l’attribut style de l’élément LineLayout.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Type simple LineLayoutStyleType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 67b07d9de51e16148905768d7a6f268038bb1afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530260"
---
# <a name="linelayoutstyletype-simple-type"></a><span data-ttu-id="9e7fd-103">Type simple LineLayoutStyleType</span><span class="sxs-lookup"><span data-stu-id="9e7fd-103">LineLayoutStyleType Simple Type</span></span>

<span data-ttu-id="9e7fd-104">Définit les valeurs valides pour l’attribut **style** de l' [élément LineLayout](linelayout-element.md).</span><span class="sxs-lookup"><span data-stu-id="9e7fd-104">Defines the valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md).</span></span>

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="9e7fd-105">Modèles</span><span class="sxs-lookup"><span data-stu-id="9e7fd-105">Patterns</span></span>

<span data-ttu-id="9e7fd-106">Le type simple **LineLayoutStyleType** est une chaîne qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="9e7fd-106">The **LineLayoutStyleType** simple type is a string that is restricted by the following pattern:</span></span>

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a><span data-ttu-id="9e7fd-107">Notes</span><span class="sxs-lookup"><span data-stu-id="9e7fd-107">Remarks</span></span>

<span data-ttu-id="9e7fd-108">Les valeurs valides pour l’attribut **style** de l' [élément LineLayout](linelayout-element.md) sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e7fd-108">Valid values for the **Style** attribute of the [LineLayout element](linelayout-element.md) are:</span></span>

-   <span data-ttu-id="9e7fd-109">Aucun</span><span class="sxs-lookup"><span data-stu-id="9e7fd-109">None</span></span>
-   <span data-ttu-id="9e7fd-110">Unie</span><span class="sxs-lookup"><span data-stu-id="9e7fd-110">Solid</span></span>
-   <span data-ttu-id="9e7fd-111">Tiret</span><span class="sxs-lookup"><span data-stu-id="9e7fd-111">Dash</span></span>
-   <span data-ttu-id="9e7fd-112">Points</span><span class="sxs-lookup"><span data-stu-id="9e7fd-112">Dot</span></span>
-   <span data-ttu-id="9e7fd-113">Tiret-point</span><span class="sxs-lookup"><span data-stu-id="9e7fd-113">DashDot</span></span>
-   <span data-ttu-id="9e7fd-114">Tiret-point-point</span><span class="sxs-lookup"><span data-stu-id="9e7fd-114">DashDotDot</span></span>
-   <span data-ttu-id="9e7fd-115">Double</span><span class="sxs-lookup"><span data-stu-id="9e7fd-115">Double</span></span>

## <a name="requirements"></a><span data-ttu-id="9e7fd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e7fd-116">Requirements</span></span>



| <span data-ttu-id="9e7fd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e7fd-117">Requirement</span></span> | <span data-ttu-id="9e7fd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e7fd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9e7fd-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e7fd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e7fd-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e7fd-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9e7fd-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e7fd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e7fd-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e7fd-122">None supported</span></span><br/>                                     |



 

 




