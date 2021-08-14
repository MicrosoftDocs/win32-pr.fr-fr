---
description: La \_ structure DWORD étiquetée définit une étiquette qui s’affiche lorsqu’une valeur de propriété DWORD spécifique est détectée.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: Structure de LABELED_DWORD (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 10f3e0dd09b37821a00f2c10f99c0ea6d509ff388e9d7394a8b2c4958438f979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364844"
---
# <a name="labeled_dword-structure"></a>\_Structure DWORD étiquetée

La **structure \_ DWORD étiquetée** définit une étiquette qui s’affiche lorsqu’une valeur de propriété DWORD spécifique est détectée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a>Membres

<dl> <dt>

**Valeur**
</dt> <dd>

Valeur DWORD de la propriété que vous souhaitez détecter.

</dd> <dt>

**Étiquette**
</dt> <dd>

Description textuelle ou étiquette qui s’affiche lorsque la valeur DWORD spécifiée dans le membre **value** est détectée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le membre **lpLabeledDwordTable** de la structure [Set](set.md) pointe vers un tableau de structures d' **ensemble** qui définissent un ou plusieurs membres **étiquette** des paires valeur DWORD. Les paires sont utilisées lorsque vous souhaitez afficher une étiquette à la place d’une valeur DWORD spécifique trouvée dans le paquet de protocole.

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

 

 




