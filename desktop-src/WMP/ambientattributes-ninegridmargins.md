---
title: AmbientAttributes.nineGridMargins
description: L’attribut nineGridMargins spécifie des largeurs de marge pour la mise à l’échelle non uniforme de l’élément Skin.
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- Lecteur Windows Media AmbientAttributes. nineGridMargins
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530443"
---
# <a name="ambientattributesninegridmargins"></a>AmbientAttributes.nineGridMargins

L’attribut **nineGridMargins** spécifie des largeurs de marge pour la mise à l’échelle non uniforme de l’élément Skin.

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture qui contient les largeurs des marges sous la forme «*widthLeft*,*widthTop*,*widthRight*,*widthBottom*». Chaque valeur de largeur est un nombre qui représente la largeur, en pixels, d’une marge pour la grille neuf.

## <a name="remarks"></a>Notes

Une *grille de neuf* est une technique utilisée pour diviser les éléments de l’interface utilisateur en neuf régions rectangulaires, organisées en 3 et 3 matrices. Lorsqu’un élément est redimensionné, les neuf régions de grille peuvent être mises à l’échelle selon un facteur différent.

Chacune des quatre valeurs de largeur que vous spécifiez représente la largeur d’une ligne ou d’une colonne de trois régions adjacentes. Chaque ligne ou colonne forme le côté gauche, le haut, le côté droit ou le bas de la grille neuf.

[AmbientAttributes. resizeImages](ambientattributes-resizeimages.md) doit avoir la valeur true pour que cet attribut fonctionne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> </dl>

 

 





