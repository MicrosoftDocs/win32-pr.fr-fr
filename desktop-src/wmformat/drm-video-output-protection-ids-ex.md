---
title: Structure DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: La \_ \_ \_ structure d’ID de protection de sortie vidéo DRM \_ \_ contient un tableau \_ de \_ structures de protection de sortie vidéo DRM \_ .
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- Structure DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404698"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a>\_ID de protection de sortie vidéo DRM \_ \_ \_ \_ ex structure

La structure d' **\_ ID de \_ protection de sortie \_ \_ \_ vidéo DRM** contient un tableau de structures de **\_ \_ \_ protection de sortie vidéo DRM** .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
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

Nombre d’éléments dans le tableau référencé par **rgVop**.

</dd> <dt>

**rgVop**
</dt> <dd>

Adresse d’un tableau de structures de **\_ protection de sortie vidéo DRM \_ \_ \_ ex** . **DRM \_ Protection de sortie vidéo par \_ \_ \_ ex** . est un type défini comme [**protection de sortie DRM, par \_ \_ \_ exemple**](drm-output-protection-ex.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Spécifications



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

 

 





