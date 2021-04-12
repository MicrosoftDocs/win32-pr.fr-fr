---
description: Spécifie si l’accès à tous les réseaux d’infrastructure est bloqué.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: Élément denyAllESS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201357"
---
# <a name="denyalless-networkfilter-element"></a><span data-ttu-id="4fbd4-103">Élément denyAllESS (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="4fbd4-103">denyAllESS (networkFilter) Element</span></span>

<span data-ttu-id="4fbd4-104">L’élément denyAllESS (networkFilter) spécifie si l’accès à tous les réseaux d’infrastructure est bloqué.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-104">The denyAllESS (networkFilter) element specifies if access to all infrastructure networks is blocked.</span></span> <span data-ttu-id="4fbd4-105">Lorsque **denyAllESS** a la valeur true, les machines ne peuvent pas se connecter à un réseau d’infrastructure ; dans le cas contraire, les machines peuvent se connecter à des réseaux d’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-105">When **denyAllESS** has a value of TRUE, machines cannot connect to an infrastructure network; otherwise, machines may connect to infrastructure networks.</span></span>

<span data-ttu-id="4fbd4-106">La valeur par défaut de cet élément est FALSe.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="4fbd4-107">Si **denyAllESS** n’est pas spécifié dans un profil, par défaut, les ordinateurs peuvent se connecter aux réseaux d’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-107">If **denyAllESS** is not specified in a profile, then by default machines may connect to infrastructure networks.</span></span>

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

<span data-ttu-id="4fbd4-108">L’élément **denyAllESS** est défini par l’élément [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4fbd4-108">The **denyAllESS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fbd4-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fbd4-109">Requirements</span></span>



| <span data-ttu-id="4fbd4-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fbd4-110">Requirement</span></span> | <span data-ttu-id="4fbd4-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fbd4-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4fbd4-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fbd4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4fbd4-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fbd4-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4fbd4-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fbd4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4fbd4-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fbd4-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4fbd4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fbd4-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="4fbd4-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="4fbd4-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4fbd4-118">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="4fbd4-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="4fbd4-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="4fbd4-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4fbd4-120">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="4fbd4-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




