---
title: Type simple HexInt64Type
description: Définit un type hexadécimal sur 8 octets. | Type simple HexInt64Type
ms.assetid: 2e81ec2b-cf67-42df-92a0-bf45b6dca051
keywords:
- Journal des types simples HexInt64Type
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8947e594bb067140510b0b5d2046a898018a291e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393940"
---
# <a name="hexint64type-simple-type"></a><span data-ttu-id="0e510-105">Type simple HexInt64Type</span><span class="sxs-lookup"><span data-stu-id="0e510-105">HexInt64Type Simple Type</span></span>

<span data-ttu-id="0e510-106">Définit un type hexadécimal sur 8 octets.</span><span class="sxs-lookup"><span data-stu-id="0e510-106">Defines an 8-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="0e510-107">Modèles</span><span class="sxs-lookup"><span data-stu-id="0e510-107">Patterns</span></span>

<span data-ttu-id="0e510-108">Le type simple **HexInt64Type** est une [chaîne](/dotnet/api/system.string) qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="0e510-108">The **HexInt64Type** simple type is a [string](/dotnet/api/system.string) that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,16}`

    <span data-ttu-id="0e510-109">La valeur peut contenir entre un et seize caractères hexadécimaux (par exemple, 0xA ou 0xac7bd361004fe190).</span><span class="sxs-lookup"><span data-stu-id="0e510-109">The value can contain from one to sixteen hexadecimal characters (for example, 0xa or 0xac7bd361004fe190).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e510-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e510-110">Requirements</span></span>



| <span data-ttu-id="0e510-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e510-111">Requirement</span></span> | <span data-ttu-id="0e510-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e510-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e510-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e510-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0e510-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e510-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e510-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e510-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0e510-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e510-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

