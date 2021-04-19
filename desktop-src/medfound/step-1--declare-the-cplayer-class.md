---
description: Cette rubrique est l’étape 1 du didacticiel comment lire des fichiers multimédias avec Media Foundation.
ms.assetid: 10767bbf-3b47-4df1-be73-18678397c0ab
title: 'Étape 1 : déclarer la classe CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1593842ecece68fcd3c4cca35a7e2e28eac503c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531677"
---
# <a name="step-1-declare-the-cplayer-class"></a>Étape 1 : déclarer la classe CPlayer

Cette rubrique est l’étape 1 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md). Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).

Dans ce didacticiel, la fonctionnalité de lecture est encapsulée dans la `CPlayer` classe. La classe `CPlayer` est déclarée comme suit :


```C++
const UINT WM_APP_PLAYER_EVENT = WM_APP + 1;   

    // WPARAM = IMFMediaEvent*, WPARAM = MediaEventType

enum PlayerState
{
    Closed = 0,     // No session.
    Ready,          // Session was created, ready to open a file. 
    OpenPending,    // Session is opening a file.
    Started,        // Session is playing a file.
    Paused,         // Session is paused.
    Stopped,        // Session is stopped (ready to play). 
    Closing         // Application has closed the session, but is waiting for MESessionClosed.
};

class CPlayer : public IMFAsyncCallback
{
public:
    static HRESULT CreateInstance(HWND hVideo, HWND hEvent, CPlayer **ppPlayer);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP  GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP  Invoke(IMFAsyncResult* pAsyncResult);

    // Playback
    HRESULT       OpenURL(const WCHAR *sURL);
    HRESULT       Play();
    HRESULT       Pause();
    HRESULT       Stop();
    HRESULT       Shutdown();
    HRESULT       HandleEvent(UINT_PTR pUnkPtr);
    PlayerState   GetState() const { return m_state; }

    // Video functionality
    HRESULT       Repaint();
    HRESULT       ResizeVideo(WORD width, WORD height);
    
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }

protected:
    
    // Constructor is private. Use static CreateInstance method to instantiate.
    CPlayer(HWND hVideo, HWND hEvent);

    // Destructor is private. Caller should call Release.
    virtual ~CPlayer(); 

    HRESULT Initialize();
    HRESULT CreateSession();
    HRESULT CloseSession();
    HRESULT StartPlayback();

    // Media event handlers
    virtual HRESULT OnTopologyStatus(IMFMediaEvent *pEvent);
    virtual HRESULT OnPresentationEnded(IMFMediaEvent *pEvent);
    virtual HRESULT OnNewPresentation(IMFMediaEvent *pEvent);

    // Override to handle additional session events.
    virtual HRESULT OnSessionEvent(IMFMediaEvent*, MediaEventType) 
    { 
        return S_OK; 
    }

protected:
    long                    m_nRefCount;        // Reference count.

    IMFMediaSession         *m_pSession;
    IMFMediaSource          *m_pSource;
    IMFVideoDisplayControl  *m_pVideoDisplay;

    HWND                    m_hwndVideo;        // Video window.
    HWND                    m_hwndEvent;        // App window to receive events.
    PlayerState             m_state;            // Current state of the media session.
    HANDLE                  m_hCloseEvent;      // Event to wait on while closing.
};
```



Voici quelques points à noter `CPlayer` :

-   L' **événement de \_ \_ joueur d' \_ application WM** constant définit un message de fenêtre privée. Ce message est utilisé pour notifier l’application des événements de session multimédia. Consultez [étape 5 : gérer les événements de session multimédia](step-5--handle-media-session-events.md).
-   L' `PlayerState` énumération définit les États possibles de l' `CPlayer` objet.
-   La `CPlayer` classe implémente l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , qui est utilisée pour recevoir des notifications d’événements à partir de la session multimédia.
-   Le `CPlayer` constructeur est privé. L’application appelle la `CreateInstance` méthode statique pour créer une instance de la `CPlayer` classe.
-   Le `CPlayer` destructeur est également privé. La `CPlayer` classe implémente **IUnknown**, de sorte que la durée de vie de l’objet est contrôlée par son décompte de références (*m \_ nRefCount*). Pour détruire l’objet, l’application appelle **IUnknown :: Release**, et non **Delete**.
-   L' `CPlayer` objet gère à la fois la session multimédia et la source du média.

## <a name="implement-iunknown"></a>Implémenter IUnknown

La `CPlayer` classe implémente [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), qui hérite de **IUnknown**.

Le code présenté ici est une implémentation relativement standard de **IUnknown**. Si vous préférez, vous pouvez utiliser la Active Template Library (ATL) pour implémenter ces méthodes. Toutefois, `CPlayer` ne prend pas en charge [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ni les fonctionnalités com avancées, donc il n’y a aucune raison d’utiliser ATL ici.


```C++
HRESULT CPlayer::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CPlayer, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

ULONG CPlayer::AddRef()
{
    return InterlockedIncrement(&m_nRefCount);
}

ULONG CPlayer::Release()
{
    ULONG uCount = InterlockedDecrement(&m_nRefCount);
    if (uCount == 0)
    {
        delete this;
    }
    return uCount;
}
```



[Étape 2 : créer l’objet CPlayer](step-2--create-the-cplayer-object.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> <dt>

[Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
