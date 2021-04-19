---
description: Le décodeur Dolby audio est une Media Foundation transformation (MFT) qui encode le son mono ou stéréo sur Dolby Digital, également appelé Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Encodeur audio Dolby Digital
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6c5b59bc09cd8c0fd56f22703ef8afdfe3921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513162"
---
# <a name="dolby-digital-audio-encoder"></a><span data-ttu-id="ad1f5-103">Encodeur audio Dolby Digital</span><span class="sxs-lookup"><span data-stu-id="ad1f5-103">Dolby Digital Audio Encoder</span></span>

<span data-ttu-id="ad1f5-104">Le décodeur Dolby audio est une [Media Foundation transformation](media-foundation-transforms.md) (MFT) qui encode le son mono ou stéréo sur Dolby Digital, également appelé Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that encodes mono or stereo audio to Dolby Digital, also called Dolby AC-3.</span></span> <span data-ttu-id="ad1f5-105">L’encodeur ne prend pas en charge les entrées multicanal, telles que la configuration du canal 5,1.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-105">The encoder does not support multi-channel input, such as the 5.1 channel configuration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad1f5-106">Pour les versions de Windows antérieures à Windows 8, l’implémentation Microsoft de la technologie Dolby Digital est limitée aux termes du programme de gestion de licences Dolby Digital à utiliser par les applications Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-106">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="ad1f5-107">Pour plus d’informations sur Dolby Digital Audio, reportez-vous à la version B du document ATSC *audio compression standard (AC-3, E-AC-3)*.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-107">For more information about Dolby Digital audio, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="ad1f5-108">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="ad1f5-108">Class Identifier</span></span>

<span data-ttu-id="ad1f5-109">L’identificateur de classe (CLSID) du décodeur Dolby audio est **CLSID \_ CMSDolbyDigitalEncMFT**, défini dans le fichier d’en-tête wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-109">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDolbyDigitalEncMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="ad1f5-110">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="ad1f5-110">Output Types</span></span>

<span data-ttu-id="ad1f5-111">Le type de sortie doit être défini en premier, avant le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-111">The output type must be set first, before the input type.</span></span> <span data-ttu-id="ad1f5-112">Le tableau suivant répertorie les attributs obligatoires et facultatifs pour le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-112">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad1f5-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="ad1f5-113">Attribute</span></span></th>
<th><span data-ttu-id="ad1f5-114">Description</span><span class="sxs-lookup"><span data-stu-id="ad1f5-114">Description</span></span></th>
<th><span data-ttu-id="ad1f5-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ad1f5-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ad1f5-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="ad1f5-117">Type principal.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-117">Major type.</span></span></td>
<td><span data-ttu-id="ad1f5-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-118">Required.</span></span> <span data-ttu-id="ad1f5-119">Doit être <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-119">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad1f5-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="ad1f5-121">Sous-type audio.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-121">Audio subtype.</span></span></td>
<td><span data-ttu-id="ad1f5-122">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-122">Required.</span></span> <span data-ttu-id="ad1f5-123">Doit être <strong>MFAudioFormat_Dolby_AC3</strong>.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-123">Must be <strong>MFAudioFormat_Dolby_AC3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad1f5-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="ad1f5-125">Échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-125">Samples per second.</span></span></td>
<td><span data-ttu-id="ad1f5-126">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-126">Required.</span></span> <span data-ttu-id="ad1f5-127">Les valeurs suivantes sont admises :</span><span class="sxs-lookup"><span data-stu-id="ad1f5-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="ad1f5-128">32000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-128">32000</span></span></li>
<li><span data-ttu-id="ad1f5-129">44100</span><span class="sxs-lookup"><span data-stu-id="ad1f5-129">44100</span></span></li>
<li><span data-ttu-id="ad1f5-130">48 000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-130">48000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad1f5-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="ad1f5-132">Nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-132">Number of channels.</span></span></td>
<td><span data-ttu-id="ad1f5-133">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-133">Required.</span></span> <span data-ttu-id="ad1f5-134">Doit avoir la valeur 1 (mono) ou 2 (stéréo).</span><span class="sxs-lookup"><span data-stu-id="ad1f5-134">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad1f5-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="ad1f5-136">Spécifie l’affectation des canaux audio aux positions des haut-parleurs.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-136">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="ad1f5-137">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-137">Optional.</span></span> <span data-ttu-id="ad1f5-138">S’il est défini, la valeur doit être 0x3 pour les canaux stéréo (avant gauche et droit) ou 0x4 pour mono (canal avant centre).</span><span class="sxs-lookup"><span data-stu-id="ad1f5-138">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad1f5-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="ad1f5-140">Débit binaire du flux AC-3 encodé, en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-140">Bit rate of the encoded AC-3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="ad1f5-141">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-141">Optional.</span></span> <span data-ttu-id="ad1f5-142">Consultez la section Notes pour connaître les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-142">See Remarks for valid values.</span></span> <span data-ttu-id="ad1f5-143">Si cet attribut n’est pas défini, l’encodeur utilise une vitesse de transmission par défaut, comme décrit dans la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-143">If this attribute is not set, the encoder uses a default bit rate, as described in Remarks.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ad1f5-144">Si les attributs facultatifs ne sont pas définis, l’encodeur les ajoute au type de média après que le type a été défini.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-144">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="ad1f5-145">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="ad1f5-145">Input Types</span></span>

