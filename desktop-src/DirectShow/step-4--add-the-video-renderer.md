---
description: Cette rubrique est l’étape 4 de la lecture audio/vidéo du didacticiel dans DirectShow.
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 'Étape 4 : ajouter le convertisseur vidéo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17a0622909525f69cf64fd374c8512a8fa9bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522479"
---
# <a name="step-4-add-the-video-renderer"></a><span data-ttu-id="45730-103">Étape 4 : ajouter le convertisseur vidéo</span><span class="sxs-lookup"><span data-stu-id="45730-103">Step 4: Add the Video Renderer</span></span>

<span data-ttu-id="45730-104">Cette rubrique est l’étape 4 de la [lecture audio/vidéo du didacticiel dans DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="45730-104">This topic is step 4 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="45730-105">Le code complet est présenté dans la rubrique [exemple de lecture DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="45730-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="45730-106">DirectShow fournit plusieurs filtres différents qui restituent la vidéo :</span><span class="sxs-lookup"><span data-stu-id="45730-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="45730-107">[**Filtre de convertisseur vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="45730-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="45730-108">[Filtre de convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="45730-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="45730-109">[Filtre de convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="45730-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="45730-110">Pour plus d’informations sur les différences entre ces filtres, consultez [choix du convertisseur vidéo approprié](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="45730-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="45730-111">Dans ce didacticiel, chaque filtre de convertisseur vidéo est encapsulé par une classe qui soustrait certaines des différences entre eux.</span><span class="sxs-lookup"><span data-stu-id="45730-111">In this tutorial, each video renderer filter is wrapped by a class that abstracts some of the differences between them.</span></span> <span data-ttu-id="45730-112">Ces classes dérivent toutes d’une classe de base abstraite nommée `CVideoRenderer` .</span><span class="sxs-lookup"><span data-stu-id="45730-112">These classes all derive from an abstract base class named `CVideoRenderer`.</span></span> <span data-ttu-id="45730-113">La déclaration de `CVideoRenderer` est indiquée à l' [étape 2 : déclarer CVideoRenderer et les classes dérivées](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="45730-113">The declaration of `CVideoRenderer` is shown in [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

<span data-ttu-id="45730-114">La méthode suivante tente de créer chaque convertisseur vidéo à son tour, en commençant par EVR, puis VMR-9 et enfin VMR-7.</span><span class="sxs-lookup"><span data-stu-id="45730-114">The following method tries to create each video renderer in turn, starting with the EVR, then the VMR-9, and finally the VMR-7.</span></span>


```C++
HRESULT DShowPlayer::CreateVideoRenderer()
{
    HRESULT hr = E_FAIL;

    enum { Try_EVR, Try_VMR9, Try_VMR7 };

    for (DWORD i = Try_EVR; i <= Try_VMR7; i++)
    {
        switch (i)
        {
        case Try_EVR:
            m_pVideo = new (std::nothrow) CEVR();
            break;

        case Try_VMR9:
            m_pVideo = new (std::nothrow) CVMR9();
            break;

        case Try_VMR7:
            m_pVideo = new (std::nothrow) CVMR7();
            break;
        }

        if (m_pVideo == NULL)
        {
            hr = E_OUTOFMEMORY;
            break;
        }

        hr = m_pVideo->AddToGraph(m_pGraph, m_hwnd);
        if (SUCCEEDED(hr))
        {
            break;
        }

        delete m_pVideo;
        m_pVideo = NULL;
    }
    return hr;
}

```



### <a name="evr-filter"></a><span data-ttu-id="45730-115">Filtre EVR</span><span class="sxs-lookup"><span data-stu-id="45730-115">EVR Filter</span></span>

<span data-ttu-id="45730-116">Le code suivant crée le filtre EVR et l’ajoute au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="45730-116">The following code creates the EVR filter and adds it to the filter graph.</span></span> <span data-ttu-id="45730-117">La fonction `AddFilterByCLSID` utilisée dans cet exemple est présentée dans la rubrique [Ajouter un filtre par CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="45730-117">The function `AddFilterByCLSID` used in this example is shown in the topic [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>


```C++
HRESULT CEVR::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pEVR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_EnhancedVideoRenderer, 
        &pEVR, L"EVR");

    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitializeEVR(pEVR, hwnd, &m_pVideoDisplay);
    if (FAILED(hr))
    {
        goto done;
    }

    // Note: Because IMFVideoDisplayControl is a service interface,
    // you cannot QI the pointer to get back the IBaseFilter pointer.
    // Therefore, we need to cache the IBaseFilter pointer.

    m_pEVR = pEVR;
    m_pEVR->AddRef();

done:
    SafeRelease(&pEVR);
    return hr;
}
```



<span data-ttu-id="45730-118">La `InitializeEVR` fonction initialise le filtre EVR.</span><span class="sxs-lookup"><span data-stu-id="45730-118">The `InitializeEVR` function initializes the EVR filter.</span></span> <span data-ttu-id="45730-119">Cette fonction effectue les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="45730-119">This function performs the following steps.</span></span>

1.  <span data-ttu-id="45730-120">Interroge le filtre de l’interface [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="45730-120">Queries the filter for the [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="45730-121">Appelle [**IMFGetService :: GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) pour obtenir un pointeur vers l’interface [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="45730-121">Calls [**IMFGetService::GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span>
3.  <span data-ttu-id="45730-122">Appelle [**IMFVideoDisplayControl :: SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) pour définir la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="45730-122">Calls [**IMFVideoDisplayControl::SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) to set the video window.</span></span>
4.  <span data-ttu-id="45730-123">Appelle [**IMFVideoDisplayControl :: SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) pour configurer le EVR afin de conserver les proportions vidéo.</span><span class="sxs-lookup"><span data-stu-id="45730-123">Calls [**IMFVideoDisplayControl::SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) to configure the EVR to preserve the video aspect ratio.</span></span>

<span data-ttu-id="45730-124">Le code suivant illustre la `InitializeEVR` fonction.</span><span class="sxs-lookup"><span data-stu-id="45730-124">The following code shows the `InitializeEVR` function.</span></span>


```C++
HRESULT InitializeEVR( 
    IBaseFilter *pEVR,              // Pointer to the EVR
    HWND hwnd,                      // Clipping window
    IMFVideoDisplayControl** ppDisplayControl
    ) 
{ 
    IMFGetService *pGS = NULL;
    IMFVideoDisplayControl *pDisplay = NULL;

    HRESULT hr = pEVR->QueryInterface(IID_PPV_ARGS(&pGS)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGS->GetService(MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&pDisplay));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pDisplay->SetVideoWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pDisplay->SetAspectRatioMode(MFVideoARMode_PreservePicture);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IMFVideoDisplayControl pointer to the caller.
    *ppDisplayControl = pDisplay;
    (*ppDisplayControl)->AddRef();

done:
    SafeRelease(&pGS);
    SafeRelease(&pDisplay);
    return hr; 
} 
```



<span data-ttu-id="45730-125">Une fois le graphique construit, les `DShowPlayer::RenderStreams` appels `CVideoRenderer::FinalizeGraph` .</span><span class="sxs-lookup"><span data-stu-id="45730-125">After the graph is built, the `DShowPlayer::RenderStreams` calls `CVideoRenderer::FinalizeGraph`.</span></span> <span data-ttu-id="45730-126">Cette méthode effectue toute initialisation ou nettoyage final.</span><span class="sxs-lookup"><span data-stu-id="45730-126">This method performs any final initialization or cleanup.</span></span> <span data-ttu-id="45730-127">Le code suivant illustre l' `CEVR` implémentation de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="45730-127">The following code shows the `CEVR` implementation of this method.</span></span>


```C++
HRESULT CEVR::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pEVR == NULL)
    {
        return S_OK;
    }

    BOOL bRemoved;
    HRESULT hr = RemoveUnconnectedRenderer(pGraph, m_pEVR, &bRemoved);
    if (bRemoved)
    {
        SafeRelease(&m_pEVR);
        SafeRelease(&m_pVideoDisplay);
    }
    return hr;
}
```



<span data-ttu-id="45730-128">Si le EVR n’est connecté à aucun autre filtre, cette méthode supprime le EVR du graphique.</span><span class="sxs-lookup"><span data-stu-id="45730-128">If the EVR is not connected to any other filter, this method removes the EVR from the graph.</span></span> <span data-ttu-id="45730-129">Cela peut se produire si le fichier multimédia ne contient pas de flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="45730-129">This can occur if the media file does not contain a video stream.</span></span>

### <a name="vmr-9-filter"></a><span data-ttu-id="45730-130">Filtre VMR-9</span><span class="sxs-lookup"><span data-stu-id="45730-130">VMR-9 Filter</span></span>

<span data-ttu-id="45730-131">Le code suivant crée le filtre VMR-9 et l’ajoute au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="45730-131">The following code creates the VMR-9 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR9::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer9, 
        &pVMR, L"VMR-9");
    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR 
        // is connected.
        hr = InitWindowlessVMR9(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="45730-132">La `InitWindowlessVMR9` fonction initialise VMR-9 en mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="45730-132">The `InitWindowlessVMR9` function initializes the VMR-9 for windowless mode.</span></span> <span data-ttu-id="45730-133">(Pour plus d’informations sur le mode sans fenêtre, consultez [mode sans fenêtre VMR](vmr-windowless-mode.md).) Cette fonction effectue les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="45730-133">(For more information about windowless mode, see [VMR Windowless Mode](vmr-windowless-mode.md).) This function performs the following steps.</span></span>

1.  <span data-ttu-id="45730-134">Interroge le filtre VMR-9 pour l’interface [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .</span><span class="sxs-lookup"><span data-stu-id="45730-134">Queries the VMR-9 filter for the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) interface.</span></span>
2.  <span data-ttu-id="45730-135">Appelle la méthode [**IVMRFilterConfig9 :: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) pour définir le mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="45730-135">Calls the [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="45730-136">Interroge le filtre VMR-9 pour l’interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="45730-136">Queries the VMR-9 filter for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
4.  <span data-ttu-id="45730-137">Appelle la méthode [**IVMRWindowlessControl9 :: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) pour définir la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="45730-137">Calls the [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="45730-138">Appelle la méthode [**IVMRWindowlessControl9 :: SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) pour conserver les proportions vidéo.</span><span class="sxs-lookup"><span data-stu-id="45730-138">Calls the [**IVMRWindowlessControl9::SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="45730-139">Le code suivant illustre la `InitWindowlessVMR9` fonction.</span><span class="sxs-lookup"><span data-stu-id="45730-139">The following code shows the `InitWindowlessVMR9` function.</span></span>


```C++
HRESULT InitWindowlessVMR9( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl9** ppWC   // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig9 * pConfig = NULL; 
    IVMRWindowlessControl9 *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMR9Mode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR9ARMode_LetterBox);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="45730-140">La `CVMR9::FinalizeGraph` méthode vérifie si le filtre VMR-9 est connecté et, dans le cas contraire, le supprime du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="45730-140">The `CVMR9::FinalizeGraph` method checks if the VMR-9 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR9::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



### <a name="vmr-7-filter"></a><span data-ttu-id="45730-141">Filtre VMR-7</span><span class="sxs-lookup"><span data-stu-id="45730-141">VMR-7 Filter</span></span>

<span data-ttu-id="45730-142">Les étapes pour le filtre VMR-7 sont quasiment identiques à celles de VMR-9, sauf que les interfaces VMR-7 sont utilisées à la place.</span><span class="sxs-lookup"><span data-stu-id="45730-142">The steps for the VMR-7 filter are nearly identical to those for the VMR-9, except the VMR-7 interfaces are used instead.</span></span> <span data-ttu-id="45730-143">Le code suivant crée le filtre VMR-7 et l’ajoute au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="45730-143">The following code creates the VMR-7 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR7::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer, 
        &pVMR, L"VMR-7");

    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR
        // is connected.
        hr = InitWindowlessVMR(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="45730-144">La `InitWindowlessVMR` fonction initialise VMR-7 en mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="45730-144">The `InitWindowlessVMR` function initializes the VMR-7 for windowless mode.</span></span> <span data-ttu-id="45730-145">Cette fonction effectue les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="45730-145">This function performs the following steps.</span></span>

1.  <span data-ttu-id="45730-146">Interroge le filtre VMR-7 pour l’interface [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) .</span><span class="sxs-lookup"><span data-stu-id="45730-146">Queries the VMR-7 filter for the [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) interface.</span></span>
2.  <span data-ttu-id="45730-147">Appelle la méthode [**IVMRFilterConfig :: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) pour définir le mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="45730-147">Calls the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="45730-148">Interroge le filtre VMR-7 pour l’interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="45730-148">Queries the VMR-7 filter for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
4.  <span data-ttu-id="45730-149">Appelle la méthode [**IVMRWindowlessControl :: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) pour définir la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="45730-149">Calls the [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="45730-150">Appelle la méthode [**IVMRWindowlessControl :: SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) pour conserver les proportions vidéo.</span><span class="sxs-lookup"><span data-stu-id="45730-150">Calls the [**IVMRWindowlessControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="45730-151">Le code suivant illustre la `InitWindowlessVMR` fonction.</span><span class="sxs-lookup"><span data-stu-id="45730-151">The following code shows the `InitWindowlessVMR` function.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl** ppWC    // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig* pConfig = NULL; 
    IVMRWindowlessControl *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR_ARMODE_LETTER_BOX);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="45730-152">La `CVMR7::FinalizeGraph` méthode vérifie si le filtre VMR-7 est connecté et, dans le cas contraire, le supprime du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="45730-152">The `CVMR7::FinalizeGraph` method checks if the VMR-7 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR7::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="45730-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45730-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45730-154">Exemple de lecture DirectShow</span><span class="sxs-lookup"><span data-stu-id="45730-154">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="45730-155">Utilisation du filtre DirectShow EVR</span><span class="sxs-lookup"><span data-stu-id="45730-155">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="45730-156">Utilisation du convertisseur de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="45730-156">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
