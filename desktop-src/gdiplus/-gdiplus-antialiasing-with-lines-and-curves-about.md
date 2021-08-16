---
description: lorsque vous utilisez Windows GDI+ pour dessiner une ligne, vous fournissez le point de départ et le point de fin de la ligne, mais vous n’avez pas besoin de fournir des informations sur les pixels individuels sur la ligne.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Anticrénelage avec des lignes et des courbes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d6fd1df9c8dca6bb600c723fa61cf14b99e53a51670768a7323ca33e12b9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117697108"
---
# <a name="antialiasing-with-lines-and-curves"></a>Anticrénelage avec des lignes et des courbes

lorsque vous utilisez Windows GDI+ pour dessiner une ligne, vous fournissez le point de départ et le point de fin de la ligne, mais vous n’avez pas besoin de fournir des informations sur les pixels individuels sur la ligne. GDI+ fonctionne conjointement avec le logiciel de pilote d’affichage pour déterminer les pixels qui seront activés pour afficher la ligne sur un périphérique d’affichage particulier.

Envisagez une ligne rouge droite qui va du point (4, 2) jusqu’au point (16, 10). Supposons que le système de coordonnées a son origine dans l’angle supérieur gauche et que l’unité de mesure est le pixel. Supposons également que l’axe des x pointe vers la droite et que l’axe des y pointe vers le dessous. L’illustration suivante montre une vue agrandie de la ligne rouge dessinée sur un arrière-plan multicolore.

![Illustration montrant des pixels rouges pleins sur un arrière-plan multicolore](images/aboutgdip02-art33.png)

Notez que les pixels rouges utilisés pour le rendu de la ligne sont opaques. Aucun pixel partiellement transparent n’est impliqué dans l’affichage de la ligne. Ce type de rendu de ligne donne une apparence irrégulière à la ligne, et la ligne ressemble à un peu comme un escalier. Cette technique de représentation d’une ligne avec un escalier est appelée crénelage. l’escalier est un alias pour la ligne théorique.

Une technique plus sophistiquée pour le rendu d’une ligne implique l’utilisation de pixels partiellement transparents avec des pixels rouges purs. Les pixels sont définis sur le rouge pur ou sur un mélange de rouge et de couleur d’arrière-plan en fonction de leur proximité sur la ligne. Ce type de rendu est appelé « anticrénelage » et produit une ligne que l’oeil humain perçoit comme plus lisse. L’illustration suivante montre comment certains pixels sont fusionnés avec l’arrière-plan pour produire une ligne avec un alias.

![Illustration montrant des pixels qui sont des nuances de rouge sur le même arrière-plan](images/aboutgdip02-art34.png)

L’anticrénelage (lissage) peut également être appliqué à des courbes. L’illustration suivante montre une vue agrandie d’une ellipse lissée.

![illustration d’une ellipse constituée de différentes nuances de pixels bleus sur un arrière-plan blanc](images/aboutgdip02-art35.png)

L’illustration suivante montre la même ellipse dans sa taille réelle, une fois sans anticrénelage et une fois avec l’anticrénelage.

![capture d’écran de deux ellipses : le premier avec anticrénelage apparaît correctement](images/aboutgdip02-art36.png)

Pour dessiner des lignes et des courbes qui utilisent l’anticrénelage, créez un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et transmettez *SmoothingModeAntiAlias* à sa méthode [**Graphics :: SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) . Appelez ensuite l’une des méthodes de dessin de ce même objet **Graphics** .


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



**SmoothingModeAntiAlias** est un élément de l’énumération [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) .

 

 



