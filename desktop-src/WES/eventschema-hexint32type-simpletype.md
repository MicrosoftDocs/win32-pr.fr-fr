---
title: Type simple HexInt32Type (schéma d’événement)
description: Définit un type hexadécimal sur 4 octets. | Type simple HexInt32Type (schéma d’événement)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
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
ms.openlocfilehash: 5c9bd7a11d0e648cc451ec837f0f8711ca334d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953620"
---
# <a name="hexint32type-simple-type-event-schema"></a><span data-ttu-id="85ba7-105">Type simple HexInt32Type (schéma d’événement)</span><span class="sxs-lookup"><span data-stu-id="85ba7-105">HexInt32Type Simple Type (Event Schema)</span></span>

<span data-ttu-id="85ba7-106">Définit un type hexadécimal sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="85ba7-106">Defines a 4-byte hexadecimal type.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="85ba7-107">Modèles</span><span class="sxs-lookup"><span data-stu-id="85ba7-107">Patterns</span></span>

<span data-ttu-id="85ba7-108">Le type simple **HexInt32Type** est une **chaîne** qui est limitée par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="85ba7-108">The **HexInt32Type** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `0[xX][0-9A-Fa-f]{1,8}`

    <span data-ttu-id="85ba7-109">La valeur peut contenir de un à huit caractères hexadécimaux (par exemple, 0xA ou 0xac7bd361).</span><span class="sxs-lookup"><span data-stu-id="85ba7-109">The value can contain from one to eight hexadecimal characters (for example, 0xa or 0xac7bd361).</span></span>

## <a name="requirements"></a><span data-ttu-id="85ba7-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85ba7-110">Requirements</span></span>



| <span data-ttu-id="85ba7-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85ba7-111">Requirement</span></span> | <span data-ttu-id="85ba7-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="85ba7-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="85ba7-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85ba7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="85ba7-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85ba7-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="85ba7-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85ba7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="85ba7-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85ba7-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





