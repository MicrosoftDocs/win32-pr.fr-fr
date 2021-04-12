---
description: Un sous-ensemble de la fonctionnalité de l’API WiFi native est pris en charge sur Windows XP avec Service Pack 2 (SP2) et Windows XP avec Service Pack 3 (SP3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Prise en charge de l’API WiFi native sur Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319381"
---
# <a name="native-wifi-api-support-on-windows-xp"></a><span data-ttu-id="d1196-103">Prise en charge de l’API WiFi native sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="d1196-103">Native Wifi API Support on Windows XP</span></span>

<span data-ttu-id="d1196-104">Un sous-ensemble de la fonctionnalité de l’API WiFi native est pris en charge sur Windows XP avec Service Pack 2 (SP2) et Windows XP avec Service Pack 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="d1196-104">A subset of the Native Wifi API functionality is supported on Windows XP with Service Pack 2 (SP2) and Windows XP with Service Pack 3 (SP3).</span></span> <span data-ttu-id="d1196-105">Cette fonctionnalité est incluse dans Windows XP avec SP3 par défaut.</span><span class="sxs-lookup"><span data-stu-id="d1196-105">This functionality is included in Windows XP with SP3 by default.</span></span> <span data-ttu-id="d1196-106">Dans Windows XP avec SP2, cette fonctionnalité peut être ajoutée en appliquant un correctif, connu sous le nom d’API de réseau local sans fil pour Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="d1196-106">In Windows XP with SP2, this functionality can be added by applying a hotfix, which is known as Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="d1196-107">Pour plus d’informations ou pour télécharger le correctif logiciel, consultez la rubrique « les développeurs ne peuvent pas créer de programmes clients sans fil qui gèrent des profils sans fil et des connexions sur le service de configuration sans fil sans fil dans Microsoft Windows XP Service Pack 2 (SP2) » dans la base de connaissances d’aide et de support à l’adresse [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .</span><span class="sxs-lookup"><span data-stu-id="d1196-107">For more information or to download the hotfix, see "Developers cannot create wireless client programs that manage wireless profiles and connections over the Wireless Zero Configuration service in Microsoft Windows XP Service Pack 2 (SP2)" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997).</span></span>

<span data-ttu-id="d1196-108">En raison des différences architecturales sous-jacentes dans Windows XP, l’API WiFi native sur présente certaines limites.</span><span class="sxs-lookup"><span data-stu-id="d1196-108">Because of underlying architectural differences in Windows XP, the Native Wifi API on has some limitations.</span></span> <span data-ttu-id="d1196-109">Voici une liste de limitations :</span><span class="sxs-lookup"><span data-stu-id="d1196-109">Here is a list of limitations:</span></span>

-   <span data-ttu-id="d1196-110">Au plus un SSID peut être associé à un profil.</span><span class="sxs-lookup"><span data-stu-id="d1196-110">At most one SSID can be associated with a profile.</span></span>
-   <span data-ttu-id="d1196-111">Les réseaux d’infrastructure apparaissent toujours avant les réseaux ad hoc dans la liste des profils.</span><span class="sxs-lookup"><span data-stu-id="d1196-111">Infrastructure networks always appear before ad hoc networks in the profile list.</span></span>
-   <span data-ttu-id="d1196-112">Les noms de profil sont dérivés du SSID et ne peuvent pas être définis par l’utilisateur sur une chaîne arbitraire.</span><span class="sxs-lookup"><span data-stu-id="d1196-112">Profile names are derived from the SSID, and cannot be set by the user to an arbitrary string.</span></span>
-   <span data-ttu-id="d1196-113">Les types PHY ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d1196-113">PHY types are not supported.</span></span>
-   <span data-ttu-id="d1196-114">La mise en cache de la clé PMK (Pairwise Master Key) n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d1196-114">Pairwise master key (PMK) caching is not supported.</span></span>
-   <span data-ttu-id="d1196-115">Les fonctions d’extensibilité du fournisseur de matériel indépendant (IHV) ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d1196-115">Independent hardware vendor (IHV) extensibility functions are not supported.</span></span>
-   <span data-ttu-id="d1196-116">Les autorisations de profil ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d1196-116">Profile permissions are not supported.</span></span>
-   <span data-ttu-id="d1196-117">Seule la \_ connexion ACM de notification WLAN \_ \_ \_ est terminée et \_ les \_ notifications d’accès hors connexion ACM de notification WLAN \_ sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="d1196-117">Only the wlan\_notification\_acm\_connection\_complete and the wlan\_notification\_acm\_disconnected notifications are available.</span></span>
-   <span data-ttu-id="d1196-118">Les paramètres globaux de configuration 802.1 X et EAPOL ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d1196-118">Global 802.1X and EAPOL configuration settings are not supported.</span></span>

<span data-ttu-id="d1196-119">Les fonctions suivantes sont prises en charge par Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :</span><span class="sxs-lookup"><span data-stu-id="d1196-119">The following functions are supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>

-   [<span data-ttu-id="d1196-120">**\_rappel de notification WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="d1196-120">**WLAN\_NOTIFICATION\_CALLBACK**</span></span>](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [<span data-ttu-id="d1196-121">**WlanAllocateMemory**</span><span class="sxs-lookup"><span data-stu-id="d1196-121">**WlanAllocateMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [<span data-ttu-id="d1196-122">**WlanCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="d1196-122">**WlanCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [<span data-ttu-id="d1196-123">**WlanConnect**</span><span class="sxs-lookup"><span data-stu-id="d1196-123">**WlanConnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [<span data-ttu-id="d1196-124">**WlanDeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="d1196-124">**WlanDeleteProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [<span data-ttu-id="d1196-125">**WlanDisconnect**</span><span class="sxs-lookup"><span data-stu-id="d1196-125">**WlanDisconnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [<span data-ttu-id="d1196-126">**WlanEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="d1196-126">**WlanEnumInterfaces**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [<span data-ttu-id="d1196-127">**WlanFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="d1196-127">**WlanFreeMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [<span data-ttu-id="d1196-128">**WlanGetAvailableNetworkList**</span><span class="sxs-lookup"><span data-stu-id="d1196-128">**WlanGetAvailableNetworkList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [<span data-ttu-id="d1196-129">**WlanGetProfile**</span><span class="sxs-lookup"><span data-stu-id="d1196-129">**WlanGetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [<span data-ttu-id="d1196-130">**WlanGetProfileList**</span><span class="sxs-lookup"><span data-stu-id="d1196-130">**WlanGetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [<span data-ttu-id="d1196-131">**WlanOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="d1196-131">**WlanOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [<span data-ttu-id="d1196-132">**WlanQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="d1196-132">**WlanQueryInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [<span data-ttu-id="d1196-133">**WlanReasonCodeToString**</span><span class="sxs-lookup"><span data-stu-id="d1196-133">**WlanReasonCodeToString**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [<span data-ttu-id="d1196-134">**WlanRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="d1196-134">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [<span data-ttu-id="d1196-135">**WlanScan**</span><span class="sxs-lookup"><span data-stu-id="d1196-135">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [<span data-ttu-id="d1196-136">**WlanSetInterface**</span><span class="sxs-lookup"><span data-stu-id="d1196-136">**WlanSetInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [<span data-ttu-id="d1196-137">**WlanSetProfile**</span><span class="sxs-lookup"><span data-stu-id="d1196-137">**WlanSetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [<span data-ttu-id="d1196-138">**WlanSetProfileEapXmlUserData**</span><span class="sxs-lookup"><span data-stu-id="d1196-138">**WlanSetProfileEapXmlUserData**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [<span data-ttu-id="d1196-139">**WlanSetProfileList**</span><span class="sxs-lookup"><span data-stu-id="d1196-139">**WlanSetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [<span data-ttu-id="d1196-140">**WlanSetProfilePosition**</span><span class="sxs-lookup"><span data-stu-id="d1196-140">**WlanSetProfilePosition**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a><span data-ttu-id="d1196-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1196-141">Related topics</span></span>

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[<span data-ttu-id="d1196-142">À propos de la WiFi Native</span><span class="sxs-lookup"><span data-stu-id="d1196-142">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 
