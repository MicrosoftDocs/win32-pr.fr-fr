---
title: Type simple HexInt8Type
description: Définit un type hexadécimal sur 1 octet.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- Journal des types simples HexInt8Type
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466966"
---
# <a name="hexint8type-simple-type"></a><span data-ttu-id="9b5ea-104">Type simple HexInt8Type</span><span class="sxs-lookup"><span data-stu-id="9b5ea-104">HexInt8Type Simple Type</span></span>

<span data-ttu-id="9b5ea-105">Définit un type hexadécimal sur 1 octet.</span><span class="sxs-lookup"><span data-stu-id="9b5ea-105">Defines a 1-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="9b5ea-106">Modèles</span><span class="sxs-lookup"><span data-stu-id="9b5ea-106">Patterns</span></span>

<span data-ttu-id="9b5ea-107">Le type simple **HexInt8Type** est une [chaîne](/dotnet/api/system.string) qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="9b5ea-107">The **HexInt8Type** simple type is a [string](/dotnet/api/system.string) that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,2}`

    <span data-ttu-id="9b5ea-108">La valeur peut contenir de un à deux caractères hexadécimaux (par exemple, 0xA ou 0xac).</span><span class="sxs-lookup"><span data-stu-id="9b5ea-108">The value can contain from one to two hexadecimal characters (for example, 0xa or 0xac).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b5ea-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b5ea-109">Requirements</span></span>



| <span data-ttu-id="9b5ea-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b5ea-110">Requirement</span></span> | <span data-ttu-id="9b5ea-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b5ea-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9b5ea-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b5ea-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9b5ea-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b5ea-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9b5ea-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b5ea-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9b5ea-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b5ea-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

