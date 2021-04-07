---
description: Le décodeur Dolby audio est une table MFT qui décode Dolby Digital (AC-3) et Dolby Digital plus.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Décodeur audio Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749261"
---
# <a name="dolby-audio-decoder"></a><span data-ttu-id="1fb52-103">Décodeur audio Dolby</span><span class="sxs-lookup"><span data-stu-id="1fb52-103">Dolby Audio Decoder</span></span>

<span data-ttu-id="1fb52-104">Le décodeur Dolby audio est une [Media Foundation transformation](media-foundation-transforms.md) (MFT) qui décode les types de flux suivants :</span><span class="sxs-lookup"><span data-stu-id="1fb52-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that decodes the following stream types:</span></span>

-   <span data-ttu-id="1fb52-105">Dolby Digital, également appelé Dolby AC-3</span><span class="sxs-lookup"><span data-stu-id="1fb52-105">Dolby Digital, also called Dolby AC-3</span></span>
-   <span data-ttu-id="1fb52-106">Dolby Digital plus, également appelé AC-3 amélioré (E-AC-3)</span><span class="sxs-lookup"><span data-stu-id="1fb52-106">Dolby Digital Plus, also called Enhanced AC-3 (E-AC-3)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1fb52-107">Pour les versions de Windows antérieures à Windows 8, l’implémentation Microsoft de la technologie Dolby Digital est limitée aux termes du programme de gestion de licences Dolby Digital à utiliser par les applications Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1fb52-107">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="1fb52-108">Pour plus d’informations sur ces formats, reportez-vous à la version B du document de la *norme de compression audio numérique (ATSC-3, E-AC-3)*.</span><span class="sxs-lookup"><span data-stu-id="1fb52-108">For more information about these formats, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

<span data-ttu-id="1fb52-109">Le décodeur peut également convertir un flux Dolby Digital plus en format Dolby Digital pour la sortie AC-3 S/PIDF, ou formater un flux Dolby Digital plus pour la sortie numérique HDMI.</span><span class="sxs-lookup"><span data-stu-id="1fb52-109">The decoder can also convert a Dolby Digital Plus stream to Dolby Digital format for AC-3 S/PIDF output, or format a Dolby Digital Plus stream for HDMI digital output.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="1fb52-110">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="1fb52-110">Class Identifier</span></span>

<span data-ttu-id="1fb52-111">L’identificateur de classe (CLSID) du décodeur Dolby audio est **CLSID \_ CMSDDPlusDecMFT**, défini dans le fichier d’en-tête wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="1fb52-111">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDDPlusDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="1fb52-112">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="1fb52-112">Input Types</span></span>

<span data-ttu-id="1fb52-113">Le décodeur audio Dolby prend en charge les sous-types d’entrée suivants.</span><span class="sxs-lookup"><span data-stu-id="1fb52-113">The Dolby audio decoder supports the following input subtypes.</span></span>



