---
description: Une figure fermée, telle qu’un rectangle ou une ellipse, se compose d’un plan et d’un intérieur.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Pinceaux et formes remplies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566200"
---
# <a name="brushes-and-filled-shapes"></a>Pinceaux et formes remplies

Une figure fermée, telle qu’un rectangle ou une ellipse, se compose d’un plan et d’un intérieur. Le contour est dessiné à l’aide d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) et l’intérieur est rempli d’un objet [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) . Windows GDI+ fournit plusieurs classes Brush pour remplir l’intérieur des figures fermées : [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)et [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush). Toutes ces classes héritent de la classe **Brush** . L’illustration suivante montre un rectangle rempli d’un pinceau plein et une Ellipse remplie avec un pinceau hachuré.

![Illustration montrant un rectangle bleu et une ellipse magenta remplie d’un motif hachuré bleu](images/aboutgdip02-art17.png)

 

-   [Pinceaux solides](#solid-brushes)
-   [Pinceaux hachuré](#hatch-brushes)
-   [Pinceaux de texture](#texture-brushes)
-   [Pinceaux de dégradé](#gradient-brushes)

## <a name="solid-brushes"></a>Pinceaux solides

Pour remplir une forme fermée, vous avez besoin d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et d’un objet [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) . L’objet **Graphics** fournit des méthodes, telles que [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) et [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), et l’objet **Brush** stocke les attributs du remplissage, tels que la couleur et le motif. L’adresse de l’objet **Brush** est passée comme l’un des arguments à la méthode Fill. L’exemple suivant remplit une ellipse avec une couleur rouge unie.


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



Notez que dans l’exemple précédent, le pinceau est de type [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), qui hérite de [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).

## <a name="hatch-brushes"></a>Pinceaux hachuré

Lorsque vous remplissez une forme avec un pinceau hachuré, vous spécifiez une couleur de premier plan, une couleur d’arrière-plan et un style de hachurage. La couleur de premier plan est la couleur de la hachure.


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



GDI+ fournit plus de 50 styles de hachures, spécifiés dans [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle). Les trois styles indiqués dans l’illustration suivante sont horizontal, ForwardDiagonal et Cross.

![Illustration montrant trois ellipses colorées en bleu, chacune avec un style de hachurage différent](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a>Pinceaux de texture

Avec un pinceau de texture, vous pouvez remplir une forme à l’aide d’un modèle stocké dans une bitmap. Par exemple, supposons que l’image suivante soit stockée dans un fichier sur disque nommé MyTexture.bmp.

![capture d’écran d’un petit carré rempli avec différentes couleurs](images/aboutgdip02-art19.png)

L’exemple suivant remplit une ellipse en répétant l’image stockée dans MyTexture.bmp.


```
Image myImage(L"MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



L’illustration suivante montre l’Ellipse remplie.

![Illustration montrant une Ellipse remplie avec le modèle défini précédemment](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a>Pinceaux de dégradé

Vous pouvez utiliser un pinceau de dégradé pour remplir une forme avec une couleur qui change progressivement d’une partie de la forme à une autre. Par exemple, un pinceau de dégradé horizontal change de couleur lorsque vous passez du côté gauche d’une figure à droite. L’exemple suivant remplit une ellipse avec un pinceau de dégradé horizontal qui passe du bleu au vert lorsque vous vous déplacez du côté gauche de l’ellipse vers le côté droit.


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



L’illustration suivante montre l’Ellipse remplie.

![Illustration montrant une ellipse avec un dégradé : bleu à droite au vert à gauche](images/aboutgdip02-art21.png)

Vous pouvez configurer un pinceau de dégradé de tracé pour modifier la couleur au fur et à mesure que vous déplacez du centre d’une figure vers la limite.

![Ilustration d’une ellipse en bleu foncé au centre, en l’ombrage du bleu clair à la périphérie](images/aboutgdip02-art22.png)

Les pinceaux de dégradé de tracés sont relativement flexibles. Le pinceau de dégradé utilisé pour remplir le triangle dans l’illustration suivante change progressivement du rouge au centre de trois couleurs différentes aux sommets.

![illustration d’un triangle rouge au centre, en l’ombrage d’une couleur différente à chaque vertex](images/aboutgdip02-art23.png)

 

 