<span data-ttu-id="ad1f5-146">Le tableau suivant répertorie les attributs obligatoires et facultatifs pour le type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-146">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad1f5-147">Attribut</span><span class="sxs-lookup"><span data-stu-id="ad1f5-147">Attribute</span></span></th>
<th><span data-ttu-id="ad1f5-148">Description</span><span class="sxs-lookup"><span data-stu-id="ad1f5-148">Description</span></span></th>
<th><span data-ttu-id="ad1f5-149">Notes</span><span class="sxs-lookup"><span data-stu-id="ad1f5-149">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ad1f5-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="ad1f5-151">Type principal.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-151">Major type.</span></span></td>
<td><span data-ttu-id="ad1f5-152">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-152">Required.</span></span> <span data-ttu-id="ad1f5-153">Doit être <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-153">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad1f5-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="ad1f5-155">Sous-type audio.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-155">Audio subtype.</span></span></td>
<td><span data-ttu-id="ad1f5-156">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-156">Required.</span></span> <span data-ttu-id="ad1f5-157">Doit être <strong>MFAudioFormat_PCM</strong> ou <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-157">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad1f5-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="ad1f5-159">Nombre de bits par échantillon audio.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-159">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="ad1f5-160">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-160">Required.</span></span> <span data-ttu-id="ad1f5-161">La valeur doit être 16 si le sous-type est <strong>MFAudioFormat_PCM</strong>, ou 32 si le sous-type est <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-161">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad1f5-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="ad1f5-163">Échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-163">Samples per second.</span></span></td>
<td><span data-ttu-id="ad1f5-164">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-164">Required.</span></span> <span data-ttu-id="ad1f5-165">Doit correspondre au type de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-165">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad1f5-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="ad1f5-167">Nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-167">Number of channels.</span></span></td>
<td><span data-ttu-id="ad1f5-168">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-168">Required.</span></span> <span data-ttu-id="ad1f5-169">Doit correspondre au type de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-169">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad1f5-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="ad1f5-171">Alignement de bloc, en octets.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-171">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="ad1f5-172">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-172">Required.</span></span> <span data-ttu-id="ad1f5-173">Calculez la valeur comme suit :</span><span class="sxs-lookup"><span data-stu-id="ad1f5-173">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="ad1f5-174"><strong>MFAudioFormat_PCM</strong>: nombre de canaux × 2.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-174"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="ad1f5-175"><strong>MFAudioFormat_Float</strong>: nombre de canaux × 4.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-175"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad1f5-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="ad1f5-177">Vitesse de transmission du flux de données AC3 encodé, en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-177">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="ad1f5-178">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-178">Required.</span></span> <span data-ttu-id="ad1f5-179">Doit être égal à alignement de bloc × échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-179">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ad1f5-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="ad1f5-181">Spécifie l’affectation des canaux audio aux positions des haut-parleurs.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-181">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="ad1f5-182">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-182">Optional.</span></span> <span data-ttu-id="ad1f5-183">Si cette valeur est définie, la valeur doit correspondre au type de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-183">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ad1f5-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="ad1f5-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="ad1f5-185">Nombre de bits de données audio valides dans chaque exemple audio.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-185">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="ad1f5-186">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-186">Optional.</span></span> <span data-ttu-id="ad1f5-187">Si cette valeur est définie, la valeur doit être identique à <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-187">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ad1f5-188">L’encodeur ne prend pas en charge la conversion de taux d’échantillonnage ou la conversion stéréo/mono.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-188">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad1f5-189">Notes</span><span class="sxs-lookup"><span data-stu-id="ad1f5-189">Remarks</span></span>

