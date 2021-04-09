---
description: Spécifie l’identificateur SSID (Service Set Identifier) d’un réseau sans fil.
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: Élément networkName (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: da635c392a29419e7b151cc2c4fb080ff7d3fca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867909"
---
# <a name="networkname-networkitemtype-element"></a><span data-ttu-id="7d029-103">Élément networkName (networkItemType)</span><span class="sxs-lookup"><span data-stu-id="7d029-103">networkName (networkItemType) Element</span></span>

<span data-ttu-id="7d029-104">L’élément networkName (networkItemType) spécifie l’identificateur SSID (Service Set Identifier) d’un réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="7d029-104">The networkName (networkItemType) element specifies the service set identifier (SSID) of a wireless network.</span></span>

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

<span data-ttu-id="7d029-105">L’élément **networkName** est défini par le type complexe [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7d029-105">The **networkName** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d029-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d029-106">Requirements</span></span>



| <span data-ttu-id="7d029-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d029-107">Requirement</span></span> | <span data-ttu-id="7d029-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d029-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7d029-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d029-109">Minimum supported client</span></span><br/> | <span data-ttu-id="7d029-110">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d029-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7d029-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d029-111">Minimum supported server</span></span><br/> | <span data-ttu-id="7d029-112">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d029-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d029-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d029-113">See also</span></span>

<dl> <dt>

<span data-ttu-id="7d029-114">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="7d029-114">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7d029-115">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="7d029-115">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="7d029-116">**Éléments parents immédiats possibles dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="7d029-116">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7d029-117">**réseau (allowList)**</span><span class="sxs-lookup"><span data-stu-id="7d029-117">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="7d029-118">**réseau (de blocage)**</span><span class="sxs-lookup"><span data-stu-id="7d029-118">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




