---
description: Cette section répertorie les types de médias utilisés pour les données MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Types de média MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e44db1f4423365efb7814d61b35c1985142aa14
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910027"
---
# <a name="mpeg-1-media-types"></a><span data-ttu-id="292ee-103">Types de média MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-103">MPEG-1 Media Types</span></span>

<span data-ttu-id="292ee-104">Cette section répertorie les types de médias utilisés pour les données MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="292ee-104">This section lists the media types used for MPEG-1 data.</span></span>

## <a name="mpeg-1-system-stream"></a><span data-ttu-id="292ee-105">Flux système MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-105">MPEG-1 System Stream</span></span>



| <span data-ttu-id="292ee-106">Étiquette</span><span class="sxs-lookup"><span data-stu-id="292ee-106">Label</span></span> | <span data-ttu-id="292ee-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="292ee-107">Value</span></span> |
|-----------------------|-------------------------------------------------|
| <span data-ttu-id="292ee-108">Type principal</span><span class="sxs-lookup"><span data-stu-id="292ee-108">Major type</span></span>            | <span data-ttu-id="292ee-109">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="292ee-109">MEDIATYPE\_Stream</span></span>                               |
| <span data-ttu-id="292ee-110">Subtype</span><span class="sxs-lookup"><span data-stu-id="292ee-110">Subtype</span></span>               | <span data-ttu-id="292ee-111">MEDIASUBTYPE \_ MPEG1System</span><span class="sxs-lookup"><span data-stu-id="292ee-111">MEDIASUBTYPE\_MPEG1System</span></span>                       |
| <span data-ttu-id="292ee-112">Type de format</span><span class="sxs-lookup"><span data-stu-id="292ee-112">Format Type</span></span>           | <span data-ttu-id="292ee-113">FORMAT \_ MPEGStreams</span><span class="sxs-lookup"><span data-stu-id="292ee-113">FORMAT\_MPEGStreams</span></span>                             |
| <span data-ttu-id="292ee-114">Structure de format</span><span class="sxs-lookup"><span data-stu-id="292ee-114">Format Structure</span></span>      | [<span data-ttu-id="292ee-115">**AM \_ MPEGSYSTEMTYPE**</span><span class="sxs-lookup"><span data-stu-id="292ee-115">**AM\_MPEGSYSTEMTYPE**</span></span>](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| <span data-ttu-id="292ee-116">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="292ee-116">Media Sample Contents</span></span> | <span data-ttu-id="292ee-117">Flux d’octets ; aucun alignement</span><span class="sxs-lookup"><span data-stu-id="292ee-117">Byte stream; no alignment</span></span>                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a><span data-ttu-id="292ee-118">Flux système MPEG-1 à partir d’un CD vidéo</span><span class="sxs-lookup"><span data-stu-id="292ee-118">MPEG-1 System Stream from Video CD</span></span>



| <span data-ttu-id="292ee-119">Étiquette</span><span class="sxs-lookup"><span data-stu-id="292ee-119">Label</span></span> | <span data-ttu-id="292ee-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="292ee-120">Value</span></span> |
|-----------------------|----------------------------|
| <span data-ttu-id="292ee-121">Type principal</span><span class="sxs-lookup"><span data-stu-id="292ee-121">Major type</span></span>            | <span data-ttu-id="292ee-122">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="292ee-122">MEDIATYPE\_Stream</span></span>          |
| <span data-ttu-id="292ee-123">Subtype</span><span class="sxs-lookup"><span data-stu-id="292ee-123">Subtype</span></span>               | <span data-ttu-id="292ee-124">MEDIASUBTYPE \_ MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="292ee-124">MEDIASUBTYPE\_MPEG1VideoCD</span></span> |
| <span data-ttu-id="292ee-125">Type de format</span><span class="sxs-lookup"><span data-stu-id="292ee-125">Format Type</span></span>           | <span data-ttu-id="292ee-126">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="292ee-126">GUID\_NULL</span></span>                 |
| <span data-ttu-id="292ee-127">Structure de format</span><span class="sxs-lookup"><span data-stu-id="292ee-127">Format Structure</span></span>      | <span data-ttu-id="292ee-128">Aucun</span><span class="sxs-lookup"><span data-stu-id="292ee-128">None</span></span>                       |
| <span data-ttu-id="292ee-129">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="292ee-129">Media Sample Contents</span></span> | <span data-ttu-id="292ee-130">Flux d’octets ; aucun alignement.</span><span class="sxs-lookup"><span data-stu-id="292ee-130">Byte stream; no alignment.</span></span> |



 

## <a name="mpeg-1-audio-packet"></a><span data-ttu-id="292ee-131">Paquet audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-131">MPEG-1 Audio Packet</span></span>



| <span data-ttu-id="292ee-132">Étiquette</span><span class="sxs-lookup"><span data-stu-id="292ee-132">Label</span></span> | <span data-ttu-id="292ee-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="292ee-133">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="292ee-134">Type principal</span><span class="sxs-lookup"><span data-stu-id="292ee-134">Major type</span></span>            | <span data-ttu-id="292ee-135">Audio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="292ee-135">MEDIATYPE\_Audio</span></span>                               |
| <span data-ttu-id="292ee-136">Subtype</span><span class="sxs-lookup"><span data-stu-id="292ee-136">Subtype</span></span>               | <span data-ttu-id="292ee-137">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="292ee-137">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="292ee-138">Type de format</span><span class="sxs-lookup"><span data-stu-id="292ee-138">Format Type</span></span>           | <span data-ttu-id="292ee-139">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="292ee-139">FORMAT\_WaveFormatEx</span></span>                           |
| <span data-ttu-id="292ee-140">Structure de format</span><span class="sxs-lookup"><span data-stu-id="292ee-140">Format Structure</span></span>      | [<span data-ttu-id="292ee-141">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="292ee-141">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| <span data-ttu-id="292ee-142">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="292ee-142">Media Sample Contents</span></span> | <span data-ttu-id="292ee-143">Paquet MPEG-1 unique, y compris l’en-tête de paquet.</span><span class="sxs-lookup"><span data-stu-id="292ee-143">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-audio-payload"></a><span data-ttu-id="292ee-144">Charge utile MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-144">MPEG-1 Audio Payload</span></span>



| <span data-ttu-id="292ee-145">Étiquette</span><span class="sxs-lookup"><span data-stu-id="292ee-145">Label</span></span> | <span data-ttu-id="292ee-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="292ee-146">Value</span></span> |
|-----------------------|--------------------------------------------|
| <span data-ttu-id="292ee-147">Type principal</span><span class="sxs-lookup"><span data-stu-id="292ee-147">Major type</span></span>            | <span data-ttu-id="292ee-148">Audio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="292ee-148">MEDIATYPE\_Audio</span></span>                           |
| <span data-ttu-id="292ee-149">Subtype</span><span class="sxs-lookup"><span data-stu-id="292ee-149">Subtype</span></span>               | <span data-ttu-id="292ee-150">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="292ee-150">MEDIASUBTYPE\_MPEG1Payload</span></span>                 |
| <span data-ttu-id="292ee-151">Type de format</span><span class="sxs-lookup"><span data-stu-id="292ee-151">Format Type</span></span>           | <span data-ttu-id="292ee-152">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="292ee-152">FORMAT\_WaveFormatEx</span></span>                       |
| <span data-ttu-id="292ee-153">Structure de format</span><span class="sxs-lookup"><span data-stu-id="292ee-153">Format Structure</span></span>      | [<span data-ttu-id="292ee-154">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="292ee-154">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| <span data-ttu-id="292ee-155">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="292ee-155">Media Sample Contents</span></span> | <span data-ttu-id="292ee-156">Données audio MPEG-1 alignées sur les octets.</span><span class="sxs-lookup"><span data-stu-id="292ee-156">Byte-aligned MPEG-1 audio data.</span></span>            |



 

## <a name="mpeg-1-video-packet"></a><span data-ttu-id="292ee-157">Paquet vidéo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-157">MPEG-1 Video Packet</span></span>



| <span data-ttu-id="292ee-158">Étiquette</span><span class="sxs-lookup"><span data-stu-id="292ee-158">Label</span></span> | <span data-ttu-id="292ee-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="292ee-159">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="292ee-160">Type principal</span><span class="sxs-lookup"><span data-stu-id="292ee-160">Major type</span></span>            | <span data-ttu-id="292ee-161">Vidéo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="292ee-161">MEDIATYPE\_Video</span></span>                               |
| <span data-ttu-id="292ee-162">Subtype</span><span class="sxs-lookup"><span data-stu-id="292ee-162">Subtype</span></span>               | <span data-ttu-id="292ee-163">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="292ee-163">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="292ee-164">Type de format</span><span class="sxs-lookup"><span data-stu-id="292ee-164">Format Type</span></span>           | <span data-ttu-id="292ee-165">FORMAT \_ mpegvideo</span><span class="sxs-lookup"><span data-stu-id="292ee-165">FORMAT\_MPEGVideo</span></span>                              |
| <span data-ttu-id="292ee-166">Structure de format</span><span class="sxs-lookup"><span data-stu-id="292ee-166">Format Structure</span></span>      | [<span data-ttu-id="292ee-167">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="292ee-167">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| <span data-ttu-id="292ee-168">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="292ee-168">Media Sample Contents</span></span> | <span data-ttu-id="292ee-169">Paquet MPEG-1 unique, y compris l’en-tête de paquet.</span><span class="sxs-lookup"><span data-stu-id="292ee-169">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-video-payload"></a><span data-ttu-id="292ee-170">Charge utile vidéo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-170">MPEG-1 Video payload</span></span>



| <span data-ttu-id="292ee-171">Étiquette</span><span class="sxs-lookup"><span data-stu-id="292ee-171">Label</span></span> | <span data-ttu-id="292ee-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="292ee-172">Value</span></span> |
|-----------------------|------------------------------------------|
| <span data-ttu-id="292ee-173">Type principal</span><span class="sxs-lookup"><span data-stu-id="292ee-173">Major type</span></span>            | <span data-ttu-id="292ee-174">Vidéo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="292ee-174">MEDIATYPE\_Video</span></span>                         |
| <span data-ttu-id="292ee-175">Subtype</span><span class="sxs-lookup"><span data-stu-id="292ee-175">Subtype</span></span>               | <span data-ttu-id="292ee-176">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="292ee-176">MEDIASUBTYPE\_MPEG1Payload</span></span>               |
| <span data-ttu-id="292ee-177">Type de format</span><span class="sxs-lookup"><span data-stu-id="292ee-177">Format Type</span></span>           | <span data-ttu-id="292ee-178">FORMAT \_ mpegvideo</span><span class="sxs-lookup"><span data-stu-id="292ee-178">FORMAT\_MPEGVideo</span></span>                        |
| <span data-ttu-id="292ee-179">Structure de format</span><span class="sxs-lookup"><span data-stu-id="292ee-179">Format Structure</span></span>      | [<span data-ttu-id="292ee-180">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="292ee-180">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| <span data-ttu-id="292ee-181">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="292ee-181">Media Sample Contents</span></span> | <span data-ttu-id="292ee-182">Données vidéo MPEG-1 alignées sur les octets.</span><span class="sxs-lookup"><span data-stu-id="292ee-182">Byte-aligned MPEG-1 video data.</span></span>          |



 

## <a name="mpeg-1-native-video-stream"></a><span data-ttu-id="292ee-183">Flux vidéo natif MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-183">MPEG-1 Native Video Stream</span></span>



| <span data-ttu-id="292ee-184">Étiquette</span><span class="sxs-lookup"><span data-stu-id="292ee-184">Label</span></span> | <span data-ttu-id="292ee-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="292ee-185">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="292ee-186">Type principal</span><span class="sxs-lookup"><span data-stu-id="292ee-186">Major type</span></span>            | <span data-ttu-id="292ee-187">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="292ee-187">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="292ee-188">Subtype</span><span class="sxs-lookup"><span data-stu-id="292ee-188">Subtype</span></span>               | <span data-ttu-id="292ee-189">MEDIASUBTYPE \_ MPEG1Video</span><span class="sxs-lookup"><span data-stu-id="292ee-189">MEDIASUBTYPE\_ MPEG1Video</span></span>                      |
| <span data-ttu-id="292ee-190">Type de format</span><span class="sxs-lookup"><span data-stu-id="292ee-190">Format Type</span></span>           | <span data-ttu-id="292ee-191">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="292ee-191">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="292ee-192">Structure de format</span><span class="sxs-lookup"><span data-stu-id="292ee-192">Format Structure</span></span>      | <span data-ttu-id="292ee-193">Aucun</span><span class="sxs-lookup"><span data-stu-id="292ee-193">None</span></span>                                           |
| <span data-ttu-id="292ee-194">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="292ee-194">Media Sample Contents</span></span> | <span data-ttu-id="292ee-195">Tableau d’octets de flux vidéo (aucune couche système).</span><span class="sxs-lookup"><span data-stu-id="292ee-195">Array of video stream bytes (no system layer).</span></span> |



 

## <a name="mpeg-1-native-audio-stream"></a><span data-ttu-id="292ee-196">Flux audio natif MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-196">MPEG-1 Native Audio Stream</span></span>



| <span data-ttu-id="292ee-197">Étiquette</span><span class="sxs-lookup"><span data-stu-id="292ee-197">Label</span></span> | <span data-ttu-id="292ee-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="292ee-198">Value</span></span> |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="292ee-199">Type principal</span><span class="sxs-lookup"><span data-stu-id="292ee-199">Major type</span></span>            | <span data-ttu-id="292ee-200">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="292ee-200">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="292ee-201">Subtype</span><span class="sxs-lookup"><span data-stu-id="292ee-201">Subtype</span></span>               | <span data-ttu-id="292ee-202">MEDIASUBTYPE \_ MPEG1Audio</span><span class="sxs-lookup"><span data-stu-id="292ee-202">MEDIASUBTYPE\_ MPEG1Audio</span></span>                      |
| <span data-ttu-id="292ee-203">Type de format</span><span class="sxs-lookup"><span data-stu-id="292ee-203">Format Type</span></span>           | <span data-ttu-id="292ee-204">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="292ee-204">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="292ee-205">Structure de format</span><span class="sxs-lookup"><span data-stu-id="292ee-205">Format Structure</span></span>      | <span data-ttu-id="292ee-206">Aucun</span><span class="sxs-lookup"><span data-stu-id="292ee-206">None</span></span>                                           |
| <span data-ttu-id="292ee-207">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="292ee-207">Media Sample Contents</span></span> | <span data-ttu-id="292ee-208">Tableau d’octets de flux audio (aucune couche système).</span><span class="sxs-lookup"><span data-stu-id="292ee-208">Array of audio stream bytes (no system layer).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="292ee-209">Remarques</span><span class="sxs-lookup"><span data-stu-id="292ee-209">Remarks</span></span>

<span data-ttu-id="292ee-210">Les filtres MPEG-1 DirectShow prennent en charge ces types comme suit.</span><span class="sxs-lookup"><span data-stu-id="292ee-210">The DirectShow MPEG-1 filters support these types as follows.</span></span>



| <span data-ttu-id="292ee-211">Filtrer</span><span class="sxs-lookup"><span data-stu-id="292ee-211">Filter</span></span>               | <span data-ttu-id="292ee-212">Direction</span><span class="sxs-lookup"><span data-stu-id="292ee-212">Direction</span></span> | <span data-ttu-id="292ee-213">Types de média pris en charge</span><span class="sxs-lookup"><span data-stu-id="292ee-213">Supported media types</span></span>                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="292ee-214">Séparateur MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-214">MPEG-1 Splitter</span></span>      | <span data-ttu-id="292ee-215">Entrée</span><span class="sxs-lookup"><span data-stu-id="292ee-215">Input</span></span>     | <span data-ttu-id="292ee-216">MPEG-1 système streamMPEG-1 flux système à partir du CD vidéo</span><span class="sxs-lookup"><span data-stu-id="292ee-216">MPEG-1 system streamMPEG-1 system stream from Video CD</span></span><br/>                                                 |
| <span data-ttu-id="292ee-217">Séparateur MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-217">MPEG-1 Splitter</span></span>      | <span data-ttu-id="292ee-218">Sortie</span><span class="sxs-lookup"><span data-stu-id="292ee-218">Output</span></span>    | <span data-ttu-id="292ee-219">Charge utile MPEG-1 audio packetMPEG-1 audio</span><span class="sxs-lookup"><span data-stu-id="292ee-219">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/> <span data-ttu-id="292ee-220">Paquet vidéo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-220">MPEG-1 Video packet</span></span><br/> <span data-ttu-id="292ee-221">Charge utile vidéo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-221">MPEG-1 Video payload</span></span><br/> |
| <span data-ttu-id="292ee-222">Codec audio logiciel</span><span class="sxs-lookup"><span data-stu-id="292ee-222">Software Audio Codec</span></span> | <span data-ttu-id="292ee-223">Entrée</span><span class="sxs-lookup"><span data-stu-id="292ee-223">Input</span></span>     | <span data-ttu-id="292ee-224">Charge utile MPEG-1 audio packetMPEG-1 audio</span><span class="sxs-lookup"><span data-stu-id="292ee-224">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/>                                                                |
| <span data-ttu-id="292ee-225">Codec vidéo logiciel</span><span class="sxs-lookup"><span data-stu-id="292ee-225">Software Video Codec</span></span> | <span data-ttu-id="292ee-226">Entrée</span><span class="sxs-lookup"><span data-stu-id="292ee-226">Input</span></span>     | <span data-ttu-id="292ee-227">Charge utile vidéo MPEG-1 Video packetMPEG-1</span><span class="sxs-lookup"><span data-stu-id="292ee-227">MPEG-1 Video packetMPEG-1 Video payload</span></span><br/>                                                                |
| <span data-ttu-id="292ee-228">Codec audio logiciel</span><span class="sxs-lookup"><span data-stu-id="292ee-228">Software Audio Codec</span></span> | <span data-ttu-id="292ee-229">Sortie</span><span class="sxs-lookup"><span data-stu-id="292ee-229">Output</span></span>    | <span data-ttu-id="292ee-230">Audio PCM</span><span class="sxs-lookup"><span data-stu-id="292ee-230">PCM audio</span></span>                                                                                                         |
| <span data-ttu-id="292ee-231">Codec vidéo logiciel</span><span class="sxs-lookup"><span data-stu-id="292ee-231">Software Video Codec</span></span> | <span data-ttu-id="292ee-232">Sortie</span><span class="sxs-lookup"><span data-stu-id="292ee-232">Output</span></span>    | <span data-ttu-id="292ee-233">Vidéo non compressée (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RVB-8)</span><span class="sxs-lookup"><span data-stu-id="292ee-233">Uncompressed video (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span></span>                                    |



 

<span data-ttu-id="292ee-234">Les types de média de paquets vidéo MPEG-1 et de charge utile contiennent un en-tête de séquence complet afin que les données puissent être lues à partir du milieu d’un fichier sans avoir besoin d’un en-tête de séquence pour initialiser la lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="292ee-234">MPEG-1 Video packet and payload media types contain a complete sequence header so that data can be played from the middle of a file without needing a sequence header to initialize the video playback.</span></span>

<span data-ttu-id="292ee-235">L’en-tête de séquence vidéo est ajouté au type de données vidéo pour la vidéo MPEG, de sorte que la lecture peut commencer à partir du milieu d’un flux.</span><span class="sxs-lookup"><span data-stu-id="292ee-235">The video sequence header is appended to the video data type for MPEG video so that play can begin from the middle of a stream.</span></span> <span data-ttu-id="292ee-236">La longueur de ce champ est de 140 octets. Il comprend le code de début d’en-tête de séquence (0x000001B3) au début, ainsi que toutes les matrices de quantification trouvées dans le premier en-tête de séquence rencontré.</span><span class="sxs-lookup"><span data-stu-id="292ee-236">The length of this field is up to 140 bytes; it includes the sequence header start code (0x000001B3) at the start, along with any quantization matrices found in the first sequence header encountered.</span></span>

 

 




