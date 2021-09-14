---
title: Structure DRM_VIDEO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: La \_ \_ structure de l’ID de protection de la sortie vidéo DRM \_ \_ contient un tableau de \_ structures de protection de sortie vidéo DRM \_ \_ .
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- Structure DRM_VIDEO_OUTPUT_PROTECTION_IDS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295191"
---
# <a name="drm_video_output_protection_ids-structure"></a>Structure des ID de protection de la \_ sortie vidéo DRM \_ \_ \_

La structure de l’ID de protection de la **\_ \_ sortie \_ \_ vidéo DRM** contient un tableau de structures de **\_ \_ \_ protection de sortie vidéo DRM** .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**cEntries**
</dt> <dd>

Nombre d’éléments dans le tableau référencé par **rgVop**.

</dd> <dt>

**rgVop**
</dt> <dd>

Adresse d’un tableau de structures de **\_ \_ \_ protection de sortie vidéo DRM** . **DRM \_ La \_ \_ protection de sortie vidéo** est un type défini comme [**\_ \_ protection de sortie DRM**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est utilisée en tant que membre de la structure de [**\_ lecture DRM \_ OPL**](drmdrm-play-opl.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ID de \_ protection de sortie audio \_ DRM \_**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**\_ID de \_ protection de sortie vidéo DRM \_ \_ \_ ex**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





