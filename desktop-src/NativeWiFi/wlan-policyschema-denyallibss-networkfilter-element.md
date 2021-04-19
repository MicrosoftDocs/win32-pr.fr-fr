---
description: Spécifie si l’accès à tous les réseaux ad hoc est bloqué.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: Élément denyAllIBSS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514414"
---
# <a name="denyallibss-networkfilter-element"></a><span data-ttu-id="43f09-103">Élément denyAllIBSS (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="43f09-103">denyAllIBSS (networkFilter) Element</span></span>

<span data-ttu-id="43f09-104">L’élément denyAllIBSS (networkFilter) spécifie si l’accès à tous les réseaux ad hoc est bloqué.</span><span class="sxs-lookup"><span data-stu-id="43f09-104">The denyAllIBSS (networkFilter) element specifies if access to all ad-hoc networks is blocked.</span></span> <span data-ttu-id="43f09-105">Lorsque **denyAllIBSS** a la valeur true, les machines ne peuvent pas se connecter à un réseau ad hoc. dans le cas contraire, les machines peuvent se connecter à des réseaux ad hoc.</span><span class="sxs-lookup"><span data-stu-id="43f09-105">When **denyAllIBSS** has a value of TRUE, machines cannot connect to an ad-hoc network; otherwise, machines may connect to ad-hoc networks.</span></span>

<span data-ttu-id="43f09-106">La valeur par défaut de cet élément est FALSe.</span><span class="sxs-lookup"><span data-stu-id="43f09-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="43f09-107">Si **denyAllIBSS** n’est pas spécifié dans un profil, par défaut, les ordinateurs peuvent se connecter à des réseaux ad hoc.</span><span class="sxs-lookup"><span data-stu-id="43f09-107">If **denyAllIBSS** is not specified in a profile, then by default machines may connect to ad-hoc networks.</span></span>

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

<span data-ttu-id="43f09-108">L’élément **denyAllIBSS** est défini par l’élément [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="43f09-108">The **denyAllIBSS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="43f09-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43f09-109">Requirements</span></span>



| <span data-ttu-id="43f09-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43f09-110">Requirement</span></span> | <span data-ttu-id="43f09-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="43f09-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="43f09-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43f09-112">Minimum supported client</span></span><br/> | <span data-ttu-id="43f09-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43f09-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="43f09-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43f09-114">Minimum supported server</span></span><br/> | <span data-ttu-id="43f09-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43f09-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43f09-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43f09-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="43f09-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="43f09-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="43f09-118">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="43f09-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="43f09-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="43f09-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="43f09-120">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="43f09-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