| <span data-ttu-id="1fb52-114">Subtype</span><span class="sxs-lookup"><span data-stu-id="1fb52-114">Subtype</span></span>                                 | <span data-ttu-id="1fb52-115">Description</span><span class="sxs-lookup"><span data-stu-id="1fb52-115">Description</span></span>                                                                                                                                                 | <span data-ttu-id="1fb52-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fb52-116">Header</span></span>       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="1fb52-117">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="1fb52-117">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>            | <span data-ttu-id="1fb52-118">Audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="1fb52-118">Dolby Digital audio.</span></span>                                                                                                                                        | <span data-ttu-id="1fb52-119">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="1fb52-119">mfapi.h</span></span>      |
| <span data-ttu-id="1fb52-120">**MEDIASUBTYPE \_ DVM**</span><span class="sxs-lookup"><span data-stu-id="1fb52-120">**MEDIASUBTYPE\_DVM**</span></span>                   | <span data-ttu-id="1fb52-121">Audio Dolby Digital ; consultez [**sous-types audio**](../directshow/audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="1fb52-121">Dolby Digital audio; see [**Audio Subtypes**](../directshow/audio-subtypes.md).</span></span> <span data-ttu-id="1fb52-122">Ce sous-type peut être utilisé de façon interchangeable avec **MEDIASUBTYPE \_ Dolby \_ AC3**.</span><span class="sxs-lookup"><span data-stu-id="1fb52-122">This subtype can be used interchangeably with **MEDIASUBTYPE\_DOLBY\_AC3**.</span></span><br/> | <span data-ttu-id="1fb52-123">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="1fb52-123">wmcodecdsp.h</span></span> |
| <span data-ttu-id="1fb52-124">**MFAudioFormat \_ Dolby \_ Digital \_ plus**</span><span class="sxs-lookup"><span data-stu-id="1fb52-124">**MFAudioFormat\_Dolby\_Digital\_Plus**</span></span> | <span data-ttu-id="1fb52-125">Audio Dolby Digital plus.</span><span class="sxs-lookup"><span data-stu-id="1fb52-125">Dolby Digital Plus audio.</span></span>                                                                                                                                   | <span data-ttu-id="1fb52-126">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="1fb52-126">mfapi.h</span></span>      |



 

<span data-ttu-id="1fb52-127">Le tableau suivant répertorie les attributs requis et facultatifs pour le type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1fb52-127">The following table lists the requires and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fb52-128">Attribut</span><span class="sxs-lookup"><span data-stu-id="1fb52-128">Attribute</span></span></th>
<th><span data-ttu-id="1fb52-129">Description</span><span class="sxs-lookup"><span data-stu-id="1fb52-129">Description</span></span></th>
<th><span data-ttu-id="1fb52-130">Notes</span><span class="sxs-lookup"><span data-stu-id="1fb52-130">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fb52-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="1fb52-132">Type principal.</span><span class="sxs-lookup"><span data-stu-id="1fb52-132">Major type.</span></span></td>
<td><span data-ttu-id="1fb52-133">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1fb52-133">Required.</span></span> <span data-ttu-id="1fb52-134">Doit être <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="1fb52-134">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb52-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="1fb52-136">Sous-type audio.</span><span class="sxs-lookup"><span data-stu-id="1fb52-136">Audio subtype.</span></span></td>
<td><span data-ttu-id="1fb52-137">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1fb52-137">Required.</span></span> <span data-ttu-id="1fb52-138">Pour plus d’informations, consultez le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="1fb52-138">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb52-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="1fb52-140">Taux d’échantillonnage, en échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="1fb52-140">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="1fb52-141">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1fb52-141">Optional.</span></span> <span data-ttu-id="1fb52-142">Les valeurs valides sont les suivantes : 48000, 44100, 32000, 24000, 22050 et 16000.</span><span class="sxs-lookup"><span data-stu-id="1fb52-142">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="1fb52-143">Si cet attribut n’est pas défini, la valeur par défaut est 48000.</span><span class="sxs-lookup"><span data-stu-id="1fb52-143">If this attribute is not set, the default value is 48000.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1fb52-144">Les flux Dolby AC-3 sont limités aux trois tarifs les plus élevés de cette liste.</span><span class="sxs-lookup"><span data-stu-id="1fb52-144">Dolby AC-3 streams are limited to the three highest rates in this list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb52-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="1fb52-146">Nombre de canaux, y compris le canal à fréquence faible (LFE), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1fb52-146">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="1fb52-147">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1fb52-147">Optional.</span></span> <span data-ttu-id="1fb52-148">Les valeurs valides sont comprises entre 1 (mono) et 8 (configuration de canal 7,1).</span><span class="sxs-lookup"><span data-stu-id="1fb52-148">Valid values are in the range 1 (mono) to 8 (7.1 channel configuration).</span></span> <span data-ttu-id="1fb52-149">Si cet attribut n’est pas défini, la valeur par défaut est 2 (stéréo).</span><span class="sxs-lookup"><span data-stu-id="1fb52-149">If this attribute is not set, the default value is 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb52-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="1fb52-151">Spécifie l’affectation des canaux audio aux positions des haut-parleurs.</span><span class="sxs-lookup"><span data-stu-id="1fb52-151">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="1fb52-152">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1fb52-152">Optional.</span></span> <span data-ttu-id="1fb52-153">S’il est spécifié, la valeur doit être cohérente avec le nombre de canaux audio.</span><span class="sxs-lookup"><span data-stu-id="1fb52-153">If specified, the value must be consistent with the number of audio channels.</span></span> <span data-ttu-id="1fb52-154">Si l’attribut n’est pas défini, le décodeur utilise un masque de canal par défaut, en fonction du nombre de canaux.</span><span class="sxs-lookup"><span data-stu-id="1fb52-154">If the attribute is not set, the decoder uses a default channel mask, based on the number of channels.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1fb52-155">Le tableau suivant répertorie les configurations Dolby Channel prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1fb52-155">The following table lists the supported Dolby channel configurations.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fb52-156">Configuration du canal</span><span class="sxs-lookup"><span data-stu-id="1fb52-156">Channel configuration</span></span></th>
<th><span data-ttu-id="1fb52-157">Nombre de canaux</span><span class="sxs-lookup"><span data-stu-id="1fb52-157">Number of channels</span></span></th>
<th><span data-ttu-id="1fb52-158">Masques de canal</span><span class="sxs-lookup"><span data-stu-id="1fb52-158">Channel masks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fb52-159">1/0 (mono)</span><span class="sxs-lookup"><span data-stu-id="1fb52-159">1/0 (mono)</span></span></td>
<td><span data-ttu-id="1fb52-160">1</span><span class="sxs-lookup"><span data-stu-id="1fb52-160">1</span></span></td>
<td><span data-ttu-id="1fb52-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="1fb52-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb52-162">2/0 (stéréo) ou 1 + 1 (double mono)</span><span class="sxs-lookup"><span data-stu-id="1fb52-162">2/0 (stereo) or 1+1 (dual mono)</span></span></td>
<td><span data-ttu-id="1fb52-163">2</span><span class="sxs-lookup"><span data-stu-id="1fb52-163">2</span></span></td>
<td><span data-ttu-id="1fb52-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="1fb52-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb52-165">3/0</span><span class="sxs-lookup"><span data-stu-id="1fb52-165">3/0</span></span></td>
<td><span data-ttu-id="1fb52-166">3</span><span class="sxs-lookup"><span data-stu-id="1fb52-166">3</span></span></td>
<td><span data-ttu-id="1fb52-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span><span class="sxs-lookup"><span data-stu-id="1fb52-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb52-168">2/1</span><span class="sxs-lookup"><span data-stu-id="1fb52-168">2/1</span></span></td>
<td><span data-ttu-id="1fb52-169">3</span><span class="sxs-lookup"><span data-stu-id="1fb52-169">3</span></span></td>
<td><span data-ttu-id="1fb52-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="1fb52-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb52-171">3/1</span><span class="sxs-lookup"><span data-stu-id="1fb52-171">3/1</span></span></td>
<td><span data-ttu-id="1fb52-172">4</span><span class="sxs-lookup"><span data-stu-id="1fb52-172">4</span></span></td>
<td><span data-ttu-id="1fb52-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="1fb52-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb52-174">2/2</span><span class="sxs-lookup"><span data-stu-id="1fb52-174">2/2</span></span></td>
<td><span data-ttu-id="1fb52-175">4</span><span class="sxs-lookup"><span data-stu-id="1fb52-175">4</span></span></td>
<td><span data-ttu-id="1fb52-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="1fb52-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="1fb52-177">ou</span><span class="sxs-lookup"><span data-stu-id="1fb52-177">or</span></span><br/> <span data-ttu-id="1fb52-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="1fb52-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb52-179">3/2</span><span class="sxs-lookup"><span data-stu-id="1fb52-179">3/2</span></span></td>
<td><span data-ttu-id="1fb52-180">5</span><span class="sxs-lookup"><span data-stu-id="1fb52-180">5</span></span></td>
<td><span data-ttu-id="1fb52-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="1fb52-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="1fb52-182">ou</span><span class="sxs-lookup"><span data-stu-id="1fb52-182">or</span></span><br/> <span data-ttu-id="1fb52-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="1fb52-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb52-184">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="1fb52-184">3/2 + LFE</span></span></td>
<td><span data-ttu-id="1fb52-185">6</span><span class="sxs-lookup"><span data-stu-id="1fb52-185">6</span></span></td>
<td><span data-ttu-id="1fb52-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="1fb52-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="1fb52-187">ou</span><span class="sxs-lookup"><span data-stu-id="1fb52-187">or</span></span><br/> <span data-ttu-id="1fb52-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="1fb52-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb52-189">3/2/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="1fb52-189">3/2/2 + LFE</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="1fb52-190">Dolby Digital plus uniquement.</span><span class="sxs-lookup"><span data-stu-id="1fb52-190">Dolby Digital Plus only.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="1fb52-191">8</span><span class="sxs-lookup"><span data-stu-id="1fb52-191">8</span></span></td>
<td><span data-ttu-id="1fb52-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span><span class="sxs-lookup"><span data-stu-id="1fb52-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1fb52-193">En outre, les configurations de canal 1/0, 2/0, 3/0, 2/1, 3/1 et 2/2 peuvent également apparaître avec un canal LFE.</span><span class="sxs-lookup"><span data-stu-id="1fb52-193">In addition, channel configurations 1/0, 2/0, 3/0, 2/1, 3/1, and 2/2 may also appear with an LFE channel.</span></span>

## <a name="output-types"></a><span data-ttu-id="1fb52-194">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="1fb52-194">Output Types</span></span>

<span data-ttu-id="1fb52-195">Le décodeur audio Dolby prend en charge les sous-types de sortie suivants.</span><span class="sxs-lookup"><span data-stu-id="1fb52-195">The Dolby audio decoder supports the following output subtypes.</span></span>



| <span data-ttu-id="1fb52-196">Subtype</span><span class="sxs-lookup"><span data-stu-id="1fb52-196">Subtype</span></span>                                                   | <span data-ttu-id="1fb52-197">Description</span><span class="sxs-lookup"><span data-stu-id="1fb52-197">Description</span></span>                                                                                                                               | <span data-ttu-id="1fb52-198">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fb52-198">Header</span></span>    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1fb52-199">**MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**</span><span class="sxs-lookup"><span data-stu-id="1fb52-199">**MFAudioFormat\_Dolby\_AC3\_SPDIF**</span></span>                      | <span data-ttu-id="1fb52-200">Audio Dolby AC-3 formaté pour la sortie numérique S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="1fb52-200">Dolby AC-3 audio formatted for S/PDIF digital output.</span></span>                                                                                     | <span data-ttu-id="1fb52-201">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="1fb52-201">mfapi.h</span></span>   |
| <span data-ttu-id="1fb52-202">**KSDATAFORMAT \_ sous-type \_ IEC61937 \_ Dolby \_ Digital \_ plus**</span><span class="sxs-lookup"><span data-stu-id="1fb52-202">**KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**</span></span> | <span data-ttu-id="1fb52-203">Audio Dolby Digital plus formaté pour la sortie numérique HDMI.</span><span class="sxs-lookup"><span data-stu-id="1fb52-203">Dolby Digital Plus audio formatted for HDMI digital output.</span></span>                                                                               | <span data-ttu-id="1fb52-204">ksmedia. h</span><span class="sxs-lookup"><span data-stu-id="1fb52-204">ksmedia.h</span></span> |
| <span data-ttu-id="1fb52-205">**MFAudioFormat \_ float**</span><span class="sxs-lookup"><span data-stu-id="1fb52-205">**MFAudioFormat\_Float**</span></span>                                  | <span data-ttu-id="1fb52-206">Audio PCM à virgule flottante IEEE 32 bits</span><span class="sxs-lookup"><span data-stu-id="1fb52-206">IEEE 32-bit floating-point PCM audio</span></span><br/> <span data-ttu-id="1fb52-207">**Windows 10**: stéréo, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="1fb52-207">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="1fb52-208">**Versions précédentes**: stéréo, 5,1</span><span class="sxs-lookup"><span data-stu-id="1fb52-208">**Previous versions**: stereo, 5.1</span></span><br/> | <span data-ttu-id="1fb52-209">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="1fb52-209">mfapi.h</span></span>   |
| <span data-ttu-id="1fb52-210">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="1fb52-210">**MFAudioFormat\_PCM**</span></span>                                    | <span data-ttu-id="1fb52-211">audio PCM 16 bits</span><span class="sxs-lookup"><span data-stu-id="1fb52-211">16-bit PCM audio</span></span><br/> <span data-ttu-id="1fb52-212">**Windows 10**: stéréo, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="1fb52-212">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="1fb52-213">**Versions précédentes**: stéréo, 5,1</span><span class="sxs-lookup"><span data-stu-id="1fb52-213">**Previous versions**: stereo, 5.1</span></span><br/>                     | <span data-ttu-id="1fb52-214">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="1fb52-214">mfapi.h</span></span>   |



 

<span data-ttu-id="1fb52-215">Le tableau suivant répertorie les attributs obligatoires et facultatifs pour le type de média de sortie.</span><span class="sxs-lookup"><span data-stu-id="1fb52-215">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fb52-216">Attribut</span><span class="sxs-lookup"><span data-stu-id="1fb52-216">Attribute</span></span></th>
<th><span data-ttu-id="1fb52-217">Description</span><span class="sxs-lookup"><span data-stu-id="1fb52-217">Description</span></span></th>
<th><span data-ttu-id="1fb52-218">Notes</span><span class="sxs-lookup"><span data-stu-id="1fb52-218">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fb52-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="1fb52-220">Type principal.</span><span class="sxs-lookup"><span data-stu-id="1fb52-220">Major type.</span></span></td>
<td><span data-ttu-id="1fb52-221">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1fb52-221">Required.</span></span> <span data-ttu-id="1fb52-222">Doit être <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="1fb52-222">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb52-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="1fb52-224">Sous-type audio.</span><span class="sxs-lookup"><span data-stu-id="1fb52-224">Audio subtype.</span></span></td>
<td><span data-ttu-id="1fb52-225">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1fb52-225">Required.</span></span> <span data-ttu-id="1fb52-226">Pour plus d’informations, consultez le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="1fb52-226">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb52-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="1fb52-228">Taux d’échantillonnage, en échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="1fb52-228">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="1fb52-229">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1fb52-229">Required.</span></span> <span data-ttu-id="1fb52-230">Les valeurs valides sont les suivantes : 48000, 44100, 32000, 24000, 22050 et 16000.</span><span class="sxs-lookup"><span data-stu-id="1fb52-230">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="1fb52-231">Le taux d’échantillonnage de sortie doit être identique au taux d’échantillonnage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1fb52-231">The output sample rate must be identical to the input sample rate.</span></span> <span data-ttu-id="1fb52-232">Le décodeur ne peut pas modifier la fréquence d’échantillonnage du flux.</span><span class="sxs-lookup"><span data-stu-id="1fb52-232">The decoder cannot change the sampling rate of the stream.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb52-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="1fb52-234">Nombre de canaux, y compris le canal à fréquence faible (LFE), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1fb52-234">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="1fb52-235">Requis pour la sortie PCM.</span><span class="sxs-lookup"><span data-stu-id="1fb52-235">Required for PCM output.</span></span> <br/> <span data-ttu-id="1fb52-236">Non nécessaire pour la sortie numérique.</span><span class="sxs-lookup"><span data-stu-id="1fb52-236">Not needed for digital output.</span></span> <br/> <span data-ttu-id="1fb52-237">Si le type d’entrée est mono, stéréo ou double-mono (tout sans canal LFE), la seule valeur valide est 2, pour la sortie stéréo.</span><span class="sxs-lookup"><span data-stu-id="1fb52-237">If the input type is mono, stereo, or dual-mono (all without LFE channel), the only valid value is 2, for stereo output.</span></span> <span data-ttu-id="1fb52-238">Dans le cas contraire, la valeur peut être :</span><span class="sxs-lookup"><span data-stu-id="1fb52-238">Otherwise, the value can be:</span></span> <br/>
<ul>
<li><span data-ttu-id="1fb52-239">2 pour downmix stéréo</span><span class="sxs-lookup"><span data-stu-id="1fb52-239">2 for stereo downmix</span></span></li>
<li><span data-ttu-id="1fb52-240">6 pour les configurations de canal 5,1</span><span class="sxs-lookup"><span data-stu-id="1fb52-240">6 for 5.1 channel configurations</span></span></li>
<li><span data-ttu-id="1fb52-241">8 pour les configurations de canal 7,1</span><span class="sxs-lookup"><span data-stu-id="1fb52-241">8 for 7.1 channel configurations</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb52-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="1fb52-243">Spécifie l’affectation des canaux audio aux positions des haut-parleurs.</span><span class="sxs-lookup"><span data-stu-id="1fb52-243">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="1fb52-244">Requis pour la sortie PCM si le nombre de canaux est supérieur à 2.</span><span class="sxs-lookup"><span data-stu-id="1fb52-244">Required for PCM output if the number of channels is greater than 2.</span></span> <span data-ttu-id="1fb52-245">La valeur doit être :</span><span class="sxs-lookup"><span data-stu-id="1fb52-245">The value must be:</span></span><br/>
<ul>
<li><span data-ttu-id="1fb52-246">0x3 pour sortie stéréo</span><span class="sxs-lookup"><span data-stu-id="1fb52-246">0x3 for stereo output</span></span></li>
<li><span data-ttu-id="1fb52-247">0x3F pour sortie de canal 5,1</span><span class="sxs-lookup"><span data-stu-id="1fb52-247">0x3F for 5.1 channel output</span></span></li>
<li><span data-ttu-id="1fb52-248">0x63F pour la sortie du canal 7,1</span><span class="sxs-lookup"><span data-stu-id="1fb52-248">0x63F for 7.1 channel output</span></span></li>
</ul>
<span data-ttu-id="1fb52-249">Non nécessaire pour la sortie numérique.</span><span class="sxs-lookup"><span data-stu-id="1fb52-249">Not needed for digital output.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb52-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="1fb52-251">Nombre de bits par échantillon audio.</span><span class="sxs-lookup"><span data-stu-id="1fb52-251">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="1fb52-252">Requis pour la sortie PCM.</span><span class="sxs-lookup"><span data-stu-id="1fb52-252">Required for PCM output.</span></span> <span data-ttu-id="1fb52-253">La valeur doit être 32 pour <strong>MFAudioFormat_Float</strong>, et 16 pour <strong>MFAudioFormat_PCM</strong>.</span><span class="sxs-lookup"><span data-stu-id="1fb52-253">The value must be 32 for <strong>MFAudioFormat_Float</strong>, and 16 for <strong>MFAudioFormat_PCM</strong>.</span></span><br/> <span data-ttu-id="1fb52-254">Non nécessaire pour la sortie numérique.</span><span class="sxs-lookup"><span data-stu-id="1fb52-254">Not needed for digital output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb52-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="1fb52-256">Nombre de bits de données audio valides dans chaque exemple audio.</span><span class="sxs-lookup"><span data-stu-id="1fb52-256">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="1fb52-257">Facultatif pour la sortie PCM.</span><span class="sxs-lookup"><span data-stu-id="1fb52-257">Optional for PCM output.</span></span> <span data-ttu-id="1fb52-258">Si cette valeur est définie, la valeur doit être identique à <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="1fb52-258">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span><br/> <span data-ttu-id="1fb52-259">Non nécessaire pour les sous-types de sortie numérique.</span><span class="sxs-lookup"><span data-stu-id="1fb52-259">Not needed for the digital output subtypes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fb52-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="1fb52-261">Alignement de bloc, en octets.</span><span class="sxs-lookup"><span data-stu-id="1fb52-261">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="1fb52-262">Facultatif pour la sortie PCM.</span><span class="sxs-lookup"><span data-stu-id="1fb52-262">Optional for PCM output.</span></span> <span data-ttu-id="1fb52-263">Non nécessaire pour la sortie numérique.</span><span class="sxs-lookup"><span data-stu-id="1fb52-263">Not needed for digital output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fb52-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="1fb52-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="1fb52-265">Nombre moyen d’octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="1fb52-265">Average number of bytes per second.</span></span></td>
<td><span data-ttu-id="1fb52-266">Facultatif pour la sortie PCM.</span><span class="sxs-lookup"><span data-stu-id="1fb52-266">Optional for PCM output.</span></span> <span data-ttu-id="1fb52-267">Non nécessaire pour la sortie numérique.</span><span class="sxs-lookup"><span data-stu-id="1fb52-267">Not needed for digital output.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a><span data-ttu-id="1fb52-268">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="1fb52-268">Transform Attributes</span></span>

<span data-ttu-id="1fb52-269">Le décodeur audio Dolby implémente la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="1fb52-269">The Dolby audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="1fb52-270">L’application peut utiliser cette méthode pour récupérer ou définir les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="1fb52-270">The application can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="1fb52-271">Attribut</span><span class="sxs-lookup"><span data-stu-id="1fb52-271">Attribute</span></span>                                                                                | <span data-ttu-id="1fb52-272">Description</span><span class="sxs-lookup"><span data-stu-id="1fb52-272">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1fb52-273">CODECAPI \_ AVDecAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="1fb52-273">CODECAPI\_AVDecAudioDualMono</span></span>](../directshow/avdecaudiodualmono-property.md)                        | <span data-ttu-id="1fb52-274">Spécifie si un flux audio Dolby à 2 canaux est encodé en stéréo ou en double mono.</span><span class="sxs-lookup"><span data-stu-id="1fb52-274">Specifies whether a 2-channel Dolby audio stream is encoded as stereo or dual-mono.</span></span> <span data-ttu-id="1fb52-275">Avant que la première trame Dolby soit décodée, la valeur est **EAVDecAudioDualMono \_ non spécifié**.</span><span class="sxs-lookup"><span data-stu-id="1fb52-275">Before the first Dolby frame is decoded, the value is **eAVDecAudioDualMono\_UnSpecified**.</span></span> <span data-ttu-id="1fb52-276">Une fois le décodage commencé, la valeur reflète le frame Dolby le plus récent.</span><span class="sxs-lookup"><span data-stu-id="1fb52-276">After decoding begins, the value reflects the most recent Dolby frame.</span></span><br/> <span data-ttu-id="1fb52-277">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1fb52-277">Read-only.</span></span> <br/> |
| [<span data-ttu-id="1fb52-278">CODECAPI \_ AVDecAudioDualMonoReproMode</span><span class="sxs-lookup"><span data-stu-id="1fb52-278">CODECAPI\_AVDecAudioDualMonoReproMode</span></span>](../directshow/avdecaudiodualmonorepromode-property.md)      | <span data-ttu-id="1fb52-279">Spécifie la manière dont le décodeur reproduit le son double mono.</span><span class="sxs-lookup"><span data-stu-id="1fb52-279">Specifies how the decoder reproduces dual-mono audio.</span></span> <span data-ttu-id="1fb52-280">La valeur par défaut **est \_ eAVDecAudioDualMonoReproMode \_ mono gauche**.</span><span class="sxs-lookup"><span data-stu-id="1fb52-280">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span> <span data-ttu-id="1fb52-281">L’application peut définir cette propriété à tout moment.</span><span class="sxs-lookup"><span data-stu-id="1fb52-281">The application can set this property at any time.</span></span><br/> <span data-ttu-id="1fb52-282">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1fb52-282">Read/write.</span></span><br/>                                                                            |
| [<span data-ttu-id="1fb52-283">CODECAPI \_ AVDecCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="1fb52-283">CODECAPI\_AVDecCommonMeanBitRate</span></span>](../directshow/avdeccommonmeanbitrate.md)                         | <span data-ttu-id="1fb52-284">Pour les flux Dolby Digital (AC-3), spécifie la vitesse de transmission du flux d’entrée en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="1fb52-284">For Dolby Digital (AC-3) streams, specifies the bit rate of the input stream in bits per second.</span></span> <span data-ttu-id="1fb52-285">Pour Dolby Digital plus (E-AC3), la valeur est toujours égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1fb52-285">For Dolby Digital Plus (E-AC3), the value is always zero.</span></span><br/> <span data-ttu-id="1fb52-286">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1fb52-286">Read only.</span></span><br/>                                                                                              |
| [<span data-ttu-id="1fb52-287">CODECAPI \_ AVDecDDDynamicRangeScaleHigh</span><span class="sxs-lookup"><span data-stu-id="1fb52-287">CODECAPI\_AVDecDDDynamicRangeScaleHigh</span></span>](../directshow/avdecdddynamicrangescalehigh-property.md)    | <span data-ttu-id="1fb52-288">La coupe de haut niveau lorsque le décodeur effectue un contrôle de plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="1fb52-288">The high-level cut when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="1fb52-289">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1fb52-289">Read/write.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="1fb52-290">CODECAPI \_ AVDecDDDynamicRangeScaleLow</span><span class="sxs-lookup"><span data-stu-id="1fb52-290">CODECAPI\_AVDecDDDynamicRangeScaleLow</span></span>](../directshow/avdecdddynamicrangescalelow-property.md)      | <span data-ttu-id="1fb52-291">Renforcement de bas niveau lorsque le décodeur effectue un contrôle de plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="1fb52-291">The low-level boost when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="1fb52-292">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1fb52-292">Read/write.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="1fb52-293">CODECAPI \_ AVDecDDOperationalMode</span><span class="sxs-lookup"><span data-stu-id="1fb52-293">CODECAPI\_AVDecDDOperationalMode</span></span>](../directshow/avdecddoperationalmode-property.md)                | <span data-ttu-id="1fb52-294">Mode de contrôle de compression.</span><span class="sxs-lookup"><span data-stu-id="1fb52-294">The compression control mode.</span></span><br/> <span data-ttu-id="1fb52-295">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1fb52-295">Read/write.</span></span><br/>                                                                                                                                                                                                                          |
| [<span data-ttu-id="1fb52-296">CODECAPI \_ AVDecDDStereoDownMixMode</span><span class="sxs-lookup"><span data-stu-id="1fb52-296">CODECAPI\_AVDecDDStereoDownMixMode</span></span>](codecapi-avdecddstereodownmixmode.md)              | <span data-ttu-id="1fb52-297">Type de downmix stéréo.</span><span class="sxs-lookup"><span data-stu-id="1fb52-297">The type of stereo downmix.</span></span> <span data-ttu-id="1fb52-298">Cette propriété s’applique lorsque l’entrée est un flux multicanaux et que la sortie est un flux stéréo.</span><span class="sxs-lookup"><span data-stu-id="1fb52-298">This property applies when the input is a multichannel stream and the output is a stereo stream.</span></span><br/> <span data-ttu-id="1fb52-299">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1fb52-299">Read/write.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="1fb52-300">\_modification du \_ format dynamique de la prise en charge de \_ MFT \_</span><span class="sxs-lookup"><span data-stu-id="1fb52-300">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE</span></span>](mft-support-dynamic-format-change-attribute.md) | <span data-ttu-id="1fb52-301">Cet attribut retourne la **valeur false**, ce qui indique que le décodeur doit être vidé avant qu’un nouveau type d’entrée soit défini.</span><span class="sxs-lookup"><span data-stu-id="1fb52-301">This attribute returns **FALSE**, indicating that the decoder must be drained before a new input type is set.</span></span><br/> <span data-ttu-id="1fb52-302">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1fb52-302">Read/write.</span></span><br/>                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="1fb52-303">Notes</span><span class="sxs-lookup"><span data-stu-id="1fb52-303">Remarks</span></span>

