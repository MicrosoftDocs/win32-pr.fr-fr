---
description: Indique s’il faut se connecter à un réseau masqué.
ms.assetid: 31b859e9-adc7-49e2-91d9-4fb63a35addb
title: Élément SSIDConfig (unbroadcast)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nonBroadcast
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 695bede631b19c028a55a2f3ca82ba994ca12ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531827"
---
# <a name="nonbroadcast-ssidconfig-element"></a><span data-ttu-id="ee7c1-103">Élément SSIDConfig (unbroadcast)</span><span class="sxs-lookup"><span data-stu-id="ee7c1-103">nonBroadcast (SSIDConfig) Element</span></span>

<span data-ttu-id="ee7c1-104">L’élément non diffusion (SSIDConfig) indique s’il faut se connecter à un réseau masqué.</span><span class="sxs-lookup"><span data-stu-id="ee7c1-104">The nonBroadcast (SSIDConfig) element indicates whether to connect to a hidden network.</span></span> <span data-ttu-id="ee7c1-105">Si un réseau ne diffuse pas son SSID, il s’agit d’un réseau masqué.</span><span class="sxs-lookup"><span data-stu-id="ee7c1-105">If a network does not broadcast its SSID, then it is known as a hidden network.</span></span> <span data-ttu-id="ee7c1-106">Si plusieurs SSID sont définis dans le profil, ils doivent tous avoir la même valeur de dédiffusion.</span><span class="sxs-lookup"><span data-stu-id="ee7c1-106">If multiple SSIDs are set within the profile, they must all have the same nonBroadcast value.</span></span>

<span data-ttu-id="ee7c1-107">Si [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) a la valeur **ESS**, cette valeur peut être « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="ee7c1-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **ESS**, this value can be either "true" or "false".</span></span> <span data-ttu-id="ee7c1-108">Si cet élément n’est pas présent, la valeur par défaut est « false ».</span><span class="sxs-lookup"><span data-stu-id="ee7c1-108">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="ee7c1-109">Si [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) est défini sur **IBSS**, cette valeur doit être « false ».</span><span class="sxs-lookup"><span data-stu-id="ee7c1-109">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to **IBSS**, this value must be "false".</span></span> <span data-ttu-id="ee7c1-110">Si cet élément n’est pas présent, la valeur par défaut est « false ».</span><span class="sxs-lookup"><span data-stu-id="ee7c1-110">If this element is not present, the default value is "false".</span></span>

<span data-ttu-id="ee7c1-111">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ee7c1-111">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="nonBroadcast"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="ee7c1-112">L’élément est défini par l’élément [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ee7c1-112">The element is defined by the [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="ee7c1-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="ee7c1-113">Examples</span></span>

<span data-ttu-id="ee7c1-114">Pour afficher un exemple de profil qui utilise l’élément non **Broadcast** , consultez [exemple de profil de non-diffusion](non-broadcast-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ee7c1-114">To view a sample profile that uses the **nonBroadcast** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee7c1-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee7c1-115">Requirements</span></span>



| <span data-ttu-id="ee7c1-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee7c1-116">Requirement</span></span> | <span data-ttu-id="ee7c1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee7c1-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee7c1-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee7c1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee7c1-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee7c1-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee7c1-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee7c1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee7c1-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee7c1-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee7c1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee7c1-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee7c1-123">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="ee7c1-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ee7c1-124">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="ee7c1-124">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="ee7c1-125">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="ee7c1-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ee7c1-126">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ee7c1-126">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




