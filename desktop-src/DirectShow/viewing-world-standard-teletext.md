---
description: Affichage du télétexte standard du monde
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Affichage du télétexte standard du monde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b0885c08403de9578a8dee1eca6e000408ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318726"
---
# <a name="viewing-world-standard-teletext"></a><span data-ttu-id="d776b-103">Affichage du télétexte standard du monde</span><span class="sxs-lookup"><span data-stu-id="d776b-103">Viewing World Standard Teletext</span></span>

> [!Note]  
> <span data-ttu-id="d776b-104">Cette fonctionnalité a été supprimée de Windows Vista et des systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="d776b-104">This functionality has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="d776b-105">Il peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d776b-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="d776b-106">Le WST (World standard Teletext) est encodé dans l’intervalle de blanc vertical (VBI) du signal de télévision analogique.</span><span class="sxs-lookup"><span data-stu-id="d776b-106">World Standard Teletext (WST) is encoded in the vertical blanking interval (VBI) of the analog television signal.</span></span> <span data-ttu-id="d776b-107">Le graphique de filtre pour afficher un aperçu du télétexte est similaire au graphique utilisé pour afficher les sous-titres.</span><span class="sxs-lookup"><span data-stu-id="d776b-107">The filter graph for previewing teletext is similar to the graph used to view closed captions.</span></span> <span data-ttu-id="d776b-108">Le diagramme suivant illustre ce graphique.</span><span class="sxs-lookup"><span data-stu-id="d776b-108">The following diagram illustrates this graph.</span></span>

![graphique d’aperçu WST](images/vidcap10.png)

<span data-ttu-id="d776b-110">Ce graphique utilise les filtres suivants pour l’affichage de WST :</span><span class="sxs-lookup"><span data-stu-id="d776b-110">This graph uses the following filters for WST display:</span></span>

