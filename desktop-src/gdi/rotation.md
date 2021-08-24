---
description: De nombreuses applications CAO offrent des fonctionnalités qui font pivoter des objets dessinés dans la zone cliente.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Rotation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa6552411e2e018d04ff55cbeeb430d185fe62d61dc59d421d08dbe6e0d7174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602699"
---
# <a name="rotation"></a>Rotation

De nombreuses applications CAO offrent des fonctionnalités qui font pivoter des objets dessinés dans la zone cliente. Les applications qui incluent des fonctionnalités de rotation utilisent la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour définir l’espace universel approprié sur la transformation d’espace de page. Cette fonction reçoit un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) contenant les valeurs appropriées. Les membres eM11, eM12, eM21 et eM22 de XFORM spécifient respectivement le cosinus, le sinus, le sinus négatif et le cosinus de l’angle de rotation.

Lorsque la *rotation* se produit, les points qui constituent un objet sont pivotés par rapport à l’origine de l’espace de coordonnées. L’illustration suivante montre un rectangle 20 par 20, pivoté de 30 degrés lorsqu’il est copié à partir de l’espace de coordonnées universelles vers l’espace de coordonnées de page.

![Illustration montrant deux espaces de coordonnées ; chaque a un rectange dans un emplacement différent et avec une rotation différente](images/cstrn-11.png)

Dans l’illustration précédente, chaque point du rectangle a pivoté de 30 degrés par rapport à l’origine de l’espace de coordonnées.

L’algorithme suivant calcule la nouvelle coordonnée x (x) pour un point (x, y) qui pivote par angle A par rapport à l’origine de l’espace de coordonnées.

``` syntax
x' = (x * cos A) - (y * sin A) 
```

L’algorithme suivant calcule la coordonnée y (y) pour un point (x, y) qui est pivoté par l’angle A par rapport à l’origine.

``` syntax
y' = (x * sin A) + (y * cos A) 
```

Les deux transformations de rotation peuvent être combinées dans une matrice 2 par 2 comme suit.

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

La matrice 2-par-2 qui a produit la rotation contient les valeurs suivantes.

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a>Dérivation de l’algorithme de rotation

Les algorithmes de rotation sont basés sur le niveau de l’addition de trigonométrie, indiquant que la fonction trigonométrique d’une somme de deux angles (a1 et a2) peut être exprimée en termes de fonctions trigonométriques des deux angles.

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

L’illustration suivante montre un point p pivoté dans le sens inverse des aiguilles d’une montre vers une nouvelle position p. En outre, il affiche deux triangles formés par une ligne dessinée de l’origine de l’espace de coordonnées à chaque point et une ligne dessinée à partir de chaque point sur l’axe x.

![Diagramme montrant l’origine, p et p et deux triangles](images/cstrn-12.png)

À l’aide de trigonométriques, la coordonnée x du point p peut être obtenue en multipliant la longueur de l’hypoténuse h par le cosinus de a1.

``` syntax
x = h * cos A1 
```

La coordonnée y du point p peut être obtenue en multipliant la longueur de l’hypoténuse h par le sinus de a1.

``` syntax
y = h * sin A1 
```

De même, la coordonnée x du point p peut être obtenue en multipliant la longueur de l’hypoténuse h par le cosinus de (a1 + a2).

``` syntax
x' = h * cos (A1 + A2) 
```

Enfin, la coordonnée y du point p peut être obtenue en multipliant la longueur de l’hypoténuse h par le sinus de (a1 + a2).

``` syntax
y' = h * sin (A1 + A2) 
```

À l’aide de l’ajout de l’ajout, les algorithmes précédents deviennent les suivants :

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

Les algorithmes de rotation d’un point donné pivotés par angle a2 peuvent être obtenus en remplaçant x pour chaque occurrence de (h \* cos a1) et en remplaçant y par chaque occurrence de (h \* Sin a1).

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



