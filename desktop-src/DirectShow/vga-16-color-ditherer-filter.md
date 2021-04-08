---
description: Filtre de couleur VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtre de couleur VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034807"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="67dc9-103">Filtre de couleur VGA 16</span><span class="sxs-lookup"><span data-stu-id="67dc9-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="67dc9-104">Le filtre de couleur VGA 16 est converti à partir d’un type de couleur RVB en un affichage de couleurs de 4 bits, de sorte que les flux vidéo AVI et MPEG peuvent être affichés sur des moniteurs 16 couleurs plus anciens.</span><span class="sxs-lookup"><span data-stu-id="67dc9-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="67dc9-105">Ce filtre est inséré dans le graphique entre un filtre de décompresseur et un filtre de convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="67dc9-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67dc9-106">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="67dc9-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="67dc9-107">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="67dc9-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="67dc9-108">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="67dc9-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="67dc9-109">\_Vidéo MediaType, MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="67dc9-109">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="67dc9-110">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="67dc9-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="67dc9-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="67dc9-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="67dc9-112">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="67dc9-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="67dc9-113">\_Vidéo MediaType, MEDIASUBTYPE \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="67dc9-113">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="67dc9-114">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="67dc9-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="67dc9-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="67dc9-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="67dc9-116">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="67dc9-116">Filter CLSID</span></span>                             | <span data-ttu-id="67dc9-117">CLSID \_ tramé</span><span class="sxs-lookup"><span data-stu-id="67dc9-117">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="67dc9-118">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="67dc9-118">Property Page CLSID</span></span>                      | <span data-ttu-id="67dc9-119">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="67dc9-119">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="67dc9-120">Exécutable</span><span class="sxs-lookup"><span data-stu-id="67dc9-120">Executable</span></span>                               | <span data-ttu-id="67dc9-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="67dc9-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="67dc9-122">Mérite</span><span class="sxs-lookup"><span data-stu-id="67dc9-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="67dc9-123">MÉRITE \_ improbable</span><span class="sxs-lookup"><span data-stu-id="67dc9-123">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="67dc9-124">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="67dc9-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="67dc9-125">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="67dc9-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="67dc9-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67dc9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67dc9-127">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="67dc9-127">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



