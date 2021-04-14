---
description: Ce filtre décode la vidéo MPEG-1, MPEG-2, H. 264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Décodeur vidéo Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392428"
---
# <a name="microsoft-mpeg-2-video-decoder"></a><span data-ttu-id="9716e-103">Décodeur vidéo Microsoft MPEG-2</span><span class="sxs-lookup"><span data-stu-id="9716e-103">Microsoft MPEG-2 Video Decoder</span></span>

<span data-ttu-id="9716e-104">Ce filtre décode la vidéo MPEG-1, MPEG-2, H. 264.</span><span class="sxs-lookup"><span data-stu-id="9716e-104">This filter decodes MPEG-1, MPEG-2, H.264 video.</span></span>

> [!Note]  
> <span data-ttu-id="9716e-105">Le décodage de la vidéo H. 264 requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9716e-105">Decoding of H.264 video requires Windows 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9716e-106">Ce filtre n’est pas pris en charge sur les plateformes IA-64.</span><span class="sxs-lookup"><span data-stu-id="9716e-106">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="9716e-107">Dans le registre, le nom convivial de ce filtre est « Microsoft DTV-DVD Video décoder ».</span><span class="sxs-lookup"><span data-stu-id="9716e-107">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Video Decoder".</span></span>



<span data-ttu-id="9716e-108">Informations de filtre</span><span class="sxs-lookup"><span data-stu-id="9716e-108">Filter Information</span></span>

<span data-ttu-id="9716e-109">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="9716e-109">Filter Interfaces</span></span>

