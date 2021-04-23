---
description: Filtre source de fichier (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtre source de fichier (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909697"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="eef0d-103">Filtre source de fichier (Async)</span><span class="sxs-lookup"><span data-stu-id="eef0d-103">File Source (Async) Filter</span></span>

<span data-ttu-id="eef0d-104">Le filtre de source de fichier asynchrone ouvre et lit les fichiers locaux de nombreux formats de données différents et transmet les données à un filtre d’analyseur.</span><span class="sxs-lookup"><span data-stu-id="eef0d-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="eef0d-105">Pour télécharger des fichiers multimédias à partir du Web via HTTP, utilisez le filtre de [source de fichier (URL)](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="eef0d-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="eef0d-106">Pour lire des fichiers ASF, utilisez le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="eef0d-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



| <span data-ttu-id="eef0d-107">Étiquette</span><span class="sxs-lookup"><span data-stu-id="eef0d-107">Label</span></span> | <span data-ttu-id="eef0d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="eef0d-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef0d-109">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="eef0d-109">Filter Interfaces</span></span>                        | <span data-ttu-id="eef0d-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="eef0d-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="eef0d-111">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="eef0d-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="eef0d-112">Non applicable</span><span class="sxs-lookup"><span data-stu-id="eef0d-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="eef0d-113">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="eef0d-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="eef0d-114">Non applicable</span><span class="sxs-lookup"><span data-stu-id="eef0d-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="eef0d-115">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="eef0d-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="eef0d-116">**MediaType \_ Flux** de.</span><span class="sxs-lookup"><span data-stu-id="eef0d-116">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="eef0d-117">Le sous-type dépend du format du média.</span><span class="sxs-lookup"><span data-stu-id="eef0d-117">The subtype depends on the media format.</span></span> <span data-ttu-id="eef0d-118">(**MEDIASUBTYPE \_ null** si le filtre ne reconnaît pas le format.)</span><span class="sxs-lookup"><span data-stu-id="eef0d-118">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="eef0d-119">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="eef0d-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="eef0d-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="eef0d-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="eef0d-121">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="eef0d-121">Filter CLSID</span></span>                             | <span data-ttu-id="eef0d-122">**CLSID \_ AsyncReader**</span><span class="sxs-lookup"><span data-stu-id="eef0d-122">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="eef0d-123">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="eef0d-123">Property Page CLSID</span></span>                      | <span data-ttu-id="eef0d-124">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="eef0d-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="eef0d-125">Exécutable</span><span class="sxs-lookup"><span data-stu-id="eef0d-125">Executable</span></span>                               | <span data-ttu-id="eef0d-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="eef0d-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="eef0d-127">Mérite</span><span class="sxs-lookup"><span data-stu-id="eef0d-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="eef0d-128">**MÉRITE \_ improbable**</span><span class="sxs-lookup"><span data-stu-id="eef0d-128">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="eef0d-129">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="eef0d-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="eef0d-130">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="eef0d-130">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="eef0d-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eef0d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eef0d-132">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="eef0d-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



