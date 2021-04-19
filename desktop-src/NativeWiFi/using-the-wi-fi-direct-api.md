---
description: Montre comment utiliser Wi-Fi fonctions directes dans les applications de bureau.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Utilisation des fonctions Wi-Fi direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8850f5b278a158e32f78118cf5d0d408c123192e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519687"
---
# <a name="using-the-wi-fi-direct-functions"></a><span data-ttu-id="cacf7-103">Utilisation des fonctions Wi-Fi direct</span><span class="sxs-lookup"><span data-stu-id="cacf7-103">Using the Wi-Fi Direct functions</span></span>

<span data-ttu-id="cacf7-104">Cette rubrique montre comment utiliser Wi-Fi fonctions directes dans les applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="cacf7-104">This topics shows how to use Wi-Fi Direct functions in desktop apps.</span></span> <span data-ttu-id="cacf7-105">À compter de Windows 8 et de Windows Server 2012, Wi-Fi fonctions directes ont été ajoutées à l’API WiFi native.</span><span class="sxs-lookup"><span data-stu-id="cacf7-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="cacf7-106">La fonctionnalité de Wi-Fi directe est basée sur le développement de la Wi-Fi spécifications techniques d’égal à égal v 1.1 par le Wi-Fi Alliance (voir [spécifications de Wi-Fi Alliance publiées](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="cacf7-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="cacf7-107">L’objectif de la spécification technique d’égal à égal Wi-Fi consiste à fournir une solution pour Wi-Fi la connectivité appareil-appareil sans avoir besoin d’un point d’accès sans fil (AP sans fil) pour configurer la connexion ou l’utilisation du mécanisme existant Wi-Fi ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="cacf7-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="cacf7-108">Le mode ad hoc n’est peut-être pas disponible dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="cacf7-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="cacf7-109">À partir de Windows 8.1 et de Windows Server 2012 R2, utilisez Wi-Fi direct à la place.</span><span class="sxs-lookup"><span data-stu-id="cacf7-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="cacf7-110">Les fonctions suivantes prennent en charge la fonctionnalité Wi-Fi directe.</span><span class="sxs-lookup"><span data-stu-id="cacf7-110">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="cacf7-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : indique que l’application souhaite annuler une fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) en attente qui n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="cacf7-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="cacf7-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : ferme un handle vers le service Wi-Fi direct.</span><span class="sxs-lookup"><span data-stu-id="cacf7-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="cacf7-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : ferme une session après un appel précédemment réussi à la fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .</span><span class="sxs-lookup"><span data-stu-id="cacf7-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="cacf7-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : ouvre un handle vers le service Wi-Fi direct et négocie une version de l’API Wi-Fi direct à utiliser.</span><span class="sxs-lookup"><span data-stu-id="cacf7-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="cacf7-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : récupère et applique un profil stocké pour une Wi-Fi appareil hérité direct.</span><span class="sxs-lookup"><span data-stu-id="cacf7-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="cacf7-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : démarre une connexion à la demande à un appareil spécifique Wi-Fi direct, qui a été précédemment associé à l’expérience de couplage Windows.</span><span class="sxs-lookup"><span data-stu-id="cacf7-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="cacf7-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : met à jour la visibilité de l’appareil pour le Wi-Fi adresse directe de l’appareil pour un nœud d’appareil Wi-Fi installé spécifique installé.</span><span class="sxs-lookup"><span data-stu-id="cacf7-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="cacf7-118">[**WFD \_ OUVERTURE d’une \_ session \_ complète \_ callback**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : définit la fonction de rappel qui est appelée par la fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) lorsque l’opération **WFDStartOpenSession** est terminée.</span><span class="sxs-lookup"><span data-stu-id="cacf7-118">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="cacf7-119">Pour une application de bureau, la fonctionnalité de Wi-Fi directe requiert que les appareils Wi-FI direct soient déjà associés par l’utilisateur à l’interface utilisateur expérience de couplage Windows.</span><span class="sxs-lookup"><span data-stu-id="cacf7-119">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="cacf7-120">Une fois cette association terminée, un profil est stocké, ce qui permet au Wi-Fi fonctions directes d’être utilisées pour démarrer une session Wi-Fi directe afin d’établir une connexion entre les Wi-Fi les appareils directs.</span><span class="sxs-lookup"><span data-stu-id="cacf7-120">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="cacf7-121">Pour utiliser Wi-Fi directe, une application doit d’abord obtenir un handle pour le service Wi-Fi direct en appelant la fonction [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) .</span><span class="sxs-lookup"><span data-stu-id="cacf7-121">In order to use Wi-Fi Direct, an app must first obtain a handle to the Wi-Fi Direct service by calling the [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) function.</span></span> <span data-ttu-id="cacf7-122">Le handle Wi-Fi direct (WFD) retourné par la fonction **WFDOpenHandle** est utilisé pour les appels de fonction directe Wi-Fis directs passés au service Wi-Fi direct.</span><span class="sxs-lookup"><span data-stu-id="cacf7-122">The Wi-Fi Direct (WFD) handle returned by the **WFDOpenHandle** function is used for subsequent Wi-Fi Direct function calls made to the Wi-Fi Direct service.</span></span>

