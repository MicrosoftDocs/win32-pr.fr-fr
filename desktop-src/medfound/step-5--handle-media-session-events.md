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
# <a name="step-5-handle-media-session-events"></a>Étape 5 : gérer les événements de session multimédia

Cette rubrique est l’étape 5 du didacticiel [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md). Le code complet est présenté dans la rubrique [exemple de lecture de session multimédia](media-session-playback-example.md).

Pour plus d’informations sur cette rubrique, consultez l’article sur les [générateurs d’événements multimédias](media-event-generators.md). Cette rubrique contient les sections suivantes :

-   [Obtention d’événements de session](#getting-session-events)
-   [MESessionTopologyStatus](#mesessiontopologystatus)
-   [MEEndOfPresentation](#meendofpresentation)
-   [MENewPresentation](#menewpresentation)
-   [Rubriques connexes](#related-topics)

## <a name="getting-session-events"></a>Obtention d’événements de session

Pour obtenir des événements de la session multimédia, l’objet CPlayer appelle la méthode [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) , comme indiqué à [l’étape 4 : créer la session multimédia](step-4--create-the-media-session.md). Cette méthode est asynchrone, ce qui signifie qu’elle retourne immédiatement à l’appelant. Lorsque l’événement de session suivant se produit, la session multimédia appelle la méthode [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) de l’objet CPlayer.

Il est important de se souvenir que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) est appelé à partir d’un thread de travail, et non du thread d’application. Par conséquent, l’implémentation de **Invoke** doit être de sécurité multithread. Une approche consisterait à protéger les données de membre à l’aide d’une section critique. Toutefois, la `CPlayer` classe illustre une approche alternative :

1.  Dans la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , l’objet CPlayer publie un message d’événement de **lecteur d' \_ application \_ \_ WM** dans l’application. Le paramètre de message est un pointeur [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .
2.  L’application reçoit le message d' **\_ événement du \_ lecteur \_ d’application WM** .
3.  L’application appelle la `CPlayer::HandleEvent` méthode, en passant le pointeur [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .
4.  La `HandleEvent` méthode répond à l’événement.

Le code suivant illustre la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) :


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



La méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) effectue les étapes suivantes :

1.  Appelez [**IMFMediaEventGenerator :: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) pour récupérer l’événement. Cette méthode retourne un pointeur vers l’interface [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .
2.  Appelez [**IMFMediaEvent :: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) pour recevoir le code de l’événement.
3.  Si le code d’événement est [MESessionClosed](mesessionclosed.md), appelez SetEvent pour définir l’événement *m \_ hCloseEvent* . La raison de cette étape est expliquée à l' [étape 7 : arrêter la session multimédia](step-7--shut-down-the-media-session.md)et également dans les commentaires de code.
4.  Pour tous les autres codes d’événement, appelez [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) pour demander l’événement suivant.
5.  Publiez un message d' **\_ événement de \_ lecteur \_ d’application WM** dans la fenêtre.

Le code suivant illustre la méthode HandleEvent, qui est appelée lorsque l’application reçoit le message d' **\_ événement du \_ lecteur \_ d’application WM** :


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



Cette méthode appelle [**IMFMediaEvent :: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) pour récupérer le type d’événement et [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) pour récupérer la réussite du code d’échec associé à l’événement. La prochaine action effectuée dépend du code de l’événement.

## <a name="mesessiontopologystatus"></a>MESessionTopologyStatus

L’événement [MESessionTopologyStatus](mesessiontopologystatus.md) signale une modification de l’état de la topologie. L' [**attribut \_ \_ \_ État**](mf-event-topology-status-attribute.md) de la topologie de l’événement MF de l’objet d’événement contient l’État. Pour cet exemple, la seule valeur intéressante est **MF \_ TOPOSTATUS \_ Ready**, qui indique que la lecture est prête pour le démarrage.


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



La `CPlayer::StartPlayback` méthode est illustrée à l' [étape 6 : contrôler la lecture](step-6--control-playback.md).

Cet exemple appelle également [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour obtenir l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) à partir du [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR). Cette interface est nécessaire pour gérer le redessin et le redimensionnement de la fenêtre vidéo, également illustrée à l' [étape 6 : contrôler la lecture](step-6--control-playback.md).

## <a name="meendofpresentation"></a>MEEndOfPresentation

L’événement [MEEndOfPresentation](meendofpresentation.md) signale que la lecture a atteint la fin du fichier. La session multimédia bascule automatiquement vers l’état arrêté.


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a>MENewPresentation

L’événement [MENewPresentation](menewpresentation.md) signale le début d’une nouvelle présentation. Les données d’événement sont un pointeur [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pour la nouvelle présentation.

Dans de nombreux cas, vous ne recevrez pas d’événement. Dans ce cas, utilisez le pointeur [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pour créer une nouvelle topologie de lecture, comme indiqué à l' [étape 3 : ouvrir un fichier multimédia](step-3--open-a-media-file.md). Puis met en file d’attente la nouvelle topologie sur la session multimédia.


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



[Étape 6 : contrôler la lecture](step-6--control-playback.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> <dt>

[Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



