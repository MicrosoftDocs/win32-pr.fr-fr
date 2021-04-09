---
description: L’expérience de l’utilisation de l’environnement par défaut fournie par le système permet d’obtenir tous les flux de communication non disponibles dans le système lorsqu’un flux de communication s’ouvre.
ms.assetid: 1b92574e-7cde-49c0-a68e-223492412361
title: Considérations relatives à l’implémentation pour l’installation de notifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de07ea23b7cdc8d726ab68a5a6554bf1713a921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110938"
---
# <a name="implementation-considerations-for-ducking-notifications"></a><span data-ttu-id="0df45-103">Considérations relatives à l’implémentation pour l’installation de notifications</span><span class="sxs-lookup"><span data-stu-id="0df45-103">Implementation Considerations for Ducking Notifications</span></span>

<span data-ttu-id="0df45-104">L’expérience de l’utilisation de l' [environnement par défaut](stream-attenuation.md) fournie par le système permet d’obtenir tous les flux de communication non disponibles dans le système lorsqu’un flux de communication s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="0df45-104">The [Default Ducking Experience](stream-attenuation.md) provided by the system ducks all non-communication streams available in the system when a communication stream opens.</span></span> <span data-ttu-id="0df45-105">Une application multimédia peut remplacer la gestion par défaut si elle connaît le début et la fin de la session de communication.</span><span class="sxs-lookup"><span data-stu-id="0df45-105">A media application can override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="0df45-106">Examinez le scénario implémenté par l’application multimédia dans l’exemple [DuckingMediaPlayer](duckingmediaplayer.md) .</span><span class="sxs-lookup"><span data-stu-id="0df45-106">Consider the scenario implemented by the media application in the [DuckingMediaPlayer](duckingmediaplayer.md) sample.</span></span> <span data-ttu-id="0df45-107">L’application interrompt le flux audio qu’elle lit lorsqu’elle reçoit une notification de canard et poursuit la lecture lorsqu’elle reçoit une notification de désduck.</span><span class="sxs-lookup"><span data-stu-id="0df45-107">The application pauses the audio stream that it is playing when it receives a duck notification and continues playback when it receives an unduck notification.</span></span> <span data-ttu-id="0df45-108">Les événements suspendre et continuer sont reflétés dans l’interface utilisateur de l’application multimédia.</span><span class="sxs-lookup"><span data-stu-id="0df45-108">The pause and continue events are reflected in the media application's user interface.</span></span> <span data-ttu-id="0df45-109">Cela est pris en charge par le biais de deux messages de fenêtre définis par l’application, de la \_ session d’application WM \_ \_ et de la session d' \_ application WM \_ \_ désintégrée.</span><span class="sxs-lookup"><span data-stu-id="0df45-109">This is supported through two application-defined window messages, WM\_APP\_SESSION\_DUCKED and WM\_APP\_SESSION\_UNDUCKED.</span></span> <span data-ttu-id="0df45-110">Les notifications de l’canard sont reçues de façon asynchrone en arrière-plan et l’application multimédia ne doit pas bloquer le thread de notification pour traiter les messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0df45-110">The ducking notifications are received asynchronously in the background and the media application must not block the notification thread to process the window messages.</span></span> <span data-ttu-id="0df45-111">Les messages de fenêtre doivent être traités sur le thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0df45-111">The window messages must be processed on the user interface thread.</span></span>

<span data-ttu-id="0df45-112">Le comportement d’un canard fonctionne via un mécanisme de notification.</span><span class="sxs-lookup"><span data-stu-id="0df45-112">The ducking behavior works through a notification mechanism.</span></span> <span data-ttu-id="0df45-113">Pour fournir une expérience personnalisée, l’application multimédia doit implémenter l’interface [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) et inscrire l’implémentation auprès du système audio.</span><span class="sxs-lookup"><span data-stu-id="0df45-113">To provide a customized experience, the media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="0df45-114">Une fois l’inscription réussie, l’application multimédia reçoit des notifications d’événements sous la forme de rappels via les méthodes de l’interface.</span><span class="sxs-lookup"><span data-stu-id="0df45-114">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="0df45-115">Le gestionnaire de sessions qui gère la session de communication appelle [**IAudioVolumeDuckNotification :: OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) lorsque le flux de communication s’ouvre, puis appelle [**IAudioVolumeDuckNotification :: OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) lorsque le flux est fermé sur le périphérique de communication.</span><span class="sxs-lookup"><span data-stu-id="0df45-115">The session manager handling the communication session calls [**IAudioVolumeDuckNotification::OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) when the communication stream opens and then calls [**IAudioVolumeDuckNotification::OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) when the stream is closed on the communication device.</span></span>

