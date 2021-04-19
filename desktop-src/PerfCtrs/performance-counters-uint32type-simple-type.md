---
description: Définit un type d’entier non signé.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Type simple UInt32Type (compteurs de performance)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c32901167bcf181e5400ddb1d3b91ed7383965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518681"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="ee9af-103">Type simple UInt32Type (compteurs de performance)</span><span class="sxs-lookup"><span data-stu-id="ee9af-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="ee9af-104">Définit un type d’entier non signé.</span><span class="sxs-lookup"><span data-stu-id="ee9af-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="ee9af-105">Notes</span><span class="sxs-lookup"><span data-stu-id="ee9af-105">Remarks</span></span>

<span data-ttu-id="ee9af-106">Vous pouvez spécifier la valeur sous la forme d’un entier de 4 octets ou d’une valeur hexadécimale dans la plage comprise entre 0 et 4 294 967 295.</span><span class="sxs-lookup"><span data-stu-id="ee9af-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee9af-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee9af-107">Requirements</span></span>



| <span data-ttu-id="ee9af-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee9af-108">Requirement</span></span> | <span data-ttu-id="ee9af-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee9af-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee9af-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee9af-110">Minimum supported client</span></span><br/> | <span data-ttu-id="ee9af-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee9af-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee9af-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee9af-112">Minimum supported server</span></span><br/> | <span data-ttu-id="ee9af-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee9af-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




