---
title: Slider. Value
description: L’attribut value spécifie ou récupère la position actuelle du curseur. | Slider. Value
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- slider. value Lecteur Windows Media
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f9ae7c0dc45f3a14cad2aa5b7332b037302b6658043233bbd98b1d99a12e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118627"
---
# <a name="slidervalue"></a>Slider. Value

L’attribut **value** spécifie ou récupère la position actuelle du curseur.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur par défaut est **min**.

## <a name="remarks"></a>Remarques

La **valeur** doit toujours être supérieure ou égale à **min** et inférieure ou égale à **Max**. Si vous spécifiez une valeur en dehors de cette plage, la **valeur** et la position du curseur ne sont pas modifiées.

Consultez **CUSTOMSLIDER**. attribut [positionImage](customslider-positionimage.md) pour un exemple illustrant l’utilisation des attributs de l’élément **Slider** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Slider (élément)**](slider-element.md)
</dt> <dt>

[**Slider. min.**](slider-min.md)
</dt> </dl>

 

 





