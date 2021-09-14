---
description: la \_ structure PERFINFO DSHOW \_ STREAMTRACE contient des données pour un événement de trace DirectShow de type GUID \_ STREAMTRACE.
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
ms.openlocfilehash: e17d013d90b133f9c6819b8d9ddf4b5970582cae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007479"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a>PERFINFO \_ DShow \_ STREAMTRACE, structure

la `PERFINFO_DSHOW_STREAMTRACE` structure contient des données pour un événement de trace DirectShow de type GUID \_ STREAMTRACE.

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

**reserved**
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




| Identificateur d’événement | Description | 
|------------------|-------------|
| PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION | Consigné lorsque le filtre de <a href="mpeg-2-demultiplexer.md">démultiplexage MPEG-2</a> convertit un horodatage de présentation en temps de flux.<ul><li><strong>Data</strong>[0] : heure de début convertie.</li><li><strong>Data</strong>[1] : heure d’arrêt convertie.</li><li><strong>données</strong>[2]. Identificateur de flux pour la broche d’entrée.</li><li><strong>Data</strong>[3] : pts qui a été converti.</li></ul> | 
| PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE | Journalisé lorsque le démultiplexeur MPEG-2 reçoit un échantillon.<ul><li><strong>Data</strong>[0] : heure actuelle retournée par <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE | Consigné quand VMR planifie un exemple de rendu, juste avant que VMR appelle <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock :: AdviseTime</strong></a>.<ul><li><strong>Data</strong>[0] : temps de référence au début de la diffusion en continu, ce qui correspond au temps de flux zéro.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE | Consigné quand VMR commence une opération de décodage, c’est-à-dire lorsque le décodeur appelle <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator :: BeginFrame</strong></a>. Aucune donnée d'événement. | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE | Consigné quand VMR commence une opération de composition de désentrelacement ou de vidéo. Aucune donnée d'événement. | 
| PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME | Consigné quand VMR supprime une frame ; par exemple, si un exemple est en retard.<ul><li><strong>Data</strong>[0] : exemple d’heure de début.</li><li><strong>données</strong>[1] : heure de fin de l’exemple.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_END_ADVISE | Consigné quand VMR reçoit une notification d’avis de l’horloge de référence. Aucune donnée d'événement. | 
| PERFINFO_STREAMTRACE_VMR_END_DECODE | Consigné quand VMR met fin à une opération de décodage, c’est-à-dire lorsque le décodeur appelle <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator :: EndFrame</strong></a>. Aucune donnée d'événement. | 
| PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE | Consigné quand VMR termine une opération de composition de désentrelacement ou de vidéo. Aucune donnée d'événement. | 
| PERFINFO_STREAMTRACE_VMR_RECEIVE | Consigné quand VMR reçoit un nouvel exemple. Aucune donnée d'événement. | 
| PERFINFO_STREAMTRACE_VMR_RENDER_TIME | Consigné quand VMR termine le rendu d’une trame.<ul><li><strong>Data</strong>[0] : temps nécessaire au rendu de ce frame.</li><li><strong>Data</strong>[1] : exécution moyenne des heures de rendu de trame.</li></ul> | 




 

pour consigner cet événement à partir d’un filtre de DirectShow, utilisez la fonction **PERFLOG \_ STREAMTRACE** , qui est définie dans le fichier d’en-tête Dxmperf. h. cet en-tête est inclus dans les classes de base DirectShow.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Perfstruct. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Celles](directshow-structures.md)
</dt> <dt>

[Suivi d’événements dans DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUID d’événements de trace](trace-guids.md)
</dt> </dl>

 

 
