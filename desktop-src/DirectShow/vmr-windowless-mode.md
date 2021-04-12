---
description: Mode sans fenêtre VMR
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: Mode sans fenêtre VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b137fbc1351f2bbe5ed38673b681e45558675d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318725"
---
# <a name="vmr-windowless-mode"></a><span data-ttu-id="66532-103">Mode sans fenêtre VMR</span><span class="sxs-lookup"><span data-stu-id="66532-103">VMR Windowless Mode</span></span>

<span data-ttu-id="66532-104">Le mode sans fenêtre est la méthode recommandée pour que les applications affichent des vidéos dans une fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="66532-104">Windowless mode is the preferred way for applications to render video inside an application window.</span></span> <span data-ttu-id="66532-105">En mode sans fenêtre, le convertisseur de mixage vidéo ne charge pas son composant de gestionnaire de fenêtres et ne prend donc pas en charge les interfaces [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) ou [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="66532-105">In windowless mode, the Video Mixing Renderer does not load its Window Manager component, and therefore does not support the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) or [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interfaces.</span></span> <span data-ttu-id="66532-106">Au lieu de cela, l’application fournit la fenêtre de lecture et définit un rectangle de destination dans la zone cliente pour que VMR dessine la vidéo.</span><span class="sxs-lookup"><span data-stu-id="66532-106">Instead, the application provides the playback window and sets a destination rectangle in the client area for the VMR to draw the video.</span></span> <span data-ttu-id="66532-107">VMR utilise un objet DirectDraw Clipper pour s’assurer que la vidéo est tronquée à la fenêtre de l’application et qu’elle n’apparaît pas sur les autres fenêtres.</span><span class="sxs-lookup"><span data-stu-id="66532-107">The VMR uses a DirectDraw clipper object to ensure that the video is clipped to the application's window and does not appear on any other windows.</span></span> <span data-ttu-id="66532-108">VMR ne sous-classe pas la fenêtre de l’application ou n’installe pas de raccordements système/processus.</span><span class="sxs-lookup"><span data-stu-id="66532-108">The VMR does not subclass the application's window or install any system/process hooks.</span></span>

<span data-ttu-id="66532-109">En mode sans fenêtre, la séquence d’événements pendant la connexion et la transition à l’état d’exécution sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="66532-109">In windowless mode, the sequence of events during connection and transition to the run state is as follows:</span></span>

-   <span data-ttu-id="66532-110">Le filtre amont propose un type de média, que VMR accepte ou rejette.</span><span class="sxs-lookup"><span data-stu-id="66532-110">The upstream filter proposes a media type, which the VMR either accepts or rejects.</span></span>
-   <span data-ttu-id="66532-111">Si le type de média est accepté, VMR appelle l’Allocator-Presenter pour obtenir une surface DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="66532-111">If the media type is accepted, the VMR calls the allocator-presenter to obtain a DirectDraw surface.</span></span> <span data-ttu-id="66532-112">Si la surface est créée avec succès, les codes confidentiels se connectent et le VMR est prêt à passer à l’état d’exécution.</span><span class="sxs-lookup"><span data-stu-id="66532-112">If the surface is created successfully, the pins connect and the VMR is ready to transition into the run state.</span></span>
-   <span data-ttu-id="66532-113">Lorsque le graphique de filtre s’exécute, le décodeur appelle **GetBuffer** pour obtenir un échantillon de support à partir de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="66532-113">When the filter graph runs, the decoder calls **GetBuffer** to get a media sample from the allocator.</span></span> <span data-ttu-id="66532-114">VMR interroge l’Allocator-Presenter pour s’assurer que la profondeur de pixel, la taille du rectangle et d’autres paramètres sur sa surface DirectDraw sont compatibles avec la vidéo entrante.</span><span class="sxs-lookup"><span data-stu-id="66532-114">The VMR queries the allocator-presenter to ensure that the pixel depth, rectangle size, and other parameters on its DirectDraw surface are compatible with the incoming video.</span></span> <span data-ttu-id="66532-115">S’ils sont compatibles, VMR retourne la surface DirectDraw au décodeur.</span><span class="sxs-lookup"><span data-stu-id="66532-115">If they are compatible, the VMR returns the DirectDraw surface to the decoder.</span></span> <span data-ttu-id="66532-116">Une fois que le décodeur a décodé dans la surface, l’unité de synchronisation principale de VMR valide les horodatages.</span><span class="sxs-lookup"><span data-stu-id="66532-116">After the decoder has decoded into the surface, the VMR's Core Synchronization Unit validates the time stamps.</span></span> <span data-ttu-id="66532-117">Cette unité bloque l’appel de **réception** jusqu’à ce que l’heure de la présentation arrive.</span><span class="sxs-lookup"><span data-stu-id="66532-117">This unit blocks the **Receive** call until the presentation time arrives.</span></span> <span data-ttu-id="66532-118">À ce stade, VMR appelle **PresentImage** sur l’Allocator-Presenter, qui présente la surface à la carte graphique.</span><span class="sxs-lookup"><span data-stu-id="66532-118">At that point, the VMR calls **PresentImage** on the allocator-presenter, which presents the surface to the graphics card.</span></span>

<span data-ttu-id="66532-119">L’illustration suivante montre le VMR en mode sans fenêtre avec plusieurs flux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="66532-119">The following illustration shows the VMR in windowless mode with multiple input streams.</span></span>

![VMR en mode sans fenêtre](images/vmr-windowless-mult-streams.png)

<span data-ttu-id="66532-121">**Configuration de VMR-7 en mode sans fenêtre**</span><span class="sxs-lookup"><span data-stu-id="66532-121">**Configuring the VMR-7 for Windowless Mode**</span></span>

<span data-ttu-id="66532-122">Pour configurer VMR-7 en mode sans fenêtre, effectuez toutes les étapes suivantes avant de connecter les broches d’entrée de VMR :</span><span class="sxs-lookup"><span data-stu-id="66532-122">To configure the VMR-7 for windowless mode, perform all of the following steps before connecting any of the VMR's input pins:</span></span>

1.  <span data-ttu-id="66532-123">Créez le filtre et ajoutez-le au graphique.</span><span class="sxs-lookup"><span data-stu-id="66532-123">Create the filter and add it to the graph.</span></span>
2.  <span data-ttu-id="66532-124">Appelez la méthode [**IVMRFilterConfig :: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) avec l' \_ indicateur sans fenêtre VMRMode.</span><span class="sxs-lookup"><span data-stu-id="66532-124">Call the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method with the VMRMode\_Windowless flag.</span></span>
3.  <span data-ttu-id="66532-125">Éventuellement, configurez le VMR pour plusieurs flux d’entrée en appelant [**IVMRFilterConfig :: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="66532-125">Optionally, configure the VMR for multiple input streams by calling [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="66532-126">VMR crée une broche d’entrée pour chaque flux.</span><span class="sxs-lookup"><span data-stu-id="66532-126">The VMR creates an input pin for each stream.</span></span> <span data-ttu-id="66532-127">Utilisez l’interface [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) pour définir l’ordre de plan et d’autres paramètres pour le flux.</span><span class="sxs-lookup"><span data-stu-id="66532-127">Use the [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) interface to set the Z-order and other parameters for the stream.</span></span> <span data-ttu-id="66532-128">Pour plus d’informations, consultez [VMR avec plusieurs flux (mode de mixage)](vmr-with-multiple-streams--mixing-mode.md).</span><span class="sxs-lookup"><span data-stu-id="66532-128">For more information, see [VMR with Multiple Streams (Mixing Mode)](vmr-with-multiple-streams--mixing-mode.md).</span></span>

    <span data-ttu-id="66532-129">Si vous n’appelez pas **SetNumberOfStreams**, VMR-7 est défini par défaut sur une seule broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="66532-129">If you do not call **SetNumberOfStreams**, the VMR-7 defaults to one input pin.</span></span> <span data-ttu-id="66532-130">Une fois les broches d’entrée connectées, le nombre de broches ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="66532-130">After the input pins are connected, the number of pins cannot be changed.</span></span>

4.  <span data-ttu-id="66532-131">Appelez [**IVMRWindowlessControl :: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) pour spécifier la fenêtre dans laquelle la vidéo rendue s’affichera.</span><span class="sxs-lookup"><span data-stu-id="66532-131">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) to specify the window in which the rendered video will appear.</span></span>

<span data-ttu-id="66532-132">Une fois ces étapes terminées, vous pouvez connecter les broches d’entrée du filtre VMR.</span><span class="sxs-lookup"><span data-stu-id="66532-132">Once these steps are completed, you can connect the VMR filter's input pins.</span></span> <span data-ttu-id="66532-133">Il existe plusieurs façons de générer le graphique, par exemple en connectant des broches directement, à l’aide de méthodes Connect intelligentes telles que [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), ou à l’aide de la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) du générateur de graphique de capture.</span><span class="sxs-lookup"><span data-stu-id="66532-133">There are various ways to build the graph, such as connecting pins directly, using Intelligent Connect methods such as [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), or using the Capture Graph Builder's [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="66532-134">Pour plus d’informations, consultez [General Graph-Building techniques](general-graph-building-techniques.md).</span><span class="sxs-lookup"><span data-stu-id="66532-134">For more information, see [General Graph-Building Techniques](general-graph-building-techniques.md).</span></span>

<span data-ttu-id="66532-135">Pour définir la position de la vidéo dans la fenêtre de l’application, appelez la méthode [**IVMRWindowlessControl :: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) .</span><span class="sxs-lookup"><span data-stu-id="66532-135">To set the position of the video within the application window, call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method.</span></span> <span data-ttu-id="66532-136">La méthode [**IVMRWindowlessControl :: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) retourne la taille de la vidéo native.</span><span class="sxs-lookup"><span data-stu-id="66532-136">The [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method returns the native video size.</span></span> <span data-ttu-id="66532-137">Pendant la lecture, l’application doit notifier VMR des messages Windows suivants :</span><span class="sxs-lookup"><span data-stu-id="66532-137">During playback, the application should notify the VMR of the following Windows messages:</span></span>

-   <span data-ttu-id="66532-138">WM \_ Paint : appelez [**IVMRWindowlessControl :: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) pour redessiner l’image.</span><span class="sxs-lookup"><span data-stu-id="66532-138">WM\_PAINT: Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) to repaint the image.</span></span>
-   <span data-ttu-id="66532-139">WM \_ DISPLAYCHANGE : appelez [**IVMRWindowlessControl ::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="66532-139">WM\_DISPLAYCHANGE: Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="66532-140">VMR effectue toutes les actions nécessaires pour afficher la vidéo au niveau de la nouvelle résolution ou de la profondeur de couleurs.</span><span class="sxs-lookup"><span data-stu-id="66532-140">The VMR takes any actions that are needed to display the video at the new resolution or color depth.</span></span>
-   <span data-ttu-id="66532-141">\_Taille du WM : recalcule la position de la vidéo et appelle à nouveau [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="66532-141">WM\_SIZE: Recalculate the position of the video and call [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) again if necessary.</span></span>

> [!Note]  
> <span data-ttu-id="66532-142">Les applications MFC doivent définir un \_ Gestionnaire de messages WM ERASEBKGND vide ou la zone d’affichage vidéo ne se redessinera pas correctement.</span><span class="sxs-lookup"><span data-stu-id="66532-142">MFC applications must define an empty WM\_ERASEBKGND message handler, or the video display area will not repaint correctly.</span></span>

 

<span data-ttu-id="66532-143">**Configuration de VMR-9 en mode sans fenêtre**</span><span class="sxs-lookup"><span data-stu-id="66532-143">**Configuring the VMR-9 for Windowless Mode**</span></span>

<span data-ttu-id="66532-144">Pour configurer VMR-9 en mode sans fenêtre, suivez les étapes décrites pour VMR-7 en mode sans fenêtre, mais utilisez les interfaces [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) et [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="66532-144">To configure the VMR-9 for windowless mode, use the steps described for the VMR-7 for Windowless mode, but use the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) and [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interfaces.</span></span> <span data-ttu-id="66532-145">La seule différence significative est que VMR-9 crée par défaut quatre broches d’entrée au lieu d’une seule broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="66532-145">The only significant difference is that the VMR-9 creates four input pins by default, rather than one input pin.</span></span> <span data-ttu-id="66532-146">Par conséquent, il vous suffit d’appeler **SetNumberOfStreams** si vous mélangez plus de quatre flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="66532-146">Therefore, you only need to call **SetNumberOfStreams** if you are mixing more than four video streams.</span></span>

<span data-ttu-id="66532-147">**Exemple de code**</span><span class="sxs-lookup"><span data-stu-id="66532-147">**Example Code**</span></span>

<span data-ttu-id="66532-148">Le code suivant montre comment créer un filtre VMR-7, l’ajouter au graphique de filtre DirectShow, puis mettre le VMR en mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="66532-148">The following code shows how to create a VMR-7 filter, add it to the DirectShow filter graph, and then put the VMR into windowless mode.</span></span> <span data-ttu-id="66532-149">Pour VMR-9, utilisez le CLSID \_ VideoMixingRenderer9 dans **CoCreateInstance** et les interfaces VMR-9 correspondantes.</span><span class="sxs-lookup"><span data-stu-id="66532-149">For the VMR-9, use CLSID\_VideoMixingRenderer9 in **CoCreateInstance** and the corresponding VMR-9 interfaces.</span></span>


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="66532-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66532-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66532-151">Utilisation du mode sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="66532-151">Using Windowless Mode</span></span>](using-windowless-mode.md)
</dt> </dl>

 

 



