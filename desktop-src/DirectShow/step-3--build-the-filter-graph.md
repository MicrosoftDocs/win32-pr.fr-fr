---
description: Cette rubrique est l’étape 3 de la lecture audio/vidéo du didacticiel dans DirectShow.
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: 'Étape 3 : générer le filtre Graph'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad4903e08b19e15721c8b62f130261bb4d05fcd94d544380b2e501f56d60704d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072503"
---
# <a name="step-3-build-the-filter-graph"></a>Étape 3 : générer le filtre Graph

Cette rubrique est l’étape 3 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md). le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).

L’étape suivante consiste à créer un graphique de filtre pour lire le fichier multimédia.

### <a name="opening-a-media-file"></a>Ouverture d’un fichier multimédia

La `DShowPlayer::OpenFile` méthode ouvre un fichier multimédia pour la lecture. Cette méthode effectue les opérations suivantes :

1.  Crée un nouveau graphique de filtre (vide).
2.  Appelle [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) pour ajouter un filtre source pour le fichier spécifié.
3.  Génère le rendu des flux sur le filtre source.


```C++
HRESULT DShowPlayer::OpenFile(PCWSTR pszFileName)
{
    IBaseFilter *pSource = NULL;

    // Create a new filter graph. (This also closes the old one, if any.)
    HRESULT hr = InitializeGraph();
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the source filter to the graph.
    hr = m_pGraph->AddSourceFilter(pszFileName, NULL, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Try to render the streams.
    hr = RenderStreams(pSource);

done:
    if (FAILED(hr))
    {
        TearDownGraph();
    }
    SafeRelease(&pSource);
    return hr;
}
```



### <a name="creating-the-filter-graph-manager"></a>création du gestionnaire de Graph de filtres

La `DShowPlayer::InitializeGraph` méthode crée un graphique de filtre. Cette méthode effectue les opérations suivantes :

1.  appelle [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une nouvelle instance du [filtre Graph Manager](filter-graph-manager.md).
2.  interroge le gestionnaire de Graph de filtre pour les interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) et [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .
3.  Appelle [**IMediaEventEx :: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) pour configurer la notification d’événement. Pour plus d’informations, consultez [notification d’événements dans DirectShow](event-notification-in-directshow.md).


```C++
HRESULT DShowPlayer::InitializeGraph()
{
    TearDownGraph();

    // Create the Filter Graph Manager.
    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = STATE_STOPPED;

done:
    return hr;
}
```



### <a name="rendering-the-streams"></a>Rendu de l’Flux

L’étape suivante consiste à connecter le filtre source à un ou plusieurs filtres de convertisseur.

La `DShowPlayer::RenderStreams` méthode effectue les étapes suivantes.

1.  interroge le gestionnaire de Graph de filtre de l’interface [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) .
2.  Ajoute un filtre de convertisseur vidéo au graphique de filtre.
3.  Ajoute le [filtre de convertisseur DirectSound](directsound-renderer-filter.md) au graphique de filtre pour prendre en charge la lecture audio. Pour plus d’informations sur l’ajout de filtres au graphique de filtre, consultez [Ajouter un filtre par CLSID](add-a-filter-by-clsid.md).
4.  Énumère les broches de sortie sur le filtre source. Pour plus d’informations sur l’énumération des codes confidentiels, consultez [énumération des codes confidentiels](enumerating-pins.md).
5.  Pour chaque code confidentiel, appelle la méthode [**IFilterGraph2 :: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) . Cette méthode connecte la broche de sortie à un filtre de convertisseur, en ajoutant des filtres intermédiaires si nécessaire (par exemple, des décodeurs).
6.  Appelle `CVideoRenderer::FinalizeGraph` pour terminer l’initialisation du convertisseur vidéo.
7.  Supprime le filtre de [convertisseur DirectSound](directsound-renderer-filter.md) si ce filtre n’est pas connecté à un autre filtre. Cela peut se produire si le fichier source ne contient pas de flux audio.


```C++
// Render the streams from a source filter. 

HRESULT DShowPlayer::RenderStreams(IBaseFilter *pSource)
{
    BOOL bRenderedAnyPin = FALSE;

    IFilterGraph2 *pGraph2 = NULL;
    IEnumPins *pEnum = NULL;
    IBaseFilter *pAudioRenderer = NULL;
    HRESULT hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&pGraph2));
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the video renderer to the graph
    hr = CreateVideoRenderer();
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the DSound Renderer to the graph.
    hr = AddFilterByCLSID(m_pGraph, CLSID_DSoundRender, 
        &pAudioRenderer, L"Audio Renderer");
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate the pins on the source filter.
    hr = pSource->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    // Loop through all the pins
    IPin *pPin;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {           
        // Try to render this pin. 
        // It's OK if we fail some pins, if at least one pin renders.
        HRESULT hr2 = pGraph2->RenderEx(pPin, AM_RENDEREX_RENDERTOEXISTINGRENDERERS, NULL);

        pPin->Release();
        if (SUCCEEDED(hr2))
        {
            bRenderedAnyPin = TRUE;
        }
    }

    hr = m_pVideo->FinalizeGraph(m_pGraph);
    if (FAILED(hr))
    {
        goto done;
    }

    // Remove the audio renderer, if not used.
    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(m_pGraph, pAudioRenderer, &bRemoved);

done:
    SafeRelease(&pEnum);
    SafeRelease(&pAudioRenderer);
    SafeRelease(&pGraph2);

    // If we succeeded to this point, make sure we rendered at least one 
    // stream.
    if (SUCCEEDED(hr))
    {
        if (!bRenderedAnyPin)
        {
            hr = VFW_E_CANNOT_RENDER;
        }
    }
    return hr;
}
```



Voici le code de la `RemoveUnconnectedRenderer` fonction, qui est utilisé dans l’exemple précédent.


```C++
HRESULT RemoveUnconnectedRenderer(IGraphBuilder *pGraph, IBaseFilter *pRenderer, BOOL *pbRemoved)
{
    IPin *pPin = NULL;

    *pbRemoved = FALSE;

    // Look for a connected input pin on the renderer.

    HRESULT hr = FindConnectedPin(pRenderer, PINDIR_INPUT, &pPin);
    SafeRelease(&pPin);

    // If this function succeeds, the renderer is connected, so we don't remove it.
    // If it fails, it means the renderer is not connected to anything, so
    // we remove it.

    if (FAILED(hr))
    {
        hr = pGraph->RemoveFilter(pRenderer);
        *pbRemoved = TRUE;
    }

    return hr;
}
```



### <a name="releasing-the-filter-graph"></a>Libération du filtre Graph

Lorsque l’application se ferme, elle doit libérer le graphique de filtre, comme illustré dans le code suivant.


```C++
void DShowPlayer::TearDownGraph()
{
    // Stop sending event messages
    if (m_pEvent)
    {
        m_pEvent->SetNotifyWindow((OAHWND)NULL, NULL, NULL);
    }

    SafeRelease(&m_pGraph);
    SafeRelease(&m_pControl);
    SafeRelease(&m_pEvent);

    delete m_pVideo;
    m_pVideo = NULL;

    m_state = STATE_NO_GRAPH;
}
```



[Étape 4 : ajouter le convertisseur vidéo](step-4--add-the-video-renderer.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo en DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow Exemple de lecture](directshow-playback-example.md)
</dt> <dt>

[Génération du filtre Graph](building-the-filter-graph.md)
</dt> <dt>

[Techniques d' Graph-Building générales](general-graph-building-techniques.md)
</dt> </dl>

 

 
