---
title: Type simple HexInt16Type
description: Définit un type hexadécimal sur 2 octets.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- Journal des types simples HexInt16Type
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6aaa5021fbc5a7de5c16083c0f7744bc4a154c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466606"
---
# <a name="hexint16type-simple-type"></a><span data-ttu-id="51038-104">Type simple HexInt16Type</span><span class="sxs-lookup"><span data-stu-id="51038-104">HexInt16Type Simple Type</span></span>

<span data-ttu-id="51038-105">Définit un type hexadécimal sur 2 octets.</span><span class="sxs-lookup"><span data-stu-id="51038-105">Defines a 2-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="51038-106">Modèles</span><span class="sxs-lookup"><span data-stu-id="51038-106">Patterns</span></span>

<span data-ttu-id="51038-107">Le type simple **HexInt16Type** est une **chaîne** qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="51038-107">The **HexInt16Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,4}`

    <span data-ttu-id="51038-108">La valeur peut contenir de un à quatre caractères hexadécimaux (par exemple, 0xA ou 0xac7b).</span><span class="sxs-lookup"><span data-stu-id="51038-108">The value can contain from one to four hexadecimal characters (for example, 0xa or 0xac7b).</span></span>

## <a name="requirements"></a><span data-ttu-id="51038-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51038-109">Requirements</span></span>



| <span data-ttu-id="51038-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51038-110">Requirement</span></span> | <span data-ttu-id="51038-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="51038-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51038-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51038-112">Minimum supported client</span></span><br/> | <span data-ttu-id="51038-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51038-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="51038-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51038-114">Minimum supported server</span></span><br/> | <span data-ttu-id="51038-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51038-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





