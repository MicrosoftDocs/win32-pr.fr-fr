---
title: Événement Player. KeyPress
description: L’événement KeyPress se produit lorsqu’une touche est enfoncée et libérée. | Événement Player. KeyPress
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- Lecteur Windows Media d’événement keypress
- Lecteur Windows Media de l’événement keypress, classe Player
- Lecteur Windows Media de classe Player, événement keypress
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010988"
---
# <a name="playerkeypress-event"></a>Événement Player. KeyPress

L’événement **KeyPress** se produit lorsqu’une touche est enfoncée et libérée.

## <a name="syntax"></a>Syntaxe


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nKeyAscii* 
</dt> <dd>

**Nombre** (**int**) spécifiant le code ANSI numérique standard pour le caractère.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cet événement se produit lorsque la séquence de touches génère un caractère imprimable du clavier, la touche CTRL combinée à un caractère de l’alphabet standard ou l’un des quelques caractères spéciaux, et la touche entrée ou retour arrière.

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





