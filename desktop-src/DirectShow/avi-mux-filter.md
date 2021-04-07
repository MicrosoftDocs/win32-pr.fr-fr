---
description: Filtre multiplex MUX
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Filtre multiplex MUX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3755a4d5f63e824ae08eb736a5999dcac3d7ab32
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846737"
---
# <a name="avi-mux-filter"></a><span data-ttu-id="ae4c7-103">Filtre multiplex MUX</span><span class="sxs-lookup"><span data-stu-id="ae4c7-103">AVI Mux Filter</span></span>

<span data-ttu-id="ae4c7-104">Le filtre MUX AVI accepte plusieurs flux d’entrée et les entrelace au format AVI.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-104">The AVI Mux filter accepts multiple input streams and interleaves them into AVI format.</span></span> <span data-ttu-id="ae4c7-105">Le filtre utilise des codes confidentiels d’entrée distincts pour chaque flux d’entrée, et une broche de sortie pour le flux AVI.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-105">The filter uses separate input pins for each input stream, and one output pin for the AVI stream.</span></span>

<span data-ttu-id="ae4c7-106">Les applications de capture vidéo ou de création peuvent utiliser ce filtre pour enregistrer des fichiers sur disque au format AVI.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-106">Video capture or authoring applications can use this filter to save files to disk in AVI format.</span></span> <span data-ttu-id="ae4c7-107">Le filtre est généralement connecté au filtre du [writer de fichier](file-writer-filter.md) , mais il peut se connecter à n’importe quel filtre dont la broche d’entrée prend en charge les interfaces IStream et [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="ae4c7-107">The filter is typically connected to the [File Writer](file-writer-filter.md) filter, but it can connect to any filter whose input pin supports the IStream and [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae4c7-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="ae4c7-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="ae4c7-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="ae4c7-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae4c7-110">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="ae4c7-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="ae4c7-111">Tout type principal qui correspond à un FOURCC de style ancien ou MEDIATYPE_AUXLine21Data.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-111">Any major type that corresponds to an old-style FOURCC, or MEDIATYPE_AUXLine21Data.</span></span> <span data-ttu-id="ae4c7-112">(Pour plus d’informations, consultez <a href="fourccmap.md"><strong>FOURCCMap, classe</strong></a>.)</span><span class="sxs-lookup"><span data-stu-id="ae4c7-112">(For more information, see <a href="fourccmap.md"><strong>FOURCCMap Class</strong></a>.)</span></span>
<ul>
<li><span data-ttu-id="ae4c7-113">Si le type principal est MEDIATYPE_Audio, le format doit être FORMAT_WaveFormatEx.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-113">If the major type is MEDIATYPE_Audio, the format must be FORMAT_WaveFormatEx.</span></span></li>
<li><span data-ttu-id="ae4c7-114">Si le type principal est MEDIATYPE_Video, le format doit être FORMAT_VideoInfo ou FORMAT_DvInfo.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-114">If the major type is MEDIATYPE_Video, the format must be FORMAT_VideoInfo or FORMAT_DvInfo.</span></span></li>
<li><span data-ttu-id="ae4c7-115">Si le type principal est MEDIATYPE_Interleaved, le format doit être FORMAT_DvInfo.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-115">If the major type is MEDIATYPE_Interleaved, the format must be FORMAT_DvInfo.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae4c7-116">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="ae4c7-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="ae4c7-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="ae4c7-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae4c7-118">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="ae4c7-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="ae4c7-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span><span class="sxs-lookup"><span data-stu-id="ae4c7-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae4c7-120">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="ae4c7-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="ae4c7-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="ae4c7-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae4c7-122">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="ae4c7-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="ae4c7-123">CLSID_AviDest</span><span class="sxs-lookup"><span data-stu-id="ae4c7-123">CLSID_AviDest</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae4c7-124">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="ae4c7-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="ae4c7-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span><span class="sxs-lookup"><span data-stu-id="ae4c7-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae4c7-126">Exécutable</span><span class="sxs-lookup"><span data-stu-id="ae4c7-126">Executable</span></span></td>
<td><span data-ttu-id="ae4c7-127">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="ae4c7-127">qcap.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae4c7-128"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="ae4c7-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="ae4c7-129">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="ae4c7-129">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae4c7-130"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="ae4c7-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="ae4c7-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="ae4c7-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a><span data-ttu-id="ae4c7-132">Notes</span><span class="sxs-lookup"><span data-stu-id="ae4c7-132">Remarks</span></span>

