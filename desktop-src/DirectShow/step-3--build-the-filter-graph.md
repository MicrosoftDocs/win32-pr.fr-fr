---
description: Cette rubrique est l’étape 3 de la lecture audio/vidéo du didacticiel dans DirectShow.
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: 'Étape 3 : générer le graphique de filtre'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a770ad823a2578fab88a09cc44a3c7f2be4a4ca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530689"
---
# <a name="step-3-build-the-filter-graph"></a><span data-ttu-id="eb1bb-103">Étape 3 : générer le graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="eb1bb-103">Step 3: Build the Filter Graph</span></span>

<span data-ttu-id="eb1bb-104">Cette rubrique est l’étape 3 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="eb1bb-104">This topic is step 3 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="eb1bb-105">Le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="eb1bb-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="eb1bb-106">L’étape suivante consiste à créer un graphique de filtre pour lire le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-106">The next step is to build a filter graph to play the media file.</span></span>

### <a name="opening-a-media-file"></a><span data-ttu-id="eb1bb-107">Ouverture d’un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="eb1bb-107">Opening a Media File</span></span>

<span data-ttu-id="eb1bb-108">La `DShowPlayer::OpenFile` méthode ouvre un fichier multimédia pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-108">The `DShowPlayer::OpenFile` method opens a media file for playback.</span></span> <span data-ttu-id="eb1bb-109">Cette méthode effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="eb1bb-109">This method does the following:</span></span>

1.  <span data-ttu-id="eb1bb-110">Crée un nouveau graphique de filtre (vide).</span><span class="sxs-lookup"><span data-stu-id="eb1bb-110">Creates a new (empty) filter graph.</span></span>
2.  <span data-ttu-id="eb1bb-111">Appelle [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) pour ajouter un filtre source pour le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-111">Calls [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the specified file.</span></span>
3.  <span data-ttu-id="eb1bb-112">Génère le rendu des flux sur le filtre source.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-112">Renders the streams on the source filter.</span></span>


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



### <a name="creating-the-filter-graph-manager"></a><span data-ttu-id="eb1bb-113">Création du gestionnaire de graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="eb1bb-113">Creating the Filter Graph Manager</span></span>

<span data-ttu-id="eb1bb-114">La `DShowPlayer::InitializeGraph` méthode crée un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-114">The `DShowPlayer::InitializeGraph` method creates a new filter graph.</span></span> <span data-ttu-id="eb1bb-115">Cette méthode effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="eb1bb-115">This method does the following:</span></span>

