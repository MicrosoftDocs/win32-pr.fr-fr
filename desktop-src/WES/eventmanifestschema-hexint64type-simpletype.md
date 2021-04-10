---
title: Type simple UInt64Type (schéma EventManifest)
description: Définit un type long non signé.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- Journal des types simples UInt64Type
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b375a8e452760f9e59bae9cae8449889483d9b4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032814"
---
# <a name="uint64type-simple-type"></a><span data-ttu-id="d705d-104">Type simple UInt64Type</span><span class="sxs-lookup"><span data-stu-id="d705d-104">UInt64Type Simple Type</span></span>

<span data-ttu-id="d705d-105">Définit un type long non signé.</span><span class="sxs-lookup"><span data-stu-id="d705d-105">Defines an unsigned long type.</span></span> <span data-ttu-id="d705d-106">La valeur peut être spécifiée sous la forme d’un entier de 8 octets ou d’une valeur hexadécimale dans la plage comprise entre 0 et 18446744073709551615.</span><span class="sxs-lookup"><span data-stu-id="d705d-106">The value can be specified as an 8-byte integer or hexadecimal value in the range from 0 through 18,446,744,073,709,551,615.</span></span>

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="d705d-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d705d-107">Requirements</span></span>



| <span data-ttu-id="d705d-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d705d-108">Requirement</span></span> | <span data-ttu-id="d705d-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="d705d-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d705d-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d705d-110">Minimum supported client</span></span><br/> | <span data-ttu-id="d705d-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d705d-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d705d-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d705d-112">Minimum supported server</span></span><br/> | <span data-ttu-id="d705d-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d705d-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





