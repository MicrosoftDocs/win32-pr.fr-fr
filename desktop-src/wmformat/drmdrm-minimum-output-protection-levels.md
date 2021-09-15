---
title: Structure DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: La \_ \_ \_ structure des niveaux de protection de sortie minimum DRM \_ contient les niveaux de protection de sortie minimum (OPLs) pour la lecture de différents types de contenu. Un appareil doit prendre en charge la OPL minimale pour qu’un type de données reçoive ce type de données à partir du lecteur.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- Structure DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295198"
---
# <a name="drm_minimum_output_protection_levels-structure"></a>\_Structure des \_ niveaux de protection de sortie DRM minimum \_ \_

La structure des **\_ niveaux de \_ \_ protection \_ de sortie minimum DRM** contient les niveaux de protection de sortie minimum (OPLs) pour la lecture de différents types de contenu. Un appareil doit prendre en charge la OPL minimale pour qu’un type de données reçoive ce type de données à partir du lecteur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**wCompressedDigitalVideo**
</dt> <dd>

OPL minimale requise pour recevoir la vidéo numérique compressée.

</dd> <dt>

**wUncompressedDigitalVideo**
</dt> <dd>

OPL minimal requis pour recevoir une vidéo numérique non compressée.

</dd> <dt>

**wAnalogVideo**
</dt> <dd>

OPL minimal requis pour recevoir la vidéo analogique.

</dd> <dt>

**wCompressedDigitalAudio**
</dt> <dd>

OPL minimal requis pour la réception de données audio numériques compressées.

</dd> <dt>

**wUncompressedDigitalAudio**
</dt> <dd>

OPL minimal requis pour recevoir des données audio numériques non compressées.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est utilisée en tant que membre de la structure de [**\_ lecture DRM \_ OPL**](drmdrm-play-opl.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





