---
title: Slider. foregroundImage
description: L’attribut foregroundImage spécifie ou récupère l’image de premier plan du curseur.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- slider. foregroundImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7fad50a6e33ca4de5890dfca340e36aa2fdc0af0c0b938793eac4edc1dfb71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735709"
---
# <a name="sliderforegroundimage"></a>Slider. foregroundImage

L’attribut **foregroundImage** spécifie ou récupère l’image de premier plan du curseur.

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.

## <a name="remarks"></a>Remarques

Cet attribut est facultatif. Lorsque vous utilisez des images pour construire un contrôle Slider, l' **BackgroundImage** est utilisé pour l’image de curseur principale. Le **thumbImage** représente le curseur réel et peut être déplacé à l’aide de la souris. Au niveau du curseur **thumbImage** se trouve une ligne invisible dans laquelle l’image d’arrière-plan est affichée d’un côté de la ligne, et l’image de premier plan s’affiche de l’autre côté.

Lorsque le curseur **thumbImage** est déplacé à l’aide de la souris, si la **diapositive** est définie sur true, l’image de premier plan glisse comme si elle était extraite par le curseur pour couvrir l’image d’arrière-plan. Si la **diapositive** est définie sur false, l’image de premier plan ne se déplace pas, mais elle est révélée en place, comme si le curseur déplace l’image d’arrière-plan hors de l’image de premier plan.

Si l’attribut **tileed** a la valeur true et que l’image de premier plan est plus petite que la zone de premier plan du contrôle Slider, l’image est affichée en mosaïque horizontalement ou verticalement, selon l’attribut **direction** , pour occuper l’espace disponible.

Les formats pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> <dt>

[**Slider. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**Slider. Slide**](slider-slide.md)
</dt> <dt>

[**Slider. thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**Slider. Value**](slider-value.md)
</dt> </dl>

 

 