<span data-ttu-id="ae4c7-133">Les notes suivantes décrivent les différents aspects de la fonctionnalité du filtre multiplex Mux.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-133">The following remarks describe various aspects of the AVI Mux filter's functionality.</span></span>

<span data-ttu-id="ae4c7-134">Épingles</span><span class="sxs-lookup"><span data-stu-id="ae4c7-134">Pins</span></span>

<span data-ttu-id="ae4c7-135">Une fois le filtre multiplex MUX créé, il dispose d’une seule broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-135">When the AVI Mux filter is created, it has one input pin.</span></span> <span data-ttu-id="ae4c7-136">À mesure que chaque broche d’entrée est connectée, le filtre crée une nouvelle broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-136">As each input pin is connected, the filter creates a new input pin.</span></span>

<span data-ttu-id="ae4c7-137">Propriétés du flux</span><span class="sxs-lookup"><span data-stu-id="ae4c7-137">Stream Properties</span></span>

<span data-ttu-id="ae4c7-138">Les broches d’entrée prennent en charge l’interface IPropertyBag pour définir des propriétés sur des flux individuels.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-138">The input pins support the IPropertyBag interface for setting properties on individual streams.</span></span> <span data-ttu-id="ae4c7-139">Actuellement, la propriété suivante est définie :</span><span class="sxs-lookup"><span data-stu-id="ae4c7-139">Currently, the following property is defined:</span></span>



| <span data-ttu-id="ae4c7-140">Propriété</span><span class="sxs-lookup"><span data-stu-id="ae4c7-140">Property</span></span> | <span data-ttu-id="ae4c7-141">Description</span><span class="sxs-lookup"><span data-stu-id="ae4c7-141">Description</span></span>                                                           |
|----------|-----------------------------------------------------------------------|
| <span data-ttu-id="ae4c7-142">name</span><span class="sxs-lookup"><span data-stu-id="ae4c7-142">name</span></span>     | <span data-ttu-id="ae4c7-143">Nom du flux de données.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-143">The name of the stream.</span></span> <span data-ttu-id="ae4c7-144">Cette propriété est écrite sous la forme d’un `'strn'` bloc.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-144">This property is written as a `'strn'` chunk.</span></span> |



 

<span data-ttu-id="ae4c7-145">Si le filtre est en cours d’exécution ou en pause, la méthode IPropertyBag :: Write retourne VFW \_ E \_ mauvais \_ État.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-145">If the filter is running or paused, the IPropertyBag::Write method returns VFW\_E\_WRONG\_STATE.</span></span>

<span data-ttu-id="ae4c7-146">Fréquences d’images</span><span class="sxs-lookup"><span data-stu-id="ae4c7-146">Frame Rates</span></span>

<span data-ttu-id="ae4c7-147">Si le filtre amont ne spécifie pas de fréquence d’images dans le membre **AvgTimePerFrame** de la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , le multiplexeur de flux de contenu (AVI) utilise les horodatages sur la première image vidéo.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-147">If the upstream filter does not specify a frame rate in the **AvgTimePerFrame** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, the AVI Mux uses the time stamps on the first video frame.</span></span> <span data-ttu-id="ae4c7-148">Le format de fichier AVI ne prend pas en charge les fréquences d’images variables.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-148">The AVI file format does not support variable frame rates.</span></span>

<span data-ttu-id="ae4c7-149">Frames supprimés</span><span class="sxs-lookup"><span data-stu-id="ae4c7-149">Dropped Frames</span></span>

