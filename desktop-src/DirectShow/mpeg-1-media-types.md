---
description: Cette section répertorie les types de médias utilisés pour les données MPEG-1.
ms.assetid: 4ea1cb84-0558-4c4a-9483-1b0f2a8f76f8
title: Types de média MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35d1ff7c121c52db39d574f9bbae3650b04312e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106535739"
---
# <a name="mpeg-1-media-types"></a><span data-ttu-id="b654a-103">Types de média MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-103">MPEG-1 Media Types</span></span>

<span data-ttu-id="b654a-104">Cette section répertorie les types de médias utilisés pour les données MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="b654a-104">This section lists the media types used for MPEG-1 data.</span></span>

## <a name="mpeg-1-system-stream"></a><span data-ttu-id="b654a-105">Flux système MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-105">MPEG-1 System Stream</span></span>



|                       |                                                 |
|-----------------------|-------------------------------------------------|
| <span data-ttu-id="b654a-106">Type principal</span><span class="sxs-lookup"><span data-stu-id="b654a-106">Major type</span></span>            | <span data-ttu-id="b654a-107">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="b654a-107">MEDIATYPE\_Stream</span></span>                               |
| <span data-ttu-id="b654a-108">Subtype</span><span class="sxs-lookup"><span data-stu-id="b654a-108">Subtype</span></span>               | <span data-ttu-id="b654a-109">MEDIASUBTYPE \_ MPEG1System</span><span class="sxs-lookup"><span data-stu-id="b654a-109">MEDIASUBTYPE\_MPEG1System</span></span>                       |
| <span data-ttu-id="b654a-110">Type de format</span><span class="sxs-lookup"><span data-stu-id="b654a-110">Format Type</span></span>           | <span data-ttu-id="b654a-111">FORMAT \_ MPEGStreams</span><span class="sxs-lookup"><span data-stu-id="b654a-111">FORMAT\_MPEGStreams</span></span>                             |
| <span data-ttu-id="b654a-112">Structure de format</span><span class="sxs-lookup"><span data-stu-id="b654a-112">Format Structure</span></span>      | [<span data-ttu-id="b654a-113">**AM \_ MPEGSYSTEMTYPE**</span><span class="sxs-lookup"><span data-stu-id="b654a-113">**AM\_MPEGSYSTEMTYPE**</span></span>](/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype) |
| <span data-ttu-id="b654a-114">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="b654a-114">Media Sample Contents</span></span> | <span data-ttu-id="b654a-115">Flux d’octets ; aucun alignement</span><span class="sxs-lookup"><span data-stu-id="b654a-115">Byte stream; no alignment</span></span>                       |



 

## <a name="mpeg-1-system-stream-from-video-cd"></a><span data-ttu-id="b654a-116">Flux système MPEG-1 à partir d’un CD vidéo</span><span class="sxs-lookup"><span data-stu-id="b654a-116">MPEG-1 System Stream from Video CD</span></span>



|                       |                            |
|-----------------------|----------------------------|
| <span data-ttu-id="b654a-117">Type principal</span><span class="sxs-lookup"><span data-stu-id="b654a-117">Major type</span></span>            | <span data-ttu-id="b654a-118">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="b654a-118">MEDIATYPE\_Stream</span></span>          |
| <span data-ttu-id="b654a-119">Subtype</span><span class="sxs-lookup"><span data-stu-id="b654a-119">Subtype</span></span>               | <span data-ttu-id="b654a-120">MEDIASUBTYPE \_ MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="b654a-120">MEDIASUBTYPE\_MPEG1VideoCD</span></span> |
| <span data-ttu-id="b654a-121">Type de format</span><span class="sxs-lookup"><span data-stu-id="b654a-121">Format Type</span></span>           | <span data-ttu-id="b654a-122">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="b654a-122">GUID\_NULL</span></span>                 |
| <span data-ttu-id="b654a-123">Structure de format</span><span class="sxs-lookup"><span data-stu-id="b654a-123">Format Structure</span></span>      | <span data-ttu-id="b654a-124">Aucun</span><span class="sxs-lookup"><span data-stu-id="b654a-124">None</span></span>                       |
| <span data-ttu-id="b654a-125">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="b654a-125">Media Sample Contents</span></span> | <span data-ttu-id="b654a-126">Flux d’octets ; aucun alignement.</span><span class="sxs-lookup"><span data-stu-id="b654a-126">Byte stream; no alignment.</span></span> |



 

