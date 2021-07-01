---
title: Filtre d’enregistreur ASF WM (kit de développement logiciel (SDK) Windows Media format 11)
description: En savoir plus sur le filtre d’enregistreur ASF WM pour le kit de développement logiciel (SDK) du format Windows Media 11. Passez en revue les informations de filtre et consultez les rubriques connexes.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK, WM ASF Writer
- DirectShow, auteur WM ASF
- Filtres QASF, rédacteur WM ASF
- Enregistreur ASF WM, à propos de
- ASF (Advanced Systems Format), le rédacteur WM ASF
- ASF (format des systèmes avancés), enregistreur ASF WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee013b55455c3100ee23e076b767d70fb3ffda
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119664"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="9e2bc-110">Filtre d’enregistreur ASF WM (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="9e2bc-110">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="9e2bc-111">Le filtre d’enregistreur ASF WM accepte un nombre variable de flux d’entrée et crée un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-111">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="9e2bc-112">Le filtre gère l’ensemble de la compression et du multiplexage (bien que le mécanisme de compression puisse être contourné).</span><span class="sxs-lookup"><span data-stu-id="9e2bc-112">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="9e2bc-113">Vous pouvez utiliser le filtre de l’enregistreur ASF WM dans différents scénarios, notamment la capture vidéo numérique (DV), la recompression audio et la conversion de fichiers multimédias numériques Audio-Video entrelacés (AVI) ou MPEG pour la diffusion réseau.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-113">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="9e2bc-114">Ce filtre offre la seule façon de créer des fichiers Microsoft Windows Media Audio et Windows Media Video dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-114">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="9e2bc-115">Pour plus d’informations, consultez [création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="9e2bc-115">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="9e2bc-116">Le tableau suivant contient des informations sur le filtre de l’enregistreur ASF WM, comme les interfaces et les types de médias qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-116">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



| <span data-ttu-id="9e2bc-117">Informations de filtre</span><span class="sxs-lookup"><span data-stu-id="9e2bc-117">Filter Information</span></span>                       |  <span data-ttu-id="9e2bc-118">Types</span><span class="sxs-lookup"><span data-stu-id="9e2bc-118">Types</span></span>                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2bc-119">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="9e2bc-119">Filter interfaces</span></span>      | <span data-ttu-id="9e2bc-120">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="9e2bc-120">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="9e2bc-121">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="9e2bc-121">Input pin media types</span></span>  | <span data-ttu-id="9e2bc-122">Dépend du profil.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-122">Dependent on the profile.</span></span> <span data-ttu-id="9e2bc-123">En général, les types non compressés comme \_ les signaux audio ou MediaType \_ vidéo, bien que les types compressés puissent être acceptés s’ils correspondent au profil</span><span class="sxs-lookup"><span data-stu-id="9e2bc-123">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="9e2bc-124">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="9e2bc-124">Input pin interfaces</span></span>   | <span data-ttu-id="9e2bc-125">**IPIN**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (à l’aide de **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="9e2bc-125">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="9e2bc-126">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="9e2bc-126">Output pin media types</span></span> | <span data-ttu-id="9e2bc-127">Non applicable</span><span class="sxs-lookup"><span data-stu-id="9e2bc-127">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="9e2bc-128">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="9e2bc-128">Output pin interfaces</span></span>  | <span data-ttu-id="9e2bc-129">Non applicable</span><span class="sxs-lookup"><span data-stu-id="9e2bc-129">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="9e2bc-130">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="9e2bc-130">Filter CLSID</span></span>           | <span data-ttu-id="9e2bc-131">CLSID \_ WMAsfWriter</span><span class="sxs-lookup"><span data-stu-id="9e2bc-131">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="9e2bc-132">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="9e2bc-132">Property page CLSID</span></span>    | <span data-ttu-id="9e2bc-133">CLSID \_ WMAsfWriterProperties</span><span class="sxs-lookup"><span data-stu-id="9e2bc-133">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="9e2bc-134">Exécutable</span><span class="sxs-lookup"><span data-stu-id="9e2bc-134">Executable</span></span>             | <span data-ttu-id="9e2bc-135">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="9e2bc-135">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="9e2bc-136">Mérite</span><span class="sxs-lookup"><span data-stu-id="9e2bc-136">Merit</span></span>                  | <span data-ttu-id="9e2bc-137">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="9e2bc-137">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="9e2bc-138">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="9e2bc-138">Filter Category</span></span>        | <span data-ttu-id="9e2bc-139">Non spécifié</span><span class="sxs-lookup"><span data-stu-id="9e2bc-139">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="9e2bc-140">Remarques</span><span class="sxs-lookup"><span data-stu-id="9e2bc-140">Remarks</span></span>

<span data-ttu-id="9e2bc-141">Le nombre de broches d’entrée sur le filtre dépend du profil qui est passé au filtre.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-141">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="9e2bc-142">Une broche du type de média approprié est créée pour chaque flux défini dans le profil.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-142">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="9e2bc-143">Les broches d’entrée prennent en charge une méthode à partir de l’interface **IAMStreamConfig** : **IAMStreamConfig :: GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-143">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="9e2bc-144">Toutes les autres méthodes retournent E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-144">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="9e2bc-145">Appelez la méthode **GetFormat** pour interroger le format de compression de destination du pin, qui est défini par le profil actuel.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-145">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="9e2bc-146">Utilisez l’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) pour définir le profil.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-146">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="9e2bc-147">L’interface **IServiceProvider** du filtre permet aux applications de récupérer l’interface [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , qui est définie dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-147">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="9e2bc-148">L’interface **IWMWriterAdvanced2** contrôle la désentrelacement vidéo, et est utile si l’entrée est une source [*entrelacée*](wmformat-glossary.md) , telle qu’une vidéo numérique.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-148">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="9e2bc-149">Utilisez les méthodes **GetInputSetting** et **SetInputSetting** pour contrôler l’entrelacement.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-149">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="9e2bc-150">Il n’est pas recommandé que les clients utilisent l’une des autres méthodes sur cette interface.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-150">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="9e2bc-151">Cette interface ne peut être obtenue qu’une fois que le filtre a été ajouté au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="9e2bc-151">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="9e2bc-152">L’exemple suivant montre comment interroger cette interface :</span><span class="sxs-lookup"><span data-stu-id="9e2bc-152">The following example shows how to query for this interface:</span></span>


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="9e2bc-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e2bc-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e2bc-154">**Informations de référence sur DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="9e2bc-154">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
