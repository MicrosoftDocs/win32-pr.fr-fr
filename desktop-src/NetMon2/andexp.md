---
description: La structure ANDEXP contient un tableau de correspondances de modèle utilisées pour évaluer les données de frame.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: ANDEXP, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021117"
---
# <a name="andexp-structure"></a>ANDEXP, structure

La structure **ANDEXP** contient un tableau de correspondances de modèle utilisées pour évaluer les données de frame.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a>Membres

<dl> <dt>

**nPatternMatches**
</dt> <dd>

Nombre de correspondances de modèle.

</dd> <dt>

**PatternMatch**
</dt> <dd>

Tableau d’éléments de correspondance de modèle. Notez que chaque structure **ANDEXP** peut contenir jusqu’à quatre éléments de correspondance de modèle. Pour plus d’informations sur ce membre, consultez [filtres de capture](capture-filters.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Les modèles du  \[ tableau de modèles Max PatternMatch \_ \] sont joints en tant qu’homologues dans les instructions or logiques au format

(Modèle 1 \| \| Modèle 2 modèle \| \| 3).

Pour plus d’informations sur l’implémentation de cette structure, consultez [filtres de capture](capture-filters.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




