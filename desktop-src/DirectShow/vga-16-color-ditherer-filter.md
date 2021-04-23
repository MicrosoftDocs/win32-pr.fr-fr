---
description: Filtre de couleur VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtre de couleur VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908677"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="5aa17-103">Filtre de couleur VGA 16</span><span class="sxs-lookup"><span data-stu-id="5aa17-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="5aa17-104">Le filtre de couleur VGA 16 est converti à partir d’un type de couleur RVB en un affichage de couleurs de 4 bits, de sorte que les flux vidéo AVI et MPEG peuvent être affichés sur des moniteurs 16 couleurs plus anciens.</span><span class="sxs-lookup"><span data-stu-id="5aa17-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="5aa17-105">Ce filtre est inséré dans le graphique entre un filtre de décompresseur et un filtre de convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="5aa17-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



| <span data-ttu-id="5aa17-106">Étiquette</span><span class="sxs-lookup"><span data-stu-id="5aa17-106">Label</span></span> | <span data-ttu-id="5aa17-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="5aa17-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa17-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="5aa17-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="5aa17-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="5aa17-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="5aa17-110">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="5aa17-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="5aa17-111">\_Vidéo MediaType, MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="5aa17-111">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="5aa17-112">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="5aa17-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="5aa17-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5aa17-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="5aa17-114">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="5aa17-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="5aa17-115">\_Vidéo MediaType, MEDIASUBTYPE \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="5aa17-115">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="5aa17-116">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="5aa17-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="5aa17-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5aa17-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="5aa17-118">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="5aa17-118">Filter CLSID</span></span>                             | <span data-ttu-id="5aa17-119">CLSID \_ tramé</span><span class="sxs-lookup"><span data-stu-id="5aa17-119">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="5aa17-120">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="5aa17-120">Property Page CLSID</span></span>                      | <span data-ttu-id="5aa17-121">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="5aa17-121">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="5aa17-122">Exécutable</span><span class="sxs-lookup"><span data-stu-id="5aa17-122">Executable</span></span>                               | <span data-ttu-id="5aa17-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="5aa17-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="5aa17-124">Mérite</span><span class="sxs-lookup"><span data-stu-id="5aa17-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="5aa17-125">MÉRITE \_ improbable</span><span class="sxs-lookup"><span data-stu-id="5aa17-125">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="5aa17-126">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="5aa17-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="5aa17-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="5aa17-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="5aa17-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5aa17-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aa17-129">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="5aa17-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



