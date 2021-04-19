---
description: Définit un type hexadécimal sur 4 octets.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: Type simple HexInt32Type (compteurs de performance)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518476"
---
# <a name="hexint32type-simple-type-performance-counters"></a><span data-ttu-id="fe940-103">Type simple HexInt32Type (compteurs de performance)</span><span class="sxs-lookup"><span data-stu-id="fe940-103">HexInt32Type Simple Type (Performance Counters)</span></span>

<span data-ttu-id="fe940-104">Définit un type hexadécimal sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="fe940-104">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="fe940-105">Modèles</span><span class="sxs-lookup"><span data-stu-id="fe940-105">Patterns</span></span>

<span data-ttu-id="fe940-106">Le type simple **HexInt32Type** est un **XS : String** qui est limité par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="fe940-106">The **HexInt32Type** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="fe940-107">La valeur peut contenir de un à huit caractères hexadécimaux (par exemple, 0xA ou 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="fe940-107">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe940-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe940-108">Requirements</span></span>



| <span data-ttu-id="fe940-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe940-109">Requirement</span></span> | <span data-ttu-id="fe940-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe940-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fe940-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe940-111">Minimum supported client</span></span><br/> | <span data-ttu-id="fe940-112">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe940-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fe940-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe940-113">Minimum supported server</span></span><br/> | <span data-ttu-id="fe940-114">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe940-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




