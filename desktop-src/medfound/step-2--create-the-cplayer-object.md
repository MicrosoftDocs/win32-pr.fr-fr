---
description: Cette rubrique est l’étape 2 du didacticiel comment lire des fichiers multimédias avec Media Foundation.
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: 'Étape 2 : créer l’objet CPlayer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021ffa383506c0ab1be8d6c1ca327f67ed8f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517737"
---
# <a name="step-2-create-the-cplayer-object"></a><span data-ttu-id="989cc-103">Étape 2 : créer l’objet CPlayer</span><span class="sxs-lookup"><span data-stu-id="989cc-103">Step 2: Create the CPlayer Object</span></span>

<span data-ttu-id="989cc-104">Cette rubrique est l’étape 2 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="989cc-104">This topic is step 2 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="989cc-105">Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="989cc-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="989cc-106">Pour créer une instance de la `CPlayer` classe, l’application appelle la `CPlayer::CreateInstance` méthode statique.</span><span class="sxs-lookup"><span data-stu-id="989cc-106">To create an instance of the `CPlayer` class, the application calls the static `CPlayer::CreateInstance` method.</span></span> <span data-ttu-id="989cc-107">Cette méthode accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="989cc-107">This method takes the following parameters:</span></span>

-   <span data-ttu-id="989cc-108">*hVideo* spécifie la fenêtre qui affiche la vidéo.</span><span class="sxs-lookup"><span data-stu-id="989cc-108">*hVideo* specifies the window to display video.</span></span>
-   <span data-ttu-id="989cc-109">*hEvent* spécifie une fenêtre pour recevoir des événements.</span><span class="sxs-lookup"><span data-stu-id="989cc-109">*hEvent* specifies a window to receive events.</span></span> <span data-ttu-id="989cc-110">Il est possible de passer le même handle pour les deux handles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="989cc-110">It is valid to pass the same handle for both window handles.</span></span>
-   <span data-ttu-id="989cc-111">*ppPlayer* reçoit un pointeur vers une nouvelle `CPlayer` instance.</span><span class="sxs-lookup"><span data-stu-id="989cc-111">*ppPlayer* receives a pointer to a new `CPlayer` instance.</span></span>

<span data-ttu-id="989cc-112">Le code suivant montre la méthode `CreateInstance` :</span><span class="sxs-lookup"><span data-stu-id="989cc-112">The following code shows the `CreateInstance` method:</span></span>


```C++
//  Static class method to create the CPlayer object.

HRESULT CPlayer::CreateInstance(
    HWND hVideo,                  // Video window.
    HWND hEvent,                  // Window to receive notifications.
    CPlayer **ppPlayer)           // Receives a pointer to the CPlayer object.
{
    if (ppPlayer == NULL)
    {
        return E_POINTER;
    }

    CPlayer *pPlayer = new (std::nothrow) CPlayer(hVideo, hEvent);
    if (pPlayer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pPlayer->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppPlayer = pPlayer;
    }
    else
    {
        pPlayer->Release();
    }
    return hr;
}

HRESULT CPlayer::Initialize()
{
    // Start up Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        m_hCloseEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
        if (m_hCloseEvent == NULL)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    return hr;
}
```



<span data-ttu-id="989cc-113">Le code suivant illustre le `CPlayer` constructeur :</span><span class="sxs-lookup"><span data-stu-id="989cc-113">The following code shows the `CPlayer` constructor:</span></span>


```C++
CPlayer::CPlayer(HWND hVideo, HWND hEvent) : 
    m_pSession(NULL),
    m_pSource(NULL),
    m_pVideoDisplay(NULL),
    m_hwndVideo(hVideo),
    m_hwndEvent(hEvent),
    m_state(Closed),
    m_hCloseEvent(NULL),
    m_nRefCount(1)
{
}
```



<span data-ttu-id="989cc-114">Le constructeur effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="989cc-114">The constructor does the following:</span></span>

1.  <span data-ttu-id="989cc-115">Appelle [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) pour initialiser la plateforme Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="989cc-115">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="989cc-116">Crée un événement de réinitialisation automatique.</span><span class="sxs-lookup"><span data-stu-id="989cc-116">Creates an auto-reset event.</span></span> <span data-ttu-id="989cc-117">Cet événement est utilisé lors de la fermeture de la session multimédia ; Voir [étape 7 : arrêter la session multimédia](step-7--shut-down-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="989cc-117">This event is used when closing the Media Session; see [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>

<span data-ttu-id="989cc-118">Le destructeur arrête la session multimédia, comme décrit à [l’étape 7 : arrêter la session multimédia](step-7--shut-down-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="989cc-118">The destructor shuts down the Media Session, as described in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>


```C++
CPlayer::~CPlayer()
{
    assert(m_pSession == NULL);  
    // If FALSE, the app did not call Shutdown().

    // When CPlayer calls IMediaEventGenerator::BeginGetEvent on the
    // media session, it causes the media session to hold a reference 
    // count on the CPlayer. 
    
    // This creates a circular reference count between CPlayer and the 
    // media session. Calling Shutdown breaks the circular reference 
    // count.

    // If CreateInstance fails, the application will not call 
    // Shutdown. To handle that case, call Shutdown in the destructor. 

    Shutdown();
}
```



<span data-ttu-id="989cc-119">Notez que le constructeur et le destructeur sont tous deux des méthodes de classe protégées.</span><span class="sxs-lookup"><span data-stu-id="989cc-119">Note that the constructor and destructor are both protected class methods.</span></span> <span data-ttu-id="989cc-120">L’application crée l’objet à l’aide de la `CreateInstance` méthode statique.</span><span class="sxs-lookup"><span data-stu-id="989cc-120">The application creates the object using the static `CreateInstance` method.</span></span> <span data-ttu-id="989cc-121">Elle détruit l’objet en appelant **IUnknown :: Release**, plutôt que de **supprimer** explicitement.</span><span class="sxs-lookup"><span data-stu-id="989cc-121">It destroys the object by calling **IUnknown::Release**, rather than explicitly using **delete**.</span></span>

<span data-ttu-id="989cc-122">Suivant : [étape 3 : ouvrir un fichier multimédia](step-3--open-a-media-file.md)</span><span class="sxs-lookup"><span data-stu-id="989cc-122">Next: [Step 3: Open a Media File](step-3--open-a-media-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="989cc-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="989cc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="989cc-124">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="989cc-124">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="989cc-125">Comment lire des fichiers multimédias avec Media Foundation</span><span class="sxs-lookup"><span data-stu-id="989cc-125">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



