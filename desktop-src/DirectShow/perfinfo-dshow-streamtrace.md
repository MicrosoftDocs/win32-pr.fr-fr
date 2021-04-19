---
description: La \_ structure PERFINFO DShow \_ STREAMTRACE contient des données pour un événement de trace DirectShow de type GUID \_ STREAMTRACE.
ms.assetid: 41fbf95c-e86c-4c64-898f-01fbf5f8839c
title: Structure PERFINFO_DSHOW_STREAMTRACE (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_STREAMTRACE
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 2bee4f3c11cf8462c8292cc412a6da5d9f9bfa78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523518"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a><span data-ttu-id="bcef7-103">PERFINFO \_ DShow \_ STREAMTRACE, structure</span><span class="sxs-lookup"><span data-stu-id="bcef7-103">PERFINFO\_DSHOW\_STREAMTRACE structure</span></span>

<span data-ttu-id="bcef7-104">La `PERFINFO_DSHOW_STREAMTRACE` structure contient des données pour un événement de trace DirectShow de type GUID \_ STREAMTRACE.</span><span class="sxs-lookup"><span data-stu-id="bcef7-104">The `PERFINFO_DSHOW_STREAMTRACE` structure contains data for a DirectShow trace event of type GUID\_STREAMTRACE.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcef7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcef7-105">Syntax</span></span>


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a><span data-ttu-id="bcef7-106">Membres</span><span class="sxs-lookup"><span data-stu-id="bcef7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bcef7-107">**id**</span><span class="sxs-lookup"><span data-stu-id="bcef7-107">**id**</span></span>
</dt> <dd>

<span data-ttu-id="bcef7-108">Identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="bcef7-108">Event identifier.</span></span> <span data-ttu-id="bcef7-109">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="bcef7-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="bcef7-110">**réservé**</span><span class="sxs-lookup"><span data-stu-id="bcef7-110">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="bcef7-111">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bcef7-111">Reserved.</span></span> <span data-ttu-id="bcef7-112">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="bcef7-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="bcef7-113">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="bcef7-113">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="bcef7-114">Temps de flux pour cet événement, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="bcef7-114">Stream time for this event, in 100-nanosecond units.</span></span> <span data-ttu-id="bcef7-115">Cette valeur est facultative et peut être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="bcef7-115">This value is optional and can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bcef7-116">**data**</span><span class="sxs-lookup"><span data-stu-id="bcef7-116">**data**</span></span>
</dt> <dd>

<span data-ttu-id="bcef7-117">Données d’événement facultatives composées de quatre valeurs **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="bcef7-117">Optional event data consisting of four **ULONGLONG** values.</span></span> <span data-ttu-id="bcef7-118">La signification de ces données dépend de l’identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="bcef7-118">The meaning of this data depends on the event identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcef7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="bcef7-119">Remarks</span></span>

<span data-ttu-id="bcef7-120">Les identificateurs d’événements suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="bcef7-120">The following event identifiers are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bcef7-121">Identificateur d’événement</span><span class="sxs-lookup"><span data-stu-id="bcef7-121">Event identifier</span></span></th>
<th><span data-ttu-id="bcef7-122">Description</span><span class="sxs-lookup"><span data-stu-id="bcef7-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bcef7-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span><span class="sxs-lookup"><span data-stu-id="bcef7-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span></span></td>
<td><span data-ttu-id="bcef7-124">Consigné lorsque le filtre de <a href="mpeg-2-demultiplexer.md">démultiplexage MPEG-2</a> convertit un horodatage de présentation en temps de flux.</span><span class="sxs-lookup"><span data-stu-id="bcef7-124">Logged when the <a href="mpeg-2-demultiplexer.md">MPEG-2 Demultiplexer</a> filter converts a presentation time stamp (PTS) to stream time.</span></span>
<ul>
<li><span data-ttu-id="bcef7-125"><strong>métadonnée</strong>[0]: Converted start time.</span><span class="sxs-lookup"><span data-stu-id="bcef7-125"><strong>data</strong>[0]: Converted start time.</span></span></li>
<li><span data-ttu-id="bcef7-126"><strong>métadonnée</strong>[1]: Converted stop time.</span><span class="sxs-lookup"><span data-stu-id="bcef7-126"><strong>data</strong>[1]: Converted stop time.</span></span></li>
<li><span data-ttu-id="bcef7-127"><strong>données</strong>[2].</span><span class="sxs-lookup"><span data-stu-id="bcef7-127"><strong>data</strong>[2].</span></span> <span data-ttu-id="bcef7-128">Identificateur de flux pour la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bcef7-128">Stream identifier for the input pin.</span></span></li>
<li><span data-ttu-id="bcef7-129"><strong>métadonnée</strong>[3]: PTS that was converted.</span><span class="sxs-lookup"><span data-stu-id="bcef7-129"><strong>data</strong>[3]: PTS that was converted.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bcef7-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="bcef7-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span></span></td>
<td><span data-ttu-id="bcef7-131">Journalisé lorsque le démultiplexeur MPEG-2 reçoit un échantillon.</span><span class="sxs-lookup"><span data-stu-id="bcef7-131">Logged when MPEG-2 Demultiplexer receives a sample.</span></span>
<ul>
<li><span data-ttu-id="bcef7-132"><strong>données</strong> [0]: Current time returned by  <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bcef7-132"><strong>data</strong>[0]: Current time returned by <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bcef7-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span><span class="sxs-lookup"><span data-stu-id="bcef7-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span></span></td>
<td><span data-ttu-id="bcef7-134">Consigné quand VMR planifie un exemple de rendu, juste avant que VMR appelle <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock :: AdviseTime</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bcef7-134">Logged when the VMR schedules a sample for rendering, immediately before the VMR calls <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock::AdviseTime</strong></a>.</span></span>
<ul>
<li><span data-ttu-id="bcef7-135"><strong>métadonnée</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span><span class="sxs-lookup"><span data-stu-id="bcef7-135"><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bcef7-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span><span class="sxs-lookup"><span data-stu-id="bcef7-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span></span></td>
<td><span data-ttu-id="bcef7-137">Consigné quand VMR commence une opération de décodage, c’est-à-dire lorsque le décodeur appelle <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator :: BeginFrame</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bcef7-137">Logged when the VMR begins a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator::BeginFrame</strong></a>.</span></span> <span data-ttu-id="bcef7-138">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="bcef7-138">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bcef7-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="bcef7-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span></span></td>
<td><span data-ttu-id="bcef7-140">Consigné quand VMR commence une opération de composition de désentrelacement ou de vidéo.</span><span class="sxs-lookup"><span data-stu-id="bcef7-140">Logged when the VMR begins a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="bcef7-141">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="bcef7-141">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bcef7-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span><span class="sxs-lookup"><span data-stu-id="bcef7-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span></span></td>
<td><span data-ttu-id="bcef7-143">Consigné quand VMR supprime une frame ; par exemple, si un exemple est en retard.</span><span class="sxs-lookup"><span data-stu-id="bcef7-143">Logged when the VMR drops a frame; for example, if a sample was late.</span></span>
<ul>
<li><span data-ttu-id="bcef7-144"><strong>métadonnée</strong>[0]: Sample start time.</span><span class="sxs-lookup"><span data-stu-id="bcef7-144"><strong>data</strong>[0]: Sample start time.</span></span></li>
<li><span data-ttu-id="bcef7-145"><strong>métadonnée</strong>[1]: Sample end time.</span><span class="sxs-lookup"><span data-stu-id="bcef7-145"><strong>data</strong>[1]: Sample end time.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bcef7-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span><span class="sxs-lookup"><span data-stu-id="bcef7-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span></span></td>
<td><span data-ttu-id="bcef7-147">Consigné quand VMR reçoit une notification d’avis de l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="bcef7-147">Logged when the VMR receives an advise notification from the reference clock.</span></span> <span data-ttu-id="bcef7-148">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="bcef7-148">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bcef7-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span><span class="sxs-lookup"><span data-stu-id="bcef7-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span></span></td>
<td><span data-ttu-id="bcef7-150">Consigné quand VMR met fin à une opération de décodage, c’est-à-dire lorsque le décodeur appelle <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator :: EndFrame</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bcef7-150">Logged when the VMR ends a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator::EndFrame</strong></a>.</span></span> <span data-ttu-id="bcef7-151">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="bcef7-151">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bcef7-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="bcef7-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span></span></td>
<td><span data-ttu-id="bcef7-153">Consigné quand VMR termine une opération de composition de désentrelacement ou de vidéo.</span><span class="sxs-lookup"><span data-stu-id="bcef7-153">Logged when the VMR completes a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="bcef7-154">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="bcef7-154">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bcef7-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="bcef7-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span></span></td>
<td><span data-ttu-id="bcef7-156">Consigné quand VMR reçoit un nouvel exemple.</span><span class="sxs-lookup"><span data-stu-id="bcef7-156">Logged when the VMR receives a new sample.</span></span> <span data-ttu-id="bcef7-157">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="bcef7-157">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bcef7-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span><span class="sxs-lookup"><span data-stu-id="bcef7-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span></span></td>
<td><span data-ttu-id="bcef7-159">Consigné quand VMR termine le rendu d’une trame.</span><span class="sxs-lookup"><span data-stu-id="bcef7-159">Logged when the VMR finishes rendering a frame.</span></span>
<ul>
<li><span data-ttu-id="bcef7-160"><strong>métadonnée</strong>[0]: Time that it took to render this frame.</span><span class="sxs-lookup"><span data-stu-id="bcef7-160"><strong>data</strong>[0]: Time that it took to render this frame.</span></span></li>
<li><span data-ttu-id="bcef7-161"><strong>métadonnée</strong>[1]: Running average of frame rendering times.</span><span class="sxs-lookup"><span data-stu-id="bcef7-161"><strong>data</strong>[1]: Running average of frame rendering times.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bcef7-162">Pour enregistrer cet événement à partir d’un filtre DirectShow, utilisez la fonction **PERFLOG \_ STREAMTRACE** , qui est définie dans le fichier d’en-tête Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="bcef7-162">To log this event from a DirectShow filter, use the **PERFLOG\_STREAMTRACE** function, which is defined in the header file Dxmperf.h.</span></span> <span data-ttu-id="bcef7-163">Cet en-tête est inclus dans les classes de base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="bcef7-163">This header is included in the DirectShow base classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcef7-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcef7-164">Requirements</span></span>



| <span data-ttu-id="bcef7-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcef7-165">Requirement</span></span> | <span data-ttu-id="bcef7-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcef7-166">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcef7-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="bcef7-167">Header</span></span><br/> | <dl> <span data-ttu-id="bcef7-168"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcef7-168"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcef7-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcef7-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcef7-170">Structures DirectShow</span><span class="sxs-lookup"><span data-stu-id="bcef7-170">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="bcef7-171">Suivi d’événements dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="bcef7-171">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="bcef7-172">GUID d’événements de trace</span><span class="sxs-lookup"><span data-stu-id="bcef7-172">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 
