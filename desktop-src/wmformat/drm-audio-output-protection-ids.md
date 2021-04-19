---
title: Structure DRM_AUDIO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: La \_ \_ \_ structure des ID de protection de sortie audio DRM \_ contient une liste d’identificateurs de protection de sortie audio.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- Structure DRM_AUDIO_OUTPUT_PROTECTION_IDS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521719"
---
# <a name="drm_audio_output_protection_ids-structure"></a>\_Structure des \_ \_ ID de protection de sortie audio DRM \_

La structure des **\_ ID de \_ \_ protection \_ de sortie audio DRM** contient une liste d’identificateurs de protection de sortie audio.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**cEntries**
</dt> <dd>

Nombre d’entrées dans le tableau **rgAop** .

</dd> <dt>

**rgAop**
</dt> <dd>

Tableau de structures de **\_ \_ \_ protection de sortie audio DRM** . **DRM \_ La \_ \_ protection de sortie audio** est un type défini comme [**\_ \_ protection de sortie DRM**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ID de \_ protection de sortie audio DRM \_ \_ \_ ex**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**\_ID de \_ protection de sortie vidéo \_ DRM \_**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





