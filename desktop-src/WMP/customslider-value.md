---
title: CUSTOMSLIDER. Value
description: L’attribut value spécifie ou récupère la position actuelle du curseur. | CUSTOMSLIDER. Value
ms.assetid: 29e17f48-1848-458d-9da4-316013b21980
keywords:
- CUSTOMSLIDER. value Lecteur Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a256274fe2170ad50c164f7bf6768f82e3266db7a4ea5e2c6c8e28edd083c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579707"
---
# <a name="customslidervalue"></a>CUSTOMSLIDER. Value

L’attribut **value** spécifie ou récupère la position actuelle du curseur.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) avec une valeur par défaut égale à l’attribut **min** .

## <a name="remarks"></a>Notes

La **valeur** doit être supérieure ou égale à **min** et inférieure ou égale à **Max**. Si la valeur se trouve en dehors de la plage, un avertissement est émis et la valeur ne change pas.

## <a name="examples"></a>Exemples

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément **CUSTOMSLIDER** , consultez l’attribut [positionImage](customslider-positionimage.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément CUSTOMSLIDER**](customslider-element.md)
</dt> </dl>

 

 





