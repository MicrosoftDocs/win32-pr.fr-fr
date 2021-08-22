---
description: L' \_ \_ énumération de type principal de la chronologie spécifie le type principal d’un objet.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: Énumération TIMELINE_MAJOR_TYPE (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: b18088a9d01b263c80a4ff941a6b7720043da708eaeaebf4f79a2084d1ed258f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501719"
---
# <a name="timeline_major_type-enumeration"></a>\_Énumération de type principal de chronologie \_

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `TIMELINE_MAJOR_TYPE` énumération spécifie le type principal d’un objet.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**TYPE principal de la chronologie \_ \_ \_ composite**
</dt> <dd>

Objet composite. Contient une ou plusieurs pistes.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**\_piste de \_ type \_ principal de la chronologie**
</dt> <dd>

Objet Track. Contient une ou plusieurs sources.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**\_source de \_ type \_ principal de la chronologie**
</dt> <dd>

Objet source. Contient une référence à une source de média.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**\_transition de \_ type \_ principal de la chronologie**
</dt> <dd>

Objet de transition. Définit une transition entre des composites, des pistes ou des sources.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_effet de \_ type \_ principal de la chronologie**
</dt> <dd>

Objet Effect. Définit un effet d’entrée unique à appliquer à un objet composite, Track ou source.

</dd> <dt>

<span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**\_groupe de \_ types \_ principaux de la chronologie**
</dt> <dd>

Objet Group. Contient une ou plusieurs pistes d’un type donné.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAMTimeline**](iamtimeline.md)
</dt> <dt>

[**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[**IAMTimelineObj::GetTimelineType**](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




