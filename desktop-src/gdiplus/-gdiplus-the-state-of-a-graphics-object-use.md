---
description: La classe Graphics est au cœur de Windows GDI+. Pour dessiner tout, vous créez un objet Graphics, définissez ses propriétés et appelez ses méthodes (DrawLine, DrawImage, DrawString et like).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: État d’un objet Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661733f944b08633b5df84eed3ac488e612d9e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569792"
---
# <a name="the-state-of-a-graphics-object"></a>État d’un objet Graphics

La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) est au cœur de Windows GDI+. Pour dessiner tout, vous créez un objet **Graphics** , définissez ses propriétés et appelez ses méthodes ( [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))et like).

L’exemple suivant construit un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , puis appelle la méthode [**Graphics ::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) de l’objet **Graphics** :


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



Dans le code précédent, la méthode [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) retourne un handle vers un contexte de périphérique (Device Context) et ce handle est passé au constructeur [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Un contexte de périphérique est une structure (gérée par Windows) qui contient des informations sur le périphérique d’affichage en cours d’utilisation.

## <a name="graphics-state"></a>État graphique

Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fait plus que fournir des méthodes de dessin, telles que [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) et [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)). Un objet **Graphics** conserve également l’État Graphics, qui peut être divisé selon les catégories suivantes :

-   Lien vers un contexte de périphérique (Device Context)
-   Paramètres de qualité
-   Transformations
-   Une zone de découpage

### <a name="device-context"></a>Contexte de périphérique

En tant que programmeur d’applications, vous n’êtes pas obligé de réfléchir à l’interaction entre un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) et son contexte de périphérique. Cette interaction est gérée par GDI+ en arrière-plan.

### <a name="quality-settings"></a>Paramètres de qualité

Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a plusieurs propriétés qui influencent la qualité des éléments qui sont dessinés à l’écran. Vous pouvez afficher et manipuler ces propriétés en appelant les méthodes obtenir et définir. Par exemple, vous pouvez appeler la méthode [**Graphics :: SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) pour spécifier le type d’anticrénelage (le cas échéant) appliqué au texte. Les autres méthodes Set qui influencent la qualité sont [**Graphics :: SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics :: SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics :: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)et [**Graphics :: SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).

L’exemple suivant dessine deux ellipses, l’une avec le mode de lissage défini sur [* * * * SmoothingModeAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) * * et l’autre avec le mode de lissage défini sur [* * * * SmoothingModeHighSpeed * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* * :


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a>Transformations

Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) gère deux transformations (World et page) qui sont appliquées à tous les éléments dessinés par cet objet **Graphics** . Toute transformation affine peut être stockée dans la transformation universelle. Les transformations affines incluent la mise à l’échelle, la rotation, la réflexion, l’inclinaison et la translation. La transformation de page peut être utilisée pour la mise à l’échelle et pour changer d’unités (par exemple, les pixels en pouces). Pour plus d’informations sur les transformations, consultez [systèmes de coordonnées et transformations](-gdiplus-coordinate-systems-and-transformations-about.md).

L’exemple suivant définit les transformations universelles et de page d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . La transformation universelle est définie sur une rotation de 30 degrés. La transformation de page est définie de façon à ce que les coordonnées passées au deuxième [**graphique ::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) soient considérées comme des millimètres au lieu de pixels. Le code effectue deux appels identiques à la méthode **Graphics ::D rawellipse** . La transformation universelle est appliquée au premier **graphique ::D appel rawellipse** , et les deux transformations (World et page) sont appliquées au second **graphics ::D appel rawellipse** .


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



L’illustration suivante montre les deux points de suspension. Notez que la rotation à 30 degrés concerne l’origine du système de coordonnées (l’angle supérieur gauche de la zone cliente), pas les centres des points de suspension. Notez également que la largeur du stylet 1 signifie 1 pixel pour la première ellipse et 1 millimètre pour la deuxième ellipse.

![capture d’écran d’une fenêtre contenant une ellipse petite, fine et épaisse](images/graphicsascon1.png)

 

### <a name="clipping-region"></a>Zone de découpage

Un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) gère une zone de découpage qui s’applique à tous les éléments dessinés par cet objet **Graphics** . Vous pouvez définir la région de découpage en appelant la méthode [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) .

L’exemple suivant crée une région en forme de plus en formant l’Union de deux rectangles. Cette région est désignée comme zone de découpage d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Ensuite, le code dessine deux lignes qui sont limitées à l’intérieur de la zone de découpage.


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



L’illustration suivante montre les lignes écrêtées.

![Illustration montrant une forme de couleur franchie de deux lignes rouges diagonales](images/graphicsascon2.png)

 

 
