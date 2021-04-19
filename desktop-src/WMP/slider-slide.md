---
title: Slider. Slide
description: L’attribut Slide spécifie ou récupère une valeur indiquant si l’image de premier plan glisse sur l’image d’arrière-plan ou est progressivement révélée dans une position statique sur l’image d’arrière-plan.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- Slider. glissement du lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535007"
---
# <a name="sliderslide"></a>Slider. Slide

L’attribut **Slide** spécifie ou récupère une valeur indiquant si l’image de premier plan glisse sur l’image d’arrière-plan ou est progressivement révélée dans une position statique sur l’image d’arrière-plan.

``` syntax
        elementID.slide
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                                          |
|-------|----------------------------------------------------------------------|
| true  | Par défaut. L’image de premier plan glisse sur l’image d’arrière-plan.      |
| false | L’image de premier plan est révélée sur l’image d’arrière-plan. |



 

## <a name="remarks"></a>Notes

Lorsque le curseur **thumbImage** est déplacé à l’aide de la souris, si la **diapositive** est définie sur true, l’image de premier plan glisse comme si elle était extraite par le curseur pour couvrir l’image d’arrière-plan. Si la **diapositive** est définie sur false, l’image de premier plan ne se déplace pas, mais elle est révélée en place, comme si le curseur déplace l’image d’arrière-plan hors de l’image de premier plan.

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

[**Slider. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





