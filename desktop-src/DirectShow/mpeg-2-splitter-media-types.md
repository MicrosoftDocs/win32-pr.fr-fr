---
description: Types de média MPEG-2 Splitter
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Types de média MPEG-2 Splitter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e025fafabdeb8c437cc1d1cd6fbb843cf63e3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119974"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="f6381-103">Types de média MPEG-2 Splitter</span><span class="sxs-lookup"><span data-stu-id="f6381-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="f6381-104">Le filtre de [séparateur MPEG-2](mpeg-2-splitter.md) prend actuellement en charge l’audio et la vidéo.</span><span class="sxs-lookup"><span data-stu-id="f6381-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="f6381-105">Dolby AC-3 est pris en charge en tant que sous-flux, comme défini par DVD.</span><span class="sxs-lookup"><span data-stu-id="f6381-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="f6381-106">Le filtre prend également en charge le format audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="f6381-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="f6381-107">Les types de médias varient selon que le séparateur MPEG-2 fournit des paquets PES ou des charges utiles PES.</span><span class="sxs-lookup"><span data-stu-id="f6381-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="f6381-108">Vidéo</span><span class="sxs-lookup"><span data-stu-id="f6381-108">Video</span></span>

<span data-ttu-id="f6381-109">Pour les vidéos MPEG-2, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="f6381-109">For MPEG-2 video, the media types are as follows.</span></span>


