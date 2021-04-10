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
# <a name="audio-session-events"></a>Événements de session audio

Une application qui gère des flux audio en mode partagé peut s’inscrire pour recevoir des notifications lorsque des événements de session se produisent. Comme expliqué précédemment, chaque flux appartient à une [session audio](audio-sessions.md). Un événement de session est initié par une modification de l’état d’une session audio.

Une application cliente peut s’inscrire pour recevoir des notifications des types d’événements de session suivants :

-   Le niveau du volume principal ou l’état d’inactivation du mixage secondaire de la session a changé.
-   Le niveau de volume d’un ou plusieurs canaux du mixage secondaire de session a changé.
-   La session a été déconnectée.
-   L’état de l’activité de la session est passé à actif, inactif ou expiré.
-   Un nouveau paramètre de regroupement a été affecté à la session.
-   Une propriété de l’interface utilisateur de la session (icône ou nom d’affichage) a changé.

Le client reçoit les notifications de ces événements par le biais des méthodes dans son implémentation de l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Contrairement aux autres interfaces dans WASAPI, qui sont implémentées par le module système WASAPI, le client implémente **IAudioSessionEvents**. Les méthodes de cette interface reçoivent des rappels du module système WASAPI lorsque des événements de session se produisent.

Pour commencer à recevoir des notifications, le client appelle la méthode [**IAudioSessionControl :: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) pour inscrire son interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Lorsque le client n’a plus besoin de notifications, il appelle la méthode [**IAudioSessionControl :: UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) pour supprimer l’inscription.

L’exemple de code suivant montre une implémentation possible de l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) :


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



La classe CAudioSessionEvents de l’exemple de code précédent est une implémentation de l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Cette implémentation particulière peut faire partie d’une application console qui imprime des informations sur les événements de session dans une fenêtre d’invite de commandes. Comme **IAudioSessionEvents** hérite de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), la définition de classe contient des implémentations des méthodes **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)et [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Les autres méthodes publiques de la définition de classe sont spécifiques à l’interface **IAudioSessionEvents** .

Certains clients peuvent ne pas être intéressés par la surveillance de tous les types d’événements de session. Dans l’exemple de code précédent, plusieurs méthodes de notification de la classe CAudioSessionEvents ne font rien. Par exemple, la méthode [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) n’a aucun effet à l’exception de renvoyer le code d’État S \_ OK. Cette application n’analyse pas les volumes de canal, car elle ne change pas les volumes de canal (en appelant les méthodes dans l’interface [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) et ne partage pas la session avec d’autres applications susceptibles de modifier les volumes de canal.

Les trois méthodes de la classe CAudioSessionEvents qui notifient l’utilisateur des événements de session sont [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)et [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Par exemple, si l’utilisateur exécute le programme de contrôle de volume système, sndvol, et utilise le contrôle de volume dans sndvol pour modifier le niveau de volume de l’application, `OnSimpleVolumeChanged` imprime immédiatement le nouveau niveau de volume.

Pour obtenir un exemple de code qui inscrit et annule l’inscription de l’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) d’un client, consultez la rubrique [événements audio pour les applications audio héritées](audio-events-for-legacy-audio-applications.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sessions audio](audio-sessions.md)
</dt> </dl>

 

 
