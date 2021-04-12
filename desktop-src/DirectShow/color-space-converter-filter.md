---
description: Filtre de convertisseur d’espace colorimétrique
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Filtre de convertisseur d’espace colorimétrique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f054ee03dd65cf619a697d4441b4d09279e7b912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481184"
---
# <a name="color-space-converter-filter"></a><span data-ttu-id="f038b-103">Filtre de convertisseur d’espace colorimétrique</span><span class="sxs-lookup"><span data-stu-id="f038b-103">Color Space Converter Filter</span></span>

<span data-ttu-id="f038b-104">Ce filtre de transformation convertit d’un type de couleur RVB en un autre type RVB, par exemple entre une couleur RVB de 24 et 8 bits.</span><span class="sxs-lookup"><span data-stu-id="f038b-104">This transform filter converts from one RGB color type to another RGB type, such as between 24-bit and 8-bit RGB color.</span></span> <span data-ttu-id="f038b-105">Étant donné que ce type de conversion est généralement géré plus efficacement au sein d’un décompresseur vidéo, l’utilisation principale du convertisseur d’espace colorimétrique est lorsque la source de flux est composée de trames RVB non compressées.</span><span class="sxs-lookup"><span data-stu-id="f038b-105">Since this type of conversion is generally handled more efficiently within a video decompressor, the main use of the Color Space Converter is when the stream source consists of uncompressed RGB frames.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f038b-106">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="f038b-106">Filter Interfaces</span></span></td>
<td><span data-ttu-id="f038b-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="f038b-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f038b-108">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="f038b-108">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="f038b-109">MEDIATYPE_Video, FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="f038b-109">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="f038b-110">Les sous-types suivants sont valides :</span><span class="sxs-lookup"><span data-stu-id="f038b-110">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="f038b-111">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="f038b-111">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="f038b-112">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="f038b-112">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="f038b-113">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="f038b-113">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="f038b-114">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="f038b-114">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="f038b-115">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="f038b-115">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f038b-116">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="f038b-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="f038b-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f038b-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f038b-118">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f038b-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="f038b-119">MEDIATYPE_Video, FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="f038b-119">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="f038b-120">Les sous-types suivants sont valides :</span><span class="sxs-lookup"><span data-stu-id="f038b-120">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="f038b-121">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="f038b-121">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="f038b-122">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="f038b-122">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="f038b-123">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="f038b-123">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="f038b-124">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="f038b-124">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="f038b-125">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="f038b-125">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f038b-126">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f038b-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="f038b-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f038b-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f038b-128">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="f038b-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="f038b-129">CLSID_Colour</span><span class="sxs-lookup"><span data-stu-id="f038b-129">CLSID_Colour</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f038b-130">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="f038b-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="f038b-131">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f038b-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f038b-132">Exécutable</span><span class="sxs-lookup"><span data-stu-id="f038b-132">Executable</span></span></td>
<td><span data-ttu-id="f038b-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="f038b-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f038b-134"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="f038b-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="f038b-135">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="f038b-135">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f038b-136"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="f038b-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="f038b-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="f038b-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f038b-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f038b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f038b-139">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="f038b-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




