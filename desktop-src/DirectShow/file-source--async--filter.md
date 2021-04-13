---
description: Filtre source de fichier (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtre source de fichier (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481648"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="69a6f-103">Filtre source de fichier (Async)</span><span class="sxs-lookup"><span data-stu-id="69a6f-103">File Source (Async) Filter</span></span>

<span data-ttu-id="69a6f-104">Le filtre de source de fichier asynchrone ouvre et lit les fichiers locaux de nombreux formats de données différents et transmet les données à un filtre d’analyseur.</span><span class="sxs-lookup"><span data-stu-id="69a6f-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="69a6f-105">Pour télécharger des fichiers multimédias à partir du Web via HTTP, utilisez le filtre de [source de fichier (URL)](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="69a6f-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="69a6f-106">Pour lire des fichiers ASF, utilisez le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="69a6f-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69a6f-107">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="69a6f-107">Filter Interfaces</span></span>                        | <span data-ttu-id="69a6f-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="69a6f-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="69a6f-109">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="69a6f-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="69a6f-110">Non applicable</span><span class="sxs-lookup"><span data-stu-id="69a6f-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="69a6f-111">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="69a6f-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="69a6f-112">Non applicable</span><span class="sxs-lookup"><span data-stu-id="69a6f-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="69a6f-113">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="69a6f-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="69a6f-114">**MediaType \_ Flux** de.</span><span class="sxs-lookup"><span data-stu-id="69a6f-114">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="69a6f-115">Le sous-type dépend du format du média.</span><span class="sxs-lookup"><span data-stu-id="69a6f-115">The subtype depends on the media format.</span></span> <span data-ttu-id="69a6f-116">(**MEDIASUBTYPE \_ null** si le filtre ne reconnaît pas le format.)</span><span class="sxs-lookup"><span data-stu-id="69a6f-116">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="69a6f-117">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="69a6f-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="69a6f-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="69a6f-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="69a6f-119">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="69a6f-119">Filter CLSID</span></span>                             | <span data-ttu-id="69a6f-120">**CLSID \_ AsyncReader**</span><span class="sxs-lookup"><span data-stu-id="69a6f-120">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="69a6f-121">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="69a6f-121">Property Page CLSID</span></span>                      | <span data-ttu-id="69a6f-122">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="69a6f-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="69a6f-123">Exécutable</span><span class="sxs-lookup"><span data-stu-id="69a6f-123">Executable</span></span>                               | <span data-ttu-id="69a6f-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="69a6f-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="69a6f-125">Mérite</span><span class="sxs-lookup"><span data-stu-id="69a6f-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="69a6f-126">**MÉRITE \_ improbable**</span><span class="sxs-lookup"><span data-stu-id="69a6f-126">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="69a6f-127">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="69a6f-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="69a6f-128">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="69a6f-128">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="69a6f-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69a6f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69a6f-130">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="69a6f-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



