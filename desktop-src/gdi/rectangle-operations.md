---
description: La fonction SetRect crée un rectangle, la fonction CopyRect effectue une copie d’un rectangle donné et la fonction SetRectEmpty crée un rectangle vide.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Opérations de rectangle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318833"
---
# <a name="rectangle-operations"></a>Opérations de rectangle

La fonction [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) crée un rectangle, la fonction [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) effectue une copie d’un rectangle donné et la fonction [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) crée un rectangle vide. Un rectangle vide est un rectangle qui a une largeur égale à zéro, une hauteur de zéro, ou les deux. La fonction [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) détermine si un rectangle donné est vide. La fonction [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) détermine si deux rectangles sont identiques, c’est-à-dire s’ils ont les mêmes coordonnées.

La fonction [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) augmente ou diminue la largeur ou la hauteur d’un rectangle, ou les deux. Elle peut ajouter ou supprimer la largeur des deux extrémités du rectangle ; elle peut ajouter ou supprimer la hauteur à la fois du haut et du bas du rectangle.

La fonction [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) déplace un rectangle d’une quantité donnée. Il déplace le rectangle en ajoutant les valeurs x-amount, y-volume ou x et y indiquées aux coordonnées d’angle.

La fonction [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) détermine si un point donné se trouve dans un rectangle donné. Le point se trouve dans le rectangle s’il se trouve sur le côté gauche ou supérieur ou s’il est entièrement dans le rectangle. Le point n’est pas dans le rectangle s’il se trouve sur le côté droit ou inférieur.

La fonction [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) crée un nouveau rectangle qui est l’intersection de deux rectangles existants, comme indiqué dans l’illustration suivante.

![Illustration montrant deux rectangles qui se chevauchent, avec un ombrage plus sombre pour indiquer l’intersection ](images/csrec-01.png)

La fonction [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) crée un nouveau rectangle qui est l’Union de deux rectangles existants, comme indiqué dans l’illustration suivante.

![illustration de deux rectangles qui se chevauchent, avec un ombrage plus sombre indiquant les zones de l’Union, mais pas dans les deux rectangles](images/csrec-02.png)

Pour plus d’informations sur les fonctions qui dessinent des ellipses et des polygones, consultez [remplissage de formes](filled-shapes.md).

 

 



