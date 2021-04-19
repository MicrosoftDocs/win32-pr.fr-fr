---
title: Structure DRM_PLAY_OPL (wmdrmsdk. h)
description: La \_ structure OPL de la lecture DRM \_ contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de lecture.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- Structure DRM_PLAY_OPL format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528564"
---
# <a name="drm_play_opl-structure"></a>\_Structure OPL de lecture DRM \_

La **structure \_ \_ OPL de la lecture DRM** contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de lecture.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**minOPL**
</dt> <dd>

[**DRM \_ Structure \_ des \_ \_ niveaux de protection de sortie minimum**](drmdrm-minimum-output-protection-levels.md) contenant le OPL minimal requis pour lire le contenu dans différents formats.

</dd> <dt>

**oplIdReserved**
</dt> <dd>

Réservé pour un usage futur.

</dd> <dt>

**vopi**
</dt> <dd>

[**DRM \_ VIDEO \_ Output \_ \_ ID**](drmdrm-video-output-protection-ids.md) structure contenant les identificateurs de protection de sortie vidéo qui s’appliquent à la lecture du contenu.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_OPL de copie DRM \_**](drmdrm-copy-opl.md)
</dt> <dt>

[**\_OPL de lecture DRM \_ \_ ex**](drm-play-opl-ex.md)
</dt> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





