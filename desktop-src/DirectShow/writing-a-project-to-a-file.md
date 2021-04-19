---
description: Écriture d’un projet dans un fichier
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Écriture d’un projet dans un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531993"
---
# <a name="writing-a-project-to-a-file"></a><span data-ttu-id="17f82-103">Écriture d’un projet dans un fichier</span><span class="sxs-lookup"><span data-stu-id="17f82-103">Writing a Project to a File</span></span>

<span data-ttu-id="17f82-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="17f82-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="17f82-105">Cet article explique comment écrire un projet de [services de modification DirectShow](directshow-editing-services.md) dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="17f82-105">This article describes how to write a [DirectShow Editing Services](directshow-editing-services.md) project to a file.</span></span> <span data-ttu-id="17f82-106">Tout d’abord, il décrit comment écrire un fichier avec le moteur de rendu de base.</span><span class="sxs-lookup"><span data-stu-id="17f82-106">First it describes how to write a file with the basic render engine.</span></span> <span data-ttu-id="17f82-107">Il décrit ensuite la recompression intelligente avec le moteur de rendu intelligent.</span><span class="sxs-lookup"><span data-stu-id="17f82-107">Then it describes smart recompression with the smart render engine.</span></span>

<span data-ttu-id="17f82-108">Pour obtenir une vue d’ensemble de la façon dont les services d’édition DirectShow génèrent le rendu des projets, consultez [à propos des moteurs de rendu](about-the-render-engines.md).</span><span class="sxs-lookup"><span data-stu-id="17f82-108">For an overview of how DirectShow Editing Services renders projects, see [About the Render Engines](about-the-render-engines.md).</span></span>

<span data-ttu-id="17f82-109">**Utilisation du moteur de rendu de base**</span><span class="sxs-lookup"><span data-stu-id="17f82-109">**Using the Basic Render Engine**</span></span>

<span data-ttu-id="17f82-110">Commencez par créer la partie frontale du graphique, comme suit :</span><span class="sxs-lookup"><span data-stu-id="17f82-110">Start by building the front end of the graph, as follows:</span></span>

1.  <span data-ttu-id="17f82-111">Créez le moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="17f82-111">Create the render engine.</span></span>
2.  <span data-ttu-id="17f82-112">Spécifiez la chronologie.</span><span class="sxs-lookup"><span data-stu-id="17f82-112">Specify the timeline.</span></span>
3.  <span data-ttu-id="17f82-113">Définissez la plage de rendu.</span><span class="sxs-lookup"><span data-stu-id="17f82-113">Set the render range.</span></span> <span data-ttu-id="17f82-114">(facultatif)</span><span class="sxs-lookup"><span data-stu-id="17f82-114">(Optional)</span></span>
4.  <span data-ttu-id="17f82-115">Créez le composant frontal du graphique.</span><span class="sxs-lookup"><span data-stu-id="17f82-115">Build the front end of the graph.</span></span>

<span data-ttu-id="17f82-116">L’exemple de code suivant illustre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="17f82-116">The following code example shows these steps.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



<span data-ttu-id="17f82-117">Ensuite, ajoutez des filtres de multiplexeur et d’écriture de fichier au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="17f82-117">Next, add multiplexer and file-writing filters to the filter graph.</span></span> <span data-ttu-id="17f82-118">Le moyen le plus simple consiste à utiliser le [Générateur de graphiques de capture](capture-graph-builder.md), un composant DirectShow pour créer des graphiques de capture.</span><span class="sxs-lookup"><span data-stu-id="17f82-118">The easiest way to do this is with the [Capture Graph Builder](capture-graph-builder.md), a DirectShow component for building capture graphs.</span></span> <span data-ttu-id="17f82-119">Le générateur de graphiques de capture expose l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="17f82-119">The capture graph builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="17f82-120">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="17f82-120">Perform the following steps:</span></span>

