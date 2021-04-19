---
description: La \_ structure PERFINFO DShow \_ AVREND contient des données pour un événement de trace de type GUID \_ VIDEOREND. VMR enregistre cet événement immédiatement avant le rendu d’un frame.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: Structure PERFINFO_DSHOW_AVREND (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: ee2d944d086f9c1a4ea7944f023321dfbc06d547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531092"
---
# <a name="perfinfo_dshow_avrend-structure"></a>PERFINFO \_ DShow \_ AVREND, structure

La `PERFINFO_DSHOW_AVREND` structure contient des données pour un événement de trace de type GUID \_ VIDEOREND.

VMR enregistre cet événement immédiatement avant le rendu d’un frame.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a>Membres

<dl> <dt>

**cycleCounter**
</dt> <dd>

Dernier nombre de cycles d’horloge (instruction RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Heure de référence actuelle, telle qu’elle est retournée par la méthode [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .

</dd> <dt>

**sampleTime**
</dt> <dd>

Heure de début de l’exemple.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour activer cet événement, vous devez définir l' \_ indicateur DXMPERF VIDEOREND dans le paramètre *EnableFlag* lorsque vous appelez **EnableTrace**. Cet indicateur est défini dans le fichier d’en-tête Dxmperf. h, qui est inclus dans les classes de base DirectShow.

Pour enregistrer cet événement à partir d’un filtre DirectShow, utilisez la macro **PERFLOG \_ VIDEOREND** , qui est définie dans Dxmperf. h.

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

 

 




