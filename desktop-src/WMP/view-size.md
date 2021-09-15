---
title: VIEW. Size
description: La méthode size redimensionne la vue sur un bord spécifié.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- VIEW. size Lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403899"
---
# <a name="viewsize"></a>VIEW. Size

La méthode **Size** redimensionne la **vue** sur un bord spécifié.

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="handle"></span><span id="HANDLE"></span>*traitée*
</dt> <dd>

Chaîne spécifiant le bord ou le coin à déplacer lors du dimensionnement. Cette chaîne doit avoir l’une des huit valeurs suivantes.



| Edge   | Virage      |
|--------|-------------|
| top    | angle supérieur    |
| droite  | telle |
| bottom | bottomleft  |
| gauche   | côté gauche     |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode est généralement appelée à partir d’un gestionnaire **OnMouseDown** . Le redimensionnement s’effectue pendant le déplacement de la souris et arrête le redimensionnement lorsque le bouton de la souris est relâché. Si la taille de la **vue** est restreinte, vous ne pouvez pas faire glisser la souris pour redimensionner la **vue** au-delà des limites restreintes.

## <a name="examples"></a>Exemples


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIEW**](view-element.md)
</dt> </dl>

 

 





