---
description: Le routage de flux est la capacité d’une application multimédia à basculer les flux entre les appareils avec une interruption minimale de la lecture ou de la session de capture.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Routage de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b21cd15a4467cb9b08747119aab999882ae3b5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483464"
---
# <a name="stream-routing"></a><span data-ttu-id="085f1-103">Routage de flux</span><span class="sxs-lookup"><span data-stu-id="085f1-103">Stream Routing</span></span>

<span data-ttu-id="085f1-104">Le *routage de flux* est la capacité d’une application multimédia à basculer les flux entre les appareils avec une interruption minimale de la lecture ou de la session de capture.</span><span class="sxs-lookup"><span data-stu-id="085f1-104">*Stream routing* is the ability of a media application to switch streams between devices with minimal interruption to the playback or the capture session.</span></span>

<span data-ttu-id="085f1-105">Un ordinateur peut avoir plusieurs périphériques de rendu et de capture.</span><span class="sxs-lookup"><span data-stu-id="085f1-105">A computer can have multiple rendering and capture devices.</span></span> <span data-ttu-id="085f1-106">Le système répertorie ces périphériques dans le panneau de configuration **sons** .</span><span class="sxs-lookup"><span data-stu-id="085f1-106">The system lists these devices on the **Sounds** control panel.</span></span> <span data-ttu-id="085f1-107">Dans cette liste, un utilisateur peut définir un appareil comme périphérique par défaut pour chaque rôle : lecture, enregistrement ou quatre rôles de communication (rendu de la console, capture de la console, rendu de communication ou capture de communication).</span><span class="sxs-lookup"><span data-stu-id="085f1-107">From this list, a user can set a device to be the default device for each role: playback, recording, or the four communications roles (console render, console capture, communication render, or communication capture).</span></span> <span data-ttu-id="085f1-108">La liste des appareils peut être modifiée de manière dynamique, car certains de ces appareils peuvent être temporairement disponibles, par exemple un casque USB.</span><span class="sxs-lookup"><span data-stu-id="085f1-108">The list of devices may be modified dynamically as some of these devices can be available temporarily, for example a USB headset.</span></span> <span data-ttu-id="085f1-109">Lorsque plusieurs appareils sont disponibles, l’utilisateur peut modifier la valeur par défaut sur un autre appareil.</span><span class="sxs-lookup"><span data-stu-id="085f1-109">When multiple devices are available, the user can change the default to a different device.</span></span> <span data-ttu-id="085f1-110">L’utilisateur peut également modifier le format d’un appareil (taux d’échantillonnage, bits par échantillon, etc.) sous l’onglet **avancé** des propriétés de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="085f1-110">The user can also change the format of a device (sample rate, bits per sample, and so on) on the **Advanced** tab for the device properties.</span></span>

<span data-ttu-id="085f1-111">Imaginez un scénario dans lequel un utilisateur sélectionne les **intervenants** comme appareil par défaut pour le rendu des flux audio.</span><span class="sxs-lookup"><span data-stu-id="085f1-111">Consider a scenario in which a user selects **Speakers** as the default device for rendering audio streams.</span></span> <span data-ttu-id="085f1-112">L’utilisateur connecte ensuite un casque USB, sélectionne le casque comme nouvel appareil par défaut et modifie le taux d’échantillonnage de l’appareil de 44,1 kHz à 48 kHz.</span><span class="sxs-lookup"><span data-stu-id="085f1-112">The user then connects a USB headset, selects the headset as the new default device, and changes the sample rate of the device from 44.1 kHz to 48 kHz.</span></span> <span data-ttu-id="085f1-113">L’utilisateur souhaite lire le flux audio sur le casque à la nouvelle fréquence d’échantillonnage avec une interruption minimale de la session de streaming.</span><span class="sxs-lookup"><span data-stu-id="085f1-113">The user wants to play the audio stream on the headset at the new sample rate with minimal interruption to the streaming session.</span></span>

<span data-ttu-id="085f1-114">Dans ce scénario, l’application multimédia doit gérer deux cas :</span><span class="sxs-lookup"><span data-stu-id="085f1-114">In this scenario, there are two cases that the media application must handle:</span></span>

