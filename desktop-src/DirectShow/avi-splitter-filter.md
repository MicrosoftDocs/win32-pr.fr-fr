---
description: Filtre de séparateur AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtre de séparateur AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61b9a60c4c42aafa875c166ae08ccdf337793c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109714"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="7e6af-103">Filtre de séparateur AVI</span><span class="sxs-lookup"><span data-stu-id="7e6af-103">AVI Splitter Filter</span></span>

<span data-ttu-id="7e6af-104">Le filtre de séparateur AVI est utilisé pour la lecture des fichiers AVI.</span><span class="sxs-lookup"><span data-stu-id="7e6af-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="7e6af-105">Il accepte les données au format AVI et les divise en flux constitutifs pour un traitement et/ou un rendu plus poussés.</span><span class="sxs-lookup"><span data-stu-id="7e6af-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



|                                          |                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e6af-106">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="7e6af-106">Filter Interfaces</span></span>                        | <span data-ttu-id="7e6af-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="7e6af-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="7e6af-108">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="7e6af-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="7e6af-109">\_Flux de MediaType, MEDIASUBTYPE \_ AVI</span><span class="sxs-lookup"><span data-stu-id="7e6af-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="7e6af-110">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="7e6af-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="7e6af-111">[**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="7e6af-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="7e6af-112">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="7e6af-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="7e6af-113">En général, le **\_ son** de la **\_ vidéo** ou du MediaType.</span><span class="sxs-lookup"><span data-stu-id="7e6af-113">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="7e6af-114">Le type exact dépend du contenu du fichier, du fait que le fichier est compressé et du codec utilisé.</span><span class="sxs-lookup"><span data-stu-id="7e6af-114">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="7e6af-115">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="7e6af-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="7e6af-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="7e6af-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="7e6af-117">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="7e6af-117">Filter CLSID</span></span>                             | <span data-ttu-id="7e6af-118">CLSID \_ AviSplitter</span><span class="sxs-lookup"><span data-stu-id="7e6af-118">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="7e6af-119">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="7e6af-119">Property Page CLSID</span></span>                      | <span data-ttu-id="7e6af-120">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7e6af-120">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="7e6af-121">Exécutable</span><span class="sxs-lookup"><span data-stu-id="7e6af-121">Executable</span></span>                               | <span data-ttu-id="7e6af-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="7e6af-122">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="7e6af-123">Mérite</span><span class="sxs-lookup"><span data-stu-id="7e6af-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="7e6af-124">MÉRITE \_ normal</span><span class="sxs-lookup"><span data-stu-id="7e6af-124">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="7e6af-125">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="7e6af-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="7e6af-126">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="7e6af-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7e6af-127">Notes</span><span class="sxs-lookup"><span data-stu-id="7e6af-127">Remarks</span></span>

<span data-ttu-id="7e6af-128">Ce filtre est généralement connecté au filtre de [source de fichier Async](file-source--async--filter.md) sur sa broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7e6af-128">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="7e6af-129">Il peut se connecter à n’importe quel filtre dont la broche de sortie prend en charge [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) et offre le type de média correct à la broche d’entrée du filtre de séparateur avi.</span><span class="sxs-lookup"><span data-stu-id="7e6af-129">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="7e6af-130">Les broches de sortie sur le séparateur AVI prennent en charge la méthode IPropertyBag :: Read pour la lecture des propriétés à partir de flux individuels.</span><span class="sxs-lookup"><span data-stu-id="7e6af-130">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="7e6af-131">Actuellement, la propriété suivante est définie.</span><span class="sxs-lookup"><span data-stu-id="7e6af-131">Currently, the following property is defined.</span></span>



| <span data-ttu-id="7e6af-132">Propriété</span><span class="sxs-lookup"><span data-stu-id="7e6af-132">Property</span></span> | <span data-ttu-id="7e6af-133">Description</span><span class="sxs-lookup"><span data-stu-id="7e6af-133">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e6af-134">name</span><span class="sxs-lookup"><span data-stu-id="7e6af-134">name</span></span>     | <span data-ttu-id="7e6af-135">Retourne le nom du flux, issu du `'strn'` segment dans le fichier avi.</span><span class="sxs-lookup"><span data-stu-id="7e6af-135">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="7e6af-136">Si ce segment est absent, la méthode de lecture retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="7e6af-136">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="7e6af-137">La méthode IPropertyBag :: Write retourne E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="7e6af-137">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="7e6af-138">Le filtre [multiplex MUX](avi-mux-filter.md) prend en charge IPropertyBag :: Write pour l’enregistrement des propriétés de flux dans un fichier avi.</span><span class="sxs-lookup"><span data-stu-id="7e6af-138">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="7e6af-139">Le séparateur AVI n’autorise pas les filtres en aval à utiliser leur propre allocateur.</span><span class="sxs-lookup"><span data-stu-id="7e6af-139">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="7e6af-140">La durée d’entrelacement dans le fichier détermine la quantité de mémoire allouée par le séparateur AVI pour le traiter.</span><span class="sxs-lookup"><span data-stu-id="7e6af-140">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="7e6af-141">Un fichier entrelacé dans un deuxième segment nécessitera une quantité de mémoire supérieure à celle d’un fichier dont la durée d’entrelacement est définie sur un ou deux frames.</span><span class="sxs-lookup"><span data-stu-id="7e6af-141">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="7e6af-142">Sur les ordinateurs modernes, ce n’est généralement pas un problème, sauf si vous exécutez plusieurs instances du séparateur AVI simultanément.</span><span class="sxs-lookup"><span data-stu-id="7e6af-142">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="7e6af-143">Cherche</span><span class="sxs-lookup"><span data-stu-id="7e6af-143">Seeking</span></span>

<span data-ttu-id="7e6af-144">Si le fichier contient un flux vidéo, le séparateur AVI prend en charge la recherche par numéro de frame.</span><span class="sxs-lookup"><span data-stu-id="7e6af-144">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="7e6af-145">Pour activer la recherche basée sur des frames, appelez [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) sur le [Gestionnaire de graphique de filtre](filter-graph-manager.md) avec le **\_ \_ cadre de format d’heure** de valeur.</span><span class="sxs-lookup"><span data-stu-id="7e6af-145">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="7e6af-146">Si le fichier contient un flux audio, le séparateur AVI prend en charge la recherche par échantillon de nombre.</span><span class="sxs-lookup"><span data-stu-id="7e6af-146">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="7e6af-147">Pour activer la recherche basée sur les exemples, appelez [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) sur le gestionnaire de graphique de filtre avec l’exemple de format de date et d' **heure \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="7e6af-147">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="7e6af-148">Dans les deux cas, la broche de sortie pour ce flux doit être connectée à un filtre de convertisseur.</span><span class="sxs-lookup"><span data-stu-id="7e6af-148">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e6af-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7e6af-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e6af-150">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="7e6af-150">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



