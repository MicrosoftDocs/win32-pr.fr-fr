---
description: Filtre de source de fichier (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtre de source de fichier (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ddfa7282adbf5117bd2c52465c6eb30efbd69e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909237"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="8cd55-103">Filtre de source de fichier (URL)</span><span class="sxs-lookup"><span data-stu-id="8cd55-103">File Source (URL) Filter</span></span>

<span data-ttu-id="8cd55-104">Le filtre de source du fichier d’URL est un filtre de source asynchrone générique qui fonctionne avec n’importe quel fichier source qui peut être identifié par un Uniform Resource Locator (URL) et dont le type de média majeur est Stream.</span><span class="sxs-lookup"><span data-stu-id="8cd55-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="8cd55-105">Cela comprend les fichiers AVI, MOV, MPEG et WAV.</span><span class="sxs-lookup"><span data-stu-id="8cd55-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="8cd55-106">Le filtre en aval doit être un analyseur, tel que le [séparateur de flux MPEG-1](mpeg-1-stream-splitter-filter.md), le [séparateur AVI](avi-splitter-filter.md)ou l' [Analyseur de film QuickTime](quicktime-movie-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8cd55-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



| <span data-ttu-id="8cd55-107">Étiquette</span><span class="sxs-lookup"><span data-stu-id="8cd55-107">Label</span></span> | <span data-ttu-id="8cd55-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cd55-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd55-109">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="8cd55-109">Filter Interfaces</span></span>                        | <span data-ttu-id="8cd55-110">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="8cd55-110">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="8cd55-111">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="8cd55-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="8cd55-112">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8cd55-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="8cd55-113">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="8cd55-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="8cd55-114">Non applicable</span><span class="sxs-lookup"><span data-stu-id="8cd55-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="8cd55-115">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="8cd55-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="8cd55-116">Flux de MEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="8cd55-116">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="8cd55-117">Le sous-type dépend du format du média.</span><span class="sxs-lookup"><span data-stu-id="8cd55-117">The subtype depends on the media format.</span></span> <span data-ttu-id="8cd55-118">(MEDIASUBTYPE \_ NULL si le filtre ne reconnaît pas le format.)</span><span class="sxs-lookup"><span data-stu-id="8cd55-118">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="8cd55-119">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="8cd55-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="8cd55-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="8cd55-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="8cd55-121">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="8cd55-121">Filter CLSID</span></span>                             | <span data-ttu-id="8cd55-122">CLSID \_ URLReader</span><span class="sxs-lookup"><span data-stu-id="8cd55-122">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="8cd55-123">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="8cd55-123">Property Page CLSID</span></span>                      | <span data-ttu-id="8cd55-124">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="8cd55-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="8cd55-125">Exécutable</span><span class="sxs-lookup"><span data-stu-id="8cd55-125">Executable</span></span>                               | <span data-ttu-id="8cd55-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="8cd55-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="8cd55-127">Mérite</span><span class="sxs-lookup"><span data-stu-id="8cd55-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="8cd55-128">MÉRITE \_ improbable</span><span class="sxs-lookup"><span data-stu-id="8cd55-128">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="8cd55-129">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="8cd55-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="8cd55-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="8cd55-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="8cd55-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="8cd55-131">Remarks</span></span>

<span data-ttu-id="8cd55-132">Ce filtre utilise URLMon et prend en charge les pages de codes.</span><span class="sxs-lookup"><span data-stu-id="8cd55-132">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cd55-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8cd55-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cd55-134">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="8cd55-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