1.  <span data-ttu-id="17f82-121">Créez une instance du générateur de graphiques de capture.</span><span class="sxs-lookup"><span data-stu-id="17f82-121">Create an instance of the capture graph builder.</span></span>
2.  <span data-ttu-id="17f82-122">Obtenez un pointeur vers le graphique et transmettez-le au générateur de graphiques.</span><span class="sxs-lookup"><span data-stu-id="17f82-122">Obtain a pointer to the graph and pass it to the graph builder.</span></span>
3.  <span data-ttu-id="17f82-123">Spécifiez le nom et le type de média du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="17f82-123">Specify the name and media type of the output file.</span></span> <span data-ttu-id="17f82-124">Cette étape obtient également un pointeur vers le filtre MUX, qui est requis ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="17f82-124">This step also obtains a pointer to the mux filter, which is required later.</span></span>

<span data-ttu-id="17f82-125">L’exemple de code suivant illustre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="17f82-125">The following code example shows these steps.</span></span>


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



<span data-ttu-id="17f82-126">Enfin, connectez les broches de sortie du serveur frontal au filtre Mux.</span><span class="sxs-lookup"><span data-stu-id="17f82-126">Finally, connect the output pins on the front end to the mux filter.</span></span>

1.  <span data-ttu-id="17f82-127">Récupérez le nombre de groupes.</span><span class="sxs-lookup"><span data-stu-id="17f82-127">Retrieve the number of groups.</span></span>
2.  <span data-ttu-id="17f82-128">Pour chaque code confidentiel, obtenez un pointeur vers le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="17f82-128">For each pin, obtain a pointer to the pin.</span></span>
3.  <span data-ttu-id="17f82-129">Si vous le souhaitez, vous pouvez créer une instance d’un filtre de compression pour compresser le flux.</span><span class="sxs-lookup"><span data-stu-id="17f82-129">Optionally, create an instance of a compression filter to compress the stream.</span></span> <span data-ttu-id="17f82-130">Le type de compresseur dépend du type de média du groupe.</span><span class="sxs-lookup"><span data-stu-id="17f82-130">The type of compressor will depend on the media type of the group.</span></span> <span data-ttu-id="17f82-131">Vous pouvez utiliser l' [énumérateur de périphérique système](system-device-enumerator.md) pour énumérer les filtres de compression disponibles.</span><span class="sxs-lookup"><span data-stu-id="17f82-131">You can use the [System Device Enumerator](system-device-enumerator.md) to enumerate the available compression filters.</span></span> <span data-ttu-id="17f82-132">Pour plus d’informations, consultez [énumération des appareils et des filtres](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="17f82-132">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>
4.  <span data-ttu-id="17f82-133">Éventuellement, définissez des paramètres de compression tels que la fréquence d’images clés.</span><span class="sxs-lookup"><span data-stu-id="17f82-133">Optionally, set compression parameters such as the key-frame rate.</span></span> <span data-ttu-id="17f82-134">Cette étape est décrite en détail plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="17f82-134">This step is discussed in detail later in the article.</span></span>
5.  <span data-ttu-id="17f82-135">Appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span><span class="sxs-lookup"><span data-stu-id="17f82-135">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="17f82-136">Cette méthode prend les pointeurs vers le code confidentiel, le filtre de compression (le cas échéant) et le multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="17f82-136">This method takes pointers to the pin, the compression filter (if any), and the multiplexer.</span></span>

<span data-ttu-id="17f82-137">L’exemple de code suivant montre comment connecter les broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="17f82-137">The following code example shows how to connect the output pins.</span></span>


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



<span data-ttu-id="17f82-138">Pour définir les paramètres de compression (étape 4, précédemment), utilisez l’interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) .</span><span class="sxs-lookup"><span data-stu-id="17f82-138">To set compression parameters (step 4, previously), use the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface.</span></span> <span data-ttu-id="17f82-139">Cette interface est exposée sur les broches de sortie des filtres de compression.</span><span class="sxs-lookup"><span data-stu-id="17f82-139">This interface is exposed on the output pins of compression filters.</span></span> <span data-ttu-id="17f82-140">Énumérez les codes confidentiels du filtre de compression, puis interrogez chaque broche de sortie pour **IAMVideoCompression**.</span><span class="sxs-lookup"><span data-stu-id="17f82-140">Enumerate the compression filter's pins, and query each output pin for **IAMVideoCompression**.</span></span> <span data-ttu-id="17f82-141">(Pour plus d’informations sur l’énumération des codes confidentiels, consultez [énumération des codes confidentiels](enumerating-pins.md).) Veillez à libérer tous les pointeurs d’interface que vous avez obtenus lors de cette étape.</span><span class="sxs-lookup"><span data-stu-id="17f82-141">(For information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).) Be sure to release all the interface pointers that you obtained during this step.</span></span>

