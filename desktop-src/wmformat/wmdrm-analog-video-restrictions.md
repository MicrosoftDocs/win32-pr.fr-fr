---
title: Structure WMDRM_ANALOG_VIDEO_RESTRICTIONS (wmdrmsdk. h)
description: La \_ \_ \_ structure des restrictions de la vidéo de l’entrée WMDRM contient des informations sur une restriction pour la diffusion de contenu en tant que vidéo analogique.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- Structure WMDRM_ANALOG_VIDEO_RESTRICTIONS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d6b8fe957468baebb6da06f45ba7b37756413c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539613"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a>Structure des restrictions de la \_ vidéo analogique WMDRM \_ \_

La structure des **\_ \_ \_ restrictions** de la vidéo de l’entrée WMDRM contient des informations sur une restriction pour la diffusion de contenu en tant que vidéo analogique.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**guidRestrictionID**
</dt> <dd>

Identificateur de restriction.

</dd> <dt>

**dwRestrictionData**
</dt> <dd>

Données de restriction.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est reçue quand vous appelez [**IWMDRMLicense :: GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> <dt>

[**RESTRICTIONS de la \_ vidéo analogique WMDRM \_ \_ \_ ex**](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





