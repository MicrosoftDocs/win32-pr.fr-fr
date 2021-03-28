---
description: La plupart des applications de CAO et de dessin fournissent des fonctionnalités qui permettent de mettre à l’échelle la sortie créée par l’utilisateur.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Mise à l'échelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973523"
---
# <a name="scaling"></a>Mise à l'échelle

La plupart des applications de CAO et de dessin fournissent des fonctionnalités qui permettent de mettre à l’échelle la sortie créée par l’utilisateur. Les applications qui incluent des fonctionnalités de mise à l’échelle (ou zoom) appellent la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour définir l’espace universel approprié sur la transformation d’espace de page. Cette fonction reçoit un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) contenant les valeurs appropriées. Les membres eM11 et eM22 de XFORM spécifient respectivement les composants de mise à l’échelle horizontale et verticale.

Lorsque la *mise à l’échelle* se produit, les lignes verticales et horizontales (ou les vecteurs) qui constituent un objet sont étirées ou compressées par rapport à l’axe x ou y. L’illustration suivante montre un rectangle de 20 par 20 mis à l’échelle verticalement jusqu’à deux fois sa hauteur d’origine lorsqu’il est copié à partir d’un espace de coordonnées universelles vers l’espace de coordonnées de page.

![Illustration montrant un petit rectangle dans l’espace universel et un plus haut dans l’espace de la page](images/cstrn-10.png)

Dans l’illustration précédente, les lignes verticales qui définissent la mesure latérale du rectangle d’origine sont 20 unités, tandis que les lignes verticales qui définissent les côtés du rectangle mis à l’échelle mesurent 40 unités.

La mise à l’échelle verticale peut être représentée par l’algorithme suivant.

``` syntax
y' = y * Dy 
```

Où y est la nouvelle longueur, y est la longueur d’origine et dy est le facteur d’échelle verticale.

La mise à l’échelle horizontale peut être représentée par l’algorithme suivant.

``` syntax
x' = x * Dx 
```

Où x est la nouvelle longueur, x est la longueur d’origine et DX le facteur de mise à l’échelle horizontale.

Les transformations de mise à l’échelle verticale et horizontale peuvent être combinées en une seule opération à l’aide d’une matrice 2 par 2.

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

La matrice 2-par-2 qui a produit la transformation de mise à l’échelle contient les valeurs suivantes.

``` syntax
|1    0| 
|0    2| 
```

 

 



