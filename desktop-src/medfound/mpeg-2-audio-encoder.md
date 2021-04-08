---
description: L’encodeur audio Microsoft Media Foundation MPEG-2 est une transformation de Media Foundation qui encode le contenu audio mono ou stéréo en MPEG-1 audio (ISO/IEC 11172-3) ou MPEG-2 audio (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Encodeur audio MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863422"
---
# <a name="mpeg-2-audio-encoder"></a><span data-ttu-id="4630c-103">Encodeur audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4630c-103">MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="4630c-104">L’encodeur audio Microsoft Media Foundation MPEG-2 est une [transformation de Media Foundation](media-foundation-transforms.md) qui encode le contenu audio mono ou stéréo en MPEG-1 audio (ISO/IEC 11172-3) ou MPEG-2 audio (ISO/IEC 13818-3).</span><span class="sxs-lookup"><span data-stu-id="4630c-104">The Microsoft Media Foundation MPEG-2 audio encoder is a [Media Foundation transform](media-foundation-transforms.md) that encodes mono or stereo audio to MPEG-1 audio (ISO/IEC 11172-3) or MPEG-2 audio (ISO/IEC 13818-3).</span></span>

<span data-ttu-id="4630c-105">L’encodeur prend en charge les données audio de couche 1 et 2.</span><span class="sxs-lookup"><span data-stu-id="4630c-105">The encoder supports Layer 1 and Layer 2 audio.</span></span> <span data-ttu-id="4630c-106">Il ne prend pas en charge le format audio MPEG-Layer 3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="4630c-106">It does not support MPEG-Layer 3 (MP3) audio.</span></span> <span data-ttu-id="4630c-107">Pour MPEG-2, l’encodeur prend en charge la partie basse fréquence d’échantillonnage (LSF) de l’audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="4630c-107">For MPEG-2, the encoder supports the Low Sampling Frequencies (LSF) portion of MPEG-2 audio.</span></span> <span data-ttu-id="4630c-108">Elle ne prend pas en charge les extensions multicanaux.</span><span class="sxs-lookup"><span data-stu-id="4630c-108">It does not support the multichannel extensions.</span></span> <span data-ttu-id="4630c-109">La table MFT génère un flux élémentaire MPEG.</span><span class="sxs-lookup"><span data-stu-id="4630c-109">The MFT outputs an MPEG elementary stream.</span></span> <span data-ttu-id="4630c-110">Il ne peut pas générer des flux élémentaires, des flux de programmes ou des flux de transport de paquets.</span><span class="sxs-lookup"><span data-stu-id="4630c-110">It cannot generate packetized elementary streams, program streams, or transport streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="4630c-111">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="4630c-111">Class Identifier</span></span>

<span data-ttu-id="4630c-112">L’identificateur de classe (CLSID) de l’encodeur audio MEPG-2 est **CLSID \_ CMPEG2AudioEncoderMFT**, défini dans le fichier d’en-tête wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="4630c-112">The class identifier (CLSID) of the MEPG-2 audio encoder is **CLSID\_CMPEG2AudioEncoderMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="4630c-113">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="4630c-113">Output Types</span></span>

<span data-ttu-id="4630c-114">Le type de sortie doit être défini en premier, avant le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4630c-114">The output type must be set first, before the input type.</span></span> <span data-ttu-id="4630c-115">Le tableau suivant répertorie les attributs obligatoires et facultatifs pour le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="4630c-115">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4630c-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="4630c-116">Attribute</span></span></th>
<th><span data-ttu-id="4630c-117">Description</span><span class="sxs-lookup"><span data-stu-id="4630c-117">Description</span></span></th>
<th><span data-ttu-id="4630c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4630c-118">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4630c-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="4630c-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="4630c-120">Type principal.</span><span class="sxs-lookup"><span data-stu-id="4630c-120">Major type.</span></span></td>
<td><span data-ttu-id="4630c-121">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4630c-121">Required.</span></span> <span data-ttu-id="4630c-122">Doit être <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="4630c-122">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4630c-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="4630c-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="4630c-124">Sous-type audio.</span><span class="sxs-lookup"><span data-stu-id="4630c-124">Audio subtype.</span></span></td>
<td><span data-ttu-id="4630c-125">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4630c-125">Required.</span></span> <span data-ttu-id="4630c-126">Doit être <strong>MFAudioFormat_MPEG</strong>.</span><span class="sxs-lookup"><span data-stu-id="4630c-126">Must be <strong>MFAudioFormat_MPEG</strong>.</span></span> <span data-ttu-id="4630c-127">Ce sous-type est utilisé pour MPEG-1 et MPEG-2 audio.</span><span class="sxs-lookup"><span data-stu-id="4630c-127">This subtype is used for both MPEG-1 and MPEG-2 audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4630c-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="4630c-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="4630c-129">Échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="4630c-129">Samples per second.</span></span></td>
<td><span data-ttu-id="4630c-130">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4630c-130">Required.</span></span> <span data-ttu-id="4630c-131">Les valeurs suivantes sont prises en charge pour MPEG-1 et MPEG-2 :</span><span class="sxs-lookup"><span data-stu-id="4630c-131">The following values are supported for both MPEG-1 and MPEG-2:</span></span>
<ul>
<li><span data-ttu-id="4630c-132">32000</span><span class="sxs-lookup"><span data-stu-id="4630c-132">32000</span></span></li>
<li><span data-ttu-id="4630c-133">44100</span><span class="sxs-lookup"><span data-stu-id="4630c-133">44100</span></span></li>
<li><span data-ttu-id="4630c-134">48 000</span><span class="sxs-lookup"><span data-stu-id="4630c-134">48000</span></span></li>
</ul>
<span data-ttu-id="4630c-135">En outre, les valeurs suivantes sont prises en charge pour MPEG-2 LSF :</span><span class="sxs-lookup"><span data-stu-id="4630c-135">In addition, the following values are supported for MPEG-2 LSF:</span></span> <br/>
<ul>
<li><span data-ttu-id="4630c-136">16000</span><span class="sxs-lookup"><span data-stu-id="4630c-136">16000</span></span></li>
<li><span data-ttu-id="4630c-137">22050</span><span class="sxs-lookup"><span data-stu-id="4630c-137">22050</span></span></li>
<li><span data-ttu-id="4630c-138">24 000</span><span class="sxs-lookup"><span data-stu-id="4630c-138">24000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4630c-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="4630c-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="4630c-140">Nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="4630c-140">Number of channels.</span></span></td>
<td><span data-ttu-id="4630c-141">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4630c-141">Required.</span></span> <span data-ttu-id="4630c-142">Doit avoir la valeur 1 (mono) ou 2 (stéréo).</span><span class="sxs-lookup"><span data-stu-id="4630c-142">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4630c-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="4630c-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="4630c-144">Spécifie l’affectation des canaux audio aux positions des haut-parleurs.</span><span class="sxs-lookup"><span data-stu-id="4630c-144">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="4630c-145">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4630c-145">Optional.</span></span> <span data-ttu-id="4630c-146">S’il est défini, la valeur doit être 0x3 pour les canaux stéréo (avant gauche et droit) ou 0x4 pour mono (canal avant centre).</span><span class="sxs-lookup"><span data-stu-id="4630c-146">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4630c-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="4630c-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="4630c-148">Vitesse de transmission du flux MPEG encodé, en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="4630c-148">Bit rate of the encoded MPEG stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="4630c-149">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4630c-149">Optional.</span></span><br/> <span data-ttu-id="4630c-150">Les spécifications ISO/IEC 11172-3 et ISO/IEC 13818-3 (LSF) définissent plusieurs vitesses de transmission, en fonction de la fréquence d’échantillonnage, du nombre de canaux et de la couche audio (1 ou 2).</span><span class="sxs-lookup"><span data-stu-id="4630c-150">The ISO/IEC 11172-3 and ISO/IEC 13818-3 (LSF) specifications define several bit rates, depending on the sampling rate, the number of channels, and the audio layer (1 or 2).</span></span> <br/> <span data-ttu-id="4630c-151">L’encodeur est défini par défaut sur audio de couche 2.</span><span class="sxs-lookup"><span data-stu-id="4630c-151">The encoder defaults to Layer 2 audio.</span></span> <span data-ttu-id="4630c-152">Si l’attribut <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> n’est pas défini, l’encodeur utilise les vitesses de transmission par défaut suivantes :</span><span class="sxs-lookup"><span data-stu-id="4630c-152">If the <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> attribute is not set, the encoder uses the following default bit rates:</span></span><br/>
<ul>
<li><span data-ttu-id="4630c-153">Stéréo MPEG-1:224 000 bits par seconde (BPS) = 28 000 octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="4630c-153">MPEG-1 stereo: 224,000 bits per second (bps) = 28,000 bytes per second.</span></span></li>
<li><span data-ttu-id="4630c-154">MPEG-1 mono : 192 000 BPS = 24 000 octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="4630c-154">MPEG-1 mono: 192,000 bps = 24,000 bytes per second.</span></span></li>
<li><span data-ttu-id="4630c-155">MPEG-2 LSF, mono ou stéréo : 160 000 BPS = 20 000 octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="4630c-155">MPEG-2 LSF, mono or stereo: 160,000 bps = 20,000 bytes per second.</span></span></li>
</ul>
<span data-ttu-id="4630c-156">Cet attribut peut être défini sur d’autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="4630c-156">This attribute can be set to other values.</span></span> <span data-ttu-id="4630c-157">Si la valeur n’est pas valide conformément aux spécifications MPEG, la table MFT rejette le type de média.</span><span class="sxs-lookup"><span data-stu-id="4630c-157">If the value is not valid according to MPEG specifications, the MFT will reject the media type.</span></span><br/> <span data-ttu-id="4630c-158">Vous pouvez également définir la vitesse de transmission à l’aide de l’interface <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4630c-158">You can also set the bit rate by using the <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> interface.</span></span> <span data-ttu-id="4630c-159">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="4630c-159">See Remarks for more information.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4630c-160">Si les attributs facultatifs ne sont pas définis, l’encodeur les ajoute au type de média après que le type a été défini.</span><span class="sxs-lookup"><span data-stu-id="4630c-160">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="4630c-161">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="4630c-161">Input Types</span></span>

<span data-ttu-id="4630c-162">Le tableau suivant répertorie les attributs obligatoires et facultatifs pour le type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4630c-162">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4630c-163">Attribut</span><span class="sxs-lookup"><span data-stu-id="4630c-163">Attribute</span></span></th>
<th><span data-ttu-id="4630c-164">Description</span><span class="sxs-lookup"><span data-stu-id="4630c-164">Description</span></span></th>
<th><span data-ttu-id="4630c-165">Notes</span><span class="sxs-lookup"><span data-stu-id="4630c-165">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4630c-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="4630c-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="4630c-167">Type principal.</span><span class="sxs-lookup"><span data-stu-id="4630c-167">Major type.</span></span></td>
<td><span data-ttu-id="4630c-168">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4630c-168">Required.</span></span> <span data-ttu-id="4630c-169">Doit être <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="4630c-169">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4630c-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="4630c-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="4630c-171">Sous-type audio.</span><span class="sxs-lookup"><span data-stu-id="4630c-171">Audio subtype.</span></span></td>
<td><span data-ttu-id="4630c-172">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4630c-172">Required.</span></span> <span data-ttu-id="4630c-173">Doit être <strong>MFAudioFormat_PCM</strong> ou <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="4630c-173">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4630c-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="4630c-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="4630c-175">Nombre de bits par échantillon audio.</span><span class="sxs-lookup"><span data-stu-id="4630c-175">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="4630c-176">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4630c-176">Required.</span></span> <span data-ttu-id="4630c-177">La valeur doit être 16 si le sous-type est <strong>MFAudioFormat_PCM</strong>, ou 32 si le sous-type est <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="4630c-177">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4630c-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="4630c-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="4630c-179">Échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="4630c-179">Samples per second.</span></span></td>
<td><span data-ttu-id="4630c-180">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4630c-180">Required.</span></span> <span data-ttu-id="4630c-181">Doit correspondre au type de sortie.</span><span class="sxs-lookup"><span data-stu-id="4630c-181">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4630c-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="4630c-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="4630c-183">Nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="4630c-183">Number of channels.</span></span></td>
<td><span data-ttu-id="4630c-184">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4630c-184">Required.</span></span> <span data-ttu-id="4630c-185">Doit correspondre au type de sortie.</span><span class="sxs-lookup"><span data-stu-id="4630c-185">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4630c-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="4630c-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="4630c-187">Alignement de bloc, en octets.</span><span class="sxs-lookup"><span data-stu-id="4630c-187">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="4630c-188">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4630c-188">Required.</span></span> <span data-ttu-id="4630c-189">Calculez la valeur comme suit :</span><span class="sxs-lookup"><span data-stu-id="4630c-189">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="4630c-190"><strong>MFAudioFormat_PCM</strong>: nombre de canaux × 2.</span><span class="sxs-lookup"><span data-stu-id="4630c-190"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="4630c-191"><strong>MFAudioFormat_Float</strong>: nombre de canaux × 4.</span><span class="sxs-lookup"><span data-stu-id="4630c-191"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4630c-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="4630c-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="4630c-193">Vitesse de transmission du flux de données AC3 encodé, en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="4630c-193">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="4630c-194">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4630c-194">Required.</span></span> <span data-ttu-id="4630c-195">Doit être égal à alignement de bloc × échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="4630c-195">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4630c-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="4630c-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="4630c-197">Spécifie l’affectation des canaux audio aux positions des haut-parleurs.</span><span class="sxs-lookup"><span data-stu-id="4630c-197">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="4630c-198">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4630c-198">Optional.</span></span> <span data-ttu-id="4630c-199">Si cette valeur est définie, la valeur doit correspondre au type de sortie.</span><span class="sxs-lookup"><span data-stu-id="4630c-199">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4630c-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="4630c-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="4630c-201">Nombre de bits de données audio valides dans chaque exemple audio.</span><span class="sxs-lookup"><span data-stu-id="4630c-201">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="4630c-202">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4630c-202">Optional.</span></span> <span data-ttu-id="4630c-203">Si cette valeur est définie, la valeur doit être identique à <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="4630c-203">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4630c-204">L’encodeur ne prend pas en charge la conversion de taux d’échantillonnage ou la conversion stéréo/mono.</span><span class="sxs-lookup"><span data-stu-id="4630c-204">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span> <span data-ttu-id="4630c-205">Si les attributs facultatifs ne sont pas définis, l’encodeur les ajoute au type de média après que le type a été défini.</span><span class="sxs-lookup"><span data-stu-id="4630c-205">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="4630c-206">Propriétés du codec</span><span class="sxs-lookup"><span data-stu-id="4630c-206">Codec Properties</span></span>

<span data-ttu-id="4630c-207">L’encodeur prend en charge les propriétés suivantes par le biais de l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="4630c-207">The encoder supports the following properties through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>



| <span data-ttu-id="4630c-208">Propriété</span><span class="sxs-lookup"><span data-stu-id="4630c-208">Property</span></span>                                                                                | <span data-ttu-id="4630c-209">Description</span><span class="sxs-lookup"><span data-stu-id="4630c-209">Description</span></span>                                                                                      | <span data-ttu-id="4630c-210">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="4630c-210">Default value</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4630c-211">CODECAPI \_ AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="4630c-211">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)               | <span data-ttu-id="4630c-212">Spécifie la vitesse de transmission encodée moyenne, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="4630c-212">Specifies the average encoded bit rate, in bits per second.</span></span>                                      | <span data-ttu-id="4630c-213">Comme décrit pour l’attribut de [ \_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde de sortie audio MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) dans le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="4630c-213">As described for the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output media type.</span></span>                      |
| [<span data-ttu-id="4630c-214">CODECAPI \_ AVEncMPACodingMode</span><span class="sxs-lookup"><span data-stu-id="4630c-214">CODECAPI\_AVEncMPACodingMode</span></span>](../directshow/avencmpacodingmode-property.md)                       | <span data-ttu-id="4630c-215">Spécifie le mode d’encodage audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="4630c-215">Specifies the MPEG audio encoding mode.</span></span>                                                          | <span data-ttu-id="4630c-216">Stéréo pour l’audio à 2 canaux, ou canal unique pour l’audio à 1 canal.</span><span class="sxs-lookup"><span data-stu-id="4630c-216">Stereo for 2-channel audio, or single channel for 1-channel audio.</span></span><br/> <span data-ttu-id="4630c-217">Pour l’audio à 2 canaux, l’encodeur prend également en charge le double canal et la stéréo jointe.</span><span class="sxs-lookup"><span data-stu-id="4630c-217">For 2-channel audio, the encoder also supports dual channel and joint stereo.</span></span><br/> |
| [<span data-ttu-id="4630c-218">CODECAPI \_ AVEncMPACopyright</span><span class="sxs-lookup"><span data-stu-id="4630c-218">CODECAPI\_AVEncMPACopyright</span></span>](../directshow/avencmpacopyright-property.md)                         | <span data-ttu-id="4630c-219">Spécifie s’il faut définir le bit de copyright dans le flux audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="4630c-219">Specifies whether to set the copyright bit in the MPEG audio stream.</span></span>                             | <span data-ttu-id="4630c-220">Aucun copyright.</span><span class="sxs-lookup"><span data-stu-id="4630c-220">No copyright.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="4630c-221">CODECAPI \_ AVEncMPAEmphasisType</span><span class="sxs-lookup"><span data-stu-id="4630c-221">CODECAPI\_AVEncMPAEmphasisType</span></span>](../directshow/avencmpaemphasistype-property.md)                   | <span data-ttu-id="4630c-222">Spécifie le type de filtre de désaccentuation à utiliser lorsque le flux encodé est décodé.</span><span class="sxs-lookup"><span data-stu-id="4630c-222">Specifies the type of de-emphasis filter that should be used when the encoded stream is decoded.</span></span> | <span data-ttu-id="4630c-223">Aucune accentuation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4630c-223">No emphasis specified.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="4630c-224">AVEncMPAEnableRedundancyProtection</span><span class="sxs-lookup"><span data-stu-id="4630c-224">AVEncMPAEnableRedundancyProtection</span></span>](../directshow/avencmpaenableredundancyprotection-property.md) | <span data-ttu-id="4630c-225">Spécifie s’il faut ajouter une vérification de redondance cyclique (CRC) à l’en-tête de trame.</span><span class="sxs-lookup"><span data-stu-id="4630c-225">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span>                    | <span data-ttu-id="4630c-226">Une somme de contrôle CRC est écrite dans le flux de bits.</span><span class="sxs-lookup"><span data-stu-id="4630c-226">A CRC checksum is written to the bit stream.</span></span>                                                                                                                           |
| [<span data-ttu-id="4630c-227">CODECAPI \_ AVEncMPALayer</span><span class="sxs-lookup"><span data-stu-id="4630c-227">CODECAPI\_AVEncMPALayer</span></span>](../directshow/avencmpalayer-property.md)                                 | <span data-ttu-id="4630c-228">Spécifie la couche audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="4630c-228">Specifies the MPEG audio layer.</span></span>                                                                  | <span data-ttu-id="4630c-229">Audio de couche 2.</span><span class="sxs-lookup"><span data-stu-id="4630c-229">Layer 2 audio.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="4630c-230">CODECAPI \_ AVEncMPAOriginalBitstream</span><span class="sxs-lookup"><span data-stu-id="4630c-230">CODECAPI\_AVEncMPAOriginalBitstream</span></span>](../directshow/avencmpaoriginalbitstream-property.md)         | <span data-ttu-id="4630c-231">Spécifie s’il faut définir le bit d’origine dans le flux audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="4630c-231">Specifies whether to set for the original bit in the MPEG audio stream.</span></span>                          | <span data-ttu-id="4630c-232">Le bit « original » est désactivé.</span><span class="sxs-lookup"><span data-stu-id="4630c-232">"Original" bit is off.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="4630c-233">CODECAPI \_ AVEncMPAPrivateUserBit</span><span class="sxs-lookup"><span data-stu-id="4630c-233">CODECAPI\_AVEncMPAPrivateUserBit</span></span>](../directshow/avencmpaprivateuserbit-property.md)               | <span data-ttu-id="4630c-234">Spécifie s’il faut définir pour le bit d’utilisateur privé dans le flux audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="4630c-234">Specifies whether to set for the private user bit in the MPEG audio stream.</span></span>                      | <span data-ttu-id="4630c-235">Le bit d’utilisateur privé est désactivé.</span><span class="sxs-lookup"><span data-stu-id="4630c-235">Private user bit is off.</span></span>                                                                                                                                               |



 

