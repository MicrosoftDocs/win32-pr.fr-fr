---
description: Cette rubrique est l’étape 5 du didacticiel comment lire des fichiers multimédias avec Media Foundation.
ms.assetid: db9b896f-6f56-47b1-b129-331c984e0b16
title: 'Étape 5 : gérer les événements de session multimédia'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ea3092189644f800a5cb27d2e8b07744f5d90c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525806"
---
# <a name="step-5-handle-media-session-events"></a><span data-ttu-id="744a4-103">Étape 5 : gérer les événements de session multimédia</span><span class="sxs-lookup"><span data-stu-id="744a4-103">Step 5: Handle Media Session Events</span></span>

<span data-ttu-id="744a4-104">Cette rubrique est l’étape 5 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="744a4-104">This topic is step 5 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="744a4-105">Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="744a4-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="744a4-106">Pour plus d’informations sur cette rubrique, consultez l’article sur les [générateurs d’événements multimédias](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="744a4-106">For background on this topic, read [Media Event Generators](media-event-generators.md).</span></span> <span data-ttu-id="744a4-107">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="744a4-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="744a4-108">Obtention d’événements de session</span><span class="sxs-lookup"><span data-stu-id="744a4-108">Getting Session Events</span></span>](#getting-session-events)
-   [<span data-ttu-id="744a4-109">MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="744a4-109">MESessionTopologyStatus</span></span>](#mesessiontopologystatus)
-   [<span data-ttu-id="744a4-110">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="744a4-110">MEEndOfPresentation</span></span>](#meendofpresentation)
-   [<span data-ttu-id="744a4-111">MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="744a4-111">MENewPresentation</span></span>](#menewpresentation)
-   [<span data-ttu-id="744a4-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="744a4-112">Related topics</span></span>](#related-topics)

## <a name="getting-session-events"></a><span data-ttu-id="744a4-113">Obtention d’événements de session</span><span class="sxs-lookup"><span data-stu-id="744a4-113">Getting Session Events</span></span>

<span data-ttu-id="744a4-114">Pour obtenir des événements de la session multimédia, l’objet CPlayer appelle la méthode [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) , comme indiqué à [l’étape 4 : créer la session multimédia](step-4--create-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="744a4-114">To get events from the Media Session, the CPlayer object calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method, as shown in [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span> <span data-ttu-id="744a4-115">Cette méthode est asynchrone, ce qui signifie qu’elle retourne immédiatement à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="744a4-115">This method is asynchronous, meaning it returns to the caller immediately.</span></span> <span data-ttu-id="744a4-116">Lorsque l’événement de session suivant se produit, la session multimédia appelle la méthode [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de l’objet CPlayer.</span><span class="sxs-lookup"><span data-stu-id="744a4-116">When the next session event occurs, the Media Session calls the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the CPlayer object.</span></span>

<span data-ttu-id="744a4-117">Il est important de se souvenir que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) est appelé à partir d’un thread de travail, et non du thread d’application.</span><span class="sxs-lookup"><span data-stu-id="744a4-117">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) gets called from a worker thread, not from the application thread.</span></span> <span data-ttu-id="744a4-118">Par conséquent, l’implémentation de **Invoke** doit être de sécurité multithread.</span><span class="sxs-lookup"><span data-stu-id="744a4-118">Therefore, the implementation of **Invoke** must be multithread-safe.</span></span> <span data-ttu-id="744a4-119">Une approche consisterait à protéger les données de membre à l’aide d’une section critique.</span><span class="sxs-lookup"><span data-stu-id="744a4-119">One approach would be to protect the member data with a critical section.</span></span> <span data-ttu-id="744a4-120">Toutefois, la `CPlayer` classe illustre une approche alternative :</span><span class="sxs-lookup"><span data-stu-id="744a4-120">However, the `CPlayer` class shows an alternative approach:</span></span>

1.  <span data-ttu-id="744a4-121">Dans la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , l’objet CPlayer publie un message d’événement de **lecteur d' \_ application \_ \_ WM** dans l’application.</span><span class="sxs-lookup"><span data-stu-id="744a4-121">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the CPlayer object posts a **WM\_APP\_PLAYER\_EVENT** message to the application.</span></span> <span data-ttu-id="744a4-122">Le paramètre de message est un pointeur [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="744a4-122">The message parameter is an [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
2.  <span data-ttu-id="744a4-123">L’application reçoit le message d' **\_ événement du \_ lecteur \_ d’application WM** .</span><span class="sxs-lookup"><span data-stu-id="744a4-123">The application receives the **WM\_APP\_PLAYER\_EVENT** message.</span></span>
3.  <span data-ttu-id="744a4-124">L’application appelle la `CPlayer::HandleEvent` méthode, en passant le pointeur [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="744a4-124">The application calls the `CPlayer::HandleEvent` method, passing in the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
4.  <span data-ttu-id="744a4-125">La `HandleEvent` méthode répond à l’événement.</span><span class="sxs-lookup"><span data-stu-id="744a4-125">The `HandleEvent` method responds to the event.</span></span>

<span data-ttu-id="744a4-126">Le code suivant illustre la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) :</span><span class="sxs-lookup"><span data-stu-id="744a4-126">The following code shows the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method:</span></span>


```C++
//  Callback for the asynchronous BeginGetEvent method.

HRESULT CPlayer::Invoke(IMFAsyncResult *pResult)
{
    MediaEventType meType = MEUnknown;  // Event type

    IMFMediaEvent *pEvent = NULL;

    // Get the event from the event queue.
    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event type. 
    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (meType == MESessionClosed)
    {
        // The session was closed. 
        // The application is waiting on the m_hCloseEvent event handle. 
        SetEvent(m_hCloseEvent);
    }
    else
    {
        // For all other events, get the next event in the queue.
        hr = m_pSession->BeginGetEvent(this, NULL);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Check the application state. 
        
    // If a call to IMFMediaSession::Close is pending, it means the 
    // application is waiting on the m_hCloseEvent event and
    // the application's message loop is blocked. 

    // Otherwise, post a private window message to the application. 

    if (m_state != Closing)
    {
        // Leave a reference count on the event.
        pEvent->AddRef();

        PostMessage(m_hwndEvent, WM_APP_PLAYER_EVENT, 
            (WPARAM)pEvent, (LPARAM)meType);
    }

done:
    SafeRelease(&pEvent);
    return S_OK;
}
```



<span data-ttu-id="744a4-127">La méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="744a4-127">The [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method performs the following steps:</span></span>

1.  <span data-ttu-id="744a4-128">Appelez [**IMFMediaEventGenerator :: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) pour récupérer l’événement.</span><span class="sxs-lookup"><span data-stu-id="744a4-128">Call [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event.</span></span> <span data-ttu-id="744a4-129">Cette méthode retourne un pointeur vers l’interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="744a4-129">This method returns a pointer to the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span>
2.  <span data-ttu-id="744a4-130">Appelez [**IMFMediaEvent :: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) pour recevoir le code de l’événement.</span><span class="sxs-lookup"><span data-stu-id="744a4-130">Call [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event code.</span></span>
3.  <span data-ttu-id="744a4-131">Si le code d’événement est [MESessionClosed](mesessionclosed.md), appelez SetEvent pour définir l’événement *m \_ hCloseEvent* .</span><span class="sxs-lookup"><span data-stu-id="744a4-131">If the event code is [MESessionClosed](mesessionclosed.md), call SetEvent to set the *m\_hCloseEvent* event.</span></span> <span data-ttu-id="744a4-132">La raison de cette étape est expliquée à l' [étape 7 : arrêter la session multimédia](step-7--shut-down-the-media-session.md)et également dans les commentaires de code.</span><span class="sxs-lookup"><span data-stu-id="744a4-132">The reason for this step is explained in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md), and also in the code comments.</span></span>
4.  <span data-ttu-id="744a4-133">Pour tous les autres codes d’événement, appelez [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) pour demander l’événement suivant.</span><span class="sxs-lookup"><span data-stu-id="744a4-133">For all other event codes, call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) to request the next event.</span></span>
5.  <span data-ttu-id="744a4-134">Publiez un message d' **\_ événement de \_ lecteur \_ d’application WM** dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="744a4-134">Post a **WM\_APP\_PLAYER\_EVENT** message to the window.</span></span>

<span data-ttu-id="744a4-135">Le code suivant illustre la méthode HandleEvent, qui est appelée lorsque l’application reçoit le message d' **\_ événement du \_ lecteur \_ d’application WM** :</span><span class="sxs-lookup"><span data-stu-id="744a4-135">The following code shows the HandleEvent method, which is called when the application receives the **WM\_APP\_PLAYER\_EVENT** message:</span></span>


```C++
HRESULT CPlayer::HandleEvent(UINT_PTR pEventPtr)
{
    HRESULT hrStatus = S_OK;            
    MediaEventType meType = MEUnknown;  

    IMFMediaEvent *pEvent = (IMFMediaEvent*)pEventPtr;

    if (pEvent == NULL)
    {
        return E_POINTER;
    }

    // Get the event type.
    HRESULT hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event status. If the operation that triggered the event 
    // did not succeed, the status is a failure code.
    hr = pEvent->GetStatus(&hrStatus);

    // Check if the async operation succeeded.
    if (SUCCEEDED(hr) && FAILED(hrStatus)) 
    {
        hr = hrStatus;
    }
    if (FAILED(hr))
    {
        goto done;
    }

    switch(meType)
    {
    case MESessionTopologyStatus:
        hr = OnTopologyStatus(pEvent);
        break;

    case MEEndOfPresentation:
        hr = OnPresentationEnded(pEvent);
        break;

    case MENewPresentation:
        hr = OnNewPresentation(pEvent);
        break;

    default:
        hr = OnSessionEvent(pEvent, meType);
        break;
    }

done:
    SafeRelease(&pEvent);
    return hr;
}
```



<span data-ttu-id="744a4-136">Cette méthode appelle [**IMFMediaEvent :: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) pour récupérer le type d’événement et [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) pour récupérer la réussite du code d’échec associé à l’événement.</span><span class="sxs-lookup"><span data-stu-id="744a4-136">This method calls [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event type and [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the success of failure code associated with the event.</span></span> <span data-ttu-id="744a4-137">La prochaine action effectuée dépend du code de l’événement.</span><span class="sxs-lookup"><span data-stu-id="744a4-137">The next action taken depends on the event code.</span></span>

## <a name="mesessiontopologystatus"></a><span data-ttu-id="744a4-138">MESessionTopologyStatus</span><span class="sxs-lookup"><span data-stu-id="744a4-138">MESessionTopologyStatus</span></span>

<span data-ttu-id="744a4-139">L’événement [MESessionTopologyStatus](mesessiontopologystatus.md) signale une modification de l’état de la topologie.</span><span class="sxs-lookup"><span data-stu-id="744a4-139">The [MESessionTopologyStatus](mesessiontopologystatus.md) event signals a change in the status of the topology.</span></span> <span data-ttu-id="744a4-140">L' [**attribut \_ \_ \_ État**](mf-event-topology-status-attribute.md) de la topologie de l’événement MF de l’objet d’événement contient l’État.</span><span class="sxs-lookup"><span data-stu-id="744a4-140">The [**MF\_EVENT\_TOPOLOGY\_STATUS**](mf-event-topology-status-attribute.md) attribute of the event object contains the status.</span></span> <span data-ttu-id="744a4-141">Pour cet exemple, la seule valeur intéressante est **MF \_ TOPOSTATUS \_ Ready**, qui indique que la lecture est prête pour le démarrage.</span><span class="sxs-lookup"><span data-stu-id="744a4-141">For this example, the only value of interest is **MF\_TOPOSTATUS\_READY**, which indicates that playback is ready to start.</span></span>


```C++
HRESULT CPlayer::OnTopologyStatus(IMFMediaEvent *pEvent)
{
    UINT32 status; 

    HRESULT hr = pEvent->GetUINT32(MF_EVENT_TOPOLOGY_STATUS, &status);
    if (SUCCEEDED(hr) && (status == MF_TOPOSTATUS_READY))
    {
        SafeRelease(&m_pVideoDisplay);

        // Get the IMFVideoDisplayControl interface from EVR. This call is
        // expected to fail if the media file does not have a video stream.

        (void)MFGetService(m_pSession, MR_VIDEO_RENDER_SERVICE, 
            IID_PPV_ARGS(&m_pVideoDisplay));

        hr = StartPlayback();
    }
    return hr;
}
```



<span data-ttu-id="744a4-142">La `CPlayer::StartPlayback` méthode est illustrée à l' [étape 6 : contrôler la lecture](step-6--control-playback.md).</span><span class="sxs-lookup"><span data-stu-id="744a4-142">The `CPlayer::StartPlayback` method is shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

<span data-ttu-id="744a4-143">Cet exemple appelle également [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour obtenir l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) à partir du [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="744a4-143">This example also calls [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface from the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="744a4-144">Cette interface est nécessaire pour gérer le redessin et le redimensionnement de la fenêtre vidéo, également illustrée à l' [étape 6 : contrôler la lecture](step-6--control-playback.md).</span><span class="sxs-lookup"><span data-stu-id="744a4-144">This interface is needed to handle repainting and resizing the video window, also shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

## <a name="meendofpresentation"></a><span data-ttu-id="744a4-145">MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="744a4-145">MEEndOfPresentation</span></span>

<span data-ttu-id="744a4-146">L’événement [MEEndOfPresentation](meendofpresentation.md) signale que la lecture a atteint la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="744a4-146">The [MEEndOfPresentation](meendofpresentation.md) event signals that playback has reached the end of the file.</span></span> <span data-ttu-id="744a4-147">La session multimédia bascule automatiquement vers l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="744a4-147">The Media Session automatically switches back to the stopped state.</span></span>


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a><span data-ttu-id="744a4-148">MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="744a4-148">MENewPresentation</span></span>

<span data-ttu-id="744a4-149">L’événement [MENewPresentation](menewpresentation.md) signale le début d’une nouvelle présentation.</span><span class="sxs-lookup"><span data-stu-id="744a4-149">The [MENewPresentation](menewpresentation.md) event signals the start of a new presentation.</span></span> <span data-ttu-id="744a4-150">Les données d’événement sont un pointeur [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pour la nouvelle présentation.</span><span class="sxs-lookup"><span data-stu-id="744a4-150">The event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer for the new presentation.</span></span>

<span data-ttu-id="744a4-151">Dans de nombreux cas, vous ne recevrez pas d’événement.</span><span class="sxs-lookup"><span data-stu-id="744a4-151">In many cases, you will not receive this event at all.</span></span> <span data-ttu-id="744a4-152">Dans ce cas, utilisez le pointeur [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pour créer une nouvelle topologie de lecture, comme indiqué à l' [étape 3 : ouvrir un fichier multimédia](step-3--open-a-media-file.md).</span><span class="sxs-lookup"><span data-stu-id="744a4-152">If you do, use the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer to create a new playback topology, as shown in [Step 3: Open a Media File](step-3--open-a-media-file.md).</span></span> <span data-ttu-id="744a4-153">Puis met en file d’attente la nouvelle topologie sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="744a4-153">Then queue the new topology on the Media Session.</span></span>


```C++
//  Handler for MENewPresentation event.
//
//  This event is sent if the media source has a new presentation, which 
//  requires a new topology. 

HRESULT CPlayer::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFTopology *pTopology = NULL;

    // Get the presentation descriptor from the event.
    HRESULT hr = GetEventObject(pEvent, &pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pPD,  m_hwndVideo,&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

done:
    SafeRelease(&pTopology);
    SafeRelease(&pPD);
    return S_OK;
}
```



<span data-ttu-id="744a4-154">[Étape 6 : contrôler la lecture](step-6--control-playback.md)</span><span class="sxs-lookup"><span data-stu-id="744a4-154">Next: [Step 6: Control Playback](step-6--control-playback.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="744a4-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="744a4-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="744a4-156">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="744a4-156">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="744a4-157">Comment lire des fichiers multimédias avec Media Foundation</span><span class="sxs-lookup"><span data-stu-id="744a4-157">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



