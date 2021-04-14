---
description: Filtre tee de code confidentiel infini
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtre tee de code confidentiel infini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a80baf047cdd5559fadaa0f13ea1352d4ed0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392739"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="92d81-103">Filtre tee de code confidentiel infini</span><span class="sxs-lookup"><span data-stu-id="92d81-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="92d81-104">Ce filtre remet les exemples livrés à sa broche d’entrée à un nombre variable de broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="92d81-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="92d81-105">Lorsqu’une instance du filtre est créée, elle possède une broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="92d81-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="92d81-106">Chaque fois qu’une broche de sortie est connectée, le filtre crée une autre broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="92d81-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="92d81-107">Toutes les broches de sortie partagent le même type de support que la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="92d81-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="92d81-108">Une version de ce filtre est également fournie en tant qu’exemple de kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="92d81-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="92d81-109">Consultez [exemple de filtre InfTee](inftee-filter-sample.md).</span><span class="sxs-lookup"><span data-stu-id="92d81-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d81-110">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="92d81-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="92d81-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="92d81-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="92d81-112">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="92d81-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="92d81-113">Tout type de média</span><span class="sxs-lookup"><span data-stu-id="92d81-113">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="92d81-114">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="92d81-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="92d81-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="92d81-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="92d81-116">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="92d81-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="92d81-117">Tout type de média.</span><span class="sxs-lookup"><span data-stu-id="92d81-117">Any media type.</span></span> <span data-ttu-id="92d81-118">Le type de sortie correspond toujours au type d’entrée, pour toutes les broches de sortie</span><span class="sxs-lookup"><span data-stu-id="92d81-118">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="92d81-119">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="92d81-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="92d81-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="92d81-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="92d81-121">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="92d81-121">Filter CLSID</span></span>                             | <span data-ttu-id="92d81-122">CLSID \_ InfTee</span><span class="sxs-lookup"><span data-stu-id="92d81-122">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="92d81-123">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="92d81-123">Property Page CLSID</span></span>                      | <span data-ttu-id="92d81-124">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="92d81-124">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="92d81-125">Exécutable</span><span class="sxs-lookup"><span data-stu-id="92d81-125">Executable</span></span>                               | <span data-ttu-id="92d81-126">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="92d81-126">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="92d81-127">Mérite</span><span class="sxs-lookup"><span data-stu-id="92d81-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="92d81-128">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="92d81-128">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="92d81-129">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="92d81-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="92d81-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="92d81-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="92d81-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92d81-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92d81-132">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="92d81-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



