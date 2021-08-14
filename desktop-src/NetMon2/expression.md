---
description: Contient un groupe de tableaux ANDEXP évalués comme homologues.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Structure d’EXPRESSION (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4efa1f79477e3dcc13bedfddb2cdca7fd660f5430b7d7f2b87dbd9d4b4425098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366837"
---
# <a name="expression-structure"></a>Structure de l’EXPRESSION

La structure d' **expression** contient un groupe de tableaux **ANDEXP** évalués comme pairs dans des expressions and logiques, qui ont le format

(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a>Membres

<dl> <dt>

**nAndExps**
</dt> <dd>

Nombre de modèles **ANDEXP** .

</dd> <dt>

**AndExp**
</dt> <dd>

Tableau de modèles **ANDEXP** . Le filtre de capture réorganise toutes les lignes de ce tableau en instructions AND logiques. N’oubliez pas que chaque structure d’EXPRESSION peut contenir un maximum de quatre modèles **ANDEXP** .

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour plus d’informations sur l’implémentation de cette structure dans le cadre d’un filtre de capture, consultez [filtres de capture](capture-filters.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




