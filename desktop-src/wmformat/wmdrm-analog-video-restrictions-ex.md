---
title: Structure WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX (wmdrmsdk. h)
description: La \_ \_ \_ structure ex des restrictions de la vidéo analogique WMDRM \_ contient des informations étendues sur une restriction pour la diffusion de contenu sous forme de vidéo analogique.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- Structure WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59c9ca5f58cf2adadeb5a6a0618457472cde976c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545416"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a>Limites de la \_ vidéo analogique WMDRM \_ \_ \_ ex structure

La structure ex des restrictions de la **\_ \_ vidéo \_ \_ analogique WMDRM** contient des informations étendues sur une restriction pour la diffusion de contenu sous forme de vidéo analogique.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwVersion**
</dt> <dd>

Numéro de version.

</dd> <dt>

**guidRestrictionID**
</dt> <dd>

ID de restriction.

</dd> <dt>

**cbRestrictionData**
</dt> <dd>

Taille des données de restriction en octets.

</dd> <dt>

**pbRestrictionData**
</dt> <dd>

Données de restriction.

</dd> </dl>

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> <dt>

[**RESTRICTIONS de la \_ vidéo analogique WMDRM \_ \_**](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





