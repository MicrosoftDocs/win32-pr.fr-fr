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
ms.openlocfilehash: 7ee2ac65e10e0dc9be46ab103fe21abcc78dc403302b298f3eb2fc83000802cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982951"
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

## <a name="remarks"></a>Remarques

Les modèles du  \[ tableau de modèles Max PatternMatch \_ \] sont joints en tant qu’homologues dans les instructions or logiques au format

(Modèle 1 \| \| Modèle 2 modèle \| \| 3).

Pour plus d’informations sur l’implémentation de cette structure, consultez [filtres de capture](capture-filters.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




