---
title: Type simple HexInt32Type (schéma EventManifest)
description: Définit un type hexadécimal sur 4 octets. | Type simple HexInt32Type (schéma EventManifest)
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
keywords:
- Journal des types simples HexInt32Type
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4630bc4d7d513a0fedad2191c63ca71571ce655a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522308"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a><span data-ttu-id="03d3c-105">Type simple HexInt32Type (schéma EventManifest)</span><span class="sxs-lookup"><span data-stu-id="03d3c-105">HexInt32Type Simple Type (EventManifest Schema)</span></span>

<span data-ttu-id="03d3c-106">Définit un type hexadécimal sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="03d3c-106">Defines a 4-byte hexadecimal type.</span></span>

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="03d3c-107">Modèles</span><span class="sxs-lookup"><span data-stu-id="03d3c-107">Patterns</span></span>

<span data-ttu-id="03d3c-108">Le type simple **HexInt32Type** est une **chaîne** qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="03d3c-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="03d3c-109">La valeur peut contenir de un à huit caractères hexadécimaux (par exemple, 0xA ou 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="03d3c-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="03d3c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03d3c-110">Requirements</span></span>



| <span data-ttu-id="03d3c-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03d3c-111">Requirement</span></span> | <span data-ttu-id="03d3c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="03d3c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="03d3c-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03d3c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="03d3c-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03d3c-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="03d3c-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03d3c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="03d3c-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03d3c-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





