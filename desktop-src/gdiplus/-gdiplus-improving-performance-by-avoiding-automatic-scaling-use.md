---
description: Si vous transmettez uniquement l’angle supérieur gauche d’une image à la méthode DrawImage, Windows GDI+ peut mettre à l’échelle l’image, ce qui réduit les performances.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Amélioration des performances en évitant la mise à l’échelle automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972875"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a>Amélioration des performances en évitant la mise à l’échelle automatique

Si vous transmettez uniquement l’angle supérieur gauche d’une image à la méthode **DrawImage** , Windows GDI+ peut mettre à l’échelle l’image, ce qui réduit les performances.

L’appel suivant à la méthode **DrawImage** spécifie un angle supérieur gauche de (50, 30), mais ne spécifie pas de rectangle de destination :


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



Bien qu’il s’agisse de la version la plus simple de la méthode **DrawImage** en ce qui concerne le nombre d’arguments requis, elle n’est pas nécessairement la plus efficace. Si le nombre de points par pouce sur le périphérique d’affichage actuel est différent du nombre de points par pouce sur le périphérique où l’image a été créée, GDI+ met à l’échelle l’image afin que sa taille physique sur le périphérique d’affichage actuel soit aussi proche que possible de sa taille physique sur l’appareil où elle a été créée.

Si vous souhaitez empêcher une telle mise à l’échelle, transmettez la largeur et la hauteur d’un rectangle de destination à la méthode **DrawImage** . L’exemple suivant dessine la même image deux fois. Dans le premier cas, la largeur et la hauteur du rectangle de destination ne sont pas spécifiées, et l’image est mise à l’échelle automatiquement. Dans le deuxième cas, la largeur et la hauteur (mesurées en pixels) du rectangle de destination sont spécifiées comme étant identiques à la largeur et à la hauteur de l’image d’origine.


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



L’illustration suivante montre l’image rendue deux fois.

![capture d’écran d’une fenêtre qui contient deux versions d’une image à des échelles différentes](images/scaledtexture1.png)

 

 



