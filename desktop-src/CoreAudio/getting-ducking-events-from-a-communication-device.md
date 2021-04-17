---
description: Une application multimédia qui souhaite fournir une expérience d’un canard personnalisé doit écouter les notifications d’événements lorsqu’un flux de communication est ouvert ou fermé dans le système.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Obtention d’événements de canard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e45557c25570a89452a39683a0b6732b9632129
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523724"
---
# <a name="getting-ducking-events"></a><span data-ttu-id="b8d74-103">Obtention d’événements de canard</span><span class="sxs-lookup"><span data-stu-id="b8d74-103">Getting Ducking Events</span></span>

<span data-ttu-id="b8d74-104">Une application multimédia qui souhaite fournir une expérience d’un canard personnalisé doit écouter les notifications d’événements lorsqu’un flux de communication est ouvert ou fermé dans le système.</span><span class="sxs-lookup"><span data-stu-id="b8d74-104">A media application that wants to provide a customised ducking experience must listen for the event notifications when a communication stream is opened or closed in the system.</span></span> <span data-ttu-id="b8d74-105">L’implémentation personnalisée peut être fournie à l’aide de MediaFoundation, DirectShow ou DirectSound, qui utilisent les API audio de base.</span><span class="sxs-lookup"><span data-stu-id="b8d74-105">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="b8d74-106">Un client direct WASAPI peut également remplacer la gestion par défaut s’il sait à quel moment la session de communication démarre et se termine.</span><span class="sxs-lookup"><span data-stu-id="b8d74-106">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="b8d74-107">Pour fournir une implémentation personnalisée, une application multimédia doit recevoir des notifications du système lorsqu’une application de communication démarre ou termine un flux de communication.</span><span class="sxs-lookup"><span data-stu-id="b8d74-107">To provide a custom implementation, a media application needs to get notifications from the system when a communication application starts or ends a communication stream.</span></span> <span data-ttu-id="b8d74-108">L’application multimédia doit implémenter l’interface [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) et inscrire l’implémentation auprès du système audio.</span><span class="sxs-lookup"><span data-stu-id="b8d74-108">The media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="b8d74-109">Une fois l’inscription réussie, l’application multimédia reçoit des notifications d’événements sous la forme de rappels via les méthodes de l’interface.</span><span class="sxs-lookup"><span data-stu-id="b8d74-109">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="b8d74-110">Pour plus d’informations, consultez [considérations relatives à l’implémentation pour l’installation de notifications](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b8d74-110">For more information, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

<span data-ttu-id="b8d74-111">Pour envoyer des notifications de canard, le système audio doit savoir quelle session audio est à l’écoute des événements de l’événement.</span><span class="sxs-lookup"><span data-stu-id="b8d74-111">To send ducking notifications, the audio system must know which audio session is listening for the ducking events.</span></span> <span data-ttu-id="b8d74-112">Chaque session audio est identifiée de manière unique avec un GUID (identificateur d’instance de session).</span><span class="sxs-lookup"><span data-stu-id="b8d74-112">Each audio session is uniquely identified with a GUID—session instance identifier.</span></span> <span data-ttu-id="b8d74-113">Le gestionnaire de sessions permet à une application d’obtenir des informations sur la session, telles que le titre de la session audio, l’état du rendu et l’identificateur de l’instance de session.</span><span class="sxs-lookup"><span data-stu-id="b8d74-113">The session manager allows an application to get information about the session such as title of audio session, the rendering state, and the session instance identifier.</span></span> <span data-ttu-id="b8d74-114">L’identificateur peut être récupéré à l’aide de l’interface de contrôle de stratégie, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span><span class="sxs-lookup"><span data-stu-id="b8d74-114">The identifier can be retrieved by using the policy control interface, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span></span>

<span data-ttu-id="b8d74-115">Les étapes suivantes résument le processus d’obtention de l’identificateur d’instance de session de l’application multimédia :</span><span class="sxs-lookup"><span data-stu-id="b8d74-115">The following steps summarize the process of getting the session instance identifier of the media application:</span></span>

1.  <span data-ttu-id="b8d74-116">Instanciez l’énumérateur d’appareil et utilisez-le pour obtenir une référence au point de terminaison de l’appareil que l’application multimédia utilise pour restituer le flux de non-communication.</span><span class="sxs-lookup"><span data-stu-id="b8d74-116">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="b8d74-117">Activez le gestionnaire de sessions à partir du point de terminaison de l’appareil et récupérez une référence à l’interface [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) du gestionnaire de sessions.</span><span class="sxs-lookup"><span data-stu-id="b8d74-117">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="b8d74-118">En utilisant le pointeur [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) , vous pouvez obtenir une référence à l’interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) du gestionnaire de sessions.</span><span class="sxs-lookup"><span data-stu-id="b8d74-118">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="b8d74-119">Interrogez le [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) à partir de l’interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .</span><span class="sxs-lookup"><span data-stu-id="b8d74-119">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="b8d74-120">Appelez [**IAudioSessionControl2 :: GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) et récupérez une chaîne qui contient l’identificateur de session pour la session audio en cours.</span><span class="sxs-lookup"><span data-stu-id="b8d74-120">Call [**IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) and retrieve a string that contains the session identifier for the current audio session.</span></span>

