---
description: Cette section décrit la prise en charge Media Foundation pour les fichiers Matroska Media Container (MKV).
title: Prise en charge de Matroska Media Container (MKV)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdd860f58087bc8a0f3fe95d278bfa81edc412d0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "110154214"
---
# <a name="matroska-media-container-mkv-support"></a><span data-ttu-id="fb30c-103">Prise en charge de Matroska Media Container (MKV)</span><span class="sxs-lookup"><span data-stu-id="fb30c-103">Matroska Media Container (MKV) support</span></span>

<span data-ttu-id="fb30c-104">Cette section décrit la prise en charge Media Foundation pour les fichiers Matroska Media Container (MKV).</span><span class="sxs-lookup"><span data-stu-id="fb30c-104">This section describes the Media Foundation support for Matroska Media Container (MKV) files.</span></span>

<span data-ttu-id="fb30c-105">Le format MKV peut prendre en charge plusieurs codecs vidéo et audio, comme H. 264 et AAC audio.</span><span class="sxs-lookup"><span data-stu-id="fb30c-105">The MKV format can support multiple video and audio codecs, such as H.264 and AAC audio.</span></span> <span data-ttu-id="fb30c-106">En général, les conteneurs décrivent la disposition des données audio et vidéo et les informations supplémentaires qui sont utilisées pour décrire ces flux A/V.</span><span class="sxs-lookup"><span data-stu-id="fb30c-106">In general, containers describe how video and audio data is laid out and what supplementary information is used to describe those A/V streams.</span></span> <span data-ttu-id="fb30c-107">Les conteneurs peuvent également inclure des données qui complètent les flux A/V, telles que le titre, les langues des flux audio, les pistes de sous-titre ou de légende, les polices pour ces sous-titres, images, informations de chapitre et menus.</span><span class="sxs-lookup"><span data-stu-id="fb30c-107">Containers can also include data that complements A/V streams, such as the title, languages of the audio streams, subtitle or caption tracks, fonts for those subtitles, images, chapter information, and menus.</span></span> <span data-ttu-id="fb30c-108">MKV est un format très flexible qui prend en charge un grand nombre de ces fonctionnalités de conteneur.</span><span class="sxs-lookup"><span data-stu-id="fb30c-108">MKV is a highly flexible format that supports many of these container features.</span></span> <span data-ttu-id="fb30c-109">Pour plus d’informations sur le format MKV, consultez [https://matroska.org](https://matroska.org/)</span><span class="sxs-lookup"><span data-stu-id="fb30c-109">For more info about the MKV format, see [https://matroska.org](https://matroska.org/)</span></span>


## <a name="mkv-container-feature-support"></a><span data-ttu-id="fb30c-110">Prise en charge des fonctionnalités de conteneur MKV</span><span class="sxs-lookup"><span data-stu-id="fb30c-110">MKV container feature support</span></span>
<span data-ttu-id="fb30c-111">Les fonctionnalités de conteneur MKV sont prises en charge sur le par Media Foundation des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb30c-111">MKV container features are supported on the by Media Foundation in the following ways:</span></span>
- <span data-ttu-id="fb30c-112">Si une ou plusieurs pistes vidéo sont présentes, la première piste est lue.</span><span class="sxs-lookup"><span data-stu-id="fb30c-112">If one or more video tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="fb30c-113">Si une ou plusieurs pistes audio sont présentes, la première piste est lue.</span><span class="sxs-lookup"><span data-stu-id="fb30c-113">If one or more audio tracks are present, the first track will be played.</span></span>
- <span data-ttu-id="fb30c-114">Les suivis de légende sont pris en charge, mais ne sont pas sélectionnés (lus) par défaut.</span><span class="sxs-lookup"><span data-stu-id="fb30c-114">Caption tracks are supported, but are not selected (played) by default.</span></span>
- <span data-ttu-id="fb30c-115">Si une ou plusieurs polices ou images sont présentes, les légendes et les images ne sont pas rendues, même si le fichier est chargé et lu.</span><span class="sxs-lookup"><span data-stu-id="fb30c-115">If one or more fonts or images are present, captions and images won’t render, although the file will load and play.</span></span>
- <span data-ttu-id="fb30c-116">Les informations de menu ne sont pas prises en charge et ne sont pas affichées, mais le fichier est chargé et lu.</span><span class="sxs-lookup"><span data-stu-id="fb30c-116">Menu information is not supported and won’t be displayed, but the file will load and play.</span></span>
- <span data-ttu-id="fb30c-117">Si les fichiers contenant des chapitres font référence à des fichiers supplémentaires, les fichiers supplémentaires ne sont pas lus.</span><span class="sxs-lookup"><span data-stu-id="fb30c-117">If files with chapters refer to supplemental files, the supplemental files won’t play.</span></span>
- <span data-ttu-id="fb30c-118">Les images miniatures sont disponibles lorsque vous recherchez des fichiers sur des lecteurs USB à l’aide de l’Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fb30c-118">Thumbnail images are available when browsing for files on USB drives using the file browser.</span></span>

<span data-ttu-id="fb30c-119">Cet ensemble de fonctionnalités doit permettre la lecture de la plupart des fichiers MKV s’ils contiennent des codecs pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fb30c-119">This set of features should allow playback of most MKV files if they contain supported codecs.</span></span>
<span data-ttu-id="fb30c-120">Les fichiers MKV qui contiennent des pistes vidéo et audio encodées avec les codecs répertoriés dans la section suivante sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fb30c-120">MKV files that contain video and audio tracks encoded with the codecs listed in the following section are supported.</span></span>

## <a name="supported-mkv-codecs"></a><span data-ttu-id="fb30c-121">Codecs MKV pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb30c-121">Supported MKV codecs</span></span>

### <a name="video-codec-support-for-mkv"></a><span data-ttu-id="fb30c-122">Prise en charge des codecs vidéo pour MKV</span><span class="sxs-lookup"><span data-stu-id="fb30c-122">Video codec support for MKV</span></span>

<span data-ttu-id="fb30c-123">ID Matroska : V_MPEG4/ISO/AVC</span><span class="sxs-lookup"><span data-stu-id="fb30c-123">Matroska ID: V_MPEG4/ISO/AVC</span></span>

- <span data-ttu-id="fb30c-124">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_H264</span><span class="sxs-lookup"><span data-stu-id="fb30c-124">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_H264</span></span>
- <span data-ttu-id="fb30c-125">Description : vidéo H. 264</span><span class="sxs-lookup"><span data-stu-id="fb30c-125">Description: H.264 video</span></span>
- <span data-ttu-id="fb30c-126">Identificateurs FourCC ou WAV : H264 –</span><span class="sxs-lookup"><span data-stu-id="fb30c-126">FourCC or WAV identifiers: H264</span></span>

<span data-ttu-id="fb30c-127">ID Matroska : V_MPEG2</span><span class="sxs-lookup"><span data-stu-id="fb30c-127">Matroska ID: V_MPEG2</span></span>

- <span data-ttu-id="fb30c-128">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MPEG2</span><span class="sxs-lookup"><span data-stu-id="fb30c-128">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPEG2</span></span>
- <span data-ttu-id="fb30c-129">Description : vidéo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="fb30c-129">Description: MPEG-2 video</span></span>

<span data-ttu-id="fb30c-130">ID Matroska : V_MPEG1</span><span class="sxs-lookup"><span data-stu-id="fb30c-130">Matroska ID: V_MPEG1</span></span>

- <span data-ttu-id="fb30c-131">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MPG1</span><span class="sxs-lookup"><span data-stu-id="fb30c-131">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MPG1</span></span>
- <span data-ttu-id="fb30c-132">Description : MPEG-1 Video</span><span class="sxs-lookup"><span data-stu-id="fb30c-132">Description: MPEG-1 video</span></span>
- <span data-ttu-id="fb30c-133">Identificateurs FourCC ou WAV : MPG1</span><span class="sxs-lookup"><span data-stu-id="fb30c-133">FourCC or WAV identifiers: MPG1</span></span>

<span data-ttu-id="fb30c-134">ID Matroska : V_MPEG4/MS/V3</span><span class="sxs-lookup"><span data-stu-id="fb30c-134">Matroska ID: V_MPEG4/MS/V3</span></span>

- <span data-ttu-id="fb30c-135">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MP43</span><span class="sxs-lookup"><span data-stu-id="fb30c-135">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP43</span></span>
- <span data-ttu-id="fb30c-136">Description : codec Microsoft MPEG 4 version 3</span><span class="sxs-lookup"><span data-stu-id="fb30c-136">Description: Microsoft MPEG 4 codec version 3</span></span>
- <span data-ttu-id="fb30c-137">Identificateurs FourCC ou WAV : MP43</span><span class="sxs-lookup"><span data-stu-id="fb30c-137">FourCC or WAV identifiers: MP43</span></span>

<span data-ttu-id="fb30c-138">ID Matroska : V_MPEG4/ISO/ASP</span><span class="sxs-lookup"><span data-stu-id="fb30c-138">Matroska ID: V_MPEG4/ISO/ASP</span></span>

- <span data-ttu-id="fb30c-139">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="fb30c-139">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="fb30c-140">Description : vidéo MPEG-4 part 2</span><span class="sxs-lookup"><span data-stu-id="fb30c-140">Description: MPEG-4 part 2 video</span></span>
- <span data-ttu-id="fb30c-141">Identificateurs FourCC ou WAV : MP4V</span><span class="sxs-lookup"><span data-stu-id="fb30c-141">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="fb30c-142">ID Matroska : V_MS/VFW/FOURCC</span><span class="sxs-lookup"><span data-stu-id="fb30c-142">Matroska ID: V_MS/VFW/FOURCC</span></span>

- <span data-ttu-id="fb30c-143">Description : correspond à plusieurs codecs généralement pris en charge dans le format AVI et disponibles sur la console.</span><span class="sxs-lookup"><span data-stu-id="fb30c-143">Description: Maps to several codecs usually supported in the AVI format that are available on the console.</span></span>

<span data-ttu-id="fb30c-144">ID Matroska : V_THEORA</span><span class="sxs-lookup"><span data-stu-id="fb30c-144">Matroska ID: V_THEORA</span></span>

- <span data-ttu-id="fb30c-145">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_Theora</span><span class="sxs-lookup"><span data-stu-id="fb30c-145">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_Theora</span></span>
- <span data-ttu-id="fb30c-146">Description : Theora</span><span class="sxs-lookup"><span data-stu-id="fb30c-146">Description: Theora</span></span>
- <span data-ttu-id="fb30c-147">Identificateurs FourCC ou WAV : Theo</span><span class="sxs-lookup"><span data-stu-id="fb30c-147">FourCC or WAV identifiers: theo</span></span>

<span data-ttu-id="fb30c-148">ID Matroska : V_MPEG4/ISO/SP</span><span class="sxs-lookup"><span data-stu-id="fb30c-148">Matroska ID: V_MPEG4/ISO/SP</span></span>

- <span data-ttu-id="fb30c-149">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="fb30c-149">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="fb30c-150">Description : profil simple ISO MPEG4 (DivX4)</span><span class="sxs-lookup"><span data-stu-id="fb30c-150">Description: MPEG4 ISO simple profile (DivX4)</span></span>
- <span data-ttu-id="fb30c-151">Identificateurs FourCC ou WAV : MP4V</span><span class="sxs-lookup"><span data-stu-id="fb30c-151">FourCC or WAV identifiers: MP4V</span></span>

<span data-ttu-id="fb30c-152">ID Matroska : V_MPEG4/ISO/AP</span><span class="sxs-lookup"><span data-stu-id="fb30c-152">Matroska ID: V_MPEG4/ISO/AP</span></span>

- <span data-ttu-id="fb30c-153">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MP4V</span><span class="sxs-lookup"><span data-stu-id="fb30c-153">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MP4V</span></span>
- <span data-ttu-id="fb30c-154">Description : profil simple Advanced standard MPEG4 ISO (DivX5, XviD, FFMPEG)</span><span class="sxs-lookup"><span data-stu-id="fb30c-154">Description: MPEG4 ISO advanced simple profile (DivX5, XviD, FFMPEG)</span></span>
- <span data-ttu-id="fb30c-155">Identificateurs FourCC ou WAV : MP4V</span><span class="sxs-lookup"><span data-stu-id="fb30c-155">FourCC or WAV identifiers: MP4V</span></span>


<span data-ttu-id="fb30c-156">ID Matroska : V_MPEGH/ISO/HEVC</span><span class="sxs-lookup"><span data-stu-id="fb30c-156">Matroska ID: V_MPEGH/ISO/HEVC</span></span> 

- <span data-ttu-id="fb30c-157">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_HEVC</span><span class="sxs-lookup"><span data-stu-id="fb30c-157">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_HEVC</span></span>
- <span data-ttu-id="fb30c-158">Description : HEVC/H. 265</span><span class="sxs-lookup"><span data-stu-id="fb30c-158">Description: HEVC/H.265</span></span>
- <span data-ttu-id="fb30c-159">Identificateurs FourCC ou WAV :</span><span class="sxs-lookup"><span data-stu-id="fb30c-159">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="fb30c-160">ID Matroska : V_VP8</span><span class="sxs-lookup"><span data-stu-id="fb30c-160">Matroska ID: V_VP8</span></span>

- <span data-ttu-id="fb30c-161">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_VP80</span><span class="sxs-lookup"><span data-stu-id="fb30c-161">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP80</span></span>
- <span data-ttu-id="fb30c-162">Description : format du codec VP8</span><span class="sxs-lookup"><span data-stu-id="fb30c-162">Description: VP8 Codec format</span></span>
- <span data-ttu-id="fb30c-163">Identificateurs FourCC ou WAV : VP80</span><span class="sxs-lookup"><span data-stu-id="fb30c-163">FourCC or WAV identifiers: VP80</span></span>

<span data-ttu-id="fb30c-164">ID Matroska : V_VP9</span><span class="sxs-lookup"><span data-stu-id="fb30c-164">Matroska ID: V_VP9</span></span>

- <span data-ttu-id="fb30c-165">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_VP90</span><span class="sxs-lookup"><span data-stu-id="fb30c-165">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_VP90</span></span>
- <span data-ttu-id="fb30c-166">Description : format du codec VP9</span><span class="sxs-lookup"><span data-stu-id="fb30c-166">Description: VP9 Codec format</span></span>
- <span data-ttu-id="fb30c-167">Identificateurs FourCC ou WAV : VP90</span><span class="sxs-lookup"><span data-stu-id="fb30c-167">FourCC or WAV identifiers: VP90</span></span>

<span data-ttu-id="fb30c-168">ID Matroska : V_MJPEG</span><span class="sxs-lookup"><span data-stu-id="fb30c-168">Matroska ID: V_MJPEG</span></span>

- <span data-ttu-id="fb30c-169">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_MJPG</span><span class="sxs-lookup"><span data-stu-id="fb30c-169">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_MJPG</span></span>
- <span data-ttu-id="fb30c-170">Description : Motion JPEG</span><span class="sxs-lookup"><span data-stu-id="fb30c-170">Description: Motion JPEG</span></span>
- <span data-ttu-id="fb30c-171">Identificateurs FourCC ou WAV : MJPG</span><span class="sxs-lookup"><span data-stu-id="fb30c-171">FourCC or WAV identifiers: MJPG</span></span>

<span data-ttu-id="fb30c-172">ID Matroska : V_AV1</span><span class="sxs-lookup"><span data-stu-id="fb30c-172">Matroska ID: V_AV1</span></span>

- <span data-ttu-id="fb30c-173">MF_MT_SUBTYPE Media Foundation MSFT : MFVideoFormat_AV1</span><span class="sxs-lookup"><span data-stu-id="fb30c-173">MSFT Media Foundation MF_MT_SUBTYPE: MFVideoFormat_AV1</span></span>
- <span data-ttu-id="fb30c-174">Description : AOMedia Video 1</span><span class="sxs-lookup"><span data-stu-id="fb30c-174">Description: AOMedia Video 1</span></span>
- <span data-ttu-id="fb30c-175">Identificateurs FourCC ou WAV : AV01</span><span class="sxs-lookup"><span data-stu-id="fb30c-175">FourCC or WAV identifiers: AV01</span></span>

### <a name="audio-codec-support-for-mkv"></a><span data-ttu-id="fb30c-176">Prise en charge des codecs audio pour MKV</span><span class="sxs-lookup"><span data-stu-id="fb30c-176">Audio codec support for MKV</span></span>

<span data-ttu-id="fb30c-177">ID Matroska : A_AAC</span><span class="sxs-lookup"><span data-stu-id="fb30c-177">Matroska ID: A_AAC</span></span>

- <span data-ttu-id="fb30c-178">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="fb30c-178">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="fb30c-179">Description : codage audio avancé (AAC)</span><span class="sxs-lookup"><span data-stu-id="fb30c-179">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="fb30c-180">Identificateurs FourCC ou WAV : WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="fb30c-180">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="fb30c-181">ID Matroska : A_AC3</span><span class="sxs-lookup"><span data-stu-id="fb30c-181">Matroska ID: A_AC3</span></span>

- <span data-ttu-id="fb30c-182">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_Dolby_AC3</span><span class="sxs-lookup"><span data-stu-id="fb30c-182">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_AC3</span></span>
- <span data-ttu-id="fb30c-183">Description : Dolby AC3</span><span class="sxs-lookup"><span data-stu-id="fb30c-183">Description: Dolby AC3</span></span>
- <span data-ttu-id="fb30c-184">Identificateurs FourCC ou WAV : WAVE_FORMAT_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="fb30c-184">FourCC or WAV identifiers: WAVE_FORMAT_DOLBY_AC3_SPDIF</span></span>

<span data-ttu-id="fb30c-185">ID Matroska : A_MPEG/L3</span><span class="sxs-lookup"><span data-stu-id="fb30c-185">Matroska ID: A_MPEG/L3</span></span>

- <span data-ttu-id="fb30c-186">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_MP3</span><span class="sxs-lookup"><span data-stu-id="fb30c-186">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MP3</span></span>
- <span data-ttu-id="fb30c-187">Description : MPEG Audio Layer-3 (MP3)</span><span class="sxs-lookup"><span data-stu-id="fb30c-187">Description: MPEG Audio Layer-3 (MP3)</span></span>
- <span data-ttu-id="fb30c-188">Identificateurs FourCC ou WAV : WAVE_FORMAT_MPEGLAYER3</span><span class="sxs-lookup"><span data-stu-id="fb30c-188">FourCC or WAV identifiers: WAVE_FORMAT_MPEGLAYER3</span></span>

<span data-ttu-id="fb30c-189">ID Matroska : A_MPEG/L1</span><span class="sxs-lookup"><span data-stu-id="fb30c-189">Matroska ID: A_MPEG/L1</span></span>

- <span data-ttu-id="fb30c-190">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="fb30c-190">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="fb30c-191">Description : charge utile MPEG-1</span><span class="sxs-lookup"><span data-stu-id="fb30c-191">Description: MPEG-1 audio payload</span></span>
- <span data-ttu-id="fb30c-192">Identificateurs FourCC ou WAV : WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="fb30c-192">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="fb30c-193">ID Matroska : A_PCM/INT/BIG</span><span class="sxs-lookup"><span data-stu-id="fb30c-193">Matroska ID: A_PCM/INT/BIG</span></span>

- <span data-ttu-id="fb30c-194">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="fb30c-194">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="fb30c-195">Description : audio PCM non compressé</span><span class="sxs-lookup"><span data-stu-id="fb30c-195">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="fb30c-196">Identificateurs FourCC ou WAV : WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="fb30c-196">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="fb30c-197">ID Matroska : A_PCM/INT/LIT</span><span class="sxs-lookup"><span data-stu-id="fb30c-197">Matroska ID: A_PCM/INT/LIT</span></span>

- <span data-ttu-id="fb30c-198">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_PCM</span><span class="sxs-lookup"><span data-stu-id="fb30c-198">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_PCM</span></span>
- <span data-ttu-id="fb30c-199">Description : audio PCM non compressé</span><span class="sxs-lookup"><span data-stu-id="fb30c-199">Description: Uncompressed PCM audio</span></span>
- <span data-ttu-id="fb30c-200">Identificateurs FourCC ou WAV : WAVE_FORMAT_PCM</span><span class="sxs-lookup"><span data-stu-id="fb30c-200">FourCC or WAV identifiers: WAVE_FORMAT_PCM</span></span>

<span data-ttu-id="fb30c-201">ID Matroska : A_PCM/FLOAT/IEEE</span><span class="sxs-lookup"><span data-stu-id="fb30c-201">Matroska ID: A_PCM/FLOAT/IEEE</span></span>

- <span data-ttu-id="fb30c-202">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_Float</span><span class="sxs-lookup"><span data-stu-id="fb30c-202">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Float</span></span>
- <span data-ttu-id="fb30c-203">Description : audio à virgule flottante IEEE non compressé</span><span class="sxs-lookup"><span data-stu-id="fb30c-203">Description: Uncompressed IEEE floating-point audio</span></span>
- <span data-ttu-id="fb30c-204">Identificateurs FourCC ou WAV : WAVE_FORMAT_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="fb30c-204">FourCC or WAV identifiers: WAVE_FORMAT_IEEE_FLOAT</span></span>

<span data-ttu-id="fb30c-205">ID Matroska : A_ALAC</span><span class="sxs-lookup"><span data-stu-id="fb30c-205">Matroska ID: A_ALAC</span></span>

- <span data-ttu-id="fb30c-206">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_ALAC</span><span class="sxs-lookup"><span data-stu-id="fb30c-206">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_ALAC</span></span>
- <span data-ttu-id="fb30c-207">Description : codec audio Apple sans perte</span><span class="sxs-lookup"><span data-stu-id="fb30c-207">Description: Apple Lossless Audio Codec</span></span>
- <span data-ttu-id="fb30c-208">Identificateurs FourCC ou WAV :</span><span class="sxs-lookup"><span data-stu-id="fb30c-208">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="fb30c-209">ID Matroska : A_MPEG/L2</span><span class="sxs-lookup"><span data-stu-id="fb30c-209">Matroska ID: A_MPEG/L2</span></span>

- <span data-ttu-id="fb30c-210">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_MPEG</span><span class="sxs-lookup"><span data-stu-id="fb30c-210">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_MPEG</span></span>
- <span data-ttu-id="fb30c-211">Description : MPEG Audio 1, 2 couche II</span><span class="sxs-lookup"><span data-stu-id="fb30c-211">Description: MPEG Audio 1, 2 Layer II</span></span>
- <span data-ttu-id="fb30c-212">Identificateurs FourCC ou WAV : WAVE_FORMAT_MPEG</span><span class="sxs-lookup"><span data-stu-id="fb30c-212">FourCC or WAV identifiers: WAVE_FORMAT_MPEG</span></span>

<span data-ttu-id="fb30c-213">ID Matroska : A_DTS</span><span class="sxs-lookup"><span data-stu-id="fb30c-213">Matroska ID: A_DTS</span></span>

- <span data-ttu-id="fb30c-214">MF_MT_SUBTYPE Media Foundation MSFT : MEDIASUBTYPE_DTS_HD</span><span class="sxs-lookup"><span data-stu-id="fb30c-214">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DTS_HD</span></span>
- <span data-ttu-id="fb30c-215">Description : système de théâtre numérique</span><span class="sxs-lookup"><span data-stu-id="fb30c-215">Description: Digital Theatre System</span></span>
- <span data-ttu-id="fb30c-216">Identificateurs FourCC ou WAV : WAVE_FORMAT_DTS</span><span class="sxs-lookup"><span data-stu-id="fb30c-216">FourCC or WAV identifiers: WAVE_FORMAT_DTS</span></span>

<span data-ttu-id="fb30c-217">ID Matroska : A_OPUS</span><span class="sxs-lookup"><span data-stu-id="fb30c-217">Matroska ID: A_OPUS</span></span>

- <span data-ttu-id="fb30c-218">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_Opus</span><span class="sxs-lookup"><span data-stu-id="fb30c-218">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Opus</span></span>
- <span data-ttu-id="fb30c-219">Description : opus</span><span class="sxs-lookup"><span data-stu-id="fb30c-219">Description: Opus</span></span>
- <span data-ttu-id="fb30c-220">Identificateurs FourCC ou WAV : WAVE_FORMAT_OPUS</span><span class="sxs-lookup"><span data-stu-id="fb30c-220">FourCC or WAV identifiers: WAVE_FORMAT_OPUS</span></span>

<span data-ttu-id="fb30c-221">ID Matroska : A_VORBIS</span><span class="sxs-lookup"><span data-stu-id="fb30c-221">Matroska ID: A_VORBIS</span></span>

- <span data-ttu-id="fb30c-222">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_Vorbis</span><span class="sxs-lookup"><span data-stu-id="fb30c-222">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Vorbis</span></span>
- <span data-ttu-id="fb30c-223">Description : Vorbis</span><span class="sxs-lookup"><span data-stu-id="fb30c-223">Description: Vorbis</span></span>
- <span data-ttu-id="fb30c-224">Identificateurs FourCC ou WAV :</span><span class="sxs-lookup"><span data-stu-id="fb30c-224">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="fb30c-225">ID Matroska : A_FLAC</span><span class="sxs-lookup"><span data-stu-id="fb30c-225">Matroska ID: A_FLAC</span></span>

- <span data-ttu-id="fb30c-226">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_FLAC</span><span class="sxs-lookup"><span data-stu-id="fb30c-226">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_FLAC</span></span>
- <span data-ttu-id="fb30c-227">Description : codec audio gratuit sans perte</span><span class="sxs-lookup"><span data-stu-id="fb30c-227">Description: Free Lossless Audio Codec</span></span>
- <span data-ttu-id="fb30c-228">Identificateurs FourCC ou WAV : WAVE_FORMAT_FLAC</span><span class="sxs-lookup"><span data-stu-id="fb30c-228">FourCC or WAV identifiers: WAVE_FORMAT_FLAC</span></span>

<span data-ttu-id="fb30c-229">ID Matroska : A_AAC/MAIN</span><span class="sxs-lookup"><span data-stu-id="fb30c-229">Matroska ID: A_AAC/MAIN</span></span>

- <span data-ttu-id="fb30c-230">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_AAC</span><span class="sxs-lookup"><span data-stu-id="fb30c-230">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_AAC</span></span>
- <span data-ttu-id="fb30c-231">Description : codage audio avancé (AAC)</span><span class="sxs-lookup"><span data-stu-id="fb30c-231">Description: Advanced Audio Coding (AAC)</span></span>
- <span data-ttu-id="fb30c-232">Identificateurs FourCC ou WAV : WAVE_FORMAT_MPEG_HEAAC</span><span class="sxs-lookup"><span data-stu-id="fb30c-232">FourCC or WAV identifiers: WAVE_FORMAT_MPEG_HEAAC</span></span>

<span data-ttu-id="fb30c-233">ID Matroska : A_EAC3</span><span class="sxs-lookup"><span data-stu-id="fb30c-233">Matroska ID: A_EAC3</span></span>

- <span data-ttu-id="fb30c-234">MF_MT_SUBTYPE Media Foundation MSFT : MFAudioFormat_Dolby_DDPlus</span><span class="sxs-lookup"><span data-stu-id="fb30c-234">MSFT Media Foundation MF_MT_SUBTYPE: MFAudioFormat_Dolby_DDPlus</span></span>
- <span data-ttu-id="fb30c-235">Description : Enhanced AC-3</span><span class="sxs-lookup"><span data-stu-id="fb30c-235">Description: Enhanced AC-3</span></span>
- <span data-ttu-id="fb30c-236">Identificateurs FourCC ou WAV :</span><span class="sxs-lookup"><span data-stu-id="fb30c-236">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="fb30c-237">ID Matroska : A_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="fb30c-237">Matroska ID: A_TRUEHD</span></span>

- <span data-ttu-id="fb30c-238">MF_MT_SUBTYPE Media Foundation MSFT : MEDIASUBTYPE_DOLBY_TRUEHD</span><span class="sxs-lookup"><span data-stu-id="fb30c-238">MSFT Media Foundation MF_MT_SUBTYPE: MEDIASUBTYPE_DOLBY_TRUEHD</span></span>
- <span data-ttu-id="fb30c-239">Description : Dolby TrueHD</span><span class="sxs-lookup"><span data-stu-id="fb30c-239">Description: Dolby TrueHD</span></span>
- <span data-ttu-id="fb30c-240">Identificateurs FourCC ou WAV :</span><span class="sxs-lookup"><span data-stu-id="fb30c-240">FourCC or WAV identifiers:</span></span> 

<span data-ttu-id="fb30c-241">ID Matroska : A_MS/ACM</span><span class="sxs-lookup"><span data-stu-id="fb30c-241">Matroska ID: A_MS/ACM</span></span>

- <span data-ttu-id="fb30c-242">MSFT Media Foundation MF_MT_SUBTYPE : correspond à plusieurs types audio WAVE_FORMAT définis dans mmreg. h</span><span class="sxs-lookup"><span data-stu-id="fb30c-242">MSFT Media Foundation MF_MT_SUBTYPE: Maps to several WAVE_FORMAT audio types defined in mmreg.h</span></span>


### <a name="subtitles-codec-support-for-mkv"></a><span data-ttu-id="fb30c-243">Prise en charge du codec sous-titres pour MKV</span><span class="sxs-lookup"><span data-stu-id="fb30c-243">Subtitles codec support for MKV</span></span>

<span data-ttu-id="fb30c-244">ID Matroska : S_TEXT/ASCII</span><span class="sxs-lookup"><span data-stu-id="fb30c-244">Matroska ID: S_TEXT/ASCII</span></span>

- <span data-ttu-id="fb30c-245">MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="fb30c-245">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="fb30c-246">Description : texte ASCII</span><span class="sxs-lookup"><span data-stu-id="fb30c-246">Description: ASCII text</span></span>

<span data-ttu-id="fb30c-247">ID Matroska : S_TEXT/UTF8</span><span class="sxs-lookup"><span data-stu-id="fb30c-247">Matroska ID: S_TEXT/UTF8</span></span>

- <span data-ttu-id="fb30c-248">MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_SRT</span><span class="sxs-lookup"><span data-stu-id="fb30c-248">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SRT</span></span>
- <span data-ttu-id="fb30c-249">Description : texte brut UTF-8</span><span class="sxs-lookup"><span data-stu-id="fb30c-249">Description: UTF-8 Plain Text</span></span>

<span data-ttu-id="fb30c-250">ID Matroska : S_TEXT/SSA</span><span class="sxs-lookup"><span data-stu-id="fb30c-250">Matroska ID: S_TEXT/SSA</span></span>

- <span data-ttu-id="fb30c-251">MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="fb30c-251">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="fb30c-252">Description : format des sous-titres</span><span class="sxs-lookup"><span data-stu-id="fb30c-252">Description: Subtitles Format</span></span>

<span data-ttu-id="fb30c-253">ID Matroska : S_TEXT/ASS</span><span class="sxs-lookup"><span data-stu-id="fb30c-253">Matroska ID: S_TEXT/ASS</span></span>

- <span data-ttu-id="fb30c-254">MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_SSA</span><span class="sxs-lookup"><span data-stu-id="fb30c-254">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_SSA</span></span>
- <span data-ttu-id="fb30c-255">Description : format des sous-titres avancés</span><span class="sxs-lookup"><span data-stu-id="fb30c-255">Description: Advanced Subtitles Format</span></span>

<span data-ttu-id="fb30c-256">ID Matroska : S_VOBSUB</span><span class="sxs-lookup"><span data-stu-id="fb30c-256">Matroska ID: S_VOBSUB</span></span>

- <span data-ttu-id="fb30c-257">MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_VobSub</span><span class="sxs-lookup"><span data-stu-id="fb30c-257">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_VobSub</span></span>
- <span data-ttu-id="fb30c-258">Description : VobSub sous-titres</span><span class="sxs-lookup"><span data-stu-id="fb30c-258">Description: VobSub subtitles</span></span>

<span data-ttu-id="fb30c-259">ID Matroska : S_HDMV/PGS</span><span class="sxs-lookup"><span data-stu-id="fb30c-259">Matroska ID: S_HDMV/PGS</span></span>

- <span data-ttu-id="fb30c-260">MF_MT_SUBTYPE Media Foundation MSFT : MFSubtitleFormat_PGS</span><span class="sxs-lookup"><span data-stu-id="fb30c-260">MSFT Media Foundation MF_MT_SUBTYPE: MFSubtitleFormat_PGS</span></span>
- <span data-ttu-id="fb30c-261">Description : HDMV Presentation Graphics sous-titres (PG)</span><span class="sxs-lookup"><span data-stu-id="fb30c-261">Description: HDMV presentation graphics subtitles (PGS)</span></span>


## <a name="technical-details-regarding-codecs"></a><span data-ttu-id="fb30c-262">Détails techniques concernant les codecs</span><span class="sxs-lookup"><span data-stu-id="fb30c-262">Technical details regarding codecs</span></span>

<span data-ttu-id="fb30c-263">Pour obtenir des détails techniques sur les codecs, consultez les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="fb30c-263">See the following for technical details regarding codecs.</span></span>

- [<span data-ttu-id="fb30c-264">Spécifications du codec Matroska</span><span class="sxs-lookup"><span data-stu-id="fb30c-264">Matroska Codec Specs</span></span>](http://www.matroska.org/technical/specs/codecid/index.html)
- [<span data-ttu-id="fb30c-265">GUID de sous-type audio</span><span class="sxs-lookup"><span data-stu-id="fb30c-265">Audio Subtype GUIDs</span></span>](audio-subtype-guids.md)
- [<span data-ttu-id="fb30c-266">GUID de sous-type de vidéo</span><span class="sxs-lookup"><span data-stu-id="fb30c-266">Video Subtype GUIDs</span></span>](video-subtype-guids.md)


## <a name="related-topics"></a><span data-ttu-id="fb30c-267">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb30c-267">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb30c-268">Formats multimédias pris en charge dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb30c-268">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="fb30c-269">Guide de programmation Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fb30c-269">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



