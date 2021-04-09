---
description: Création de graphiques à l’aide du générateur de graphiques de capture
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: Création de graphiques à l’aide du générateur de graphiques de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846729"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a><span data-ttu-id="2f7bf-103">Création de graphiques à l’aide du générateur de graphiques de capture</span><span class="sxs-lookup"><span data-stu-id="2f7bf-103">Building Graphs with the Capture Graph Builder</span></span>

<span data-ttu-id="2f7bf-104">En dépit de son nom, le générateur de graphiques de capture est utile pour créer de nombreux types de graphiques de filtres personnalisés, non seulement des graphiques de capture.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-104">Despite its name, the Capture Graph Builder is useful for building many kinds of custom filter graphs, not only capture graphs.</span></span> <span data-ttu-id="2f7bf-105">Cet article fournit une brève vue d’ensemble de l’utilisation de cet objet.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-105">This article provides a brief overview of how to use this object.</span></span>

<span data-ttu-id="2f7bf-106">Le générateur de graphiques de capture expose l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-106">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="2f7bf-107">Commencez par appeler [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer le générateur de graphiques de capture et le gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-107">Start by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="2f7bf-108">Ensuite, initialisez le générateur de graphiques de capture en appelant [**ICaptureGraphBuilder2 :: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) avec un pointeur vers le gestionnaire de graphique de filtre, comme suit :</span><span class="sxs-lookup"><span data-stu-id="2f7bf-108">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager, as follows:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a><span data-ttu-id="2f7bf-109">Connexion de filtres</span><span class="sxs-lookup"><span data-stu-id="2f7bf-109">Connecting Filters</span></span>

<span data-ttu-id="2f7bf-110">La méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) connecte deux ou trois filtres ensemble dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-110">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method connects two or three filters together in a chain.</span></span> <span data-ttu-id="2f7bf-111">En règle générale, la méthode fonctionne mieux lorsque chaque filtre n’a pas plus d’une broche d’entrée ou d’une broche de sortie du même type.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-111">Generally, the method works best when each filter has no more than one input pin or output pin of the same type.</span></span> <span data-ttu-id="2f7bf-112">Pour commencer, cette discussion ignore les deux premiers paramètres de **RenderStream** et se focalise sur les trois derniers paramètres.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-112">This discussion begins by ignoring the first two parameters of **RenderStream** and focusing on the last three parameters.</span></span> <span data-ttu-id="2f7bf-113">Le troisième paramètre est un pointeur [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , qui peut spécifier soit un filtre (comme pointeur d’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) ), soit une broche de sortie (comme pointeur d’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) ).</span><span class="sxs-lookup"><span data-stu-id="2f7bf-113">The third parameter is an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer, which can specify either a filter (as an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface pointer) or an output pin (as an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointer).</span></span> <span data-ttu-id="2f7bf-114">Les quatrième et cinquième paramètres spécifient des pointeurs **IBaseFilter** .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-114">The fourth and fifth parameters specify **IBaseFilter** pointers.</span></span> <span data-ttu-id="2f7bf-115">La méthode **RenderStream** connecte les trois filtres dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-115">The **RenderStream** method connects all three filters in a chain.</span></span> <span data-ttu-id="2f7bf-116">Par exemple, supposons que *A*, *B* et *C* sont des filtres.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-116">For example, suppose that *A*, *B*, and *C* are filters.</span></span> <span data-ttu-id="2f7bf-117">Supposons que chaque filtre possède exactement une broche d’entrée et une broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-117">Assume for now that each filter has exactly one input pin and one output pin.</span></span> <span data-ttu-id="2f7bf-118">L’appel suivant connecte A à B, puis B à C :</span><span class="sxs-lookup"><span data-stu-id="2f7bf-118">The following call connects A to B, and then B to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

<span data-ttu-id="2f7bf-119">Toutes les connexions sont « intelligentes », ce qui signifie que des filtres supplémentaires sont ajoutés au graphique en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-119">All connections are "intelligent," meaning that additional filters are added to the graph as needed.</span></span> <span data-ttu-id="2f7bf-120">Pour plus d’informations, consultez [connexion intelligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="2f7bf-120">For details, see [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="2f7bf-121">Pour connecter uniquement deux filtres, définissez la valeur du milieu sur **null**.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-121">To connect just two filters, set the middle value to **NULL**.</span></span> <span data-ttu-id="2f7bf-122">Par exemple, cet appel connecte un à C :</span><span class="sxs-lookup"><span data-stu-id="2f7bf-122">For example, this call connects A to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

