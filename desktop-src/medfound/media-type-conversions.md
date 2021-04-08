---
description: Conversions de type de média
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Conversions de type de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3a72e74439251f9661e0ff27166c504e47c238
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761467"
---
# <a name="media-type-conversions"></a><span data-ttu-id="a7315-103">Conversions de type de média</span><span class="sxs-lookup"><span data-stu-id="a7315-103">Media Type Conversions</span></span>

<span data-ttu-id="a7315-104">Il est parfois nécessaire de convertir les types de média Media Foundation et les anciennes structures de type de média à partir de DirectShow ou du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="a7315-104">Occasionally it is necessary to convert between Media Foundation media types and the older media type structures from DirectShow or the Windows Media Format SDK.</span></span>

### <a name="from-a-format-structure-to-a-media-foundation-type"></a><span data-ttu-id="a7315-105">D’une structure de format à un type de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a7315-105">From a Format Structure to a Media Foundation Type</span></span>

<span data-ttu-id="a7315-106">Les fonctions suivantes initialisent un type de média Media Foundation à partir d’une structure de format.</span><span class="sxs-lookup"><span data-stu-id="a7315-106">The following functions initialize a Media Foundation media type from a format structure.</span></span> <span data-ttu-id="a7315-107">Ces fonctions sont également utiles si un flux de données ou un en-tête de fichier contient une structure de format.</span><span class="sxs-lookup"><span data-stu-id="a7315-107">These functions are also useful if a data stream or a file header contains a format structure.</span></span> <span data-ttu-id="a7315-108">Par exemple, l’en-tête de fichier pour les fichiers audio WAVE contient une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a7315-108">For example, the file header for WAVE audio files contains a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7315-109">Structure à convertir</span><span class="sxs-lookup"><span data-stu-id="a7315-109">Structure to Convert</span></span></th>
<th><span data-ttu-id="a7315-110">Fonction</span><span class="sxs-lookup"><span data-stu-id="a7315-110">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7315-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="a7315-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)</span></span><br/> <span data-ttu-id="a7315-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (objets multimédia DirectX)</span><span class="sxs-lookup"><span data-stu-id="a7315-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (DirectX Media Objects)</span></span> <br/> <span data-ttu-id="a7315-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (kit de développement logiciel (SDK) Windows Media Format)</span><span class="sxs-lookup"><span data-stu-id="a7315-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows Media Format SDK)</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a7315-114">Ces structures sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="a7315-114">These structures are equivalent.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="a7315-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7315-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="a7315-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7315-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="a7315-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7315-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="a7315-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7315-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="a7315-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7315-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span></span></td>
<td><span data-ttu-id="a7315-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7315-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="a7315-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7315-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> ou <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> or <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"><strong>WAVEFORMATEXTENSIBLE</strong></a></span></span></td>
<td><span data-ttu-id="a7315-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="a7315-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a><span data-ttu-id="a7315-130">D’un type de Media Foundation à une structure de format</span><span class="sxs-lookup"><span data-stu-id="a7315-130">From a Media Foundation Type to a Format Structure</span></span>

<span data-ttu-id="a7315-131">Les fonctions suivantes permettent de créer ou d’initialiser une structure de format à partir d’un type de média Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a7315-131">The following functions create or initialize a format structure from a Media Foundation media type.</span></span>