<span data-ttu-id="ae4c7-150">Le filtre multiplex MUX calcule les images supprimées en fonction des durées de support de chaque échantillon, le cas échéant, ou des horodatages de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-150">The AVI Mux filter calculates dropped frames based on each sample's media times, if available, or else the sample's time stamps.</span></span> <span data-ttu-id="ae4c7-151">Il écrit une entrée d’index de longueur nulle pour chaque frame supprimé.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-151">It writes a zero-length index entry for every dropped frame.</span></span>

<span data-ttu-id="ae4c7-152">IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="ae4c7-152">IMediaSeeking</span></span>

<span data-ttu-id="ae4c7-153">Le filtre multiplex MUX implémente l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) comme suit :</span><span class="sxs-lookup"><span data-stu-id="ae4c7-153">The AVI Mux filter implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface as follows:</span></span>

-   <span data-ttu-id="ae4c7-154">La méthode [**getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) retourne la progression actuelle du multiplexage.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-154">The [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the current progress of the multiplexing.</span></span> <span data-ttu-id="ae4c7-155">Si vous transcodez un fichier (plus lentement que le temps réel), cette valeur est plus précise que la valeur renvoyée par le gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-155">If you are transcoding a file (slower than real time), this value is more accurate than the value returned by the Filter Graph Manager.</span></span> <span data-ttu-id="ae4c7-156">Pour plus d’informations, consultez la section Notes de la page de référence GetCurrentPosition.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-156">For more information, see the Remarks section of the GetCurrentPosition reference page.</span></span>
-   <span data-ttu-id="ae4c7-157">La méthode [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) interroge chaque filtre en amont et retourne la durée du flux le plus long.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-157">The [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method queries each upstream filter and returns the duration of the longest stream.</span></span> <span data-ttu-id="ae4c7-158">Si l’un de ces filtres échoue à l’appel GetDuration (ou ne prend pas en charge IMediaSeeking), le multiplexeur de contenu AVI retourne un code d’échec et remplit le paramètre *pDuration* avec la durée la plus longue trouvée.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-158">If any of these filters fails the GetDuration call (or does not support IMediaSeeking), the AVI Mux returns a failure code and fills in the *pDuration* parameter with the longest duration found.</span></span> <span data-ttu-id="ae4c7-159">Toutefois, dans ce cas, la valeur de *pDuration* n’est pas nécessairement la longueur du flux d’entrée le plus long.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-159">However, the value of *pDuration* in this case is not necessarily the length of the longest input stream.</span></span>
-   <span data-ttu-id="ae4c7-160">La méthode AVI MUX n’implémente pas les méthodes GetStopPosition, GetPositions, GetAvailable, GetRate ou GetPreroll ; elle n’implémente pas non plus \* de méthodes Set pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-160">The AVI Mux does not implement the GetStopPosition, GetPositions, GetAvailable, GetRate, or GetPreroll methods; nor does it implement any Set\* methods for seeking.</span></span>

<span data-ttu-id="ae4c7-161">Extensions de format de fichier AVI 2,0</span><span class="sxs-lookup"><span data-stu-id="ae4c7-161">AVI 2.0 File Format Extensions</span></span>

<span data-ttu-id="ae4c7-162">DirectShow prend actuellement en charge les extensions de format de fichier AVI 2,0 suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae4c7-162">DirectShow currently supports the following AVI 2.0 file format extensions:</span></span>

-   <span data-ttu-id="ae4c7-163">Augmentation de la taille du fichier AVI (supérieure à 1 Go)</span><span class="sxs-lookup"><span data-stu-id="ae4c7-163">Increased AVI file size (greater than 1 GB)</span></span>
-   <span data-ttu-id="ae4c7-164">Indexation hiérarchique</span><span class="sxs-lookup"><span data-stu-id="ae4c7-164">Hierarchical indexing</span></span>

<span data-ttu-id="ae4c7-165">Pour plus d’informations, consultez la version 1,02 des « extensions de format de fichier AVI OpenDML » publiées par le sous-comité du format de fichier AVI M-JPEG OpenDML.</span><span class="sxs-lookup"><span data-stu-id="ae4c7-165">For more information, see version 1.02 of the "OpenDML AVI File Format Extensions" published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae4c7-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae4c7-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae4c7-167">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="ae4c7-167">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



