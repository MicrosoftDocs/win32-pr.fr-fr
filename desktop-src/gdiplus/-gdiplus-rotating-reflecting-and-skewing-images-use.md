---
description: Vous pouvez faire pivoter, réfléchir et incliner une image en spécifiant des points de destination pour les angles supérieur gauche, supérieur droit et inférieur gauche de l’image d’origine.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Rotation, réflexion et inclinaison des images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951694"
---
# <a name="rotating-reflecting-and-skewing-images"></a>Rotation, réflexion et inclinaison des images

Vous pouvez faire pivoter, réfléchir et incliner une image en spécifiant des points de destination pour les angles supérieur gauche, supérieur droit et inférieur gauche de l’image d’origine. Les trois points de destination déterminent une transformation affine qui mappe l’image rectangulaire d’origine à un parallélogramme. (Le coin inférieur droit de l’image d’origine est mappé au quatrième angle du parallélogramme, qui est calculé à partir des trois points de destination spécifiés.)

Supposons, par exemple, que l’image d’origine soit un rectangle avec l’angle supérieur gauche à (0, 0), le coin supérieur droit à (100, 0) et l’angle inférieur gauche à (0, 50). Supposons à présent que nous puissions mapper ces trois points aux points de destination comme suit.



| Point d’origine       | Point de destination |
|----------------------|-------------------|
| En haut à gauche (0, 0)    | (200, 20)         |
| En haut à droite (100, 0) | (110, 100)        |
| En bas à gauche (0, 50)   | (250, 30)         |



 

L’illustration suivante montre l’image d’origine et l’image mappée au parallélogramme. L’image d’origine a été inclinée, reflétée, pivotée et traduite. L’axe des x le long du bord supérieur de l’image d’origine est mappé à la ligne qui s’exécute via (200, 20) et (110, 100). L’axe des y, le long du bord gauche de l’image d’origine, est mappé à la ligne qui s’exécute via (200, 20) et (250, 30).

![Illustration montrant des bandes colorées à l’origine des axes de coordonnées et les mêmes rayures inclinées et à un emplacement, une rotation et une taille différents](images/stripes1.png)

L’exemple suivant produit les images illustrées dans l’illustration précédente.


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



L’illustration suivante montre une transformation similaire appliquée à une image photographique.

![Illustration montrant deux fois la même photo ; la seconde est inversée, inclinée et a une taille, une rotation et un emplacement différents](images/transformedclimber.png)

L’illustration suivante montre une transformation similaire appliquée à un métafichier.

![Illustration montrant des formes et du texte, puis de nouveau mais inversée, inclinée et avec un emplacement, une rotation et une taille différents](images/transformedmetafile.png)

 

 