| <span data-ttu-id="a7315-132">Fonction</span><span class="sxs-lookup"><span data-stu-id="a7315-132">Function</span></span>                                                                             | <span data-ttu-id="a7315-133">Structure cible</span><span class="sxs-lookup"><span data-stu-id="a7315-133">Target Structure</span></span>                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7315-134">**IMFMediaType::GetRepresentation**</span><span class="sxs-lookup"><span data-stu-id="a7315-134">**IMFMediaType::GetRepresentation**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | <span data-ttu-id="a7315-135">[**Am \_ \_Type de média**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span><span class="sxs-lookup"><span data-stu-id="a7315-135">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span></span> |
| [<span data-ttu-id="a7315-136">**MFCreateAMMediaTypeFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a7315-136">**MFCreateAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [<span data-ttu-id="a7315-137">**\_type de média am \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-137">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [<span data-ttu-id="a7315-138">**MFCreateMFVideoFormatFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a7315-138">**MFCreateMFVideoFormatFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [<span data-ttu-id="a7315-139">**MFVIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="a7315-139">**MFVIDEOFORMAT**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [<span data-ttu-id="a7315-140">**MFCreateWaveFormatExFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a7315-140">**MFCreateWaveFormatExFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | <span data-ttu-id="a7315-141">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ou [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a7315-141">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span></span>                                                                                    |
| [<span data-ttu-id="a7315-142">**MFInitAMMediaTypeFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a7315-142">**MFInitAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [<span data-ttu-id="a7315-143">**\_type de média am \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-143">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a><span data-ttu-id="a7315-144">Mappages de format</span><span class="sxs-lookup"><span data-stu-id="a7315-144">Format Mappings</span></span>

<span data-ttu-id="a7315-145">Les tableaux suivants répertorient les attributs de Media Foundation qui correspondent à différentes structures de format.</span><span class="sxs-lookup"><span data-stu-id="a7315-145">The following tables list the Media Foundation attributes that correspond to various format structures.</span></span> <span data-ttu-id="a7315-146">Tous ces attributs ne peuvent pas être traduits directement.</span><span class="sxs-lookup"><span data-stu-id="a7315-146">Not all of these attributes can be translated directly.</span></span> <span data-ttu-id="a7315-147">Pour effectuer des conversions, vous devez utiliser les fonctions listées dans la section précédente. ces tables sont fournies principalement à des fins de référence.</span><span class="sxs-lookup"><span data-stu-id="a7315-147">To perform conversions, you should use the functions listed in the previous section; these tables are provided mainly for reference.</span></span>

### <a name="am_media_type"></a><span data-ttu-id="a7315-148">\_type de média am \_</span><span class="sxs-lookup"><span data-stu-id="a7315-148">AM\_MEDIA\_TYPE</span></span>



| <span data-ttu-id="a7315-149">Membre</span><span class="sxs-lookup"><span data-stu-id="a7315-149">Member</span></span>                   | <span data-ttu-id="a7315-150">Attribut</span><span class="sxs-lookup"><span data-stu-id="a7315-150">Attribute</span></span>                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a7315-151">**bTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="a7315-151">**bTemporalCompression**</span></span> | [<span data-ttu-id="a7315-152">**MF \_ MT \_ tous les \_ exemples \_ indépendants**</span><span class="sxs-lookup"><span data-stu-id="a7315-152">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) |
| <span data-ttu-id="a7315-153">**bFixedSizeSamples**</span><span class="sxs-lookup"><span data-stu-id="a7315-153">**bFixedSizeSamples**</span></span>    | [<span data-ttu-id="a7315-154">**\_exemples de \_ \_ taille fixe \_ MF MF**</span><span class="sxs-lookup"><span data-stu-id="a7315-154">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)           |
| <span data-ttu-id="a7315-155">**lSampleSize**</span><span class="sxs-lookup"><span data-stu-id="a7315-155">**lSampleSize**</span></span>          | [<span data-ttu-id="a7315-156">**taille de l’échantillon MF MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-156">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a><span data-ttu-id="a7315-157">WAVEFORMATEX, WAVEFORMATEXTENSIBLE</span><span class="sxs-lookup"><span data-stu-id="a7315-157">WAVEFORMATEX, WAVEFORMATEXTENSIBLE</span></span>



| <span data-ttu-id="a7315-158">Membre</span><span class="sxs-lookup"><span data-stu-id="a7315-158">Member</span></span>                  | <span data-ttu-id="a7315-159">Attribut</span><span class="sxs-lookup"><span data-stu-id="a7315-159">Attribute</span></span>                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7315-160">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="a7315-160">**wFormatTag**</span></span>          | [<span data-ttu-id="a7315-161">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="a7315-161">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)<br/> <span data-ttu-id="a7315-162">Si **wFormatTag** est \_ un format Wave \_ extensible, le sous-type se trouve dans le membre **subformat** .</span><span class="sxs-lookup"><span data-stu-id="a7315-162">If **wFormatTag** is WAVE\_FORMAT\_EXTENSIBLE, the subtype is found in the **SubFormat** member.</span></span><br/> |
| <span data-ttu-id="a7315-163">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="a7315-163">**nChannels**</span></span>           | [<span data-ttu-id="a7315-164">**\_canaux de \_ \_ numéros audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-164">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| <span data-ttu-id="a7315-165">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="a7315-165">**nSamplesPerSec**</span></span>      | [<span data-ttu-id="a7315-166">**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="a7315-166">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| <span data-ttu-id="a7315-167">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="a7315-167">**nAvgBytesPerSec**</span></span>     | [<span data-ttu-id="a7315-168">**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="a7315-168">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| <span data-ttu-id="a7315-169">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="a7315-169">**nBlockAlign**</span></span>         | [<span data-ttu-id="a7315-170">**\_alignement de \_ \_ bloc audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-170">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| <span data-ttu-id="a7315-171">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="a7315-171">**wBitsPerSample**</span></span>      | [<span data-ttu-id="a7315-172">**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**</span><span class="sxs-lookup"><span data-stu-id="a7315-172">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| <span data-ttu-id="a7315-173">**wValidBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="a7315-173">**wValidBitsPerSample**</span></span> | [<span data-ttu-id="a7315-174">**\_bits de \_ sortie audio MF- \_ octets valides \_ \_ par \_ exemple**</span><span class="sxs-lookup"><span data-stu-id="a7315-174">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| <span data-ttu-id="a7315-175">**wSamplesPerBlock**</span><span class="sxs-lookup"><span data-stu-id="a7315-175">**wSamplesPerBlock**</span></span>    | [<span data-ttu-id="a7315-176">**\_ \_ échantillons audio MF \_ MT \_ par \_ bloc**</span><span class="sxs-lookup"><span data-stu-id="a7315-176">**MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK**</span></span>](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| <span data-ttu-id="a7315-177">**dwChannelMask**</span><span class="sxs-lookup"><span data-stu-id="a7315-177">**dwChannelMask**</span></span>       | [<span data-ttu-id="a7315-178">**\_masque de \_ \_ canal audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-178">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| <span data-ttu-id="a7315-179">**SubFormat**</span><span class="sxs-lookup"><span data-stu-id="a7315-179">**SubFormat**</span></span>           | [<span data-ttu-id="a7315-180">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="a7315-180">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                                                                                                        |
| <span data-ttu-id="a7315-181">Données supplémentaires</span><span class="sxs-lookup"><span data-stu-id="a7315-181">Extra data</span></span>              | [<span data-ttu-id="a7315-182">**\_ \_ données utilisateur MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="a7315-182">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a><span data-ttu-id="a7315-183">VIDEOINFOHEADER, VIDEOINFOHEADER2</span><span class="sxs-lookup"><span data-stu-id="a7315-183">VIDEOINFOHEADER, VIDEOINFOHEADER2</span></span>



| <span data-ttu-id="a7315-184">Membre</span><span class="sxs-lookup"><span data-stu-id="a7315-184">Member</span></span>                                         | <span data-ttu-id="a7315-185">Attribut</span><span class="sxs-lookup"><span data-stu-id="a7315-185">Attribute</span></span>                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7315-186">**dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="a7315-186">**dwBitRate**</span></span>                                  | [<span data-ttu-id="a7315-187">**\_vitesse de \_ \_ transmission moy. MF**</span><span class="sxs-lookup"><span data-stu-id="a7315-187">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="a7315-188">**dwBitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="a7315-188">**dwBitErrorRate**</span></span>                             | [<span data-ttu-id="a7315-189">**\_taux d' \_ \_ erreur de bits Moy \_ \_ . MF**</span><span class="sxs-lookup"><span data-stu-id="a7315-189">**MF\_MT\_AVG\_BIT\_ERROR\_RATE**</span></span>](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| <span data-ttu-id="a7315-190">**AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="a7315-190">**AvgTimePerFrame**</span></span>                            | <span data-ttu-id="a7315-191">[**MF \_ \_ \_ Fréquence d’images MT**](mf-mt-frame-rate-attribute.md); utilisez [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) pour calculer cette valeur.</span><span class="sxs-lookup"><span data-stu-id="a7315-191">[**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md); use [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) to calculate this value.</span></span>                                                                             |
| <span data-ttu-id="a7315-192">**dwInterlaceFlags**</span><span class="sxs-lookup"><span data-stu-id="a7315-192">**dwInterlaceFlags**</span></span>                           | [<span data-ttu-id="a7315-193">**\_ \_ mode entrelacé MF-MT \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-193">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| <span data-ttu-id="a7315-194">**dwCopyProtectFlags**</span><span class="sxs-lookup"><span data-stu-id="a7315-194">**dwCopyProtectFlags**</span></span>                         | <span data-ttu-id="a7315-195">Aucun équivalent défini</span><span class="sxs-lookup"><span data-stu-id="a7315-195">No defined equivalent</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="a7315-196">**dwPictAspectRatioX**, **dwPictAspectRatioY**</span><span class="sxs-lookup"><span data-stu-id="a7315-196">**dwPictAspectRatioX**, **dwPictAspectRatioY**</span></span> | <span data-ttu-id="a7315-197">[**MF \_ Proportions de \_ pixels MT \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md); doit passer des proportions d’image aux proportions d’image.</span><span class="sxs-lookup"><span data-stu-id="a7315-197">[**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md); must convert from picture aspect ratio to picture aspect ratio.</span></span>                                                                                                      |
| <span data-ttu-id="a7315-198">**dwControlFlags**</span><span class="sxs-lookup"><span data-stu-id="a7315-198">**dwControlFlags**</span></span>                             | <span data-ttu-id="a7315-199">[**MF \_ \_indicateurs de \_ contrôle \_ du PAD MT**](mf-mt-pad-control-flags-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="a7315-199">[**MF\_MT\_PAD\_CONTROL\_FLAGS**](mf-mt-pad-control-flags-attribute.md).</span></span> <span data-ttu-id="a7315-200">Si l’indicateur **AMCONTROL \_ COLORINFO \_ présent** est présent, définissez les attributs de couleur étendus décrits dans [informations sur la couleur étendue](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="a7315-200">If the **AMCONTROL\_COLORINFO\_PRESENT** flag is present, set the extended color attributes described in [Extended Color Information](extended-color-information.md).</span></span> |
| <span data-ttu-id="a7315-201">**bmiHeader. bilargeur**, **BmiHeader. bihauteur**</span><span class="sxs-lookup"><span data-stu-id="a7315-201">**bmiHeader.biWidth**, **bmiHeader.biHeight**</span></span>  | [<span data-ttu-id="a7315-202">**\_taille de \_ trame MF MF \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-202">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| <span data-ttu-id="a7315-203">**bmiHeader.biBitCount**</span><span class="sxs-lookup"><span data-stu-id="a7315-203">**bmiHeader.biBitCount**</span></span>                       | <span data-ttu-id="a7315-204">Implicite dans le sous-type ([**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md)).</span><span class="sxs-lookup"><span data-stu-id="a7315-204">Implicit in the subtype ([**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md)).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="a7315-205">**bmiHeader. bicompression**</span><span class="sxs-lookup"><span data-stu-id="a7315-205">**bmiHeader.biCompression**</span></span>                    | <span data-ttu-id="a7315-206">Implicite dans le sous-type.</span><span class="sxs-lookup"><span data-stu-id="a7315-206">Implicit in the subtype.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="a7315-207">**bmiHeader.biSizeImage**</span><span class="sxs-lookup"><span data-stu-id="a7315-207">**bmiHeader.biSizeImage**</span></span>                      | [<span data-ttu-id="a7315-208">**taille de l’échantillon MF MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-208">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="a7315-209">Informations sur la palette</span><span class="sxs-lookup"><span data-stu-id="a7315-209">Palette information</span></span>                            | [<span data-ttu-id="a7315-210">**\_palette MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-210">**MF\_MT\_PALETTE**</span></span>](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

<span data-ttu-id="a7315-211">Les attributs suivants peuvent être déduits à partir de la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , mais ils nécessitent également une connaissance des détails de format.</span><span class="sxs-lookup"><span data-stu-id="a7315-211">The following attributes can be inferred from the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure but also require some knowledge of the format details.</span></span> <span data-ttu-id="a7315-212">Par exemple, différents formats YUV ont des exigences Stride différentes.</span><span class="sxs-lookup"><span data-stu-id="a7315-212">For example, different YUV formats have different stride requirements.</span></span>

-   [<span data-ttu-id="a7315-213">**\_Stride MT \_ par défaut \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-213">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)
-   [<span data-ttu-id="a7315-214">**\_ouverture de \_ l' \_ affichage \_ de la version MF**</span><span class="sxs-lookup"><span data-stu-id="a7315-214">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="a7315-215">**\_ouverture de \_ l' \_ analyse \_ panoramique MF MT**</span><span class="sxs-lookup"><span data-stu-id="a7315-215">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a><span data-ttu-id="a7315-216">MPEG1VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="a7315-216">MPEG1VIDEOINFO</span></span>



| <span data-ttu-id="a7315-217">Membre</span><span class="sxs-lookup"><span data-stu-id="a7315-217">Member</span></span>                                   | <span data-ttu-id="a7315-218">Attribut</span><span class="sxs-lookup"><span data-stu-id="a7315-218">Attribute</span></span>                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a7315-219">**dwStartTimeCode**</span><span class="sxs-lookup"><span data-stu-id="a7315-219">**dwStartTimeCode**</span></span>                      | [<span data-ttu-id="a7315-220">**\_code d' \_ heure de début du MPEG MF MT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-220">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="a7315-221">**bSequenceHeader**</span><span class="sxs-lookup"><span data-stu-id="a7315-221">**bSequenceHeader**</span></span>                      | [<span data-ttu-id="a7315-222">**\_ \_ \_ en-tête de séquence MPEG MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-222">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="a7315-223">**biXPelsPerMeter**, **biYPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="a7315-223">**biXPelsPerMeter**, **biYPelsPerMeter**</span></span> | [<span data-ttu-id="a7315-224">**\_ \_ \_ rapport hauteur/largeur des pixels \_ MF**</span><span class="sxs-lookup"><span data-stu-id="a7315-224">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a><span data-ttu-id="a7315-225">MPEG2VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="a7315-225">MPEG2VIDEOINFO</span></span>



| <span data-ttu-id="a7315-226">Membre</span><span class="sxs-lookup"><span data-stu-id="a7315-226">Member</span></span>               | <span data-ttu-id="a7315-227">Attribut</span><span class="sxs-lookup"><span data-stu-id="a7315-227">Attribute</span></span>                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a7315-228">**dwStartTimeCode**</span><span class="sxs-lookup"><span data-stu-id="a7315-228">**dwStartTimeCode**</span></span>  | [<span data-ttu-id="a7315-229">**\_code d' \_ heure de début du MPEG MF MT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-229">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="a7315-230">**dwSequenceHeader**</span><span class="sxs-lookup"><span data-stu-id="a7315-230">**dwSequenceHeader**</span></span> | [<span data-ttu-id="a7315-231">**\_ \_ \_ en-tête de séquence MPEG MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a7315-231">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="a7315-232">**dwProfile**</span><span class="sxs-lookup"><span data-stu-id="a7315-232">**dwProfile**</span></span>        | [<span data-ttu-id="a7315-233">**\_Profil de \_ MPEG2 \_ MT pour MF**</span><span class="sxs-lookup"><span data-stu-id="a7315-233">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md)                 |
| <span data-ttu-id="a7315-234">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="a7315-234">**dwLevel**</span></span>          | [<span data-ttu-id="a7315-235">**\_ \_ Niveau MPEG2 MT \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="a7315-235">**MF\_MT\_MPEG2\_LEVEL**</span></span>](mf-mt-mpeg2-level-attribute.md)                     |
| <span data-ttu-id="a7315-236">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="a7315-236">**dwFlags**</span></span>          | [<span data-ttu-id="a7315-237">**\_ \_ Indicateurs MPEG2 MT \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="a7315-237">**MF\_MT\_MPEG2\_FLAGS**</span></span>](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a><span data-ttu-id="a7315-238">Exemples</span><span class="sxs-lookup"><span data-stu-id="a7315-238">Examples</span></span>

<span data-ttu-id="a7315-239">Le code suivant remplit une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) à partir d’un type de média vidéo.</span><span class="sxs-lookup"><span data-stu-id="a7315-239">The following code fills in a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure from a video media type.</span></span> <span data-ttu-id="a7315-240">Notez que ces conversions perdent certaines des informations de format (entrelacement, fréquence d’images, données de couleur étendues).</span><span class="sxs-lookup"><span data-stu-id="a7315-240">Note that this conversions loses some of the format information (interlacing, frame rate, extended color data).</span></span> <span data-ttu-id="a7315-241">Toutefois, il peut être utile lors de l’enregistrement d’une image bitmap à partir d’une image vidéo, par exemple.</span><span class="sxs-lookup"><span data-stu-id="a7315-241">However, it might be useful when saving a bitmap from a video frame, for example.</span></span>


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a7315-242">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7315-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7315-243">Types de médias</span><span class="sxs-lookup"><span data-stu-id="a7315-243">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