<span data-ttu-id="17f82-142">Après avoir généré le graphique de filtre, appelez la méthode [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) sur le gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="17f82-142">After you build the filter graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method on the filter graph manager.</span></span> <span data-ttu-id="17f82-143">Au fur et à mesure que le graphique de filtre s’exécute, il écrit les données dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="17f82-143">As the filter graph runs, it writes the data to a file.</span></span> <span data-ttu-id="17f82-144">Utilisez la notification d’événement pour attendre la fin de la lecture.</span><span class="sxs-lookup"><span data-stu-id="17f82-144">Use event notification to wait for playback to complete.</span></span> <span data-ttu-id="17f82-145">(Consultez [réponse aux événements](responding-to-events.md).) Une fois la lecture terminée, vous devez appeler explicitement [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) pour arrêter le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="17f82-145">(See [Responding to Events](responding-to-events.md).) When playback finishes, you must explicitly call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) to stop the filter graph.</span></span> <span data-ttu-id="17f82-146">Dans le cas contraire, le fichier n’est pas écrit correctement.</span><span class="sxs-lookup"><span data-stu-id="17f82-146">Otherwise, the file is not written correctly.</span></span>

<span data-ttu-id="17f82-147">**Utilisation du moteur de rendu intelligent**</span><span class="sxs-lookup"><span data-stu-id="17f82-147">**Using the Smart Render Engine**</span></span>

<span data-ttu-id="17f82-148">Pour bénéficier des avantages de la recompression intelligente, utilisez le moteur de rendu intelligent à la place du moteur de rendu de base.</span><span class="sxs-lookup"><span data-stu-id="17f82-148">To get the benefits of smart recompression, use the smart render engine in place of the basic render engine.</span></span> <span data-ttu-id="17f82-149">Les étapes de création du graphique sont presque les mêmes.</span><span class="sxs-lookup"><span data-stu-id="17f82-149">The steps in building the graph are almost the same.</span></span> <span data-ttu-id="17f82-150">La principale différence réside dans le fait que la compression est gérée au premier plan du graphique, et non dans la section d’écriture de fichiers.</span><span class="sxs-lookup"><span data-stu-id="17f82-150">The major difference is that compression is handled in the front end of the graph, not in the file-writing section.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17f82-151">N’utilisez pas le moteur de rendu intelligent pour lire ou écrire des fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="17f82-151">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

<span data-ttu-id="17f82-152">Chaque groupe vidéo a une propriété qui spécifie le format de compression pour ce groupe.</span><span class="sxs-lookup"><span data-stu-id="17f82-152">Each video group has a property that specifies the compression format for that group.</span></span> <span data-ttu-id="17f82-153">Le format de compression doit correspondre exactement au format non compressé de la hauteur, de la largeur, de la profondeur de bit et de la fréquence d’images du groupe.</span><span class="sxs-lookup"><span data-stu-id="17f82-153">The compression format must exactly match the group's uncompressed format in height, width, bit depth, and frame rate.</span></span> <span data-ttu-id="17f82-154">Le moteur de rendu intelligent utilise le format de compression lorsqu’il construit le graphique.</span><span class="sxs-lookup"><span data-stu-id="17f82-154">The smart render engine uses the compression format when it constructs the graph.</span></span> <span data-ttu-id="17f82-155">Avant de définir le format de compression, veillez à définir le format non compressé pour ce groupe en appelant [**IAMTimelineGroup :: SetMediaType**](iamtimelinegroup-setmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="17f82-155">Before you set the compression format, make sure to set the uncompressed format for that group by calling [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md).</span></span>

<span data-ttu-id="17f82-156">Pour définir le format de compression d’un groupe, appelez la méthode [**IAMTimelineGroup :: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) .</span><span class="sxs-lookup"><span data-stu-id="17f82-156">To set a group's compression format, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span> <span data-ttu-id="17f82-157">Cette méthode prend un pointeur vers une structure [**SCompFmt0**](scompfmt0.md) .</span><span class="sxs-lookup"><span data-stu-id="17f82-157">This method takes a pointer to an [**SCompFmt0**](scompfmt0.md) structure.</span></span> <span data-ttu-id="17f82-158">La structure **SCompFmt0** a deux membres : **nFormatId**, qui doit être zéro, et **MediaType**, qui est une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="17f82-158">The **SCompFmt0** structure has two members: **nFormatId**, which must be zero, and **MediaType**, which is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="17f82-159">Initialisez la structure du **\_ \_ type de média am** avec les informations de format.</span><span class="sxs-lookup"><span data-stu-id="17f82-159">Initialize the **AM\_MEDIA\_TYPE** structure with the format information.</span></span>

