---
description: Filtre de décodage vidéo MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Filtre de décodage vidéo MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7f48e441226dee33ef949219e8008e15c9d711
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514306"
---
# <a name="mpeg-1-video-decoder-filter"></a><span data-ttu-id="e5515-103">Filtre de décodage vidéo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="e5515-103">MPEG-1 Video Decoder Filter</span></span>

<span data-ttu-id="e5515-104">Décode une vidéo MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="e5515-104">Decodes MPEG-1 video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5515-105">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="e5515-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="e5515-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5515-107">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="e5515-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="e5515-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="e5515-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span></span><br/> <span data-ttu-id="e5515-109">Les sous-types suivants sont valides :</span><span class="sxs-lookup"><span data-stu-id="e5515-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="e5515-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span></span></li>
<li><span data-ttu-id="e5515-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5515-112">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="e5515-112">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="e5515-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"> <strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5515-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5515-114">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="e5515-114">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="e5515-115">Type majeur : <strong>MEDIATYPE_Video</strong>,</span><span class="sxs-lookup"><span data-stu-id="e5515-115">Major type: <strong>MEDIATYPE_Video</strong>,</span></span><br/> <span data-ttu-id="e5515-116">Type de format : <strong>FORMAT_VideoInfo</strong> ou <strong>FORMAT_VideoInfo2</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-116">Format type: <strong>FORMAT_VideoInfo</strong> or <strong>FORMAT_VideoInfo2</strong></span></span><br/> <span data-ttu-id="e5515-117">Sous-types</span><span class="sxs-lookup"><span data-stu-id="e5515-117">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="e5515-118"><strong>MEDIASUBTYPE_RGB24</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-118"><strong>MEDIASUBTYPE_RGB24</strong></span></span></li>
<li><span data-ttu-id="e5515-119"><strong>MEDIASUBTYPE_RGB32</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-119"><strong>MEDIASUBTYPE_RGB32</strong></span></span></li>
<li><span data-ttu-id="e5515-120"><strong>MEDIASUBTYPE_RGB8</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-120"><strong>MEDIASUBTYPE_RGB8</strong></span></span></li>
<li><span data-ttu-id="e5515-121"><strong>MEDIASUBTYPE_RGB555</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-121"><strong>MEDIASUBTYPE_RGB555</strong></span></span></li>
<li><span data-ttu-id="e5515-122"><strong>MEDIASUBTYPE_RGB565</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-122"><strong>MEDIASUBTYPE_RGB565</strong></span></span></li>
<li><span data-ttu-id="e5515-123"><strong>MEDIASUBTYPE_UYVY</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-123"><strong>MEDIASUBTYPE_UYVY</strong></span></span></li>
<li><span data-ttu-id="e5515-124"><strong>MEDIASUBTYPE_Y41P</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-124"><strong>MEDIASUBTYPE_Y41P</strong></span></span></li>
<li><span data-ttu-id="e5515-125"><strong>MEDIASUBTYPE_YUY2</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-125"><strong>MEDIASUBTYPE_YUY2</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5515-126">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="e5515-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="e5515-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5515-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5515-128">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="e5515-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="e5515-129"><strong>CLSID_CMpegVideoCodec</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-129"><strong>CLSID_CMpegVideoCodec</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5515-130">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="e5515-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="e5515-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span><span class="sxs-lookup"><span data-stu-id="e5515-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5515-132">Exécutable</span><span class="sxs-lookup"><span data-stu-id="e5515-132">Executable</span></span></td>
<td><span data-ttu-id="e5515-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="e5515-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5515-134"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="e5515-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="e5515-135">0x40000001</span><span class="sxs-lookup"><span data-stu-id="e5515-135">0x40000001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5515-136"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="e5515-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="e5515-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="e5515-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="e5515-138">Notes</span><span class="sxs-lookup"><span data-stu-id="e5515-138">Remarks</span></span>

<span data-ttu-id="e5515-139">Ce filtre peut décoder dans une surface DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="e5515-139">This filter can decode into a DirectDraw Surface.</span></span> <span data-ttu-id="e5515-140">Le filtre utilise MMX si l’ordinateur prend en charge MMX.</span><span class="sxs-lookup"><span data-stu-id="e5515-140">The filter uses MMX if the machine supports MMX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5515-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5515-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5515-142">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="e5515-142">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