<span data-ttu-id="1fb52-304">Le décodeur accepte uniquement les flux Dolby bruts, comme défini par un/52B.</span><span class="sxs-lookup"><span data-stu-id="1fb52-304">The decoder accepts only raw Dolby streams, as defined by A/52B.</span></span> <span data-ttu-id="1fb52-305">Les charges utiles telles que les flux élémentaires paquets (PES) ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1fb52-305">Payloads such as Packetized Elementary Streams (PES) are not supported.</span></span> <span data-ttu-id="1fb52-306">Pour Dolby Digital plus, le décodeur décode jusqu’à 5,1 canaux.</span><span class="sxs-lookup"><span data-stu-id="1fb52-306">For Dolby Digital Plus, the decoder decodes up to 5.1 channels.</span></span> <span data-ttu-id="1fb52-307">Sur Windows 10, les flux de canal 7,1 sont décodés sans downmix.</span><span class="sxs-lookup"><span data-stu-id="1fb52-307">On Windows 10, 7.1 channel streams are decoded without downmix.</span></span> <span data-ttu-id="1fb52-308">Sur les versions précédentes du système d’exploitation, si le flux est 7,1 canaux, seul le canal 5,1 downmix sera décodé.</span><span class="sxs-lookup"><span data-stu-id="1fb52-308">On previous OS versions, if the stream is 7.1 channels, only the 5.1 channel downmix will be decoded.</span></span> <span data-ttu-id="1fb52-309">Si le flux est Dolby Digital plus avec plus d’un sous-flux indépendant, seul le sous-flux indépendant 0 est décodé.</span><span class="sxs-lookup"><span data-stu-id="1fb52-309">If the stream is Dolby Digital Plus with more than one independent substream, only independent substream 0 is decoded.</span></span> <span data-ttu-id="1fb52-310">Le décodeur ignore les autres sous-flux indépendants.</span><span class="sxs-lookup"><span data-stu-id="1fb52-310">The decoder skips other independent substreams.</span></span> <span data-ttu-id="1fb52-311">En outre, le décodeur ignore tous les sous-flux dépendants.</span><span class="sxs-lookup"><span data-stu-id="1fb52-311">In addition, the decoder skips all dependent substreams.</span></span> <span data-ttu-id="1fb52-312">Le décodeur prend en charge le déchiffrement et le décodage des flux protégés par la technologie de Rights Management numérique (DRM).</span><span class="sxs-lookup"><span data-stu-id="1fb52-312">The decoder supports decryption and decoding of streams that are protected by Digital Rights Management (DRM) technology.</span></span>

