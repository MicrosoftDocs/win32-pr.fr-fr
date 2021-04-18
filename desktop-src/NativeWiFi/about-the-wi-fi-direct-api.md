---
description: L’API WiFi Native contient un ensemble de fonctions qui prennent en charge l’utilisation de Wi-Fi directe pour les applications de bureau.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: À propos de la fonctionnalité Wi-Fi directe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e503cb2bf86f81904b1c85c2bdf96b66c0762e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519549"
---
# <a name="about-the-wi-fi-direct-feature"></a><span data-ttu-id="82c7f-103">À propos de la fonctionnalité Wi-Fi directe</span><span class="sxs-lookup"><span data-stu-id="82c7f-103">About the Wi-Fi Direct feature</span></span>

<span data-ttu-id="82c7f-104">L’API WiFi Native contient un ensemble de fonctions qui prennent en charge l’utilisation de Wi-Fi directe pour les applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="82c7f-104">The Native Wifi API contains a set of functions that support the use of Wi-Fi Direct for desktop apps.</span></span> <span data-ttu-id="82c7f-105">À compter de Windows 8 et de Windows Server 2012, Wi-Fi fonctions directes ont été ajoutées à l’API WiFi native.</span><span class="sxs-lookup"><span data-stu-id="82c7f-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="82c7f-106">La fonctionnalité de Wi-Fi directe est basée sur le développement de la Wi-Fi spécifications techniques d’égal à égal v 1.1 par le Wi-Fi Alliance (voir [spécifications de Wi-Fi Alliance publiées](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="82c7f-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="82c7f-107">L’objectif de la spécification technique d’égal à égal Wi-Fi consiste à fournir une solution pour Wi-Fi la connectivité appareil-appareil sans avoir besoin d’un point d’accès sans fil (AP sans fil) pour configurer la connexion ou l’utilisation du mécanisme existant Wi-Fi ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="82c7f-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="82c7f-108">Le mode ad hoc n’est peut-être pas disponible dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="82c7f-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="82c7f-109">À partir de Windows 8.1 et de Windows Server 2012 R2, utilisez Wi-Fi direct à la place.</span><span class="sxs-lookup"><span data-stu-id="82c7f-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="82c7f-110">Pour une application de bureau, la fonctionnalité de Wi-Fi directe requiert que les appareils Wi-FI direct soient déjà associés par l’utilisateur à l’interface utilisateur expérience de couplage Windows.</span><span class="sxs-lookup"><span data-stu-id="82c7f-110">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="82c7f-111">Une fois cette association terminée, un profil est stocké, ce qui permet au Wi-Fi fonctions directes d’être utilisées pour démarrer une session Wi-Fi directe afin d’établir une connexion entre les Wi-Fi les appareils directs.</span><span class="sxs-lookup"><span data-stu-id="82c7f-111">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="82c7f-112">Les fonctions suivantes prennent en charge la fonctionnalité Wi-Fi directe.</span><span class="sxs-lookup"><span data-stu-id="82c7f-112">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="82c7f-113">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : indique que l’application souhaite annuler une fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) en attente qui n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="82c7f-113">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="82c7f-114">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : ferme un handle vers le service Wi-Fi direct.</span><span class="sxs-lookup"><span data-stu-id="82c7f-114">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="82c7f-115">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : ferme une session après un appel précédemment réussi à la fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .</span><span class="sxs-lookup"><span data-stu-id="82c7f-115">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="82c7f-116">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : ouvre un handle vers le service Wi-Fi direct et négocie une version de l’API Wi-Fi direct à utiliser.</span><span class="sxs-lookup"><span data-stu-id="82c7f-116">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="82c7f-117">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : récupère et applique un profil stocké pour une Wi-Fi appareil hérité direct.</span><span class="sxs-lookup"><span data-stu-id="82c7f-117">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="82c7f-118">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : démarre une connexion à la demande à un appareil spécifique Wi-Fi direct, qui a été précédemment associé à l’expérience de couplage Windows.</span><span class="sxs-lookup"><span data-stu-id="82c7f-118">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="82c7f-119">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : met à jour la visibilité de l’appareil pour le Wi-Fi adresse directe de l’appareil pour un nœud d’appareil Wi-Fi installé spécifique installé.</span><span class="sxs-lookup"><span data-stu-id="82c7f-119">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="82c7f-120">[**WFD \_ OUVERTURE d’une \_ session \_ complète \_ callback**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : définit la fonction de rappel qui est appelée par la fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) lorsque l’opération **WFDStartOpenSession** est terminée.</span><span class="sxs-lookup"><span data-stu-id="82c7f-120">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="82c7f-121">Pour plus d’informations sur l’utilisation de Wi-Fi direct dans une application de bureau, consultez [utilisation des fonctions directes Wi-Fi](using-the-wi-fi-direct-api.md).</span><span class="sxs-lookup"><span data-stu-id="82c7f-121">For more information on using Wi-Fi Direct in a desktop app, see [Using the Wi-Fi Direct functions](using-the-wi-fi-direct-api.md).</span></span>

<span data-ttu-id="82c7f-122">Pour plus d’informations sur Wi-Fi directe pour une utilisation dans les applications du Windows Store, consultez [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) et les classes associées dans l’espace de noms [**Windows. Networking. proximite**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="82c7f-122">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82c7f-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82c7f-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="82c7f-124">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="82c7f-124">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="82c7f-125">À propos de la WiFi Native</span><span class="sxs-lookup"><span data-stu-id="82c7f-125">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="82c7f-126">À propos de l’API WiFi Native</span><span class="sxs-lookup"><span data-stu-id="82c7f-126">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="82c7f-127">À propos de l’API ad hoc sans fil</span><span class="sxs-lookup"><span data-stu-id="82c7f-127">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="82c7f-128">Utilisation des fonctions Wi-Fi direct</span><span class="sxs-lookup"><span data-stu-id="82c7f-128">Using the Wi-Fi Direct functions</span></span>](using-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="82c7f-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="82c7f-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="82c7f-130">**PeerFinder**</span><span class="sxs-lookup"><span data-stu-id="82c7f-130">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="82c7f-131">**\_rappel d’ouverture de session WFD \_ \_ terminé \_**</span><span class="sxs-lookup"><span data-stu-id="82c7f-131">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="82c7f-132">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="82c7f-132">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="82c7f-133">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="82c7f-133">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="82c7f-134">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="82c7f-134">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="82c7f-135">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="82c7f-135">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="82c7f-136">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="82c7f-136">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="82c7f-137">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="82c7f-137">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="82c7f-138">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="82c7f-138">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="82c7f-139">**Windows.Networking.Proximity**</span><span class="sxs-lookup"><span data-stu-id="82c7f-139">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
