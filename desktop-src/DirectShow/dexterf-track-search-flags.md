---
description: L' \_ \_ énumération DEXTERF Track Search \_ Flags spécifie les conditions limites sur une recherche d’un objet dans la chronologie.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: Énumération DEXTERF_TRACK_SEARCH_FLAGS (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537589"
---
# <a name="dexterf_track_search_flags-enumeration"></a>\_ \_ Énumération d’indicateurs de recherche DEXTERF Track \_

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `DEXTERF_TRACK_SEARCH_FLAGS` énumération spécifie les conditions limites sur une recherche d’un objet dans la chronologie.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**délimitation DEXTERF \_**
</dt> <dd>

Recherche un objet qui s’étend sur l’heure spécifiée.

</dd> <dt>

<span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF \_ exactement \_ à**
</dt> <dd>

Recherche un objet qui démarre exactement à l’heure spécifiée.

</dd> <dt>

<span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF les \_ transferts**
</dt> <dd>

Recherchez un objet qui commence à l’heure spécifiée ou une version ultérieure.

</dd> </dl>

## <a name="remarks"></a>Notes

Ces conditions limites sont résumées dans le tableau suivant.



| Valeur d'énumération    | Condition limite                        |
|----------------------|-------------------------------------------|
| délimitation DEXTERF \_    | Start <= TimeStop > Time<br/> |
| DEXTERF \_ exactement \_ à | Start = = heure                             |
| DEXTERF les \_ transferts    | >de début = heure                          |



 

-   Start : heure de début de l’objet récupéré.
-   Arrêter : heure d’arrêt de l’objet récupéré.
-   Heure : durée de recherche spécifiée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




