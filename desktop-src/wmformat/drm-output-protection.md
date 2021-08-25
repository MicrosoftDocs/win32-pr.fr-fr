---
title: Structure DRM_OUTPUT_PROTECTION (wmdrmsdk. h)
description: La \_ structure protection de la sortie DRM contient des \_ informations sur une technologie de protection de sortie.
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- Structure DRM_OUTPUT_PROTECTION format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82454d8b4982e6546b003ae3977c7a98869d46ba393ea49f0b97773f95572777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881129"
---
# <a name="drm_output_protection-structure"></a>Structure de protection de \_ sortie DRM \_

La **structure \_ \_ protection de la sortie DRM** contient des informations sur une technologie de protection de sortie.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**Guidid ne**
</dt> <dd>

GUID identifiant la technologie de protection de sortie.

</dd> <dt>

**bConfigData**
</dt> <dd>

Données de configuration pour la technologie.

</dd> </dl>

## <a name="remarks"></a>Remarques

**DRM \_ La \_ \_** protection de sortie audio et la protection de sortie de la **\_ vidéo \_ \_ DRM** sont toutes deux définies comme **\_ \_ protection de sortie DRM** dans les instructions **typedef** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PROTECTION de la sortie DRM par \_ \_ \_ exemple**](drm-output-protection-ex.md)
</dt> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





