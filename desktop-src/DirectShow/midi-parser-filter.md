---
description: Filtre de l’analyseur MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtre de l’analyseur MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b741b2c82eda224a24ffee8a56f8977cbb510f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103949981"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="3ac6a-103">Filtre de l’analyseur MIDI</span><span class="sxs-lookup"><span data-stu-id="3ac6a-103">MIDI Parser Filter</span></span>

<span data-ttu-id="3ac6a-104">Le filtre de l’analyseur MIDI lit les données MIDI qui se trouvent dans. MID et. Fichiers RMI.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="3ac6a-105">Le filtre accepte un flux à partir de la source du [fichier Async](file-source--async--filter.md) ou des filtres de la [source du fichier URL](file-source--url--filter.md) et génère des échantillons midi dans le [**Convertisseur midi**](midi-renderer-filter.md) pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac6a-106">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="3ac6a-106">Filter Interfaces</span></span>                        | <span data-ttu-id="3ac6a-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="3ac6a-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="3ac6a-108">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="3ac6a-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="3ac6a-109">\_Flux de MediaType, MEDIASUBTYPE \_ midi</span><span class="sxs-lookup"><span data-stu-id="3ac6a-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="3ac6a-110">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="3ac6a-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="3ac6a-111">[**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3ac6a-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="3ac6a-112">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="3ac6a-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="3ac6a-113">\_Midi MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="3ac6a-113">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="3ac6a-114">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="3ac6a-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="3ac6a-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="3ac6a-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="3ac6a-116">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="3ac6a-116">Filter CLSID</span></span>                             | <span data-ttu-id="3ac6a-117">CLSID \_ MIDIParser</span><span class="sxs-lookup"><span data-stu-id="3ac6a-117">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="3ac6a-118">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="3ac6a-118">Property Page CLSID</span></span>                      | <span data-ttu-id="3ac6a-119">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="3ac6a-119">No property page</span></span>                                                                                         |
| <span data-ttu-id="3ac6a-120">Exécutable</span><span class="sxs-lookup"><span data-stu-id="3ac6a-120">Executable</span></span>                               | <span data-ttu-id="3ac6a-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="3ac6a-121">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="3ac6a-122">Mérite</span><span class="sxs-lookup"><span data-stu-id="3ac6a-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="3ac6a-123">MÉRITE \_ improbable</span><span class="sxs-lookup"><span data-stu-id="3ac6a-123">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="3ac6a-124">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="3ac6a-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="3ac6a-125">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3ac6a-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="3ac6a-126">Notes</span><span class="sxs-lookup"><span data-stu-id="3ac6a-126">Remarks</span></span>

<span data-ttu-id="3ac6a-127">Pour plus d’informations, consultez la page relative au [**Convertisseur midi**](midi-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3ac6a-127">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ac6a-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ac6a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ac6a-129">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="3ac6a-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



