---
description: Utilisation du mode sans fenêtre
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Utilisation du mode sans fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866449"
---
# <a name="using-windowless-mode"></a><span data-ttu-id="e10fc-103">Utilisation du mode sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="e10fc-103">Using Windowless Mode</span></span>

<span data-ttu-id="e10fc-104">Le [filtre de convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7) et le [filtre de conversion vidéo Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) prennent en charge le *mode sans fenêtre*, qui représente une amélioration majeure par rapport à l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="e10fc-104">Both the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) support *windowless mode*, which represents a major improvement over the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="e10fc-105">Cette rubrique décrit les différences entre le mode sans fenêtre et le mode fenêtre, et l’utilisation du mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e10fc-105">This topic describes the differences between windowless mode and windowed mode, and how to use windowless mode.</span></span>

<span data-ttu-id="e10fc-106">Pour garantir une compatibilité descendante avec les applications existantes, VMR est par défaut en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e10fc-106">To remain backward-compatible with existing applications, the VMR defaults to windowed mode.</span></span> <span data-ttu-id="e10fc-107">En mode fenêtre, le convertisseur crée sa propre fenêtre pour afficher la vidéo.</span><span class="sxs-lookup"><span data-stu-id="e10fc-107">In windowed mode, the renderer creates its own window to display the video.</span></span> <span data-ttu-id="e10fc-108">En général, l’application définit la fenêtre vidéo en tant qu’enfant de la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="e10fc-108">Typically the application sets the video window to be a child of the application window.</span></span> <span data-ttu-id="e10fc-109">L’existence d’une fenêtre vidéo distincte provoque certains problèmes, toutefois :</span><span class="sxs-lookup"><span data-stu-id="e10fc-109">The existence of a separate video window causes some problems, however:</span></span>

-   <span data-ttu-id="e10fc-110">Plus important encore, il existe un risque de blocages si les messages de fenêtre sont envoyés entre les threads.</span><span class="sxs-lookup"><span data-stu-id="e10fc-110">Most importantly, there is a potential for deadlocks if window messages are sent between threads.</span></span>
-   <span data-ttu-id="e10fc-111">Le gestionnaire de graphique de filtre doit transférer certains messages de fenêtre, tels que WM \_ Paint, au convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="e10fc-111">The Filter Graph Manager must forward certain window messages, such as WM\_PAINT, to the Video Renderer.</span></span> <span data-ttu-id="e10fc-112">L’application doit utiliser l’implémentation de [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) par le gestionnaire de graphique de filtre (et non pas les convertisseurs vidéo), afin que le gestionnaire de graphique de filtre conserve l’état interne correct.</span><span class="sxs-lookup"><span data-stu-id="e10fc-112">The application must use the Filter Graph Manager's implementation of [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (and not the Video Renderer's), so that the Filter Graph Manager maintains the correct internal state.</span></span>
-   <span data-ttu-id="e10fc-113">Pour recevoir des événements de souris ou de clavier à partir de la fenêtre vidéo, l’application doit définir un *drain de message*, ce qui amène la fenêtre vidéo à transférer ces messages à l’application.</span><span class="sxs-lookup"><span data-stu-id="e10fc-113">To receive mouse or keyboard events from the video window, the application must set a *message drain*, causing the video window to forward these messages to the application.</span></span>
-   <span data-ttu-id="e10fc-114">Pour éviter les problèmes de découpage, la fenêtre vidéo doit avoir les styles de fenêtre appropriés.</span><span class="sxs-lookup"><span data-stu-id="e10fc-114">To prevent clipping problems, the video window must have the right window styles.</span></span>

