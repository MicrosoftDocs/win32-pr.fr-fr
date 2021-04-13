---
description: GUID de sous-type audio
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: GUID de sous-type audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484129"
---
# <a name="audio-subtype-guids"></a><span data-ttu-id="418a9-103">GUID de sous-type audio</span><span class="sxs-lookup"><span data-stu-id="418a9-103">Audio Subtype GUIDs</span></span>

<span data-ttu-id="418a9-104">Les GUID de sous-type audio suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="418a9-104">The following audio subtype GUIDs are defined.</span></span> <span data-ttu-id="418a9-105">Pour spécifier le sous-type, définissez l’attribut de sous- [**\_ \_ type MF MT**](mf-mt-subtype-attribute.md) sur le type de média.</span><span class="sxs-lookup"><span data-stu-id="418a9-105">To specify the subtype, set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="418a9-106">Sauf indication contraire, ces constantes sont définies dans le fichier d’en-tête mfapi. h.</span><span class="sxs-lookup"><span data-stu-id="418a9-106">Except where noted, these constants are defined in the header file mfapi.h.</span></span>

<span data-ttu-id="418a9-107">Quand ces sous-types sont utilisés, affectez à l’attribut de [ \_ \_ \_ type principal MF MT](mf-mt-major-type-attribute.md) la valeur **MFMediaType \_ audio**.</span><span class="sxs-lookup"><span data-stu-id="418a9-107">When these subtypes are used, set the [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="418a9-108">GUID</span><span class="sxs-lookup"><span data-stu-id="418a9-108">GUID</span></span></th>
<th><span data-ttu-id="418a9-109">Description</span><span class="sxs-lookup"><span data-stu-id="418a9-109">Description</span></span></th>
<th><span data-ttu-id="418a9-110">Balise de format (FOURCC)</span><span class="sxs-lookup"><span data-stu-id="418a9-110">Format Tag (FOURCC)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="418a9-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span></span></td>
<td><span data-ttu-id="418a9-112">Codage audio avancé (AAC).</span><span class="sxs-lookup"><span data-stu-id="418a9-112">Advanced Audio Coding (AAC).</span></span><br/> <span data-ttu-id="418a9-113">Ce sous-type est utilisé pour l’AAC contenu dans un fichier AVI dont la balise de format audio est égale à 0x00FF.</span><span class="sxs-lookup"><span data-stu-id="418a9-113">This subtype is used for AAC contained in an AVI file with an audio format tag equal to 0x00FF.</span></span> <br/> <span data-ttu-id="418a9-114">Pour plus d’informations, consultez <a href="aac-decoder.md"><strong>décodeur AAC</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="418a9-114">For more information, see <a href="aac-decoder.md"><strong>AAC Decoder</strong></a>.</span></span><br/> <span data-ttu-id="418a9-115">Défini dans wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="418a9-115">Defined in wmcodecdsp.h</span></span><br/></td>
<td><span data-ttu-id="418a9-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="418a9-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-117"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-117"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="418a9-118">Codage audio avancé (AAC).</span><span class="sxs-lookup"><span data-stu-id="418a9-118">Advanced Audio Coding (AAC).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="418a9-119">Équivalent à MEDIASUBTYPE_MPEG_HEAAC, défini dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="418a9-119">Equivalent to MEDIASUBTYPE_MPEG_HEAAC, defined in wmcodecdsp.h.</span></span>
</blockquote>
<br/> <span data-ttu-id="418a9-120">Le flux peut contenir des données AAC brutes ou des données AAC dans un flux ADTS (audio Data Transport Stream).</span><span class="sxs-lookup"><span data-stu-id="418a9-120">The stream can contain raw AAC data or AAC data in an Audio Data Transport Stream (ADTS) stream.</span></span><br/> <span data-ttu-id="418a9-121">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="418a9-121">For more information, see:</span></span><br/>
<ul>
<li><span data-ttu-id="418a9-122"><a href="aac-decoder.md"><strong>Décodeur AAC</strong></a></span><span class="sxs-lookup"><span data-stu-id="418a9-122"><a href="aac-decoder.md"><strong>AAC Decoder</strong></a></span></span></li>
<li><span data-ttu-id="418a9-123"><a href="mpeg-4-file-source.md">Source de fichier MPEG-4</a></span><span class="sxs-lookup"><span data-stu-id="418a9-123"><a href="mpeg-4-file-source.md">MPEG-4 File Source</a></span></span></li>
</ul></td>
<td><span data-ttu-id="418a9-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span><span class="sxs-lookup"><span data-stu-id="418a9-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-125"><strong>MFAudioFormat_ADTS</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-125"><strong>MFAudioFormat_ADTS</strong></span></span></td>
<td><span data-ttu-id="418a9-126">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="418a9-126">Not used.</span></span></td>
<td><span data-ttu-id="418a9-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span><span class="sxs-lookup"><span data-stu-id="418a9-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-128"><strong>MFAudioFormat_ALAC</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-128"><strong>MFAudioFormat_ALAC</strong></span></span></td>
<td><span data-ttu-id="418a9-129">Codec audio Apple sans perte</span><span class="sxs-lookup"><span data-stu-id="418a9-129">Apple Lossless Audio Codec</span></span><br/> <span data-ttu-id="418a9-130">Pris en charge dans Windows 10 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="418a9-130">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="418a9-131">WAVE_FORMAT_ALAC (0x6C61)</span><span class="sxs-lookup"><span data-stu-id="418a9-131">WAVE_FORMAT_ALAC (0x6C61)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-132"><strong>MFAudioFormat_AMR_NB</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-132"><strong>MFAudioFormat_AMR_NB</strong></span></span></td>
<td><span data-ttu-id="418a9-133">Adaptative audio à plusieurs débits</span><span class="sxs-lookup"><span data-stu-id="418a9-133">Adaptative Multi-Rate audio</span></span><br/> <span data-ttu-id="418a9-134">Pris en charge dans Windows 8.1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="418a9-134">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="418a9-135">WAVE_FORMAT_AMR_NB</span><span class="sxs-lookup"><span data-stu-id="418a9-135">WAVE_FORMAT_AMR_NB</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-136"><strong>MFAudioFormat_AMR_WB</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-136"><strong>MFAudioFormat_AMR_WB</strong></span></span></td>
<td><span data-ttu-id="418a9-137">Adaptative audio à large bande à débit multiple</span><span class="sxs-lookup"><span data-stu-id="418a9-137">Adaptative Multi-Rate Wideband audio</span></span><br/> <span data-ttu-id="418a9-138">Pris en charge dans Windows 8.1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="418a9-138">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="418a9-139">WAVE_FORMAT_AMR_WB</span><span class="sxs-lookup"><span data-stu-id="418a9-139">WAVE_FORMAT_AMR_WB</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-140"><strong>MFAudioFormat_AMR_WP</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-140"><strong>MFAudioFormat_AMR_WP</strong></span></span></td>
<td><span data-ttu-id="418a9-141">Pris en charge dans Windows 8.1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="418a9-141">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="418a9-142">WAVE_FORMAT_AMR_WP</span><span class="sxs-lookup"><span data-stu-id="418a9-142">WAVE_FORMAT_AMR_WP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-143"><strong>MFAudioFormat_Dolby_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-143"><strong>MFAudioFormat_Dolby_AC3</strong></span></span></td>
<td><span data-ttu-id="418a9-144">Dolby Digital (AC-3).</span><span class="sxs-lookup"><span data-stu-id="418a9-144">Dolby Digital (AC-3).</span></span><br/> <span data-ttu-id="418a9-145">Même valeur GUID que <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, qui est définie dans ksuuids. h</span><span class="sxs-lookup"><span data-stu-id="418a9-145">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, which is defined in ksuuids.h</span></span><br/></td>
<td><span data-ttu-id="418a9-146">Aucun</span><span class="sxs-lookup"><span data-stu-id="418a9-146">None.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span></span></td>
<td><span data-ttu-id="418a9-148">Audio Dolby AC-3 sur Sony/Philips Digital Interface (S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="418a9-148">Dolby AC-3 audio over Sony/Philips Digital Interface (S/PDIF).</span></span><br/> <span data-ttu-id="418a9-149">Cette valeur GUID est identique aux sous-types suivants :</span><span class="sxs-lookup"><span data-stu-id="418a9-149">This GUID value is identical to the following subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="418a9-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, défini dans ksmedia. h.</span><span class="sxs-lookup"><span data-stu-id="418a9-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, defined in ksmedia.h.</span></span></li>
<li><span data-ttu-id="418a9-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, défini dans UUID. h.</span><span class="sxs-lookup"><span data-stu-id="418a9-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, defined in uuids.h.</span></span></li>
</ul></td>
<td><span data-ttu-id="418a9-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span><span class="sxs-lookup"><span data-stu-id="418a9-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span></span></td>
<td><span data-ttu-id="418a9-154">Dolby Digital plus.</span><span class="sxs-lookup"><span data-stu-id="418a9-154">Dolby Digital Plus.</span></span><br/> <span data-ttu-id="418a9-155">Même valeur GUID que <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, qui est définie dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="418a9-155">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, which is defined in wmcodecdsp.h.</span></span><br/></td>
<td><span data-ttu-id="418a9-156">Aucun</span><span class="sxs-lookup"><span data-stu-id="418a9-156">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-157"><strong>MFAudioFormat_DRM</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-157"><strong>MFAudioFormat_DRM</strong></span></span></td>
<td><span data-ttu-id="418a9-158">Données audio chiffrées utilisées avec un chemin d’accès audio sécurisé.</span><span class="sxs-lookup"><span data-stu-id="418a9-158">Encrypted audio data used with secure audio path.</span></span></td>
<td><span data-ttu-id="418a9-159">WAVE_FORMAT_DRM (0x0009)</span><span class="sxs-lookup"><span data-stu-id="418a9-159">WAVE_FORMAT_DRM (0x0009)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-160"><strong>MFAudioFormat_DTS</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-160"><strong>MFAudioFormat_DTS</strong></span></span></td>
<td><span data-ttu-id="418a9-161">Audio Digital Theater Systems (DTS).</span><span class="sxs-lookup"><span data-stu-id="418a9-161">Digital Theater Systems (DTS) audio.</span></span></td>
<td><span data-ttu-id="418a9-162">WAVE_FORMAT_DTS (0x0008)</span><span class="sxs-lookup"><span data-stu-id="418a9-162">WAVE_FORMAT_DTS (0x0008)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-163"><strong>MFAudioFormat_FLAC</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-163"><strong>MFAudioFormat_FLAC</strong></span></span></td>
<td><span data-ttu-id="418a9-164">Codec audio sans perte gratuit</span><span class="sxs-lookup"><span data-stu-id="418a9-164">Free Lossless Audio Codec</span></span><br/> <span data-ttu-id="418a9-165">Pris en charge dans Windows 10 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="418a9-165">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="418a9-166">WAVE_FORMAT_FLAC (0xF1AC)</span><span class="sxs-lookup"><span data-stu-id="418a9-166">WAVE_FORMAT_FLAC (0xF1AC)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-167"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-167"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="418a9-168">Audio à virgule flottante IEEE non compressé.</span><span class="sxs-lookup"><span data-stu-id="418a9-168">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="418a9-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span><span class="sxs-lookup"><span data-stu-id="418a9-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span></span></td>
<td><span data-ttu-id="418a9-171">Audio à virgule flottante IEEE non compressé.</span><span class="sxs-lookup"><span data-stu-id="418a9-171">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="418a9-172">Aucun</span><span class="sxs-lookup"><span data-stu-id="418a9-172">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-173"><strong>MFAudioFormat_MP3</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-173"><strong>MFAudioFormat_MP3</strong></span></span></td>
<td><span data-ttu-id="418a9-174">MPEG Audio Layer-3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="418a9-174">MPEG Audio Layer-3 (MP3).</span></span></td>
<td><span data-ttu-id="418a9-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span><span class="sxs-lookup"><span data-stu-id="418a9-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-176"><strong>MFAudioFormat_MPEG</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-176"><strong>MFAudioFormat_MPEG</strong></span></span></td>
<td><span data-ttu-id="418a9-177">Charge utile MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="418a9-177">MPEG-1 audio payload.</span></span></td>
<td><span data-ttu-id="418a9-178">WAVE_FORMAT_MPEG (0x0050)</span><span class="sxs-lookup"><span data-stu-id="418a9-178">WAVE_FORMAT_MPEG (0x0050)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-179"><strong>MFAudioFormat_MSP1</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-179"><strong>MFAudioFormat_MSP1</strong></span></span></td>
<td><span data-ttu-id="418a9-180">Codec vocal Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="418a9-180">Windows Media Audio 9 Voice codec.</span></span></td>
<td><span data-ttu-id="418a9-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span><span class="sxs-lookup"><span data-stu-id="418a9-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-182"><strong>MFAudioFormat_Opus</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-182"><strong>MFAudioFormat_Opus</strong></span></span></td>
<td><span data-ttu-id="418a9-183">Opus</span><span class="sxs-lookup"><span data-stu-id="418a9-183">Opus</span></span><br/> <span data-ttu-id="418a9-184">Pris en charge dans Windows 10 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="418a9-184">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="418a9-185">WAVE_FORMAT_OPUS (0x704F)</span><span class="sxs-lookup"><span data-stu-id="418a9-185">WAVE_FORMAT_OPUS (0x704F)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-186"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-186"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="418a9-187">Audio PCM non compressé.</span><span class="sxs-lookup"><span data-stu-id="418a9-187">Uncompressed PCM audio.</span></span></td>
<td><span data-ttu-id="418a9-188">WAVE_FORMAT_PCM (1)</span><span class="sxs-lookup"><span data-stu-id="418a9-188">WAVE_FORMAT_PCM (1)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-189"><strong>MFAudioFormat_QCELP</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-189"><strong>MFAudioFormat_QCELP</strong></span></span></td>
<td><span data-ttu-id="418a9-190">QCELP (code Qualcomm avec prédiction linéaire incorrecte).</span><span class="sxs-lookup"><span data-stu-id="418a9-190">QCELP (Qualcomm Code Excited Linear Prediction) audio.</span></span></td>
<td><span data-ttu-id="418a9-191">Aucun</span><span class="sxs-lookup"><span data-stu-id="418a9-191">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-192"><strong>MFAudioFormat_WMASPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-192"><strong>MFAudioFormat_WMASPDIF</strong></span></span></td>
<td><span data-ttu-id="418a9-193">Codec Windows Media Audio 9 Professional sur S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="418a9-193">Windows Media Audio 9 Professional codec over S/PDIF.</span></span></td>
<td><span data-ttu-id="418a9-194">WAVE_FORMAT_WMASPDIF (0x0164)</span><span class="sxs-lookup"><span data-stu-id="418a9-194">WAVE_FORMAT_WMASPDIF (0x0164)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span></span></td>
<td><span data-ttu-id="418a9-196">Codec Windows Media Audio 9 Lossless ou Windows Media Audio Codec 9,1.</span><span class="sxs-lookup"><span data-stu-id="418a9-196">Windows Media Audio 9 Lossless codec or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="418a9-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span><span class="sxs-lookup"><span data-stu-id="418a9-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="418a9-198"><strong>MFAudioFormat_WMAudioV8</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-198"><strong>MFAudioFormat_WMAudioV8</strong></span></span></td>
<td><span data-ttu-id="418a9-199">Codec Windows Media Audio 8, Windows Media Audio 9 codec ou Windows Media Audio Codec 9,1.</span><span class="sxs-lookup"><span data-stu-id="418a9-199">Windows Media Audio 8 codec, Windows Media Audio 9 codec, or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="418a9-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span><span class="sxs-lookup"><span data-stu-id="418a9-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="418a9-201"><strong>MFAudioFormat_WMAudioV9</strong></span><span class="sxs-lookup"><span data-stu-id="418a9-201"><strong>MFAudioFormat_WMAudioV9</strong></span></span></td>
<td><span data-ttu-id="418a9-202">Codec Windows Media Audio 9 Professional ou Windows Media Audio Codec professionnel 9,1.</span><span class="sxs-lookup"><span data-stu-id="418a9-202">Windows Media Audio 9 Professional codec or Windows Media Audio 9.1 Professional codec.</span></span></td>
<td><span data-ttu-id="418a9-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span><span class="sxs-lookup"><span data-stu-id="418a9-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="418a9-204">Les balises de format répertoriées dans la troisième colonne de cette table sont utilisées dans la structure **WAVEFORMATEX** , et sont définies dans le fichier d’en-tête mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="418a9-204">The format tags listed in the third column of this table are used in the **WAVEFORMATEX** structure, and are defined in the header file mmreg.h.</span></span>

<span data-ttu-id="418a9-205">Pour une balise de format audio donnée, vous pouvez créer un GUID de sous-type audio comme suit :</span><span class="sxs-lookup"><span data-stu-id="418a9-205">Given an audio format tag, you can create an audio subtype GUID as follows:</span></span>

1.  <span data-ttu-id="418a9-206">Commencez par la valeur **MFAudioFormat \_ base**, qui est définie dans mfaph. i.</span><span class="sxs-lookup"><span data-stu-id="418a9-206">Start with the value **MFAudioFormat\_Base**, which is defined in mfaph.i.</span></span>
2.  <span data-ttu-id="418a9-207">Remplacez le premier **DWORD** de ce GUID par la balise format.</span><span class="sxs-lookup"><span data-stu-id="418a9-207">Replace the first **DWORD** of this GUID with the format tag.</span></span>

<span data-ttu-id="418a9-208">Vous pouvez utiliser la macro [**définir le \_ \_ GUID du MediaType**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) pour définir une nouvelle constante GUID qui suit ce modèle.</span><span class="sxs-lookup"><span data-stu-id="418a9-208">You can use the [**DEFINE\_MEDIATYPE\_GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) macro to define a new GUID constant that follows this pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="418a9-209">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="418a9-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="418a9-210">Types de média audio</span><span class="sxs-lookup"><span data-stu-id="418a9-210">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="418a9-211">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="418a9-211">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="418a9-212">GUID de type de média</span><span class="sxs-lookup"><span data-stu-id="418a9-212">Media Type GUIDs</span></span>](media-type-guids.md)
</dt> <dt>

[<span data-ttu-id="418a9-213">Types de médias</span><span class="sxs-lookup"><span data-stu-id="418a9-213">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