## <a name="mpeg-1-audio-packet"></a><span data-ttu-id="b654a-127">Paquet audio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-127">MPEG-1 Audio Packet</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="b654a-128">Type principal</span><span class="sxs-lookup"><span data-stu-id="b654a-128">Major type</span></span>            | <span data-ttu-id="b654a-129">Audio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="b654a-129">MEDIATYPE\_Audio</span></span>                               |
| <span data-ttu-id="b654a-130">Subtype</span><span class="sxs-lookup"><span data-stu-id="b654a-130">Subtype</span></span>               | <span data-ttu-id="b654a-131">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="b654a-131">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="b654a-132">Type de format</span><span class="sxs-lookup"><span data-stu-id="b654a-132">Format Type</span></span>           | <span data-ttu-id="b654a-133">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="b654a-133">FORMAT\_WaveFormatEx</span></span>                           |
| <span data-ttu-id="b654a-134">Structure de format</span><span class="sxs-lookup"><span data-stu-id="b654a-134">Format Structure</span></span>      | [<span data-ttu-id="b654a-135">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="b654a-135">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat)     |
| <span data-ttu-id="b654a-136">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="b654a-136">Media Sample Contents</span></span> | <span data-ttu-id="b654a-137">Paquet MPEG-1 unique, y compris l’en-tête de paquet.</span><span class="sxs-lookup"><span data-stu-id="b654a-137">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-audio-payload"></a><span data-ttu-id="b654a-138">Charge utile MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-138">MPEG-1 Audio Payload</span></span>



|                       |                                            |
|-----------------------|--------------------------------------------|
| <span data-ttu-id="b654a-139">Type principal</span><span class="sxs-lookup"><span data-stu-id="b654a-139">Major type</span></span>            | <span data-ttu-id="b654a-140">Audio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="b654a-140">MEDIATYPE\_Audio</span></span>                           |
| <span data-ttu-id="b654a-141">Subtype</span><span class="sxs-lookup"><span data-stu-id="b654a-141">Subtype</span></span>               | <span data-ttu-id="b654a-142">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="b654a-142">MEDIASUBTYPE\_MPEG1Payload</span></span>                 |
| <span data-ttu-id="b654a-143">Type de format</span><span class="sxs-lookup"><span data-stu-id="b654a-143">Format Type</span></span>           | <span data-ttu-id="b654a-144">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="b654a-144">FORMAT\_WaveFormatEx</span></span>                       |
| <span data-ttu-id="b654a-145">Structure de format</span><span class="sxs-lookup"><span data-stu-id="b654a-145">Format Structure</span></span>      | [<span data-ttu-id="b654a-146">**MPEG1WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="b654a-146">**MPEG1WAVEFORMAT**</span></span>](/windows/desktop/api/mmreg/ns-mmreg-mpeg1waveformat) |
| <span data-ttu-id="b654a-147">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="b654a-147">Media Sample Contents</span></span> | <span data-ttu-id="b654a-148">Données audio MPEG-1 alignées sur les octets.</span><span class="sxs-lookup"><span data-stu-id="b654a-148">Byte-aligned MPEG-1 audio data.</span></span>            |



 