<span data-ttu-id="cacf7-123">La fonction [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) démarre une opération asynchrone pour démarrer une connexion à la demande à un appareil spécifique Wi-Fi direct.</span><span class="sxs-lookup"><span data-stu-id="cacf7-123">The [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function starts an asynchronous operation to start an on-demand connection to a specific Wi-Fi Direct device.</span></span> <span data-ttu-id="cacf7-124">L’appareil Wi-Fi cible doit avoir été associé à l’expérience de couplage Windows.</span><span class="sxs-lookup"><span data-stu-id="cacf7-124">The target Wi-Fi device must previously have been paired through the Windows Pairing experience.</span></span> <span data-ttu-id="cacf7-125">Lorsque l’opération asynchrone se termine, la fonction de rappel spécifiée dans le paramètre *pfnCallback* est appelée.</span><span class="sxs-lookup"><span data-stu-id="cacf7-125">When the asynchronous operation completes, the callback function specified in the *pfnCallback* parameter is called.</span></span>

<span data-ttu-id="cacf7-126">Une fois qu’une application a été effectuée à l’aide du service Wi-Fi direct, l’application doit appeler la fonction [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) pour signaler au service direct Wi-Fi que l’application est effectuée à l’aide du service.</span><span class="sxs-lookup"><span data-stu-id="cacf7-126">Once an application is done using the Wi-Fi Direct service, the application should call the [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) function to signal to the Wi-Fi Direct service that the application is done using the service.</span></span> <span data-ttu-id="cacf7-127">Cela permet au service Wi-Fi direct de libérer les ressources utilisées par l’application.</span><span class="sxs-lookup"><span data-stu-id="cacf7-127">This allows the Wi-Fi Direct service to release resources used by the application.</span></span>

<span data-ttu-id="cacf7-128">Pour plus d’informations sur Wi-Fi directe pour une utilisation dans les applications du Windows Store, consultez [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) et les classes associées dans l’espace de noms [**Windows. Networking. proximite**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="cacf7-128">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cacf7-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cacf7-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cacf7-130">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="cacf7-130">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="cacf7-131">À propos de la WiFi Native</span><span class="sxs-lookup"><span data-stu-id="cacf7-131">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="cacf7-132">À propos de l’API WiFi Native</span><span class="sxs-lookup"><span data-stu-id="cacf7-132">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="cacf7-133">À propos de la fonctionnalité Wi-Fi directe</span><span class="sxs-lookup"><span data-stu-id="cacf7-133">About the Wi-Fi Direct feature</span></span>](about-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="cacf7-134">**Référence**</span><span class="sxs-lookup"><span data-stu-id="cacf7-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cacf7-135">**PeerFinder**</span><span class="sxs-lookup"><span data-stu-id="cacf7-135">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="cacf7-136">**\_rappel d’ouverture de session WFD \_ \_ terminé \_**</span><span class="sxs-lookup"><span data-stu-id="cacf7-136">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="cacf7-137">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="cacf7-137">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="cacf7-138">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="cacf7-138">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="cacf7-139">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="cacf7-139">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="cacf7-140">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="cacf7-140">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="cacf7-141">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="cacf7-141">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="cacf7-142">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="cacf7-142">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="cacf7-143">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="cacf7-143">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="cacf7-144">**Windows.Networking.Proximity**</span><span class="sxs-lookup"><span data-stu-id="cacf7-144">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
