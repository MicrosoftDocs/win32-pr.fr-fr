---
title: BUTTONELEMENT. mappingColor
description: L’attribut mappingColor spécifie ou récupère la clé de couleur qui identifie ce BUTTONELEMENT dans le BUTTONGROUP.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- BUTTONELEMENT. mappingColor Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855675"
---
# <a name="buttonelementmappingcolor"></a>BUTTONELEMENT. mappingColor

L’attribut **mappingColor** spécifie ou récupère la clé de couleur qui identifie ce **BUTTONELEMENT** dans le **BUTTONGROUP**.

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant toute valeur de couleur Microsoft Internet Explorer. Il n'a aucune valeur par défaut.

## <a name="remarks"></a>Notes

Cet attribut spécifie la couleur de la région dans le groupe de boutons **mappingImage** qui correspond à cet élément de bouton. Tous les clics sur cette région sont gérés par cet élément bouton.

Si une couleur non valide est spécifiée, le **BUTTONELEMENT** n’est pas activé.

## <a name="examples"></a>Exemples

L’exemple suivant est un fichier de définition d’apparence complet qui illustre l’utilisation de certains des attributs **BUTTONELEMENT** . Il se trouve dans le répertoire d’exemples qui a été installé avec le kit de développement logiciel (SDK).


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence de couleur**](color-reference.md)
</dt> <dt>

[**Élément BUTTONELEMENT**](buttonelement-element.md)
</dt> <dt>

[**BUTTONGROUP. mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





