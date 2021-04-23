---
description: Filtre de compresseur AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtre de compresseur AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212ab58eb3800e0ad5531ebc5c50d3b054e7866c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909467"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="f6302-103">Filtre de compresseur AVI</span><span class="sxs-lookup"><span data-stu-id="f6302-103">AVI Compressor Filter</span></span>

<span data-ttu-id="f6302-104">Le filtre de compresseur AVI permet aux codecs du gestionnaire de compression vidéo (VCM) de joindre un graphique de filtres.</span><span class="sxs-lookup"><span data-stu-id="f6302-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="f6302-105">Chaque codec apparaît sous la forme d’une instance distincte du filtre.</span><span class="sxs-lookup"><span data-stu-id="f6302-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="f6302-106">Vous ne pouvez pas créer directement ce filtre avec CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="f6302-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="f6302-107">Au lieu de cela, vous devez utiliser l’énumérateur du périphérique système.</span><span class="sxs-lookup"><span data-stu-id="f6302-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="f6302-108">Pour plus d’informations, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="f6302-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="f6302-109">La broche d’entrée du filtre se connecte aux filtres qui génèrent des données vidéo non compressées, telles que les filtres de capture vidéo ou le [filtre de séparateur AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f6302-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="f6302-110">La broche de sortie du filtre se connecte généralement à un filtre MUX, tel que le [filtre multiplex MUX](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f6302-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="f6302-111">Si le codec prend en charge une boîte de dialogue de configuration de VFW de style ancien ou une boîte de dialogue à propos de, une application peut l’afficher à l’aide de l’interface [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .</span><span class="sxs-lookup"><span data-stu-id="f6302-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="f6302-112">Les compresseurs MPEG ne sont jamais implémentés en tant que codecs VCM, mais uniquement en tant que filtres DirectShow natifs.</span><span class="sxs-lookup"><span data-stu-id="f6302-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



| <span data-ttu-id="f6302-113">Étiquette</span><span class="sxs-lookup"><span data-stu-id="f6302-113">Label</span></span> | <span data-ttu-id="f6302-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6302-114">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6302-115">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="f6302-115">Filter Interfaces</span></span>                        | <span data-ttu-id="f6302-116">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="f6302-116">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="f6302-117">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="f6302-117">Input Pin Media Types</span></span>                    | <span data-ttu-id="f6302-118">\_Vidéo MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="f6302-118">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="f6302-119">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="f6302-119">Input Pin Interfaces</span></span>                     | <span data-ttu-id="f6302-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f6302-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="f6302-121">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f6302-121">Output Pin Media Types</span></span>                   | <span data-ttu-id="f6302-122">\_Vidéo MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="f6302-122">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="f6302-123">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f6302-123">Output Pin Interfaces</span></span>                    | <span data-ttu-id="f6302-124">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f6302-124">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="f6302-125">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="f6302-125">Filter CLSID</span></span>                             | <span data-ttu-id="f6302-126">Non applicable</span><span class="sxs-lookup"><span data-stu-id="f6302-126">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="f6302-127">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="f6302-127">Property Page CLSID</span></span>                      | <span data-ttu-id="f6302-128">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f6302-128">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="f6302-129">Exécutable</span><span class="sxs-lookup"><span data-stu-id="f6302-129">Executable</span></span>                               | <span data-ttu-id="f6302-130">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="f6302-130">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="f6302-131">Mérite</span><span class="sxs-lookup"><span data-stu-id="f6302-131">Merit</span></span>](merit.md)                       | <span data-ttu-id="f6302-132">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="f6302-132">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="f6302-133">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="f6302-133">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f6302-134">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="f6302-134">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="f6302-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6302-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6302-136">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="f6302-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



