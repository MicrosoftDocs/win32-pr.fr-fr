---
description: Nouveautés du Wi-Fi natif
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Nouveautés du Wi-Fi natif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126627f4cf6431fbac2bf4d1f6ec58561bfd8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521467"
---
# <a name="whats-new-in-native-wifi"></a><span data-ttu-id="d09f8-103">Nouveautés du Wi-Fi natif</span><span class="sxs-lookup"><span data-stu-id="d09f8-103">What's New in Native Wifi</span></span>

## <a name="windows-10-version-2004"></a><span data-ttu-id="d09f8-104">Windows 10, version 2004</span><span class="sxs-lookup"><span data-stu-id="d09f8-104">Windows 10, version 2004</span></span>

<span data-ttu-id="d09f8-105">Consultez [approvisionner un profil de Wi-Fi via un site Web](prov-wifi-profile-via-website.md).</span><span class="sxs-lookup"><span data-stu-id="d09f8-105">See [Provision a Wi-Fi profile via a website](prov-wifi-profile-via-website.md).</span></span>

## <a name="windows-10"></a><span data-ttu-id="d09f8-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d09f8-106">Windows 10</span></span>

<span data-ttu-id="d09f8-107">La prise en charge de hotspot 2,0 a été ajoutée au [ \_ schéma de profil WLAN](wlan-profileschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="d09f8-107">Support for Hotspot 2.0 has been added to the [WLAN\_profile schema](wlan-profileschema-schema.md).</span></span> <span data-ttu-id="d09f8-108">La zone réactive 2,0 permet la connexion automatique aux services de Wi-Fi publics à l’aide des informations d’identification existantes et de l’appartenance aux réseaux de fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="d09f8-108">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="d09f8-109">Les fournisseurs de services spécifient la façon dont les connexions sont établies à l’aide des nouveaux éléments de schéma pour décrire les réseaux à utiliser et comment s’y authentifier.</span><span class="sxs-lookup"><span data-stu-id="d09f8-109">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span> <span data-ttu-id="d09f8-110">Pour plus d’informations, consultez la documentation de l’élément [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d09f8-110">See the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element documentation for details.</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="d09f8-111">Windows 8 et Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d09f8-111">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="d09f8-112">Les fonctionnalités suivantes ont été ajoutées aux API WiFi natives sur Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="d09f8-112">The following features have been added to the Native Wifi APIs on Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="d09f8-113">Une fonctionnalité directe Wi-Fi basée sur le développement de la spécification technique d’égal à égal Wi-Fi v 1.1 par l’Alliance d' Wi-Fi (voir [spécifications publiées pour la Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="d09f8-113">A Wi-Fi Direct feature based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="d09f8-114">L’objectif de la spécification technique d’égal à égal Wi-Fi consiste à fournir une solution pour Wi-Fi la connectivité appareil-appareil sans avoir besoin d’un point d’accès sans fil (AP sans fil) pour configurer la connexion ou l’utilisation du mécanisme ad hoc (IBSS) Wi-Fi existant.</span><span class="sxs-lookup"><span data-stu-id="d09f8-114">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism.</span></span>

<span data-ttu-id="d09f8-115">Les fonctions suivantes prennent en charge la fonctionnalité Wi-Fi directe.</span><span class="sxs-lookup"><span data-stu-id="d09f8-115">The following functions support the Wi-Fi Direct feature.</span></span>

-   [<span data-ttu-id="d09f8-116">**\_rappel d’ouverture de session WFD \_ \_ terminé \_**</span><span class="sxs-lookup"><span data-stu-id="d09f8-116">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [<span data-ttu-id="d09f8-117">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="d09f8-117">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [<span data-ttu-id="d09f8-118">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="d09f8-118">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [<span data-ttu-id="d09f8-119">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="d09f8-119">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [<span data-ttu-id="d09f8-120">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="d09f8-120">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [<span data-ttu-id="d09f8-121">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="d09f8-121">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [<span data-ttu-id="d09f8-122">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="d09f8-122">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [<span data-ttu-id="d09f8-123">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="d09f8-123">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="d09f8-124">Windows 7 et Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d09f8-124">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="d09f8-125">Les fonctionnalités suivantes ont été ajoutées aux API WiFi natives sur Windows 7 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="d09f8-125">The following features have been added to the Native Wifi APIs on Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="d09f8-126">Le réseau hébergé sans fil permet à un seul adaptateur sans fil physique de se connecter en tant que client à un point d’accès matériel, tout en faisant office de point d’accès logiciel, ce qui permet à d’autres périphériques sans fil de s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="d09f8-126">The wireless Hosted Network allows a single physical wireless adapter to connect as a client to a hardware access point (AP), while at the same time acting as a software AP allowing other wireless-capable devices to connect to it.</span></span>

<span data-ttu-id="d09f8-127">Les fonctions suivantes prennent en charge la fonctionnalité de réseau hébergé sans fil.</span><span class="sxs-lookup"><span data-stu-id="d09f8-127">The following functions support the wireless Hosted Network feature.</span></span>

-   [<span data-ttu-id="d09f8-128">**WlanHostedNetworkForceStart**</span><span class="sxs-lookup"><span data-stu-id="d09f8-128">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [<span data-ttu-id="d09f8-129">**WlanHostedNetworkForceStop**</span><span class="sxs-lookup"><span data-stu-id="d09f8-129">**WlanHostedNetworkForceStop**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [<span data-ttu-id="d09f8-130">**WlanHostedNetworkInitSettings**</span><span class="sxs-lookup"><span data-stu-id="d09f8-130">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [<span data-ttu-id="d09f8-131">**WlanHostedNetworkQueryProperty**</span><span class="sxs-lookup"><span data-stu-id="d09f8-131">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [<span data-ttu-id="d09f8-132">**WlanHostedNetworkQuerySecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="d09f8-132">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [<span data-ttu-id="d09f8-133">**WlanHostedNetworkQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="d09f8-133">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [<span data-ttu-id="d09f8-134">**WlanHostedNetworkRefreshSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="d09f8-134">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [<span data-ttu-id="d09f8-135">**WlanHostedNetworkSetProperty**</span><span class="sxs-lookup"><span data-stu-id="d09f8-135">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [<span data-ttu-id="d09f8-136">**WlanHostedNetworkSetSecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="d09f8-136">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [<span data-ttu-id="d09f8-137">**WlanHostedNetworkStartUsing**</span><span class="sxs-lookup"><span data-stu-id="d09f8-137">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [<span data-ttu-id="d09f8-138">**WlanHostedNetworkStopUsing**</span><span class="sxs-lookup"><span data-stu-id="d09f8-138">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [<span data-ttu-id="d09f8-139">**WlanRegisterVirtualStationNotification**</span><span class="sxs-lookup"><span data-stu-id="d09f8-139">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

<span data-ttu-id="d09f8-140">Les nouvelles structures suivantes fonctionnent avec un réseau hébergé sans fil.</span><span class="sxs-lookup"><span data-stu-id="d09f8-140">The following new structures that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="d09f8-141">**\_paramètres de \_ \_ connexion réseau hébergée WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="d09f8-141">**WLAN\_HOSTED\_NETWORK\_CONNECTION\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [<span data-ttu-id="d09f8-142">**changement d’état de l' \_ \_ \_ homologue des données du réseau hébergé \_ \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="d09f8-142">**WLAN\_HOSTED\_NETWORK\_DATA\_PEER\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [<span data-ttu-id="d09f8-143">**\_État de \_ l' \_ homologue du réseau hébergé WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="d09f8-143">**WLAN\_HOSTED\_NETWORK\_PEER\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [<span data-ttu-id="d09f8-144">**\_ \_ État radio du réseau hébergé \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="d09f8-144">**WLAN\_HOSTED\_NETWORK\_RADIO\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [<span data-ttu-id="d09f8-145">**\_paramètres de \_ \_ sécurité réseau hébergés WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="d09f8-145">**WLAN\_HOSTED\_NETWORK\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [<span data-ttu-id="d09f8-146">**\_changement d' \_ État du réseau hébergé \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="d09f8-146">**WLAN\_HOSTED\_NETWORK\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [<span data-ttu-id="d09f8-147">**\_État du \_ réseau \_ hébergé WLAN**</span><span class="sxs-lookup"><span data-stu-id="d09f8-147">**WLAN\_HOSTED\_NETWORK\_STATUS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

<span data-ttu-id="d09f8-148">Les nouvelles énumérations suivantes fonctionnent avec un réseau hébergé sans fil.</span><span class="sxs-lookup"><span data-stu-id="d09f8-148">The following new enumerations that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="d09f8-149">**\_Code de \_ notification du réseau hébergé \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="d09f8-149">**WLAN\_HOSTED\_NETWORK\_NOTIFICATION\_CODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [<span data-ttu-id="d09f8-150">**\_OPCODE du \_ réseau \_ hébergé WLAN**</span><span class="sxs-lookup"><span data-stu-id="d09f8-150">**WLAN\_HOSTED\_NETWORK\_OPCODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [<span data-ttu-id="d09f8-151">**\_État d' \_ \_ authentification des homologues du réseau hébergé \_ WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="d09f8-151">**WLAN\_HOSTED\_NETWORK\_PEER\_AUTH\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [<span data-ttu-id="d09f8-152">**\_raison du \_ réseau \_ hébergé WLAN**</span><span class="sxs-lookup"><span data-stu-id="d09f8-152">**WLAN\_HOSTED\_NETWORK\_REASON**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [<span data-ttu-id="d09f8-153">**\_État du \_ réseau \_ hébergé WLAN**</span><span class="sxs-lookup"><span data-stu-id="d09f8-153">**WLAN\_HOSTED\_NETWORK\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a><span data-ttu-id="d09f8-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d09f8-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d09f8-155">À propos du réseau hébergé sans fil</span><span class="sxs-lookup"><span data-stu-id="d09f8-155">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="d09f8-156">Utilisation du partage de connexion Internet et d’un réseau hébergé sans fil</span><span class="sxs-lookup"><span data-stu-id="d09f8-156">Using Wireless Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



