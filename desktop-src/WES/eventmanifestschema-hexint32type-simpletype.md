---
title: Type simple UInt32Type (Journal des événements Windows)
description: UInt32Type simple type (Journal des événements Windows)-définit un type d’entier non signé.
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
ms.openlocfilehash: 631bb3e8424db8a5d781aaa43df6096730aaa4d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090567"
---
# <a name="uint32type-simple-type-windows-event-log"></a><span data-ttu-id="39387-104">Type simple UInt32Type (Journal des événements Windows)</span><span class="sxs-lookup"><span data-stu-id="39387-104">UInt32Type Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="39387-105">Définit un type d’entier non signé.</span><span class="sxs-lookup"><span data-stu-id="39387-105">Defines an unsigned integer type.</span></span> <span data-ttu-id="39387-106">La valeur peut être spécifiée sous la forme d’un entier de 4 octets ou d’une valeur hexadécimale dans la plage comprise entre 0 et 4 294 967 295.</span><span class="sxs-lookup"><span data-stu-id="39387-106">The value can be specified as a 4-byte integer or hexadecimal value in the range from 0 through 4,294,967,295.</span></span>

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="39387-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39387-107">Requirements</span></span>



| <span data-ttu-id="39387-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39387-108">Requirement</span></span> | <span data-ttu-id="39387-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="39387-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="39387-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39387-110">Minimum supported client</span></span><br/> | <span data-ttu-id="39387-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39387-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="39387-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39387-112">Minimum supported server</span></span><br/> | <span data-ttu-id="39387-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39387-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





