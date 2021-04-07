---
description: L’élément param spécifie la valeur d’une propriété sur une transition, un effet ou un autre sous-objet.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: param, élément (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb1d007a7f3e2dcffaa7b9163c76be604fed7a9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846558"
---
# <a name="param-element"></a>Élément param

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `param` élément spécifie la valeur d’une propriété sur une transition, un effet ou un autre sous-objet.

## <a name="attributes"></a>Attributs

[**nom**](name-attribute.md), [ **valeur**](value-attribute.md)

## <a name="parentchild-information"></a>Informations parent/enfant



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**clip**](clip-element.md), [**effet**](effect-element.md), [**transition**](transition-element.md) |
| Children | [**at**](at-element.md), [ **linéaire**](linear-element.md)                                               |



 

## <a name="remarks"></a>Notes

L’attribut **value** spécifie la valeur de la propriété au début de la transition ou de l’effet. Utilisez l’élément **at** ou **Linear** pour spécifier la modification des valeurs. Si l’élément **param** ne contient pas d’éléments **at** ou **Linear** , la valeur reste constante sur la durée de l’effet ou de la transition.

> [!Note]  
> Un élément **param** à l’intérieur d’un élément **clip** ne peut pas contenir d’éléments **au niveau** ou **linéaires** .

 

De nombreuses transitions prennent en charge une propriété de **progression** standard qui varie de 0 à 1,0, indiquant quel pourcentage de la transition est reflété dans la sortie. À la **progression** = 0,0, la transition se trouve au début de sa séquence (entièrement la première image vidéo). À la **progression** = 0,5, la transition est à moitié terminée. (Par exemple, dans une réinitialisation, à la **progression** = 0,5 la limite de transition se trouve au centre de l’image) À la **progression** = 1,0, la transition est terminée (entièrement la deuxième image). Par défaut, les transitions passent de **Progress** = 0,0 au début de la transition vers **Progress** = 1,0 à la fin.

D’autres propriétés sont généralement spécifiques à une transition ou un effet particulier. Par exemple, la transition de réinitialisation prend en charge une propriété **GradientSize** qui contrôle la largeur de la zone de transition.

Pour exécuter une transition vers l’arrière, définissez la propriété **Progress** sur 1,0 au début de la transition et utilisez l’élément **linéaire** pour changer la valeur en 0,0, comme illustré dans l’exemple suivant :


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a>Exemples


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments XTL](xtl-elements.md)
</dt> </dl>

 

 



