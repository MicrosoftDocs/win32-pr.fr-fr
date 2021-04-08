---
title: Type simple UInt16Type
description: Définit un type short non signé.
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- Journal des types simples UInt16Type
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e687f42a43a12266267a0531ce078e8c6b5d1031
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743229"
---
# <a name="uint16type-simple-type"></a><span data-ttu-id="76e61-104">Type simple UInt16Type</span><span class="sxs-lookup"><span data-stu-id="76e61-104">UInt16Type Simple Type</span></span>

<span data-ttu-id="76e61-105">Définit un type short non signé.</span><span class="sxs-lookup"><span data-stu-id="76e61-105">Defines an unsigned short type.</span></span> <span data-ttu-id="76e61-106">La valeur peut être spécifiée sous la forme d’un entier sur 2 octets ou d’une valeur hexadécimale dans la plage comprise entre 0 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="76e61-106">The value can be specified as a 2-byte integer or hexadecimal value in the range from 0 through 65,535.</span></span>

``` syntax
<xs:simpleType name="UInt16Type">
    <xs:union
        memberValues="unsignedShort HexInt16Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="76e61-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76e61-107">Requirements</span></span>



| <span data-ttu-id="76e61-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76e61-108">Requirement</span></span> | <span data-ttu-id="76e61-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="76e61-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="76e61-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76e61-110">Minimum supported client</span></span><br/> | <span data-ttu-id="76e61-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76e61-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="76e61-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76e61-112">Minimum supported server</span></span><br/> | <span data-ttu-id="76e61-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76e61-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





