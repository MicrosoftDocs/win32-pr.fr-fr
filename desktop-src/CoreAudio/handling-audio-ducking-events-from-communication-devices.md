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
# <a name="implementation-considerations-for-ducking-notifications"></a>Considérations relatives à l’implémentation pour l’installation de notifications

L’expérience de l’utilisation de l' [environnement par défaut](stream-attenuation.md) fournie par le système permet d’obtenir tous les flux de communication non disponibles dans le système lorsqu’un flux de communication s’ouvre. Une application multimédia peut remplacer la gestion par défaut si elle connaît le début et la fin de la session de communication.

Examinez le scénario implémenté par l’application multimédia dans l’exemple [DuckingMediaPlayer](duckingmediaplayer.md) . L’application interrompt le flux audio qu’elle lit lorsqu’elle reçoit une notification de canard et poursuit la lecture lorsqu’elle reçoit une notification de désduck. Les événements suspendre et continuer sont reflétés dans l’interface utilisateur de l’application multimédia. Cela est pris en charge par le biais de deux messages de fenêtre définis par l’application, de la \_ session d’application WM \_ \_ et de la session d' \_ application WM \_ \_ désintégrée. Les notifications de l’canard sont reçues de façon asynchrone en arrière-plan et l’application multimédia ne doit pas bloquer le thread de notification pour traiter les messages de fenêtre. Les messages de fenêtre doivent être traités sur le thread d’interface utilisateur.

Le comportement d’un canard fonctionne via un mécanisme de notification. Pour fournir une expérience personnalisée, l’application multimédia doit implémenter l’interface [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) et inscrire l’implémentation auprès du système audio. Une fois l’inscription réussie, l’application multimédia reçoit des notifications d’événements sous la forme de rappels via les méthodes de l’interface. Le gestionnaire de sessions qui gère la session de communication appelle [**IAudioVolumeDuckNotification :: OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) lorsque le flux de communication s’ouvre, puis appelle [**IAudioVolumeDuckNotification :: OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) lorsque le flux est fermé sur le périphérique de communication.

Le code suivant illustre un exemple d’implémentation de l’interface [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) . Pour obtenir la définition de CMediaPlayer ::D uckingOptOut, consultez l’article sur l’obtention d’événements d’un appareil de communication.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’un appareil de communication](using-the-communication-device.md)
</dt> <dt>

[Expérience de l’utilisation des canards par défaut](stream-attenuation.md)
</dt> <dt>

[Désactivation de l’expérience de l’utilisation des canards par défaut](disabling-the-ducking-experience.md)
</dt> <dt>

[Fournir un comportement de canard personnalisé](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Obtention d’événements de canard](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