<span data-ttu-id="e10fc-115">Le mode sans fenêtre permet d’éviter ces problèmes en faisant en sorte que VMR dessine directement dans la zone cliente de la fenêtre d’application, à l’aide de DirectDraw pour découper le rectangle vidéo.</span><span class="sxs-lookup"><span data-stu-id="e10fc-115">Windowless mode avoids these problems by having the VMR draw directly on the application window's client area, using DirectDraw to clip the video rectangle.</span></span> <span data-ttu-id="e10fc-116">Le mode sans fenêtre réduit considérablement le risque d’interblocages.</span><span class="sxs-lookup"><span data-stu-id="e10fc-116">Windowless mode significantly reduces the chance of deadlocks.</span></span> <span data-ttu-id="e10fc-117">En outre, l’application n’a pas besoin de définir la fenêtre propriétaire ou les styles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e10fc-117">Also, the application does not have to set the owner window or the window styles.</span></span> <span data-ttu-id="e10fc-118">En fait, quand VMR est en mode sans fenêtre, il n’expose même pas l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) , qui n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e10fc-118">In fact, when the VMR is in windowless mode, it does not even expose the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, which is no longer needed.</span></span>

<span data-ttu-id="e10fc-119">Pour utiliser le mode sans fenêtre, vous devez configurer explicitement VMR.</span><span class="sxs-lookup"><span data-stu-id="e10fc-119">To use windowless mode, you must explicitly configure the VMR.</span></span> <span data-ttu-id="e10fc-120">Toutefois, vous constaterez que est plus flexible et plus facile à utiliser que le mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e10fc-120">However, you will find that is more flexible and easier to use than windowed mode.</span></span>

<span data-ttu-id="e10fc-121">Le filtre VMR-7 et le filtre VMR-9 exposent des interfaces différentes, mais les étapes sont équivalentes à chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="e10fc-121">The VMR-7 filter and the VMR-9 filter expose different interfaces, but the steps are equivalent for each.</span></span>

## <a name="configure-the-vmr-for-windowless-mode"></a><span data-ttu-id="e10fc-122">Configurer VMR pour le mode sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="e10fc-122">Configure the VMR for Windowless Mode</span></span>

<span data-ttu-id="e10fc-123">Pour remplacer le comportement par défaut de VMR, configurez le VMR avant de générer le graphique de filtre :</span><span class="sxs-lookup"><span data-stu-id="e10fc-123">To override the VMR's default behavior, configure the VMR before building the filter graph:</span></span>

<span data-ttu-id="e10fc-124">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="e10fc-124">**VMR-7**</span></span>

1.  <span data-ttu-id="e10fc-125">Créez le gestionnaire de graphe de filtre.</span><span class="sxs-lookup"><span data-stu-id="e10fc-125">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="e10fc-126">Créez VMR-7 et ajoutez-le au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e10fc-126">Create the VMR-7 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="e10fc-127">Appelez [**IVMRFilterConfig :: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) sur VMR-7 avec l’indicateur **\_ sans fenêtre VMRMode** .</span><span class="sxs-lookup"><span data-stu-id="e10fc-127">Call [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) on the VMR-7 with the **VMRMode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="e10fc-128">Interrogez VMR-7 pour l’interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="e10fc-128">Query the VMR-7 for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
5.  <span data-ttu-id="e10fc-129">Appelez [**IVMRWindowlessControl :: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) sur VMR-7.</span><span class="sxs-lookup"><span data-stu-id="e10fc-129">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) on the VMR-7.</span></span> <span data-ttu-id="e10fc-130">Spécifiez un handle vers la fenêtre dans laquelle la vidéo doit apparaître.</span><span class="sxs-lookup"><span data-stu-id="e10fc-130">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="e10fc-131">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="e10fc-131">**VMR-9**</span></span>

