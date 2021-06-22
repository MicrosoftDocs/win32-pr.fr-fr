---
description: 'Le décodeur Microsoft Media Foundation AAC est une Media Foundation transformation qui décode les profils de codage audio avancé (AAC) et d’efficacité élevée (HE-AAC) suivants :'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Décodeur AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7554d6bc4a13fe1e4af4c51e75f1fe8a0bd38286
ms.sourcegitcommit: 3a0a8a8fdce560a81a27789a1c04172ed96147b1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2021
ms.locfileid: "112436589"
---
# <a name="aac-decoder"></a><span data-ttu-id="f16ce-103">Décodeur AAC</span><span class="sxs-lookup"><span data-stu-id="f16ce-103">AAC Decoder</span></span>

<span data-ttu-id="f16ce-104">Le décodeur Microsoft Media Foundation AAC est une [Media Foundation transformation](media-foundation-transforms.md) qui décode les profils de codage audio avancé (AAC) et d’efficacité élevée (HE-AAC) suivants :</span><span class="sxs-lookup"><span data-stu-id="f16ce-104">The Microsoft Media Foundation AAC decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>

-   <span data-ttu-id="f16ce-105">Profil LC (Multichannel) MPEG-2 AAC</span><span class="sxs-lookup"><span data-stu-id="f16ce-105">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span>
-   <span data-ttu-id="f16ce-106">MPEG-4 HE-AAC v1 (Multichannel) avec le cœur AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="f16ce-106">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span>
-   <span data-ttu-id="f16ce-107">MPEG-4 HE-AAC V2 (stéréo) avec le cœur AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="f16ce-107">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span>

<span data-ttu-id="f16ce-108">Le décodeur AAC prend en charge les flux AAC bruts sans en-tête ni AAC dans un flux de transport de données audio (ADTS).</span><span class="sxs-lookup"><span data-stu-id="f16ce-108">The AAC decoder supports both raw AAC streams with no headers and AAC in an audio data transport stream (ADTS).</span></span>

<span data-ttu-id="f16ce-109">À compter de Windows 8, le décodeur AAC prend également en charge le décodage des flux de transport audio MPEG-4 avec une couche multiplex (LATM) et une couche de synchronisation (garantie).</span><span class="sxs-lookup"><span data-stu-id="f16ce-109">Starting in Windows 8, the AAC decoder also supports decoding MPEG-4 audio transport streams with a multiplex layer (LATM) and synchronization layer (LOAS).</span></span> <span data-ttu-id="f16ce-110">Il peut également convertir un flux LATM/garantie en ADTS.</span><span class="sxs-lookup"><span data-stu-id="f16ce-110">It can also convert an LATM/LOAS stream to ADTS.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="f16ce-111">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="f16ce-111">Class Identifier</span></span>

<span data-ttu-id="f16ce-112">L’identificateur de classe (CLSID) de l’encodeur AAC est **CLSID \_ CMSAACDecMFT**, défini dans le fichier d’en-tête wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="f16ce-112">The class identifier (CLSID) of the AAC encoder is **CLSID\_CMSAACDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="f16ce-113">Types de médias</span><span class="sxs-lookup"><span data-stu-id="f16ce-113">Media Types</span></span>

<span data-ttu-id="f16ce-114">Le décodeur AAC prend en charge les types de média suivants.</span><span class="sxs-lookup"><span data-stu-id="f16ce-114">The AAC decoder supports the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="f16ce-115">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="f16ce-115">Input Types</span></span>

<span data-ttu-id="f16ce-116">Le décodeur AAC prend en charge les sous-types audio suivants :</span><span class="sxs-lookup"><span data-stu-id="f16ce-116">The AAC decoder supports the following audio subtypes:</span></span>