<span data-ttu-id="ad1f5-190">Chaque trame audio Dolby AC-3 contient 1536 échantillons audio par canal.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-190">Each Dolby AC-3 audio frame contains 1536 audio samples per channel.</span></span> <span data-ttu-id="ad1f5-191">Toutefois, chaque mémoire tampon d’entrée de l’encodeur peut contenir un nombre quelconque d’échantillons PCM.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-191">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="ad1f5-192">La taille de chaque mémoire tampon d’entrée doit être un multiple de l’alignement de bloc.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-192">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="ad1f5-193">L’encodeur met en cache les exemples d’entrée jusqu’à ce qu’il soit suffisant pour les échantillons audio 1536 par canal ; à partir de là, l’encodeur génère une trame AC-3.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-193">The encoder caches input samples until it has enough for 1536 audio samples per channel; at which point the encoder outputs one AC-3 frame.</span></span>

<span data-ttu-id="ad1f5-194">Chaque mémoire tampon de sortie contient une trame AC-3 brute.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-194">Each output buffer contains one raw AC-3 frame.</span></span> <span data-ttu-id="ad1f5-195">La durée est équivalente à la durée des échantillons PCM 1536 au taux d’échantillonnage actuel (32 ms) à 48 kHz, 34,83 ms à 44,1 kHz et 48 MS à 32 kHz).</span><span class="sxs-lookup"><span data-stu-id="ad1f5-195">The duration is equivalent to the duration of 1536 PCM samples at the current sampling rate (32 msec) at 48 kHz sample rate, 34.83 msec at 44.1 kHz, and 48 msec at 32 kHz).</span></span> <span data-ttu-id="ad1f5-196">La taille de chaque mémoire tampon de sortie dépend de la vitesse de transmission et du taux d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-196">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

<span data-ttu-id="ad1f5-197">Pour spécifier la vitesse de transmission de l’encodage, définissez l’attribut de sortie [ \_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde du type MF MT audio par seconde](mf-mt-audio-avg-bytes-per-second-attribute.md) dans le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-197">To specify the encoding bit rate, set the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output type.</span></span> <span data-ttu-id="ad1f5-198">Le tableau suivant indique la relation entre la vitesse de transmission de l’encodage et le \_ \_ nombre moyen d’octets de sortie audio MF MT \_ \_ \_ par \_ seconde.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-198">The following table shows the relation between encoding bit rate and MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND.</span></span>



