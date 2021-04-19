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
# <a name="perfinfo_dshow_streamtrace-structure"></a>PERFINFO \_ DShow \_ STREAMTRACE, structure

La `PERFINFO_DSHOW_STREAMTRACE` structure contient des données pour un événement de trace DirectShow de type GUID \_ STREAMTRACE.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a>Membres

<dl> <dt>

**id**
</dt> <dd>

Identificateur d’événement. Consultez la section Notes.

</dd> <dt>

**réservé**
</dt> <dd>

Réservé. Définit la valeur zéro.

</dd> <dt>

**dshowClock**
</dt> <dd>

Temps de flux pour cet événement, en unités de 100 nanosecondes. Cette valeur est facultative et peut être égale à zéro.

</dd> <dt>

**data**
</dt> <dd>

Données d’événement facultatives composées de quatre valeurs **ULONGLONG** . La signification de ces données dépend de l’identificateur d’événement.

</dd> </dl>

## <a name="remarks"></a>Notes

Les identificateurs d’événements suivants sont définis.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificateur d’événement</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</td>
<td>Consigné lorsque le filtre de <a href="mpeg-2-demultiplexer.md">démultiplexage MPEG-2</a> convertit un horodatage de présentation en temps de flux.
<ul>
<li><strong>métadonnée</strong>[0]: Converted start time.</li>
<li><strong>métadonnée</strong>[1]: Converted stop time.</li>
<li><strong>données</strong>[2]. Identificateur de flux pour la broche d’entrée.</li>
<li><strong>métadonnée</strong>[3]: PTS that was converted.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</td>
<td>Journalisé lorsque le démultiplexeur MPEG-2 reçoit un échantillon.
<ul>
<li><strong>données</strong> [0]: Current time returned by  <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</td>
<td>Consigné quand VMR planifie un exemple de rendu, juste avant que VMR appelle <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock :: AdviseTime</strong></a>.
<ul>
<li><strong>métadonnée</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</td>
<td>Consigné quand VMR commence une opération de décodage, c’est-à-dire lorsque le décodeur appelle <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator :: BeginFrame</strong></a>. Aucune donnée d'événement.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</td>
<td>Consigné quand VMR commence une opération de composition de désentrelacement ou de vidéo. Aucune donnée d'événement.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</td>
<td>Consigné quand VMR supprime une frame ; par exemple, si un exemple est en retard.
<ul>
<li><strong>métadonnée</strong>[0]: Sample start time.</li>
<li><strong>métadonnée</strong>[1]: Sample end time.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_ADVISE</td>
<td>Consigné quand VMR reçoit une notification d’avis de l’horloge de référence. Aucune donnée d'événement.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_END_DECODE</td>
<td>Consigné quand VMR met fin à une opération de décodage, c’est-à-dire lorsque le décodeur appelle <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator :: EndFrame</strong></a>. Aucune donnée d'événement.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</td>
<td>Consigné quand VMR termine une opération de composition de désentrelacement ou de vidéo. Aucune donnée d'événement.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_RECEIVE</td>
<td>Consigné quand VMR reçoit un nouvel exemple. Aucune donnée d'événement.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_RENDER_TIME</td>
<td>Consigné quand VMR termine le rendu d’une trame.
<ul>
<li><strong>métadonnée</strong>[0]: Time that it took to render this frame.</li>
<li><strong>métadonnée</strong>[1]: Running average of frame rendering times.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Pour enregistrer cet événement à partir d’un filtre DirectShow, utilisez la fonction **PERFLOG \_ STREAMTRACE** , qui est définie dans le fichier d’en-tête Dxmperf. h. Cet en-tête est inclus dans les classes de base DirectShow.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Perfstruct. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures DirectShow](directshow-structures.md)
</dt> <dt>

[Suivi d’événements dans DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUID d’événements de trace](trace-guids.md)
</dt> </dl>

 

 
