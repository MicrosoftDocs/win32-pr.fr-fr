---
description: Un polygone est une figure fermée avec au moins trois côtés droits.
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: Polygones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf1f8a2b9b3ce30ceadb22a0832ec50fed98c87eba961081760e5a966932e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036457"
---
# <a name="polygons"></a>Polygones

Un polygone est une figure fermée avec au moins trois côtés droits. Par exemple, un triangle est un polygone avec trois côtés, un rectangle est un polygone avec quatre côtés et un pentagone est un polygone avec cinq côtés. L’illustration suivante montre plusieurs polygones.

![Illustration montrant cinq polygones de différentes formes, tailles et couleurs](images/aboutgdip02-art07.png)

Pour dessiner un polygone, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) et d’un tableau d’objets [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (ou [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)). L’objet **Graphics** fournit la méthode [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) . L’objet **Pen** stocke les attributs du polygone, tels que la largeur et la couleur de ligne, et le tableau d’objets **point** stocke les points à connecter par des lignes droites. Les adresses de l’objet **Pen** et le tableau d’objets **point** sont passés comme arguments à la méthode DrawPolygon. L’exemple suivant dessine un polygone à trois côtés. Notez qu’il n’y a que trois points dans **myPointArray**: (0, 0), (50, 30) et (30, 60). La méthode DrawPolygon ferme automatiquement le polygone en dessinant une ligne de (30, 60) au point de départ (0,0);


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



L’illustration suivante montre le polygone.

![Illustration montrant un triangle par rapport aux axes de coordonnées](images/aboutgdip02-art08.png)

 

 



