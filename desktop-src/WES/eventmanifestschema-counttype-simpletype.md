---
title: Type simple CountType
description: Définit un type de nombre qui est utilisé pour spécifier le nombre d’éléments dans un tableau.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- Journal des types simples CountType
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743837"
---
# <a name="counttype-simple-type"></a><span data-ttu-id="ba3fa-104">Type simple CountType</span><span class="sxs-lookup"><span data-stu-id="ba3fa-104">CountType Simple Type</span></span>

<span data-ttu-id="ba3fa-105">Définit un type de nombre qui est utilisé pour spécifier le nombre d’éléments dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="ba3fa-105">Defines a count type that is used to specify the number of elements in an array.</span></span> <span data-ttu-id="ba3fa-106">La valeur peut être spécifiée sous la forme d’une valeur XS : unsignedShort ou sous la forme d’une chaîne qui fait référence au nom du nœud d’élément de données qui contient la valeur Short unsiged.</span><span class="sxs-lookup"><span data-stu-id="ba3fa-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsiged short value.</span></span>

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="ba3fa-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba3fa-107">Requirements</span></span>



| <span data-ttu-id="ba3fa-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba3fa-108">Requirement</span></span> | <span data-ttu-id="ba3fa-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba3fa-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ba3fa-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba3fa-110">Minimum supported client</span></span><br/> | <span data-ttu-id="ba3fa-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba3fa-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ba3fa-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba3fa-112">Minimum supported server</span></span><br/> | <span data-ttu-id="ba3fa-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba3fa-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





