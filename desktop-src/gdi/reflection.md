---
description: Certaines applications fournissent des fonctionnalités qui reflètent (ou miroir) des objets dessinés dans la zone cliente.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Réflexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03d872273e7d0b9f23d9ffb31c6304c8b59b59eda80c7181802120f89c0d764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092699"
---
# <a name="reflection"></a>Réflexion

Certaines applications fournissent des fonctionnalités qui reflètent (ou miroir) des objets dessinés dans la zone cliente. Les applications qui contiennent des fonctionnalités de réflexion utilisent la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour définir les valeurs appropriées dans l’espace universel pour la transformation d’espace de page. Cette fonction reçoit un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) contenant les valeurs appropriées. Les membres eM11 et eM22 de XFORM spécifient respectivement les composants de réflexion horizontale et verticale.

La *transformation de réflexion* crée une image miroir d’un objet par rapport à l’axe x ou y. En résumé, la réflexion n’est qu’une mise à l’échelle négative. Pour produire une réflexion horizontale, les coordonnées x sont multipliées par 1. Pour produire une réflexion verticale, les coordonnées y sont multipliées par 1.

La réflexion horizontale peut être représentée par l’algorithme suivant :

``` syntax
x' = -x 
```

où x est la coordonnée x et x’est le résultat de la réflexion.

La matrice 2 par 2 qui a produit une réflexion horizontale contient les valeurs suivantes :

``` syntax
|-1    0| 
|0     1| 
```

La réflexion verticale peut être représentée par l’algorithme suivant :

``` syntax
y' = -y 
```

où y est la coordonnée y et y est le résultat de la réflexion.

La matrice 2-par-2 qui a produit la réflexion verticale contient les valeurs suivantes :

``` syntax
|1    0| 
|0   -1| 
```

Les opérations de réflexion horizontale et de réflexion verticale peuvent être combinées en une seule opération à l’aide de la matrice 2 par 2 suivante :

``` syntax
|-1    0| 
|0    -1| 
```

 

 



