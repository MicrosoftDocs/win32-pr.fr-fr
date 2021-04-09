---
description: Microsoft Media Foundation.
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: Encodeur audio MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea2b22d2fe8cd51f9a2990970493e0415f34d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034159"
---
# <a name="mp3-audio-encoder"></a><span data-ttu-id="e2a1b-103">Encodeur audio MP3</span><span class="sxs-lookup"><span data-stu-id="e2a1b-103">MP3 Audio Encoder</span></span>

<span data-ttu-id="e2a1b-104">L’encodeur audio MP3 Microsoft Media Foundation est une [transformation de Media Foundation](media-foundation-transforms.md) (MFT) qui encode le contenu audio MPEG-1 (MP3).</span><span class="sxs-lookup"><span data-stu-id="e2a1b-104">The Microsoft Media Foundation MP3 audio encoder is a [Media Foundation Transform](media-foundation-transforms.md) (MFT) that encodes MPEG-1 layer 3 (MP3) audio.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="e2a1b-105">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="e2a1b-105">Class Identifier</span></span>

<span data-ttu-id="e2a1b-106">L’identificateur de classe (CLSID) de l’encodeur MP3 est **CLSID \_ MP3ACMCodecWrapper**, défini dans le fichier d’en-tête wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-106">The class identifier (CLSID) of the MP3 encoder is **CLSID\_MP3ACMCodecWrapper**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="e2a1b-107">Types de médias</span><span class="sxs-lookup"><span data-stu-id="e2a1b-107">Media Types</span></span>

<span data-ttu-id="e2a1b-108">L’encodeur MP3 prend en charge les types de média suivants.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-108">The MP3 encoder supports the following media types.</span></span> <span data-ttu-id="e2a1b-109">Le type de sortie doit être défini avant le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-109">The output type must be set before the input type.</span></span>

### <a name="output-types"></a><span data-ttu-id="e2a1b-110">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="e2a1b-110">Output Types</span></span>

