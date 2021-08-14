---
title: CUSTOMSLIDER.positionImage
description: L’attribut positionImage spécifie ou récupère l’image interactive utilisée pour déterminer l’image de position à partir du fichier image à afficher.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- CUSTOMSLIDER. positionImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727601ceb7ed078e40a284ab291f2e182a4270682b5f1db104515e31d3dbe2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749989"
---
# <a name="customsliderpositionimage"></a>CUSTOMSLIDER.positionImage

L’attribut **positionImage** spécifie ou récupère l’image interactive utilisée pour déterminer l’image de position à partir du fichier image à afficher.

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.

## <a name="remarks"></a>Remarques

Cet attribut est obligatoire et doit être spécifié.

Le **positionImage** n’est pas affiché. Au lieu de cela, elle sert de carte qui définit les zones interactives de l’image affichée. L’image affichée est l’une des sous-images du fichier image et représente l’état réel du curseur. Le **positionImage** comprend un nombre de régions de l’échelle gris égal au nombre de ces sous-images. Les sous-images doivent avoir les mêmes dimensions que le **positionImage** ou le curseur personnalisé ne fonctionnera pas correctement.

Vous ne pouvez pas cliquer sur une région qui n’est pas en gris. Les régions intercliquables doivent être définies sur des valeurs de couleur qui s’adaptent uniformément à la gamme de nuances de gris du noir au blanc, la première région étant le noir pur et la dernière région étant un blanc pur. Les valeurs de couleur de chaque région successive doivent être incrémentées d’une valeur égale à 255 divisée par le nombre total de régions moins un, en arrondissant au nombre entier le plus proche.

Par exemple, s’il existe six régions, l’incrément est de 51 (255 divisé par 5) et les six valeurs de mise à l’échelle de gris sont 0, 51, 102, 153, 204 et 255. Les valeurs de couleur hexadécimale pour les six régions seraient \# 000000, \# 333333, \# 666666, \# 999999, \# cccccc et \# FFFFFF.

De cette façon, les régions auront une séquence dictée par leurs valeurs de couleur de l’échelle grise, et cette séquence correspondra à la séquence de sous-images dans le fichier image. Quand l’utilisateur clique sur l’une des régions, la sous-image correspondante est affichée et la **valeur** du curseur personnalisé est mise à jour en conséquence.

Les types de fichiers image pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).

## <a name="examples"></a>Exemples

Voici un exemple de curseur personnalisé **positionImage**. L’image correspondante est présentée dans la section exemple de la propriété **image** .

![exemple de graphique positionimage](images/dialmap.png)

Le code suivant illustre l’utilisation des attributs **CUSTOMSLIDER** .


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

    <SLIDER
      id = "myslider"
      min = "0"
      max = "wmpprop:player.currentMedia.duration"
      onmouseup = "player.controls.currentPosition = myslider.value; "
      tooltip = "current position"
      height = "10"
      width = "180"
      top = "150"
      left = "88"
      backgroundColor = "red"
      foregroundColor = "blue"
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER. image**](customslider-image.md)
</dt> </dl>

 

 





