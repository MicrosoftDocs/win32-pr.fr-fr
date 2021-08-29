---
title: AmbientAttributes.nineGridMargins
description: L’attribut nineGridMargins spécifie des largeurs de marge pour la mise à l’échelle non uniforme de l’élément Skin.
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- AmbientAttributes. nineGridMargins Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d68e9e5ea8d90312d648e4b0af674a93eec84ddcd09ac7d2cb4bc6bc99ae158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573999"
---
# <a name="ambientattributesninegridmargins"></a>AmbientAttributes.nineGridMargins

L’attribut **nineGridMargins** spécifie des largeurs de marge pour la mise à l’échelle non uniforme de l’élément Skin.

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture qui contient les largeurs des marges sous la forme «*widthLeft*,*widthTop*,*widthRight*,*widthBottom*». Chaque valeur de largeur est un nombre qui représente la largeur, en pixels, d’une marge pour la grille neuf.

## <a name="remarks"></a>Remarques

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

 

 





