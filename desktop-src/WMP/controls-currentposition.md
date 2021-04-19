---
title: Controls. currentPosition
description: La propriété currentPosition spécifie ou récupère, en secondes, la position actuelle dans l’élément multimédia à partir du début.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Controls. currentPosition Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543297"
---
# <a name="controlscurrentposition"></a>Controls. currentPosition

La propriété **CurrentPosition** spécifie ou récupère, en secondes, la position actuelle dans l’élément multimédia à partir du début.

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture/écriture (**double**).

## <a name="examples"></a>Exemples

L’exemple suivant utilise **CurrentPosition** pour rechercher une position fournie par l’utilisateur. Un élément bouton HTML est créé pour exécuter le code JScript. Un élément d’entrée de texte HTML, nommé setPosition, a été créé pour accepter une valeur, en secondes, de l’utilisateur. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Controls (objet)**](controls-object.md)
</dt> </dl>

 

 





