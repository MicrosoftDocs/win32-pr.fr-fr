---
description: Filtre de l’analyseur MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtre de l’analyseur MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ce659559852497b8ec55709e77f9510a1deaf2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908427"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="087dd-103">Filtre de l’analyseur MIDI</span><span class="sxs-lookup"><span data-stu-id="087dd-103">MIDI Parser Filter</span></span>

<span data-ttu-id="087dd-104">Le filtre de l’analyseur MIDI lit les données MIDI qui se trouvent dans. MID et. Fichiers RMI.</span><span class="sxs-lookup"><span data-stu-id="087dd-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="087dd-105">Le filtre accepte un flux à partir de la source du [fichier Async](file-source--async--filter.md) ou des filtres de la [source du fichier URL](file-source--url--filter.md) et génère des échantillons midi dans le [**Convertisseur midi**](midi-renderer-filter.md) pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="087dd-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



| <span data-ttu-id="087dd-106">Étiquette</span><span class="sxs-lookup"><span data-stu-id="087dd-106">Label</span></span> | <span data-ttu-id="087dd-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="087dd-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="087dd-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="087dd-108">Filter Interfaces</span></span>                        | <span data-ttu-id="087dd-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="087dd-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="087dd-110">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="087dd-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="087dd-111">\_Flux de MediaType, MEDIASUBTYPE \_ midi</span><span class="sxs-lookup"><span data-stu-id="087dd-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="087dd-112">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="087dd-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="087dd-113">[**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="087dd-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="087dd-114">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="087dd-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="087dd-115">\_Midi MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="087dd-115">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="087dd-116">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="087dd-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="087dd-117">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="087dd-117">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="087dd-118">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="087dd-118">Filter CLSID</span></span>                             | <span data-ttu-id="087dd-119">CLSID \_ MIDIParser</span><span class="sxs-lookup"><span data-stu-id="087dd-119">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="087dd-120">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="087dd-120">Property Page CLSID</span></span>                      | <span data-ttu-id="087dd-121">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="087dd-121">No property page</span></span>                                                                                         |
| <span data-ttu-id="087dd-122">Exécutable</span><span class="sxs-lookup"><span data-stu-id="087dd-122">Executable</span></span>                               | <span data-ttu-id="087dd-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="087dd-123">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="087dd-124">Mérite</span><span class="sxs-lookup"><span data-stu-id="087dd-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="087dd-125">MÉRITE \_ improbable</span><span class="sxs-lookup"><span data-stu-id="087dd-125">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="087dd-126">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="087dd-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="087dd-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="087dd-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="087dd-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="087dd-128">Remarks</span></span>

<span data-ttu-id="087dd-129">Pour plus d’informations, consultez la page relative au [**Convertisseur midi**](midi-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="087dd-129">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="087dd-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="087dd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="087dd-131">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="087dd-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



