---
description: Filtre de décompresseur MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtre de décompresseur MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910017"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="6b0b7-103">Filtre de décompresseur MJPEG</span><span class="sxs-lookup"><span data-stu-id="6b0b7-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="6b0b7-104">Ce filtre décode un flux vidéo de Motion JPEG en vidéo non compressée.</span><span class="sxs-lookup"><span data-stu-id="6b0b7-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="6b0b7-105">Certaines caméras vidéo numériques produisent un flux vidéo JPEG motion.</span><span class="sxs-lookup"><span data-stu-id="6b0b7-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



| <span data-ttu-id="6b0b7-106">Étiquette</span><span class="sxs-lookup"><span data-stu-id="6b0b7-106">Label</span></span> | <span data-ttu-id="6b0b7-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b0b7-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0b7-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="6b0b7-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="6b0b7-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="6b0b7-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="6b0b7-110">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="6b0b7-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="6b0b7-111">\_Vidéo MediaType, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="6b0b7-111">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="6b0b7-112">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="6b0b7-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="6b0b7-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="6b0b7-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="6b0b7-114">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="6b0b7-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="6b0b7-115">\_vidéo MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="6b0b7-115">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="6b0b7-116">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="6b0b7-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="6b0b7-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="6b0b7-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="6b0b7-118">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="6b0b7-118">Filter CLSID</span></span>                             | <span data-ttu-id="6b0b7-119">CLSID \_ MjpegDec</span><span class="sxs-lookup"><span data-stu-id="6b0b7-119">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="6b0b7-120">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="6b0b7-120">Property Page CLSID</span></span>                      | <span data-ttu-id="6b0b7-121">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="6b0b7-121">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="6b0b7-122">Exécutable</span><span class="sxs-lookup"><span data-stu-id="6b0b7-122">Executable</span></span>                               | <span data-ttu-id="6b0b7-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="6b0b7-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="6b0b7-124">Mérite</span><span class="sxs-lookup"><span data-stu-id="6b0b7-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="6b0b7-125">MÉRITE \_ normal</span><span class="sxs-lookup"><span data-stu-id="6b0b7-125">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="6b0b7-126">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="6b0b7-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="6b0b7-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="6b0b7-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="6b0b7-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="6b0b7-128">Remarks</span></span>

<span data-ttu-id="6b0b7-129">Ce filtre est compatible avec Motion JPEG Video qui utilise le code FOURCC « MJPG ».</span><span class="sxs-lookup"><span data-stu-id="6b0b7-129">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="6b0b7-130">Il ne peut pas décoder d’autres types de mouvement JPEG.</span><span class="sxs-lookup"><span data-stu-id="6b0b7-130">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="6b0b7-131">Pour cela, vous devez utiliser un filtre de décodeur tiers.</span><span class="sxs-lookup"><span data-stu-id="6b0b7-131">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b0b7-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b0b7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b0b7-133">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="6b0b7-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



