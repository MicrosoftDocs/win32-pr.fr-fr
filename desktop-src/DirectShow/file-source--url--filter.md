---
description: Filtre de source de fichier (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtre de source de fichier (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109571"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="90da0-103">Filtre de source de fichier (URL)</span><span class="sxs-lookup"><span data-stu-id="90da0-103">File Source (URL) Filter</span></span>

<span data-ttu-id="90da0-104">Le filtre de source du fichier d’URL est un filtre de source asynchrone générique qui fonctionne avec n’importe quel fichier source qui peut être identifié par un Uniform Resource Locator (URL) et dont le type de média majeur est Stream.</span><span class="sxs-lookup"><span data-stu-id="90da0-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="90da0-105">Cela comprend les fichiers AVI, MOV, MPEG et WAV.</span><span class="sxs-lookup"><span data-stu-id="90da0-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="90da0-106">Le filtre en aval doit être un analyseur, tel que le [séparateur de flux MPEG-1](mpeg-1-stream-splitter-filter.md), le [séparateur AVI](avi-splitter-filter.md)ou l' [Analyseur de film QuickTime](quicktime-movie-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="90da0-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90da0-107">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="90da0-107">Filter Interfaces</span></span>                        | <span data-ttu-id="90da0-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="90da0-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="90da0-109">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="90da0-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="90da0-110">Non applicable</span><span class="sxs-lookup"><span data-stu-id="90da0-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="90da0-111">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="90da0-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="90da0-112">Non applicable</span><span class="sxs-lookup"><span data-stu-id="90da0-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="90da0-113">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="90da0-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="90da0-114">Flux de MEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="90da0-114">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="90da0-115">Le sous-type dépend du format du média.</span><span class="sxs-lookup"><span data-stu-id="90da0-115">The subtype depends on the media format.</span></span> <span data-ttu-id="90da0-116">(MEDIASUBTYPE \_ NULL si le filtre ne reconnaît pas le format.)</span><span class="sxs-lookup"><span data-stu-id="90da0-116">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="90da0-117">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="90da0-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="90da0-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="90da0-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="90da0-119">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="90da0-119">Filter CLSID</span></span>                             | <span data-ttu-id="90da0-120">CLSID \_ URLReader</span><span class="sxs-lookup"><span data-stu-id="90da0-120">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="90da0-121">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="90da0-121">Property Page CLSID</span></span>                      | <span data-ttu-id="90da0-122">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="90da0-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="90da0-123">Exécutable</span><span class="sxs-lookup"><span data-stu-id="90da0-123">Executable</span></span>                               | <span data-ttu-id="90da0-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="90da0-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="90da0-125">Mérite</span><span class="sxs-lookup"><span data-stu-id="90da0-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="90da0-126">MÉRITE \_ improbable</span><span class="sxs-lookup"><span data-stu-id="90da0-126">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="90da0-127">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="90da0-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="90da0-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="90da0-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="90da0-129">Notes</span><span class="sxs-lookup"><span data-stu-id="90da0-129">Remarks</span></span>

<span data-ttu-id="90da0-130">Ce filtre utilise URLMon et prend en charge les pages de codes.</span><span class="sxs-lookup"><span data-stu-id="90da0-130">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90da0-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90da0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90da0-132">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="90da0-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



