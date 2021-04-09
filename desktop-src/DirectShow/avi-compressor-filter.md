---
description: Filtre de compresseur AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtre de compresseur AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ef342d1ea740503d9fc1e9e9b898aadc3801
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845718"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="ee205-103">Filtre de compresseur AVI</span><span class="sxs-lookup"><span data-stu-id="ee205-103">AVI Compressor Filter</span></span>

<span data-ttu-id="ee205-104">Le filtre de compresseur AVI permet aux codecs du gestionnaire de compression vidéo (VCM) de joindre un graphique de filtres.</span><span class="sxs-lookup"><span data-stu-id="ee205-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="ee205-105">Chaque codec apparaît sous la forme d’une instance distincte du filtre.</span><span class="sxs-lookup"><span data-stu-id="ee205-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="ee205-106">Vous ne pouvez pas créer directement ce filtre avec CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="ee205-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="ee205-107">Au lieu de cela, vous devez utiliser l’énumérateur du périphérique système.</span><span class="sxs-lookup"><span data-stu-id="ee205-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="ee205-108">Pour plus d’informations, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="ee205-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="ee205-109">La broche d’entrée du filtre se connecte aux filtres qui génèrent des données vidéo non compressées, telles que les filtres de capture vidéo ou le [filtre de séparateur AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ee205-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="ee205-110">La broche de sortie du filtre se connecte généralement à un filtre MUX, tel que le [filtre multiplex MUX](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ee205-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="ee205-111">Si le codec prend en charge une boîte de dialogue de configuration de VFW de style ancien ou une boîte de dialogue à propos de, une application peut l’afficher à l’aide de l’interface [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .</span><span class="sxs-lookup"><span data-stu-id="ee205-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="ee205-112">Les compresseurs MPEG ne sont jamais implémentés en tant que codecs VCM, mais uniquement en tant que filtres DirectShow natifs.</span><span class="sxs-lookup"><span data-stu-id="ee205-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee205-113">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="ee205-113">Filter Interfaces</span></span>                        | <span data-ttu-id="ee205-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="ee205-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="ee205-115">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="ee205-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="ee205-116">\_Vidéo MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="ee205-116">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="ee205-117">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="ee205-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="ee205-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="ee205-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="ee205-119">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="ee205-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="ee205-120">\_Vidéo MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="ee205-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="ee205-121">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="ee205-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="ee205-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="ee205-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="ee205-123">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="ee205-123">Filter CLSID</span></span>                             | <span data-ttu-id="ee205-124">Non applicable</span><span class="sxs-lookup"><span data-stu-id="ee205-124">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="ee205-125">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="ee205-125">Property Page CLSID</span></span>                      | <span data-ttu-id="ee205-126">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ee205-126">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="ee205-127">Exécutable</span><span class="sxs-lookup"><span data-stu-id="ee205-127">Executable</span></span>                               | <span data-ttu-id="ee205-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="ee205-128">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="ee205-129">Mérite</span><span class="sxs-lookup"><span data-stu-id="ee205-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="ee205-130">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="ee205-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="ee205-131">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="ee205-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ee205-132">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="ee205-132">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="ee205-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee205-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee205-134">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="ee205-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



