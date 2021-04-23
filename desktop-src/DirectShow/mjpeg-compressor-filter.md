---
description: Filtre de compresseur MJPEG
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtre de compresseur MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02928df4d09b50c0ac152aed99ed87dc6362fb70
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910007"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="0e1ac-103">Filtre de compresseur MJPEG</span><span class="sxs-lookup"><span data-stu-id="0e1ac-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="0e1ac-104">Ce filtre compresse un flux vidéo non compressé à l’aide de la compression Motion JPEG.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



| <span data-ttu-id="0e1ac-105">Étiquette</span><span class="sxs-lookup"><span data-stu-id="0e1ac-105">Label</span></span> | <span data-ttu-id="0e1ac-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e1ac-106">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e1ac-107">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="0e1ac-107">Filter Interfaces</span></span>                        | <span data-ttu-id="0e1ac-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="0e1ac-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="0e1ac-109">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="0e1ac-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="0e1ac-110">\_vidéo MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="0e1ac-110">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="0e1ac-111">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="0e1ac-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="0e1ac-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0e1ac-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="0e1ac-113">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="0e1ac-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="0e1ac-114">\_Vidéo MediaType, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="0e1ac-114">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="0e1ac-115">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="0e1ac-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="0e1ac-116">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0e1ac-116">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="0e1ac-117">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="0e1ac-117">Filter CLSID</span></span>                             | <span data-ttu-id="0e1ac-118">CLSID \_ MJPGEnc</span><span class="sxs-lookup"><span data-stu-id="0e1ac-118">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="0e1ac-119">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="0e1ac-119">Property Page CLSID</span></span>                      | <span data-ttu-id="0e1ac-120">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="0e1ac-120">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="0e1ac-121">Exécutable</span><span class="sxs-lookup"><span data-stu-id="0e1ac-121">Executable</span></span>                               | <span data-ttu-id="0e1ac-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="0e1ac-122">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="0e1ac-123">Mérite</span><span class="sxs-lookup"><span data-stu-id="0e1ac-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="0e1ac-124">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="0e1ac-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="0e1ac-125">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="0e1ac-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0e1ac-126">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="0e1ac-126">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="0e1ac-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="0e1ac-127">Remarks</span></span>

<span data-ttu-id="0e1ac-128">Ce filtre encode à l’aide du sous-type de média MEDIASUBTYPE \_ MJPG, qui correspond au code FourCC « MJPG ».</span><span class="sxs-lookup"><span data-stu-id="0e1ac-128">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e1ac-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e1ac-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e1ac-130">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="0e1ac-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



