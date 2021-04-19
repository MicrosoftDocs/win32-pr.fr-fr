---
description: Types de média MPEG-2 Splitter
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Types de média MPEG-2 Splitter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb10310bd126346c8e1558801200682792836d92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522881"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="389d5-103">Types de média MPEG-2 Splitter</span><span class="sxs-lookup"><span data-stu-id="389d5-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="389d5-104">Le filtre de [séparateur MPEG-2](mpeg-2-splitter.md) prend actuellement en charge l’audio et la vidéo.</span><span class="sxs-lookup"><span data-stu-id="389d5-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="389d5-105">Dolby AC-3 est pris en charge en tant que sous-flux, comme défini par DVD.</span><span class="sxs-lookup"><span data-stu-id="389d5-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="389d5-106">Le filtre prend également en charge le format audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="389d5-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="389d5-107">Les types de médias varient selon que le séparateur MPEG-2 fournit des paquets PES ou des charges utiles PES.</span><span class="sxs-lookup"><span data-stu-id="389d5-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="389d5-108">Vidéo</span><span class="sxs-lookup"><span data-stu-id="389d5-108">Video</span></span>

<span data-ttu-id="389d5-109">Pour les vidéos MPEG-2, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="389d5-109">For MPEG-2 video, the media types are as follows.</span></span>



|                  |                                          |                                |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="389d5-110">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="389d5-110">PES output</span></span>                               | <span data-ttu-id="389d5-111">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="389d5-111">Payload output</span></span>                 |
| <span data-ttu-id="389d5-112">Type principal</span><span class="sxs-lookup"><span data-stu-id="389d5-112">Major Type</span></span>       | <span data-ttu-id="389d5-113">**\_PES MPEG2 de MediaType \_**</span><span class="sxs-lookup"><span data-stu-id="389d5-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="389d5-114">**Vidéo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="389d5-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="389d5-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="389d5-115">Subtype</span></span>          | <span data-ttu-id="389d5-116">**\_Vidéo MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="389d5-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="389d5-117">**\_Vidéo MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="389d5-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="389d5-118">Type de format</span><span class="sxs-lookup"><span data-stu-id="389d5-118">Format Type</span></span>      | <span data-ttu-id="389d5-119">**FORMAT \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="389d5-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="389d5-120">**FORMAT \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="389d5-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="389d5-121">Structure de format</span><span class="sxs-lookup"><span data-stu-id="389d5-121">Format Structure</span></span> | [<span data-ttu-id="389d5-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="389d5-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="389d5-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="389d5-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="389d5-124">Audio AC-3</span><span class="sxs-lookup"><span data-stu-id="389d5-124">AC-3 Audio</span></span>

<span data-ttu-id="389d5-125">Pour le son AC-3, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="389d5-125">For AC-3 audio, the media types are as follows.</span></span>



|                  |                                      |                              |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="389d5-126">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="389d5-126">PES output</span></span>                           | <span data-ttu-id="389d5-127">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="389d5-127">Payload output</span></span>               |
| <span data-ttu-id="389d5-128">Type principal</span><span class="sxs-lookup"><span data-stu-id="389d5-128">Major Type</span></span>       | <span data-ttu-id="389d5-129">\_PES MPEG2 de MediaType \_</span><span class="sxs-lookup"><span data-stu-id="389d5-129">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="389d5-130">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="389d5-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="389d5-131">Subtype</span><span class="sxs-lookup"><span data-stu-id="389d5-131">Subtype</span></span>          | <span data-ttu-id="389d5-132">MEDIASUBTYPE \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="389d5-132">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="389d5-133">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="389d5-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="389d5-134">Type de format</span><span class="sxs-lookup"><span data-stu-id="389d5-134">Format Type</span></span>      | <span data-ttu-id="389d5-135">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="389d5-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="389d5-136">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="389d5-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="389d5-137">Structure de format</span><span class="sxs-lookup"><span data-stu-id="389d5-137">Format Structure</span></span> | <span data-ttu-id="389d5-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="389d5-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="389d5-139">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="389d5-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="389d5-140">Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour AC-3 est **actuellement \_ \_ inconnu**, mais cela peut changer.</span><span class="sxs-lookup"><span data-stu-id="389d5-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="389d5-141">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="389d5-141">MPEG-2 Audio</span></span>

