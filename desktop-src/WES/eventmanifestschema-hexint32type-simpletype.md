---
title: Type simple UInt32Type (Journal des événements Windows)
description: Définit un type d’entier non signé.
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- Journal des types simples UInt32Type
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2a24326197c72b08032f5144fea1a69fbe68089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942078"
---
# <a name="uint32type-simple-type-windows-event-log"></a><span data-ttu-id="6f80c-104">Type simple UInt32Type (Journal des événements Windows)</span><span class="sxs-lookup"><span data-stu-id="6f80c-104">UInt32Type Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="6f80c-105">Définit un type d’entier non signé.</span><span class="sxs-lookup"><span data-stu-id="6f80c-105">Defines an unsigned integer type.</span></span> <span data-ttu-id="6f80c-106">La valeur peut être spécifiée sous la forme d’un entier de 4 octets ou d’une valeur hexadécimale dans la plage comprise entre 0 et 4 294 967 295.</span><span class="sxs-lookup"><span data-stu-id="6f80c-106">The value can be specified as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="6f80c-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f80c-107">Requirements</span></span>



| <span data-ttu-id="6f80c-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f80c-108">Requirement</span></span> | <span data-ttu-id="6f80c-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f80c-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6f80c-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f80c-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6f80c-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f80c-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6f80c-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f80c-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6f80c-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f80c-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





