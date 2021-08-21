---
title: Slider. backgroundImage
description: L’attribut backgroundImage spécifie ou récupère l’image d’arrière-plan du curseur.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- slider. backgroundImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c4f6d31e3f870541310b23544a15c7b9af0043014a9013310cea7dd4ee072
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832996"
---
# <a name="sliderbackgroundimage"></a>Slider. backgroundImage

L’attribut **BackgroundImage** spécifie ou récupère l’image d’arrière-plan du curseur.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.

## <a name="remarks"></a>Remarques

Cet attribut est facultatif. Lorsque vous utilisez des images pour construire un curseur, l' **BackgroundImage** est utilisé pour l’image de curseur principale. Le **thumbImage** représente le curseur réel et peut être déplacé à l’aide de la souris. Au niveau du curseur **thumbImage** se trouve une ligne invisible dans laquelle l’image d’arrière-plan est affichée d’un côté de la ligne, et l’image de premier plan s’affiche de l’autre côté.

Lorsque le curseur **thumbImage** est déplacé à l’aide de la souris, si la **diapositive** est définie sur true, l’image de premier plan glisse comme si elle était extraite par le curseur pour couvrir l’image d’arrière-plan. Si la **diapositive** est définie sur false, l’image de premier plan ne se déplace pas, mais elle est révélée en place, comme si le curseur déplace l’image d’arrière-plan hors de l’image de premier plan.

Si l’attribut **tileed** a la valeur true et que l’image d’arrière-plan est plus petite que le contrôle Slider, l’image est affichée en mosaïque horizontale ou verticale en fonction de l’attribut **direction** . Si l’attribut de **bordure** est défini sur une valeur supérieure à zéro, le nombre spécifié est le nombre de pixels à partir de la gauche et de la droite ou du haut et du bas de l’image (là encore, en fonction de l’attribut de **direction** ) qui sera réservé pour les bordures du contrôle Slider. Dans ce cas, seule la partie centrale de l’image est utilisée pour la mosaïque du reste du contrôle.

Les formats pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> <dt>

[**Slider. foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**Slider. Slide**](slider-slide.md)
</dt> <dt>

[**Slider. thumbImage**](slider-thumbimage.md)
</dt> </dl>

 

 





