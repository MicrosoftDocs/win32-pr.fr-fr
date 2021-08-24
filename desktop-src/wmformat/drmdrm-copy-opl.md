---
title: Structure DRM_COPY_OPL (wmdrmsdk. h)
description: La \_ \_ structure OPL de la copie DRM contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de copie.
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- Structure DRM_COPY_OPL format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ec6e376b2df4cd3e5462766d6fd992ed7d2356a1bc81d0ff74c662a99697af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708979"
---
# <a name="drm_copy_opl-structure"></a>\_ \_ Structure OPL de la copie DRM

La **structure \_ \_ OPL de la copie DRM** contient des informations sur les niveaux de protection de sortie (OPLs) spécifiés dans une licence pour les actions de copie.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**wMinimumCopyLevel**
</dt> <dd>

OPL minimal pour les actions de copie.

</dd> <dt>

**oplIdIncludes**
</dt> <dd>

[**DRM \_ OPL \_ structure \_ ID de sortie**](drmdrm-opl-output-ids.md) contenant les identificateurs des technologies à autoriser. Ce membre est utilisé pour les technologies de sortie qui sont affectées OPLs inférieur au niveau de copie minimal, mais sur lequel le contenu peut être copié.

</dd> <dt>

**oplIdExcludes**
</dt> <dd>

[**DRM \_ OPL \_ structure \_ ID de sortie**](drmdrm-opl-output-ids.md) contenant les identificateurs de sortie des technologies à restreindre. Ce membre est utilisé pour les technologies de sortie auxquelles sont affectées des OPLs qui dépassent le niveau de copie minimal, mais que l’émetteur de licence n’accorde pas de droits pour la copie vers.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_OPL de lecture DRM \_**](drmdrm-play-opl.md)
</dt> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





