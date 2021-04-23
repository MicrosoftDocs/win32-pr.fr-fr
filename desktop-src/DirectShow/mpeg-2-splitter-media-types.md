---
description: Types de média MPEG-2 Splitter
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Types de média MPEG-2 Splitter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e878acaea8bc87bee2bf5c46a6f7e66c7aa0a485
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909426"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="5f927-103">Types de média MPEG-2 Splitter</span><span class="sxs-lookup"><span data-stu-id="5f927-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="5f927-104">Le filtre de [séparateur MPEG-2](mpeg-2-splitter.md) prend actuellement en charge l’audio et la vidéo.</span><span class="sxs-lookup"><span data-stu-id="5f927-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="5f927-105">Dolby AC-3 est pris en charge en tant que sous-flux, comme défini par DVD.</span><span class="sxs-lookup"><span data-stu-id="5f927-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="5f927-106">Le filtre prend également en charge le format audio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="5f927-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="5f927-107">Les types de médias varient selon que le séparateur MPEG-2 fournit des paquets PES ou des charges utiles PES.</span><span class="sxs-lookup"><span data-stu-id="5f927-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="5f927-108">Vidéo</span><span class="sxs-lookup"><span data-stu-id="5f927-108">Video</span></span>

<span data-ttu-id="5f927-109">Pour les vidéos MPEG-2, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="5f927-109">For MPEG-2 video, the media types are as follows.</span></span>



| <span data-ttu-id="5f927-110">Étiquette</span><span class="sxs-lookup"><span data-stu-id="5f927-110">Label</span></span> | <span data-ttu-id="5f927-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f927-111">Value</span></span> |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="5f927-112">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="5f927-112">PES output</span></span>                               | <span data-ttu-id="5f927-113">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="5f927-113">Payload output</span></span>                 |
| <span data-ttu-id="5f927-114">Type principal</span><span class="sxs-lookup"><span data-stu-id="5f927-114">Major Type</span></span>       | <span data-ttu-id="5f927-115">**\_PES MPEG2 de MediaType \_**</span><span class="sxs-lookup"><span data-stu-id="5f927-115">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="5f927-116">**Vidéo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="5f927-116">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="5f927-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="5f927-117">Subtype</span></span>          | <span data-ttu-id="5f927-118">**\_Vidéo MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="5f927-118">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="5f927-119">**\_Vidéo MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="5f927-119">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="5f927-120">Type de format</span><span class="sxs-lookup"><span data-stu-id="5f927-120">Format Type</span></span>      | <span data-ttu-id="5f927-121">**FORMAT \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="5f927-121">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="5f927-122">**FORMAT \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="5f927-122">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="5f927-123">Structure de format</span><span class="sxs-lookup"><span data-stu-id="5f927-123">Format Structure</span></span> | [<span data-ttu-id="5f927-124">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="5f927-124">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="5f927-125">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="5f927-125">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="5f927-126">Audio AC-3</span><span class="sxs-lookup"><span data-stu-id="5f927-126">AC-3 Audio</span></span>

<span data-ttu-id="5f927-127">Pour le son AC-3, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="5f927-127">For AC-3 audio, the media types are as follows.</span></span>



| <span data-ttu-id="5f927-128">Étiquette</span><span class="sxs-lookup"><span data-stu-id="5f927-128">Label</span></span> | <span data-ttu-id="5f927-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f927-129">Value</span></span> |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="5f927-130">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="5f927-130">PES output</span></span>                           | <span data-ttu-id="5f927-131">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="5f927-131">Payload output</span></span>               |
| <span data-ttu-id="5f927-132">Type principal</span><span class="sxs-lookup"><span data-stu-id="5f927-132">Major Type</span></span>       | <span data-ttu-id="5f927-133">\_PES MPEG2 de MediaType \_</span><span class="sxs-lookup"><span data-stu-id="5f927-133">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="5f927-134">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="5f927-134">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="5f927-135">Subtype</span><span class="sxs-lookup"><span data-stu-id="5f927-135">Subtype</span></span>          | <span data-ttu-id="5f927-136">MEDIASUBTYPE \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="5f927-136">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="5f927-137">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="5f927-137">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="5f927-138">Type de format</span><span class="sxs-lookup"><span data-stu-id="5f927-138">Format Type</span></span>      | <span data-ttu-id="5f927-139">FORMAT \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="5f927-139">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="5f927-140">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5f927-140">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="5f927-141">Structure de format</span><span class="sxs-lookup"><span data-stu-id="5f927-141">Format Structure</span></span> | <span data-ttu-id="5f927-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5f927-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="5f927-143">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="5f927-143">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="5f927-144">Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour AC-3 est **actuellement \_ \_ inconnu**, mais cela peut changer.</span><span class="sxs-lookup"><span data-stu-id="5f927-144">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="5f927-145">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="5f927-145">MPEG-2 Audio</span></span>

