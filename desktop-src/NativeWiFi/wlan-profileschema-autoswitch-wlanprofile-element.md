---
description: Détermine le comportement d’itinérance d’un réseau connecté automatiquement lorsqu’un réseau plus préféré est à portée.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: AutoSwitch (WLANProfile) (élément)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863346"
---
# <a name="autoswitch-wlanprofile-element"></a><span data-ttu-id="882c8-103">AutoSwitch (WLANProfile) (élément)</span><span class="sxs-lookup"><span data-stu-id="882c8-103">autoSwitch (WLANProfile) Element</span></span>

<span data-ttu-id="882c8-104">L’élément AutoSwitch (WLANProfile) détermine le comportement d’itinérance d’un réseau connecté automatiquement lorsqu’un réseau plus préféré est à portée.</span><span class="sxs-lookup"><span data-stu-id="882c8-104">The autoSwitch (WLANProfile) element determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="882c8-105">.</span><span class="sxs-lookup"><span data-stu-id="882c8-105">.</span></span> <span data-ttu-id="882c8-106">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="882c8-106">This element is optional.</span></span>

<span data-ttu-id="882c8-107">Si AutoSwitch a la valeur « true » et que [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) est défini sur « auto », une connexion à un réseau plus favori doit être tentée chaque fois qu’un réseau préféré est mis en plage.</span><span class="sxs-lookup"><span data-stu-id="882c8-107">If autoSwitch is "true" and [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", a connection to a more preferred network must be attempted whenever a more preferred network comes into range.</span></span> <span data-ttu-id="882c8-108">Un réseau plus favori est un réseau qui est classé plus haut dans la liste des réseaux sans fil préférés.</span><span class="sxs-lookup"><span data-stu-id="882c8-108">A more preferred network is one that is ordered higher in the list of preferred wireless networks.</span></span> <span data-ttu-id="882c8-109">Cette tentative de connexion se produit lorsqu’elle est connectée à un autre réseau.</span><span class="sxs-lookup"><span data-stu-id="882c8-109">This connection attempt occurs when connected to another network.</span></span>

<span data-ttu-id="882c8-110">Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) a la valeur « auto », cette valeur peut être « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="882c8-110">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", this value can be either "true" or "false".</span></span>

<span data-ttu-id="882c8-111">Si [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) est défini sur « Manual », cette valeur doit être définie sur « false ».</span><span class="sxs-lookup"><span data-stu-id="882c8-111">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "manual", this value must be set to "false".</span></span> <span data-ttu-id="882c8-112">Cet élément n’a aucun effet sur un réseau connecté manuellement.</span><span class="sxs-lookup"><span data-stu-id="882c8-112">This element has no effect on a manually connected network.</span></span>

<span data-ttu-id="882c8-113">Une valeur de commutation automatique définie sur « true » entraîne une fréquence plus élevée d’analyse périodique des nouveaux réseaux.</span><span class="sxs-lookup"><span data-stu-id="882c8-113">An autoSwitch value set to "true" results in a higher frequency of periodic scanning for new networks.</span></span> <span data-ttu-id="882c8-114">Cela peut entraîner une pollution accrue de la fréquence radio par rapport à ces analyses périodiques et une consommation énergétique accrue utilisée par la carte réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="882c8-114">This may result in increased radio frequency pollution from these periodic scans and increased power consumption used by the wireless network adapter.</span></span>

<span data-ttu-id="882c8-115">**Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé :** Les modifications sont implémentées sur Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé pour optimiser les performances de mise en réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="882c8-115">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="882c8-116">Ces modifications sont conçues pour réduire la pollution de la fréquence radio, la consommation d’énergie et l’interruption du trafic en temps réel sur les réseaux sans fil.</span><span class="sxs-lookup"><span data-stu-id="882c8-116">These changes are designed to reduce radio frequency pollution, power consumption, and disruption to real-time traffic over wireless networks.</span></span> <span data-ttu-id="882c8-117">Le paramètre par défaut pour **AutoSwitch** lorsque cet élément n’est pas défini dans un profil de réseau local sans fil a changé.</span><span class="sxs-lookup"><span data-stu-id="882c8-117">The default setting for **autoSwitch** when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="882c8-118">La valeur par défaut est remplacée par la valeur « false » sur Windows 7 et Windows Server 2008 R2 avec le service de réseau local sans fil installé.</span><span class="sxs-lookup"><span data-stu-id="882c8-118">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="882c8-119">Le paramètre par défaut était « true » sur Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="882c8-119">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="882c8-120">Il est recommandé que la valeur de l’élément **AutoSwitch** utilisé par une application dans un profil de réseau local sans fil soit définie sur « false » pour réduire la fréquence de l’analyse périodique des nouveaux réseaux, à moins qu’il soit absolument nécessaire pour une application de définir cette valeur sur « true ».</span><span class="sxs-lookup"><span data-stu-id="882c8-120">It is recommended that the value of the **autoSwitch** element used by an application in a wireless LAN profile be set to "false" to reduce the frequency of periodic scanning for new networks, unless it is absolutely necessary for an application to set this value to "true".</span></span>

<span data-ttu-id="882c8-121">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="882c8-121">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

<span data-ttu-id="882c8-122">L’élément **AutoSwitch** est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="882c8-122">The **autoSwitch** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="882c8-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="882c8-123">Examples</span></span>

<span data-ttu-id="882c8-124">Pour afficher des exemples de profils qui utilisent l’élément **AutoSwitch** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="882c8-124">To view sample profiles that use the **autoSwitch** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="882c8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="882c8-125">Requirements</span></span>



| <span data-ttu-id="882c8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="882c8-126">Requirement</span></span> | <span data-ttu-id="882c8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="882c8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="882c8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="882c8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="882c8-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="882c8-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="882c8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="882c8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="882c8-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="882c8-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="882c8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="882c8-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="882c8-133">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="882c8-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="882c8-134">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="882c8-134">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="882c8-135">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="882c8-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="882c8-136">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="882c8-136">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




