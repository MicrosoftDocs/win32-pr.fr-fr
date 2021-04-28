---
description: Type simple UInt32Type (compteurs de performance)-définit un type entier non signé.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Type simple UInt32Type (compteurs de performance)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114577"
---
# <a name="uint32type-simple-type-performance-counters"></a><span data-ttu-id="b5f06-103">Type simple UInt32Type (compteurs de performance)</span><span class="sxs-lookup"><span data-stu-id="b5f06-103">UInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="b5f06-104">Définit un type d’entier non signé.</span><span class="sxs-lookup"><span data-stu-id="b5f06-104">Defines an unsigned integer type.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="b5f06-105">Notes </span><span class="sxs-lookup"><span data-stu-id="b5f06-105">Remarks</span></span>

<span data-ttu-id="b5f06-106">Vous pouvez spécifier la valeur sous la forme d’un entier de 4 octets ou d’une valeur hexadécimale dans la plage comprise entre 0 et 4 294 967 295.</span><span class="sxs-lookup"><span data-stu-id="b5f06-106">You can specify the value as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f06-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5f06-107">Requirements</span></span>



| <span data-ttu-id="b5f06-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5f06-108">Requirement</span></span> | <span data-ttu-id="b5f06-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5f06-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b5f06-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5f06-110">Minimum supported client</span></span><br/> | <span data-ttu-id="b5f06-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5f06-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b5f06-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5f06-112">Minimum supported server</span></span><br/> | <span data-ttu-id="b5f06-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5f06-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




