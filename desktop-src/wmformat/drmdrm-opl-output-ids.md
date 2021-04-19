---
title: Structure DRM_OPL_OUTPUT_IDS (wmdrmsdk. h)
description: La \_ \_ \_ structure des ID de sortie DRM OPL contient un certain nombre d’identificateurs de sortie de niveau de protection de sortie (OPL).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- Structure DRM_OPL_OUTPUT_IDS format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525536"
---
# <a name="drm_opl_output_ids-structure"></a>\_Structure des \_ ID de sortie DRM OPL \_

La structure des **\_ ID de \_ sortie \_ DRM OPL** contient un certain nombre d’identificateurs de sortie de niveau de protection de sortie (OPL).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**CID**
</dt> <dd>

Nombre d’identificateurs dans le tableau référencé par **rgIds**.

</dd> <dt>

**rgIds**
</dt> <dd>

Adresse d’un tableau de GUID. Chaque membre du tableau contient un identificateur de sortie OPL.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est utilisée en tant que membre des structures [**DRM \_ Copy \_ OPL**](drmdrm-copy-opl.md) et [**DRM \_ Play \_ OPL**](drmdrm-play-opl.md) pour identifier les groupes d’identificateurs de sortie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





