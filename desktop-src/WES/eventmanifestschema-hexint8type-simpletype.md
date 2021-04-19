---
title: Type simple UInt8Type
description: Définit un type d’octet non signé.
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- Journal des types simples UInt8Type
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3236d7416cbb199037813a8ae870d4f87718081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509101"
---
# <a name="uint8type-simple-type"></a><span data-ttu-id="fa0ee-104">Type simple UInt8Type</span><span class="sxs-lookup"><span data-stu-id="fa0ee-104">UInt8Type Simple Type</span></span>

<span data-ttu-id="fa0ee-105">Définit un type d’octet non signé.</span><span class="sxs-lookup"><span data-stu-id="fa0ee-105">Defines an unsigned byte type.</span></span> <span data-ttu-id="fa0ee-106">La valeur peut être spécifiée sous la forme d’un entier de 1 octet ou d’une valeur hexadécimale dans la plage comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="fa0ee-106">The value can be specified as a 1-byte integer or hexadecimal value in the range from 0 through 255.</span></span>

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="fa0ee-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa0ee-107">Requirements</span></span>



| <span data-ttu-id="fa0ee-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa0ee-108">Requirement</span></span> | <span data-ttu-id="fa0ee-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa0ee-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fa0ee-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa0ee-110">Minimum supported client</span></span><br/> | <span data-ttu-id="fa0ee-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa0ee-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fa0ee-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa0ee-112">Minimum supported server</span></span><br/> | <span data-ttu-id="fa0ee-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa0ee-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





