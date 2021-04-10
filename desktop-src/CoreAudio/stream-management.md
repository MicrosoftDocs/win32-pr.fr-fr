---
description: Gestion de flux
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Gestion de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07180d8b46f4d079c08f4b619cf4a7773a6104d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110934"
---
# <a name="stream-management"></a><span data-ttu-id="b7283-103">Gestion de flux</span><span class="sxs-lookup"><span data-stu-id="b7283-103">Stream Management</span></span>

<span data-ttu-id="b7283-104">Après avoir énuméré les [périphériques de point de terminaison audio](audio-endpoint-devices.md) dans le système et identifié un appareil de rendu ou de capture approprié, la tâche suivante pour une application cliente audio consiste à ouvrir une connexion avec l’appareil de point de terminaison et à gérer le flux de données audio sur cette connexion.</span><span class="sxs-lookup"><span data-stu-id="b7283-104">After enumerating the [audio endpoint devices](audio-endpoint-devices.md) in the system and identifying a suitable rendering or capture device, the next task for an audio client application is to open a connection with the endpoint device and to manage the flow of audio data over that connection.</span></span> <span data-ttu-id="b7283-105">[WASAPI](wasapi.md) permet aux clients de créer et de gérer des flux audio.</span><span class="sxs-lookup"><span data-stu-id="b7283-105">[WASAPI](wasapi.md) enables clients to create and manage audio streams.</span></span>