<span data-ttu-id="2f7bf-123">Vous pouvez créer des chaînes plus longues en appelant la méthode à deux reprises :</span><span class="sxs-lookup"><span data-stu-id="2f7bf-123">You can create longer chains by calling the method twice:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

<span data-ttu-id="2f7bf-124">Si le dernier paramètre a la **valeur null**, la méthode localise automatiquement un convertisseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-124">If the last parameter is **NULL**, the method automatically locates a default renderer.</span></span> <span data-ttu-id="2f7bf-125">Elle utilise le [convertisseur vidéo](video-renderer-filter.md) pour la vidéo et le [convertisseur DirectSound](directsound-renderer-filter.md) pour l’audio.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-125">It uses the [Video Renderer](video-renderer-filter.md) for video and the [DirectSound Renderer](directsound-renderer-filter.md) for audio.</span></span> <span data-ttu-id="2f7bf-126">Faisant</span><span class="sxs-lookup"><span data-stu-id="2f7bf-126">Thus:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

<span data-ttu-id="2f7bf-127">équivaut à :</span><span class="sxs-lookup"><span data-stu-id="2f7bf-127">is equivalent to</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

<span data-ttu-id="2f7bf-128">où *R* est le convertisseur approprié.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-128">where *R* is the appropriate renderer.</span></span> <span data-ttu-id="2f7bf-129">Toutefois, pour connecter le filtre de convertisseur de mixage vidéo au lieu du convertisseur vidéo, vous devez le spécifier explicitement.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-129">To connect the Video Mixing Renderer filter instead of the Video Renderer, however, you must specify it explicitly.</span></span>

<span data-ttu-id="2f7bf-130">Si vous spécifiez un filtre dans le troisième paramètre, plutôt qu’un code confidentiel, vous devrez peut-être indiquer quelle broche de sortie doit être utilisée pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-130">If you specify a filter in the third parameter, rather than a pin, you may need to indicate which output pin should be used for the connection.</span></span> <span data-ttu-id="2f7bf-131">C’est l’objectif des deux premiers paramètres de la méthode.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-131">That is the purpose of the method's first two parameters.</span></span> <span data-ttu-id="2f7bf-132">Le premier paramètre s’applique uniquement aux filtres de capture.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-132">The first parameter applies only to capture filters.</span></span> <span data-ttu-id="2f7bf-133">Il spécifie un GUID qui indique une catégorie de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-133">It specifies a GUID that indicates a pin category.</span></span> <span data-ttu-id="2f7bf-134">Pour obtenir la liste complète des catégories, consultez [jeu de propriétés pin](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="2f7bf-134">For a complete list of categories, see [Pin Property Set](pin-property-set.md).</span></span> <span data-ttu-id="2f7bf-135">Deux des catégories sont valides pour tous les filtres de capture :</span><span class="sxs-lookup"><span data-stu-id="2f7bf-135">Two of the categories are valid for all capture filters:</span></span>

-   <span data-ttu-id="2f7bf-136">**ÉPINGLer la \_ capture de catégorie \_**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-136">**PIN\_CATEGORY\_CAPTURE**</span></span>
-   <span data-ttu-id="2f7bf-137">**Aperçu de la \_ catégorie pin \_**</span><span class="sxs-lookup"><span data-stu-id="2f7bf-137">**PIN\_CATEGORY\_PREVIEW**</span></span>

<span data-ttu-id="2f7bf-138">Si un filtre de capture ne fournit pas de codes confidentiels distincts pour la capture et l’aperçu, la méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insère un filtre [tee intelligent](smart-tee-filter.md) , qui fractionne le flux en un flux de capture et un flux d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-138">If a capture filter does not supply separate pins for capture and preview, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="2f7bf-139">Du point de vue de l’application, vous pouvez simplement traiter tous les filtres de capture comme ayant des codes confidentiels séparés et ignorer la topologie sous-jacente du graphique.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-139">From the application's standpoint, you can simply treat all capture filters as having separate pins and ignore the underlying topology of the graph.</span></span>