<span data-ttu-id="389d5-142">Pour le son MPEG-2, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="389d5-142">For MPEG-2 audio, the media types are as follows.</span></span>



|                  |                               |                                |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="389d5-143">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="389d5-143">PES output</span></span>                    | <span data-ttu-id="389d5-144">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="389d5-144">Payload output</span></span>                 |
| <span data-ttu-id="389d5-145">Type principal</span><span class="sxs-lookup"><span data-stu-id="389d5-145">Major Type</span></span>       | <span data-ttu-id="389d5-146">**\_PES MPEG2 de MediaType \_**</span><span class="sxs-lookup"><span data-stu-id="389d5-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="389d5-147">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="389d5-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="389d5-148">Subtype</span><span class="sxs-lookup"><span data-stu-id="389d5-148">Subtype</span></span>          | <span data-ttu-id="389d5-149">**MEDIASUBTYE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="389d5-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="389d5-150">**MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="389d5-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="389d5-151">Type de format</span><span class="sxs-lookup"><span data-stu-id="389d5-151">Format Type</span></span>      | <span data-ttu-id="389d5-152">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="389d5-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="389d5-153">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="389d5-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="389d5-154">Structure de format</span><span class="sxs-lookup"><span data-stu-id="389d5-154">Format Structure</span></span> | <span data-ttu-id="389d5-155">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="389d5-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="389d5-156">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="389d5-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="389d5-157">Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour le format audio MPEG-2 est actuellement **\_ \_ inconnu**, mais cela peut changer.</span><span class="sxs-lookup"><span data-stu-id="389d5-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="389d5-158">Le séparateur MPEG-2 suppose que les flux D0 à DF sont utilisés pour le flux d’extension multicanaux, comme c’est le cas pour le DVD MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="389d5-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="389d5-159">Par conséquent, chaque fois que Stream C *x* est sélectionné, le séparateur transfère également les paquets pour le flux D *x* .</span><span class="sxs-lookup"><span data-stu-id="389d5-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="389d5-160">LPCM audio</span><span class="sxs-lookup"><span data-stu-id="389d5-160">LPCM Audio</span></span>

<span data-ttu-id="389d5-161">Pour les LPCM audio, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="389d5-161">For LPCM audio, the media types are as follows.</span></span>



|                  |                                    |                                    |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="389d5-162">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="389d5-162">PES output</span></span>                         | <span data-ttu-id="389d5-163">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="389d5-163">Payload output</span></span>                     |
| <span data-ttu-id="389d5-164">Type principal</span><span class="sxs-lookup"><span data-stu-id="389d5-164">Major Type</span></span>       | <span data-ttu-id="389d5-165">**\_PES MPEG2 de MediaType \_**</span><span class="sxs-lookup"><span data-stu-id="389d5-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="389d5-166">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="389d5-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="389d5-167">Subtype</span><span class="sxs-lookup"><span data-stu-id="389d5-167">Subtype</span></span>          | <span data-ttu-id="389d5-168">**MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="389d5-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="389d5-169">**MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="389d5-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="389d5-170">Type de format</span><span class="sxs-lookup"><span data-stu-id="389d5-170">Format Type</span></span>      | <span data-ttu-id="389d5-171">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="389d5-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="389d5-172">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="389d5-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="389d5-173">Structure de format</span><span class="sxs-lookup"><span data-stu-id="389d5-173">Format Structure</span></span> | <span data-ttu-id="389d5-174">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="389d5-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="389d5-175">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="389d5-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="389d5-176">Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour l’audio LPCM est actuellement **\_ \_ inconnu**, mais cela peut changer.</span><span class="sxs-lookup"><span data-stu-id="389d5-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="389d5-177">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="389d5-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="389d5-178">Types de média MPEG-2</span><span class="sxs-lookup"><span data-stu-id="389d5-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