## <a name="mpeg-1-video-packet"></a><span data-ttu-id="b654a-149">Paquet vidéo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-149">MPEG-1 Video Packet</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="b654a-150">Type principal</span><span class="sxs-lookup"><span data-stu-id="b654a-150">Major type</span></span>            | <span data-ttu-id="b654a-151">Vidéo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="b654a-151">MEDIATYPE\_Video</span></span>                               |
| <span data-ttu-id="b654a-152">Subtype</span><span class="sxs-lookup"><span data-stu-id="b654a-152">Subtype</span></span>               | <span data-ttu-id="b654a-153">MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="b654a-153">MEDIASUBTYPE\_MPEG1Packet</span></span>                      |
| <span data-ttu-id="b654a-154">Type de format</span><span class="sxs-lookup"><span data-stu-id="b654a-154">Format Type</span></span>           | <span data-ttu-id="b654a-155">FORMAT \_ mpegvideo</span><span class="sxs-lookup"><span data-stu-id="b654a-155">FORMAT\_MPEGVideo</span></span>                              |
| <span data-ttu-id="b654a-156">Structure de format</span><span class="sxs-lookup"><span data-stu-id="b654a-156">Format Structure</span></span>      | [<span data-ttu-id="b654a-157">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="b654a-157">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)       |
| <span data-ttu-id="b654a-158">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="b654a-158">Media Sample Contents</span></span> | <span data-ttu-id="b654a-159">Paquet MPEG-1 unique, y compris l’en-tête de paquet.</span><span class="sxs-lookup"><span data-stu-id="b654a-159">Single MPEG-1 packet, including packet header.</span></span> |



 

## <a name="mpeg-1-video-payload"></a><span data-ttu-id="b654a-160">Charge utile vidéo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-160">MPEG-1 Video payload</span></span>



|                       |                                          |
|-----------------------|------------------------------------------|
| <span data-ttu-id="b654a-161">Type principal</span><span class="sxs-lookup"><span data-stu-id="b654a-161">Major type</span></span>            | <span data-ttu-id="b654a-162">Vidéo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="b654a-162">MEDIATYPE\_Video</span></span>                         |
| <span data-ttu-id="b654a-163">Subtype</span><span class="sxs-lookup"><span data-stu-id="b654a-163">Subtype</span></span>               | <span data-ttu-id="b654a-164">MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="b654a-164">MEDIASUBTYPE\_MPEG1Payload</span></span>               |
| <span data-ttu-id="b654a-165">Type de format</span><span class="sxs-lookup"><span data-stu-id="b654a-165">Format Type</span></span>           | <span data-ttu-id="b654a-166">FORMAT \_ mpegvideo</span><span class="sxs-lookup"><span data-stu-id="b654a-166">FORMAT\_MPEGVideo</span></span>                        |
| <span data-ttu-id="b654a-167">Structure de format</span><span class="sxs-lookup"><span data-stu-id="b654a-167">Format Structure</span></span>      | [<span data-ttu-id="b654a-168">**MPEG1VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="b654a-168">**MPEG1VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) |
| <span data-ttu-id="b654a-169">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="b654a-169">Media Sample Contents</span></span> | <span data-ttu-id="b654a-170">Données vidéo MPEG-1 alignées sur les octets.</span><span class="sxs-lookup"><span data-stu-id="b654a-170">Byte-aligned MPEG-1 video data.</span></span>          |



 

## <a name="mpeg-1-native-video-stream"></a><span data-ttu-id="b654a-171">Flux vidéo natif MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-171">MPEG-1 Native Video Stream</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="b654a-172">Type principal</span><span class="sxs-lookup"><span data-stu-id="b654a-172">Major type</span></span>            | <span data-ttu-id="b654a-173">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="b654a-173">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="b654a-174">Subtype</span><span class="sxs-lookup"><span data-stu-id="b654a-174">Subtype</span></span>               | <span data-ttu-id="b654a-175">MEDIASUBTYPE \_ MPEG1Video</span><span class="sxs-lookup"><span data-stu-id="b654a-175">MEDIASUBTYPE\_ MPEG1Video</span></span>                      |
| <span data-ttu-id="b654a-176">Type de format</span><span class="sxs-lookup"><span data-stu-id="b654a-176">Format Type</span></span>           | <span data-ttu-id="b654a-177">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="b654a-177">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="b654a-178">Structure de format</span><span class="sxs-lookup"><span data-stu-id="b654a-178">Format Structure</span></span>      | <span data-ttu-id="b654a-179">Aucun</span><span class="sxs-lookup"><span data-stu-id="b654a-179">None</span></span>                                           |
| <span data-ttu-id="b654a-180">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="b654a-180">Media Sample Contents</span></span> | <span data-ttu-id="b654a-181">Tableau d’octets de flux vidéo (aucune couche système).</span><span class="sxs-lookup"><span data-stu-id="b654a-181">Array of video stream bytes (no system layer).</span></span> |



 