-   <span data-ttu-id="085f1-115">Le flux doit être transféré vers le nouvel appareil par défaut avec une interruption minimale de la lecture.</span><span class="sxs-lookup"><span data-stu-id="085f1-115">The stream must be transferred to the new default device with minimal interruption to playback.</span></span>
-   <span data-ttu-id="085f1-116">Le nouvel appareil doit reprendre la lecture dans le nouveau format (c’est-à-dire que l’utilisateur peut modifier plus que le taux d’échantillonnage).</span><span class="sxs-lookup"><span data-stu-id="085f1-116">The new device must resume playback in the new format (that is, the user can change more than the sample rate).</span></span>

<span data-ttu-id="085f1-117">Dans Windows Vista, pour prendre en charge ce scénario, l’application multimédia devait fournir l’implémentation du routage de flux.</span><span class="sxs-lookup"><span data-stu-id="085f1-117">In Windows Vista, to support this scenario, the media application had to provide the implementation for stream routing.</span></span> <span data-ttu-id="085f1-118">L’application était responsable de l’arrêt des flux existants et du redémarrage des flux sur le nouvel appareil.</span><span class="sxs-lookup"><span data-stu-id="085f1-118">The application was responsible for terminating existing streams and restarting the streams on the new device.</span></span> <span data-ttu-id="085f1-119">Si l’utilisateur a modifié l’appareil par défaut ou son format Mix modifié, toutes les sessions associées ont été fermées et l’application devait gérer la récupération.</span><span class="sxs-lookup"><span data-stu-id="085f1-119">If the user changed the default device or its mix format changed, then all of the associated sessions were closed and the application had to handle the recovery.</span></span>

<span data-ttu-id="085f1-120">Dans Windows 7, une application peut transférer en toute transparence un flux à partir d’un périphérique par défaut existant vers un nouveau point de terminaison audio par défaut.</span><span class="sxs-lookup"><span data-stu-id="085f1-120">In Windows 7, an application can seamlessly transfer a stream from an existing default device to a new default audio endpoint.</span></span> <span data-ttu-id="085f1-121">Les ensembles d’API audio de haut niveau, tels que Media Foundation, DirectSound et les API WAVE, implémentent la fonctionnalité de routage de flux.</span><span class="sxs-lookup"><span data-stu-id="085f1-121">High-level audio API sets such as Media Foundation, DirectSound, and WAVE APIs implement the stream routing feature.</span></span> <span data-ttu-id="085f1-122">Les applications multimédias qui utilisent ces ensembles d’API pour lire ou capturer un flux à partir de l’appareil par défaut utilisent l’implémentation par défaut et n’ont pas besoin de modifier l’application.</span><span class="sxs-lookup"><span data-stu-id="085f1-122">Media applications that use these API sets to play or capture a stream from the default device use the default implementation and will not have to modify the application.</span></span> <span data-ttu-id="085f1-123">Toutefois, si votre application multimédia utilise MMDeviceAPI ou WASAPI directement, l’application doit fournir l’implémentation du routage du flux.</span><span class="sxs-lookup"><span data-stu-id="085f1-123">However, if your media application uses MMDeviceAPI or WASAPI directly, the application needs to provide the stream routing implementation.</span></span>

> [!Note]  
> <span data-ttu-id="085f1-124">MMDeviceAPI et WASAPI sont des composants d’API audio essentiels qu’une application peut utiliser pour afficher ou capturer un flux sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="085f1-124">MMDeviceAPI and WASAPI are Core Audio API components that an application can use to render or capture a stream on a device.</span></span> <span data-ttu-id="085f1-125">Le MMDeviceAPI Découvre le nouvel appareil de point de terminaison audio et WASAPI gère le flux de données audio entre une application multimédia et l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="085f1-125">The MMDeviceAPI discovers the new audio endpoint device, and WASAPI manages the flow of audio data between a media application and the audio endpoint device.</span></span>

 

<span data-ttu-id="085f1-126">Pour implémenter la fonctionnalité de routage de flux, l’application doit écouter les notifications envoyées par MMDeviceAPI et WASAPI lorsque :</span><span class="sxs-lookup"><span data-stu-id="085f1-126">To implement the stream routing feature, the application must listen for the notifications sent by MMDeviceAPI and WASAPI when:</span></span>