| <span data-ttu-id="f16ce-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="f16ce-117">Subtype</span></span>                     | <span data-ttu-id="f16ce-118">Description</span><span class="sxs-lookup"><span data-stu-id="f16ce-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="f16ce-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="f16ce-119">Header</span></span>       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="f16ce-120">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="f16ce-120">**MFAudioFormat_AAC**</span></span>      | <span data-ttu-id="f16ce-121">AAC brut ou ADTS AAC.</span><span class="sxs-lookup"><span data-stu-id="f16ce-121">Raw AAC or ADTS AAC.</span></span><br/> <span data-ttu-id="f16ce-122">Pour ce sous-type, le type de média donne le taux d’échantillonnage et le nombre de canaux avant l’application des outils de réplication en bande spectrale (SBR) et de la stéréo paramétrique (PS), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f16ce-122">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="f16ce-123">L’effet de l’outil SBR est de doubler le taux d’échantillonnage décodé par rapport au taux d’échantillonnage AAC-LC de base.</span><span class="sxs-lookup"><span data-stu-id="f16ce-123">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="f16ce-124">L’effet de l’outil PS est de décoder le stéréo à partir d’un flux en AAC-LC Core à canaux mono.</span><span class="sxs-lookup"><span data-stu-id="f16ce-124">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span><br/> <span data-ttu-id="f16ce-125">Ce sous-type est équivalent à **MEDIASUBTYPE_MPEG_HEAAC**, défini dans wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="f16ce-125">This subtype is equivalent to **MEDIASUBTYPE_MPEG_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="f16ce-126">Consultez [GUID de sous-type audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f16ce-126">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> <br/> <span data-ttu-id="f16ce-127">La [source du fichier MPEG-4](mpeg-4-file-source.md) et l’analyseur ADTS génèrent ce sous-type.</span><span class="sxs-lookup"><span data-stu-id="f16ce-127">The [MPEG-4 File Source](mpeg-4-file-source.md) and the ADTS Parser output this subtype.</span></span> <br/> | <span data-ttu-id="f16ce-128">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="f16ce-128">mfapi.h</span></span>      |
| <span data-ttu-id="f16ce-129">**MEDIASUBTYPE_RAW_AAC1**</span><span class="sxs-lookup"><span data-stu-id="f16ce-129">**MEDIASUBTYPE_RAW_AAC1**</span></span> | <span data-ttu-id="f16ce-130">AAC brut.</span><span class="sxs-lookup"><span data-stu-id="f16ce-130">Raw AAC.</span></span> <br/> <span data-ttu-id="f16ce-131">Ce sous-type est utilisé pour l’AAC contenu dans un fichier AVI avec la balise de format audio égale à WAVE_FORMAT_RAW_AAC1 (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="f16ce-131">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE_FORMAT_RAW_AAC1 (0x00FF).</span></span> <br/> <span data-ttu-id="f16ce-132">Pour ce sous-type, le type de média donne le taux d’échantillonnage et le nombre de canaux après l’application des outils SBR et PS, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f16ce-132">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="f16ce-133">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="f16ce-133">wmcodecdsp.h</span></span> |



 

<span data-ttu-id="f16ce-134">Pour configurer le décodeur AAC, définissez les attributs suivants sur le type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f16ce-134">To configure the AAC decoder, set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f16ce-135">Attribut</span><span class="sxs-lookup"><span data-stu-id="f16ce-135">Attribute</span></span></th>
<th><span data-ttu-id="f16ce-136">Description</span><span class="sxs-lookup"><span data-stu-id="f16ce-136">Description</span></span></th>
<th><span data-ttu-id="f16ce-137">Notes</span><span class="sxs-lookup"><span data-stu-id="f16ce-137">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f16ce-138"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16ce-138"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="f16ce-139">Type principal.</span><span class="sxs-lookup"><span data-stu-id="f16ce-139">Major type.</span></span></td>
<td><span data-ttu-id="f16ce-140">Doit être <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="f16ce-140">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f16ce-141"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16ce-141"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="f16ce-142">Sous-type audio.</span><span class="sxs-lookup"><span data-stu-id="f16ce-142">Audio subtype.</span></span></td>
<td><span data-ttu-id="f16ce-143">Pour plus d’informations, reportez-vous à la description précédente.</span><span class="sxs-lookup"><span data-stu-id="f16ce-143">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f16ce-144"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="f16ce-144"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="f16ce-145">Profil et niveau audio.</span><span class="sxs-lookup"><span data-stu-id="f16ce-145">Audio profile and level.</span></span> <br/></td>
<td><span data-ttu-id="f16ce-146">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f16ce-146">Optional.</span></span> <span data-ttu-id="f16ce-147">S’applique uniquement aux <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="f16ce-147">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <br/> <span data-ttu-id="f16ce-148">La valeur de cet attribut est le champ <strong>audioProfileLevelIndication</strong> , tel que défini par la norme ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="f16ce-148">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span> <br/> <span data-ttu-id="f16ce-149">S’il est inconnu, défini à zéro ou à 0xFE ( &quot; aucun profil audio n’est spécifié &quot; ).</span><span class="sxs-lookup"><span data-stu-id="f16ce-149">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f16ce-150"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="f16ce-150"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="f16ce-151">Type de charge utile.</span><span class="sxs-lookup"><span data-stu-id="f16ce-151">Payload type.</span></span><br/></td>
<td><span data-ttu-id="f16ce-152">S’applique uniquement aux <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="f16ce-152">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <span data-ttu-id="f16ce-153">Le décodeur prend en charge les types de charge utile suivants :</span><span class="sxs-lookup"><span data-stu-id="f16ce-153">The decoder supports the following payload types:</span></span> <br/>
<ul>
<li><span data-ttu-id="f16ce-154">0 : AAC brut.</span><span class="sxs-lookup"><span data-stu-id="f16ce-154">0: Raw AAC.</span></span> <span data-ttu-id="f16ce-155">Le flux contient uniquement des éléments raw_data_block (), comme défini par MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="f16ce-155">The stream contains raw_data_block() elements only, as defined by MPEG-2.</span></span></li>
<li><span data-ttu-id="f16ce-156">1 : ADTS.</span><span class="sxs-lookup"><span data-stu-id="f16ce-156">1: ADTS.</span></span> <span data-ttu-id="f16ce-157">Le flux contient un adts_sequence (), tel que défini par MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="f16ce-157">The stream contains an adts_sequence(), as defined by MPEG-2.</span></span> <span data-ttu-id="f16ce-158">Une seule raw_data_block () par adts_frame () est autorisée.</span><span class="sxs-lookup"><span data-stu-id="f16ce-158">Only one raw_data_block() per adts_frame() is allowed.</span></span></li>
<li><span data-ttu-id="f16ce-159">3 : flux de transport audio avec une couche de synchronisation (garantie) et une couche multiplex (LATM).</span><span class="sxs-lookup"><span data-stu-id="f16ce-159">3: Audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span> <span data-ttu-id="f16ce-160">Parmi les trois types de garantie, seul <strong>AudioSyncStream</strong> est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f16ce-160">Of the three types of LOAS, only <strong>AudioSyncStream</strong> is supported.</span></span> <span data-ttu-id="f16ce-161">La couche multiplex est <strong>AudioMuxElement</strong>, restreinte à un programme audio et une couche.</span><span class="sxs-lookup"><span data-stu-id="f16ce-161">The multiplex layer is <strong>AudioMuxElement</strong>, restricted to one audio program and one layer.</span></span></li>
</ul><span data-ttu-id="f16ce-162">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> est facultatif.</span><span class="sxs-lookup"><span data-stu-id="f16ce-162">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="f16ce-163">Si cet attribut n’est pas spécifié, la valeur par défaut 0 est utilisée, qui spécifie que le flux contient uniquement des éléments raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="f16ce-163">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f16ce-164"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16ce-164"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="f16ce-165">Profondeur de bits souhaitée du fichier audio PCM décodé.</span><span class="sxs-lookup"><span data-stu-id="f16ce-165">Desired bit depth of the decoded PCM audio.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="f16ce-166"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16ce-166"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="f16ce-167">Spécifie l’affectation des canaux audio aux positions des haut-parleurs.</span><span class="sxs-lookup"><span data-stu-id="f16ce-167">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="f16ce-168">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f16ce-168">Optional.</span></span> <span data-ttu-id="f16ce-169">Pour plus d’informations, consultez <a href="#format-constraints">mettre en forme les contraintes</a>.</span><span class="sxs-lookup"><span data-stu-id="f16ce-169">For more information, see <a href="#format-constraints">Format Constraints</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f16ce-170"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16ce-170"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="f16ce-171">Nombre de canaux, y compris le canal à fréquence faible (LFE), le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f16ce-171">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/></td>
<td><span data-ttu-id="f16ce-172">L’interprétation de cette valeur dépend du sous-type de média, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="f16ce-172">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f16ce-173"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16ce-173"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="f16ce-174">Taux d’échantillonnage, en échantillons par seconde.</span><span class="sxs-lookup"><span data-stu-id="f16ce-174">Sample rate, in samples per second.</span></span><br/></td>
<td><span data-ttu-id="f16ce-175">L’interprétation de cette valeur dépend du sous-type de média, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="f16ce-175">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f16ce-176"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16ce-176"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="f16ce-177">Informations de mise en forme supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f16ce-177">Additional format information.</span></span></td>
<td><span data-ttu-id="f16ce-178">La valeur de cet attribut dépend du sous-type.</span><span class="sxs-lookup"><span data-stu-id="f16ce-178">The value of this attribute depends on the subtype.</span></span><br/>
<ul>
<li><span data-ttu-id="f16ce-179"><strong>MFAudioFormat_AAC</strong>: contient la partie de la structure <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> qui apparaît après la structure <strong>WAVEFORMATEX</strong> (autrement dit, après le membre <strong>wfx</strong> ).</span><span class="sxs-lookup"><span data-stu-id="f16ce-179"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="f16ce-180">Cela est suivi des données AudioSpecificConfig (), telles que définies par la norme ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="f16ce-180">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="f16ce-181"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contient les données AudioSpecificConfig ().</span><span class="sxs-lookup"><span data-stu-id="f16ce-181"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span> <span data-ttu-id="f16ce-182">Ces données doivent apparaître. dans le cas contraire, le décodeur rejettera le type de média.</span><span class="sxs-lookup"><span data-stu-id="f16ce-182">This data must appear; otherwise, the decoder will reject the media type.</span></span></li>
</ul>
<span data-ttu-id="f16ce-183">La longueur des données AudioSpecificConfig () est de 2 octets pour AAC-LC ou HE-AAC avec signal implicite de SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="f16ce-183">The length of the AudioSpecificConfig() data is 2 bytes for AAC-LC or HE-AAC with implicit signaling of SBR/PS.</span></span> <span data-ttu-id="f16ce-184">Elle est supérieure à 2 octets pour le HE-AAC avec signalement explicite de SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="f16ce-184">It is more than 2 bytes for HE-AAC with explicit signaling of SBR/PS.</span></span><br/> <span data-ttu-id="f16ce-185">La valeur de <strong>audioObjectType</strong> telle que définie dans AudioSpecificConfig () doit être 2, ce qui indique AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="f16ce-185">The value of <strong>audioObjectType</strong> as defined in AudioSpecificConfig() must be 2, indicating AAC-LC.</span></span> <span data-ttu-id="f16ce-186">La valeur de <strong>extensionAudioObjectType</strong> doit être 5 pour SBR ou 29 pour PS.</span><span class="sxs-lookup"><span data-stu-id="f16ce-186">The value of <strong>extensionAudioObjectType</strong> must be 5 for SBR or 29 for PS.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a><span data-ttu-id="f16ce-187">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="f16ce-187">Output Types</span></span>

<span data-ttu-id="f16ce-188">Le décodeur prend en charge les types de sortie suivants :</span><span class="sxs-lookup"><span data-stu-id="f16ce-188">The decoder supports the following output types:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f16ce-189">Subtype</span><span class="sxs-lookup"><span data-stu-id="f16ce-189">Subtype</span></span></th>
<th><span data-ttu-id="f16ce-190">Description</span><span class="sxs-lookup"><span data-stu-id="f16ce-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f16ce-191"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="f16ce-191"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="f16ce-192">Audio à virgule flottante IEEE.</span><span class="sxs-lookup"><span data-stu-id="f16ce-192">IEEE floating-point audio.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f16ce-193"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="f16ce-193"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="f16ce-194">audio PCM 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f16ce-194">16-bit PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f16ce-195"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="f16ce-195"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="f16ce-196">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f16ce-196">Requires Windows 8.</span></span> <br/> <span data-ttu-id="f16ce-197">Ce type de sortie peut être utilisé pour convertir un flux AAC au format garantie/LATM au format ADTS.</span><span class="sxs-lookup"><span data-stu-id="f16ce-197">This output type can be used to convert an AAC stream in the LOAS/LATM format to ADTS format.</span></span> <br/> <span data-ttu-id="f16ce-198">Pour convertir un flux garantie/LATM en un flux ADTS, définissez le type d’entrée sur <strong>MFAudioFormat_AAC</strong> avec le type de charge utile 3 (garantie).</span><span class="sxs-lookup"><span data-stu-id="f16ce-198">To convert an LOAS/LATM stream to an ADTS stream, set the input type to <strong>MFAudioFormat_AAC</strong> with payload type 3 (LOAS).</span></span> <span data-ttu-id="f16ce-199">Définissez ensuite le type de sortie sur <strong>MFAudioFormat_AAC</strong> avec le type de charge utile 1 (ADTS).</span><span class="sxs-lookup"><span data-stu-id="f16ce-199">Then set the output type to <strong>MFAudioFormat_AAC</strong> with payload type 1 (ADTS).</span></span> <span data-ttu-id="f16ce-200">Le décodeur reformatera le conainter sans décoder le flux binaire.</span><span class="sxs-lookup"><span data-stu-id="f16ce-200">The decoder will reformat the conainter without decoding the bitstream.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f16ce-201">Le décodeur n’inscrit pas <strong>MFAudioFormat_AAC</strong> comme type de sortie.</span><span class="sxs-lookup"><span data-stu-id="f16ce-201">The decoder does not register <strong>MFAudioFormat_AAC</strong> as an output type.</span></span> <span data-ttu-id="f16ce-202">Toutefois, si l’application définit le type d’entrée comme décrit, la méthode <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform :: GetOutputAvailableType</strong></a> retourne <strong>MFAudioFormat_AAC</strong> dans la liste des types de sortie disponibles.</span><span class="sxs-lookup"><span data-stu-id="f16ce-202">However, if the application sets the input type as described, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> method returns <strong>MFAudioFormat_AAC</strong> in the list of available output types.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f16ce-203">Si le flux d’entrée contient plus de deux canaux, le décodeur AAC fournit deux options pour le format de sortie :</span><span class="sxs-lookup"><span data-stu-id="f16ce-203">If the input stream contains more than two channels, the AAC decoder provides two options for the output format:</span></span>

-   <span data-ttu-id="f16ce-204">La même configuration de canal que le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f16ce-204">The same channel configuration as the input type.</span></span>
-   <span data-ttu-id="f16ce-205">Pliure en stéréo.</span><span class="sxs-lookup"><span data-stu-id="f16ce-205">Stereo fold-down.</span></span>

## <a name="format-constraints"></a><span data-ttu-id="f16ce-206">Contraintes de format</span><span class="sxs-lookup"><span data-stu-id="f16ce-206">Format Constraints</span></span>

<span data-ttu-id="f16ce-207">Le taux d’échantillonnage audio décodé doit être l’un des suivants, après l’application de SBR (le cas échéant) :</span><span class="sxs-lookup"><span data-stu-id="f16ce-207">The decoded audio sampling rate must be one of the following, after SBR is applied (if present):</span></span>

-   <span data-ttu-id="f16ce-208">8 kHz</span><span class="sxs-lookup"><span data-stu-id="f16ce-208">8 kHz</span></span>
-   <span data-ttu-id="f16ce-209">11,025 kHz</span><span class="sxs-lookup"><span data-stu-id="f16ce-209">11.025 kHz</span></span>
-   <span data-ttu-id="f16ce-210">12 kHz</span><span class="sxs-lookup"><span data-stu-id="f16ce-210">12 kHz</span></span>
-   <span data-ttu-id="f16ce-211">16 kHz</span><span class="sxs-lookup"><span data-stu-id="f16ce-211">16 kHz</span></span>
-   <span data-ttu-id="f16ce-212">22,05 kHz</span><span class="sxs-lookup"><span data-stu-id="f16ce-212">22.05 kHz</span></span>
-   <span data-ttu-id="f16ce-213">24 kHz</span><span class="sxs-lookup"><span data-stu-id="f16ce-213">24 kHz</span></span>
-   <span data-ttu-id="f16ce-214">32 kHz</span><span class="sxs-lookup"><span data-stu-id="f16ce-214">32 kHz</span></span>
-   <span data-ttu-id="f16ce-215">44,1 kHz</span><span class="sxs-lookup"><span data-stu-id="f16ce-215">44.1 kHz</span></span>
-   <span data-ttu-id="f16ce-216">48 kHz</span><span class="sxs-lookup"><span data-stu-id="f16ce-216">48 kHz</span></span>

<span data-ttu-id="f16ce-217">Les taux d’échantillonnage supérieurs à 48 kHz ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f16ce-217">Sampling rates above 48 kHz are not supported.</span></span>

<span data-ttu-id="f16ce-218">Le décodeur prend en charge jusqu’à 6 canaux audio.</span><span class="sxs-lookup"><span data-stu-id="f16ce-218">The decoder supports up to 6 audio channels.</span></span> <span data-ttu-id="f16ce-219">Pour chaque configuration de haut-parleur, le décodeur s’attend à ce que les éléments syntaxiques AAC apparaissent dans un certain ordre.</span><span class="sxs-lookup"><span data-stu-id="f16ce-219">For each speaker configuration, the decoder expects the AAC syntactic elements to appear in a certain order.</span></span> <span data-ttu-id="f16ce-220">Le tableau suivant répertorie les configurations de conférencier prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f16ce-220">The following table lists the supported speaker configurations.</span></span> <span data-ttu-id="f16ce-221">La troisième colonne de la table répertorie les éléments syntaxiques attendus et leur ordre, en utilisant la notation suivante :</span><span class="sxs-lookup"><span data-stu-id="f16ce-221">The third column of the table lists the expected syntactic elements and their order, using the following notation:</span></span>

-   <span data-ttu-id="f16ce-222"><SCE1>: Le single_channel_element (SCE) associé au haut-parleur central.</span><span class="sxs-lookup"><span data-stu-id="f16ce-222"><SCE1>: The single_channel_element (SCE) associated with the front center speaker.</span></span>
-   <span data-ttu-id="f16ce-223"><SCE2>: SCE associée à l’orateur Back central.</span><span class="sxs-lookup"><span data-stu-id="f16ce-223"><SCE2>: The SCE associated with the back center speaker.</span></span>
-   <span data-ttu-id="f16ce-224"><CPE1>: Le channel_pair_element (CPE) associé aux haut-parleurs frontaux.</span><span class="sxs-lookup"><span data-stu-id="f16ce-224"><CPE1>: The channel_pair_element (CPE) associated with the front speakers.</span></span>
-   <span data-ttu-id="f16ce-225"><CPE2>: L’ECP associé aux enceintes Back (ou Side)</span><span class="sxs-lookup"><span data-stu-id="f16ce-225"><CPE2>: The CPE associated with the back (or side) speakers</span></span>
-   <span data-ttu-id="f16ce-226"><LFE>: Le lfe_channel_element (LFE).</span><span class="sxs-lookup"><span data-stu-id="f16ce-226"><LFE>: The lfe_channel_element (LFE).</span></span>

<span data-ttu-id="f16ce-227">Pour plus d’informations sur ces éléments syntaxiques, reportez-vous à la norme ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="f16ce-227">For more information about these syntactic elements, refer to ISO/IEC 13818-7.</span></span>



| <span data-ttu-id="f16ce-228">Configuration</span><span class="sxs-lookup"><span data-stu-id="f16ce-228">Configuration</span></span>       | <span data-ttu-id="f16ce-229">Masque de canal</span><span class="sxs-lookup"><span data-stu-id="f16ce-229">Channel Mask</span></span>                                                                                                                                                              | <span data-ttu-id="f16ce-230">Éléments syntaxiques AAC</span><span class="sxs-lookup"><span data-stu-id="f16ce-230">AAC Syntactic Elements</span></span>                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="f16ce-231">Mono</span><span class="sxs-lookup"><span data-stu-id="f16ce-231">Mono</span></span>                | <span data-ttu-id="f16ce-232">**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="f16ce-232">**SPEAKER_FRONT_CENTER**</span></span>                                                                                                                                                | <SCE1>                                    |
| <span data-ttu-id="f16ce-233">Stéréo ou double mono</span><span class="sxs-lookup"><span data-stu-id="f16ce-233">Stereo or dual mono</span></span> | <span data-ttu-id="f16ce-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="f16ce-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span></span>                                                                                                                     | <CPE1>                                    |
| <span data-ttu-id="f16ce-235">2/1</span><span class="sxs-lookup"><span data-stu-id="f16ce-235">2/1</span></span>                 | <span data-ttu-id="f16ce-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="f16ce-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span></span>                                                                                        | <CPE1><SCE1>                        |
| <span data-ttu-id="f16ce-237">2/2</span><span class="sxs-lookup"><span data-stu-id="f16ce-237">2/2</span></span>                 | <span data-ttu-id="f16ce-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="f16ce-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                                              | <CPE1><CPE2>                        |
| <span data-ttu-id="f16ce-239">3/0</span><span class="sxs-lookup"><span data-stu-id="f16ce-239">3/0</span></span>                 | <span data-ttu-id="f16ce-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="f16ce-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span></span>                                                                                       | <SCE1><CPE1>                        |
| <span data-ttu-id="f16ce-241">3/1</span><span class="sxs-lookup"><span data-stu-id="f16ce-241">3/1</span></span>                 | <span data-ttu-id="f16ce-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="f16ce-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span></span>                                                          | <SCE1><CPE1><SCE2>            |
| <span data-ttu-id="f16ce-243">3/2</span><span class="sxs-lookup"><span data-stu-id="f16ce-243">3/2</span></span>                 | <span data-ttu-id="f16ce-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="f16ce-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                | <SCE1><CPE1><CPE2>            |
| <span data-ttu-id="f16ce-245">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="f16ce-245">3/2 + LFE</span></span>           | <span data-ttu-id="f16ce-246">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="f16ce-246">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span> | <SCE1><CPE1><CPE2><LFE> |



 

<span data-ttu-id="f16ce-247">Pour les AAC bruts, chaque exemple d’entrée doit contenir exactement une trame compressée AAC complète.</span><span class="sxs-lookup"><span data-stu-id="f16ce-247">For raw AAC, each input sample must contain exactly one full AAC compressed frame.</span></span>

<span data-ttu-id="f16ce-248">Pour ADTS, chaque exemple d’entrée peut contenir plusieurs images audio, ainsi que des frames partiels, qui peuvent s’étendre sur des limites d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="f16ce-248">For ADTS, each input sample can contain multiple audio frames, as well as partial frames   that is, frames can span sample boundaries.</span></span> <span data-ttu-id="f16ce-249">Chaque en-tête ADTS doit être suivi d’une trame AAC.</span><span class="sxs-lookup"><span data-stu-id="f16ce-249">Each ADTS header must be followed by one AAC frame.</span></span>

<span data-ttu-id="f16ce-250">Le décodeur AAC ne prend pas en charge les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f16ce-250">The AAC decoder does not support any of the following:</span></span>

-   <span data-ttu-id="f16ce-251">Profil principal, Sample-Rate profil Scalable (SRS) ou profil de prédiction à long terme (LTP).</span><span class="sxs-lookup"><span data-stu-id="f16ce-251">Main profile, Sample-Rate Scalable (SRS) profile, or Long Term Prediction (LTP) profile.</span></span>
-   <span data-ttu-id="f16ce-252">Format d’échange de données audio (ADIF).</span><span class="sxs-lookup"><span data-stu-id="f16ce-252">Audio data interchange format (ADIF).</span></span>
-   <span data-ttu-id="f16ce-253">Flux de transport LATM/LAOS.</span><span class="sxs-lookup"><span data-stu-id="f16ce-253">LATM/LAOS transport streams.</span></span>
-   <span data-ttu-id="f16ce-254">Couplage des éléments de canal.</span><span class="sxs-lookup"><span data-stu-id="f16ce-254">Coupling channel elements (CCEs).</span></span> <span data-ttu-id="f16ce-255">Le décodeur ignore les images audio avec l’opération.</span><span class="sxs-lookup"><span data-stu-id="f16ce-255">The decoder will skip audio frames with CCEs.</span></span>
-   <span data-ttu-id="f16ce-256">AAC-LC avec une taille d’image 960-Sample.</span><span class="sxs-lookup"><span data-stu-id="f16ce-256">AAC-LC with a 960-sample frame size.</span></span> <span data-ttu-id="f16ce-257">Seuls 1024-les exemples de frames sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f16ce-257">Only 1024-sample frames are supported.</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="f16ce-258">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="f16ce-258">Transform Attributes</span></span>

<span data-ttu-id="f16ce-259">Le décodeur AAC implémente la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="f16ce-259">The AAC decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="f16ce-260">Les applications peuvent utiliser cette méthode pour récupérer ou définir les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="f16ce-260">Applications can use this method to get or set the following attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f16ce-261">Attribut</span><span class="sxs-lookup"><span data-stu-id="f16ce-261">Attribute</span></span></th>
<th><span data-ttu-id="f16ce-262">Description</span><span class="sxs-lookup"><span data-stu-id="f16ce-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f16ce-263"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16ce-263"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span></span></td>
<td><span data-ttu-id="f16ce-264">Spécifie si le contenu audio à 2 canaux est encodé en stéréo ou en double mono.</span><span class="sxs-lookup"><span data-stu-id="f16ce-264">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span> <span data-ttu-id="f16ce-265">Traiter en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f16ce-265">Treat as read-only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f16ce-266"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16ce-266"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span></span></td>
<td><span data-ttu-id="f16ce-267">Spécifie comment le décodeur reproduit un double audio mono.</span><span class="sxs-lookup"><span data-stu-id="f16ce-267">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="f16ce-268">La valeur par défaut est <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: sortie CH1 vers les haut-parleurs gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="f16ce-268">The default value is <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 to the left and right speakers.</span></span> <br/> <span data-ttu-id="f16ce-269">Les applications peuvent définir cette propriété pour modifier le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="f16ce-269">Applications can set this property to change the default behavior.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f16ce-270"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16ce-270"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="f16ce-271">Le décodeur AAC ne gère pas les modifications de format dynamiques et doit être vidé ou vidé avant qu’un nouveau type de média d’entrée soit défini.</span><span class="sxs-lookup"><span data-stu-id="f16ce-271">The AAC decoder does not handle dynamic format changes, and must be flushed or drained before a new input media type is set.</span></span> <span data-ttu-id="f16ce-272">Traiter cet attribut comme étant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f16ce-272">Treat this attribute as read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f16ce-273">Le décodeur AAC signale incorrectement la valeur <strong>true</strong> pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="f16ce-273">The AAC decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="f16ce-274">Dans Windows 7, le décodeur signale incorrectement la valeur <strong>true</strong> pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="f16ce-274">In Windows 7, the decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span> <span data-ttu-id="f16ce-275">Dans Windows 8, le décodeur signale <strong>false</strong>, qui est la valeur correcte</span><span class="sxs-lookup"><span data-stu-id="f16ce-275">In Windows 8, the decoder reports <strong>FALSE</strong>, which is the correct value</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a><span data-ttu-id="f16ce-276">Exemples de types de média</span><span class="sxs-lookup"><span data-stu-id="f16ce-276">Example Media Types</span></span>

<span data-ttu-id="f16ce-277">Voici un exemple de type de média d’entrée nécessaire pour un flux de 6 canaux, 48-kHz AAC-LC, à l’aide d’une charge AAC brute :</span><span class="sxs-lookup"><span data-stu-id="f16ce-277">Here is an example of the input media type needed for a 6-channel, 48-kHz AAC-LC stream, using a raw AAC payload:</span></span>



| <span data-ttu-id="f16ce-278">Attribut</span><span class="sxs-lookup"><span data-stu-id="f16ce-278">Attribute</span></span>                                                                                      | <span data-ttu-id="f16ce-279">Valeur</span><span class="sxs-lookup"><span data-stu-id="f16ce-279">Value</span></span>                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="f16ce-280">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="f16ce-280">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="f16ce-281">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="f16ce-281">**MFMediaType_Audio**</span></span>                                                               |
| [<span data-ttu-id="f16ce-282">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="f16ce-282">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="f16ce-283">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="f16ce-283">**MFAudioFormat_AAC**</span></span>                                                               |
| [<span data-ttu-id="f16ce-284">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="f16ce-284">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="f16ce-285">48 000</span><span class="sxs-lookup"><span data-stu-id="f16ce-285">48000</span></span>                                                                                |
| [<span data-ttu-id="f16ce-286">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="f16ce-286">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="f16ce-287">6</span><span class="sxs-lookup"><span data-stu-id="f16ce-287">6</span></span>                                                                                    |
| [<span data-ttu-id="f16ce-288">MF_MT_AAC_PAYLOAD_TYPE</span><span class="sxs-lookup"><span data-stu-id="f16ce-288">MF_MT_AAC_PAYLOAD_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="f16ce-289">0</span><span class="sxs-lookup"><span data-stu-id="f16ce-289">0</span></span>                                                                                    |
| [<span data-ttu-id="f16ce-290">**MF_MT_USER_DATA**</span><span class="sxs-lookup"><span data-stu-id="f16ce-290">**MF_MT_USER_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="f16ce-291">{0x00, 0x00, 0x2A, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span><span class="sxs-lookup"><span data-stu-id="f16ce-291">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span></span> |
| [<span data-ttu-id="f16ce-292">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="f16ce-292">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="f16ce-293">0x2a (facultatif)</span><span class="sxs-lookup"><span data-stu-id="f16ce-293">0x2a (optional)</span></span>                                                                      |



 

<span data-ttu-id="f16ce-294">Les 12 premiers octets de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspondent aux membres de la structure [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) suivants :</span><span class="sxs-lookup"><span data-stu-id="f16ce-294">The first 12 bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspond to the following [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure members:</span></span>

-   <span data-ttu-id="f16ce-295">**wPayloadType** = 0 (AAC brut)</span><span class="sxs-lookup"><span data-stu-id="f16ce-295">**wPayloadType** = 0 (raw AAC)</span></span>
-   <span data-ttu-id="f16ce-296">**wAudioProfileLevelIndication** = 0X2a (profil AAC, niveau 4)</span><span class="sxs-lookup"><span data-stu-id="f16ce-296">**wAudioProfileLevelIndication** = 0x2a (AAC Profile, Level 4)</span></span>
-   <span data-ttu-id="f16ce-297">**wStructType** = 0</span><span class="sxs-lookup"><span data-stu-id="f16ce-297">**wStructType** = 0</span></span>

<span data-ttu-id="f16ce-298">Les deux derniers octets de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contenir la valeur de AudioSpecificConfig (), comme défini par MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="f16ce-298">The last two bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contain the value of AudioSpecificConfig(), as defined by MPEG-4.</span></span>

-   <span data-ttu-id="f16ce-299">AudioSpecificConfig. audioObjectType = 2 (AAC LC) (5 bits)</span><span class="sxs-lookup"><span data-stu-id="f16ce-299">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)</span></span>
-   <span data-ttu-id="f16ce-300">AudioSpecificConfig. samplingFrequencyIndex = 3 (4 bits)</span><span class="sxs-lookup"><span data-stu-id="f16ce-300">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span></span>
-   <span data-ttu-id="f16ce-301">AudioSpecificConfig. channelConfiguration = 6 (4 bits)</span><span class="sxs-lookup"><span data-stu-id="f16ce-301">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span></span>
-   <span data-ttu-id="f16ce-302">GASpecificConfig. frameLengthFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="f16ce-302">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span></span>
-   <span data-ttu-id="f16ce-303">GASpecificConfig. dependsOnCoreCoder = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="f16ce-303">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span></span>
-   <span data-ttu-id="f16ce-304">GASpecificConfig. extensionFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="f16ce-304">GASpecificConfig.extensionFlag = 0 (1 bit)</span></span>

<span data-ttu-id="f16ce-305">À partir de ce type d’entrée, utilisez le type de média de sortie suivant pour recevoir le fichier audio PCM à virgule flottante 32 bits à 6 canaux du décodeur :</span><span class="sxs-lookup"><span data-stu-id="f16ce-305">Given this input type, use the following output media type to get 6-channel, 32-bit floating point PCM audio from the decoder:</span></span>



| <span data-ttu-id="f16ce-306">Attribut</span><span class="sxs-lookup"><span data-stu-id="f16ce-306">Attribute</span></span>                                                                                    | <span data-ttu-id="f16ce-307">Valeur</span><span class="sxs-lookup"><span data-stu-id="f16ce-307">Value</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [<span data-ttu-id="f16ce-308">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="f16ce-308">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="f16ce-309">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="f16ce-309">**MFMediaType_Audio**</span></span>   |
| [<span data-ttu-id="f16ce-310">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="f16ce-310">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="f16ce-311">**MFAudioFormat_Float**</span><span class="sxs-lookup"><span data-stu-id="f16ce-311">**MFAudioFormat_Float**</span></span> |
| [<span data-ttu-id="f16ce-312">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span><span class="sxs-lookup"><span data-stu-id="f16ce-312">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="f16ce-313">32</span><span class="sxs-lookup"><span data-stu-id="f16ce-313">32</span></span>                       |
| [<span data-ttu-id="f16ce-314">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="f16ce-314">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="f16ce-315">48 000</span><span class="sxs-lookup"><span data-stu-id="f16ce-315">48000</span></span>                    |
| [<span data-ttu-id="f16ce-316">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="f16ce-316">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="f16ce-317">6</span><span class="sxs-lookup"><span data-stu-id="f16ce-317">6</span></span>                        |
| [<span data-ttu-id="f16ce-318">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="f16ce-318">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="f16ce-319">1152000 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="f16ce-319">1152000 (optional)</span></span>       |
| [<span data-ttu-id="f16ce-320">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span><span class="sxs-lookup"><span data-stu-id="f16ce-320">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="f16ce-321">24 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="f16ce-321">24 (optional)</span></span>            |
| [<span data-ttu-id="f16ce-322">**MF_MT_AUDIO_CHANNEL_MASK**</span><span class="sxs-lookup"><span data-stu-id="f16ce-322">**MF_MT_AUDIO_CHANNEL_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                   | <span data-ttu-id="f16ce-323">0x3F (facultatif)</span><span class="sxs-lookup"><span data-stu-id="f16ce-323">0x3f (optional)</span></span>          |



 

<span data-ttu-id="f16ce-324">Si la mise à jour du supplément Platform pour Windows Vista est installée, le décodeur audio AAC est disponible sur Windows Vista, mais il est accessible sur Windows Vista uniquement à l’aide du [lecteur source](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="f16ce-324">If Platform Update Supplement for Windows Vista is installed, the AAC audio decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f16ce-325">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f16ce-325">Requirements</span></span>



| <span data-ttu-id="f16ce-326">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f16ce-326">Requirement</span></span> | <span data-ttu-id="f16ce-327">Valeur</span><span class="sxs-lookup"><span data-stu-id="f16ce-327">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f16ce-328">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f16ce-328">Minimum supported client</span></span><br/> | <span data-ttu-id="f16ce-329">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f16ce-329">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="f16ce-330">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f16ce-330">Minimum supported server</span></span><br/> | <span data-ttu-id="f16ce-331">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f16ce-331">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="f16ce-332">DLL</span><span class="sxs-lookup"><span data-stu-id="f16ce-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f16ce-333"><dt>Msmpeg2adec.dll sur Windows 7 ; </dt> <dt>MSAudDecMFT.dll sur Windows 8</dt></span><span class="sxs-lookup"><span data-stu-id="f16ce-333"><dt>Msmpeg2adec.dll on Windows 7; </dt> <dt>MSAudDecMFT.dll on Windows 8</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16ce-334">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f16ce-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16ce-335">Objets codec</span><span class="sxs-lookup"><span data-stu-id="f16ce-335">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="f16ce-336">Types de média AAC</span><span class="sxs-lookup"><span data-stu-id="f16ce-336">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="f16ce-337">Types de média audio</span><span class="sxs-lookup"><span data-stu-id="f16ce-337">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="f16ce-338">**Décodeur audio Microsoft MPEG-1/DD/AAC**</span><span class="sxs-lookup"><span data-stu-id="f16ce-338">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[<span data-ttu-id="f16ce-339">Prise en charge MPEG-4 dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f16ce-339">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f16ce-340">Formats multimédias pris en charge dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f16ce-340">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>
