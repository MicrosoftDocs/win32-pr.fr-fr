---
description: Le \_ schéma de profil WLAN définit les éléments suivants.
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: Éléments de schéma WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752308"
---
# <a name="wlan_profile-schema-elements"></a><span data-ttu-id="36f3d-103">\_Éléments de schéma de profil WLAN</span><span class="sxs-lookup"><span data-stu-id="36f3d-103">WLAN\_profile Schema Elements</span></span>

<span data-ttu-id="36f3d-104">Le \_ schéma de profil WLAN définit les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="36f3d-104">The WLAN\_profile schema defines the following elements.</span></span> <span data-ttu-id="36f3d-105">La plupart des éléments se trouvent dans l’espace de noms `https://www.microsoft.com/networking/WLAN/profile/v1` , à l’exception de [**FipsMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), qui se trouve dans l’espace de noms `https://www.microsoft.com/networking/WLAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="36f3d-105">Most elements are in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`, except for [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), which is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v2`.</span></span>

<span data-ttu-id="36f3d-106">La liste suivante présente les éléments définis dans l’ordre dans lequel les éléments apparaissent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="36f3d-106">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="36f3d-107">L’ordre des éléments est appliqué.</span><span class="sxs-lookup"><span data-stu-id="36f3d-107">The ordering of elements is enforced.</span></span> <span data-ttu-id="36f3d-108">Tous les éléments ne se trouvent pas dans chaque profil, car certains éléments sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="36f3d-108">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="36f3d-109">Cette liste n’affiche pas tous les éléments possibles qui peuvent apparaître dans un profil sans fil, car des éléments peuvent être ajoutés dans **XS : n’importe quel** point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="36f3d-109">This list does not show all possible elements that can appear in a wireless profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="36f3d-110">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="36f3d-110">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
    -   [<span data-ttu-id="36f3d-111">**nom (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-111">**name (WLANProfile)**</span></span>](wlan-profileschema-name-wlanprofile-element.md)
    -   [<span data-ttu-id="36f3d-112">**SSIDConfig (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-112">**SSIDConfig (WLANProfile)**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [<span data-ttu-id="36f3d-113">**SSID (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-113">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [<span data-ttu-id="36f3d-114">**hex (SSID)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-114">**hex (SSID)**</span></span>](wlan-profileschema-hex-ssid-element.md)
            -   [<span data-ttu-id="36f3d-115">**nom (SSID)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-115">**name (SSID)**</span></span>](wlan-profileschema-name-ssid-element.md)
        -   [<span data-ttu-id="36f3d-116">**dédiffusion (SSIDConfig)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-116">**nonBroadcast (SSIDConfig)**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [<span data-ttu-id="36f3d-117">**Hotspot2 (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-117">**Hotspot2 (WLANProfile)**</span></span>](wlan-profileschema-hotspot2-element.md)
        -   [<span data-ttu-id="36f3d-118">**Nom_domaine (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-118">**DomainName (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-domainname-element.md)
        -   [<span data-ttu-id="36f3d-119">**NAIRealm (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-119">**NAIRealm (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [<span data-ttu-id="36f3d-120">**Network3GPP (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-120">**Network3GPP (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [<span data-ttu-id="36f3d-121">**RoamingConsortium (Hotspot2)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-121">**RoamingConsortium (Hotspot2)**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [<span data-ttu-id="36f3d-122">**connectionType (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-122">**connectionType (WLANProfile)**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [<span data-ttu-id="36f3d-123">**connectionMode (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-123">**connectionMode (WLANProfile)**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [<span data-ttu-id="36f3d-124">**AutoSwitch (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-124">**autoSwitch (WLANProfile)**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [<span data-ttu-id="36f3d-125">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
        -   [<span data-ttu-id="36f3d-126">**connectivité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-126">**connectivity (MSM)**</span></span>](wlan-profileschema-connectivity-msm-element.md)
            -   [<span data-ttu-id="36f3d-127">**phyType (connectivité)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-127">**phyType (connectivity)**</span></span>](wlan-profileschema-phytype-connectivity-element.md)
        -   [<span data-ttu-id="36f3d-128">**sécurité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-128">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
            -   [<span data-ttu-id="36f3d-129">**authEncryption (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-129">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
                -   [<span data-ttu-id="36f3d-130">**authentification (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-130">**authentication (authEncryption)**</span></span>](wlan-profileschema-authentication-authencryption-element.md)
                -   [<span data-ttu-id="36f3d-131">**chiffrement (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-131">**encryption (authEncryption)**</span></span>](wlan-profileschema-encryption-authencryption-element.md)
                -   [<span data-ttu-id="36f3d-132">**useOneX (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-132">**useOneX (authEncryption)**</span></span>](wlan-profileschema-useonex-authencryption-element.md)
                -   [<span data-ttu-id="36f3d-133">**FIPSMode (authEncryption)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-133">**FIPSMode (authEncryption)**</span></span>](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [<span data-ttu-id="36f3d-134">**sharedKey (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-134">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
                -   [<span data-ttu-id="36f3d-135">**KeyType (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-135">**keyType (sharedKey)**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)
                -   [<span data-ttu-id="36f3d-136">**protégé (sharedKey)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-136">**protected (sharedKey)**</span></span>](wlan-profileschema-protected-sharedkey-element.md)
                -   [<span data-ttu-id="36f3d-137">**Matériel de sharedKey**</span><span class="sxs-lookup"><span data-stu-id="36f3d-137">**keyMaterial (sharedKey)**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [<span data-ttu-id="36f3d-138">**KeyIndex (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-138">**keyIndex (security)**</span></span>](wlan-profileschema-keyindex-security-element.md)
            -   [<span data-ttu-id="36f3d-139">**PMKCacheMode (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-139">**PMKCacheMode (security)**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)
            -   [<span data-ttu-id="36f3d-140">**PMKCacheTTL (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-140">**PMKCacheTTL (security)**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)
            -   [<span data-ttu-id="36f3d-141">**PMKCacheSize (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-141">**PMKCacheSize (security)**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)
            -   [<span data-ttu-id="36f3d-142">**preAuthMode (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-142">**preAuthMode (security)**</span></span>](wlan-profileschema-preauthmode-security-element.md)
            -   [<span data-ttu-id="36f3d-143">**preAuthThrottle (sécurité)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-143">**preAuthThrottle (security)**</span></span>](wlan-profileschema-preauththrottle-security-element.md)
    -   [<span data-ttu-id="36f3d-144">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-144">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [<span data-ttu-id="36f3d-145">**OUIHeader (IHV)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-145">**OUIHeader (IHV)**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)
            -   [<span data-ttu-id="36f3d-146">**OUI (OUIHeader)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-146">**OUI (OUIHeader)**</span></span>](wlan-profileschema-oui-ouiheader-element.md)
            -   [<span data-ttu-id="36f3d-147">**type (OUIHeader)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-147">**type (OUIHeader)**</span></span>](wlan-profileschema-type-ouiheader-element.md)
        -   [<span data-ttu-id="36f3d-148">**connectivité (IHV)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-148">**connectivity (IHV)**</span></span>](wlan-profileschema-connectivity-ihv-element.md)
        -   [<span data-ttu-id="36f3d-149">**sécurité (IHV)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-149">**security (IHV)**</span></span>](wlan-profileschema-security-ihv-element.md)
        -   [<span data-ttu-id="36f3d-150">**useMSOneX (IHV)**</span><span class="sxs-lookup"><span data-stu-id="36f3d-150">**useMSOneX (IHV)**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)

 

 