<span data-ttu-id="e2a1b-111">Définissez les attributs suivants sur le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-111">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e2a1b-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="e2a1b-112">Attribute</span></span></th>
<th><span data-ttu-id="e2a1b-113">Description</span><span class="sxs-lookup"><span data-stu-id="e2a1b-113">Description</span></span></th>
<th><span data-ttu-id="e2a1b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e2a1b-114">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e2a1b-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2a1b-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="e2a1b-116">Type principal.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-116">Major type.</span></span></td>
<td><span data-ttu-id="e2a1b-117">Doit être <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-117">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2a1b-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2a1b-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="e2a1b-119">Sous-type audio.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-119">Audio subtype.</span></span></td>
<td><span data-ttu-id="e2a1b-120">Doit être <strong>MFAudioFormat_MP3</strong>.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-120">Must be <strong>MFAudioFormat_MP3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2a1b-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2a1b-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="e2a1b-122">Vitesse de transmission du flux MP3 encodé, en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-122">Bit rate of the encoded MP3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="e2a1b-123">L’encodeur prend en charge toutes les vitesses de transmission définies par la norme (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256 ou 320 Kbits/s).</span><span class="sxs-lookup"><span data-stu-id="e2a1b-123">The encoder supports all bit rates defined by the standard (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, or 320 Kbps).</span></span><br/> <span data-ttu-id="e2a1b-124">Les vitesses de transmission par défaut sont de 128 Kbits/s pour mono et 320 kbps pour le stéréo.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-124">The default bit rates are 128 Kbps for mono and 320 Kbps for stereo.</span></span><br/> <span data-ttu-id="e2a1b-125">Utilisez cet attribut pour spécifier la vitesse de transmission encodée.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-125">Use this attribute to specify the encoded bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2a1b-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2a1b-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="e2a1b-127">Nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-127">Number of channels.</span></span></td>
<td><span data-ttu-id="e2a1b-128">Les valeurs suivantes sont admises :</span><span class="sxs-lookup"><span data-stu-id="e2a1b-128">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="e2a1b-129">1 (mono)</span><span class="sxs-lookup"><span data-stu-id="e2a1b-129">1 (mono)</span></span></li>
<li><span data-ttu-id="e2a1b-130">2 (stéréo)</span><span class="sxs-lookup"><span data-stu-id="e2a1b-130">2 (stereo)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2a1b-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2a1b-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="e2a1b-132">Échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-132">Samples per second.</span></span></td>
<td><span data-ttu-id="e2a1b-133">Les valeurs suivantes sont admises :</span><span class="sxs-lookup"><span data-stu-id="e2a1b-133">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="e2a1b-134">48000 (48 KHz)</span><span class="sxs-lookup"><span data-stu-id="e2a1b-134">48000 (48 KHz)</span></span></li>
<li><span data-ttu-id="e2a1b-135">44100 (44,1 KHz)</span><span class="sxs-lookup"><span data-stu-id="e2a1b-135">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="e2a1b-136">32000 (32 KHz)</span><span class="sxs-lookup"><span data-stu-id="e2a1b-136">32000 (32 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2a1b-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span><span class="sxs-lookup"><span data-stu-id="e2a1b-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span></span></td>
<td><span data-ttu-id="e2a1b-138">Données de codec supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-138">Additional codec data.</span></span></td>
<td><span data-ttu-id="e2a1b-139">Cet attribut contient les 12 octets de la structure <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> qui suivent le membre <strong>wfx</strong> de cette structure.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-139">This attribute contains the 12 bytes of the <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> structure that follow the <strong>wfx</strong> member of that structure.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e2a1b-140">Vous pouvez également remplir une structure [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) et appeler [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) pour convertir la structure en un type de média Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-140">Alternatively, you can fill in an [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure and call [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) to convert the structure to a Media Foundation media type.</span></span>

### <a name="input-types"></a><span data-ttu-id="e2a1b-141">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="e2a1b-141">Input Types</span></span>

<span data-ttu-id="e2a1b-142">Définissez les attributs suivants sur le type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-142">Set the following attributes on the input media type.</span></span>



| <span data-ttu-id="e2a1b-143">Attribut</span><span class="sxs-lookup"><span data-stu-id="e2a1b-143">Attribute</span></span>                                                                               | <span data-ttu-id="e2a1b-144">Description</span><span class="sxs-lookup"><span data-stu-id="e2a1b-144">Description</span></span>         | <span data-ttu-id="e2a1b-145">Notes</span><span class="sxs-lookup"><span data-stu-id="e2a1b-145">Remarks</span></span>                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [<span data-ttu-id="e2a1b-146">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e2a1b-146">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="e2a1b-147">Type principal.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-147">Major type.</span></span>         | <span data-ttu-id="e2a1b-148">Doit être **MFMediaType \_ audio**.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-148">Must be **MFMediaType\_Audio**.</span></span> |
| [<span data-ttu-id="e2a1b-149">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="e2a1b-149">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="e2a1b-150">Sous-type.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-150">Subtype.</span></span>            | <span data-ttu-id="e2a1b-151">Doit être **MFAudioFormat \_ PCM**.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-151">Must be **MFAudioFormat\_PCM**.</span></span> |
| [<span data-ttu-id="e2a1b-152">**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**</span><span class="sxs-lookup"><span data-stu-id="e2a1b-152">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="e2a1b-153">Bits par échantillon.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-153">Bits per sample.</span></span>    | <span data-ttu-id="e2a1b-154">Doit être 16.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-154">Must be 16.</span></span>                     |
| [<span data-ttu-id="e2a1b-155">**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="e2a1b-155">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="e2a1b-156">Échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-156">Samples per second.</span></span> | <span data-ttu-id="e2a1b-157">Doit correspondre au type de sortie.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-157">Must match the output type.</span></span>     |
| [<span data-ttu-id="e2a1b-158">**\_canaux de \_ \_ numéros audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e2a1b-158">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="e2a1b-159">Nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-159">Number of channels.</span></span> | <span data-ttu-id="e2a1b-160">Doit correspondre au type de sortie.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-160">Must match the output type.</span></span>     |



 

<span data-ttu-id="e2a1b-161">L’encodeur prend en charge uniquement l’entrée PCM de type entier 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-161">The encoder supports only 16-bit integer PCM input.</span></span> <span data-ttu-id="e2a1b-162">Elle ne prend pas en charge l’entrée à virgule flottante 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-162">It does not support 32-bit floating point input.</span></span>

### <a name="media-formats"></a><span data-ttu-id="e2a1b-163">Formats multimédias</span><span class="sxs-lookup"><span data-stu-id="e2a1b-163">Media Formats</span></span>

<span data-ttu-id="e2a1b-164">La norme MPEG-1 et MPEG-2 définit des formats audio de couche 3 252.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-164">The MPEG-1 and MPEG-2 standard defines 252 layer 3 audio formats.</span></span> <span data-ttu-id="e2a1b-165">L’encodeur MP3 prend en charge la norme avec quelques exceptions, ainsi que certains formats supplémentaires, comme décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-165">The MP3 encoder supports the standard with some exceptions, as well as some additional formats, as described below.</span></span> <span data-ttu-id="e2a1b-166">La couche 3 est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="e2a1b-166">Layer 3 is defined as:</span></span>



| <span data-ttu-id="e2a1b-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2a1b-167">Requirement</span></span> | <span data-ttu-id="e2a1b-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2a1b-168">Value</span></span> |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e2a1b-169">Canaux</span><span class="sxs-lookup"><span data-stu-id="e2a1b-169">Channels</span></span>                         | <span data-ttu-id="e2a1b-170">mono ou stéréo</span><span class="sxs-lookup"><span data-stu-id="e2a1b-170">mono or stereo</span></span>                                                |
| <span data-ttu-id="e2a1b-171">Taux d’échantillonnage MPEG-1 en kHz</span><span class="sxs-lookup"><span data-stu-id="e2a1b-171">MPEG-1 sample rates in kHz</span></span>       | <span data-ttu-id="e2a1b-172">44,1, 48, 32</span><span class="sxs-lookup"><span data-stu-id="e2a1b-172">44.1, 48, 32</span></span>                                                  |
| <span data-ttu-id="e2a1b-173">Débits binaires encodés MPEG-1 en Kbits/s</span><span class="sxs-lookup"><span data-stu-id="e2a1b-173">MPEG-1 encoded bit rates in kbps</span></span> | <span data-ttu-id="e2a1b-174">32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320</span><span class="sxs-lookup"><span data-stu-id="e2a1b-174">32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320</span></span> |
| <span data-ttu-id="e2a1b-175">Taux d’échantillonnage MPEG-2 en kHz</span><span class="sxs-lookup"><span data-stu-id="e2a1b-175">MPEG-2 sample rates in kHz</span></span>       | <span data-ttu-id="e2a1b-176">8, 11,025, 12, 16, 22,05, 24</span><span class="sxs-lookup"><span data-stu-id="e2a1b-176">8, 11.025, 12, 16, 22.05, 24</span></span>                                  |
| <span data-ttu-id="e2a1b-177">Débits binaires encodés MPEG-2 en Kbits/s</span><span class="sxs-lookup"><span data-stu-id="e2a1b-177">MPEG-2 encoded bit rates in kbps</span></span> | <span data-ttu-id="e2a1b-178">8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160</span><span class="sxs-lookup"><span data-stu-id="e2a1b-178">8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160</span></span>          |



 

<span data-ttu-id="e2a1b-179">L’encodeur MP3 prend également en charge les formats suivants.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-179">The MP3 encoder also supports the following formats.</span></span>



| <span data-ttu-id="e2a1b-180">Échantillonnage</span><span class="sxs-lookup"><span data-stu-id="e2a1b-180">Sample Rate</span></span> | <span data-ttu-id="e2a1b-181">Vitesse de transmission</span><span class="sxs-lookup"><span data-stu-id="e2a1b-181">Bit Rate</span></span>     | <span data-ttu-id="e2a1b-182">Numéro de canal</span><span class="sxs-lookup"><span data-stu-id="e2a1b-182">Channel Number</span></span> |
|-------------|--------------|----------------|
| <span data-ttu-id="e2a1b-183">8000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-183">8000</span></span>        | <span data-ttu-id="e2a1b-184">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-184">18000, 20000</span></span> | <span data-ttu-id="e2a1b-185">2</span><span class="sxs-lookup"><span data-stu-id="e2a1b-185">2</span></span>              |
| <span data-ttu-id="e2a1b-186">11025</span><span class="sxs-lookup"><span data-stu-id="e2a1b-186">11025</span></span>       | <span data-ttu-id="e2a1b-187">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-187">18000, 20000</span></span> | <span data-ttu-id="e2a1b-188">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="e2a1b-188">1 or 2</span></span>         |
| <span data-ttu-id="e2a1b-189">12 000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-189">12000</span></span>       | <span data-ttu-id="e2a1b-190">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-190">18000, 20000</span></span> | <span data-ttu-id="e2a1b-191">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="e2a1b-191">1 or 2</span></span>         |
| <span data-ttu-id="e2a1b-192">16000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-192">16000</span></span>       | <span data-ttu-id="e2a1b-193">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-193">18000, 20000</span></span> | <span data-ttu-id="e2a1b-194">1</span><span class="sxs-lookup"><span data-stu-id="e2a1b-194">1</span></span>              |
| <span data-ttu-id="e2a1b-195">32000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-195">32000</span></span>       | <span data-ttu-id="e2a1b-196">144000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-196">144000</span></span>       | <span data-ttu-id="e2a1b-197">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="e2a1b-197">1 or 2</span></span>         |
| <span data-ttu-id="e2a1b-198">44100</span><span class="sxs-lookup"><span data-stu-id="e2a1b-198">44100</span></span>       | <span data-ttu-id="e2a1b-199">144000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-199">144000</span></span>       | <span data-ttu-id="e2a1b-200">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="e2a1b-200">1 or 2</span></span>         |
| <span data-ttu-id="e2a1b-201">48 000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-201">48000</span></span>       | <span data-ttu-id="e2a1b-202">144000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-202">144000</span></span>       | <span data-ttu-id="e2a1b-203">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="e2a1b-203">1 or 2</span></span>         |



 

<span data-ttu-id="e2a1b-204">L’encodeur MP3 ne prend pas en charge les formats suivants définis par la norme.</span><span class="sxs-lookup"><span data-stu-id="e2a1b-204">The MP3 encoder does not support the following formats defined by the standard.</span></span>



| <span data-ttu-id="e2a1b-205">Échantillonnage</span><span class="sxs-lookup"><span data-stu-id="e2a1b-205">Sample Rate</span></span> | <span data-ttu-id="e2a1b-206">Vitesses de transmission</span><span class="sxs-lookup"><span data-stu-id="e2a1b-206">Bit Rates</span></span>                                    | <span data-ttu-id="e2a1b-207">Numéro de canal</span><span class="sxs-lookup"><span data-stu-id="e2a1b-207">Channel Number</span></span> |
|-------------|----------------------------------------------|----------------|
| <span data-ttu-id="e2a1b-208">12 000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-208">12000</span></span>       | <span data-ttu-id="e2a1b-209">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-209">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="e2a1b-210">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="e2a1b-210">1 or 2</span></span>         |
| <span data-ttu-id="e2a1b-211">11025</span><span class="sxs-lookup"><span data-stu-id="e2a1b-211">11025</span></span>       | <span data-ttu-id="e2a1b-212">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-212">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="e2a1b-213">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="e2a1b-213">1 or 2</span></span>         |
| <span data-ttu-id="e2a1b-214">8000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-214">8000</span></span>        | <span data-ttu-id="e2a1b-215">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-215">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="e2a1b-216">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="e2a1b-216">1 or 2</span></span>         |
| <span data-ttu-id="e2a1b-217">8000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-217">8000</span></span>        | <span data-ttu-id="e2a1b-218">8000, 11025, 12000, 16000, 22050, 24000</span><span class="sxs-lookup"><span data-stu-id="e2a1b-218">8000, 11025, 12000, 16000, 22050, 24000</span></span>      | <span data-ttu-id="e2a1b-219">2</span><span class="sxs-lookup"><span data-stu-id="e2a1b-219">2</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="e2a1b-220">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2a1b-220">Requirements</span></span>



| <span data-ttu-id="e2a1b-221">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2a1b-221">Requirement</span></span> | <span data-ttu-id="e2a1b-222">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2a1b-222">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2a1b-223">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2a1b-223">Minimum supported client</span></span><br/> | <span data-ttu-id="e2a1b-224">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2a1b-224">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="e2a1b-225">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2a1b-225">Minimum supported server</span></span><br/> | <span data-ttu-id="e2a1b-226">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2a1b-226">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2a1b-227">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2a1b-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a1b-228">Objets codec</span><span class="sxs-lookup"><span data-stu-id="e2a1b-228">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
