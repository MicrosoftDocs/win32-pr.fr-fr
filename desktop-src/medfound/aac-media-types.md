---
description: Cette rubrique explique comment spécifier le format d’un flux AAC (Advanced Audio encodage) dans Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Types de média AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953345"
---
# <a name="aac-media-types"></a><span data-ttu-id="79aaf-103">Types de média AAC</span><span class="sxs-lookup"><span data-stu-id="79aaf-103">AAC Media Types</span></span>

<span data-ttu-id="79aaf-104">Cette rubrique explique comment spécifier le format d’un flux AAC (Advanced Audio encodage) dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="79aaf-104">This topic describes how to specify the format of an Advanced Audio Coding (AAC) stream in Media Foundation.</span></span>

<span data-ttu-id="79aaf-105">Deux sous-types sont définis pour le son AAC :</span><span class="sxs-lookup"><span data-stu-id="79aaf-105">Two subtypes are defined for AAC audio:</span></span>



| <span data-ttu-id="79aaf-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="79aaf-106">Subtype</span></span>                     | <span data-ttu-id="79aaf-107">Description</span><span class="sxs-lookup"><span data-stu-id="79aaf-107">Description</span></span>          | <span data-ttu-id="79aaf-108">En-tête</span><span class="sxs-lookup"><span data-stu-id="79aaf-108">Header</span></span>       |
|-----------------------------|----------------------|--------------|
| <span data-ttu-id="79aaf-109">**MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="79aaf-109">**MFAudioFormat\_AAC**</span></span>      | <span data-ttu-id="79aaf-110">AAC brut ou ADTS AAC.</span><span class="sxs-lookup"><span data-stu-id="79aaf-110">Raw AAC or ADTS AAC.</span></span> | <span data-ttu-id="79aaf-111">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="79aaf-111">mfapi.h</span></span>      |
| <span data-ttu-id="79aaf-112">**MEDIASUBTYPE \_ brut \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="79aaf-112">**MEDIASUBTYPE\_RAW\_AAC1**</span></span> | <span data-ttu-id="79aaf-113">AAC brut.</span><span class="sxs-lookup"><span data-stu-id="79aaf-113">Raw AAC.</span></span>             | <span data-ttu-id="79aaf-114">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="79aaf-114">wmcodecdsp.h</span></span> |



 

<dl> <dt>

<span data-ttu-id="79aaf-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat \_ AAC</span><span class="sxs-lookup"><span data-stu-id="79aaf-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat\_AAC</span></span>
</dt> <dd>

<span data-ttu-id="79aaf-116">Pour ce sous-type, le type de média donne le taux d’échantillonnage et le nombre de canaux avant l’application des outils de réplication en bande spectrale (SBR) et de la stéréo paramétrique (PS), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="79aaf-116">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="79aaf-117">L’effet de l’outil SBR est de doubler le taux d’échantillonnage décodé par rapport au taux d’échantillonnage AAC-LC de base.</span><span class="sxs-lookup"><span data-stu-id="79aaf-117">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="79aaf-118">L’effet de l’outil PS est de décoder le stéréo à partir d’un flux en AAC-LC Core à canaux mono.</span><span class="sxs-lookup"><span data-stu-id="79aaf-118">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span>

