---
description: Certaines applications traduisent (ou décalent) des objets dessinés dans la zone cliente.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Traduction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987777"
---
# <a name="translation"></a>Traduction

Certaines applications traduisent (ou décalent) des objets dessinés dans la zone cliente. en appelant la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour définir l’espace universel approprié sur la transformation d’espace de page. La fonction SetWorldTransform reçoit un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) contenant les valeurs appropriées. Les membres eDx et eDy de XFORM spécifient respectivement les composants de traduction horizontale et verticale.

En cas de *traduction* , chaque point d’un objet est décalé verticalement, horizontalement, ou les deux, selon une valeur spécifiée. L’illustration suivante montre un rectangle de 20 par 20 qui a été traduit à droite de 10 unités lorsqu’il est copié à partir d’un espace de coordonnées universelles vers l’espace de coordonnées de page.

![Illustration montrant un rectangle à une position dans l’espace universel et à une autre position dans l’espace de la page](images/cstrn-09.png)

Dans l’illustration précédente, la coordonnée x de chaque point du rectangle est égale à 10 unités supérieures à la coordonnée x d’origine.

La traduction horizontale peut être représentée par l’algorithme suivant.

``` syntax
x' = x + Dx 
```

Où x correspond à la nouvelle coordonnée x, x correspond à la coordonnée x d’origine et DX à la distance horizontale déplacée.

La traduction verticale peut être représentée par l’algorithme suivant.

``` syntax
y' = y + Dy 
```

Où y est la nouvelle coordonnée y, y est la coordonnée y d’origine et dy la distance verticale déplacée.

Les transformations de translation horizontale et verticale peuvent être combinées en une seule opération à l’aide d’une matrice 3 par 3.

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

(Règles d’état de la multiplication de matrice selon lesquelles le nombre de lignes dans une matrice doit être égal au nombre de colonnes dans l’autre. L’entier 1 dans la matrice \| x y 1 \| est un espace réservé qui a été ajouté pour répondre à cette exigence.)

La matrice 3-par-3 qui a produit la transformation de traduction illustrée contient les valeurs suivantes.

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



