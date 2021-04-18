---
description: Spécifie un type de réseau.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Élément networkType (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519507"
---
# <a name="networktype-networkitemtype-element"></a><span data-ttu-id="a563b-103">Élément networkType (networkItemType)</span><span class="sxs-lookup"><span data-stu-id="a563b-103">networkType (networkItemType) Element</span></span>

<span data-ttu-id="a563b-104">L’élément networkType (networkItemType) spécifie un type de réseau.</span><span class="sxs-lookup"><span data-stu-id="a563b-104">The networkType (networkItemType) element specifies a network type.</span></span> <span data-ttu-id="a563b-105">Il existe deux types de réseaux : les réseaux d’infrastructure (ESS) et les réseaux ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="a563b-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

<span data-ttu-id="a563b-106">L’élément **networkType** est défini par le type complexe [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a563b-106">The **networkType** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a563b-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a563b-107">Requirements</span></span>



| <span data-ttu-id="a563b-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a563b-108">Requirement</span></span> | <span data-ttu-id="a563b-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a563b-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a563b-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a563b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a563b-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a563b-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a563b-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a563b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a563b-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a563b-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a563b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a563b-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="a563b-115">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="a563b-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a563b-116">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="a563b-116">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="a563b-117">**Éléments parents immédiats possibles dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="a563b-117">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a563b-118">**réseau (allowList)**</span><span class="sxs-lookup"><span data-stu-id="a563b-118">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="a563b-119">**réseau (de blocage)**</span><span class="sxs-lookup"><span data-stu-id="a563b-119">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




