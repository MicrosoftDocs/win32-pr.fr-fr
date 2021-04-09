---
description: L’encodeur AAC Microsoft Media Foundation est une Media Foundation transformation qui encode le profil LC (Advanced Audio Coding) faible complexité (LC), tel que défini par la norme ISO/IEC 13818-7 (MPEG-2 audio part 7).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Encodeur AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9730ffc17d7ac3d5e16d86ef5aa20a46b329cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862757"
---
# <a name="aac-encoder"></a><span data-ttu-id="e0582-103">Encodeur AAC</span><span class="sxs-lookup"><span data-stu-id="e0582-103">AAC Encoder</span></span>

<span data-ttu-id="e0582-104">L’encodeur AAC Microsoft Media Foundation est une [Media Foundation transformation](media-foundation-transforms.md) qui encode le profil LC (Advanced Audio Coding) faible complexité (LC), tel que défini par la norme ISO/IEC 13818-7 (MPEG-2 audio part 7).</span><span class="sxs-lookup"><span data-stu-id="e0582-104">The Microsoft Media Foundation AAC encoder is a [Media Foundation Transform](media-foundation-transforms.md) that encodes Advanced Audio Coding (AAC) Low Complexity (LC) profile, as defined by ISO/IEC 13818-7 (MPEG-2 Audio Part 7) .</span></span>

<span data-ttu-id="e0582-105">L’encodeur AAC ne prend pas en charge l’encodage sur d’autres profils AAC, tels que main, SSR ou LTP.</span><span class="sxs-lookup"><span data-stu-id="e0582-105">The AAC encoder does not support encoding to any other AAC profiles, such as Main, SSR, or LTP.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="e0582-106">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="e0582-106">Class Identifier</span></span>

<span data-ttu-id="e0582-107">L’identificateur de classe (CLSID) de l’encodeur AAC est **CLSID \_ AACMFTEncoder**, défini dans le fichier d’en-tête wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="e0582-107">The class identifier (CLSID) of the AAC encoder is **CLSID\_AACMFTEncoder**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="e0582-108">Types de médias</span><span class="sxs-lookup"><span data-stu-id="e0582-108">Media Types</span></span>

<span data-ttu-id="e0582-109">L’encodeur AAC prend en charge les types de média suivants.</span><span class="sxs-lookup"><span data-stu-id="e0582-109">The AAC encoder supports the following media types.</span></span> <span data-ttu-id="e0582-110">Vous pouvez définir les types dans l’un ou l’autre type d’entrée de commande, ou le type de sortie en premier.</span><span class="sxs-lookup"><span data-stu-id="e0582-110">You can set the types in either order input type first, or output type first.</span></span>

### <a name="input-types"></a><span data-ttu-id="e0582-111">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="e0582-111">Input Types</span></span>

<span data-ttu-id="e0582-112">Définissez les attributs suivants sur le type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e0582-112">Set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0582-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="e0582-113">Attribute</span></span></th>
<th><span data-ttu-id="e0582-114">Description</span><span class="sxs-lookup"><span data-stu-id="e0582-114">Description</span></span></th>
<th><span data-ttu-id="e0582-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e0582-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0582-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0582-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="e0582-117">Type principal.</span><span class="sxs-lookup"><span data-stu-id="e0582-117">Major type.</span></span></td>
<td><span data-ttu-id="e0582-118">Doit être <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0582-118">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0582-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0582-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="e0582-120">Sous-type.</span><span class="sxs-lookup"><span data-stu-id="e0582-120">Subtype.</span></span></td>
<td><span data-ttu-id="e0582-121">Doit être <strong>MFAudioFormat_PCM</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0582-121">Must be <strong>MFAudioFormat_PCM</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0582-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0582-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="e0582-123">Bits par échantillon.</span><span class="sxs-lookup"><span data-stu-id="e0582-123">Bits per sample.</span></span></td>
<td><span data-ttu-id="e0582-124">Doit être 16.</span><span class="sxs-lookup"><span data-stu-id="e0582-124">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0582-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0582-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="e0582-126">Échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="e0582-126">Samples per second.</span></span></td>
<td><span data-ttu-id="e0582-127">Les valeurs suivantes sont admises :</span><span class="sxs-lookup"><span data-stu-id="e0582-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="e0582-128">44100 (44,1 KHz)</span><span class="sxs-lookup"><span data-stu-id="e0582-128">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="e0582-129">48000 (48 KHz)</span><span class="sxs-lookup"><span data-stu-id="e0582-129">48000 (48 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0582-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0582-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="e0582-131">Nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="e0582-131">Number of channels.</span></span></td>
<td><span data-ttu-id="e0582-132">Doit être 1 (mono) ou 2 (stéréo), ou 6 (5,1).</span><span class="sxs-lookup"><span data-stu-id="e0582-132">Must be 1 (mono) or 2 (stereo), or 6 (5.1).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0582-133">La prise en charge de 6 canaux audio a été introduite avec Windows 10 et n’est pas disponible pour les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="e0582-133">Support for 6 audio channels was introduced with Windows 10 and is not available for earlier versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e0582-134">Une fois que le type d’entrée est défini, l’encodeur dérive les valeurs suivantes et les ajoute au type de média :</span><span class="sxs-lookup"><span data-stu-id="e0582-134">After the input type is set, the encoder derives the following values and adds them to the media type:</span></span>

