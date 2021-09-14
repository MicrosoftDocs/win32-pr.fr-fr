---
description: La structure de mot ÉTIQUETÉe \_ définit une étiquette qui s’affiche lorsqu’une valeur de propriété de mot spécifique est détectée.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: Structure de LABELED_WORD (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119221"
---
# <a name="labeled_word-structure"></a>Structure de mot ÉTIQUETÉe \_

La structure de **\_ mot étiquetée** définit une étiquette qui s’affiche lorsqu’une valeur de propriété de mot spécifique est détectée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a>Membres

<dl> <dt>

**Valeur**
</dt> <dd>

Valeur de mot de la propriété que vous souhaitez détecter.

</dd> <dt>

**Étiquette**
</dt> <dd>

Description textuelle ou étiquette qui s’affiche lorsque la valeur de mot spécifiée dans le membre de **valeur** est détectée.

</dd> </dl>

## <a name="remarks"></a>Notes

Le membre **lpLabeledWordTable** de la structure [Set](set.md) pointe vers un tableau de structures Set pour définir une ou plusieurs paires valeur d’étiquette. Ces paires sont utilisées lorsque vous souhaitez afficher une étiquette à la place d’une valeur de mot spécifique trouvée dans un paquet de protocole.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




