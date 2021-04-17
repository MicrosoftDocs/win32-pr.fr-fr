---
description: En raison des différences architecturales sous-jacentes dans le système d’exploitation, Windows XP avec Service Pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec Service Pack 2 (SP2) prennent uniquement en charge un sous-ensemble des éléments décrits dans le \_ schéma de profil WLAN et la documentation de référence du schéma Onex.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Compatibilité avec le profil sans fil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e0eebfa627fb99d50490907108a2ddc7360202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529241"
---
# <a name="wireless-profile-compatibility"></a><span data-ttu-id="be8fe-103">Compatibilité avec le profil sans fil</span><span class="sxs-lookup"><span data-stu-id="be8fe-103">Wireless Profile Compatibility</span></span>

<span data-ttu-id="be8fe-104">En raison des différences architecturales sous-jacentes dans le système d’exploitation, Windows XP avec Service Pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec Service Pack 2 (SP2) prennent uniquement en charge un sous-ensemble des éléments décrits dans le [ \_ schéma de profil WLAN](wlan-profileschema-schema.md) et la documentation de référence du [schéma Onex](onexschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="be8fe-104">Because of underlying architectural differences in the operating system, Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) support only a subset of the elements described in the [WLAN\_profile Schema](wlan-profileschema-schema.md) and [OneX Schema](onexschema-schema.md) reference material.</span></span>

<span data-ttu-id="be8fe-105">Tous les profils conformes à la configuration requise pour Windows XP avec SP3 et l’API LAN sans fil pour Windows XP avec SP2 peuvent également être utilisés sur Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="be8fe-105">All profiles that conform to Windows XP with SP3 and Wireless LAN API for Windows XP with SP2 requirements can also be used on Windows Vista and Windows Server 2008.</span></span>

## <a name="wlan_profile-support"></a><span data-ttu-id="be8fe-106">\_Prise en charge du profil WLAN</span><span class="sxs-lookup"><span data-stu-id="be8fe-106">WLAN\_profile Support</span></span>

<span data-ttu-id="be8fe-107">Les éléments de profil WLAN suivants ne \_ sont pas pris en charge dans Windows XP avec SP3 ou l’API LAN sans fil pour Windows XP avec SP2 :</span><span class="sxs-lookup"><span data-stu-id="be8fe-107">The following WLAN\_profile elements are not supported in Windows XP with SP3 or Wireless LAN API for Windows XP with SP2:</span></span>

-   <span data-ttu-id="be8fe-108">connectivité (IHV)</span><span class="sxs-lookup"><span data-stu-id="be8fe-108">connectivity (IHV)</span></span>
-   <span data-ttu-id="be8fe-109">IHV (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="be8fe-109">IHV (WLANProfile)</span></span>
-   <span data-ttu-id="be8fe-110">OUI (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="be8fe-110">OUI (OUIHeader)</span></span>
-   <span data-ttu-id="be8fe-111">phyType (connectivité)</span><span class="sxs-lookup"><span data-stu-id="be8fe-111">phyType (connectivity)</span></span>
-   <span data-ttu-id="be8fe-112">PMKCacheMode (sécurité)</span><span class="sxs-lookup"><span data-stu-id="be8fe-112">PMKCacheMode (security)</span></span>
-   <span data-ttu-id="be8fe-113">PMKCacheSize (sécurité)</span><span class="sxs-lookup"><span data-stu-id="be8fe-113">PMKCacheSize (security)</span></span>
-   <span data-ttu-id="be8fe-114">PMKCacheTTL (sécurité)</span><span class="sxs-lookup"><span data-stu-id="be8fe-114">PMKCacheTTL (security)</span></span>
-   <span data-ttu-id="be8fe-115">preAuthMode (sécurité)</span><span class="sxs-lookup"><span data-stu-id="be8fe-115">preAuthMode (security)</span></span>
-   <span data-ttu-id="be8fe-116">preAuthThrottle (sécurité)</span><span class="sxs-lookup"><span data-stu-id="be8fe-116">preAuthThrottle (security)</span></span>
-   <span data-ttu-id="be8fe-117">sécurité (IHV)</span><span class="sxs-lookup"><span data-stu-id="be8fe-117">security (IHV)</span></span>
-   <span data-ttu-id="be8fe-118">type (OUIHeader)</span><span class="sxs-lookup"><span data-stu-id="be8fe-118">type (OUIHeader)</span></span>
-   <span data-ttu-id="be8fe-119">useMSOneX (IHV)</span><span class="sxs-lookup"><span data-stu-id="be8fe-119">useMSOneX (IHV)</span></span>

<span data-ttu-id="be8fe-120">Le tableau suivant présente les \_ éléments de profil WLAN avec des valeurs restreintes pour Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :</span><span class="sxs-lookup"><span data-stu-id="be8fe-120">The following table shows WLAN\_profile elements with constrained values for Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>



| <span data-ttu-id="be8fe-121">Élément</span><span class="sxs-lookup"><span data-stu-id="be8fe-121">Element</span></span>                                                                               | <span data-ttu-id="be8fe-122">Contrainte</span><span class="sxs-lookup"><span data-stu-id="be8fe-122">Constraint</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be8fe-123">**nom (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="be8fe-123">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)             | <span data-ttu-id="be8fe-124">L’élément Name est ignoré lorsque le profil est enregistré dans le magasin de profils.</span><span class="sxs-lookup"><span data-stu-id="be8fe-124">The name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="be8fe-125">Le nom du profil est dérivé automatiquement du SSID du réseau.</span><span class="sxs-lookup"><span data-stu-id="be8fe-125">The name of the profile is derived automatically from the SSID of the network.</span></span> <span data-ttu-id="be8fe-126">Pour les profils réseau d’infrastructure, le nom du profil correspond à l’identificateur SSID du réseau.</span><span class="sxs-lookup"><span data-stu-id="be8fe-126">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="be8fe-127">Pour les profils réseau ad hoc, le nom du profil correspond à l’identificateur SSID du réseau ad hoc suivi de `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="be8fe-127">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> |
| [<span data-ttu-id="be8fe-128">**protégé (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="be8fe-128">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)       | <span data-ttu-id="be8fe-129">Doit avoir la valeur FALSe.</span><span class="sxs-lookup"><span data-stu-id="be8fe-129">Must have a value of FALSE.</span></span>                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="be8fe-130">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="be8fe-130">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md) | <span data-ttu-id="be8fe-131">Limité à un seul élément [**SSID enfant (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="be8fe-131">Restricted to one child [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a><span data-ttu-id="be8fe-132">Prise en charge OneX</span><span class="sxs-lookup"><span data-stu-id="be8fe-132">OneX Support</span></span>

<span data-ttu-id="be8fe-133">Seul l’élément [**EAPConfig**](onexschema-eapconfig-onex-element.md) est pris en charge sur Windows XP avec SP3 et l’API LAN sans fil pour Windows XP avec SP2.</span><span class="sxs-lookup"><span data-stu-id="be8fe-133">Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="be8fe-134">Les autres éléments OneX, s’ils sont présents dans un profil, seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="be8fe-134">Other OneX elements, if present in a profile, will be ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be8fe-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be8fe-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be8fe-136">À propos de l’API WiFi Native</span><span class="sxs-lookup"><span data-stu-id="be8fe-136">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="be8fe-137">Prise en charge de l’API WiFi native sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="be8fe-137">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



