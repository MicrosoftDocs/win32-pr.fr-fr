---
description: 'Une spline B&\# 233 ; la courbe est une courbe spécifiée par quatre points : deux points de terminaison (P1 et P2) et deux points de contrôle (C1 et C2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Splines de Bézier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115270"
---
# <a name="bezier-splines"></a>Splines de Bézier

Une spline de Bézier est une courbe spécifiée par quatre points : deux points de terminaison (P1 et P2) et deux points de contrôle (C1 et C2). La courbe commence à P1 et se termine à P2. La courbe ne traverse pas les points de contrôle, mais les points de contrôle agissent comme des aimants, en tirant la courbe dans certaines directions et en influençant le mode de courbure de la courbe. L’illustration suivante montre une courbe de Bézier avec ses points de terminaison et points de contrôle.

![Illustration montrant une spline de Bézier avec deux points de terminaison et deux points de contrôle](images/aboutgdip02-art11a.png)

Notez que la courbe commence à P1 et se déplace vers le point de contrôle C1. La ligne tangente à la courbe à l’instant P1 est la ligne dessinée de P1 à C1. Notez également que la ligne tangente au point de terminaison P2 est la ligne dessinée de C2 à P2.

Pour dessiner une spline de Bézier, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . L’objet **Graphics** fournit la méthode [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) , et l’objet **Pen** stocke les attributs de la courbe, tels que la largeur et la couleur de ligne. L’adresse de l’objet **Pen** est passée comme l’un des arguments à la méthode DrawBezier. Les arguments restants passés à la méthode DrawBezier sont les points de terminaison et les points de contrôle. L’exemple suivant dessine une spline de Bézier avec le point de départ (0, 0), les points de contrôle (40, 20) et (80, 150) et le point de fin (100, 10).


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



L’illustration suivante montre la courbe, les points de contrôle et deux lignes tangentes.

![Illustration montrant une spline de Bézier avec deux points de terminaison, deux points de contrôle et deux lignes tangentes](images/aboutgdip02-art12.png)

Les splines de Bézier ont été développées à l’origine par Pierre Bézier pour la conception dans le secteur de l’automobile. Ils ont, depuis, prouvé qu’ils sont très utiles dans de nombreux types de conception assistée par ordinateur et sont également utilisés pour définir les contours de polices. Les splines de Bézier peuvent générer une grande variété de formes, dont certaines sont présentées dans l’illustration suivante.

![Illustration montrant trois splines de Bézier](images/aboutgdip02-art13.png)

 

 



