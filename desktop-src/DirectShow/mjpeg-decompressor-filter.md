---
description: Filtre de décompresseur MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtre de décompresseur MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522455"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="20fc6-103">Filtre de décompresseur MJPEG</span><span class="sxs-lookup"><span data-stu-id="20fc6-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="20fc6-104">Ce filtre décode un flux vidéo de Motion JPEG en vidéo non compressée.</span><span class="sxs-lookup"><span data-stu-id="20fc6-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="20fc6-105">Certaines caméras vidéo numériques produisent un flux vidéo JPEG motion.</span><span class="sxs-lookup"><span data-stu-id="20fc6-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fc6-106">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="20fc6-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="20fc6-107">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="20fc6-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="20fc6-108">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="20fc6-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="20fc6-109">\_Vidéo MediaType, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="20fc6-109">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="20fc6-110">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="20fc6-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="20fc6-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="20fc6-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="20fc6-112">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="20fc6-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="20fc6-113">\_vidéo MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="20fc6-113">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="20fc6-114">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="20fc6-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="20fc6-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="20fc6-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="20fc6-116">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="20fc6-116">Filter CLSID</span></span>                             | <span data-ttu-id="20fc6-117">CLSID \_ MjpegDec</span><span class="sxs-lookup"><span data-stu-id="20fc6-117">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="20fc6-118">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="20fc6-118">Property Page CLSID</span></span>                      | <span data-ttu-id="20fc6-119">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="20fc6-119">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="20fc6-120">Exécutable</span><span class="sxs-lookup"><span data-stu-id="20fc6-120">Executable</span></span>                               | <span data-ttu-id="20fc6-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="20fc6-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="20fc6-122">Mérite</span><span class="sxs-lookup"><span data-stu-id="20fc6-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="20fc6-123">MÉRITE \_ normal</span><span class="sxs-lookup"><span data-stu-id="20fc6-123">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="20fc6-124">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="20fc6-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="20fc6-125">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="20fc6-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="20fc6-126">Notes</span><span class="sxs-lookup"><span data-stu-id="20fc6-126">Remarks</span></span>

<span data-ttu-id="20fc6-127">Ce filtre est compatible avec Motion JPEG Video qui utilise le code FOURCC « MJPG ».</span><span class="sxs-lookup"><span data-stu-id="20fc6-127">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="20fc6-128">Il ne peut pas décoder d’autres types de mouvement JPEG.</span><span class="sxs-lookup"><span data-stu-id="20fc6-128">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="20fc6-129">Pour cela, vous devez utiliser un filtre de décodeur tiers.</span><span class="sxs-lookup"><span data-stu-id="20fc6-129">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20fc6-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20fc6-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20fc6-131">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="20fc6-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



