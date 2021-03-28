---
description: 'Windows GDI+ utilise trois espaces de coordonnées : World, page et Device.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Types de systèmes de coordonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05908196662918eb93f4fa6e2b356a6989ed5a58
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104550117"
---
# <a name="types-of-coordinate-systems"></a>Types de systèmes de coordonnées

Windows GDI+ utilise trois espaces de coordonnées : World, page et Device. Lorsque vous effectuez l’appel `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , les points que vous transmettez à la méthode [**Graphics ::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) , (0,0) et (160, 80), se trouvent dans l’espace de coordonnées universel. Avant que GDI+ puisse dessiner la ligne sur l’écran, les coordonnées passent par une séquence de transformations. Une transformation convertit les coordonnées universelles en coordonnées de page et une autre transformation convertit les coordonnées de page en coordonnées de périphérique.

Supposons que vous souhaitiez utiliser un système de coordonnées dont l’origine se trouve dans le corps de la zone cliente plutôt que dans le coin supérieur gauche. Par exemple, imaginons que vous souhaitiez que l’origine soit de 100 pixels du bord gauche de la zone cliente et de 50 pixels en haut de la zone cliente. L’illustration suivante montre un tel système de coordonnées.

![capture d’écran d’une fenêtre contenant des axes de coordonnées étiquetés](images/aboutgdip05-art01.png)

Lorsque vous effectuez l’appel `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , vous recevez la ligne indiquée dans l’illustration suivante.

![capture d’écran de la fenêtre précédente, mais avec une ligne bleue qui s’étend en diagonale à partir de l’origine](images/aboutgdip05-art02.png)

Les coordonnées des points de terminaison de votre ligne dans les trois espaces de coordonnées sont les suivantes :



|        |                         |
|--------|-------------------------|
| World (Monde)  | (0, 0) à (160, 80)     |
| Page   | (100, 50) vers (260, 130) |
| Appareil | (100, 50) vers (260, 130) |



 

Notez que l’espace de coordonnées de la page a son origine dans l’angle supérieur gauche de la zone cliente. ce sera toujours le cas. Notez également que, étant donné que l’unité de mesure est le pixel, les coordonnées de l’appareil sont les mêmes que les coordonnées de la page. Si vous définissez l’unité de mesure sur une valeur autre que les pixels (par exemple, pouces), les coordonnées de l’appareil seront différentes des coordonnées de la page.

La transformation qui mappe les coordonnées universelles aux coordonnées de la page est appelée *transformation universelle* et est conservée par un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Dans l’exemple précédent, la transformation universelle est une translation de 100 unités sur la direction x et de 50 unités sur l’axe y. L’exemple suivant définit la transformation universelle d’un objet **Graphics** , puis utilise cet objet **Graphics** pour dessiner la ligne indiquée dans la figure précédente.


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



La transformation qui mappe les coordonnées de page aux coordonnées de l’appareil est appelée *transformation de page*. La classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fournit quatre méthodes pour la manipulation et l’inspection de la transformation de page : [**Graphics :: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics :: GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics :: SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)et [**Graphics :: GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale). La classe **Graphics** fournit également deux méthodes, [**Graphics :: GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) et [**Graphics :: GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), pour l’examen des points horizontaux et verticaux par pouce du périphérique d’affichage.

Vous pouvez utiliser la méthode [**Graphics :: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pour spécifier une unité de mesure. L’exemple suivant dessine une ligne de (0,0) à (2,3) où le point (2, 1) est de 2 pouces à droite et de 1 pouce en dessous du point (0, 0).


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> Si vous ne spécifiez pas de largeur du stylet lorsque vous construisez votre stylet, l’exemple précédent dessine une ligne d’une largeur d’un pouce. Vous pouvez spécifier la largeur du stylet dans le deuxième argument du constructeur [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) :
> <br/><br/>
> `Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.

 

Si nous supposons que le périphérique d’affichage a 96 points par pouce dans la direction horizontale et 96 points par pouce dans la direction verticale, les points de terminaison de la ligne de l’exemple précédent ont les coordonnées suivantes dans les trois espaces de coordonnées :



|        |                     |
|--------|---------------------|
| World (Monde)  | (0, 0) à (2, 1)    |
| Page   | (0, 0) à (2, 1)    |
| Appareil | (0,0, to (192, 96) |



 

Vous pouvez combiner les transformations universelles et de page pour obtenir un grand nombre d’effets. Par exemple, supposons que vous souhaitiez utiliser des pouces comme unité de mesure et que vous souhaitez que l’origine de votre système de coordonnées soit de 2 pouces à partir du bord gauche de la zone cliente et de 1/2 centimètres à partir du haut de la zone cliente. L’exemple suivant définit les transformations universelles et de page d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , puis dessine une ligne comprise entre (0,0) et (2, 1).


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



L’illustration suivante montre la ligne et le système de coordonnées.

![capture d’écran de la fenêtre précédente, mais plus grande, avec les axes positionnés à gauche et libellés différemment](images/aboutgdip05-art03.png)

Si nous supposons que le périphérique d’affichage a 96 points par pouce dans la direction horizontale et 96 points par pouce dans la direction verticale, les points de terminaison de la ligne de l’exemple précédent ont les coordonnées suivantes dans les trois espaces de coordonnées :



|        |                         |
|--------|-------------------------|
| World (Monde)  | (0, 0) à (2, 1)        |
| Page   | (2, 0,5) à (4, 1,5)    |
| Appareil | (192, 48) vers (384, 144) |



 

 

 
