---
title: TEXT. Value
description: L’attribut value spécifie ou récupère le texte affiché dans le contrôle de texte.
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- TEXT. Value lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525451"
---
# <a name="textvalue"></a>TEXT. Value

L’attribut **value** spécifie ou récupère le texte affiché dans le contrôle de texte.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Si la largeur du contrôle de texte est insuffisante pour contenir le texte fourni, le texte est rogné et des points de suspension s’affichent pour illustrer le fait. Si l’attribut **ToolTip** n’a pas été défini, le texte complet s’affiche alors sous la forme d’une info-bulle lorsque le curseur pointe sur le contrôle.

Si aucune largeur n’est spécifiée, la largeur par défaut du contrôle correspond à la largeur de la chaîne.

Si la hauteur du contrôle n’est pas spécifiée, la hauteur par défaut est une ligne.

Si l’attribut **wordWrap** a la valeur true et que la hauteur du contrôle est suffisante pour accueillir une autre ligne de texte, le texte est renvoyé à la ligne suivante. L’encapsulage se produit uniquement entre les mots. Les sauts de ligne peuvent également être forcés, comme expliqué sous **wordWrap**.

## <a name="examples"></a>Exemples

L’exemple suivant est un fichier de définition d’apparence complet qui illustre l’utilisation des attributs de l’élément de **texte** . Il se trouve dans le répertoire d’exemples qui a été installé avec le kit de développement logiciel (SDK).


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément de texte**](text-element.md)
</dt> <dt>

[**TEXT. toolTip**](text-tooltip.md)
</dt> <dt>

[**TEXT. wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