<span data-ttu-id="5f927-146">Pour le son MPEG-2, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="5f927-146">For MPEG-2 audio, the media types are as follows.</span></span>



| <span data-ttu-id="5f927-147">Étiquette</span><span class="sxs-lookup"><span data-stu-id="5f927-147">Label</span></span> | <span data-ttu-id="5f927-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f927-148">Value</span></span> |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="5f927-149">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="5f927-149">PES output</span></span>                    | <span data-ttu-id="5f927-150">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="5f927-150">Payload output</span></span>                 |
| <span data-ttu-id="5f927-151">Type principal</span><span class="sxs-lookup"><span data-stu-id="5f927-151">Major Type</span></span>       | <span data-ttu-id="5f927-152">**\_PES MPEG2 de MediaType \_**</span><span class="sxs-lookup"><span data-stu-id="5f927-152">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="5f927-153">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="5f927-153">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="5f927-154">Subtype</span><span class="sxs-lookup"><span data-stu-id="5f927-154">Subtype</span></span>          | <span data-ttu-id="5f927-155">**MEDIASUBTYE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="5f927-155">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="5f927-156">**MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="5f927-156">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="5f927-157">Type de format</span><span class="sxs-lookup"><span data-stu-id="5f927-157">Format Type</span></span>      | <span data-ttu-id="5f927-158">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5f927-158">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="5f927-159">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5f927-159">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="5f927-160">Structure de format</span><span class="sxs-lookup"><span data-stu-id="5f927-160">Format Structure</span></span> | <span data-ttu-id="5f927-161">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="5f927-161">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="5f927-162">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="5f927-162">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="5f927-163">Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour le format audio MPEG-2 est actuellement **\_ \_ inconnu**, mais cela peut changer.</span><span class="sxs-lookup"><span data-stu-id="5f927-163">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="5f927-164">Le séparateur MPEG-2 suppose que les flux D0 à DF sont utilisés pour le flux d’extension multicanaux, comme c’est le cas pour le DVD MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="5f927-164">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="5f927-165">Par conséquent, chaque fois que Stream C *x* est sélectionné, le séparateur transfère également les paquets pour le flux D *x* .</span><span class="sxs-lookup"><span data-stu-id="5f927-165">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="5f927-166">LPCM audio</span><span class="sxs-lookup"><span data-stu-id="5f927-166">LPCM Audio</span></span>

<span data-ttu-id="5f927-167">Pour les LPCM audio, les types de médias sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="5f927-167">For LPCM audio, the media types are as follows.</span></span>



| <span data-ttu-id="5f927-168">Étiquette</span><span class="sxs-lookup"><span data-stu-id="5f927-168">Label</span></span> | <span data-ttu-id="5f927-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f927-169">Value</span></span> |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="5f927-170">Sortie PES</span><span class="sxs-lookup"><span data-stu-id="5f927-170">PES output</span></span>                         | <span data-ttu-id="5f927-171">Sortie de la charge utile</span><span class="sxs-lookup"><span data-stu-id="5f927-171">Payload output</span></span>                     |
| <span data-ttu-id="5f927-172">Type principal</span><span class="sxs-lookup"><span data-stu-id="5f927-172">Major Type</span></span>       | <span data-ttu-id="5f927-173">**\_PES MPEG2 de MediaType \_**</span><span class="sxs-lookup"><span data-stu-id="5f927-173">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="5f927-174">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="5f927-174">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="5f927-175">Subtype</span><span class="sxs-lookup"><span data-stu-id="5f927-175">Subtype</span></span>          | <span data-ttu-id="5f927-176">**MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="5f927-176">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="5f927-177">**MEDIASUBTYPE \_ DVD \_ LPCM \_ audio**</span><span class="sxs-lookup"><span data-stu-id="5f927-177">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="5f927-178">Type de format</span><span class="sxs-lookup"><span data-stu-id="5f927-178">Format Type</span></span>      | <span data-ttu-id="5f927-179">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5f927-179">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="5f927-180">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5f927-180">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="5f927-181">Structure de format</span><span class="sxs-lookup"><span data-stu-id="5f927-181">Format Structure</span></span> | <span data-ttu-id="5f927-182">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="5f927-182">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="5f927-183">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="5f927-183">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="5f927-184">Le membre **wFormatTag** de la structure **WAVEFORMATEX** pour l’audio LPCM est actuellement **\_ \_ inconnu**, mais cela peut changer.</span><span class="sxs-lookup"><span data-stu-id="5f927-184">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f927-185">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f927-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f927-186">Types de média MPEG-2</span><span class="sxs-lookup"><span data-stu-id="5f927-186">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