<span data-ttu-id="1fb52-313">Si le type de média d’entrée a une configuration de canal autre que mono, stéréo ou double-mono (tout cela sans canal LFE), le décodeur fournit deux options pour les configurations de canal de sortie :</span><span class="sxs-lookup"><span data-stu-id="1fb52-313">If the input media type has a channel configuration other than mono, stereo, or dual-mono (all without LFE channel), the decoder provides two options for the output channel configurations:</span></span>

-   <span data-ttu-id="1fb52-314">sortie à 8 canaux (configuration de canal 7,1)</span><span class="sxs-lookup"><span data-stu-id="1fb52-314">8-channel output (7.1 channel configuration)</span></span>
-   <span data-ttu-id="1fb52-315">sortie à 6 canaux (configuration de canal 5,1)</span><span class="sxs-lookup"><span data-stu-id="1fb52-315">6-channel output (5.1 channel configuration)</span></span>
-   <span data-ttu-id="1fb52-316">Downmix stéréo</span><span class="sxs-lookup"><span data-stu-id="1fb52-316">Stereo downmix</span></span>

<span data-ttu-id="1fb52-317">Si l’option stéréo downmix est sélectionnée, le type de downmix peut être défini sur la table MFT à l’aide de la propriété [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) .</span><span class="sxs-lookup"><span data-stu-id="1fb52-317">If stereo downmix is selected, the type of downmix can be set on the MFT by using the [CODECAPI\_AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) property.</span></span>