<span data-ttu-id="b8d74-121">Pour obtenir des notifications sur les flux de communication, l’application multimédia appelle [**IAudioSessionManager2 :: RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span><span class="sxs-lookup"><span data-stu-id="b8d74-121">To get ducking notifications about communication streams, the media application calls [**IAudioSessionManager2::RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span></span> <span data-ttu-id="b8d74-122">L’application multimédia fournit son identificateur d’instance de session au système audio et un pointeur vers l’implémentation de [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) .</span><span class="sxs-lookup"><span data-stu-id="b8d74-122">The media application supplies its session instance identifier to the audio system and a pointer to the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) implementation.</span></span> <span data-ttu-id="b8d74-123">L’application peut désormais recevoir une notification d’événement lorsqu’un flux est ouvert sur le périphérique de communication.</span><span class="sxs-lookup"><span data-stu-id="b8d74-123">The application can now receive event notification when a stream opened on the communication device.</span></span> <span data-ttu-id="b8d74-124">Pour ne plus recevoir de notification, l’application multimédia doit appeler [**IAudioSessionManager2 :: UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span><span class="sxs-lookup"><span data-stu-id="b8d74-124">To stop getting notification, the media application must call [**IAudioSessionManager2::UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span></span>

<span data-ttu-id="b8d74-125">Le code suivant montre comment une application peut s’inscrire pour recevoir des notifications de canard.</span><span class="sxs-lookup"><span data-stu-id="b8d74-125">The following code shows how an application can register to get ducking notifications.</span></span> <span data-ttu-id="b8d74-126">La classe CMediaPlayer est définie dans [considérations d’implémentation pour l’application de notifications](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b8d74-126">The CMediaPlayer class is defined in [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span> <span data-ttu-id="b8d74-127">L’exemple [DuckingMediaPlayer](duckingmediaplayer.md) implémente cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="b8d74-127">The [DuckingMediaPlayer](duckingmediaplayer.md) sample implements this functionality.</span></span>


```C++
////////////////////////////////////////////////////////////////////
//Description: Registers for duck notifications depending on the 
//             the ducking options specified by the caller.
//Parameters: 
//    If DuckingOptOutChecked is TRUE, the client is registered for
//    to receive ducking notifications; 
//    FALSE, the client's registration is deleted.
////////////////////////////////////////////////////////////////////

HRESULT CMediaPlayer::DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;

    LPWSTR sessionId = NULL;

    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(
              eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate the session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>
                                 (&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(
                                  NULL, 0, &pSessionControl);
        
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                               IID_PPV_ARGS(&pSessionControl2));
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    // Get the session instance identifier.
    
    if (SUCCEEDED(hr))
    {
        hr = pSessionControl2->GetSessionInstanceIdentifier(
                                 sessionId);
                
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }

    //  Register for ducking events depending on 
    //  the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionManager2->RegisterDuckNotification(
                                    sessionId, this);
        }
        else
        {
            hr = pSessionManager2->UnregisterDuckNotification
                                      (FALSE);
        }
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b8d74-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8d74-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8d74-129">Utilisation d’un appareil de communication</span><span class="sxs-lookup"><span data-stu-id="b8d74-129">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="b8d74-130">Expérience de l’utilisation des canards par défaut</span><span class="sxs-lookup"><span data-stu-id="b8d74-130">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="b8d74-131">Désactivation de l’expérience de l’utilisation des canards par défaut</span><span class="sxs-lookup"><span data-stu-id="b8d74-131">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="b8d74-132">Fournir un comportement de canard personnalisé</span><span class="sxs-lookup"><span data-stu-id="b8d74-132">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="b8d74-133">Considérations relatives à l’implémentation pour l’installation de notifications</span><span class="sxs-lookup"><span data-stu-id="b8d74-133">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