<span data-ttu-id="4630c-236">Pour obtenir un pointeur vers l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) , appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur la table MFT.</span><span class="sxs-lookup"><span data-stu-id="4630c-236">To get a pointer to the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the MFT.</span></span>

<span data-ttu-id="4630c-237">La table MFT implémente les méthodes [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) suivantes :</span><span class="sxs-lookup"><span data-stu-id="4630c-237">The MFT implements the following [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods:</span></span>

-   [<span data-ttu-id="4630c-238">**GetParameterRange**</span><span class="sxs-lookup"><span data-stu-id="4630c-238">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="4630c-239">**GetParameterValues**</span><span class="sxs-lookup"><span data-stu-id="4630c-239">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [<span data-ttu-id="4630c-240">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="4630c-240">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="4630c-241">**IsModifiable**</span><span class="sxs-lookup"><span data-stu-id="4630c-241">**IsModifiable**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [<span data-ttu-id="4630c-242">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="4630c-242">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="4630c-243">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="4630c-243">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

<span data-ttu-id="4630c-244">Toutes les autres méthodes [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) retournent **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="4630c-244">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods return **E\_NOTIMPL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4630c-245">Notes</span><span class="sxs-lookup"><span data-stu-id="4630c-245">Remarks</span></span>

<span data-ttu-id="4630c-246">Chaque trame audio MPEG contient des échantillons audio 384 (couche 1) ou 1152 (couche 2) par canal.</span><span class="sxs-lookup"><span data-stu-id="4630c-246">Each MPEG audio frame contains either 384 (Layer 1) or 1152 (Layer 2) audio samples per channel.</span></span> <span data-ttu-id="4630c-247">Toutefois, chaque mémoire tampon d’entrée de l’encodeur peut contenir un nombre quelconque d’échantillons PCM.</span><span class="sxs-lookup"><span data-stu-id="4630c-247">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="4630c-248">La taille de chaque mémoire tampon d’entrée doit être un multiple de l’alignement de bloc.</span><span class="sxs-lookup"><span data-stu-id="4630c-248">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="4630c-249">L’encodeur met en cache les exemples d’entrée jusqu’à ce qu’il soit suffisant pour une trame audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="4630c-249">The encoder caches input samples until it has enough for an MPEG audio frame.</span></span>

<span data-ttu-id="4630c-250">Chaque mémoire tampon de sortie contient une trame MPEG brute.</span><span class="sxs-lookup"><span data-stu-id="4630c-250">Each output buffer contains one raw MPEG frame.</span></span> <span data-ttu-id="4630c-251">La taille de chaque mémoire tampon de sortie dépend de la vitesse de transmission et du taux d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="4630c-251">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

### <a name="configuring-the-encoder"></a><span data-ttu-id="4630c-252">Configuration de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="4630c-252">Configuring the Encoder</span></span>

<span data-ttu-id="4630c-253">Pour modifier l’un des paramètres par défaut de l’encodeur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4630c-253">To change any of the default settings on the encoder, perform the following steps:</span></span>

1.  <span data-ttu-id="4630c-254">Créez une instance de la MFT de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="4630c-254">Create an instance of the encoder MFT.</span></span>
2.  <span data-ttu-id="4630c-255">Appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour afficher la liste des types de sortie préférés.</span><span class="sxs-lookup"><span data-stu-id="4630c-255">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of the preferred output types.</span></span> <span data-ttu-id="4630c-256">L’encodeur énumère tous les taux d’échantillonnage pour mono et stéréo.</span><span class="sxs-lookup"><span data-stu-id="4630c-256">The encoder enumerates all sample rates for both mono and stereo.</span></span> <span data-ttu-id="4630c-257">Sélectionnez l’un de ces types de média, en fonction du taux d’échantillonnage et du nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="4630c-257">Select one of these media types, based on the sample rate and number of channels.</span></span> <span data-ttu-id="4630c-258">L' [attribut \_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde de sortie audio MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) indique la vitesse de transmission par défaut en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="4630c-258">The [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute indicates the default bit rate, in bytes per second.</span></span>
3.  <span data-ttu-id="4630c-259">Facultatif : vous pouvez remplacer la vitesse de transmission par défaut en définissant une nouvelle valeur pour [MF \_ MT \_ audio \_ AVG \_ octets \_ par \_ seconde](mf-mt-audio-avg-bytes-per-second-attribute.md) sur le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="4630c-259">Optional: You can override the default bit rate by setting a new value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) on the output media type.</span></span> <span data-ttu-id="4630c-260">Les vitesses de transmission valides dépendent du taux d’échantillonnage, du nombre de canaux et de la couche audio.</span><span class="sxs-lookup"><span data-stu-id="4630c-260">Valid bit rates depend on the sample rate, number of channels, and audio layer.</span></span>
    > [!Note]  
    > <span data-ttu-id="4630c-261">À ce stade du processus de configuration, l’encodeur utilise par défaut l’audio de couche 2 et n’accepte que les débits de couche 2.</span><span class="sxs-lookup"><span data-stu-id="4630c-261">At this point in the configuration process, the encoder defaults to Layer 2 audio and will only accept Layer 2 bit rates.</span></span> <span data-ttu-id="4630c-262">Vous serez en mesure de basculer l’encodeur vers la couche 1 à une étape ultérieure (Voir l’étape 7).</span><span class="sxs-lookup"><span data-stu-id="4630c-262">You will be able to switch the encoder to Layer 1 in a later step (see step 7).</span></span> <span data-ttu-id="4630c-263">Dans ce cas, laissez la vitesse de transmission par défaut pour l’instant ; vous pouvez le modifier à nouveau à l’étape 8.</span><span class="sxs-lookup"><span data-stu-id="4630c-263">In that case, leave the default bit rate for now; you can change it again in step 8.</span></span>

     

4.  <span data-ttu-id="4630c-264">Appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="4630c-264">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the output media type.</span></span> <span data-ttu-id="4630c-265">Si vous définissez votre propre valeur pour [MF \_ MT \_ audio \_ Moy \_ octets \_ par \_ seconde](mf-mt-audio-avg-bytes-per-second-attribute.md) et que la MFT rejette le type de média de sortie, cela est probablement dû au fait que vous avez spécifié une vitesse de transmission non valide.</span><span class="sxs-lookup"><span data-stu-id="4630c-265">If you set your own value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) and the MFT rejects the output media type, it is likely because you specified an invalid bit rate.</span></span>
5.  <span data-ttu-id="4630c-266">Appelez [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) pour énumérer le type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4630c-266">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to enumerate the input media type.</span></span> <span data-ttu-id="4630c-267">Étant donné que le taux d’échantillonnage et le nombre de canaux doivent être identiques à ceux du type de sortie, seules deux options sont énumérées : entrée PCM à virgule flottante 32 bits et entrée PCM de type entier 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4630c-267">Because the sample rate and number of channels must be identical to the output type, only two options are enumerated: 32-bit floating-point PCM input and 16-bit integer PCM input.</span></span> <span data-ttu-id="4630c-268">Sélectionnez l’une de ces.</span><span class="sxs-lookup"><span data-stu-id="4630c-268">Select one of these.</span></span>
6.  <span data-ttu-id="4630c-269">Appelez [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) pour définir le type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4630c-269">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the input media type.</span></span>
7.  <span data-ttu-id="4630c-270">Facultatif : pour encoder l’audio de couche 1, définissez la propriété [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) sur **eAVEncMPALayer \_ 1**.</span><span class="sxs-lookup"><span data-stu-id="4630c-270">Optional: To encode Layer 1 audio, set the [CODECAPI\_AVEncMPALayer](../directshow/avencmpalayer-property.md) property to **eAVEncMPALayer\_1**.</span></span>
8.  <span data-ttu-id="4630c-271">Facultatif : pour modifier la vitesse de transmission, définissez la propriété [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="4630c-271">Optional: To change the bit rate, set the [CODECAPI\_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <span data-ttu-id="4630c-272">La vitesse de transmission doit être l’un des taux de bits valides indiqués dans les spécifications MPEG-1 ou MPEG-2 LSF.</span><span class="sxs-lookup"><span data-stu-id="4630c-272">The bit rate must be one of the valid bit rates listed in the MPEG-1 or MPEG-2 LSF specifications.</span></span> <span data-ttu-id="4630c-273">Vous pouvez également appeler [**ICodecAPI :: getParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) pour obtenir une liste de vitesses de transmission valides, en fonction des paramètres actuels.</span><span class="sxs-lookup"><span data-stu-id="4630c-273">Alternatively, you can call [**ICodecAPI::GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) to get a list of valid bit rates, based on the current settings.</span></span>
9.  <span data-ttu-id="4630c-274">Facultatif : avec l’audio à 2 canaux, vous pouvez définir la propriété [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) pour changer le mode de codage en double canal ou stéréo jointe.</span><span class="sxs-lookup"><span data-stu-id="4630c-274">Optional: With 2-channel audio, you can set the [CODECAPI\_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) property to change the coding mode to dual channel or joint stereo.</span></span> <span data-ttu-id="4630c-275">Vous pouvez appeler [**ICodecAPI :: GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) pour accéder aux options valides.</span><span class="sxs-lookup"><span data-stu-id="4630c-275">You can call [**ICodecAPI::GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) to get the valid options.</span></span> <span data-ttu-id="4630c-276">(Pour l’audio de canal 1, la seule option est mono.)</span><span class="sxs-lookup"><span data-stu-id="4630c-276">(For 1-channel audio, the only option is mono.)</span></span>
10. <span data-ttu-id="4630c-277">Facultatif : définissez les autres propriétés [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) indiquées précédemment.</span><span class="sxs-lookup"><span data-stu-id="4630c-277">Optional: Set any of the other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties listed previously.</span></span>

<span data-ttu-id="4630c-278">Il est important de suivre l’ordre de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="4630c-278">It is important to follow the order of these steps.</span></span> <span data-ttu-id="4630c-279">En particulier, définissez le type de média de sortie avant de modifier les propriétés de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="4630c-279">In particular, set the output media type before changing any [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties.</span></span> <span data-ttu-id="4630c-280">En outre, vous devez définir les propriétés de **ICodecAPI** avant que MFT ne reçoive le premier exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4630c-280">Also, you must set **ICodecAPI** properties before the MFT receives the first input sample.</span></span> <span data-ttu-id="4630c-281">Une fois que la MFT reçoit l’entrée, les propriétés du codec sont en lecture seule et [**ICodecAPI :: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) retourne la valeur **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="4630c-281">After the MFT receives input, the codec properties are read-only, and [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) returns the value **S\_FALSE**.</span></span>

### <a name="supported-bit-rates"></a><span data-ttu-id="4630c-282">Vitesses de transmission prises en charge</span><span class="sxs-lookup"><span data-stu-id="4630c-282">Supported Bit Rates</span></span>

<span data-ttu-id="4630c-283">L’encodeur prend en charge les vitesses de transmission suivantes.</span><span class="sxs-lookup"><span data-stu-id="4630c-283">The encoder supports the following bit rates.</span></span>



<span data-ttu-id="4630c-284">MPEG-1</span><span class="sxs-lookup"><span data-stu-id="4630c-284">MPEG-1</span></span>

<span data-ttu-id="4630c-285">MPEG-2</span><span class="sxs-lookup"><span data-stu-id="4630c-285">MPEG-2</span></span>

<span data-ttu-id="4630c-286">Couche 1</span><span class="sxs-lookup"><span data-stu-id="4630c-286">Layer 1</span></span>

<span data-ttu-id="4630c-287">Couche 2</span><span class="sxs-lookup"><span data-stu-id="4630c-287">Layer 2</span></span>

<span data-ttu-id="4630c-288">Couche 1</span><span class="sxs-lookup"><span data-stu-id="4630c-288">Layer 1</span></span>

<span data-ttu-id="4630c-289">Couche 2</span><span class="sxs-lookup"><span data-stu-id="4630c-289">Layer 2</span></span>

<span data-ttu-id="4630c-290">32</span><span class="sxs-lookup"><span data-stu-id="4630c-290">32</span></span>

<span data-ttu-id="4630c-291">32\*</span><span class="sxs-lookup"><span data-stu-id="4630c-291">32\*</span></span>

<span data-ttu-id="4630c-292">32</span><span class="sxs-lookup"><span data-stu-id="4630c-292">32</span></span>

<span data-ttu-id="4630c-293">8</span><span class="sxs-lookup"><span data-stu-id="4630c-293">8</span></span>

<span data-ttu-id="4630c-294">64</span><span class="sxs-lookup"><span data-stu-id="4630c-294">64</span></span>

<span data-ttu-id="4630c-295">48\*</span><span class="sxs-lookup"><span data-stu-id="4630c-295">48\*</span></span>

<span data-ttu-id="4630c-296">38</span><span class="sxs-lookup"><span data-stu-id="4630c-296">38</span></span>

<span data-ttu-id="4630c-297">16</span><span class="sxs-lookup"><span data-stu-id="4630c-297">16</span></span>

<span data-ttu-id="4630c-298">96</span><span class="sxs-lookup"><span data-stu-id="4630c-298">96</span></span>

<span data-ttu-id="4630c-299">56\*</span><span class="sxs-lookup"><span data-stu-id="4630c-299">56\*</span></span>

<span data-ttu-id="4630c-300">56</span><span class="sxs-lookup"><span data-stu-id="4630c-300">56</span></span>

<span data-ttu-id="4630c-301">24</span><span class="sxs-lookup"><span data-stu-id="4630c-301">24</span></span>

<span data-ttu-id="4630c-302">128</span><span class="sxs-lookup"><span data-stu-id="4630c-302">128</span></span>

<span data-ttu-id="4630c-303">64</span><span class="sxs-lookup"><span data-stu-id="4630c-303">64</span></span>

<span data-ttu-id="4630c-304">64</span><span class="sxs-lookup"><span data-stu-id="4630c-304">64</span></span>

<span data-ttu-id="4630c-305">32</span><span class="sxs-lookup"><span data-stu-id="4630c-305">32</span></span>

<span data-ttu-id="4630c-306">160</span><span class="sxs-lookup"><span data-stu-id="4630c-306">160</span></span>

<span data-ttu-id="4630c-307">80\*</span><span class="sxs-lookup"><span data-stu-id="4630c-307">80\*</span></span>

<span data-ttu-id="4630c-308">80</span><span class="sxs-lookup"><span data-stu-id="4630c-308">80</span></span>

<span data-ttu-id="4630c-309">40</span><span class="sxs-lookup"><span data-stu-id="4630c-309">40</span></span>

<span data-ttu-id="4630c-310">192</span><span class="sxs-lookup"><span data-stu-id="4630c-310">192</span></span>

<span data-ttu-id="4630c-311">96</span><span class="sxs-lookup"><span data-stu-id="4630c-311">96</span></span>

<span data-ttu-id="4630c-312">96</span><span class="sxs-lookup"><span data-stu-id="4630c-312">96</span></span>

<span data-ttu-id="4630c-313">48</span><span class="sxs-lookup"><span data-stu-id="4630c-313">48</span></span>

<span data-ttu-id="4630c-314">224</span><span class="sxs-lookup"><span data-stu-id="4630c-314">224</span></span>

<span data-ttu-id="4630c-315">112</span><span class="sxs-lookup"><span data-stu-id="4630c-315">112</span></span>

<span data-ttu-id="4630c-316">112</span><span class="sxs-lookup"><span data-stu-id="4630c-316">112</span></span>

<span data-ttu-id="4630c-317">56</span><span class="sxs-lookup"><span data-stu-id="4630c-317">56</span></span>

<span data-ttu-id="4630c-318">256</span><span class="sxs-lookup"><span data-stu-id="4630c-318">256</span></span>

<span data-ttu-id="4630c-319">128</span><span class="sxs-lookup"><span data-stu-id="4630c-319">128</span></span>

<span data-ttu-id="4630c-320">128</span><span class="sxs-lookup"><span data-stu-id="4630c-320">128</span></span>

<span data-ttu-id="4630c-321">64</span><span class="sxs-lookup"><span data-stu-id="4630c-321">64</span></span>

<span data-ttu-id="4630c-322">288</span><span class="sxs-lookup"><span data-stu-id="4630c-322">288</span></span>

<span data-ttu-id="4630c-323">160</span><span class="sxs-lookup"><span data-stu-id="4630c-323">160</span></span>

<span data-ttu-id="4630c-324">144</span><span class="sxs-lookup"><span data-stu-id="4630c-324">144</span></span>

<span data-ttu-id="4630c-325">80</span><span class="sxs-lookup"><span data-stu-id="4630c-325">80</span></span>

<span data-ttu-id="4630c-326">320</span><span class="sxs-lookup"><span data-stu-id="4630c-326">320</span></span>

<span data-ttu-id="4630c-327">192</span><span class="sxs-lookup"><span data-stu-id="4630c-327">192</span></span>

<span data-ttu-id="4630c-328">160</span><span class="sxs-lookup"><span data-stu-id="4630c-328">160</span></span>

<span data-ttu-id="4630c-329">96</span><span class="sxs-lookup"><span data-stu-id="4630c-329">96</span></span>

<span data-ttu-id="4630c-330">352</span><span class="sxs-lookup"><span data-stu-id="4630c-330">352</span></span>

<span data-ttu-id="4630c-331">224\*\*</span><span class="sxs-lookup"><span data-stu-id="4630c-331">224\*\*</span></span>

<span data-ttu-id="4630c-332">176</span><span class="sxs-lookup"><span data-stu-id="4630c-332">176</span></span>

<span data-ttu-id="4630c-333">112</span><span class="sxs-lookup"><span data-stu-id="4630c-333">112</span></span>

<span data-ttu-id="4630c-334">384</span><span class="sxs-lookup"><span data-stu-id="4630c-334">384</span></span>

<span data-ttu-id="4630c-335">256\*\*</span><span class="sxs-lookup"><span data-stu-id="4630c-335">256\*\*</span></span>

<span data-ttu-id="4630c-336">192</span><span class="sxs-lookup"><span data-stu-id="4630c-336">192</span></span>

<span data-ttu-id="4630c-337">128</span><span class="sxs-lookup"><span data-stu-id="4630c-337">128</span></span>

<span data-ttu-id="4630c-338">416</span><span class="sxs-lookup"><span data-stu-id="4630c-338">416</span></span>

<span data-ttu-id="4630c-339">230\*\*</span><span class="sxs-lookup"><span data-stu-id="4630c-339">230\*\*</span></span>

<span data-ttu-id="4630c-340">224</span><span class="sxs-lookup"><span data-stu-id="4630c-340">224</span></span>

<span data-ttu-id="4630c-341">144</span><span class="sxs-lookup"><span data-stu-id="4630c-341">144</span></span>

<span data-ttu-id="4630c-342">448</span><span class="sxs-lookup"><span data-stu-id="4630c-342">448</span></span>

<span data-ttu-id="4630c-343">384\*\*</span><span class="sxs-lookup"><span data-stu-id="4630c-343">384\*\*</span></span>

<span data-ttu-id="4630c-344">256</span><span class="sxs-lookup"><span data-stu-id="4630c-344">256</span></span>

<span data-ttu-id="4630c-345">160</span><span class="sxs-lookup"><span data-stu-id="4630c-345">160</span></span>



 

<dl> <span data-ttu-id="4630c-346">\* Mono uniquement</span><span class="sxs-lookup"><span data-stu-id="4630c-346">\* Mono only</span></span>  
<span data-ttu-id="4630c-347">\*\* Stéréo uniquement</span><span class="sxs-lookup"><span data-stu-id="4630c-347">\*\* Stereo only</span></span>  
</dl>

### <a name="example-media-types"></a><span data-ttu-id="4630c-348">Exemples de types de média</span><span class="sxs-lookup"><span data-stu-id="4630c-348">Example Media Types</span></span>

<span data-ttu-id="4630c-349">Voici un exemple des types de médias nécessaires pour encoder le PCM d’entiers 16 bits, 48-kHz de l’audio stéréo à la vitesse de transmission par défaut.</span><span class="sxs-lookup"><span data-stu-id="4630c-349">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate.</span></span>

<span data-ttu-id="4630c-350">Type de média de sortie :</span><span class="sxs-lookup"><span data-stu-id="4630c-350">Output media type:</span></span>

| <span data-ttu-id="4630c-351">Attribut</span><span class="sxs-lookup"><span data-stu-id="4630c-351">Attribute</span></span>                                                                           | <span data-ttu-id="4630c-352">Valeur</span><span class="sxs-lookup"><span data-stu-id="4630c-352">Value</span></span>                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [<span data-ttu-id="4630c-353">\_type de \_ majeurese MF MT \_</span><span class="sxs-lookup"><span data-stu-id="4630c-353">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="4630c-354">**MFMediaType \_ audio**</span><span class="sxs-lookup"><span data-stu-id="4630c-354">**MFMediaType\_Audio**</span></span>  |
| [<span data-ttu-id="4630c-355">\_sous- \_ type MF MT</span><span class="sxs-lookup"><span data-stu-id="4630c-355">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="4630c-356">**\_MPEG MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="4630c-356">**MFAudioFormat\_MPEG**</span></span> |
| [<span data-ttu-id="4630c-357">\_ \_ échantillons audio MF \_ MT \_ par \_ seconde</span><span class="sxs-lookup"><span data-stu-id="4630c-357">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="4630c-358">48 000</span><span class="sxs-lookup"><span data-stu-id="4630c-358">48000</span></span>                   |
| [<span data-ttu-id="4630c-359">\_canaux de \_ \_ numéros audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="4630c-359">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="4630c-360">2</span><span class="sxs-lookup"><span data-stu-id="4630c-360">2</span></span>                       |



 

<span data-ttu-id="4630c-361">Type de média d’entrée :</span><span class="sxs-lookup"><span data-stu-id="4630c-361">Input media type:</span></span>

| <span data-ttu-id="4630c-362">Attribut</span><span class="sxs-lookup"><span data-stu-id="4630c-362">Attribute</span></span>                                                                                | <span data-ttu-id="4630c-363">Valeur</span><span class="sxs-lookup"><span data-stu-id="4630c-363">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="4630c-364">\_type de \_ majeurese MF MT \_</span><span class="sxs-lookup"><span data-stu-id="4630c-364">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="4630c-365">**MFMediaType \_ audio**</span><span class="sxs-lookup"><span data-stu-id="4630c-365">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="4630c-366">\_sous- \_ type MF MT</span><span class="sxs-lookup"><span data-stu-id="4630c-366">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="4630c-367">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="4630c-367">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="4630c-368">\_bits de \_ sortie audio MF \_ \_ par \_ échantillon</span><span class="sxs-lookup"><span data-stu-id="4630c-368">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="4630c-369">16</span><span class="sxs-lookup"><span data-stu-id="4630c-369">16</span></span>                     |
| [<span data-ttu-id="4630c-370">\_ \_ échantillons audio MF \_ MT \_ par \_ seconde</span><span class="sxs-lookup"><span data-stu-id="4630c-370">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="4630c-371">48 000</span><span class="sxs-lookup"><span data-stu-id="4630c-371">48000</span></span>                  |
| [<span data-ttu-id="4630c-372">\_canaux de \_ \_ numéros audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="4630c-372">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="4630c-373">2</span><span class="sxs-lookup"><span data-stu-id="4630c-373">2</span></span>                      |
| [<span data-ttu-id="4630c-374">\_alignement de \_ \_ bloc audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="4630c-374">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="4630c-375">4</span><span class="sxs-lookup"><span data-stu-id="4630c-375">4</span></span>                      |
| [<span data-ttu-id="4630c-376">\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde</span><span class="sxs-lookup"><span data-stu-id="4630c-376">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="4630c-377">192000</span><span class="sxs-lookup"><span data-stu-id="4630c-377">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="4630c-378">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4630c-378">Requirements</span></span>



| <span data-ttu-id="4630c-379">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4630c-379">Requirement</span></span> | <span data-ttu-id="4630c-380">Valeur</span><span class="sxs-lookup"><span data-stu-id="4630c-380">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4630c-381">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4630c-381">Minimum supported client</span></span><br/> | <span data-ttu-id="4630c-382">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4630c-382">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4630c-383">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4630c-383">Minimum supported server</span></span><br/> | <span data-ttu-id="4630c-384">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4630c-384">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="4630c-385">DLL</span><span class="sxs-lookup"><span data-stu-id="4630c-385">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4630c-386"><dt>Msmpeg2enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4630c-386"><dt>Msmpeg2enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4630c-387">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4630c-387">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4630c-388">Objets codec</span><span class="sxs-lookup"><span data-stu-id="4630c-388">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
