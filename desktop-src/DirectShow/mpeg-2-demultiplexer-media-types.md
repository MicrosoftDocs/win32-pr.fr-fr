---
description: Types de média du démultiplexeur MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Types de média du démultiplexeur MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21eecff138b987c791ecd97056fb4cf417dd98d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106542097"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="8eb6b-103">Types de média du démultiplexeur MPEG-2</span><span class="sxs-lookup"><span data-stu-id="8eb6b-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="8eb6b-104">Le filtre de [démultiplexage MPEG-2](mpeg-2-demultiplexer.md) reconnaît les types de média suivants.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="8eb6b-105">Types d’entrée</span><span class="sxs-lookup"><span data-stu-id="8eb6b-105">Input Types</span></span>

<span data-ttu-id="8eb6b-106">Le type principal est toujours **un \_ flux de MediaType**.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="8eb6b-107">Le sous-type peut être l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="8eb6b-108">GUID</span><span class="sxs-lookup"><span data-stu-id="8eb6b-108">GUID</span></span>                                             | <span data-ttu-id="8eb6b-109">Description</span><span class="sxs-lookup"><span data-stu-id="8eb6b-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb6b-110">**\_Sous-type \_ KSDATAFORMAT \_ transport MPEG2 BDA \_**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="8eb6b-111">Flux de transport à partir d’un filtre d’appareil d’architecture de pilote de diffusion (BDA).</span><span class="sxs-lookup"><span data-stu-id="8eb6b-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="8eb6b-112">Le démultiplexeur MPEG-2 traite ce sous-type de la même façon que le **\_ \_ transport MEDIASUBTYPE MPEG2**.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="8eb6b-113">**\_Programme MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="8eb6b-114">Flux de programme</span><span class="sxs-lookup"><span data-stu-id="8eb6b-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="8eb6b-115">**\_Transport MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="8eb6b-116">Flux de transport (TS), avec paquets de 188 octets</span><span class="sxs-lookup"><span data-stu-id="8eb6b-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="8eb6b-117">**\_Stride de \_ transport MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="8eb6b-118">Flux de transport avec des paquets « strided ».</span><span class="sxs-lookup"><span data-stu-id="8eb6b-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="8eb6b-119">Ce sous-type indique que les paquets TS peuvent être remplis avec des octets supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="8eb6b-120">Pour plus d’informations, [**consultez \_ \_ Stride transport Stride**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6b-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="8eb6b-121">Pour les paquets de transport strided (**MEDIASUBTYPE \_ MPEG2 \_ transport \_ Stride**), chaque échantillon de support doit contenir un nombre entier de paquets de transport, comme décrit dans [**MPEG2 \_ transport \_ Stride**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6b-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="8eb6b-122">Pour tous les autres types d’entrée, il n’existe aucune restriction sur les limites de l’échantillon. les paquets individuels peuvent s’étendre sur des limites d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="8eb6b-123">Types de sortie</span><span class="sxs-lookup"><span data-stu-id="8eb6b-123">Output Types</span></span>

<span data-ttu-id="8eb6b-124">Le démultiplexeur MPEG-2 ne valide pas les types de sortie ; le filtre en aval est chargé d’analyser les données qu’il reçoit du démultiplexeur.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="8eb6b-125">Toutefois, les types suivants sont généralement acceptés par les filtres en aval comme sortie du démultiplexeur.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="8eb6b-126">Sections MPEG-2</span><span class="sxs-lookup"><span data-stu-id="8eb6b-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8eb6b-127">Type principal</span><span class="sxs-lookup"><span data-stu-id="8eb6b-127">Major Type</span></span></td>
<td><span data-ttu-id="8eb6b-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="8eb6b-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8eb6b-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="8eb6b-129">Subtype</span></span></td>
<td><span data-ttu-id="8eb6b-130">Un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8eb6b-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="8eb6b-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: informations sur le service ATSC.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="8eb6b-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: informations sur le service DVB.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="8eb6b-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: informations sur le service de diffusion numérique de services intégrés (ISDB).</span><span class="sxs-lookup"><span data-stu-id="8eb6b-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="8eb6b-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: données de la section MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="8eb6b-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8eb6b-135">Type de format</span><span class="sxs-lookup"><span data-stu-id="8eb6b-135">Format Type</span></span></td>
<td><span data-ttu-id="8eb6b-136">Aucun</span><span class="sxs-lookup"><span data-stu-id="8eb6b-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="8eb6b-137">Vidéo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="8eb6b-137">MPEG-2 Video</span></span>



|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="8eb6b-138">Type principal</span><span class="sxs-lookup"><span data-stu-id="8eb6b-138">Major type</span></span>       | <span data-ttu-id="8eb6b-139">**Vidéo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-139">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="8eb6b-140">Subtype</span><span class="sxs-lookup"><span data-stu-id="8eb6b-140">Subtype</span></span>          | <span data-ttu-id="8eb6b-141">**\_Vidéo MEDIASUBTYPE MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-141">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="8eb6b-142">Type de format</span><span class="sxs-lookup"><span data-stu-id="8eb6b-142">Format Type</span></span>      | <span data-ttu-id="8eb6b-143">**FORMAT \_ mpeg2video**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-143">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="8eb6b-144">Structure de format</span><span class="sxs-lookup"><span data-stu-id="8eb6b-144">Format Structure</span></span> | [<span data-ttu-id="8eb6b-145">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-145">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="8eb6b-146">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="8eb6b-146">MPEG-2 Audio</span></span>



|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="8eb6b-147">Type principal</span><span class="sxs-lookup"><span data-stu-id="8eb6b-147">Major type</span></span>       | <span data-ttu-id="8eb6b-148">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-148">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="8eb6b-149">Subtype</span><span class="sxs-lookup"><span data-stu-id="8eb6b-149">Subtype</span></span>          | <span data-ttu-id="8eb6b-150">**MEDIASUBTYPE \_ MPEG2 \_ audio**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="8eb6b-151">Type de format</span><span class="sxs-lookup"><span data-stu-id="8eb6b-151">Format Type</span></span>      | <span data-ttu-id="8eb6b-152">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="8eb6b-152">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="8eb6b-153">Structure de format</span><span class="sxs-lookup"><span data-stu-id="8eb6b-153">Format Structure</span></span> | <span data-ttu-id="8eb6b-154">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8eb6b-154">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8eb6b-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8eb6b-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eb6b-156">Types de média MPEG-2</span><span class="sxs-lookup"><span data-stu-id="8eb6b-156">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
