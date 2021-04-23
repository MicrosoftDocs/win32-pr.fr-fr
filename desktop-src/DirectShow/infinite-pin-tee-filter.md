---
description: Filtre tee de code confidentiel infini
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtre tee de code confidentiel infini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3433a0c2f5fe55fa59c42ed6e02d34f6e2cf0e6d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909227"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="ab4e2-103">Filtre tee de code confidentiel infini</span><span class="sxs-lookup"><span data-stu-id="ab4e2-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="ab4e2-104">Ce filtre remet les exemples livrés à sa broche d’entrée à un nombre variable de broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="ab4e2-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="ab4e2-105">Lorsqu’une instance du filtre est créée, elle possède une broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="ab4e2-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="ab4e2-106">Chaque fois qu’une broche de sortie est connectée, le filtre crée une autre broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="ab4e2-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="ab4e2-107">Toutes les broches de sortie partagent le même type de support que la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ab4e2-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="ab4e2-108">Une version de ce filtre est également fournie en tant qu’exemple de kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="ab4e2-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="ab4e2-109">Consultez [exemple de filtre InfTee](inftee-filter-sample.md).</span><span class="sxs-lookup"><span data-stu-id="ab4e2-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



| <span data-ttu-id="ab4e2-110">Étiquette</span><span class="sxs-lookup"><span data-stu-id="ab4e2-110">Label</span></span> | <span data-ttu-id="ab4e2-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab4e2-111">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab4e2-112">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="ab4e2-112">Filter Interfaces</span></span>                        | [<span data-ttu-id="ab4e2-113">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="ab4e2-113">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="ab4e2-114">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="ab4e2-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="ab4e2-115">Tout type de média</span><span class="sxs-lookup"><span data-stu-id="ab4e2-115">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="ab4e2-116">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="ab4e2-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="ab4e2-117">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="ab4e2-117">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="ab4e2-118">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="ab4e2-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="ab4e2-119">Tout type de média.</span><span class="sxs-lookup"><span data-stu-id="ab4e2-119">Any media type.</span></span> <span data-ttu-id="ab4e2-120">Le type de sortie correspond toujours au type d’entrée, pour toutes les broches de sortie</span><span class="sxs-lookup"><span data-stu-id="ab4e2-120">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="ab4e2-121">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="ab4e2-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="ab4e2-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="ab4e2-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="ab4e2-123">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="ab4e2-123">Filter CLSID</span></span>                             | <span data-ttu-id="ab4e2-124">CLSID \_ InfTee</span><span class="sxs-lookup"><span data-stu-id="ab4e2-124">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="ab4e2-125">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="ab4e2-125">Property Page CLSID</span></span>                      | <span data-ttu-id="ab4e2-126">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="ab4e2-126">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="ab4e2-127">Exécutable</span><span class="sxs-lookup"><span data-stu-id="ab4e2-127">Executable</span></span>                               | <span data-ttu-id="ab4e2-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="ab4e2-128">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="ab4e2-129">Mérite</span><span class="sxs-lookup"><span data-stu-id="ab4e2-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="ab4e2-130">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="ab4e2-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="ab4e2-131">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="ab4e2-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ab4e2-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="ab4e2-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="ab4e2-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ab4e2-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab4e2-134">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="ab4e2-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



