---
description: 'Il peut arriver que vous souhaitiez créer une image bitmap hors écran qui présente les caractéristiques suivantes :'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Utilisation du mode de composition pour contrôler la fusion alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414290"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a>Utilisation du mode de composition pour contrôler la fusion alpha

Il peut arriver que vous souhaitiez créer une image bitmap hors écran qui présente les caractéristiques suivantes :

-   Les couleurs ont des valeurs alpha inférieures à 255.
-   Les couleurs ne sont pas fusionnées entre elles lorsque vous créez l’image bitmap.
-   Lorsque vous affichez la bitmap terminée, les couleurs de la bitmap sont fusionnées alpha avec les couleurs d’arrière-plan sur le périphérique d’affichage.

Pour créer une telle image bitmap, construisez un objet [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) vide, puis construisez un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basé sur cette image bitmap. Définissez le mode de composition de l’objet **Graphics** sur CompositingModeSourceCopy.

L’exemple suivant crée un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basé sur un objet [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . Le code utilise l’objet **Graphics** avec deux pinceaux translucides (alpha = 160) pour peindre sur l’image bitmap. Le code remplit une ellipse rouge et une ellipse verte à l’aide des pinceaux translucides. L’ellipse verte chevauche l’ellipse rouge, mais le vert n’est pas mélangé au rouge, car le mode de composition de l’objet **Graphics** est défini sur CompositingModeSourceCopy.

Ensuite, le code se prépare à dessiner à l’écran en appelant [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) et en créant un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basé sur un contexte de périphérique. Le code dessine le bitmap à l’écran deux fois : une fois sur un arrière-plan blanc et une fois sur un arrière-plan multicolore. Les pixels de l’image bitmap qui font partie des deux points de suspension ont un composant alpha de 160, de sorte que les points de suspension sont fusionnés avec les couleurs d’arrière-plan de l’écran.


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



L’illustration suivante montre la sortie du code précédent. Notez que les ellipses sont fusionnées avec l’arrière-plan, mais elles ne sont pas fusionnées les unes avec les autres.

![Illustration montrant deux ellipses de couleur différente, chacune d’entre elles fondue avec son arrière-plan multicolore](images/sourcecopy.png)

L’exemple de code précédent contient l’instruction suivante :


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



Si vous souhaitez que les ellipses soient fusionnées les unes avec les autres, et avec l’arrière-plan, remplacez cette instruction par ce qui suit :


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



L’illustration suivante montre la sortie du code modifié.

![utilisation du mode de composition pour contrôler l’illustration de la fusion alpha](images/sourceover.png)

 

 