> [!Note]  
> <span data-ttu-id="17f82-160">Si vous souhaitez que le projet final ait le même format que l’un de vos fichiers sources, vous pouvez obtenir la \_ structure du type de média am \_ directement à partir du fichier source, à l’aide du détecteur de média.</span><span class="sxs-lookup"><span data-stu-id="17f82-160">If you want the final project to have the same format as one of your source files, you can get the AM\_MEDIA\_TYPE structure directly from the source file, using the media detector.</span></span> <span data-ttu-id="17f82-161">Consultez [**IMediaDet :: obtenir \_ StreamMediaType**](imediadet-get-streammediatype.md).</span><span class="sxs-lookup"><span data-stu-id="17f82-161">See [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md).</span></span>

 

<span data-ttu-id="17f82-162">Effectuez un cast de la variable [**SCompFmt0**](scompfmt0.md) en un pointeur de type **long**, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="17f82-162">Cast the [**SCompFmt0**](scompfmt0.md) variable to a pointer of type **long**, as shown in the following example.</span></span>


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



<span data-ttu-id="17f82-163">Le moteur de rendu intelligent recherche automatiquement un filtre de compression compatible.</span><span class="sxs-lookup"><span data-stu-id="17f82-163">The smart render engine automatically searches for a compatible compression filter.</span></span> <span data-ttu-id="17f82-164">Vous pouvez également spécifier un filtre de compression pour un groupe en appelant [**ISmartRenderEngine :: SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).</span><span class="sxs-lookup"><span data-stu-id="17f82-164">You can also specify a compression filter for a group by calling [**ISmartRenderEngine::SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).</span></span>

<span data-ttu-id="17f82-165">Pour générer le graphique, utilisez les mêmes étapes que celles décrites pour le moteur de rendu de base dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="17f82-165">To build the graph, use the same steps that were described for the Basic Render Engine in the previous section.</span></span> <span data-ttu-id="17f82-166">Les seules différences sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="17f82-166">The only differences are the following:</span></span>

-   <span data-ttu-id="17f82-167">Utilisez le moteur de rendu intelligent, et non le moteur de rendu de base.</span><span class="sxs-lookup"><span data-stu-id="17f82-167">Use the smart render engine, not the basic render engine.</span></span> <span data-ttu-id="17f82-168">L’identificateur de classe est CLSID \_ SmartRenderEngine.</span><span class="sxs-lookup"><span data-stu-id="17f82-168">The class identifier is CLSID\_SmartRenderEngine.</span></span>
-   <span data-ttu-id="17f82-169">Définissez les paramètres de compression après avoir créé le serveur frontal mais avant d’afficher les broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="17f82-169">Set compression parameters after you build the front end but before you render the output pins.</span></span> <span data-ttu-id="17f82-170">Appelez la méthode [**ISmartRenderEngine :: GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) pour obtenir un pointeur vers le filtre de compression d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="17f82-170">Call the [**ISmartRenderEngine::GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) method to obtain a pointer to a group's compression filter.</span></span> <span data-ttu-id="17f82-171">Interrogez ensuite l’interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="17f82-171">Then query for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, as described previously.</span></span>
-   <span data-ttu-id="17f82-172">Lorsque vous affichez les broches de sortie, il n’est pas nécessaire d’insérer un filtre de compression.</span><span class="sxs-lookup"><span data-stu-id="17f82-172">When you render the output pins, there is no need to insert a compression filter.</span></span> <span data-ttu-id="17f82-173">Le flux est déjà compressé.</span><span class="sxs-lookup"><span data-stu-id="17f82-173">The stream is already compressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17f82-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17f82-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17f82-175">Rendu d’un projet</span><span class="sxs-lookup"><span data-stu-id="17f82-175">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