## <a name="mpeg-1-native-audio-stream"></a><span data-ttu-id="b654a-182">Flux audio natif MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-182">MPEG-1 Native Audio Stream</span></span>



|                       |                                                |
|-----------------------|------------------------------------------------|
| <span data-ttu-id="b654a-183">Type principal</span><span class="sxs-lookup"><span data-stu-id="b654a-183">Major type</span></span>            | <span data-ttu-id="b654a-184">Flux de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="b654a-184">MEDIATYPE\_Stream</span></span>                              |
| <span data-ttu-id="b654a-185">Subtype</span><span class="sxs-lookup"><span data-stu-id="b654a-185">Subtype</span></span>               | <span data-ttu-id="b654a-186">MEDIASUBTYPE \_ MPEG1Audio</span><span class="sxs-lookup"><span data-stu-id="b654a-186">MEDIASUBTYPE\_ MPEG1Audio</span></span>                      |
| <span data-ttu-id="b654a-187">Type de format</span><span class="sxs-lookup"><span data-stu-id="b654a-187">Format Type</span></span>           | <span data-ttu-id="b654a-188">GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="b654a-188">GUID\_NULL</span></span>                                     |
| <span data-ttu-id="b654a-189">Structure de format</span><span class="sxs-lookup"><span data-stu-id="b654a-189">Format Structure</span></span>      | <span data-ttu-id="b654a-190">Aucun</span><span class="sxs-lookup"><span data-stu-id="b654a-190">None</span></span>                                           |
| <span data-ttu-id="b654a-191">Exemple de contenu multimédia</span><span class="sxs-lookup"><span data-stu-id="b654a-191">Media Sample Contents</span></span> | <span data-ttu-id="b654a-192">Tableau d’octets de flux audio (aucune couche système).</span><span class="sxs-lookup"><span data-stu-id="b654a-192">Array of audio stream bytes (no system layer).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b654a-193">Notes</span><span class="sxs-lookup"><span data-stu-id="b654a-193">Remarks</span></span>

<span data-ttu-id="b654a-194">Les filtres MPEG-1 DirectShow prennent en charge ces types comme suit.</span><span class="sxs-lookup"><span data-stu-id="b654a-194">The DirectShow MPEG-1 filters support these types as follows.</span></span>