[<span data-ttu-id="9716e-110">**IAMDecoderCaps**</span><span class="sxs-lookup"><span data-stu-id="9716e-110">**IAMDecoderCaps**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [<span data-ttu-id="9716e-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="9716e-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="9716e-112">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="9716e-112">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="9716e-113">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="9716e-113">Input Pin Media Types</span></span>

<span data-ttu-id="9716e-114">Broche d’entrée vidéo :</span><span class="sxs-lookup"><span data-stu-id="9716e-114">Video input pin:</span></span>

-   <span data-ttu-id="9716e-115">\_ \_ Pack chiffré DVD \_ de MediaType, \_ vidéo MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="9716e-115">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="9716e-116">MEDIATYPE \_ MPEG2 \_ PES, MEDIASUBTYPE \_ MPEG2 \_ Video</span><span class="sxs-lookup"><span data-stu-id="9716e-116">MEDIATYPE\_MPEG2\_PES, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="9716e-117">\_Vidéo MediaType, MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="9716e-117">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Packet</span></span>
-   <span data-ttu-id="9716e-118">\_Vidéo MediaType, MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="9716e-118">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Payload</span></span>
-   <span data-ttu-id="9716e-119">\_Vidéo MediaType, \_ vidéo MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="9716e-119">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>

<span data-ttu-id="9716e-120">Broche d’entrée de la sous-image :</span><span class="sxs-lookup"><span data-stu-id="9716e-120">Subpicture input pin:</span></span><br/>

-   <span data-ttu-id="9716e-121">\_ \_ Pack chiffré DVD de MediaType, sous- \_ \_ image de DVD MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="9716e-121">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_DVD\_SUBPICTURE</span></span>

<span data-ttu-id="9716e-122">À compter de Windows 7, la broche d’entrée vidéo prend également en charge les types d’entrée suivants :</span><span class="sxs-lookup"><span data-stu-id="9716e-122">Starting in Windows 7, the video input pin also supports the following input types:</span></span><br/>

-   <span data-ttu-id="9716e-123">**MediaType \_ Vidéo**, **MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="9716e-123">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_AVC1**</span></span>
-   <span data-ttu-id="9716e-124">**MediaType \_ Vidéo**, **MEDIASUBTYPE \_ H264 –**</span><span class="sxs-lookup"><span data-stu-id="9716e-124">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_H264**</span></span>
-   <span data-ttu-id="9716e-125">**MediaType \_ Vidéo**, **MEDIASUBTYPE \_ H264 –**</span><span class="sxs-lookup"><span data-stu-id="9716e-125">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_h264**</span></span>
-   <span data-ttu-id="9716e-126">**MediaType \_ Vidéo**, **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="9716e-126">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_X264**</span></span>
-   <span data-ttu-id="9716e-127">**MediaType \_ Vidéo**, **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="9716e-127">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_x264**</span></span>

<span data-ttu-id="9716e-128">Pour plus d’informations, consultez [types de vidéo H. 264](h-264-video-types.md) .</span><span class="sxs-lookup"><span data-stu-id="9716e-128">See [H.264 Video Types](h-264-video-types.md) for more information.</span></span> <span data-ttu-id="9716e-129">Le type de média d’entrée peut changer dynamiquement entre les types MPEG2 et H. 264.</span><span class="sxs-lookup"><span data-stu-id="9716e-129">The input media type can change dynamically between MPEG2 and H.264 types.</span></span><br/>

<span data-ttu-id="9716e-130">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="9716e-130">Input Pin Interfaces</span></span>

[<span data-ttu-id="9716e-131">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="9716e-131">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="9716e-132">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="9716e-132">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="9716e-133">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="9716e-133">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="9716e-134">**IMFSampleProtection**</span><span class="sxs-lookup"><span data-stu-id="9716e-134">**IMFSampleProtection**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [<span data-ttu-id="9716e-135">**IPin**</span><span class="sxs-lookup"><span data-stu-id="9716e-135">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="9716e-136">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="9716e-136">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="9716e-137">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="9716e-137">Output Pin Media Types</span></span>

<span data-ttu-id="9716e-138">Broche de sortie vidéo :</span><span class="sxs-lookup"><span data-stu-id="9716e-138">Video output pin:</span></span>

-   <span data-ttu-id="9716e-139">\_Vidéo MediaType, DXVA \_ ModeMPEG2 \_ A (DXVA 1,0)</span><span class="sxs-lookup"><span data-stu-id="9716e-139">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_A (DXVA 1.0)</span></span>
-   <span data-ttu-id="9716e-140">\_Vidéo MediaType, DXVA \_ ModeMPEG2 \_ C (DXVA 1,0)</span><span class="sxs-lookup"><span data-stu-id="9716e-140">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_C (DXVA 1.0)</span></span>
-   <span data-ttu-id="9716e-141">\_Vidéo MediaType, MEDIASUBTYPE \_ I420 (décodage logiciel ou DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="9716e-141">MEDIATYPE\_Video, MEDIASUBTYPE\_I420 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="9716e-142">\_Vidéo MediaType, MEDIASUBTYPE \_ NV12 (décodage logiciel ou DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="9716e-142">MEDIATYPE\_Video, MEDIASUBTYPE\_NV12 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="9716e-143">\_Vidéo MediaType, MEDIASUBTYPE \_ YUY2 (décodage logiciel ou DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="9716e-143">MEDIATYPE\_Video, MEDIASUBTYPE\_YUY2 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="9716e-144">\_Vidéo MediaType, MEDIASUBTYPE \_ IMC3 (DXVA 2.0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="9716e-144">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC3 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="9716e-145">\_Vidéo MediaType, MEDIASUBTYPE \_ IMC4 (DXVA 2.0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="9716e-145">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC4 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="9716e-146">\_Vidéo MediaType, MEDIASUBTYPE \_ S340 (DXVA 2.0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="9716e-146">MEDIATYPE\_Video, MEDIASUBTYPE\_S340 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="9716e-147">\_Vidéo MediaType, MEDIASUBTYPE \_ YV12 (DXVA 2.0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="9716e-147">MEDIATYPE\_Video, MEDIASUBTYPE\_YV12 (DXVA2.0 only)</span></span>

<span data-ttu-id="9716e-148">Broche de sortie ligne-21 :</span><span class="sxs-lookup"><span data-stu-id="9716e-148">Line-21 output pin:</span></span><br/>

-   <span data-ttu-id="9716e-149">MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket</span><span class="sxs-lookup"><span data-stu-id="9716e-149">MEDIATYPE\_AUXLine21Data, MEDIASUBTYPE\_Line21\_GOPPacket</span></span>

<span data-ttu-id="9716e-150">Broche de sortie de la sous-image :</span><span class="sxs-lookup"><span data-stu-id="9716e-150">Subpicture output pin:</span></span><br/>

-   <span data-ttu-id="9716e-151">\_Vidéo MediaType, MEDIASUBTYPE \_ AI44</span><span class="sxs-lookup"><span data-stu-id="9716e-151">MEDIATYPE\_Video, MEDIASUBTYPE\_AI44</span></span>
-   <span data-ttu-id="9716e-152">\_Vidéo MediaType, MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="9716e-152">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="9716e-153">\_Vidéo MediaType, MEDIASUBTYPE \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="9716e-153">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="9716e-154">\_Vidéo MediaType, MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="9716e-154">MEDIATYPE\_Video, MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="9716e-155">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="9716e-155">Output Pin Interfaces</span></span>

<span data-ttu-id="9716e-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (broche de sortie vidéo uniquement)</span><span class="sxs-lookup"><span data-stu-id="9716e-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (video output pin only)</span></span><br/> [<span data-ttu-id="9716e-157">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="9716e-157">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="9716e-158">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="9716e-158">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="9716e-159">**IPin**</span><span class="sxs-lookup"><span data-stu-id="9716e-159">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="9716e-160">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="9716e-160">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [<span data-ttu-id="9716e-161">**IVPConfig**</span><span class="sxs-lookup"><span data-stu-id="9716e-161">**IVPConfig**</span></span>](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

<span data-ttu-id="9716e-162">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="9716e-162">Filter CLSID</span></span>

<span data-ttu-id="9716e-163">**CLSID \_ CMPEG2VidDecoderDS** (défini dans wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="9716e-163">**CLSID\_CMPEG2VidDecoderDS** (defined in wmcodecdsp.h)</span></span>

<span data-ttu-id="9716e-164">Exécutable</span><span class="sxs-lookup"><span data-stu-id="9716e-164">Executable</span></span>

<span data-ttu-id="9716e-165">msmpeg2vdec.dll</span><span class="sxs-lookup"><span data-stu-id="9716e-165">msmpeg2vdec.dll</span></span>

[<span data-ttu-id="9716e-166">Mérite</span><span class="sxs-lookup"><span data-stu-id="9716e-166">Merit</span></span>](merit.md)

<span data-ttu-id="9716e-167">**Mérite \_ NORMAL** -1</span><span class="sxs-lookup"><span data-stu-id="9716e-167">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="9716e-168">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="9716e-168">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="9716e-169">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="9716e-169">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="9716e-170">Notes</span><span class="sxs-lookup"><span data-stu-id="9716e-170">Remarks</span></span>

<span data-ttu-id="9716e-171">Ce filtre a deux broches d’entrée et trois broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="9716e-171">This filter has two input pins and three output pins.</span></span>

<span data-ttu-id="9716e-172">Broches d’entrée :</span><span class="sxs-lookup"><span data-stu-id="9716e-172">Input pins:</span></span>

-   <span data-ttu-id="9716e-173">Entrée vidéo</span><span class="sxs-lookup"><span data-stu-id="9716e-173">Video input</span></span>
-   <span data-ttu-id="9716e-174">Entrée de sous-image</span><span class="sxs-lookup"><span data-stu-id="9716e-174">Subpicture input</span></span>

<span data-ttu-id="9716e-175">Broches de sortie :</span><span class="sxs-lookup"><span data-stu-id="9716e-175">Output pins:</span></span>

-   <span data-ttu-id="9716e-176">Sortie vidéo</span><span class="sxs-lookup"><span data-stu-id="9716e-176">Video output</span></span>
-   <span data-ttu-id="9716e-177">Sortie ligne-21</span><span class="sxs-lookup"><span data-stu-id="9716e-177">Line-21 output</span></span>
-   <span data-ttu-id="9716e-178">Sortie de sous-image</span><span class="sxs-lookup"><span data-stu-id="9716e-178">Subpicture output</span></span>

<span data-ttu-id="9716e-179">Le filtre ne crée pas la broche de sortie de sous-image, sauf si la broche d’entrée vidéo est connectée avec un type de média de **\_ \_ \_ Pack chiffré de DVD MediaType** .</span><span class="sxs-lookup"><span data-stu-id="9716e-179">The filter does not create the subpicture output pin unless the video input pin is connected with a **MEDIATYPE\_DVD\_ENCRYPTED\_PACK** media type.</span></span>

### <a name="mpeg-12-support"></a><span data-ttu-id="9716e-180">Support MPEG-1/2</span><span class="sxs-lookup"><span data-stu-id="9716e-180">MPEG-1/2 Support</span></span>

<span data-ttu-id="9716e-181">Pour MPEG-1 et MPEG-2, le décodeur prend en charge les formats suivants :</span><span class="sxs-lookup"><span data-stu-id="9716e-181">For MPEG-1 and MPEG-2, the decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9716e-182">Profils/niveaux</span><span class="sxs-lookup"><span data-stu-id="9716e-182">Profiles/Levels</span></span></td>
<td><span data-ttu-id="9716e-183">N’importe quelle combinaison des profils et niveaux suivants :</span><span class="sxs-lookup"><span data-stu-id="9716e-183">Any combination of the following profiles and levels:</span></span><br/>
<ul>
<li><span data-ttu-id="9716e-184">Profils : simple, main</span><span class="sxs-lookup"><span data-stu-id="9716e-184">Profiles: Simple, Main</span></span></li>
<li><span data-ttu-id="9716e-185">Niveaux : faible, principal, élevé, élevé 1440</span><span class="sxs-lookup"><span data-stu-id="9716e-185">Levels: Low, Main, High, High 1440</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9716e-186">Formats de chrominance</span><span class="sxs-lookup"><span data-stu-id="9716e-186">Chroma Formats</span></span></td>
<td><span data-ttu-id="9716e-187">4:2:0 Chroma</span><span class="sxs-lookup"><span data-stu-id="9716e-187">4:2:0 chroma</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9716e-188">Résolution maximale</span><span class="sxs-lookup"><span data-stu-id="9716e-188">Maximum Resolution</span></span></td>
<td><span data-ttu-id="9716e-189">1920 × 1088 pixels</span><span class="sxs-lookup"><span data-stu-id="9716e-189">1920 × 1088 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9716e-190">DXVA</span><span class="sxs-lookup"><span data-stu-id="9716e-190">DXVA</span></span></td>
<td><span data-ttu-id="9716e-191">Le décodeur prend en charge la version 1 et la version 2 de DirectX Video Acceleration (DXVA).</span><span class="sxs-lookup"><span data-stu-id="9716e-191">The decoder supports DirectX Video Acceleration (DXVA) version 1 and version 2.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9716e-192">Le décodeur ne prend pas en charge les flux binaires évolutifs.</span><span class="sxs-lookup"><span data-stu-id="9716e-192">The decoder does not support scalable bitstreams.</span></span> <span data-ttu-id="9716e-193">L’entrée doit être un flux vidéo élémentaire.</span><span class="sxs-lookup"><span data-stu-id="9716e-193">The input must be an elementary video stream.</span></span>

<span data-ttu-id="9716e-194">Le décodeur ne prend pas en charge les formats de chrominance 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="9716e-194">The decoder does not support 4:2:2 chroma formats.</span></span>

### <a name="h264-support"></a><span data-ttu-id="9716e-195">Prise en charge H. 264</span><span class="sxs-lookup"><span data-stu-id="9716e-195">H.264 Support</span></span>

<span data-ttu-id="9716e-196">Pour H. 264, le décodeur prend en charge les formats suivants :</span><span class="sxs-lookup"><span data-stu-id="9716e-196">For H.264, the decoder supports the following formats:</span></span>



| <span data-ttu-id="9716e-197">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9716e-197">Requirement</span></span> | <span data-ttu-id="9716e-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="9716e-198">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9716e-199">Profils/niveaux</span><span class="sxs-lookup"><span data-stu-id="9716e-199">Profiles/Levels</span></span>    | <span data-ttu-id="9716e-200">Les profils de base, principal et élevé, jusqu’au niveau 5,1.</span><span class="sxs-lookup"><span data-stu-id="9716e-200">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="9716e-201">(Pour plus d’informations, consultez la spécification ITU-T H. 264.)</span><span class="sxs-lookup"><span data-stu-id="9716e-201">(See ITU-T H.264 specification for details.)</span></span>                                                                                                                                                                          |
| <span data-ttu-id="9716e-202">Formats de chrominance</span><span class="sxs-lookup"><span data-stu-id="9716e-202">Chroma Formats</span></span>     | <span data-ttu-id="9716e-203">4:2:0 Chroma ou monochrome</span><span class="sxs-lookup"><span data-stu-id="9716e-203">4:2:0 chroma or monochrome</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="9716e-204">Résolution minimale</span><span class="sxs-lookup"><span data-stu-id="9716e-204">Minimum Resolution</span></span> | <span data-ttu-id="9716e-205">48 × 48 pixels</span><span class="sxs-lookup"><span data-stu-id="9716e-205">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="9716e-206">Résolution maximale</span><span class="sxs-lookup"><span data-stu-id="9716e-206">Maximum Resolution</span></span> | <span data-ttu-id="9716e-207">1920 × 1088 pixels</span><span class="sxs-lookup"><span data-stu-id="9716e-207">1920 × 1088 pixels</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="9716e-208">DXVA</span><span class="sxs-lookup"><span data-stu-id="9716e-208">DXVA</span></span>               | <span data-ttu-id="9716e-209">Le décodeur prend en charge la version 2 DXVA, mais pas la version 1 de la version DXVA.</span><span class="sxs-lookup"><span data-stu-id="9716e-209">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="9716e-210">Le décodage DXVA est pris en charge uniquement pour les flux de bits de ligne de base, principal et de profil principal compatibles.</span><span class="sxs-lookup"><span data-stu-id="9716e-210">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="9716e-211">(Les flux de bits de base compatibles avec les principaux sont définis comme **profil \_ idc**= 66 et **\_ \_ indicateur Set1 restreint**= 1.)</span><span class="sxs-lookup"><span data-stu-id="9716e-211">(Main-compatible Baseline bitstreams are defined as **profile\_idc**=66 and **constrained\_set1\_flag**=1.)</span></span> |



 

<span data-ttu-id="9716e-212">Le décodeur ne prend pas en charge la technologie de grain de film.</span><span class="sxs-lookup"><span data-stu-id="9716e-212">The decoder does not support Film Grain Technology.</span></span>

<span data-ttu-id="9716e-213">Pour plus d’informations sur les types de média H. 264, consultez la page [types de vidéo h. 264](h-264-video-types.md).</span><span class="sxs-lookup"><span data-stu-id="9716e-213">For information about the H.264 media types, see [H.264 Video Types](h-264-video-types.md).</span></span>

### <a name="codec-properties"></a><span data-ttu-id="9716e-214">Propriétés du codec</span><span class="sxs-lookup"><span data-stu-id="9716e-214">Codec Properties</span></span>

<span data-ttu-id="9716e-215">Les broches d’entrée prennent en charge les jeux de propriétés suivants via [**IKsPropertySet**](ikspropertyset.md):</span><span class="sxs-lookup"><span data-stu-id="9716e-215">The input pins support the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="9716e-216">**Jeu de propriétés protection de copie de DVD**</span><span class="sxs-lookup"><span data-stu-id="9716e-216">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="9716e-217">[**Jeu de propriétés**](dvd-subpicture-property-set.md) de sous-image de DVD (code confidentiel de sous-image uniquement)</span><span class="sxs-lookup"><span data-stu-id="9716e-217">[**DVD Subpicture Property Set**](dvd-subpicture-property-set.md) (subpicture pin only)</span></span>

<span data-ttu-id="9716e-218">Les broches d’entrée prennent en charge les propriétés suivantes par le biais de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="9716e-218">The input pins support the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="9716e-219">Propriété</span><span class="sxs-lookup"><span data-stu-id="9716e-219">Property</span></span>                                                                  | <span data-ttu-id="9716e-220">Nécessite</span><span class="sxs-lookup"><span data-stu-id="9716e-220">Requires</span></span>      |
|---------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="9716e-221">**AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="9716e-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md)         | <span data-ttu-id="9716e-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9716e-222">Windows Vista</span></span> |
| [<span data-ttu-id="9716e-223">**AVDecVideoInputScanType**</span><span class="sxs-lookup"><span data-stu-id="9716e-223">**AVDecVideoInputScanType**</span></span>](avdecvideoinputscantype-property.md)       | <span data-ttu-id="9716e-224">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9716e-224">Windows Vista</span></span> |
| [<span data-ttu-id="9716e-225">**AVDecVideoPixelAspectRatio**</span><span class="sxs-lookup"><span data-stu-id="9716e-225">**AVDecVideoPixelAspectRatio**</span></span>](avdecvideopixelaspectratio-property.md) | <span data-ttu-id="9716e-226">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9716e-226">Windows Vista</span></span> |



 

<span data-ttu-id="9716e-227">Le filtre prend en charge les propriétés suivantes par le biais de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="9716e-227">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="9716e-228">Propriété</span><span class="sxs-lookup"><span data-stu-id="9716e-228">Property</span></span>                                                                                | <span data-ttu-id="9716e-229">Nécessite</span><span class="sxs-lookup"><span data-stu-id="9716e-229">Requires</span></span>      |
|-----------------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="9716e-230">**AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="9716e-230">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                          | <span data-ttu-id="9716e-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9716e-231">Windows Vista</span></span> |
| [<span data-ttu-id="9716e-232">**AVDecVideoAcceleration \_ H264 –**</span><span class="sxs-lookup"><span data-stu-id="9716e-232">**AVDecVideoAcceleration\_H264**</span></span>](avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="9716e-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9716e-233">Windows 7</span></span>     |
| [<span data-ttu-id="9716e-234">**AVDecVideoAcceleration \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="9716e-234">**AVDecVideoAcceleration\_MPEG2**</span></span>](avdecvideoacceleration-mpeg2-property.md)          | <span data-ttu-id="9716e-235">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9716e-235">Windows 7</span></span>     |
| [<span data-ttu-id="9716e-236">**AVDecVideoDropPicWithMissingRef**</span><span class="sxs-lookup"><span data-stu-id="9716e-236">**AVDecVideoDropPicWithMissingRef**</span></span>](avdecvideodroppicwithmissingref-property.md)     | <span data-ttu-id="9716e-237">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9716e-237">Windows 7</span></span>     |
| [<span data-ttu-id="9716e-238">**AVDecVideoFastDecodeMode**</span><span class="sxs-lookup"><span data-stu-id="9716e-238">**AVDecVideoFastDecodeMode**</span></span>](avdecvideofastdecodemode.md)                            | <span data-ttu-id="9716e-239">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9716e-239">Windows 7</span></span>     |
| [<span data-ttu-id="9716e-240">**AVDecVideoImageSize**</span><span class="sxs-lookup"><span data-stu-id="9716e-240">**AVDecVideoImageSize**</span></span>](avdecvideoimagesize.md)                                      | <span data-ttu-id="9716e-241">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9716e-241">Windows 7</span></span>     |
| [<span data-ttu-id="9716e-242">**AVDecVideoSoftwareDeinterlaceMode**</span><span class="sxs-lookup"><span data-stu-id="9716e-242">**AVDecVideoSoftwareDeinterlaceMode**</span></span>](avdecvideosoftwaredeinterlacemode-property.md) | <span data-ttu-id="9716e-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9716e-243">Windows 7</span></span>     |
| [<span data-ttu-id="9716e-244">**AVDecVideoThumbnailGenerationMode**</span><span class="sxs-lookup"><span data-stu-id="9716e-244">**AVDecVideoThumbnailGenerationMode**</span></span>](avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="9716e-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9716e-245">Windows 7</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="9716e-246">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9716e-246">Requirements</span></span>



| <span data-ttu-id="9716e-247">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9716e-247">Requirement</span></span> | <span data-ttu-id="9716e-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="9716e-248">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9716e-249">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9716e-249">Minimum supported client</span></span><br/> | <span data-ttu-id="9716e-250">Windows Vista Édition familiale Premium, Windows Vista Édition intégrale, Windows 7 Édition familiale Premium, Windows 7 professionnel, Windows 7 entreprise, applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9716e-250">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9716e-251">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9716e-251">Minimum supported server</span></span><br/> | <span data-ttu-id="9716e-252">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9716e-252">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="9716e-253">En-tête</span><span class="sxs-lookup"><span data-stu-id="9716e-253">Header</span></span><br/>                   | <dl> <span data-ttu-id="9716e-254"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9716e-254"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="9716e-255">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9716e-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9716e-256">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="9716e-256">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="9716e-257">**Types de supports DVD**</span><span class="sxs-lookup"><span data-stu-id="9716e-257">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> <dt>

[<span data-ttu-id="9716e-258">Types vidéo H. 264</span><span class="sxs-lookup"><span data-stu-id="9716e-258">H.264 Video Types</span></span>](h-264-video-types.md)
</dt> </dl>

 

 
