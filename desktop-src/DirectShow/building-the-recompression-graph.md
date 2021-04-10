---
description: Génération du graphique de recompression
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Génération du graphique de recompression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845854"
---
# <a name="building-the-recompression-graph"></a><span data-ttu-id="c9963-103">Génération du graphique de recompression</span><span class="sxs-lookup"><span data-stu-id="c9963-103">Building the Recompression Graph</span></span>

<span data-ttu-id="c9963-104">Un graphique de filtre classique pour la recompression de fichiers AVI ressemble à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="c9963-104">A typical filter graph for AVI file recompression looks like the following:</span></span>

![graphique de recompression AVI](images/avi2avi4.png)

<span data-ttu-id="c9963-106">Le [filtre de séparateur AVI](avi-splitter-filter.md) extrait les données du [filtre source de fichier (Async)](file-source--async--filter.md) et les analyse dans des flux vidéo et audio.</span><span class="sxs-lookup"><span data-stu-id="c9963-106">The [AVI Splitter Filter](avi-splitter-filter.md) pulls data from the [File Source (Async) Filter](file-source--async--filter.md) and parses it into video and audio streams.</span></span> <span data-ttu-id="c9963-107">Le décompresseur vidéo décode la vidéo compressée, où elle est recompressée par le compresseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="c9963-107">The video decompressor decodes the compressed video, where it is recompressed by the video compressor.</span></span> <span data-ttu-id="c9963-108">Le choix des décompresseurs dépend du fichier source ; il sera géré automatiquement par [intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="c9963-108">The choice of decompressors depends on the source file; it will be handled automatically by [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="c9963-109">L’application doit choisir le compresseur, généralement en présentant une liste à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c9963-109">The application must choose the compressor, typically by presenting a list to the user.</span></span> <span data-ttu-id="c9963-110">(Voir [choix d’un filtre de compression](choosing-a-compression-filter.md).)</span><span class="sxs-lookup"><span data-stu-id="c9963-110">(See [Choosing a Compression Filter](choosing-a-compression-filter.md).)</span></span>

<span data-ttu-id="c9963-111">La vidéo compressée passe alors au [filtre multiplex MUX](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="c9963-111">The compressed video then goes to the [AVI Mux Filter](avi-mux-filter.md).</span></span> <span data-ttu-id="c9963-112">Le flux audio de cet exemple n’étant pas compressé, il passe directement du séparateur AVI à AVI Mux.</span><span class="sxs-lookup"><span data-stu-id="c9963-112">The audio stream in this example is not compressed, so it goes directly from the AVI Splitter to the AVI Mux.</span></span> <span data-ttu-id="c9963-113">Le multiplexeur de fichiers AVI entrelace les deux flux et le [filtre du writer de fichier](file-writer-filter.md) écrit la sortie sur le disque.</span><span class="sxs-lookup"><span data-stu-id="c9963-113">The AVI Mux interleaves the two streams, and the [File Writer Filter](file-writer-filter.md) writes the output to disk.</span></span> <span data-ttu-id="c9963-114">Notez que le multiplexeur de données AVI est requis même si le fichier d’origine n’a pas de flux audio.</span><span class="sxs-lookup"><span data-stu-id="c9963-114">Note that the AVI Mux is required even if the original file does not have an audio stream.</span></span>

<span data-ttu-id="c9963-115">Le moyen le plus simple de créer ce graphique de filtre consiste à utiliser le [Générateur de graphiques de capture](capture-graph-builder.md), qui est un composant DirectShow pour générer des graphiques de capture et d’autres graphiques de filtres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="c9963-115">The easiest way to build this filter graph is to use the [Capture Graph Builder](capture-graph-builder.md), which is a DirectShow component for building capture graphs and other custom filter graphs.</span></span>

<span data-ttu-id="c9963-116">Commencez par appeler CoCreateInstance pour créer le générateur de graphiques de capture :</span><span class="sxs-lookup"><span data-stu-id="c9963-116">Start by calling CoCreateInstance to create the Capture Graph Builder:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



<span data-ttu-id="c9963-117">Utilisez ensuite le générateur de graphiques de capture pour générer le graphique de filtre :</span><span class="sxs-lookup"><span data-stu-id="c9963-117">Then use the Capture Graph Builder to build the filter graph:</span></span>

1.  <span data-ttu-id="c9963-118">Générez la section de rendu du graphique, qui comprend le filtre multiplex MUX et le [writer de fichier](file-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="c9963-118">Build the rendering section of the graph, which includes the AVI Mux filter and the [File Writer](file-writer-filter.md).</span></span>
2.  <span data-ttu-id="c9963-119">Ajoutez le filtre source et le filtre de compression au graphique.</span><span class="sxs-lookup"><span data-stu-id="c9963-119">Add the source filter and the compression filter to the graph.</span></span>
3.  <span data-ttu-id="c9963-120">Connectez le filtre source au filtre MUX.</span><span class="sxs-lookup"><span data-stu-id="c9963-120">Connect the source filter to the MUX filter.</span></span> <span data-ttu-id="c9963-121">Le générateur de graphiques de capture insère les filtres de séparateur et de décodeur nécessaires pour analyser le fichier source.</span><span class="sxs-lookup"><span data-stu-id="c9963-121">The capture graph builder inserts whatever splitter and decoder filters are needed to parse the source file.</span></span> <span data-ttu-id="c9963-122">Il peut également acheminer les flux vidéo et audio via des filtres de compression.</span><span class="sxs-lookup"><span data-stu-id="c9963-122">It can also route the video and audio streams through compression filters.</span></span>

<span data-ttu-id="c9963-123">Les sections suivantes décrivent chacune de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="c9963-123">The following sections explain each of these steps.</span></span>

<span data-ttu-id="c9963-124">Générer la section de rendu</span><span class="sxs-lookup"><span data-stu-id="c9963-124">Build the Rendering Section</span></span>

<span data-ttu-id="c9963-125">Pour générer la section de rendu du graphique, appelez la méthode [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) .</span><span class="sxs-lookup"><span data-stu-id="c9963-125">To build the rendering section of the graph, call the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method.</span></span> <span data-ttu-id="c9963-126">Cette méthode accepte les paramètres d’entrée qui spécifient le sous-type de média pour la sortie et le nom du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="c9963-126">This method takes input parameters that specify the media subtype for the output and the name of the output file.</span></span> <span data-ttu-id="c9963-127">Elle retourne des pointeurs vers le filtre MUX et le writer de fichier.</span><span class="sxs-lookup"><span data-stu-id="c9963-127">It returns pointers to the MUX filter and the file writer.</span></span> <span data-ttu-id="c9963-128">Le filtre MUX est nécessaire pour l’étape suivante de la génération de graphiques.</span><span class="sxs-lookup"><span data-stu-id="c9963-128">The MUX filter is needed for the next stage of graph building.</span></span> <span data-ttu-id="c9963-129">Le pointeur vers le writer de fichier n’est pas nécessaire pour cet exemple, afin que le paramètre puisse être **null**:</span><span class="sxs-lookup"><span data-stu-id="c9963-129">The pointer to the file writer is not needed for this example, so that parameter can be **NULL**:</span></span>


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



<span data-ttu-id="c9963-130">Lorsque la méthode est retournée, le filtre MUX a un nombre de références en suspens. par conséquent, veillez à libérer le pointeur ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="c9963-130">When the method returns, the MUX filter has an outstanding reference count, so be sure to release the pointer later.</span></span>

<span data-ttu-id="c9963-131">Le diagramme suivant montre le graphique de filtre à ce stade.</span><span class="sxs-lookup"><span data-stu-id="c9963-131">The following diagram shows the filter graph at this point.</span></span>

![section de rendu du graphique de filtre](images/avi2avi1.png)

<span data-ttu-id="c9963-133">Le filtre MUX expose deux interfaces pour le contrôle du format AVI :</span><span class="sxs-lookup"><span data-stu-id="c9963-133">The MUX filter exposes two interfaces for controlling the AVI format:</span></span>

-   <span data-ttu-id="c9963-134">[**Interface IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): définit le mode d’entrelacement.</span><span class="sxs-lookup"><span data-stu-id="c9963-134">[**IConfigInterleaving Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): Sets the interleaving mode.</span></span>
-   <span data-ttu-id="c9963-135">[**Interface IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): définit le flux principal et l’index de compatibilité avi.</span><span class="sxs-lookup"><span data-stu-id="c9963-135">[**IConfigAviMux Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): Sets the master stream and the AVI compatibility index.</span></span>

<span data-ttu-id="c9963-136">Ajouter les filtres source et de compression</span><span class="sxs-lookup"><span data-stu-id="c9963-136">Add the Source and Compression Filters</span></span>

<span data-ttu-id="c9963-137">L’étape suivante consiste à ajouter les filtres source et de compression au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c9963-137">The next step is to add the source and compression filters to the filter graph.</span></span> <span data-ttu-id="c9963-138">Le générateur de graphiques de capture crée automatiquement une instance du gestionnaire de graphes de filtre quand vous appelez SetOutputFileName.</span><span class="sxs-lookup"><span data-stu-id="c9963-138">The Capture Graph Builder automatically creates an instance of the Filter Graph Manager when you call SetOutputFileName.</span></span> <span data-ttu-id="c9963-139">Pour obtenir un pointeur vers cette dernière, appelez la méthode [**ICaptureGraphBuilder2 :: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) :</span><span class="sxs-lookup"><span data-stu-id="c9963-139">Get a pointer to it by calling the [**ICaptureGraphBuilder2::GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) method:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



<span data-ttu-id="c9963-140">À présent, appelez la méthode [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) pour ajouter le filtre de source de fichier Async et la méthode [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) pour ajouter le compresseur vidéo :</span><span class="sxs-lookup"><span data-stu-id="c9963-140">Now call the [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) method to add the Async File Source filter, and the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method to add the video compressor:</span></span>


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



<span data-ttu-id="c9963-141">À ce stade, le filtre source et le filtre de compression ne sont pas connectés à d’autres éléments dans le graphique, comme indiqué dans l’illustration suivante :</span><span class="sxs-lookup"><span data-stu-id="c9963-141">At this point, the source filter and the compression filter are not connected to anything else in the graph, as shown in the following illustration:</span></span>

![filtrer le graphique avec les filtres source et de compression](images/avi2avi2.png)

<span data-ttu-id="c9963-143">Connecter la source au multiplexeur</span><span class="sxs-lookup"><span data-stu-id="c9963-143">Connect the Source to the Mux</span></span>

<span data-ttu-id="c9963-144">La dernière étape consiste à connecter le filtre source au filtre multiplex MUX par le biais du compresseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="c9963-144">The final step is to connect the source filter to the AVI Mux filter, through the video compressor.</span></span> <span data-ttu-id="c9963-145">Utilisez la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , qui connecte une broche de sortie sur le filtre source à un filtre de récepteur spécifié, éventuellement à l’aide d’un filtre de compression.</span><span class="sxs-lookup"><span data-stu-id="c9963-145">Use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method, which connects an output pin on the source filter to a specified sink filter, optionally through a compression filter.</span></span>

<span data-ttu-id="c9963-146">Les deux premiers paramètres spécifient les codes confidentiels du filtre source à connecter, en désignant une catégorie de code confidentiel et un type de média.</span><span class="sxs-lookup"><span data-stu-id="c9963-146">The first two parameters specify which of the source filter's pins to connect, by designating a pin category and a media type.</span></span> <span data-ttu-id="c9963-147">Le filtre de source de fichier Async n’a qu’une seule broche de sortie. ces paramètres doivent donc avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c9963-147">The Async File Source filter has only one output pin, so these parameters should be **NULL**.</span></span> <span data-ttu-id="c9963-148">Les trois paramètres suivants spécifient le filtre source, le filtre de compression (le cas échéant) et le filtre Mux.</span><span class="sxs-lookup"><span data-stu-id="c9963-148">The next three parameters specify the source filter, the compression filter (if any), and the Mux filter.</span></span>

<span data-ttu-id="c9963-149">L’exemple de code suivant affiche le flux vidéo via le compresseur vidéo :</span><span class="sxs-lookup"><span data-stu-id="c9963-149">The following code example renders the video stream through the video compressor:</span></span>


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



<span data-ttu-id="c9963-150">Le diagramme suivant illustre le graphique de filtre jusqu’à présent.</span><span class="sxs-lookup"><span data-stu-id="c9963-150">The following diagram shows the filter graph so far.</span></span>

![flux vidéo rendu](images/avi2avi3.png)

<span data-ttu-id="c9963-152">En supposant que le fichier source possède un flux audio, le filtre de [fractionnement AVI](avi-splitter-filter.md) a créé une broche de sortie pour l’audio.</span><span class="sxs-lookup"><span data-stu-id="c9963-152">Assuming that the source file has an audio stream, the [AVI Splitter](avi-splitter-filter.md) filter has created an output pin for the audio.</span></span> <span data-ttu-id="c9963-153">Pour connecter ce code confidentiel, appelez à nouveau RenderStream :</span><span class="sxs-lookup"><span data-stu-id="c9963-153">To connect this pin, call RenderStream again:</span></span>


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



<span data-ttu-id="c9963-154">Ici, aucun filtre de compression n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="c9963-154">Here, no compression filter is specified.</span></span> <span data-ttu-id="c9963-155">La broche de sortie du filtre source est déjà connectée, de sorte que la méthode RenderStream recherche une broche de sortie non connectée sur le filtre Splitter.</span><span class="sxs-lookup"><span data-stu-id="c9963-155">The source filter's output pin is already connected, so the RenderStream method searches for an unconnected output pin on the splitter filter.</span></span> <span data-ttu-id="c9963-156">Il recherche le code confidentiel audio et le connecte directement au filtre MUX.</span><span class="sxs-lookup"><span data-stu-id="c9963-156">It finds the audio pin and connects it directly to the MUX filter.</span></span> <span data-ttu-id="c9963-157">Si le fichier source n’a pas de flux audio, le deuxième appel à RenderStream échoue.</span><span class="sxs-lookup"><span data-stu-id="c9963-157">If the source file does not have an audio stream, the second call to RenderStream will fail.</span></span> <span data-ttu-id="c9963-158">Ce comportement est normal.</span><span class="sxs-lookup"><span data-stu-id="c9963-158">This is expected behavior.</span></span> <span data-ttu-id="c9963-159">Le graphique étant terminé après le premier appel à RenderStream, l’échec dans le deuxième appel est sans conséquence.</span><span class="sxs-lookup"><span data-stu-id="c9963-159">The graph is complete after the first call to RenderStream, so the failure in the second call is harmless.</span></span>

<span data-ttu-id="c9963-160">Dans cet exemple, l’ordre des deux appels RenderStream est important.</span><span class="sxs-lookup"><span data-stu-id="c9963-160">In this example, the order of the two RenderStream calls is important.</span></span> <span data-ttu-id="c9963-161">Étant donné que le deuxième appel ne spécifie pas de compresseur, il connecte tout code confidentiel non connecté du séparateur AVI.</span><span class="sxs-lookup"><span data-stu-id="c9963-161">Because the second call does not specify a compressor, it will connect any unconnected pin from the AVI Splitter.</span></span> <span data-ttu-id="c9963-162">Si vous effectuez cet appel avant l’autre, il peut connecter le flux vidéo au AVI MUX, sans votre compresseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="c9963-162">If you make this call before the other one, it might connect the video stream to the AVI Mux, without your video compressor.</span></span> <span data-ttu-id="c9963-163">Par conséquent, l’appel plus spécifique (avec le filtre de compression) doit se produire en premier.</span><span class="sxs-lookup"><span data-stu-id="c9963-163">Therefore, the more specific call (with the compression filter) must happen first.</span></span>

<span data-ttu-id="c9963-164">La discussion précédente suppose que le fichier source est un fichier AVI.</span><span class="sxs-lookup"><span data-stu-id="c9963-164">The previous discussion has assumed that the source file is an AVI file.</span></span> <span data-ttu-id="c9963-165">Toutefois, cette technique fonctionne également avec d’autres types de fichiers, tels que les fichiers MPEG.</span><span class="sxs-lookup"><span data-stu-id="c9963-165">However, this technique also works with other file types, such as MPEG files.</span></span> <span data-ttu-id="c9963-166">Le graphique de filtre résultant est quelque peu différent.</span><span class="sxs-lookup"><span data-stu-id="c9963-166">The resulting filter graph will be somewhat different.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9963-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9963-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9963-168">Recompression d’un fichier AVI</span><span class="sxs-lookup"><span data-stu-id="c9963-168">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 