| <span data-ttu-id="b654a-195">Filtrer</span><span class="sxs-lookup"><span data-stu-id="b654a-195">Filter</span></span>               | <span data-ttu-id="b654a-196">Sens</span><span class="sxs-lookup"><span data-stu-id="b654a-196">Direction</span></span> | <span data-ttu-id="b654a-197">Types de média pris en charge</span><span class="sxs-lookup"><span data-stu-id="b654a-197">Supported media types</span></span>                                                                                             |
|----------------------|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b654a-198">Séparateur MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-198">MPEG-1 Splitter</span></span>      | <span data-ttu-id="b654a-199">Entrée</span><span class="sxs-lookup"><span data-stu-id="b654a-199">Input</span></span>     | <span data-ttu-id="b654a-200">MPEG-1 système streamMPEG-1 flux système à partir du CD vidéo</span><span class="sxs-lookup"><span data-stu-id="b654a-200">MPEG-1 system streamMPEG-1 system stream from Video CD</span></span><br/>                                                 |
| <span data-ttu-id="b654a-201">Séparateur MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-201">MPEG-1 Splitter</span></span>      | <span data-ttu-id="b654a-202">Output</span><span class="sxs-lookup"><span data-stu-id="b654a-202">Output</span></span>    | <span data-ttu-id="b654a-203">Charge utile MPEG-1 audio packetMPEG-1 audio</span><span class="sxs-lookup"><span data-stu-id="b654a-203">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/> <span data-ttu-id="b654a-204">Paquet vidéo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-204">MPEG-1 Video packet</span></span><br/> <span data-ttu-id="b654a-205">Charge utile vidéo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-205">MPEG-1 Video payload</span></span><br/> |
| <span data-ttu-id="b654a-206">Codec audio logiciel</span><span class="sxs-lookup"><span data-stu-id="b654a-206">Software Audio Codec</span></span> | <span data-ttu-id="b654a-207">Entrée</span><span class="sxs-lookup"><span data-stu-id="b654a-207">Input</span></span>     | <span data-ttu-id="b654a-208">Charge utile MPEG-1 audio packetMPEG-1 audio</span><span class="sxs-lookup"><span data-stu-id="b654a-208">MPEG-1 Audio packetMPEG-1 Audio payload</span></span><br/>                                                                |
| <span data-ttu-id="b654a-209">Codec vidéo logiciel</span><span class="sxs-lookup"><span data-stu-id="b654a-209">Software Video Codec</span></span> | <span data-ttu-id="b654a-210">Entrée</span><span class="sxs-lookup"><span data-stu-id="b654a-210">Input</span></span>     | <span data-ttu-id="b654a-211">Charge utile vidéo MPEG-1 Video packetMPEG-1</span><span class="sxs-lookup"><span data-stu-id="b654a-211">MPEG-1 Video packetMPEG-1 Video payload</span></span><br/>                                                                |
| <span data-ttu-id="b654a-212">Codec audio logiciel</span><span class="sxs-lookup"><span data-stu-id="b654a-212">Software Audio Codec</span></span> | <span data-ttu-id="b654a-213">Output</span><span class="sxs-lookup"><span data-stu-id="b654a-213">Output</span></span>    | <span data-ttu-id="b654a-214">Audio PCM</span><span class="sxs-lookup"><span data-stu-id="b654a-214">PCM audio</span></span>                                                                                                         |
| <span data-ttu-id="b654a-215">Codec vidéo logiciel</span><span class="sxs-lookup"><span data-stu-id="b654a-215">Software Video Codec</span></span> | <span data-ttu-id="b654a-216">Output</span><span class="sxs-lookup"><span data-stu-id="b654a-216">Output</span></span>    | <span data-ttu-id="b654a-217">Vidéo non compressée (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RVB-8)</span><span class="sxs-lookup"><span data-stu-id="b654a-217">Uncompressed video (Y41P, YUY2, UYVY, RGB-24, RGB-32, RGB-565, RGB-555, RGB-8)</span></span>                                    |



 

<span data-ttu-id="b654a-218">Les types de média de paquets vidéo MPEG-1 et de charge utile contiennent un en-tête de séquence complet afin que les données puissent être lues à partir du milieu d’un fichier sans avoir besoin d’un en-tête de séquence pour initialiser la lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="b654a-218">MPEG-1 Video packet and payload media types contain a complete sequence header so that data can be played from the middle of a file without needing a sequence header to initialize the video playback.</span></span>

<span data-ttu-id="b654a-219">L’en-tête de séquence vidéo est ajouté au type de données vidéo pour la vidéo MPEG, de sorte que la lecture peut commencer à partir du milieu d’un flux.</span><span class="sxs-lookup"><span data-stu-id="b654a-219">The video sequence header is appended to the video data type for MPEG video so that play can begin from the middle of a stream.</span></span> <span data-ttu-id="b654a-220">La longueur de ce champ est de 140 octets. Il comprend le code de début d’en-tête de séquence (0x000001B3) au début, ainsi que toutes les matrices de quantification trouvées dans le premier en-tête de séquence rencontré.</span><span class="sxs-lookup"><span data-stu-id="b654a-220">The length of this field is up to 140 bytes; it includes the sequence header start code (0x000001B3) at the start, along with any quantization matrices found in the first sequence header encountered.</span></span>

 

 