1.  <span data-ttu-id="e10fc-132">Créez le gestionnaire de graphe de filtre.</span><span class="sxs-lookup"><span data-stu-id="e10fc-132">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="e10fc-133">Créez VMR-9 et ajoutez-le au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e10fc-133">Create the VMR-9 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="e10fc-134">Appelez [**IVMRFilterConfig9 :: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) sur VMR-9 avec l’indicateur **\_ sans fenêtre VMR9Mode** .</span><span class="sxs-lookup"><span data-stu-id="e10fc-134">Call [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) on the VMR-9 with the **VMR9Mode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="e10fc-135">Interrogez VMR-9 pour l’interface [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="e10fc-135">Query the VMR-9 for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
5.  <span data-ttu-id="e10fc-136">Appelez [**IVMRWindowlessControl9 :: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) sur VMR-9.</span><span class="sxs-lookup"><span data-stu-id="e10fc-136">Call [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) on the VMR-9.</span></span> <span data-ttu-id="e10fc-137">Spécifiez un handle vers la fenêtre dans laquelle la vidéo doit apparaître.</span><span class="sxs-lookup"><span data-stu-id="e10fc-137">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="e10fc-138">Maintenant, générez le reste du graphique de filtre en appelant [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou d’autres méthodes de création de graphiques.</span><span class="sxs-lookup"><span data-stu-id="e10fc-138">Now build the rest of the filter graph by calling [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or other graph-building methods.</span></span> <span data-ttu-id="e10fc-139">Le gestionnaire de graphique de filtre utilise automatiquement l’instance de VMR que vous avez ajoutée au graphique.</span><span class="sxs-lookup"><span data-stu-id="e10fc-139">The Filter Graph Manager automatically uses the instance of the VMR that you added to the graph.</span></span> <span data-ttu-id="e10fc-140">(Pour plus d’informations sur la cause de ce problème, consultez [connexion intelligente](intelligent-connect.md).)</span><span class="sxs-lookup"><span data-stu-id="e10fc-140">(For details on why this happens, see [Intelligent Connect](intelligent-connect.md).)</span></span>

<span data-ttu-id="e10fc-141">Le code suivant illustre une fonction d’assistance qui crée VMR-7, l’ajoute au graphique et configure le mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e10fc-141">The following code shows a helper function that creates the VMR-7, adds it to the graph, and sets up windowless mode.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



<span data-ttu-id="e10fc-142">Cette fonction suppose que n’affiche qu’un seul flux vidéo et ne combine pas une image bitmap statique sur la vidéo.</span><span class="sxs-lookup"><span data-stu-id="e10fc-142">This function assumes that are displaying only one video stream and are not mixing a static bitmap over the video.</span></span> <span data-ttu-id="e10fc-143">Pour plus d’informations, consultez [mode sans fenêtre VMR](vmr-windowless-mode.md).</span><span class="sxs-lookup"><span data-stu-id="e10fc-143">For details, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span> <span data-ttu-id="e10fc-144">Vous appelez cette fonction comme suit :</span><span class="sxs-lookup"><span data-stu-id="e10fc-144">You would call this function as follows:</span></span>


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a><span data-ttu-id="e10fc-145">Positionner la vidéo</span><span class="sxs-lookup"><span data-stu-id="e10fc-145">Position the Video</span></span>

<span data-ttu-id="e10fc-146">Après avoir configuré VMR, l’étape suivante consiste à définir la position de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="e10fc-146">After configuring the VMR, the next step is to set the position of the video.</span></span> <span data-ttu-id="e10fc-147">Il y a deux rectangles à prendre en compte, le rectangle *source* et le rectangle de *destination* .</span><span class="sxs-lookup"><span data-stu-id="e10fc-147">There are two rectangles to consider, the *source* rectangle and the *destination* rectangle.</span></span> <span data-ttu-id="e10fc-148">Le rectangle source définit la partie de la vidéo à afficher.</span><span class="sxs-lookup"><span data-stu-id="e10fc-148">The source rectangle defines which portion of the video to display.</span></span> <span data-ttu-id="e10fc-149">Le rectangle de destination spécifie la région dans la zone cliente de la fenêtre qui contiendra la vidéo.</span><span class="sxs-lookup"><span data-stu-id="e10fc-149">The destination rectangle specifies the region in the window's client area that will contain the video.</span></span> <span data-ttu-id="e10fc-150">VMR découpe l’image vidéo dans le rectangle source et étire l’image rognée pour l’ajuster au rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="e10fc-150">The VMR crops the video image to the source rectangle and stretches the cropped image to fit the destination rectangle.</span></span>

<span data-ttu-id="e10fc-151">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="e10fc-151">**VMR-7**</span></span>

1.  <span data-ttu-id="e10fc-152">Appelez la méthode [**IVMRWindowlessControl :: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) pour spécifier les deux rectangles.</span><span class="sxs-lookup"><span data-stu-id="e10fc-152">Call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="e10fc-153">Le rectangle source doit être inférieur ou égal à la taille de la vidéo Native ; vous pouvez utiliser la méthode [**IVMRWindowlessControl :: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) pour accéder à la taille vidéo native.</span><span class="sxs-lookup"><span data-stu-id="e10fc-153">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="e10fc-154">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="e10fc-154">**VMR-9**</span></span>

1.  <span data-ttu-id="e10fc-155">Appelez la méthode [**IVMRWindowlessControl9 :: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) pour spécifier les deux rectangles.</span><span class="sxs-lookup"><span data-stu-id="e10fc-155">Call the [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="e10fc-156">Le rectangle source doit être inférieur ou égal à la taille de la vidéo Native ; vous pouvez utiliser la méthode [**IVMRWindowlessControl9 :: GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) pour accéder à la taille vidéo native.</span><span class="sxs-lookup"><span data-stu-id="e10fc-156">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl9::GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="e10fc-157">Par exemple, le code suivant définit les rectangles source et de destination pour VMR-7.</span><span class="sxs-lookup"><span data-stu-id="e10fc-157">For example, the following code sets the source and destination rectangles for the VMR-7.</span></span> <span data-ttu-id="e10fc-158">Il définit le rectangle source comme étant la totalité de l’image vidéo et le rectangle de destination sur la totalité de la zone cliente de la fenêtre :</span><span class="sxs-lookup"><span data-stu-id="e10fc-158">It sets the source rectangle equal to the entire video image, and the destination rectangle equal to the entire window client area:</span></span>


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



<span data-ttu-id="e10fc-159">Si vous souhaitez que vidéo occupe une plus petite partie de la zone cliente, modifiez le paramètre *rcDest* .</span><span class="sxs-lookup"><span data-stu-id="e10fc-159">If you want to video to occupy a smaller portion of the client area, modify the *rcDest* parameter.</span></span> <span data-ttu-id="e10fc-160">Si vous souhaitez rogner l’image vidéo, modifiez le paramètre *rcSrc* .</span><span class="sxs-lookup"><span data-stu-id="e10fc-160">If you want to crop the video image, modify the *rcSrc* parameter.</span></span>

## <a name="handle-window-messages"></a><span data-ttu-id="e10fc-161">Gérer les messages de fenêtre</span><span class="sxs-lookup"><span data-stu-id="e10fc-161">Handle Window Messages</span></span>

<span data-ttu-id="e10fc-162">Dans la mesure où VMR n’a pas sa propre fenêtre, il doit être notifié s’il doit redessiner ou redimensionner la vidéo.</span><span class="sxs-lookup"><span data-stu-id="e10fc-162">Because the VMR does not have its own window, it must be notified if it need to repaint or resize the video.</span></span> <span data-ttu-id="e10fc-163">Répondez aux messages de fenêtre suivants en appelant les méthodes VMR listées.</span><span class="sxs-lookup"><span data-stu-id="e10fc-163">Respond to the following window messages by calling the VMR methods listed.</span></span>

<span data-ttu-id="e10fc-164">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="e10fc-164">**VMR-7**</span></span>

1.  <span data-ttu-id="e10fc-165">[**WM \_ PEINDRE**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="e10fc-165">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="e10fc-166">Appelez [**IVMRWindowlessControl :: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="e10fc-166">Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span> <span data-ttu-id="e10fc-167">Cette méthode fait en sorte que VMR-7 redessine la trame vidéo la plus récente.</span><span class="sxs-lookup"><span data-stu-id="e10fc-167">This method causes the VMR-7 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="e10fc-168">[**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): appelez [**IVMRWindowlessControl ::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="e10fc-168">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="e10fc-169">Cette méthode indique à VMR-7 que la vidéo doit être affichée à une nouvelle résolution ou profondeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="e10fc-169">This method notifies the VMR-7 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="e10fc-170">[**WM \_ SIZE**](../winmsg/wm-size.md) ou [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): recalcule la position de la vidéo et appelle [**IVMRWindowlessControl :: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) pour mettre à jour la position, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e10fc-170">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) to update the position, if needed.</span></span>

<span data-ttu-id="e10fc-171">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="e10fc-171">**VMR-9**</span></span>

1.  <span data-ttu-id="e10fc-172">[**WM \_ PEINDRE**](../gdi/wm-paint.md).</span><span class="sxs-lookup"><span data-stu-id="e10fc-172">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="e10fc-173">Appelez [**IVMRWindowlessControl9 :: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="e10fc-173">Call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span> <span data-ttu-id="e10fc-174">Cette méthode oblige VMR-9 à redessiner l’image vidéo la plus récente.</span><span class="sxs-lookup"><span data-stu-id="e10fc-174">This method causes the VMR-9 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="e10fc-175">[**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): appelez [**IVMRWindowlessControl9 ::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="e10fc-175">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span> <span data-ttu-id="e10fc-176">Cette méthode indique à VMR-9 que la vidéo doit être affichée à une nouvelle résolution ou profondeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="e10fc-176">This method notifies the VMR-9 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="e10fc-177">[**WM \_ SIZE**](../winmsg/wm-size.md) ou [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): recalcule la position de la vidéo et appelle [**IVMRWindowlessControl9 :: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) pour mettre à jour la position, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e10fc-177">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) to update the position, if needed.</span></span>

> [!Note]  
> <span data-ttu-id="e10fc-178">Le gestionnaire par défaut pour le message [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) envoie un message de [**\_ taille WM**](../winmsg/wm-size.md) .</span><span class="sxs-lookup"><span data-stu-id="e10fc-178">The default handler for the [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) message sends a [**WM\_SIZE**](../winmsg/wm-size.md) message.</span></span> <span data-ttu-id="e10fc-179">Toutefois, si votre application intercepte **WM \_ WINDOWPOSCHANGED** et ne le transmet pas [**à DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), vous devez appeler **SetVideoPosition** dans votre gestionnaire **WM \_ WINDOWPOSCHANGED** , en plus de votre gestionnaire de **\_ taille WM** .</span><span class="sxs-lookup"><span data-stu-id="e10fc-179">But if your application intercepts **WM\_WINDOWPOSCHANGED** and does not pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), you should call **SetVideoPosition** in your **WM\_WINDOWPOSCHANGED** handler, in addition to your **WM\_SIZE** handler.</span></span>

 

<span data-ttu-id="e10fc-180">L’exemple suivant illustre un gestionnaire de messages de [**\_ peinture WM**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="e10fc-180">The following example shows a [**WM\_PAINT**](../gdi/wm-paint.md) message handler.</span></span> <span data-ttu-id="e10fc-181">Il peint une région définie par le rectangle client moins le rectangle vidéo.</span><span class="sxs-lookup"><span data-stu-id="e10fc-181">It paints a region defined by the client rectangle minus the video rectangle.</span></span> <span data-ttu-id="e10fc-182">Ne dessinez pas sur le rectangle vidéo, car VMR la dessinera, provoquant le scintillement.</span><span class="sxs-lookup"><span data-stu-id="e10fc-182">Do not draw onto the video rectangle, because the VMR will paint over it, causing flickering.</span></span> <span data-ttu-id="e10fc-183">Pour la même raison, ne définissez pas de pinceau d’arrière-plan dans votre classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e10fc-183">For the same reason, do not set a background brush in your window class.</span></span>


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



<span data-ttu-id="e10fc-184">Bien que vous deviez répondre aux messages de [**\_ peinture WM**](../gdi/wm-paint.md) , vous n’avez rien à faire entre les messages de **\_ peinture WM** pour mettre à jour la vidéo.</span><span class="sxs-lookup"><span data-stu-id="e10fc-184">Although you must respond to [**WM\_PAINT**](../gdi/wm-paint.md) messages, there is nothing you need to do between **WM\_PAINT** messages to update the video.</span></span> <span data-ttu-id="e10fc-185">Comme le montre cet exemple, le mode sans fenêtre vous permet de traiter l’image vidéo simplement comme une zone de dessin automatique sur la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e10fc-185">As this example shows, windowless mode lets you treat the video image simply as a self-drawing region on the window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e10fc-186">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e10fc-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e10fc-187">Utilisation du convertisseur de mixage vidéo</span><span class="sxs-lookup"><span data-stu-id="e10fc-187">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="e10fc-188">Rendu vidéo</span><span class="sxs-lookup"><span data-stu-id="e10fc-188">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
