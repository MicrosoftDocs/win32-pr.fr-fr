---
title: Structure DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: La \_ \_ \_ \_ \_ structure ex structure de protection des sorties audio DRM contient une liste d’identificateurs de protection de sortie audio. Cette structure étend les \_ \_ \_ ID de protection de sortie audio DRM \_ en ajoutant un numéro de version.
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- Structure DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545644"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a>\_ID de protection de sortie audio DRM \_ \_ \_ \_ ex structure

La structure ex structure de **\_ \_ protection des sorties \_ \_ \_ audio DRM** contient une liste d’identificateurs de protection de sortie audio. Cette structure étend **les \_ \_ ID de \_ protection \_ de sortie audio DRM** en ajoutant un numéro de version.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwVersion**
</dt> <dd>

Numéro de version.

</dd> <dt>

**cEntries**
</dt> <dd>

Nombre d’entrées dans le tableau **rgAop** .

</dd> <dt>

**rgAop**
</dt> <dd>

Tableau des **structures \_ \_ ex de \_ protection \_ de sortie audio DRM** . **DRM \_ \_Protection de sortie audio \_ \_ ex** est un type défini comme [**protection de sortie DRM, par \_ \_ \_ exemple**](drm-output-protection-ex.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



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

 

 





