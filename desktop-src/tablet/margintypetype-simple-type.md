---
description: Définit le type qui contient des valeurs valides pour l’attribut de type de l’élément Margin.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Type simple MarginTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210292"
---
# <a name="margintypetype-simple-type"></a><span data-ttu-id="a4bf5-103">Type simple MarginTypeType</span><span class="sxs-lookup"><span data-stu-id="a4bf5-103">MarginTypeType Simple Type</span></span>

<span data-ttu-id="a4bf5-104">Définit le type qui contient des valeurs valides pour l’attribut de **type** de l' [élément Margin](margin-element.md).</span><span class="sxs-lookup"><span data-stu-id="a4bf5-104">Defines the type that contains valid values for the **Type** attribute for the [Margin element](margin-element.md).</span></span>

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="a4bf5-105">Modèles</span><span class="sxs-lookup"><span data-stu-id="a4bf5-105">Patterns</span></span>

<span data-ttu-id="a4bf5-106">Le type simple **MarginTypeType** est une **chaîne** qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="a4bf5-106">The **MarginTypeType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `Left|Right`

## <a name="remarks"></a><span data-ttu-id="a4bf5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a4bf5-107">Remarks</span></span>

<span data-ttu-id="a4bf5-108">Les valeurs valides pour l’attribut de **type** de l' [élément Margin](margin-element.md) sont « Left » et « Right ».</span><span class="sxs-lookup"><span data-stu-id="a4bf5-108">The valid values for the **Type** attribute for the [Margin element](margin-element.md) are "Left" and "Right".</span></span>

## <a name="requirements"></a><span data-ttu-id="a4bf5-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4bf5-109">Requirements</span></span>



| <span data-ttu-id="a4bf5-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4bf5-110">Requirement</span></span> | <span data-ttu-id="a4bf5-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4bf5-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a4bf5-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4bf5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a4bf5-113">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4bf5-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a4bf5-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4bf5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a4bf5-115">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4bf5-115">None supported</span></span><br/>                                     |



 

 