|                | <span data-ttu-id="f6381-110">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="f6381-110">PES output</span></span> | <span data-ttu-id="f6381-111">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="f6381-111">Payload output</span></span>
|------------------|------------------------------------------|--------------------------------|
| <span data-ttu-id="f6381-112">**Type principal**</span><span class="sxs-lookup"><span data-stu-id="f6381-112">**Major type**</span></span>       | <span data-ttu-id="f6381-113">**\_PES MPEG2 de MediaType \_**</span><span class="sxs-lookup"><span data-stu-id="f6381-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="f6381-114">**Vidéo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="f6381-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="f6381-115">**Sous-type**</span><span class="sxs-lookup"><span data-stu-id="f6381-115">**Subtype**</span></span>          | <span data-ttu-id="f6381-116">**\_Vidéo MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="f6381-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="f6381-117">**\_Vidéo MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="f6381-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="f6381-118">**Type de format**</span><span class="sxs-lookup"><span data-stu-id="f6381-118">**Format type**</span></span>      | <span data-ttu-id="f6381-119">**FORMAT \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="f6381-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="f6381-120">**FORMAT \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="f6381-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="f6381-121">**Structure de format**</span><span class="sxs-lookup"><span data-stu-id="f6381-121">**Format structure**</span></span> | [<span data-ttu-id="f6381-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="f6381-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="f6381-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="f6381-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="f6381-124">Audio AC-3</span><span class="sxs-lookup"><span data-stu-id="f6381-124">AC-3 Audio</span></span>

<span data-ttu-id="f6381-125">Pour le son AC-3, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="f6381-125">For AC-3 audio, the media types are as follows.</span></span>

| | <span data-ttu-id="f6381-126">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="f6381-126">PES output</span></span> | <span data-ttu-id="f6381-127">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="f6381-127">Payload output</span></span> |
|------------------|--------------------------------------|------------------------------|
| <span data-ttu-id="f6381-128">**Type principal**</span><span class="sxs-lookup"><span data-stu-id="f6381-128">**Major type**</span></span>       | <span data-ttu-id="f6381-129">**\_PES MPEG2 de MediaType \_**</span><span class="sxs-lookup"><span data-stu-id="f6381-129">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="f6381-130">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="f6381-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="f6381-131">**Sous-type**</span><span class="sxs-lookup"><span data-stu-id="f6381-131">**Subtype**</span></span>          | <span data-ttu-id="f6381-132">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="f6381-132">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>             | <span data-ttu-id="f6381-133">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="f6381-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="f6381-134">**Type de format**</span><span class="sxs-lookup"><span data-stu-id="f6381-134">**Format type**</span></span>      | <span data-ttu-id="f6381-135">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="f6381-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="f6381-136">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="f6381-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="f6381-137">**Structure de format**</span><span class="sxs-lookup"><span data-stu-id="f6381-137">**Format structure**</span></span> | <span data-ttu-id="f6381-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6381-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="f6381-139">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="f6381-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="f6381-140">Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour AC-3 est **actuellement \_ \_ inconnu**, mais cela peut changer.</span><span class="sxs-lookup"><span data-stu-id="f6381-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="f6381-141">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f6381-141">MPEG-2 Audio</span></span>

<span data-ttu-id="f6381-142">Pour le son MPEG-2, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="f6381-142">For MPEG-2 audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="f6381-143">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="f6381-143">PES output</span></span> | <span data-ttu-id="f6381-144">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="f6381-144">Payload output</span></span> |
|------------------|-------------------------------|--------------------------------|
| <span data-ttu-id="f6381-145">**Type principal**</span><span class="sxs-lookup"><span data-stu-id="f6381-145">**Major type**</span></span>       | <span data-ttu-id="f6381-146">**\_PES MPEG2 de MediaType \_**</span><span class="sxs-lookup"><span data-stu-id="f6381-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="f6381-147">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="f6381-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="f6381-148">**Sous-type**</span><span class="sxs-lookup"><span data-stu-id="f6381-148">**Subtype**</span></span>          | <span data-ttu-id="f6381-149">**MEDIASUBTYE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="f6381-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="f6381-150">**MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="f6381-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="f6381-151">**Type de format**</span><span class="sxs-lookup"><span data-stu-id="f6381-151">**Format type**</span></span>      | <span data-ttu-id="f6381-152">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="f6381-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="f6381-153">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="f6381-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="f6381-154">**Structure de format**</span><span class="sxs-lookup"><span data-stu-id="f6381-154">**Format structure**</span></span> | <span data-ttu-id="f6381-155">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="f6381-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="f6381-156">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="f6381-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="f6381-157">Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour le format audio MPEG-2 est actuellement **\_ \_ inconnu**, mais cela peut changer.</span><span class="sxs-lookup"><span data-stu-id="f6381-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="f6381-158">Le séparateur MPEG-2 suppose que les flux D0 à DF sont utilisés pour le flux d’extension multicanaux, comme c’est le cas pour le DVD MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="f6381-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="f6381-159">Par conséquent, chaque fois que Stream C *x* est sélectionné, le séparateur transfère également les paquets pour le flux D *x* .</span><span class="sxs-lookup"><span data-stu-id="f6381-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="f6381-160">LPCM audio</span><span class="sxs-lookup"><span data-stu-id="f6381-160">LPCM Audio</span></span>

<span data-ttu-id="f6381-161">Pour les LPCM audio, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="f6381-161">For LPCM audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="f6381-162">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="f6381-162">PES output</span></span> | <span data-ttu-id="f6381-163">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="f6381-163">Payload output</span></span> |
|------------------|------------------------------------|------------------------------------|
| <span data-ttu-id="f6381-164">**Type principal**</span><span class="sxs-lookup"><span data-stu-id="f6381-164">**Major type**</span></span>       | <span data-ttu-id="f6381-165">**\_PES MPEG2 de MediaType \_**</span><span class="sxs-lookup"><span data-stu-id="f6381-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="f6381-166">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="f6381-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="f6381-167">**Sous-type**</span><span class="sxs-lookup"><span data-stu-id="f6381-167">**Subtype**</span></span>          | <span data-ttu-id="f6381-168">**MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="f6381-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="f6381-169">**MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="f6381-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="f6381-170">**Type de format**</span><span class="sxs-lookup"><span data-stu-id="f6381-170">**Format type**</span></span>      | <span data-ttu-id="f6381-171">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="f6381-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="f6381-172">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="f6381-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="f6381-173">**Structure de format**</span><span class="sxs-lookup"><span data-stu-id="f6381-173">**Format structure**</span></span> | <span data-ttu-id="f6381-174">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="f6381-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="f6381-175">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="f6381-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="f6381-176">Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour l’audio LPCM est actuellement **\_ \_ inconnu**, mais cela peut changer.</span><span class="sxs-lookup"><span data-stu-id="f6381-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6381-177">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6381-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6381-178">Types de média MPEG-2</span><span class="sxs-lookup"><span data-stu-id="f6381-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