-   <span data-ttu-id="d776b-111">[Convertisseur de tee/récepteur à récepteur](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="d776b-111">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="d776b-112">Accepte les informations VBI du filtre de capture et les divise en flux distincts pour chaque service de données présent sur le signal.</span><span class="sxs-lookup"><span data-stu-id="d776b-112">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span>
-   <span data-ttu-id="d776b-113">[Codec WST](wst-codec-filter.md).</span><span class="sxs-lookup"><span data-stu-id="d776b-113">[WST Codec](wst-codec-filter.md).</span></span> <span data-ttu-id="d776b-114">Décode les données de télétexte à partir des exemples VBI.</span><span class="sxs-lookup"><span data-stu-id="d776b-114">Decodes the Teletext data from the VBI samples.</span></span>
-   <span data-ttu-id="d776b-115">[Décodeur WST](wst-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="d776b-115">[WST Decoder](wst-decoder-filter.md).</span></span> <span data-ttu-id="d776b-116">Convertit les données de télétexte et dessine le texte sur des bitmaps.</span><span class="sxs-lookup"><span data-stu-id="d776b-116">Translates teletext data and draws the text onto bitmaps.</span></span> <span data-ttu-id="d776b-117">Le filtre en aval (dans ce cas, le mélangeur de superposition) recouvre les bitmaps dans la vidéo.</span><span class="sxs-lookup"><span data-stu-id="d776b-117">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="d776b-118">La méthode **RenderStream** du générateur de graphiques de capture ne prend pas en charge directement les filtres WST, de sorte que votre application doit effectuer un travail supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d776b-118">The Capture Graph Builder's **RenderStream** method does not support the WST filters directly, so your application must do some extra work.</span></span>

1.  <span data-ttu-id="d776b-119">Ajoutez le filtre de mixage de superposition au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="d776b-119">Add the Overlay Mixer filter to the filter graph.</span></span> <span data-ttu-id="d776b-120">Le code suivant utilise la fonction AddFilterByCLSID décrite dans [Ajouter un filtre par CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="d776b-120">The following code uses the AddFilterByCLSID function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span> <span data-ttu-id="d776b-121">(AddFilterByCLSID n’est pas une API DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="d776b-121">(AddFilterByCLSID is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  <span data-ttu-id="d776b-122">Connectez la broche d’aperçu au filtre de convertisseur vidéo par le biais du mélangeur de superposition.</span><span class="sxs-lookup"><span data-stu-id="d776b-122">Connect the preview pin to the Video Renderer filter through the Overlay Mixer.</span></span> <span data-ttu-id="d776b-123">Vous pouvez utiliser la méthode **RenderStream** , comme suit :</span><span class="sxs-lookup"><span data-stu-id="d776b-123">You can use the **RenderStream** method, as follows:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  <span data-ttu-id="d776b-124">Ajoutez le filtre de convertisseur de tee/récepteur-à-récepteur au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="d776b-124">Add the Tee/Sink-to-Sink Converter filter to the filter graph.</span></span> <span data-ttu-id="d776b-125">Le code suivant utilise la fonction CreateKernelFilter décrite dans [création de filtres de Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d776b-125">The following code uses the CreateKernelFilter function described in [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span> <span data-ttu-id="d776b-126">(CreateKernelFilter n’est pas une API DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="d776b-126">(CreateKernelFilter is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  <span data-ttu-id="d776b-127">Ajoutez le filtre de codec WST au graphique de filtre :</span><span class="sxs-lookup"><span data-stu-id="d776b-127">Add the WST Codec filter to the filter graph:</span></span>
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  <span data-ttu-id="d776b-128">Appelez **RenderStream** pour connecter le code confidentiel de filtre de capture au convertisseur tee/Sink-to-récepteur, et le convertisseur de tee/récepteur-à-récepteur au filtre de codec WST :</span><span class="sxs-lookup"><span data-stu-id="d776b-128">Call **RenderStream** to connect the capture filter's VBI pin to the Tee/Sink-to-Sink Converter, and the Tee/Sink-to-Sink Converter to the WST Codec filter:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  <span data-ttu-id="d776b-129">Appelez à nouveau **RenderStream** pour connecter le filtre de codec WST au mélangeur de superposition.</span><span class="sxs-lookup"><span data-stu-id="d776b-129">Call **RenderStream** again to connect the WST Codec filter to the Overlay Mixer.</span></span> <span data-ttu-id="d776b-130">Le filtre de décodage WST est automatiquement placé dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="d776b-130">The WST Decoder filter is automatically brought into the graph.</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  <span data-ttu-id="d776b-131">N’oubliez pas de libérer toutes les interfaces de filtre.</span><span class="sxs-lookup"><span data-stu-id="d776b-131">Remember to release all of the filter interfaces.</span></span>
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> <span data-ttu-id="d776b-132">Actuellement, le filtre de décodage WST ne prend pas en charge les connexions au filtre de convertisseur de mixage vidéo (VMR).</span><span class="sxs-lookup"><span data-stu-id="d776b-132">Currently, the WST Decoder filter does not support connections to the Video Mixing Renderer (VMR) filter.</span></span> <span data-ttu-id="d776b-133">Par conséquent, vous devez utiliser le filtre de convertisseur vidéo hérité pour afficher Teletext.</span><span class="sxs-lookup"><span data-stu-id="d776b-133">Therefore, you must use the legacy Video Renderer filter to view teletext.</span></span>

 

<span data-ttu-id="d776b-134">Si le filtre de capture possède un code vidéo (PIN \_ CATEGPORY \_ VIDEOPORT \_ VBI), connectez-le au filtre d' [allocateur de surface VBI](vbi-surface-allocator.md) .</span><span class="sxs-lookup"><span data-stu-id="d776b-134">If the capture filter has a video port VBI pin (PIN\_CATEGPORY\_VIDEOPORT\_VBI), connect it to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="d776b-135">Dans le cas contraire, le graphique ne s’exécutera pas correctement.</span><span class="sxs-lookup"><span data-stu-id="d776b-135">The graph will not run correctly otherwise.</span></span> <span data-ttu-id="d776b-136">L’exemple de code suivant utilise la fonction AddFilterByCLSID, décrite dans [Ajouter un filtre par CLSID](add-a-filter-by-clsid.md)et la fonction FindPinByCategory, décrite dans [utilisation des catégories de code confidentiel](working-with-pin-categories.md).</span><span class="sxs-lookup"><span data-stu-id="d776b-136">The following code example uses the AddFilterByCLSID function, described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the FindPinByCategory function, described in [Working with Pin Categories](working-with-pin-categories.md).</span></span> <span data-ttu-id="d776b-137">(Aucune fonction n’est une API DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="d776b-137">(Neither function is a DirectShow API.)</span></span>


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="d776b-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d776b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d776b-139">Sous-titres et télétexte</span><span class="sxs-lookup"><span data-stu-id="d776b-139">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



