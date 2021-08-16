---
title: Structure WMDRM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: La \_ structure des \_ niveaux de protection de sortie WMDRM \_ contient les niveaux de protection de sortie (OPLs) requis par une licence pour effectuer diverses actions.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- Structure WMDRM_OUTPUT_PROTECTION_LEVELS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a19d7098266857f8a17e395ad749b216e45ce101278812f67c032943933955a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843960"
---
# <a name="wmdrm_output_protection_levels-structure"></a>\_Structure des \_ niveaux de protection de sortie WMDRM \_

La structure des **\_ niveaux de \_ protection \_ de sortie WMDRM** contient les niveaux de protection de sortie (OPLs) requis par une licence pour effectuer diverses actions.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
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

</dd> <dt>

**wMinimumCopyProtectionLevel**
</dt> <dd>

OPL minimal requis pour copier le contenu.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est utilisée par la méthode [**IWMDRMLicense :: GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