<span data-ttu-id="0df45-116">Le code suivant illustre un exemple d’implémentation de l’interface [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) .</span><span class="sxs-lookup"><span data-stu-id="0df45-116">The following code shows a sample implementation of the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface.</span></span> <span data-ttu-id="0df45-117">Pour obtenir la définition de CMediaPlayer ::D uckingOptOut, consultez l’article sur l’obtention d’événements d’un appareil de communication.</span><span class="sxs-lookup"><span data-stu-id="0df45-117">For the definition of CMediaPlayer::DuckingOptOut, see Getting Ducking Events from a Communication Device.</span></span>


```C++
class CMediaPlayer : public IAudioVolumeDuckNotification
{
    LONG _refCount;

    HWND _AppWindow;

    ~CMediaPlayer();

    STDMETHOD(OnVolumeDuckNotification) (LPCWSTR sessionID, 
                  UINT32 countCommunicationSessions);
    STDMETHOD(OnVolumeUnduckNotification) (LPCWSTR sessionID);

public:
    CDuckingImpl(HWND hWnd);
    HRESULT DuckingOptOut(bool GetDuckEvents);

    // IUnknown
    IFACEMETHODIMP QueryInterface(__in REFIID riid, __deref_out void **ppv);
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
};

CMediaPlayer::CMediaPlayer(HWND AppWindow) :
        _AppWindow(AppWindow),
        _refCount(1)
{
}
CMediaPlayer::~CMediaPlayer()
{
}

// When we receive a duck notification, 
// post a "Session Ducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeDuckNotification(LPCWSTR SessionID, 
                                                    UINT32 CountCommunicationsSessions)
{
    PostMessage(_AppWindow, WM_APP_SESSION_DUCKED, 0, 0);
    return 0;
}


// When we receive an unduck notification, 
// post a "Session Unducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeUnduckNotification(LPCWSTR SessionID)
{
    PostMessage(_AppWindow, WM_APP_SESSION_UNDUCKED, 0, 0);
    return 0;
}

IFACEMETHODIMP CMediaPlayer::QueryInterface(REFIID iid, void **pvObject)
{
    if (pvObject == NULL)
    {
        return E_POINTER;
    }
    *pvObject = NULL;
    if (iid == IID_IUnknown)
    {
        *pvObject = static_cast<IUnknown *>(static_cast<IAudioVolumeDuckNotification *>
                                                                              (this));
        AddRef();
    }
    else if (iid == __uuidof(IAudioVolumeDuckNotification))
    {
        *pvObject = static_cast<IAudioVolumeDuckNotification *>(this);
        AddRef();
    }
    else
    {
        return E_NOINTERFACE;
    }
    return S_OK;
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::AddRef()
{
    return InterlockedIncrement(&_refCount);
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::Release()
{
    LONG refs = InterlockedDecrement(&_refCount);

    if (refs == 0)
    {
        delete this; 
    }

    return refs;   
}
```



## <a name="related-topics"></a><span data-ttu-id="0df45-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0df45-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0df45-119">Utilisation d’un appareil de communication</span><span class="sxs-lookup"><span data-stu-id="0df45-119">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="0df45-120">Expérience de l’utilisation des canards par défaut</span><span class="sxs-lookup"><span data-stu-id="0df45-120">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="0df45-121">Désactivation de l’expérience de l’utilisation des canards par défaut</span><span class="sxs-lookup"><span data-stu-id="0df45-121">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="0df45-122">Fournir un comportement de canard personnalisé</span><span class="sxs-lookup"><span data-stu-id="0df45-122">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="0df45-123">Obtention d’événements de canard</span><span class="sxs-lookup"><span data-stu-id="0df45-123">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



