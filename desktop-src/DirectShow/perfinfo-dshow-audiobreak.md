---
description: La \_ structure PERFINFO DShow \_ AUDIOBREAK contient des données pour un événement de trace de type GUID \_ AUDIOBREAK. Le filtre de convertisseur DirectSound enregistre cet événement en cas de rupture dans le flux audio.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: Structure PERFINFO_DSHOW_AUDIOBREAK (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544118"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a>PERFINFO \_ DShow \_ AUDIOBREAK, structure

La `PERFINFO_DSHOW_AUDIOBREAK` structure contient des données pour un événement de trace de type GUID \_ AUDIOBREAK.

Le filtre de [convertisseur DirectSound](directsound-renderer-filter.md) enregistre cet événement en cas de rupture dans le flux audio.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a>Membres

<dl> <dt>

**cycleCounter**
</dt> <dd>

Dernier nombre de cycles d’horloge (instruction RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Position d’écriture actuelle dans la mémoire tampon DirectSound.

</dd> <dt>

**sampleTime**
</dt> <dd>

Début de la coupure audio dans la mémoire tampon DirectSound.

</dd> <dt>

**sampleDuration**
</dt> <dd>

Durée de l’arrêt, en millisecondes.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour activer cet événement, vous devez définir l' \_ indicateur de bit AUDIOBREAK dans le paramètre *EnableFlag* lorsque vous appelez **EnableTrace**. Cet indicateur est défini dans le fichier d’en-tête Dxmperf. h, qui est inclus dans les classes de base DirectShow.

Pour enregistrer cet événement à partir d’un filtre DirectShow, utilisez la macro **PERFLOG \_ AUDIOBREAK** , qui est définie dans Dxmperf. h.

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

 

 