-   [<span data-ttu-id="e0582-135">**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="e0582-135">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="e0582-136">**\_alignement de \_ \_ bloc audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e0582-136">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="e0582-137">**\_vitesse de \_ \_ transmission moy. MF**</span><span class="sxs-lookup"><span data-stu-id="e0582-137">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a><span data-ttu-id="e0582-138">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="e0582-138">Output Types</span></span>

<span data-ttu-id="e0582-139">Définissez les attributs suivants sur le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="e0582-139">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0582-140">Attribut</span><span class="sxs-lookup"><span data-stu-id="e0582-140">Attribute</span></span></th>
<th><span data-ttu-id="e0582-141">Description</span><span class="sxs-lookup"><span data-stu-id="e0582-141">Description</span></span></th>
<th><span data-ttu-id="e0582-142">Notes</span><span class="sxs-lookup"><span data-stu-id="e0582-142">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0582-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0582-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="e0582-144">Type principal.</span><span class="sxs-lookup"><span data-stu-id="e0582-144">Major type.</span></span></td>
<td><span data-ttu-id="e0582-145">Doit être <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0582-145">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0582-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0582-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="e0582-147">Sous-type audio.</span><span class="sxs-lookup"><span data-stu-id="e0582-147">Audio subtype.</span></span></td>
<td><span data-ttu-id="e0582-148">Doit être <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="e0582-148">Must be <strong>MFAudioFormat_AAC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0582-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0582-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="e0582-150">Bits par échantillon.</span><span class="sxs-lookup"><span data-stu-id="e0582-150">Bits per sample.</span></span></td>
<td><span data-ttu-id="e0582-151">Doit être 16.</span><span class="sxs-lookup"><span data-stu-id="e0582-151">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0582-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0582-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="e0582-153">Échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="e0582-153">Samples per second.</span></span></td>
<td><span data-ttu-id="e0582-154">Doit correspondre au type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e0582-154">Must match the input type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0582-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0582-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="e0582-156">Nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="e0582-156">Number of channels.</span></span></td>
<td><span data-ttu-id="e0582-157">Doit correspondre au type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e0582-157">Must match the input type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0582-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0582-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="e0582-159">Vitesse de transmission du flux AAC encodé, en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="e0582-159">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="e0582-160">Les valeurs suivantes sont admises :</span><span class="sxs-lookup"><span data-stu-id="e0582-160">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="e0582-161">12 000</span><span class="sxs-lookup"><span data-stu-id="e0582-161">12000</span></span></li>
<li><span data-ttu-id="e0582-162">16000</span><span class="sxs-lookup"><span data-stu-id="e0582-162">16000</span></span></li>
<li><span data-ttu-id="e0582-163">20000</span><span class="sxs-lookup"><span data-stu-id="e0582-163">20000</span></span></li>
<li><span data-ttu-id="e0582-164">24 000</span><span class="sxs-lookup"><span data-stu-id="e0582-164">24000</span></span></li>
</ul>
<span data-ttu-id="e0582-165">La valeur par défaut pour mono et stéréo est 12000 (96 Kbits/s).</span><span class="sxs-lookup"><span data-stu-id="e0582-165">The default value for both mono and stereo is 12000 (96 Kbps).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0582-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="e0582-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="e0582-167">Type de charge utile AAC.</span><span class="sxs-lookup"><span data-stu-id="e0582-167">The AAC payload type.</span></span></td>
<td><span data-ttu-id="e0582-168">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e0582-168">Optional.</span></span> <span data-ttu-id="e0582-169">Si cette valeur est définie, la valeur doit être égale à zéro, ce qui indique que le flux contient uniquement des éléments raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="e0582-169">If set, the value must be zero, indicating that the stream contains raw_data_block elements only.</span></span><br/> <span data-ttu-id="e0582-170">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e0582-170">Optional.</span></span> <span data-ttu-id="e0582-171">Si l’attribut n’est pas défini, la valeur par défaut est zéro, ce qui indique que le flux contient uniquement des éléments de raw_data_block (AAC brut).</span><span class="sxs-lookup"><span data-stu-id="e0582-171">If the attribute is not set, the default value is zero, indicating that the stream contains raw_data_block elements only (raw AAC).</span></span> <br/> <span data-ttu-id="e0582-172">Dans Windows 7, si cet attribut est défini, la valeur doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="e0582-172">In Windows 7, if this attribute is set, the value must be zero.</span></span><br/> <span data-ttu-id="e0582-173">À compter de Windows 8, la valeur peut être 0 (AAC brut) ou 1 (ADTS AAC).</span><span class="sxs-lookup"><span data-stu-id="e0582-173">Starting in Windows 8, the value can be 0 (raw AAC) or 1 (ADTS AAC).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0582-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="e0582-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="e0582-175">Le niveau et le profil audio AAC.</span><span class="sxs-lookup"><span data-stu-id="e0582-175">The AAC audio profile and level.</span></span></td>
<td><span data-ttu-id="e0582-176">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="e0582-176">Optional.</span></span> <span data-ttu-id="e0582-177">Les valeurs suivantes sont admises :</span><span class="sxs-lookup"><span data-stu-id="e0582-177">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="e0582-178">0x29 (par défaut)</span><span class="sxs-lookup"><span data-stu-id="e0582-178">0x29 (default)</span></span></li>
<li><span data-ttu-id="e0582-179">0x2A</span><span class="sxs-lookup"><span data-stu-id="e0582-179">0x2A</span></span></li>
<li><span data-ttu-id="e0582-180">0x2B</span><span class="sxs-lookup"><span data-stu-id="e0582-180">0x2B</span></span></li>
<li><span data-ttu-id="e0582-181">0x2C</span><span class="sxs-lookup"><span data-stu-id="e0582-181">0x2C</span></span></li>
<li><span data-ttu-id="e0582-182">0x2E</span><span class="sxs-lookup"><span data-stu-id="e0582-182">0x2E</span></span></li>
<li><span data-ttu-id="e0582-183">0x2F</span><span class="sxs-lookup"><span data-stu-id="e0582-183">0x2F</span></span></li>
<li><span data-ttu-id="e0582-184">0x30</span><span class="sxs-lookup"><span data-stu-id="e0582-184">0x30</span></span></li>
<li><span data-ttu-id="e0582-185">0x31</span><span class="sxs-lookup"><span data-stu-id="e0582-185">0x31</span></span></li>
<li><span data-ttu-id="e0582-186">0x32</span><span class="sxs-lookup"><span data-stu-id="e0582-186">0x32</span></span></li>
<li><span data-ttu-id="e0582-187">0x33</span><span class="sxs-lookup"><span data-stu-id="e0582-187">0x33</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e0582-188">Le tableau suivant répertorie les valeurs qui peuvent être utilisées pour l’attribut MF_MT_AAC_PROFILE_LEVEL_INDICATION.</span><span class="sxs-lookup"><span data-stu-id="e0582-188">The following table lists the values that can be used for the MF_MT_AAC_PROFILE_LEVEL_INDICATION attribute.</span></span>

| <span data-ttu-id="e0582-189">Valeur MF_MT_AAC_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="e0582-189">MF_MT_AAC_PROFILE_LEVEL_INDICATION value</span></span> | <span data-ttu-id="e0582-190">Profil</span><span class="sxs-lookup"><span data-stu-id="e0582-190">Profile</span></span>                           |
|------------------------------------------|-----------------------------------|
| <span data-ttu-id="e0582-191">0x29</span><span class="sxs-lookup"><span data-stu-id="e0582-191">0x29</span></span>                                     | <span data-ttu-id="e0582-192">Profil AAC L2</span><span class="sxs-lookup"><span data-stu-id="e0582-192">AAC Profile L2</span></span>                    | 
| <span data-ttu-id="e0582-193">0x2A</span><span class="sxs-lookup"><span data-stu-id="e0582-193">0x2A</span></span>                                     | <span data-ttu-id="e0582-194">Profil AAC n4</span><span class="sxs-lookup"><span data-stu-id="e0582-194">AAC Profile L4</span></span>                    | 
| <span data-ttu-id="e0582-195">0x2B</span><span class="sxs-lookup"><span data-stu-id="e0582-195">0x2B</span></span>                                     | <span data-ttu-id="e0582-196">Profil AAC n5</span><span class="sxs-lookup"><span data-stu-id="e0582-196">AAC Profile L5</span></span>                    | 
| <span data-ttu-id="e0582-197">0x2C</span><span class="sxs-lookup"><span data-stu-id="e0582-197">0x2C</span></span>                                     | <span data-ttu-id="e0582-198">Niveau d’efficacité élevé du profil L2 v1</span><span class="sxs-lookup"><span data-stu-id="e0582-198">High Efficiency v1 AAC Profile L2</span></span> | 
| <span data-ttu-id="e0582-199">0x2E</span><span class="sxs-lookup"><span data-stu-id="e0582-199">0x2E</span></span>                                     | <span data-ttu-id="e0582-200">Niveau élevé d’efficacité v1 avec le profil AAC</span><span class="sxs-lookup"><span data-stu-id="e0582-200">High Efficiency v1 AAC Profile L4</span></span> | 
| <span data-ttu-id="e0582-201">0x2F</span><span class="sxs-lookup"><span data-stu-id="e0582-201">0x2F</span></span>                                     | <span data-ttu-id="e0582-202">Profil à haute performance v1 AAC-n5</span><span class="sxs-lookup"><span data-stu-id="e0582-202">High Efficiency v1 AAC Profile L5</span></span> | 
| <span data-ttu-id="e0582-203">0x30</span><span class="sxs-lookup"><span data-stu-id="e0582-203">0x30</span></span>                                     | <span data-ttu-id="e0582-204">Haut niveau d’efficacité 2 Profil AAC L2</span><span class="sxs-lookup"><span data-stu-id="e0582-204">High Efficiency v2 AAC Profile L2</span></span> | 
| <span data-ttu-id="e0582-205">0x31</span><span class="sxs-lookup"><span data-stu-id="e0582-205">0x31</span></span>                                     | <span data-ttu-id="e0582-206">Profil L3 v2 haute efficacité</span><span class="sxs-lookup"><span data-stu-id="e0582-206">High Efficiency v2 AAC Profile L3</span></span> | 
| <span data-ttu-id="e0582-207">0x32</span><span class="sxs-lookup"><span data-stu-id="e0582-207">0x32</span></span>                                     | <span data-ttu-id="e0582-208">High EFFICACITE v2 AAC Profile n4</span><span class="sxs-lookup"><span data-stu-id="e0582-208">High Efficiency v2 AAC Profile L4</span></span> | 
| <span data-ttu-id="e0582-209">0x33</span><span class="sxs-lookup"><span data-stu-id="e0582-209">0x33</span></span>                                     | <span data-ttu-id="e0582-210">Profil à haute efficacité v2 AAC-n5</span><span class="sxs-lookup"><span data-stu-id="e0582-210">High Efficiency v2 AAC Profile L5</span></span> | 

 

<span data-ttu-id="e0582-211">Une fois le type de sortie défini, l’encodeur AAC met à jour le type en ajoutant l’attribut de [**\_ \_ \_ données utilisateur MF MT**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e0582-211">After the output type is set, the AAC encoder updates the type by adding the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="e0582-212">Cet attribut contient la partie de la structure [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) qui apparaît après la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) (autrement dit, après le membre **wfx** ).</span><span class="sxs-lookup"><span data-stu-id="e0582-212">This attribute contains the portion of the [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure that appears after the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure (that is, after the **wfx** member).</span></span> <span data-ttu-id="e0582-213">Cela est suivi des données AudioSpecificConfig (), telles que définies par la norme ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="e0582-213">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="e0582-214">Chaque exemple de sortie contient une trame AAC compressée sans en-tête.</span><span class="sxs-lookup"><span data-stu-id="e0582-214">Each output sample contains one compressed AAC frame with no header.</span></span> <span data-ttu-id="e0582-215">Ce format est équivalent à l' \_ élément Raw Data \_ Block () défini par MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="e0582-215">This format is equivalent to the raw\_data\_block() element defined by MPEG-2.</span></span> <span data-ttu-id="e0582-216">S’il est présent dans le type de sortie, l’attribut de [ \_ \_ \_ \_ type de charge utile PP MT AAC](mf-mt-aac-payload-type.md) doit avoir la valeur zéro pour indiquer ce type de charge utile.</span><span class="sxs-lookup"><span data-stu-id="e0582-216">The [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) attribute, if present in the output type, must be set to zero to indicate this payload type.</span></span>

<span data-ttu-id="e0582-217">Chaque exemple de sortie contient une trame AAC compressée correspondant aux exemples PCM 1024.</span><span class="sxs-lookup"><span data-stu-id="e0582-217">Each output sample contains one compressed AAC frame corresponding to 1024 PCM samples.</span></span> <span data-ttu-id="e0582-218">Par exemple, à 48 kHz de taux d’échantillonnage, la durée d’un cadre compressé est de 21,33 ms.</span><span class="sxs-lookup"><span data-stu-id="e0582-218">For example, at 48 Khz sampling rate, the duration of one compressed frame is 21.33 msec.</span></span>

<span data-ttu-id="e0582-219">Si [le \_ \_ type de \_ charge \_ utile MT MT AAC](mf-mt-aac-payload-type.md) est égal à zéro (valeur par défaut), chaque exemple de sortie contient un \_ élément Raw Data \_ Block () tel que défini par la norme ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="e0582-219">If [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) is zero (the default value), each output sample contains one raw\_data\_block() element as defined by ISO/IEC 13818-7.</span></span>

## <a name="example-media-types"></a><span data-ttu-id="e0582-220">Exemples de types de média</span><span class="sxs-lookup"><span data-stu-id="e0582-220">Example Media Types</span></span>

<span data-ttu-id="e0582-221">Voici un exemple des types de médias nécessaires pour encoder du son stéréo 44,1-kHz, 160-kbps en AAC brut</span><span class="sxs-lookup"><span data-stu-id="e0582-221">Here is an example of the media types needed to encode from 44.1-kHz, 160-Kbps stereo audio to raw AAC</span></span>

<span data-ttu-id="e0582-222">Type de média d’entrée :</span><span class="sxs-lookup"><span data-stu-id="e0582-222">Input media type:</span></span>



| <span data-ttu-id="e0582-223">Attribut</span><span class="sxs-lookup"><span data-stu-id="e0582-223">Attribute</span></span>                                                                                    | <span data-ttu-id="e0582-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0582-224">Value</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="e0582-225">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e0582-225">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="e0582-226">**MFMediaType \_ audio**</span><span class="sxs-lookup"><span data-stu-id="e0582-226">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="e0582-227">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="e0582-227">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="e0582-228">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="e0582-228">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="e0582-229">**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**</span><span class="sxs-lookup"><span data-stu-id="e0582-229">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="e0582-230">16</span><span class="sxs-lookup"><span data-stu-id="e0582-230">16</span></span>                     |
| [<span data-ttu-id="e0582-231">**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="e0582-231">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="e0582-232">44100</span><span class="sxs-lookup"><span data-stu-id="e0582-232">44100</span></span>                  |
| [<span data-ttu-id="e0582-233">**\_canaux de \_ \_ numéros audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e0582-233">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="e0582-234">2</span><span class="sxs-lookup"><span data-stu-id="e0582-234">2</span></span>                      |
| [<span data-ttu-id="e0582-235">**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="e0582-235">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="e0582-236">176400 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e0582-236">176400 (optional)</span></span>      |
| [<span data-ttu-id="e0582-237">**\_alignement de \_ \_ bloc audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e0582-237">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="e0582-238">4 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e0582-238">4 (optional)</span></span>           |
| [<span data-ttu-id="e0582-239">**MF \_ MT \_ tous les \_ exemples \_ indépendants**</span><span class="sxs-lookup"><span data-stu-id="e0582-239">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="e0582-240">1 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e0582-240">1 (optional)</span></span>           |
| [<span data-ttu-id="e0582-241">**\_vitesse de \_ \_ transmission moy. MF**</span><span class="sxs-lookup"><span data-stu-id="e0582-241">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                  | <span data-ttu-id="e0582-242">1411200 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e0582-242">1411200 (optional)</span></span>     |
| [<span data-ttu-id="e0582-243">**\_exemples de \_ \_ taille fixe \_ MF MF**</span><span class="sxs-lookup"><span data-stu-id="e0582-243">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)                   | <span data-ttu-id="e0582-244">1 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e0582-244">1 (optional)</span></span>           |



 

<span data-ttu-id="e0582-245">Type de média de sortie :</span><span class="sxs-lookup"><span data-stu-id="e0582-245">Output media type:</span></span>



| <span data-ttu-id="e0582-246">Attribut</span><span class="sxs-lookup"><span data-stu-id="e0582-246">Attribute</span></span>                                                                                      | <span data-ttu-id="e0582-247">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0582-247">Value</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0582-248">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e0582-248">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="e0582-249">**MFMediaType \_ audio**</span><span class="sxs-lookup"><span data-stu-id="e0582-249">**MFMediaType\_Audio**</span></span>                                                                          |
| [<span data-ttu-id="e0582-250">**\_sous- \_ type MF MT**</span><span class="sxs-lookup"><span data-stu-id="e0582-250">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="e0582-251">**MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="e0582-251">**MFAudioFormat\_AAC**</span></span>                                                                          |
| [<span data-ttu-id="e0582-252">**\_bits de \_ sortie audio MF \_ \_ par \_ échantillon**</span><span class="sxs-lookup"><span data-stu-id="e0582-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="e0582-253">16</span><span class="sxs-lookup"><span data-stu-id="e0582-253">16</span></span>                                                                                              |
| [<span data-ttu-id="e0582-254">**\_ \_ échantillons audio MF \_ MT \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="e0582-254">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="e0582-255">44100</span><span class="sxs-lookup"><span data-stu-id="e0582-255">44100</span></span>                                                                                           |
| [<span data-ttu-id="e0582-256">**\_canaux de \_ \_ numéros audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e0582-256">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="e0582-257">2</span><span class="sxs-lookup"><span data-stu-id="e0582-257">2</span></span>                                                                                               |
| [<span data-ttu-id="e0582-258">**\_octets de \_ données audio MF MT- \_ \_ octets \_ par \_ seconde**</span><span class="sxs-lookup"><span data-stu-id="e0582-258">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="e0582-259">20000</span><span class="sxs-lookup"><span data-stu-id="e0582-259">20000</span></span>                                                                                           |
| [<span data-ttu-id="e0582-260">\_type de \_ \_ charge utile de l’AAC MT \_</span><span class="sxs-lookup"><span data-stu-id="e0582-260">MF\_MT\_AAC\_PAYLOAD\_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="e0582-261">0 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e0582-261">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="e0582-262">\_indication du \_ \_ niveau de \_ profil \_ audio MF MT AAC \_</span><span class="sxs-lookup"><span data-stu-id="e0582-262">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="e0582-263">0x29 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e0582-263">0x29 (optional)</span></span>                                                                                 |
| [<span data-ttu-id="e0582-264">**\_alignement de \_ \_ bloc audio MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e0582-264">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="e0582-265">1 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e0582-265">1 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="e0582-266">**MF \_ MT \_ tous les \_ exemples \_ indépendants**</span><span class="sxs-lookup"><span data-stu-id="e0582-266">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)           | <span data-ttu-id="e0582-267">0 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e0582-267">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="e0582-268">**\_vitesse de \_ \_ transmission moy. MF**</span><span class="sxs-lookup"><span data-stu-id="e0582-268">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                    | <span data-ttu-id="e0582-269">160000 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="e0582-269">160000 (optional)</span></span>                                                                               |
| [<span data-ttu-id="e0582-270">**\_ \_ données utilisateur MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="e0582-270">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="e0582-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} facultatif</span><span class="sxs-lookup"><span data-stu-id="e0582-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} (optional)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e0582-272">Notes</span><span class="sxs-lookup"><span data-stu-id="e0582-272">Remarks</span></span>

<span data-ttu-id="e0582-273">Dans l’implémentation actuelle, chaque exemple d’entrée doit avoir une durée et une durée valides.</span><span class="sxs-lookup"><span data-stu-id="e0582-273">In the current implementation, every input sample must have a valid time and duration.</span></span> <span data-ttu-id="e0582-274">Pour définir l’heure de l’exemple, appelez [**IMFSample :: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span><span class="sxs-lookup"><span data-stu-id="e0582-274">To set the sample time, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="e0582-275">Pour définir la durée de l’exemple, appelez [**IMFSample :: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span><span class="sxs-lookup"><span data-stu-id="e0582-275">To set the sample duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="e0582-276">Si l’heure de l’exemple n’est pas définie, la méthode [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) de l’encodeur retourne **MF \_ E \_ no \_ Sample \_ timestamp**.</span><span class="sxs-lookup"><span data-stu-id="e0582-276">If the sample time is not set, the encoder's [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method returns **MF\_E\_NO\_SAMPLE\_TIMESTAMP**.</span></span> <span data-ttu-id="e0582-277">Si la durée de l’échantillon n’est pas définie, la méthode **ProcessInput** retourne **MF \_ E \_ no \_ Sample \_ Duration**.</span><span class="sxs-lookup"><span data-stu-id="e0582-277">If the sample duration is not set, the **ProcessInput** method returns **MF\_E\_NO\_SAMPLE\_DURATION**.</span></span>

<span data-ttu-id="e0582-278">La durée de l’échantillon peut être calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="e0582-278">Sample duration can be calculated as follows:</span></span>


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



<span data-ttu-id="e0582-279">où *nAudioSamplesPerChannel* est le nombre d’échantillons audio PCM par canal dans la mémoire tampon d’entrée, et *nSamplesPerSec* est le taux d’échantillonnage, en échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="e0582-279">where *nAudioSamplesPerChannel* is the number of PCM audio samples per channel in the input buffer, and *nSamplesPerSec* is the sampling rate, in samples per second.</span></span>

> [!Note]  
> <span data-ttu-id="e0582-280">En raison d’un bogue dans l’implémentation actuelle, si la durée de l’échantillon est définie sur zéro, l’appel [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) a lieu, mais un appel ultérieur à [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) lèvera une exception de division par zéro.</span><span class="sxs-lookup"><span data-stu-id="e0582-280">Due to a bug in the current implementation, if the sample duration is set to zero, the [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) call succeeds, but a subsequent call to [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) will throw a divide-by-zero exception.</span></span> <span data-ttu-id="e0582-281">Pour éviter cette erreur, définissez une durée différente de zéro valide pour chaque exemple d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e0582-281">To avoid this error, set a valid nonzero duration on each input sample.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e0582-282">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0582-282">Requirements</span></span>



| <span data-ttu-id="e0582-283">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0582-283">Requirement</span></span> | <span data-ttu-id="e0582-284">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0582-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0582-285">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0582-285">Minimum supported client</span></span><br/> | <span data-ttu-id="e0582-286">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0582-286">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e0582-287">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0582-287">Minimum supported server</span></span><br/> | <span data-ttu-id="e0582-288">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0582-288">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e0582-289">DLL</span><span class="sxs-lookup"><span data-stu-id="e0582-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0582-290"><dt>Mfaacenc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0582-290"><dt>Mfaacenc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0582-291">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0582-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0582-292">Objets codec</span><span class="sxs-lookup"><span data-stu-id="e0582-292">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="e0582-293">**Décodeur AAC**</span><span class="sxs-lookup"><span data-stu-id="e0582-293">**AAC Decoder**</span></span>](aac-decoder.md)
</dt> <dt>

[<span data-ttu-id="e0582-294">Types de média AAC</span><span class="sxs-lookup"><span data-stu-id="e0582-294">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="e0582-295">Types de média audio</span><span class="sxs-lookup"><span data-stu-id="e0582-295">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="e0582-296">Prise en charge MPEG-4 dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0582-296">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="e0582-297">Formats multimédias pris en charge dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0582-297">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

