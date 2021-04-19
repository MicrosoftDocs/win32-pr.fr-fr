---
description: Filtre de compresseur MJPEG
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtre de compresseur MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517162"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="cb105-103">Filtre de compresseur MJPEG</span><span class="sxs-lookup"><span data-stu-id="cb105-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="cb105-104">Ce filtre compresse un flux vidéo non compressé à l’aide de la compression Motion JPEG.</span><span class="sxs-lookup"><span data-stu-id="cb105-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb105-105">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="cb105-105">Filter Interfaces</span></span>                        | <span data-ttu-id="cb105-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="cb105-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="cb105-107">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="cb105-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="cb105-108">\_vidéo MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="cb105-108">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="cb105-109">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="cb105-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="cb105-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="cb105-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="cb105-111">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="cb105-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="cb105-112">\_Vidéo MediaType, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="cb105-112">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="cb105-113">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="cb105-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="cb105-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="cb105-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="cb105-115">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="cb105-115">Filter CLSID</span></span>                             | <span data-ttu-id="cb105-116">CLSID \_ MJPGEnc</span><span class="sxs-lookup"><span data-stu-id="cb105-116">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="cb105-117">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="cb105-117">Property Page CLSID</span></span>                      | <span data-ttu-id="cb105-118">Aucune page de propriétés</span><span class="sxs-lookup"><span data-stu-id="cb105-118">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="cb105-119">Exécutable</span><span class="sxs-lookup"><span data-stu-id="cb105-119">Executable</span></span>                               | <span data-ttu-id="cb105-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="cb105-120">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="cb105-121">Mérite</span><span class="sxs-lookup"><span data-stu-id="cb105-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="cb105-122">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="cb105-122">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="cb105-123">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="cb105-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="cb105-124">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="cb105-124">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="cb105-125">Notes</span><span class="sxs-lookup"><span data-stu-id="cb105-125">Remarks</span></span>

<span data-ttu-id="cb105-126">Ce filtre encode à l’aide du sous-type de média MEDIASUBTYPE \_ MJPG, qui correspond au code FourCC « MJPG ».</span><span class="sxs-lookup"><span data-stu-id="cb105-126">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb105-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb105-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb105-128">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="cb105-128">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