<span data-ttu-id="2f7bf-140">Pour la capture de fichiers, connectez le code confidentiel de capture à un filtre Mux.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-140">For file capture, connect the capture pin to a mux filter.</span></span> <span data-ttu-id="2f7bf-141">Pour l’aperçu instantané, connectez le code confidentiel de l’aperçu à un convertisseur.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-141">For live preview, connect the preview pin to a renderer.</span></span> <span data-ttu-id="2f7bf-142">Si vous permutez les deux catégories, le graphique peut supprimer un nombre excessif de frames pendant la capture de fichier ; Toutefois, si le graphique est correctement connecté, il dépose les images d’aperçu nécessaires pour maintenir le débit sur le flux de capture.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-142">If you switch the two categories, the graph might drop an excessive number of frames during the file capture; but if the graph is connected properly, it drops preview frames as needed in order to maintain throughput on the capture stream.</span></span>

<span data-ttu-id="2f7bf-143">L’exemple suivant montre comment connecter les deux flux :</span><span class="sxs-lookup"><span data-stu-id="2f7bf-143">The following example shows how to connect both streams:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="2f7bf-144">Certains filtres de capture prennent également en charge les sous-titres, indiqués par la **catégorie de pin \_ \_ VBI**.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-144">Some capture filters also support closed captions, indicated by **PIN\_CATEGORY\_VBI**.</span></span> <span data-ttu-id="2f7bf-145">Pour capturer les sous-titres dans un fichier, Affichez cette catégorie dans le filtre Mux.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-145">To capture the closed captions to a file, render this category to the mux filter.</span></span> <span data-ttu-id="2f7bf-146">Pour afficher les sous-titres dans la fenêtre d’aperçu, connectez-vous au convertisseur :</span><span class="sxs-lookup"><span data-stu-id="2f7bf-146">To view the closed captions in your preview window, connect to the renderer:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="2f7bf-147">Le deuxième paramètre de [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifie le type de média, et est généralement l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2f7bf-147">The second parameter to [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifies the media type, and is typically one of the following:</span></span>

-   <span data-ttu-id="2f7bf-148">Audio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="2f7bf-148">MEDIATYPE\_Audio</span></span>
-   <span data-ttu-id="2f7bf-149">Vidéo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="2f7bf-149">MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="2f7bf-150">MEDIATYPE \_ entrelacé (DV)</span><span class="sxs-lookup"><span data-stu-id="2f7bf-150">MEDIATYPE\_Interleaved (DV)</span></span>

<span data-ttu-id="2f7bf-151">Vous pouvez utiliser ce paramètre chaque fois que les broches de sortie du filtre prennent en charge l’énumération des types de médias préférés.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-151">You can use this parameter whenever the filter's output pins support the enumeration of preferred media types.</span></span> <span data-ttu-id="2f7bf-152">Pour les sources de fichiers, le générateur de graphiques de capture ajoute automatiquement un filtre d’analyseur si nécessaire, puis interroge les types de média sur l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-152">For file sources, the Capture Graph Builder automatically adds a parser filter if needed, and then queries the media types on the parser.</span></span> <span data-ttu-id="2f7bf-153">(Pour obtenir un exemple, consultez [recompression d’un fichier AVI](recompressing-an-avi-file.md).) En outre, si le dernier filtre de la chaîne a plusieurs broches d’entrée, la méthode tente d’énumérer leurs types de média.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-153">(For an example, see [Recompressing an AVI File](recompressing-an-avi-file.md).) Also, if the last filter in the chain has several input pins, the method attempts to enumerate their media types.</span></span> <span data-ttu-id="2f7bf-154">Toutefois, tous les filtres ne prennent pas en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-154">However, not all filters support this functionality.</span></span>

## <a name="finding-interfaces-on-filters-and-pins"></a><span data-ttu-id="2f7bf-155">Recherche d’interfaces sur les filtres et les codes confidentiels</span><span class="sxs-lookup"><span data-stu-id="2f7bf-155">Finding Interfaces on Filters and Pins</span></span>

<span data-ttu-id="2f7bf-156">Une fois que vous avez créé un graphique, vous devez généralement Rechercher les différentes interfaces exposées par les filtres et les codes confidentiels dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-156">After you build a graph, you will typically need to locate various interfaces exposed by filters and pins in the graph.</span></span> <span data-ttu-id="2f7bf-157">Par exemple, un filtre de capture peut exposer l’interface [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) , tandis que les broches de sortie du filtre peuvent exposer l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-157">For example, a capture filter might expose the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface, while the filter's output pins might expose the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface.</span></span>

<span data-ttu-id="2f7bf-158">La façon la plus simple de trouver une interface consiste à utiliser la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-158">The simplest way to find an interface is to use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method.</span></span> <span data-ttu-id="2f7bf-159">Cette méthode parcourt le graphique (filtres et codes confidentiels) jusqu’à ce qu’il trouve l’interface souhaitée.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-159">This method walks the graph (filters and pins) until it locates the desired interface.</span></span> <span data-ttu-id="2f7bf-160">Vous pouvez spécifier le point de départ de la recherche, et vous pouvez limiter la recherche aux filtres en amont ou en aval à partir du point de départ.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-160">You can specify the starting point for the search, and you can limit the search to filters upstream or downstream from the starting point.</span></span>

<span data-ttu-id="2f7bf-161">L’exemple suivant recherche l’interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) sur un code pin d’aperçu vidéo :</span><span class="sxs-lookup"><span data-stu-id="2f7bf-161">The following example searches for the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on a video preview pin:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> <span data-ttu-id="2f7bf-162">La rubrique [Rechercher une interface sur un filtre ou un code PIN](find-an-interface-on-a-filter-or-pin.md) affiche une autre approche qui utilise l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) au lieu de [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span><span class="sxs-lookup"><span data-stu-id="2f7bf-162">The topic [Find an Interface on a Filter or Pin](find-an-interface-on-a-filter-or-pin.md) shows an alternative approach that uses the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface instead of [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span></span> <span data-ttu-id="2f7bf-163">L’approche à utiliser dépend de votre application.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-163">Which approach to use depends on your application.</span></span> <span data-ttu-id="2f7bf-164">Si votre application utilise déjà **ICaptureGraphBuilder2** pour générer le graphique, [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) est une bonne approche.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-164">If your application already uses **ICaptureGraphBuilder2** to build the graph, then [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) is a good approach.</span></span> <span data-ttu-id="2f7bf-165">Sinon, envisagez d’utiliser les méthodes **IGraphBuilder** .</span><span class="sxs-lookup"><span data-stu-id="2f7bf-165">Otherwise, consider using the **IGraphBuilder** methods.</span></span>

 

## <a name="finding-pins"></a><span data-ttu-id="2f7bf-166">Rechercher des broches</span><span class="sxs-lookup"><span data-stu-id="2f7bf-166">Finding Pins</span></span>

<span data-ttu-id="2f7bf-167">Moins souvent, vous devrez peut-être localiser un code confidentiel individuel sur un filtre, bien que dans la plupart des cas, les méthodes [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) et [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) vous éviteront les difficultés.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-167">Less commonly, you may need to locate an individual pin on a filter, although in most cases the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) and [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) methods will save you the trouble.</span></span> <span data-ttu-id="2f7bf-168">Si vous avez besoin de rechercher un code PIN particulier sur un filtre, la méthode d’assistance [**ICaptureGraphBuilder2 :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) est utile.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-168">If you do need to find a particular pin on a filter, the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) helper method is useful.</span></span> <span data-ttu-id="2f7bf-169">Spécifiez la catégorie, le type de média (vidéo ou audio), la direction et si le code confidentiel doit être déconnecté.</span><span class="sxs-lookup"><span data-stu-id="2f7bf-169">Specify the category, the media type (video or audio), the direction, and whether the pin must be unconnected.</span></span>

<span data-ttu-id="2f7bf-170">Par exemple, le code suivant recherche un pin de prévisualisation vidéo non connecté sur un filtre de capture :</span><span class="sxs-lookup"><span data-stu-id="2f7bf-170">For example, the following code searches for an unconnected video preview pin on a capture filter:</span></span>


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="2f7bf-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f7bf-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f7bf-172">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="2f7bf-172">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
