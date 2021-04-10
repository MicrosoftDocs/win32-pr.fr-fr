---
description: Événements de session audio
ms.assetid: 6943b405-0807-412b-a149-fc3a8ece1b48
title: Événements de session audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ec5de18c883f817c2f650ccfc48ad0149ac84e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950638"
---
# <a name="audio-session-events"></a><span data-ttu-id="c94f7-103">Événements de session audio</span><span class="sxs-lookup"><span data-stu-id="c94f7-103">Audio Session Events</span></span>

<span data-ttu-id="c94f7-104">Une application qui gère des flux audio en mode partagé peut s’inscrire pour recevoir des notifications lorsque des événements de session se produisent.</span><span class="sxs-lookup"><span data-stu-id="c94f7-104">An application that manages shared-mode audio streams can register to receive notifications when session events occur.</span></span> <span data-ttu-id="c94f7-105">Comme expliqué précédemment, chaque flux appartient à une [session audio](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="c94f7-105">As explained previously, each stream belongs to an [audio session](audio-sessions.md).</span></span> <span data-ttu-id="c94f7-106">Un événement de session est initié par une modification de l’état d’une session audio.</span><span class="sxs-lookup"><span data-stu-id="c94f7-106">A session event is initiated by a change in the status of an audio session.</span></span>

<span data-ttu-id="c94f7-107">Une application cliente peut s’inscrire pour recevoir des notifications des types d’événements de session suivants :</span><span class="sxs-lookup"><span data-stu-id="c94f7-107">A client application can register to receive notifications of the following types of session events:</span></span>

-   <span data-ttu-id="c94f7-108">Le niveau du volume principal ou l’état d’inactivation du mixage secondaire de la session a changé.</span><span class="sxs-lookup"><span data-stu-id="c94f7-108">The master volume level or muting state of the session submix has changed.</span></span>
-   <span data-ttu-id="c94f7-109">Le niveau de volume d’un ou plusieurs canaux du mixage secondaire de session a changé.</span><span class="sxs-lookup"><span data-stu-id="c94f7-109">The volume level of one or more channels of the session submix has changed.</span></span>
-   <span data-ttu-id="c94f7-110">La session a été déconnectée.</span><span class="sxs-lookup"><span data-stu-id="c94f7-110">The session has been disconnected.</span></span>
-   <span data-ttu-id="c94f7-111">L’état de l’activité de la session est passé à actif, inactif ou expiré.</span><span class="sxs-lookup"><span data-stu-id="c94f7-111">The activity state of the session has changed to active, inactive, or expired.</span></span>
-   <span data-ttu-id="c94f7-112">Un nouveau paramètre de regroupement a été affecté à la session.</span><span class="sxs-lookup"><span data-stu-id="c94f7-112">The session has been assigned a new grouping parameter.</span></span>
-   <span data-ttu-id="c94f7-113">Une propriété de l’interface utilisateur de la session (icône ou nom d’affichage) a changé.</span><span class="sxs-lookup"><span data-stu-id="c94f7-113">A user-interface property of the session (icon or display name) has changed.</span></span>

<span data-ttu-id="c94f7-114">Le client reçoit les notifications de ces événements par le biais des méthodes dans son implémentation de l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="c94f7-114">The client receives notifications of these events through the methods in its implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="c94f7-115">Contrairement aux autres interfaces dans WASAPI, qui sont implémentées par le module système WASAPI, le client implémente **IAudioSessionEvents**.</span><span class="sxs-lookup"><span data-stu-id="c94f7-115">Unlike the other interfaces in WASAPI, which are implemented by the WASAPI system module, the client implements **IAudioSessionEvents**.</span></span> <span data-ttu-id="c94f7-116">Les méthodes de cette interface reçoivent des rappels du module système WASAPI lorsque des événements de session se produisent.</span><span class="sxs-lookup"><span data-stu-id="c94f7-116">The methods in this interface receive callbacks from the WASAPI system module when session events occur.</span></span>

<span data-ttu-id="c94f7-117">Pour commencer à recevoir des notifications, le client appelle la méthode [**IAudioSessionControl :: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) pour inscrire son interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="c94f7-117">To begin receiving notifications, the client calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="c94f7-118">Lorsque le client n’a plus besoin de notifications, il appelle la méthode [**IAudioSessionControl :: UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) pour supprimer l’inscription.</span><span class="sxs-lookup"><span data-stu-id="c94f7-118">When the client no longer requires notifications, it calls the [**IAudioSessionControl::UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) method to delete the registration.</span></span>

<span data-ttu-id="c94f7-119">L’exemple de code suivant montre une implémentation possible de l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) :</span><span class="sxs-lookup"><span data-stu-id="c94f7-119">The following code example shows a possible implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface:</span></span>


