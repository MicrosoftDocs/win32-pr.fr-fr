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
ms.openlocfilehash: 0e9cbacff2d330c869c35eb7a3d1ca46ae6c80a030495ffec42eabc3726436c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006539"
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

 

 