<span data-ttu-id="1fb52-318">Si le type de sortie est **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**, chaque mémoire tampon de sortie contient 6 144 octets.</span><span class="sxs-lookup"><span data-stu-id="1fb52-318">If the output type is **MFAudioFormat\_Dolby\_AC3\_SPDIF**, each output buffer contains 6,144 bytes.</span></span> <span data-ttu-id="1fb52-319">La mémoire tampon commence par un en-tête S/PDIF de 8 octets, suivi d’une trame AC-3 compressée, suivie d’un remplissage de zéro à 6 144 octets.</span><span class="sxs-lookup"><span data-stu-id="1fb52-319">The buffer starts with an 8-byte S/PDIF header, followed by a compressed AC-3 frame, followed by zero padding to 6,144 bytes.</span></span>

<span data-ttu-id="1fb52-320">Si le type de sortie est **KSDATAFORMAT \_ SubType \_ IEC61937 \_ Dolby \_ Digital \_ plus**, chaque mémoire tampon de sortie contient 24 576 octets.</span><span class="sxs-lookup"><span data-stu-id="1fb52-320">If the output type is **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**, each output buffer contains 24,576 bytes.</span></span> <span data-ttu-id="1fb52-321">La mémoire tampon commence par un en-tête S/PDIF de 8 octets, suivi de 1 à 6 frames Dolby Digital plus compressés correspondant aux exemples PCM 1 536, suivi de zéro remplissage à 24 576 octets.</span><span class="sxs-lookup"><span data-stu-id="1fb52-321">The buffer starts with an 8-byte S/PDIF header, followed by 1–6 compressed Dolby Digital Plus frames corresponding to 1,536 PCM samples, followed by zero padding to 24,576 bytes.</span></span> <span data-ttu-id="1fb52-322">Pour la sortie HDMI, seul le sous-flux indépendant 0 est compressé.</span><span class="sxs-lookup"><span data-stu-id="1fb52-322">For HDMI output, only independent substream 0 is packed.</span></span>