| <span data-ttu-id="ad1f5-199">Débit binaire (Kbits/s)</span><span class="sxs-lookup"><span data-stu-id="ad1f5-199">Bit rate (kbps)</span></span> | [<span data-ttu-id="ad1f5-200">\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde</span><span class="sxs-lookup"><span data-stu-id="ad1f5-200">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="ad1f5-201">Notes</span><span class="sxs-lookup"><span data-stu-id="ad1f5-201">Remarks</span></span>                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ad1f5-202">64</span><span class="sxs-lookup"><span data-stu-id="ad1f5-202">64</span></span>              | <span data-ttu-id="ad1f5-203">8000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-203">8000</span></span>                                                                                     | <span data-ttu-id="ad1f5-204">Mono uniquement.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-204">Mono only.</span></span>                                              |
| <span data-ttu-id="ad1f5-205">80</span><span class="sxs-lookup"><span data-stu-id="ad1f5-205">80</span></span>              | <span data-ttu-id="ad1f5-206">10000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-206">10000</span></span>                                                                                    | <span data-ttu-id="ad1f5-207">Mono uniquement.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-207">Mono only.</span></span>                                              |
| <span data-ttu-id="ad1f5-208">96</span><span class="sxs-lookup"><span data-stu-id="ad1f5-208">96</span></span>              | <span data-ttu-id="ad1f5-209">12 000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-209">12000</span></span>                                                                                    | <span data-ttu-id="ad1f5-210">Mono uniquement.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-210">Mono only.</span></span>                                              |
| <span data-ttu-id="ad1f5-211">112</span><span class="sxs-lookup"><span data-stu-id="ad1f5-211">112</span></span>             | <span data-ttu-id="ad1f5-212">14000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-212">14000</span></span>                                                                                    | <span data-ttu-id="ad1f5-213">Mono uniquement.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-213">Mono only.</span></span>                                              |
| <span data-ttu-id="ad1f5-214">128</span><span class="sxs-lookup"><span data-stu-id="ad1f5-214">128</span></span>             | <span data-ttu-id="ad1f5-215">16000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-215">16000</span></span>                                                                                    | <span data-ttu-id="ad1f5-216">Mono ou stéréo.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-216">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="ad1f5-217">160</span><span class="sxs-lookup"><span data-stu-id="ad1f5-217">160</span></span>             | <span data-ttu-id="ad1f5-218">20000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-218">20000</span></span>                                                                                    | <span data-ttu-id="ad1f5-219">Mono ou stéréo.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-219">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="ad1f5-220">192</span><span class="sxs-lookup"><span data-stu-id="ad1f5-220">192</span></span>             | <span data-ttu-id="ad1f5-221">24 000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-221">24000</span></span>                                                                                    | <span data-ttu-id="ad1f5-222">Mono ou stéréo.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-222">Mono or stereo.</span></span> <span data-ttu-id="ad1f5-223">Il s’agit du paramètre par défaut pour mono.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-223">This is the default setting for mono.</span></span>   |
| <span data-ttu-id="ad1f5-224">224</span><span class="sxs-lookup"><span data-stu-id="ad1f5-224">224</span></span>             | <span data-ttu-id="ad1f5-225">28000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-225">28000</span></span>                                                                                    | <span data-ttu-id="ad1f5-226">Mono ou stéréo.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-226">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="ad1f5-227">256</span><span class="sxs-lookup"><span data-stu-id="ad1f5-227">256</span></span>             | <span data-ttu-id="ad1f5-228">32000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-228">32000</span></span>                                                                                    | <span data-ttu-id="ad1f5-229">Mono ou stéréo.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-229">Mono or stereo.</span></span> <span data-ttu-id="ad1f5-230">Il s’agit du paramètre par défaut pour le stéréo.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-230">This is the default setting for stereo.</span></span> |
| <span data-ttu-id="ad1f5-231">320</span><span class="sxs-lookup"><span data-stu-id="ad1f5-231">320</span></span>             | <span data-ttu-id="ad1f5-232">40000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-232">40000</span></span>                                                                                    | <span data-ttu-id="ad1f5-233">Stéréo uniquement.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-233">Stereo only.</span></span>                                            |
| <span data-ttu-id="ad1f5-234">384</span><span class="sxs-lookup"><span data-stu-id="ad1f5-234">384</span></span>             | <span data-ttu-id="ad1f5-235">48 000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-235">48000</span></span>                                                                                    | <span data-ttu-id="ad1f5-236">Stéréo uniquement.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-236">Stereo only.</span></span>                                            |
| <span data-ttu-id="ad1f5-237">448</span><span class="sxs-lookup"><span data-stu-id="ad1f5-237">448</span></span>             | <span data-ttu-id="ad1f5-238">56 000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-238">56000</span></span>                                                                                    | <span data-ttu-id="ad1f5-239">Stéréo uniquement.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-239">Stereo only.</span></span>                                            |



 

<span data-ttu-id="ad1f5-240">Le débit binaire d’encodage par défaut est défini à 256 kbits/s pour stéréo et 192 kbps pour mono.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-240">The default encoding bit rate is set at 256 kbps for stereo and 192 kbps for mono.</span></span> <span data-ttu-id="ad1f5-241">Les paramètres par défaut sont reflétés dans les types de média retournés par la méthode [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-241">The default settings are reflected in the media types returned by the encoder's [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

### <a name="example-media-types"></a><span data-ttu-id="ad1f5-242">Exemples de types de média</span><span class="sxs-lookup"><span data-stu-id="ad1f5-242">Example Media Types</span></span>

<span data-ttu-id="ad1f5-243">Voici un exemple des types de médias nécessaires pour encoder le PCM d’entiers 16 bits, 48-kHz de l’audio stéréo à la vitesse de transmission par défaut de 256 kbits/s.</span><span class="sxs-lookup"><span data-stu-id="ad1f5-243">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate of 256 kbps.</span></span>

<span data-ttu-id="ad1f5-244">Type de média de sortie :</span><span class="sxs-lookup"><span data-stu-id="ad1f5-244">Output media type:</span></span>

| <span data-ttu-id="ad1f5-245">Attribut</span><span class="sxs-lookup"><span data-stu-id="ad1f5-245">Attribute</span></span>                                                                           | <span data-ttu-id="ad1f5-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad1f5-246">Value</span></span>                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="ad1f5-247">\_type de \_ majeurese MF MT \_</span><span class="sxs-lookup"><span data-stu-id="ad1f5-247">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="ad1f5-248">**MFMediaType \_ audio**</span><span class="sxs-lookup"><span data-stu-id="ad1f5-248">**MFMediaType\_Audio**</span></span>        |
| [<span data-ttu-id="ad1f5-249">\_sous- \_ type MF MT</span><span class="sxs-lookup"><span data-stu-id="ad1f5-249">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="ad1f5-250">**MFAudioFormat \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="ad1f5-250">**MFAudioFormat\_Dolby\_AC3**</span></span> |
| [<span data-ttu-id="ad1f5-251">\_ \_ échantillons audio MF \_ MT \_ par \_ seconde</span><span class="sxs-lookup"><span data-stu-id="ad1f5-251">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="ad1f5-252">48 000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-252">48000</span></span>                         |
| [<span data-ttu-id="ad1f5-253">\_canaux de \_ \_ numéros audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="ad1f5-253">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="ad1f5-254">2</span><span class="sxs-lookup"><span data-stu-id="ad1f5-254">2</span></span>                             |



 

<span data-ttu-id="ad1f5-255">Type de média d’entrée :</span><span class="sxs-lookup"><span data-stu-id="ad1f5-255">Input media type:</span></span>

| <span data-ttu-id="ad1f5-256">Attribut</span><span class="sxs-lookup"><span data-stu-id="ad1f5-256">Attribute</span></span>                                                                                | <span data-ttu-id="ad1f5-257">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad1f5-257">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="ad1f5-258">\_type de \_ majeurese MF MT \_</span><span class="sxs-lookup"><span data-stu-id="ad1f5-258">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="ad1f5-259">**MFMediaType \_ audio**</span><span class="sxs-lookup"><span data-stu-id="ad1f5-259">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="ad1f5-260">\_sous- \_ type MF MT</span><span class="sxs-lookup"><span data-stu-id="ad1f5-260">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="ad1f5-261">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="ad1f5-261">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="ad1f5-262">\_bits de \_ sortie audio MF \_ \_ par \_ échantillon</span><span class="sxs-lookup"><span data-stu-id="ad1f5-262">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="ad1f5-263">16</span><span class="sxs-lookup"><span data-stu-id="ad1f5-263">16</span></span>                     |
| [<span data-ttu-id="ad1f5-264">\_ \_ échantillons audio MF \_ MT \_ par \_ seconde</span><span class="sxs-lookup"><span data-stu-id="ad1f5-264">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="ad1f5-265">48 000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-265">48000</span></span>                  |
| [<span data-ttu-id="ad1f5-266">\_canaux de \_ \_ numéros audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="ad1f5-266">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="ad1f5-267">2</span><span class="sxs-lookup"><span data-stu-id="ad1f5-267">2</span></span>                      |
| [<span data-ttu-id="ad1f5-268">\_alignement de \_ \_ bloc audio MF MT \_</span><span class="sxs-lookup"><span data-stu-id="ad1f5-268">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="ad1f5-269">4</span><span class="sxs-lookup"><span data-stu-id="ad1f5-269">4</span></span>                      |
| [<span data-ttu-id="ad1f5-270">\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde</span><span class="sxs-lookup"><span data-stu-id="ad1f5-270">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="ad1f5-271">192000</span><span class="sxs-lookup"><span data-stu-id="ad1f5-271">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="ad1f5-272">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad1f5-272">Requirements</span></span>



| <span data-ttu-id="ad1f5-273">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad1f5-273">Requirement</span></span> | <span data-ttu-id="ad1f5-274">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad1f5-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad1f5-275">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad1f5-275">Minimum supported client</span></span><br/> | <span data-ttu-id="ad1f5-276">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ad1f5-276">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                       |
| <span data-ttu-id="ad1f5-277">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad1f5-277">Minimum supported server</span></span><br/> | <span data-ttu-id="ad1f5-278">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad1f5-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ad1f5-279">DLL</span><span class="sxs-lookup"><span data-stu-id="ad1f5-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad1f5-280"><dt>Msac3enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad1f5-280"><dt>Msac3enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad1f5-281">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad1f5-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad1f5-282">Objets codec</span><span class="sxs-lookup"><span data-stu-id="ad1f5-282">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 