-   <span data-ttu-id="085f1-127">L’appareil par défaut est modifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="085f1-127">The default device is changed by the user.</span></span>
-   <span data-ttu-id="085f1-128">L’appareil par défaut existant est supprimé et un nouveau périphérique par défaut est ajouté.</span><span class="sxs-lookup"><span data-stu-id="085f1-128">The existing default device is removed and a new default device is added.</span></span>
-   <span data-ttu-id="085f1-129">Le format de l’appareil a été modifié.</span><span class="sxs-lookup"><span data-stu-id="085f1-129">The device format is changed.</span></span>

<span data-ttu-id="085f1-130">En gérant ces notifications, une application peut effectuer les opérations de gestion de flux nécessaires lors du transfert du flux vers le nouvel appareil par défaut.</span><span class="sxs-lookup"><span data-stu-id="085f1-130">By handling these notifications, an application can perform the necessary stream management operations while transferring the stream to the new default device.</span></span> <span data-ttu-id="085f1-131">En outre, l’application peut afficher ou capturer des flux existants en utilisant le nouveau format spécifié par l’utilisateur pendant qu’une session de rendu est active.</span><span class="sxs-lookup"><span data-stu-id="085f1-131">In addition, the application can render or capture existing streams by using the new format specified by the user while a rendering session is active.</span></span>

<span data-ttu-id="085f1-132">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="085f1-132">This section contains the following topics:</span></span>

-   [<span data-ttu-id="085f1-133">Obtention du point de terminaison de l’appareil pour le routage du flux</span><span class="sxs-lookup"><span data-stu-id="085f1-133">Getting the Device Endpoint for Stream Routing</span></span>](getting-the-default-device-endpoint-for-stream-routing.md)
-   [<span data-ttu-id="085f1-134">Notifications appropriées pour le routage de flux</span><span class="sxs-lookup"><span data-stu-id="085f1-134">Relevant Notifications for Stream Routing</span></span>](relevant-device-notifications-for-stream-routing.md)
-   [<span data-ttu-id="085f1-135">Considérations relatives à l’implémentation du routage de flux</span><span class="sxs-lookup"><span data-stu-id="085f1-135">Stream Routing Implementation Considerations</span></span>](stream-routing-implementation-considerations.md)

<span data-ttu-id="085f1-136">Les exemples suivants, inclus dans le SDK Windows, montrent comment une application peut gérer les notifications de routage de flux.</span><span class="sxs-lookup"><span data-stu-id="085f1-136">The following samples, included in the Windows SDK, demonstrate how an application can handle stream routing notifications.</span></span>

-   [<span data-ttu-id="085f1-137">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="085f1-137">RenderSharedTimerDriven</span></span>](rendersharedtimerdriven.md)
-   [<span data-ttu-id="085f1-138">RenderSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="085f1-138">RenderSharedEventDriven</span></span>](rendersharedeventdriven.md)
-   [<span data-ttu-id="085f1-139">RenderExclusiveTimerDriven</span><span class="sxs-lookup"><span data-stu-id="085f1-139">RenderExclusiveTimerDriven</span></span>](renderexclusivetimerdriven.md)
-   [<span data-ttu-id="085f1-140">RenderExclusiveEventDriven</span><span class="sxs-lookup"><span data-stu-id="085f1-140">RenderExclusiveEventDriven</span></span>](renderexclusiveeventdriven.md)
-   [<span data-ttu-id="085f1-141">CaptureSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="085f1-141">CaptureSharedTimerDriven</span></span>](capturesharedtimerdriven.md)
-   [<span data-ttu-id="085f1-142">CaptureSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="085f1-142">CaptureSharedEventDriven</span></span>](capturesharedeventdriven.md)

## <a name="related-topics"></a><span data-ttu-id="085f1-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="085f1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="085f1-144">Gestion de flux</span><span class="sxs-lookup"><span data-stu-id="085f1-144">Stream Management</span></span>](stream-management.md)
</dt> <dt>

[<span data-ttu-id="085f1-145">À propos de l’API MMDevice</span><span class="sxs-lookup"><span data-stu-id="085f1-145">About MMDevice API</span></span>](mmdevice-api.md)
</dt> <dt>

[<span data-ttu-id="085f1-146">À propos de WASAPI</span><span class="sxs-lookup"><span data-stu-id="085f1-146">About WASAPI</span></span>](wasapi.md)
</dt> </dl>

 

 



