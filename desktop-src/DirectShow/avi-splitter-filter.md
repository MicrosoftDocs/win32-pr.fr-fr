---
description: Filtre de séparateur AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtre de séparateur AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24335511e9b7b866c85792c2036a4d4b6d089f2a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909657"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="02248-103">Filtre de séparateur AVI</span><span class="sxs-lookup"><span data-stu-id="02248-103">AVI Splitter Filter</span></span>

<span data-ttu-id="02248-104">Le filtre de séparateur AVI est utilisé pour la lecture des fichiers AVI.</span><span class="sxs-lookup"><span data-stu-id="02248-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="02248-105">Il accepte les données au format AVI et les divise en flux constitutifs pour un traitement et/ou un rendu plus poussés.</span><span class="sxs-lookup"><span data-stu-id="02248-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



| <span data-ttu-id="02248-106">Étiquette</span><span class="sxs-lookup"><span data-stu-id="02248-106">Label</span></span> | <span data-ttu-id="02248-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="02248-107">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02248-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="02248-108">Filter Interfaces</span></span>                        | <span data-ttu-id="02248-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="02248-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="02248-110">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="02248-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="02248-111">\_Flux de MediaType, MEDIASUBTYPE \_ AVI</span><span class="sxs-lookup"><span data-stu-id="02248-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="02248-112">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="02248-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="02248-113">[**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="02248-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="02248-114">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="02248-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="02248-115">En général, le **\_ son** de la **\_ vidéo** ou du MediaType.</span><span class="sxs-lookup"><span data-stu-id="02248-115">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="02248-116">Le type exact dépend du contenu du fichier, du fait que le fichier est compressé et du codec utilisé.</span><span class="sxs-lookup"><span data-stu-id="02248-116">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="02248-117">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="02248-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="02248-118">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="02248-118">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="02248-119">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="02248-119">Filter CLSID</span></span>                             | <span data-ttu-id="02248-120">CLSID \_ AviSplitter</span><span class="sxs-lookup"><span data-stu-id="02248-120">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="02248-121">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="02248-121">Property Page CLSID</span></span>                      | <span data-ttu-id="02248-122">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="02248-122">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="02248-123">Exécutable</span><span class="sxs-lookup"><span data-stu-id="02248-123">Executable</span></span>                               | <span data-ttu-id="02248-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="02248-124">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="02248-125">Mérite</span><span class="sxs-lookup"><span data-stu-id="02248-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="02248-126">MÉRITE \_ normal</span><span class="sxs-lookup"><span data-stu-id="02248-126">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="02248-127">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="02248-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="02248-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="02248-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="02248-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="02248-129">Remarks</span></span>

<span data-ttu-id="02248-130">Ce filtre est généralement connecté au filtre de [source de fichier Async](file-source--async--filter.md) sur sa broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="02248-130">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="02248-131">Il peut se connecter à n’importe quel filtre dont la broche de sortie prend en charge [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) et offre le type de média correct à la broche d’entrée du filtre de séparateur avi.</span><span class="sxs-lookup"><span data-stu-id="02248-131">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="02248-132">Les broches de sortie sur le séparateur AVI prennent en charge la méthode IPropertyBag :: Read pour la lecture des propriétés à partir de flux individuels.</span><span class="sxs-lookup"><span data-stu-id="02248-132">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="02248-133">Actuellement, la propriété suivante est définie.</span><span class="sxs-lookup"><span data-stu-id="02248-133">Currently, the following property is defined.</span></span>



| <span data-ttu-id="02248-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="02248-134">Property</span></span> | <span data-ttu-id="02248-135">Description</span><span class="sxs-lookup"><span data-stu-id="02248-135">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02248-136">name</span><span class="sxs-lookup"><span data-stu-id="02248-136">name</span></span>     | <span data-ttu-id="02248-137">Retourne le nom du flux, issu du `'strn'` segment dans le fichier avi.</span><span class="sxs-lookup"><span data-stu-id="02248-137">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="02248-138">Si ce segment est absent, la méthode de lecture retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="02248-138">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="02248-139">La méthode IPropertyBag :: Write retourne E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="02248-139">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="02248-140">Le filtre [multiplex MUX](avi-mux-filter.md) prend en charge IPropertyBag :: Write pour l’enregistrement des propriétés de flux dans un fichier avi.</span><span class="sxs-lookup"><span data-stu-id="02248-140">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="02248-141">Le séparateur AVI n’autorise pas les filtres en aval à utiliser leur propre allocateur.</span><span class="sxs-lookup"><span data-stu-id="02248-141">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="02248-142">La durée d’entrelacement dans le fichier détermine la quantité de mémoire allouée par le séparateur AVI pour le traiter.</span><span class="sxs-lookup"><span data-stu-id="02248-142">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="02248-143">Un fichier entrelacé dans un deuxième segment nécessitera une quantité de mémoire supérieure à celle d’un fichier dont la durée d’entrelacement est définie sur un ou deux frames.</span><span class="sxs-lookup"><span data-stu-id="02248-143">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="02248-144">Sur les ordinateurs modernes, ce n’est généralement pas un problème, sauf si vous exécutez plusieurs instances du séparateur AVI simultanément.</span><span class="sxs-lookup"><span data-stu-id="02248-144">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="02248-145">Cherche</span><span class="sxs-lookup"><span data-stu-id="02248-145">Seeking</span></span>

<span data-ttu-id="02248-146">Si le fichier contient un flux vidéo, le séparateur AVI prend en charge la recherche par numéro de frame.</span><span class="sxs-lookup"><span data-stu-id="02248-146">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="02248-147">Pour activer la recherche basée sur des frames, appelez [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) sur le [Gestionnaire de graphique de filtre](filter-graph-manager.md) avec le **\_ \_ cadre de format d’heure** de valeur.</span><span class="sxs-lookup"><span data-stu-id="02248-147">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="02248-148">Si le fichier contient un flux audio, le séparateur AVI prend en charge la recherche par échantillon de nombre.</span><span class="sxs-lookup"><span data-stu-id="02248-148">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="02248-149">Pour activer la recherche basée sur les exemples, appelez [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) sur le gestionnaire de graphique de filtre avec l’exemple de format de date et d' **heure \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="02248-149">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="02248-150">Dans les deux cas, la broche de sortie pour ce flux doit être connectée à un filtre de convertisseur.</span><span class="sxs-lookup"><span data-stu-id="02248-150">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02248-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02248-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02248-152">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="02248-152">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