1.  <span data-ttu-id="eb1bb-116">Appelle [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une nouvelle instance du [Gestionnaire de graphes de filtre](filter-graph-manager.md).</span><span class="sxs-lookup"><span data-stu-id="eb1bb-116">Calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="eb1bb-117">Interroge le gestionnaire de graphique de filtre pour les interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) et [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .</span><span class="sxs-lookup"><span data-stu-id="eb1bb-117">Queries the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>
3.  <span data-ttu-id="eb1bb-118">Appelle [**IMediaEventEx :: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) pour configurer la notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-118">Calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) to set up event notification.</span></span> <span data-ttu-id="eb1bb-119">Pour plus d’informations, consultez [notification d’événements dans DirectShow](event-notification-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="eb1bb-119">For more information, see [Event Notification in DirectShow](event-notification-in-directshow.md).</span></span>


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



### <a name="rendering-the-streams"></a><span data-ttu-id="eb1bb-120">Rendu des flux</span><span class="sxs-lookup"><span data-stu-id="eb1bb-120">Rendering the Streams</span></span>

<span data-ttu-id="eb1bb-121">L’étape suivante consiste à connecter le filtre source à un ou plusieurs filtres de convertisseur.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-121">The next step is to connect the source filter to one or more renderer filters.</span></span>

<span data-ttu-id="eb1bb-122">La `DShowPlayer::RenderStreams` méthode effectue les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-122">The `DShowPlayer::RenderStreams` method performs the following steps.</span></span>

1.  <span data-ttu-id="eb1bb-123">Interroge le gestionnaire de graphique de filtre pour l’interface [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) .</span><span class="sxs-lookup"><span data-stu-id="eb1bb-123">Queries the Filter Graph Manager for the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface.</span></span>
2.  <span data-ttu-id="eb1bb-124">Ajoute un filtre de convertisseur vidéo au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-124">Adds a video renderer filter to the filter graph.</span></span>
3.  <span data-ttu-id="eb1bb-125">Ajoute le [filtre de convertisseur DirectSound](directsound-renderer-filter.md) au graphique de filtre pour prendre en charge la lecture audio.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-125">Adds the [DirectSound Renderer Filter](directsound-renderer-filter.md) to the filter graph, to support audio playback.</span></span> <span data-ttu-id="eb1bb-126">Pour plus d’informations sur l’ajout de filtres au graphique de filtre, consultez [Ajouter un filtre par CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="eb1bb-126">For more information about adding filters to the filter graph, see [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>
4.  <span data-ttu-id="eb1bb-127">Énumère les broches de sortie sur le filtre source.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-127">Enumerates the output pins on the source filter.</span></span> <span data-ttu-id="eb1bb-128">Pour plus d’informations sur l’énumération des codes confidentiels, consultez [énumération des codes confidentiels](enumerating-pins.md).</span><span class="sxs-lookup"><span data-stu-id="eb1bb-128">For more information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).</span></span>
5.  <span data-ttu-id="eb1bb-129">Pour chaque code confidentiel, appelle la méthode [**IFilterGraph2 :: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) .</span><span class="sxs-lookup"><span data-stu-id="eb1bb-129">For each pin, calls the [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) method.</span></span> <span data-ttu-id="eb1bb-130">Cette méthode connecte la broche de sortie à un filtre de convertisseur, en ajoutant des filtres intermédiaires si nécessaire (par exemple, des décodeurs).</span><span class="sxs-lookup"><span data-stu-id="eb1bb-130">This method connects the output pin to a renderer filter, adding intermediate filters if needed (such as decoders).</span></span>
6.  <span data-ttu-id="eb1bb-131">Appelle `CVideoRenderer::FinalizeGraph` pour terminer l’initialisation du convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-131">Calls `CVideoRenderer::FinalizeGraph` to finish initializing the video renderer.</span></span>
7.  <span data-ttu-id="eb1bb-132">Supprime le filtre de [convertisseur DirectSound](directsound-renderer-filter.md) si ce filtre n’est pas connecté à un autre filtre.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-132">Removes the [DirectSound Renderer](directsound-renderer-filter.md) filter if that filter is not connected to another filter.</span></span> <span data-ttu-id="eb1bb-133">Cela peut se produire si le fichier source ne contient pas de flux audio.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-133">This can occur if the source file does not contain an audio stream.</span></span>


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



<span data-ttu-id="eb1bb-134">Voici le code de la `RemoveUnconnectedRenderer` fonction, qui est utilisé dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-134">Here is the code for the `RemoveUnconnectedRenderer` function, which is used in the previous example.</span></span>


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



### <a name="releasing-the-filter-graph"></a><span data-ttu-id="eb1bb-135">Libération du graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="eb1bb-135">Releasing the Filter Graph</span></span>

<span data-ttu-id="eb1bb-136">Lorsque l’application se ferme, elle doit libérer le graphique de filtre, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="eb1bb-136">When the application exits, it must release the filter graph, as shown in the following code.</span></span>


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



<span data-ttu-id="eb1bb-137">[Étape 4 : ajouter le convertisseur vidéo](step-4--add-the-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="eb1bb-137">Next: [Step 4: Add the Video Renderer](step-4--add-the-video-renderer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb1bb-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb1bb-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb1bb-139">Lecture audio/vidéo dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="eb1bb-139">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="eb1bb-140">Exemple de lecture DirectShow</span><span class="sxs-lookup"><span data-stu-id="eb1bb-140">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="eb1bb-141">Génération du graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="eb1bb-141">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="eb1bb-142">Techniques d' Graph-Building générales</span><span class="sxs-lookup"><span data-stu-id="eb1bb-142">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 
