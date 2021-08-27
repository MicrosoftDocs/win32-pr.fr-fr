---
description: Certaines applications fournissent des fonctionnalités qui déforment les objets dessinés dans la zone cliente.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Incliné
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32edb9484fd8bb2a9da15220b0acf39fd5c44c50091551205022c6458b50d4e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092629"
---
# <a name="shear"></a>Incliné

Certaines applications fournissent des fonctionnalités qui déforment les objets dessinés dans la zone cliente. Les applications qui utilisent les fonctionnalités de cisaillement utilisent la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour définir les valeurs appropriées dans l’espace universel pour la transformation d’espace de page. Cette fonction reçoit un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) contenant les valeurs appropriées. Les membres eM12 et eM21 de XFORM spécifient respectivement les constantes de proportionnalité horizontale et verticale.

Il existe deux composants de la *transformation d’inclinaison*. La première modifie les lignes verticales dans un objet. la seconde modifie les lignes horizontales. L’illustration suivante montre un rectangle 20 par 20 déformé horizontalement lorsqu’il est copié de l’espace universel vers l’espace de page.

![Illustration montrant un rectangle dans l’espace universel et un trapeziod dans l’espace de la page](images/cstrn-13.png)

Un cisaillement horizontal peut être représenté par l’algorithme suivant :

``` syntax
x' = x + (Sx * y) 
```

où x est la coordonnée d’origine x, SX est la constante de proportionnalité et x’est le résultat de la transformation d’inclinaison.

Une inclinaison verticale peut être représentée par l’algorithme suivant :

``` syntax
y' = y + (Sy * x) 
```

où y est la coordonnée y d’origine, SY est la constante de proportionnalité et y est le résultat de la transformation d’inclinaison.

Les transformations d’inclinaison horizontale et verticale peuvent être combinées en une seule opération à l’aide d’une matrice 2 par 2.

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

La matrice 2-par-2 qui a produit l’inclinaison contient les valeurs suivantes :

``` syntax
|1    1| 
|0    1| 
```

 

 



