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
# <a name="step-1-declare-the-cplayer-class"></a><span data-ttu-id="da8ad-103">Étape 1 : déclarer la classe CPlayer</span><span class="sxs-lookup"><span data-stu-id="da8ad-103">Step 1: Declare the CPlayer Class</span></span>

<span data-ttu-id="da8ad-104">Cette rubrique est l’étape 1 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="da8ad-104">This topic is step 1 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="da8ad-105">Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="da8ad-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="da8ad-106">Dans ce didacticiel, la fonctionnalité de lecture est encapsulée dans la `CPlayer` classe.</span><span class="sxs-lookup"><span data-stu-id="da8ad-106">In this tutorial, playback functionality is encapsulated in the `CPlayer` class.</span></span> <span data-ttu-id="da8ad-107">La classe `CPlayer` est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="da8ad-107">The `CPlayer` class is declared as follows:</span></span>


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



<span data-ttu-id="da8ad-108">Voici quelques points à noter `CPlayer` :</span><span class="sxs-lookup"><span data-stu-id="da8ad-108">Here are some things to note about `CPlayer`:</span></span>

-   <span data-ttu-id="da8ad-109">L' **événement de \_ \_ joueur d' \_ application WM** constant définit un message de fenêtre privée.</span><span class="sxs-lookup"><span data-stu-id="da8ad-109">The constant **WM\_APP\_PLAYER\_EVENT** defines a private window message.</span></span> <span data-ttu-id="da8ad-110">Ce message est utilisé pour notifier l’application des événements de session multimédia.</span><span class="sxs-lookup"><span data-stu-id="da8ad-110">This message is used to notify the application about Media Session events.</span></span> <span data-ttu-id="da8ad-111">Consultez [étape 5 : gérer les événements de session multimédia](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="da8ad-111">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>
-   <span data-ttu-id="da8ad-112">L' `PlayerState` énumération définit les États possibles de l' `CPlayer` objet.</span><span class="sxs-lookup"><span data-stu-id="da8ad-112">The `PlayerState` enumeration defines the possible states of the `CPlayer` object.</span></span>
-   <span data-ttu-id="da8ad-113">La `CPlayer` classe implémente l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , qui est utilisée pour recevoir des notifications d’événements à partir de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="da8ad-113">The `CPlayer` class implements the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which is used to get event notifications from the Media Session.</span></span>
-   <span data-ttu-id="da8ad-114">Le `CPlayer` constructeur est privé.</span><span class="sxs-lookup"><span data-stu-id="da8ad-114">The `CPlayer` constructor is private.</span></span> <span data-ttu-id="da8ad-115">L’application appelle la `CreateInstance` méthode statique pour créer une instance de la `CPlayer` classe.</span><span class="sxs-lookup"><span data-stu-id="da8ad-115">The application calls the static `CreateInstance` method to create an instance of the `CPlayer` class.</span></span>
-   <span data-ttu-id="da8ad-116">Le `CPlayer` destructeur est également privé.</span><span class="sxs-lookup"><span data-stu-id="da8ad-116">The `CPlayer` destructor is also private.</span></span> <span data-ttu-id="da8ad-117">La `CPlayer` classe implémente **IUnknown**, de sorte que la durée de vie de l’objet est contrôlée par son décompte de références (*m \_ nRefCount*).</span><span class="sxs-lookup"><span data-stu-id="da8ad-117">The `CPlayer` class implements **IUnknown**, so the object's lifetime is controlled through its reference count (*m\_nRefCount*).</span></span> <span data-ttu-id="da8ad-118">Pour détruire l’objet, l’application appelle **IUnknown :: Release**, et non **Delete**.</span><span class="sxs-lookup"><span data-stu-id="da8ad-118">To destroy the object, the application calls **IUnknown::Release**, not **delete**.</span></span>
-   <span data-ttu-id="da8ad-119">L' `CPlayer` objet gère à la fois la session multimédia et la source du média.</span><span class="sxs-lookup"><span data-stu-id="da8ad-119">The `CPlayer` object manages both the Media Session and the media source.</span></span>

## <a name="implement-iunknown"></a><span data-ttu-id="da8ad-120">Implémenter IUnknown</span><span class="sxs-lookup"><span data-stu-id="da8ad-120">Implement IUnknown</span></span>

<span data-ttu-id="da8ad-121">La `CPlayer` classe implémente [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), qui hérite de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="da8ad-121">The `CPlayer` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), which inherits **IUnknown**.</span></span>

<span data-ttu-id="da8ad-122">Le code présenté ici est une implémentation relativement standard de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="da8ad-122">The code shown here is a fairly standard implementation of **IUnknown**.</span></span> <span data-ttu-id="da8ad-123">Si vous préférez, vous pouvez utiliser la Active Template Library (ATL) pour implémenter ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="da8ad-123">If you prefer, you can use the Active Template Library (ATL) to implement these methods.</span></span> <span data-ttu-id="da8ad-124">Toutefois, `CPlayer` ne prend pas en charge [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ni les fonctionnalités com avancées, donc il n’y a aucune raison d’utiliser ATL ici.</span><span class="sxs-lookup"><span data-stu-id="da8ad-124">However, `CPlayer` does not support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or any advanced COM features, so there is no overwhelming reason to use ATL here.</span></span>


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



<span data-ttu-id="da8ad-125">[Étape 2 : créer l’objet CPlayer](step-2--create-the-cplayer-object.md)</span><span class="sxs-lookup"><span data-stu-id="da8ad-125">Next: [Step 2: Create the CPlayer Object](step-2--create-the-cplayer-object.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="da8ad-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da8ad-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da8ad-127">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="da8ad-127">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="da8ad-128">Comment lire des fichiers multimédias avec Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da8ad-128">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