<span data-ttu-id="1fb52-323">La table MFT du décodeur est inscrite avec l’indicateur d' **énumération MFT d’indicateur \_ \_ \_ FIELDOFUSE**, qui indique que la table MFT doit être déverrouillée par l’application avant d’être utilisée.</span><span class="sxs-lookup"><span data-stu-id="1fb52-323">The decoder MFT is registered with the flag **MFT\_ENUM\_FLAG\_FIELDOFUSE**, which indicates that the MFT that must be unlocked by the application before use.</span></span> <span data-ttu-id="1fb52-324">Pour plus d’informations, consultez [restrictions relatives au champ d’utilisation](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="1fb52-324">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb52-325">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fb52-325">Requirements</span></span>



| <span data-ttu-id="1fb52-326">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fb52-326">Requirement</span></span> | <span data-ttu-id="1fb52-327">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fb52-327">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb52-328">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fb52-328">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb52-329">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1fb52-329">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="1fb52-330">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fb52-330">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb52-331">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fb52-331">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="1fb52-332">DLL</span><span class="sxs-lookup"><span data-stu-id="1fb52-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fb52-333"><dt>Msauddecmft.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fb52-333"><dt>Msauddecmft.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fb52-334">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fb52-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb52-335">Objets codec</span><span class="sxs-lookup"><span data-stu-id="1fb52-335">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