<span data-ttu-id="79aaf-119">Ce sous-type est équivalent à **MEDIASUBTYPE \_ MPEG \_ HEAAC**, défini dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="79aaf-119">This subtype is equivalent to **MEDIASUBTYPE\_MPEG\_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="79aaf-120">Consultez [GUID de sous-type audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="79aaf-120">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="79aaf-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE \_ brut \_ AAC1</span><span class="sxs-lookup"><span data-stu-id="79aaf-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE\_RAW\_AAC1</span></span>
</dt> <dd>

<span data-ttu-id="79aaf-122">Ce sous-type est utilisé pour AAC contenu dans un fichier AVI avec la balise de format audio égale au \_ format Wave \_ RAW \_ AAC1 (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="79aaf-122">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE\_FORMAT\_RAW\_AAC1 (0x00FF).</span></span>

<span data-ttu-id="79aaf-123">Pour ce sous-type, le type de média donne le taux d’échantillonnage et le nombre de canaux après l’application des outils SBR et PS, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="79aaf-123">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span>

</dd> </dl>

<span data-ttu-id="79aaf-124">Les attributs de type de média suivants s’appliquent à l’audio AAC.</span><span class="sxs-lookup"><span data-stu-id="79aaf-124">The following media type attributes apply to AAC audio.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79aaf-125">Attribut</span><span class="sxs-lookup"><span data-stu-id="79aaf-125">Attribute</span></span></th>
<th><span data-ttu-id="79aaf-126">Description</span><span class="sxs-lookup"><span data-stu-id="79aaf-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="79aaf-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="79aaf-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="79aaf-128">Type principal.</span><span class="sxs-lookup"><span data-stu-id="79aaf-128">Major type.</span></span> <span data-ttu-id="79aaf-129">Doit être <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="79aaf-129">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79aaf-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="79aaf-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="79aaf-131">Sous-type audio.</span><span class="sxs-lookup"><span data-stu-id="79aaf-131">Audio subtype.</span></span> <span data-ttu-id="79aaf-132">Pour plus d’informations, reportez-vous à la description précédente.</span><span class="sxs-lookup"><span data-stu-id="79aaf-132">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79aaf-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="79aaf-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="79aaf-134">Profil et niveau audio.</span><span class="sxs-lookup"><span data-stu-id="79aaf-134">Audio profile and level.</span></span> <br/> <span data-ttu-id="79aaf-135">La valeur de cet attribut est le champ <strong>audioProfileLevelIndication</strong> , tel que défini par la norme ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="79aaf-135">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span><br/> <span data-ttu-id="79aaf-136">S’il est inconnu, défini à zéro ou à 0xFE ( &quot; aucun profil audio n’est spécifié &quot; ).</span><span class="sxs-lookup"><span data-stu-id="79aaf-136">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79aaf-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="79aaf-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="79aaf-138">Vitesse de transmission du flux AAC encodé, en octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="79aaf-138">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79aaf-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="79aaf-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="79aaf-140">Type de charge utile.</span><span class="sxs-lookup"><span data-stu-id="79aaf-140">Payload type.</span></span><br/> <span data-ttu-id="79aaf-141">S’applique uniquement aux <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="79aaf-141">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span><br/> <span data-ttu-id="79aaf-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> est facultatif.</span><span class="sxs-lookup"><span data-stu-id="79aaf-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="79aaf-143">Si cet attribut n’est pas spécifié, la valeur par défaut 0 est utilisée, qui spécifie que le flux contient uniquement des éléments raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="79aaf-143">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79aaf-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="79aaf-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="79aaf-145">Profondeur de bit du fichier audio PCM décodé.</span><span class="sxs-lookup"><span data-stu-id="79aaf-145">Bit depth of the decoded PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79aaf-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="79aaf-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="79aaf-147">Attribution de canaux audio aux positions des orateurs.</span><span class="sxs-lookup"><span data-stu-id="79aaf-147">Assignment of audio channels to speaker positions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79aaf-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="79aaf-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="79aaf-149">Nombre de canaux, y compris le canal à fréquence faible (LFE), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="79aaf-149">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/> <span data-ttu-id="79aaf-150">L’interprétation de cette valeur dépend du sous-type de média, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="79aaf-150">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79aaf-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="79aaf-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="79aaf-152">Taux d’échantillonnage, en échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="79aaf-152">Sample rate, in samples per second.</span></span><br/> <span data-ttu-id="79aaf-153">L’interprétation de cette valeur dépend du sous-type de média, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="79aaf-153">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79aaf-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="79aaf-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="79aaf-155">La valeur de cet attribut dépend du sous-type :</span><span class="sxs-lookup"><span data-stu-id="79aaf-155">The value of this attribute depends on the subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="79aaf-156"><strong>MFAudioFormat_AAC</strong>: contient la partie de la structure <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> qui apparaît après la structure <strong>WAVEFORMATEX</strong> (autrement dit, après le membre <strong>wfx</strong> ).</span><span class="sxs-lookup"><span data-stu-id="79aaf-156"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="79aaf-157">Cela est suivi des données AudioSpecificConfig (), telles que définies par la norme ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="79aaf-157">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="79aaf-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contient les données AudioSpecificConfig ().</span><span class="sxs-lookup"><span data-stu-id="79aaf-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="79aaf-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79aaf-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79aaf-160">Types de média audio</span><span class="sxs-lookup"><span data-stu-id="79aaf-160">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="79aaf-161">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="79aaf-161">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="79aaf-162">Prise en charge MPEG-4 dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79aaf-162">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="79aaf-163">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="79aaf-163">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

