---
title: THÈME. openViewRelative
description: La méthode openViewRelative ouvre une vue dans une nouvelle fenêtre à une position initiale spécifiée par rapport à l’angle supérieur gauche de l’apparence.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- THEMe. openViewRelative Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545483"
---
# <a name="themeopenviewrelative"></a>THÈME. openViewRelative

La méthode **openViewRelative** ouvre une **vue** dans une nouvelle fenêtre à une position initiale spécifiée par rapport à l’angle supérieur gauche de l’apparence.

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*affichage*
</dt> <dd>

**Chaîne** spécifiant l' **ID** de la **vue** à ouvrir.

</dd> <dt>

<span id="left"></span><span id="LEFT"></span>*gauche*
</dt> <dd>

**Nombre** (**long**) qui spécifie la distance initiale, en pixels, de la bordure gauche de la **vue** à partir de la bordure gauche de l’apparence. Une valeur négative indique une position initiale à gauche de la bordure de l’apparence.

</dd> <dt>

<span id="top"></span><span id="TOP"></span>*Retour au début*
</dt> <dd>

**Nombre** (**long**) qui spécifie la position initiale de la bordure supérieure de la **vue** par rapport à la bordure supérieure de l’apparence. Une valeur négative indique une position initiale au-dessus de la bordure de l’apparence.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La position spécifiée pour la **vue** est utilisée la première fois que cette méthode est appelée, après laquelle l’utilisateur peut faire glisser la **vue** vers un autre emplacement. La nouvelle position est enregistrée et, lors des appels suivants, la position la plus récente est utilisée.

## <a name="examples"></a>Exemples


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément THEMe**](theme-element.md)
</dt> <dt>

[**THÈME. évènement CloseView**](theme-closeview.md)
</dt> <dt>

[**THEMe. openView**](theme-openview.md)
</dt> </dl>

 

 





