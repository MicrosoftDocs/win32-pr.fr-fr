---
title: Structure DRM_PLAY_OPL_EX (wmdrmsdk. h)
description: La \_ structure de lecture DRM \_ OPL \_ ex contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de lecture.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- Structure DRM_PLAY_OPL_EX format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294447"
---
# <a name="drm_play_opl_ex-structure"></a>\_Structure de lecture DRM \_ OPL \_ ex

La structure de **\_ lecture DRM \_ OPL \_ ex** contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de lecture.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwVersion**
</dt> <dd>

Numéro de version.

</dd> <dt>

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

## <a name="remarks"></a>Notes

Cette structure est identique à la **structure \_ \_ OPL de la lecture DRM** , à ceci près qu’elle comprend un numéro de version.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_OPL de lecture DRM \_**](drmdrm-play-opl.md)
</dt> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





