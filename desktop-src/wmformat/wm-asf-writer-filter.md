---
title: Filtre d’enregistreur ASF WM (kit de développement logiciel (SDK) Windows Media format 11)
description: En savoir plus sur le filtre d’enregistreur ASF WM.
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
ms.openlocfilehash: d0fbd6e36a8178f6ebd1943cdaac214597e0ba4e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444700"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="76ce7-109">Filtre d’enregistreur ASF WM (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="76ce7-109">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="76ce7-110">Le filtre d’enregistreur ASF WM accepte un nombre variable de flux d’entrée et crée un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="76ce7-110">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="76ce7-111">Le filtre gère l’ensemble de la compression et du multiplexage (bien que le mécanisme de compression puisse être contourné).</span><span class="sxs-lookup"><span data-stu-id="76ce7-111">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="76ce7-112">Vous pouvez utiliser le filtre de l’enregistreur ASF WM dans différents scénarios, notamment la capture vidéo numérique (DV), la recompression audio et la conversion de fichiers multimédias numériques Audio-Video entrelacés (AVI) ou MPEG pour la diffusion réseau.</span><span class="sxs-lookup"><span data-stu-id="76ce7-112">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="76ce7-113">Ce filtre offre la seule façon de créer des fichiers Microsoft Windows Media Audio et Windows Media Video dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="76ce7-113">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="76ce7-114">Pour plus d’informations, consultez [création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="76ce7-114">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="76ce7-115">Le tableau suivant contient des informations sur le filtre de l’enregistreur ASF WM, comme les interfaces et les types de médias qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="76ce7-115">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



| <span data-ttu-id="76ce7-116">Informations de filtre</span><span class="sxs-lookup"><span data-stu-id="76ce7-116">Filter Information</span></span>                       |  <span data-ttu-id="76ce7-117">Types</span><span class="sxs-lookup"><span data-stu-id="76ce7-117">Types</span></span>                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ce7-118">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="76ce7-118">Filter interfaces</span></span>      | <span data-ttu-id="76ce7-119">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="76ce7-119">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="76ce7-120">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="76ce7-120">Input pin media types</span></span>  | <span data-ttu-id="76ce7-121">Dépend du profil.</span><span class="sxs-lookup"><span data-stu-id="76ce7-121">Dependent on the profile.</span></span> <span data-ttu-id="76ce7-122">En général, les types non compressés comme \_ les signaux audio ou MediaType \_ vidéo, bien que les types compressés puissent être acceptés s’ils correspondent au profil</span><span class="sxs-lookup"><span data-stu-id="76ce7-122">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="76ce7-123">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="76ce7-123">Input pin interfaces</span></span>   | <span data-ttu-id="76ce7-124">**IPIN**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (à l’aide de **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="76ce7-124">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="76ce7-125">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="76ce7-125">Output pin media types</span></span> | <span data-ttu-id="76ce7-126">Non applicable</span><span class="sxs-lookup"><span data-stu-id="76ce7-126">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="76ce7-127">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="76ce7-127">Output pin interfaces</span></span>  | <span data-ttu-id="76ce7-128">Non applicable</span><span class="sxs-lookup"><span data-stu-id="76ce7-128">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="76ce7-129">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="76ce7-129">Filter CLSID</span></span>           | <span data-ttu-id="76ce7-130">CLSID \_ WMAsfWriter</span><span class="sxs-lookup"><span data-stu-id="76ce7-130">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="76ce7-131">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="76ce7-131">Property page CLSID</span></span>    | <span data-ttu-id="76ce7-132">CLSID \_ WMAsfWriterProperties</span><span class="sxs-lookup"><span data-stu-id="76ce7-132">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="76ce7-133">Exécutable</span><span class="sxs-lookup"><span data-stu-id="76ce7-133">Executable</span></span>             | <span data-ttu-id="76ce7-134">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="76ce7-134">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="76ce7-135">Mérite</span><span class="sxs-lookup"><span data-stu-id="76ce7-135">Merit</span></span>                  | <span data-ttu-id="76ce7-136">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="76ce7-136">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="76ce7-137">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="76ce7-137">Filter Category</span></span>        | <span data-ttu-id="76ce7-138">Non spécifié</span><span class="sxs-lookup"><span data-stu-id="76ce7-138">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="76ce7-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="76ce7-139">Remarks</span></span>

<span data-ttu-id="76ce7-140">Le nombre de broches d’entrée sur le filtre dépend du profil qui est passé au filtre.</span><span class="sxs-lookup"><span data-stu-id="76ce7-140">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="76ce7-141">Une broche du type de média approprié est créée pour chaque flux défini dans le profil.</span><span class="sxs-lookup"><span data-stu-id="76ce7-141">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="76ce7-142">Les broches d’entrée prennent en charge une méthode à partir de l’interface **IAMStreamConfig** : **IAMStreamConfig :: GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="76ce7-142">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="76ce7-143">Toutes les autres méthodes retournent E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="76ce7-143">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="76ce7-144">Appelez la méthode **GetFormat** pour interroger le format de compression de destination du pin, qui est défini par le profil actuel.</span><span class="sxs-lookup"><span data-stu-id="76ce7-144">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="76ce7-145">Utilisez l’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) pour définir le profil.</span><span class="sxs-lookup"><span data-stu-id="76ce7-145">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="76ce7-146">L’interface **IServiceProvider** du filtre permet aux applications de récupérer l’interface [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , qui est définie dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="76ce7-146">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="76ce7-147">L’interface **IWMWriterAdvanced2** contrôle la désentrelacement vidéo, et est utile si l’entrée est une source [*entrelacée*](wmformat-glossary.md) , telle qu’une vidéo numérique.</span><span class="sxs-lookup"><span data-stu-id="76ce7-147">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="76ce7-148">Utilisez les méthodes **GetInputSetting** et **SetInputSetting** pour contrôler l’entrelacement.</span><span class="sxs-lookup"><span data-stu-id="76ce7-148">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="76ce7-149">Il n’est pas recommandé que les clients utilisent l’une des autres méthodes sur cette interface.</span><span class="sxs-lookup"><span data-stu-id="76ce7-149">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="76ce7-150">Cette interface ne peut être obtenue qu’une fois que le filtre a été ajouté au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="76ce7-150">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="76ce7-151">L’exemple suivant montre comment interroger cette interface :</span><span class="sxs-lookup"><span data-stu-id="76ce7-151">The following example shows how to query for this interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="76ce7-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76ce7-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76ce7-153">**Informations de référence sur DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="76ce7-153">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
