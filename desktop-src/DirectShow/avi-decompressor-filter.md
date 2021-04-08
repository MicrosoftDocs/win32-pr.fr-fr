---
description: Filtre de décompresseur AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtre de décompresseur AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b6fcff61dd867c598e793fb5aa8fbff67dc6cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746924"
---
# <a name="avi-decompressor-filter"></a><span data-ttu-id="1ad6e-103">Filtre de décompresseur AVI</span><span class="sxs-lookup"><span data-stu-id="1ad6e-103">AVI Decompressor Filter</span></span>

<span data-ttu-id="1ad6e-104">Le filtre de décompresseur AVI permet aux codecs du gestionnaire de compression vidéo (VCM) de joindre un graphique de filtres.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-104">The AVI Decompressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="1ad6e-105">L’application n’a pas besoin d’ajouter le filtre au graphique de filtre ; elle est automatiquement extraite par le gestionnaire de graphique de filtre, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-105">The application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span>

<span data-ttu-id="1ad6e-106">Lorsque le gestionnaire de graphique de filtre crée un graphique pour afficher un fichier AVI, il vérifie le FOURCC dans l’en-tête AVI du fichier pour déterminer si le flux vidéo est compressé.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-106">When the Filter Graph Manager is building a graph to render an AVI file, it checks the FOURCC in the file's AVI header to determine whether the video stream is compressed.</span></span> <span data-ttu-id="1ad6e-107">Si c’est le cas, le gestionnaire de graphique de filtre ajoute le décompresseur AVI, qui recherche ensuite dans le registre un décompresseur installé pouvant gérer le fichier.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-107">If it is, the Filter Graph Manager adds the AVI Decompressor, which then searches the registry for an installed decompressor that can handle the file.</span></span>

> [!Note]  
> <span data-ttu-id="1ad6e-108">Les décompresseurs MPEG ne sont jamais implémentés en tant que codecs VCM, mais uniquement en tant que filtres DirectShow natifs.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-108">MPEG decompressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 

<span data-ttu-id="1ad6e-109">Sur son code PIN amont, le décompresseur AVI se connecte généralement au [séparateur AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="1ad6e-109">On its upstream pin the AVI Decompressor typically connects to the [AVI Splitter](avi-splitter-filter.md).</span></span> <span data-ttu-id="1ad6e-110">Sur sa broche de sortie, il se connecte généralement au [convertisseur vidéo](video-renderer-filter.md) ou au [filtre MUX AVI](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="1ad6e-110">On its output pin it typically connects to the [Video Renderer](video-renderer-filter.md) or the [AVI Mux Filter](avi-mux-filter.md).</span></span>



|                                          |                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad6e-111">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="1ad6e-111">Filter Interfaces</span></span>                        | [<span data-ttu-id="1ad6e-112">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="1ad6e-112">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| <span data-ttu-id="1ad6e-113">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="1ad6e-113">Input Pin Media Types</span></span>                    | <span data-ttu-id="1ad6e-114">Type majeur : MEDIATYPE \_ VideoSubtype : doit correspondre au code FourCC pour le type de compression.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-114">Major type: MEDIATYPE\_VideoSubtype: Must correspond to the FOURCC code for the compression type.</span></span> <span data-ttu-id="1ad6e-115">Pour plus d’informations, consultez [codes FourCC](fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1ad6e-115">For more information, see [FOURCC Codes](fourcc-codes.md).</span></span><br/> <span data-ttu-id="1ad6e-116">Type de format : FORMAT \_ videoinfo</span><span class="sxs-lookup"><span data-stu-id="1ad6e-116">Format type: FORMAT\_VideoInfo</span></span><br/> |
| <span data-ttu-id="1ad6e-117">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="1ad6e-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="1ad6e-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1ad6e-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                             |
| <span data-ttu-id="1ad6e-119">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="1ad6e-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="1ad6e-120">\_Vidéo MediaType, MEDIASUBTYPE \_ null, format \_ videoinfo</span><span class="sxs-lookup"><span data-stu-id="1ad6e-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL, FORMAT\_VideoInfo</span></span>                                                                                                                                                            |
| <span data-ttu-id="1ad6e-121">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="1ad6e-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="1ad6e-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1ad6e-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                 |
| <span data-ttu-id="1ad6e-123">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="1ad6e-123">Filter CLSID</span></span>                             | <span data-ttu-id="1ad6e-124">CLSID \_ AVIDec</span><span class="sxs-lookup"><span data-stu-id="1ad6e-124">CLSID\_AVIDec</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="1ad6e-125">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="1ad6e-125">Property Page CLSID</span></span>                      | <span data-ttu-id="1ad6e-126">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-126">No property page.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="1ad6e-127">Exécutable</span><span class="sxs-lookup"><span data-stu-id="1ad6e-127">Executable</span></span>                               | <span data-ttu-id="1ad6e-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1ad6e-128">quartz.dll</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="1ad6e-129">Mérite</span><span class="sxs-lookup"><span data-stu-id="1ad6e-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="1ad6e-130">MÉRITE \_ normal</span><span class="sxs-lookup"><span data-stu-id="1ad6e-130">MERIT\_NORMAL</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="1ad6e-131">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="1ad6e-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1ad6e-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="1ad6e-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="1ad6e-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ad6e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad6e-134">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="1ad6e-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