```C++
//-----------------------------------------------------------
// Client implementation of IAudioSessionEvents interface.
// WASAPI calls these methods to notify the application when
// a parameter or property of the audio session changes.
//-----------------------------------------------------------
class CAudioSessionEvents : public IAudioSessionEvents
{
    LONG _cRef;

public:
    CAudioSessionEvents() :
        _cRef(1)
    {
    }

    ~CAudioSessionEvents()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID  riid,
                                VOID  **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioSessionEvents) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioSessionEvents*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Notification methods for audio session events

    HRESULT STDMETHODCALLTYPE OnDisplayNameChanged(
                                LPCWSTR NewDisplayName,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnIconPathChanged(
                                LPCWSTR NewIconPath,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSimpleVolumeChanged(
                                float NewVolume,
                                BOOL NewMute,
                                LPCGUID EventContext)
    {
        if (NewMute)
        {
            printf("MUTE\n");
        }
        else
        {
            printf("Volume = %d percent\n",
                   (UINT32)(100*NewVolume + 0.5));
        }

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnChannelVolumeChanged(
                                DWORD ChannelCount,
                                float NewChannelVolumeArray[],
                                DWORD ChangedChannel,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnGroupingParamChanged(
                                LPCGUID NewGroupingParam,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnStateChanged(
                                AudioSessionState NewState)
    {
        char *pszState = "?????";

        switch (NewState)
        {
        case AudioSessionStateActive:
            pszState = "active";
            break;
        case AudioSessionStateInactive:
            pszState = "inactive";
            break;
        }
        printf("New session state = %s\n", pszState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSessionDisconnected(
              AudioSessionDisconnectReason DisconnectReason)
    {
        char *pszReason = "?????";

        switch (DisconnectReason)
        {
        case DisconnectReasonDeviceRemoval:
            pszReason = "device removed";
            break;
        case DisconnectReasonServerShutdown:
            pszReason = "server shut down";
            break;
        case DisconnectReasonFormatChanged:
            pszReason = "format changed";
            break;
        case DisconnectReasonSessionLogoff:
            pszReason = "user logged off";
            break;
        case DisconnectReasonSessionDisconnected:
            pszReason = "session disconnected";
            break;
        case DisconnectReasonExclusiveModeOverride:
            pszReason = "exclusive-mode override";
            break;
        }
        printf("Audio session disconnected (reason: %s)\n",
               pszReason);

        return S_OK;
    }
};
```



<span data-ttu-id="c94f7-120">La classe CAudioSessionEvents de l’exemple de code précédent est une implémentation de l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="c94f7-120">The CAudioSessionEvents class in the preceding code example is an implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="c94f7-121">Cette implémentation particulière peut faire partie d’une application console qui imprime des informations sur les événements de session dans une fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="c94f7-121">This particular implementation might be part of a console application that prints information about session events to a Command Prompt window.</span></span> <span data-ttu-id="c94f7-122">Comme **IAudioSessionEvents** hérite de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), la définition de classe contient des implémentations des méthodes **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)et [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="c94f7-122">Because **IAudioSessionEvents** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="c94f7-123">Les autres méthodes publiques de la définition de classe sont spécifiques à l’interface **IAudioSessionEvents** .</span><span class="sxs-lookup"><span data-stu-id="c94f7-123">The remaining public methods in the class definition are specific to the **IAudioSessionEvents** interface.</span></span>

<span data-ttu-id="c94f7-124">Certains clients peuvent ne pas être intéressés par la surveillance de tous les types d’événements de session.</span><span class="sxs-lookup"><span data-stu-id="c94f7-124">Some clients might not be interested in monitoring all types of session events.</span></span> <span data-ttu-id="c94f7-125">Dans l’exemple de code précédent, plusieurs méthodes de notification de la classe CAudioSessionEvents ne font rien.</span><span class="sxs-lookup"><span data-stu-id="c94f7-125">In the preceding code example, several notification methods in the CAudioSessionEvents class do nothing.</span></span> <span data-ttu-id="c94f7-126">Par exemple, la méthode [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) n’a aucun effet à l’exception de renvoyer le code d’État S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c94f7-126">For example, the [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) method does nothing except to return status code S\_OK.</span></span> <span data-ttu-id="c94f7-127">Cette application n’analyse pas les volumes de canal, car elle ne change pas les volumes de canal (en appelant les méthodes dans l’interface [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) et ne partage pas la session avec d’autres applications susceptibles de modifier les volumes de canal.</span><span class="sxs-lookup"><span data-stu-id="c94f7-127">This application does not monitor channel volumes because it does not change the channel volumes (by calling the methods in the [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) interface), and it does not share the session with other applications that might change the channel volumes.</span></span>

<span data-ttu-id="c94f7-128">Les trois méthodes de la classe CAudioSessionEvents qui notifient l’utilisateur des événements de session sont [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)et [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span><span class="sxs-lookup"><span data-stu-id="c94f7-128">The only three methods in the CAudioSessionEvents class that notify the user of session events are [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged), and [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span></span> <span data-ttu-id="c94f7-129">Par exemple, si l’utilisateur exécute le programme de contrôle de volume système, sndvol, et utilise le contrôle de volume dans sndvol pour modifier le niveau de volume de l’application, `OnSimpleVolumeChanged` imprime immédiatement le nouveau niveau de volume.</span><span class="sxs-lookup"><span data-stu-id="c94f7-129">For example, if the user runs the system volume-control program, Sndvol, and uses the volume control in Sndvol to change the application's volume level, `OnSimpleVolumeChanged` immediately prints the new volume level.</span></span>

<span data-ttu-id="c94f7-130">Pour obtenir un exemple de code qui inscrit et annule l’inscription de l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) d’un client, consultez la rubrique [événements audio pour les applications audio héritées](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="c94f7-130">For a code example that registers and unregisters a client's [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c94f7-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c94f7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c94f7-132">Sessions audio</span><span class="sxs-lookup"><span data-stu-id="c94f7-132">Audio Sessions</span></span>](audio-sessions.md)
</dt> </dl>

 

 
