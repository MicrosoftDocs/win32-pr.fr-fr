---
description: La \_ structure LARGEINT nommée définit une étiquette qui s’affiche lorsqu’une valeur de propriété LARGEINT spécifique est détectée.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: Structure de LABELED_LARGEINT (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fab2942a2a5188527c57663af0c6000aa2cb628eaa2499eef054854df9187784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778769"
---
# <a name="labeled_largeint-structure"></a>\_Structure LARGEINT libellée

La **structure \_ LARGEINT nommée** définit une étiquette qui s’affiche lorsqu’une valeur de propriété LARGEINT spécifique est détectée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Valeur**
</dt> <dd>

Valeur LARGEINT de la propriété que vous souhaitez détecter.

</dd> <dt>

**Étiquette**
</dt> <dd>

Description textuelle ou étiquette qui s’affiche lorsque la valeur LARGEINT spécifiée dans le membre **value** est détectée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le membre **lpLabeledLargeIntTable** de la structure [Set](set.md) pointe vers un tableau de structures d' **ensemble** qui définissent un ou plusieurs membres **label** des paires valeur LARGEINT. Les paires sont utilisées lorsque vous souhaitez afficher une étiquette à la place d’une valeur LARGEINT spécifique trouvée dans un paquet de protocole.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