<span data-ttu-id="b7283-106">WASAPI implémente plusieurs interfaces pour fournir des services de gestion de flux aux clients audio.</span><span class="sxs-lookup"><span data-stu-id="b7283-106">WASAPI implements several interfaces to provide stream-management services to audio clients.</span></span> <span data-ttu-id="b7283-107">L’interface principale est [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span><span class="sxs-lookup"><span data-stu-id="b7283-107">The primary interface is [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient).</span></span> <span data-ttu-id="b7283-108">Un client obtient l’interface **IAudioClient** pour un périphérique de point de terminaison audio en appelant la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (avec l' *IID* de paramètre défini sur **REFIID** IID \_ IAudioClient) sur l’objet de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b7283-108">A client obtains the **IAudioClient** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioClient) on the endpoint object.</span></span>

<span data-ttu-id="b7283-109">Le client appelle les méthodes dans l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7283-109">The client calls the methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to do the following:</span></span>

-   <span data-ttu-id="b7283-110">Découvrez les formats audio pris en charge par l’appareil de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b7283-110">Discover which audio formats the endpoint device supports.</span></span>
-   <span data-ttu-id="b7283-111">Obtient la taille de la mémoire tampon du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b7283-111">Get the endpoint buffer size.</span></span>
-   <span data-ttu-id="b7283-112">Obtient le format et la latence du flux.</span><span class="sxs-lookup"><span data-stu-id="b7283-112">Get the stream format and latency.</span></span>
-   <span data-ttu-id="b7283-113">Démarrer, arrêter et réinitialiser le flux qui transite par l’appareil de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b7283-113">Start, stop, and reset the stream that flows through the endpoint device.</span></span>
-   <span data-ttu-id="b7283-114">Accédez à des services audio supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b7283-114">Access additional audio services.</span></span>

<span data-ttu-id="b7283-115">Pour créer un flux, un client appelle la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="b7283-115">To create a stream, a client calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span> <span data-ttu-id="b7283-116">Par le biais de cette méthode, le client spécifie le format de données du flux, la taille de la mémoire tampon du point de terminaison et si le flux fonctionne en mode partagé ou exclusif.</span><span class="sxs-lookup"><span data-stu-id="b7283-116">Through this method, the client specifies the data format for the stream, the size of the endpoint buffer, and whether the stream operates in shared or exclusive mode.</span></span>

<span data-ttu-id="b7283-117">Les autres méthodes de l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) se répartissent en deux groupes :</span><span class="sxs-lookup"><span data-stu-id="b7283-117">The remaining methods in the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface fall into two groups:</span></span>

-   <span data-ttu-id="b7283-118">Méthodes qui peuvent être appelées uniquement après que le flux a été ouvert par [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="b7283-118">Methods that can be called only after the stream has been opened by [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="b7283-119">Méthodes qui peuvent être appelées à tout moment avant ou après l’appel [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="b7283-119">Methods that can be called at any time before or after the [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call.</span></span>

<span data-ttu-id="b7283-120">Les méthodes suivantes peuvent être appelées uniquement après l’appel à [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span><span class="sxs-lookup"><span data-stu-id="b7283-120">The following methods can be called only after the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):</span></span>

-   [<span data-ttu-id="b7283-121">**IAudioClient::GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="b7283-121">**IAudioClient::GetBufferSize**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [<span data-ttu-id="b7283-122">**IAudioClient::GetCurrentPadding**</span><span class="sxs-lookup"><span data-stu-id="b7283-122">**IAudioClient::GetCurrentPadding**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [<span data-ttu-id="b7283-123">**IAudioClient :: GetService**</span><span class="sxs-lookup"><span data-stu-id="b7283-123">**IAudioClient::GetService**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [<span data-ttu-id="b7283-124">**IAudioClient::GetStreamLatency**</span><span class="sxs-lookup"><span data-stu-id="b7283-124">**IAudioClient::GetStreamLatency**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [<span data-ttu-id="b7283-125">**IAudioClient :: Reset**</span><span class="sxs-lookup"><span data-stu-id="b7283-125">**IAudioClient::Reset**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [<span data-ttu-id="b7283-126">**IAudioClient :: Start**</span><span class="sxs-lookup"><span data-stu-id="b7283-126">**IAudioClient::Start**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [<span data-ttu-id="b7283-127">**IAudioClient :: Stop**</span><span class="sxs-lookup"><span data-stu-id="b7283-127">**IAudioClient::Stop**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

<span data-ttu-id="b7283-128">Les méthodes suivantes peuvent être appelées avant ou après l’appel de [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) :</span><span class="sxs-lookup"><span data-stu-id="b7283-128">The following methods can be called before or after the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) call:</span></span>

-   [<span data-ttu-id="b7283-129">**IAudioClient::GetDevicePeriod**</span><span class="sxs-lookup"><span data-stu-id="b7283-129">**IAudioClient::GetDevicePeriod**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [<span data-ttu-id="b7283-130">**IAudioClient::GetMixFormat**</span><span class="sxs-lookup"><span data-stu-id="b7283-130">**IAudioClient::GetMixFormat**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [<span data-ttu-id="b7283-131">**IAudioClient::IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="b7283-131">**IAudioClient::IsFormatSupported**</span></span>](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

<span data-ttu-id="b7283-132">Pour accéder aux services du client audio supplémentaires, le client appelle la méthode [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .</span><span class="sxs-lookup"><span data-stu-id="b7283-132">To access the additional audio client services, the client calls the [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) method.</span></span> <span data-ttu-id="b7283-133">Par le biais de cette méthode, le client peut obtenir des références aux interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7283-133">Through this method, the client can obtain references to the following interfaces:</span></span>

-   [<span data-ttu-id="b7283-134">**IAudioRenderClient**</span><span class="sxs-lookup"><span data-stu-id="b7283-134">**IAudioRenderClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    <span data-ttu-id="b7283-135">Écrit des données de rendu dans une mémoire tampon de point de terminaison de rendu audio.</span><span class="sxs-lookup"><span data-stu-id="b7283-135">Writes rendering data to an audio-rendering endpoint buffer.</span></span>

-   [<span data-ttu-id="b7283-136">**IAudioCaptureClient**</span><span class="sxs-lookup"><span data-stu-id="b7283-136">**IAudioCaptureClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    <span data-ttu-id="b7283-137">Lit les données capturées à partir d’une mémoire tampon de point de terminaison de capture audio.</span><span class="sxs-lookup"><span data-stu-id="b7283-137">Reads captured data from an audio-capture endpoint buffer.</span></span>

-   [<span data-ttu-id="b7283-138">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="b7283-138">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    <span data-ttu-id="b7283-139">Communique avec le gestionnaire de sessions audio pour configurer et gérer la session audio associée au flux.</span><span class="sxs-lookup"><span data-stu-id="b7283-139">Communicates with the audio session manager to configure and manage the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="b7283-140">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="b7283-140">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    <span data-ttu-id="b7283-141">Contrôle le niveau de volume de la session audio associée au flux.</span><span class="sxs-lookup"><span data-stu-id="b7283-141">Controls the volume level of the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="b7283-142">**IChannelAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="b7283-142">**IChannelAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    <span data-ttu-id="b7283-143">Contrôle les niveaux de volume des canaux individuels dans la session audio associée au flux.</span><span class="sxs-lookup"><span data-stu-id="b7283-143">Controls the volume levels of the individual channels in the audio session that is associated with the stream.</span></span>

-   [<span data-ttu-id="b7283-144">**IAudioClock**</span><span class="sxs-lookup"><span data-stu-id="b7283-144">**IAudioClock**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    <span data-ttu-id="b7283-145">Analyse la vitesse et la position du flux de données de flux.</span><span class="sxs-lookup"><span data-stu-id="b7283-145">Monitors the stream data rate and stream position.</span></span>

<span data-ttu-id="b7283-146">En outre, les clients WASAPI qui requièrent la notification des événements liés à la session doivent implémenter l’interface suivante :</span><span class="sxs-lookup"><span data-stu-id="b7283-146">In addition, WASAPI clients that require notification of session-related events should implement the following interface:</span></span>

-   [<span data-ttu-id="b7283-147">**IAudioSessionEvents**</span><span class="sxs-lookup"><span data-stu-id="b7283-147">**IAudioSessionEvents**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    <span data-ttu-id="b7283-148">Pour recevoir des notifications d’événements, le client passe un pointeur vers son interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) à la méthode [**IAudioSessionControl :: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) en tant que paramètre d’appel.</span><span class="sxs-lookup"><span data-stu-id="b7283-148">To receive event notifications, the client passes a pointer to its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method as a call parameter.</span></span>

<span data-ttu-id="b7283-149">Enfin, un client peut utiliser une API de niveau supérieur pour créer un flux audio, mais il doit également avoir accès aux contrôles de session et aux contrôles de volume pour la session qui contient le flux.</span><span class="sxs-lookup"><span data-stu-id="b7283-149">Finally, a client might use a higher-level API to create an audio stream, but also require access to the session controls and volume controls for the session that contains the stream.</span></span> <span data-ttu-id="b7283-150">En général, une API de niveau supérieur ne fournit pas cet accès.</span><span class="sxs-lookup"><span data-stu-id="b7283-150">A higher-level API typically does not provide this access.</span></span> <span data-ttu-id="b7283-151">Le client peut obtenir les contrôles pour une session particulière par le biais de l’interface [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) .</span><span class="sxs-lookup"><span data-stu-id="b7283-151">The client can obtain the controls for a particular session through the [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface.</span></span> <span data-ttu-id="b7283-152">Cette interface permet au client d’obtenir les interfaces [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) et [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) pour une session sans demander au client d’utiliser l’interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) pour créer un flux et assigner le flux à la session.</span><span class="sxs-lookup"><span data-stu-id="b7283-152">This interface enables the client to obtain the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) and [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interfaces for a session without requiring the client to use the [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) interface to create a stream and to assign the stream to the session.</span></span> <span data-ttu-id="b7283-153">Un client obtient l’interface **IAudioSessionManager** pour un périphérique de point de terminaison audio en appelant la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (avec l' *IID* de paramètre défini sur **REFIID** IID \_ IAudioSessionManager) sur l’objet de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b7283-153">A client obtains the **IAudioSessionManager** interface for an audio endpoint device by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method (with parameter *iid* set to **REFIID** IID\_IAudioSessionManager) on the endpoint object.</span></span>

<span data-ttu-id="b7283-154">Les interfaces [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)et [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) sont définies dans le fichier d’en-tête Audiopolicy. h.</span><span class="sxs-lookup"><span data-stu-id="b7283-154">The [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents), and [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interfaces are defined in header file Audiopolicy.h.</span></span> <span data-ttu-id="b7283-155">Toutes les autres interfaces WASAPI sont définies dans le fichier d’en-tête Audioclient. h.</span><span class="sxs-lookup"><span data-stu-id="b7283-155">All other WASAPI interfaces are defined in header file Audioclient.h.</span></span>

<span data-ttu-id="b7283-156">Les sections suivantes décrivent comment utiliser WASAPI pour gérer des flux audio :</span><span class="sxs-lookup"><span data-stu-id="b7283-156">The following sections describe how to use WASAPI to manage audio streams:</span></span>

-   [<span data-ttu-id="b7283-157">À propos de WASAPI</span><span class="sxs-lookup"><span data-stu-id="b7283-157">About WASAPI</span></span>](wasapi.md)
-   [<span data-ttu-id="b7283-158">Rendu d’un flux</span><span class="sxs-lookup"><span data-stu-id="b7283-158">Rendering a Stream</span></span>](rendering-a-stream.md)
-   [<span data-ttu-id="b7283-159">Capture d’un flux</span><span class="sxs-lookup"><span data-stu-id="b7283-159">Capturing a Stream</span></span>](capturing-a-stream.md)
-   [<span data-ttu-id="b7283-160">Enregistrement de bouclage</span><span class="sxs-lookup"><span data-stu-id="b7283-160">Loopback Recording</span></span>](loopback-recording.md)
-   [<span data-ttu-id="b7283-161">Flux en mode exclusif</span><span class="sxs-lookup"><span data-stu-id="b7283-161">Exclusive-Mode Streams</span></span>](exclusive-mode-streams.md)
-   [<span data-ttu-id="b7283-162">Récupération à partir d’une erreur Invalid-Device</span><span class="sxs-lookup"><span data-stu-id="b7283-162">Recovering from an Invalid-Device Error</span></span>](recovering-from-an-invalid-device-error.md)
-   [<span data-ttu-id="b7283-163">Utilisation d’un appareil de communication</span><span class="sxs-lookup"><span data-stu-id="b7283-163">Using a Communication Device</span></span>](using-the-communication-device.md)
-   [<span data-ttu-id="b7283-164">Routage de flux</span><span class="sxs-lookup"><span data-stu-id="b7283-164">Stream Routing</span></span>](stream-routing.md)

## <a name="related-topics"></a><span data-ttu-id="b7283-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7283-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7283-166">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="b7283-166">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



