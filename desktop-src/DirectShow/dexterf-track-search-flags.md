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
ms.openlocfilehash: 55d7c70dffbf57ae4d9788a10dfea02911a998e21ab5ea8e3d9ad7fffcf91624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952938"
---
# <a name="dexterf_track_search_flags-enumeration"></a>\_ \_ Énumération d’indicateurs de recherche DEXTERF Track \_

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

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

## <a name="remarks"></a>Remarques

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

 

 




