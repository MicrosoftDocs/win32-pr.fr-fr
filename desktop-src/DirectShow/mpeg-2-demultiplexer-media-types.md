---
description: Types de média du démultiplexeur MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Types de média du démultiplexeur MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9b5276b975771ba62118976c8e63b4d5faa53d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909997"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="5cbd0-103">Types de média du démultiplexeur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="5cbd0-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="5cbd0-104">Le filtre de [démultiplexage MPEG-2](mpeg-2-demultiplexer.md) reconnaît les types de média suivants.</span><span class="sxs-lookup"><span data-stu-id="5cbd0-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="5cbd0-105">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="5cbd0-105">Input Types</span></span>

<span data-ttu-id="5cbd0-106">Le type principal est toujours **un \_ flux de MediaType**.</span><span class="sxs-lookup"><span data-stu-id="5cbd0-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="5cbd0-107">Le sous-type peut être l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="5cbd0-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="5cbd0-108">GUID</span><span class="sxs-lookup"><span data-stu-id="5cbd0-108">GUID</span></span>                                             | <span data-ttu-id="5cbd0-109">Description</span><span class="sxs-lookup"><span data-stu-id="5cbd0-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cbd0-110">**\_Sous-type \_ KSDATAFORMAT \_ transport MPEG2 BDA \_**</span><span class="sxs-lookup"><span data-stu-id="5cbd0-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="5cbd0-111">Flux de transport à partir d’un filtre d’appareil d’architecture de pilote de diffusion (BDA).</span><span class="sxs-lookup"><span data-stu-id="5cbd0-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="5cbd0-112">Le démultiplexeur MPEG-2 traite ce sous-type de la même façon que le **\_ \_ transport MEDIASUBTYPE MPEG2**.</span><span class="sxs-lookup"><span data-stu-id="5cbd0-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="5cbd0-113">**\_Programme MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="5cbd0-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="5cbd0-114">Flux de programme</span><span class="sxs-lookup"><span data-stu-id="5cbd0-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="5cbd0-115">**\_Transport MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="5cbd0-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="5cbd0-116">Flux de transport (TS), avec paquets de 188 octets</span><span class="sxs-lookup"><span data-stu-id="5cbd0-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="5cbd0-117">**\_Stride de \_ transport MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="5cbd0-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="5cbd0-118">Flux de transport avec des paquets « strided ».</span><span class="sxs-lookup"><span data-stu-id="5cbd0-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="5cbd0-119">Ce sous-type indique que les paquets TS peuvent être remplis avec des octets supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5cbd0-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="5cbd0-120">Pour plus d’informations, [**consultez \_ \_ Stride transport Stride**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="5cbd0-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="5cbd0-121">Pour les paquets de transport strided (**MEDIASUBTYPE \_ MPEG2 \_ transport \_ Stride**), chaque échantillon de support doit contenir un nombre entier de paquets de transport, comme décrit dans [**MPEG2 \_ transport \_ Stride**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="5cbd0-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="5cbd0-122">Pour tous les autres types d’entrée, il n’existe aucune restriction sur les limites de l’échantillon. les paquets individuels peuvent s’étendre sur des limites d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="5cbd0-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="5cbd0-123">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="5cbd0-123">Output Types</span></span>

<span data-ttu-id="5cbd0-124">Le démultiplexeur MPEG-2 ne valide pas les types de sortie ; le filtre en aval est chargé d’analyser les données qu’il reçoit du démultiplexeur.</span><span class="sxs-lookup"><span data-stu-id="5cbd0-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="5cbd0-125">Toutefois, les types suivants sont généralement acceptés par les filtres en aval comme sortie du démultiplexeur.</span><span class="sxs-lookup"><span data-stu-id="5cbd0-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="5cbd0-126">Sections MPEG-2</span><span class="sxs-lookup"><span data-stu-id="5cbd0-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5cbd0-127">Type principal</span><span class="sxs-lookup"><span data-stu-id="5cbd0-127">Major Type</span></span></td>
<td><span data-ttu-id="5cbd0-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="5cbd0-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cbd0-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="5cbd0-129">Subtype</span></span></td>
<td><span data-ttu-id="5cbd0-130">Un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5cbd0-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="5cbd0-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: informations sur le service ATSC.</span><span class="sxs-lookup"><span data-stu-id="5cbd0-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="5cbd0-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: informations sur le service DVB.</span><span class="sxs-lookup"><span data-stu-id="5cbd0-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="5cbd0-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: informations sur le service de diffusion numérique de services intégrés (ISDB).</span><span class="sxs-lookup"><span data-stu-id="5cbd0-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="5cbd0-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: données de la section MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="5cbd0-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5cbd0-135">Type de format</span><span class="sxs-lookup"><span data-stu-id="5cbd0-135">Format Type</span></span></td>
<td><span data-ttu-id="5cbd0-136">Aucun</span><span class="sxs-lookup"><span data-stu-id="5cbd0-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="5cbd0-137">Vidéo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="5cbd0-137">MPEG-2 Video</span></span>



| <span data-ttu-id="5cbd0-138">Étiquette</span><span class="sxs-lookup"><span data-stu-id="5cbd0-138">Label</span></span> | <span data-ttu-id="5cbd0-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cbd0-139">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="5cbd0-140">Type principal</span><span class="sxs-lookup"><span data-stu-id="5cbd0-140">Major type</span></span>       | <span data-ttu-id="5cbd0-141">**Vidéo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="5cbd0-141">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="5cbd0-142">Subtype</span><span class="sxs-lookup"><span data-stu-id="5cbd0-142">Subtype</span></span>          | <span data-ttu-id="5cbd0-143">**\_Vidéo MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="5cbd0-143">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="5cbd0-144">Type de format</span><span class="sxs-lookup"><span data-stu-id="5cbd0-144">Format Type</span></span>      | <span data-ttu-id="5cbd0-145">**FORMAT \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="5cbd0-145">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="5cbd0-146">Structure de format</span><span class="sxs-lookup"><span data-stu-id="5cbd0-146">Format Structure</span></span> | [<span data-ttu-id="5cbd0-147">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="5cbd0-147">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="5cbd0-148">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="5cbd0-148">MPEG-2 Audio</span></span>



| <span data-ttu-id="5cbd0-149">Étiquette</span><span class="sxs-lookup"><span data-stu-id="5cbd0-149">Label</span></span> | <span data-ttu-id="5cbd0-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cbd0-150">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="5cbd0-151">Type principal</span><span class="sxs-lookup"><span data-stu-id="5cbd0-151">Major type</span></span>       | <span data-ttu-id="5cbd0-152">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="5cbd0-152">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="5cbd0-153">Subtype</span><span class="sxs-lookup"><span data-stu-id="5cbd0-153">Subtype</span></span>          | <span data-ttu-id="5cbd0-154">**MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="5cbd0-154">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="5cbd0-155">Type de format</span><span class="sxs-lookup"><span data-stu-id="5cbd0-155">Format Type</span></span>      | <span data-ttu-id="5cbd0-156">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="5cbd0-156">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="5cbd0-157">Structure de format</span><span class="sxs-lookup"><span data-stu-id="5cbd0-157">Format Structure</span></span> | <span data-ttu-id="5cbd0-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5cbd0-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5cbd0-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5cbd0-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cbd0-160">Types de média MPEG-2</span><span class="sxs-lookup"><span data-stu-id="5cbd0-160">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
