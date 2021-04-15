---
description: Filtre de décodage vidéo DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Filtre de décodage vidéo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6baab43d4a369cb16d92974a0e6e469c914961bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520463"
---
# <a name="dv-video-decoder-filter"></a><span data-ttu-id="f3de0-103">Filtre de décodage vidéo DV</span><span class="sxs-lookup"><span data-stu-id="f3de0-103">DV Video Decoder Filter</span></span>

<span data-ttu-id="f3de0-104">Ce filtre décode un flux vidéo numérique (DV) en vidéo non compressée.</span><span class="sxs-lookup"><span data-stu-id="f3de0-104">This filter decodes a digital video (DV) stream into uncompressed video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3de0-105">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="f3de0-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="f3de0-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="f3de0-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3de0-107">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="f3de0-107">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="f3de0-108">MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="f3de0-108">MEDIATYPE_Video</span></span></li>
<li><span data-ttu-id="f3de0-109">MEDIASUBTYPE_dvsd</span><span class="sxs-lookup"><span data-stu-id="f3de0-109">MEDIASUBTYPE_dvsd</span></span></li>
<li><span data-ttu-id="f3de0-110">FORMAT_VideoInfo, FORMAT_DvInfo</span><span class="sxs-lookup"><span data-stu-id="f3de0-110">FORMAT_VideoInfo, FORMAT_DvInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3de0-111">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="f3de0-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="f3de0-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3de0-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3de0-113">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f3de0-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="f3de0-114"><strong>Type principal</strong>: MEDIATYPE_Video<strong>sous-types</strong>:</span><span class="sxs-lookup"><span data-stu-id="f3de0-114"><strong>Major type</strong>: MEDIATYPE_Video<strong>Subtypes</strong>:</span></span><br/>
<ul>
<li><span data-ttu-id="f3de0-115">MEDIASUBTYPE_YUY2</span><span class="sxs-lookup"><span data-stu-id="f3de0-115">MEDIASUBTYPE_YUY2</span></span></li>
<li><span data-ttu-id="f3de0-116">MEDIASUBTYPE_UYVY</span><span class="sxs-lookup"><span data-stu-id="f3de0-116">MEDIASUBTYPE_UYVY</span></span></li>
<li><span data-ttu-id="f3de0-117">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="f3de0-117">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="f3de0-118">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="f3de0-118">MEDIASUBTYPE_RGB32</span></span></li>
<li><span data-ttu-id="f3de0-119">MEDIASUBTYPE_ARGB32</span><span class="sxs-lookup"><span data-stu-id="f3de0-119">MEDIASUBTYPE_ARGB32</span></span></li>
<li><span data-ttu-id="f3de0-120">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="f3de0-120">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="f3de0-121">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="f3de0-121">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="f3de0-122">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="f3de0-122">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="f3de0-123">MEDIASUBTYPE_Y41P</span><span class="sxs-lookup"><span data-stu-id="f3de0-123">MEDIASUBTYPE_Y41P</span></span></li>
</ul><span data-ttu-id="f3de0-124">
<strong>Types de format</strong>:</span><span class="sxs-lookup"><span data-stu-id="f3de0-124">
<strong>Format types</strong>:</span></span><br/> <span data-ttu-id="f3de0-125">Format_VideoInfo, Format_VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="f3de0-125">Format_VideoInfo, Format_VideoInfo2</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3de0-126">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="f3de0-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="f3de0-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3de0-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3de0-128">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="f3de0-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="f3de0-129">CLSID_DVVideoCodec</span><span class="sxs-lookup"><span data-stu-id="f3de0-129">CLSID_DVVideoCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3de0-130">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="f3de0-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="f3de0-131">CLSID_DVDecPropertiesPage</span><span class="sxs-lookup"><span data-stu-id="f3de0-131">CLSID_DVDecPropertiesPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3de0-132">Exécutable</span><span class="sxs-lookup"><span data-stu-id="f3de0-132">Executable</span></span></td>
<td><span data-ttu-id="f3de0-133">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="f3de0-133">qdv.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3de0-134"><a href="merit.md">Mérite</a></span><span class="sxs-lookup"><span data-stu-id="f3de0-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="f3de0-135">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="f3de0-135">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3de0-136"><a href="filter-categories.md">Catégorie de filtre</a></span><span class="sxs-lookup"><span data-stu-id="f3de0-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="f3de0-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="f3de0-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f3de0-138">Notes</span><span class="sxs-lookup"><span data-stu-id="f3de0-138">Remarks</span></span>

<span data-ttu-id="f3de0-139">Utilisez l’interface [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) pour définir la résolution du décodage sur complète, demi-taille, quart de taille ou une taille d’un huitième.</span><span class="sxs-lookup"><span data-stu-id="f3de0-139">Use the [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) interface to set the decoding resolution to full, half size, quarter size, or one-eighth size.</span></span>

<span data-ttu-id="f3de0-140">**Entrelacement**: les versions antérieures du décodeur désentrelacent toujours la vidéo.</span><span class="sxs-lookup"><span data-stu-id="f3de0-140">**Interlacing**: Earlier versions of the decoder always deinterlace the video.</span></span> <span data-ttu-id="f3de0-141">À partir de DirectX 9,0, le décodeur vidéo DV peut préserver l’entrelacement.</span><span class="sxs-lookup"><span data-stu-id="f3de0-141">As of DirectX 9.0, the DV Video Decoder can preserve the interlacing.</span></span> <span data-ttu-id="f3de0-142">Cela permet à la vidéo entrelacée d’être désentrelacée par le convertisseur de mixage vidéo (VMR), afin d’améliorer la qualité de rendu.</span><span class="sxs-lookup"><span data-stu-id="f3de0-142">This enables the interlaced video to be deinterlaced by the Video Mixing Renderer (VMR), for improved rendering quality.</span></span> <span data-ttu-id="f3de0-143">Pour utiliser cette fonctionnalité, le filtre en aval doit prendre en charge les formats [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , indiqués par ce format \_ de valeur VideoInfo2 dans le membre **formatType** de la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="f3de0-143">To use this feature, the downstream filter must support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, indicated by that value Format\_VideoInfo2 in the **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="f3de0-144">Au niveau de la résolution complète, les indicateurs de désentrelacement (**dwInterlace**) dans la structure **VIDEOINFOHEADER2** sont définis sur `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` , indiquant les champs entrelacés.</span><span class="sxs-lookup"><span data-stu-id="f3de0-144">At full resolution output, the deinterlacing flags (**dwInterlace**) in the **VIDEOINFOHEADER2** structure are set to `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave`, indicating interlaced fields.</span></span> <span data-ttu-id="f3de0-145">À demi-résolution ou moins, **dwInterlace** est défini à zéro, ce qui indique les images progressives.</span><span class="sxs-lookup"><span data-stu-id="f3de0-145">At half resolution or lower, **dwInterlace** is set to zero, indicating progressive frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3de0-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3de0-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3de0-147">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="f3de0-147">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="f3de0-148">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="f3de0-148">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




