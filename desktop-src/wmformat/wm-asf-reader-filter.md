---
title: Filtre de lecteur ASF WM (kit de développement logiciel (SDK) Windows Media format 11)
description: En savoir plus sur le filtre de lecteur ASF WM.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK, lecteur ASF WM
- DirectShow, lecteur ASF WM
- Filtres QASF, lecteur ASF WM
- Lecteur ASF WM
- ASF (Advanced Systems Format), lecteur ASF WM
- ASF (format avancé des systèmes), lecteur ASF WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421ab634a0d68837b22961b37005c5670d73e5fa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444280"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="0b196-109">Filtre de lecteur ASF WM (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="0b196-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="0b196-110">En fonction du nom d’un fichier ASF ou d’une URL, le lecteur ASF WM lit le contenu compressé, analyse les flux et expose une broche de sortie pour chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="0b196-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="0b196-111">Ce filtre se connecte en aval au Windows Media Audio ou Windows Media Video DMOs, qui effectue la décompression.</span><span class="sxs-lookup"><span data-stu-id="0b196-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="0b196-112">La recherche est prise en charge si le fichier ASF est accessible en recherche.</span><span class="sxs-lookup"><span data-stu-id="0b196-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="0b196-113">Le lecteur ASF WM applique des horodatages aux échantillons de support en fonction de l’horodatage dans le fichier ASF, mais il ne modifie pas les horodatages de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="0b196-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="0b196-114">En interne, le filtre utilise l’objet lecteur de format Windows Media pour lire le contenu Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0b196-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="0b196-115">Dans le kit de développement logiciel (SDK) DirectX, ce filtre n’est pas le filtre source par défaut pour les fichiers ASF. ainsi, avec ce kit de développement logiciel (SDK), vous ne pouvez pas utiliser ce filtre avec la méthode **RenderFile** . vous devez l’ajouter explicitement au graphique de filtre à l’aide de son identificateur de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="0b196-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="0b196-116">Ce comportement est différent avec le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0b196-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="0b196-117">Lorsque vous installez les bibliothèques Runtime SDK du format Windows Media, le lecteur ASF WM est inscrit comme filtre par défaut pour les fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="0b196-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="0b196-118">Le tableau suivant contient des informations sur le filtre de lecteur ASF WM, telles que les interfaces et les types de médias qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="0b196-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|  <span data-ttu-id="0b196-119">Informations de filtre</span><span class="sxs-lookup"><span data-stu-id="0b196-119">Filter Information</span></span>                      |  <span data-ttu-id="0b196-120">Types</span><span class="sxs-lookup"><span data-stu-id="0b196-120">Types</span></span>                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b196-121">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="0b196-121">Filter interfaces</span></span>      | <span data-ttu-id="0b196-122">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (implémenté partiellement.</span><span class="sxs-lookup"><span data-stu-id="0b196-122">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="0b196-123">Consultez la section Notes.), **IWMReaderAdvanced2** (implémenté partiellement), **IWMDRMReader** (via **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="0b196-123">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="0b196-124">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="0b196-124">Input pin media types</span></span>  | <span data-ttu-id="0b196-125">Non applicable</span><span class="sxs-lookup"><span data-stu-id="0b196-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="0b196-126">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="0b196-126">Input pin interfaces</span></span>   | <span data-ttu-id="0b196-127">Non applicable</span><span class="sxs-lookup"><span data-stu-id="0b196-127">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="0b196-128">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="0b196-128">Output pin media types</span></span> | <span data-ttu-id="0b196-129">\_Video MediaType, MediaType \_ audio, MediaType \_ commande, MediaType \_ filetransfer</span><span class="sxs-lookup"><span data-stu-id="0b196-129">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="0b196-130">Type de format</span><span class="sxs-lookup"><span data-stu-id="0b196-130">Format type</span></span>            | <span data-ttu-id="0b196-131">**VIDEOINFOHEADER2** si le contenu est [*entrelacé*](wmformat-glossary.md), sinon **VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="0b196-131">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="0b196-132">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="0b196-132">Output pin interfaces</span></span>  | <span data-ttu-id="0b196-133">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (via **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="0b196-133">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="0b196-134">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="0b196-134">Filter CLSID</span></span>           | <span data-ttu-id="0b196-135">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="0b196-135">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="0b196-136">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="0b196-136">Property Page CLSID</span></span>    | <span data-ttu-id="0b196-137">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="0b196-137">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="0b196-138">Exécutable</span><span class="sxs-lookup"><span data-stu-id="0b196-138">Executable</span></span>             | <span data-ttu-id="0b196-139">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="0b196-139">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="0b196-140">Mérite</span><span class="sxs-lookup"><span data-stu-id="0b196-140">Merit</span></span>                  | <span data-ttu-id="0b196-141">MÉRITE \_ improbable</span><span class="sxs-lookup"><span data-stu-id="0b196-141">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="0b196-142">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="0b196-142">Filter Category</span></span>        | <span data-ttu-id="0b196-143">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="0b196-143">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="0b196-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="0b196-144">Remarks</span></span>

<span data-ttu-id="0b196-145">Le lecteur ASF WM implémente partiellement les interfaces **IWMReaderAdvanced** et **IWMReaderAdvanced2** afin de permettre aux applications d’accéder aux méthodes d’information sur l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="0b196-145">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="0b196-146">L’implémentation du filtre passe simplement les appels par le biais de à l’interface sur l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="0b196-146">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="0b196-147">Les méthodes de streaming ne sont pas implémentées, car le filtre doit avoir un contrôle total sur le processus de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="0b196-147">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="0b196-148">Les méthodes **IWMReaderAdvanced** et **IWMReaderAdvanced2** suivantes sont implémentées :</span><span class="sxs-lookup"><span data-stu-id="0b196-148">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="0b196-149">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="0b196-149">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="0b196-150">**IWMReaderAdvanced :: SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="0b196-150">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="0b196-151">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="0b196-151">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="0b196-152">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="0b196-152">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="0b196-153">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="0b196-153">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="0b196-154">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="0b196-154">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="0b196-155">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="0b196-155">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="0b196-156">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="0b196-156">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="0b196-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b196-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b196-158">**Informations de référence sur DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="0b196-158">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="0b196-159">**Lecture de fichiers ASF dans DirectShow**</span><span class="sxs-lookup"><span data-stu-id="0b196-159">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




