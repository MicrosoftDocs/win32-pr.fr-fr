---
description: Au lieu de dessiner une ligne ou une courbe avec une couleur unie, vous pouvez dessiner avec une texture.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Dessin d’une ligne remplie d’une texture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cc8f93adee4792836c4166d5787e20d9c54040448d3a7efde36ff6a580d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467033"
---
# <a name="drawing-a-line-filled-with-a-texture"></a>Dessin d’une ligne remplie d’une texture

Au lieu de dessiner une ligne ou une courbe avec une couleur unie, vous pouvez dessiner avec une texture. Pour dessiner des lignes et des courbes avec une texture, créez un objet [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) et transmettez l’adresse de cet objet **TextureBrush** à un constructeur [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . L’image associée au pinceau de texture est utilisée pour juxtaposer le plan (de façon invisible) et, lorsque le stylet dessine une ligne ou une courbe, le trait du stylet dévoile certains pixels de la texture en mosaïque.

L’exemple suivant crée un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier Texture1.jpg. Cette image est utilisée pour construire un objet [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , et l’objet **TextureBrush** est utilisé pour construire un objet [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . L’appel à [**Graphics ::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) dessine l’image avec son coin supérieur gauche à (0,0). L’appel à [**Graphics ::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) utilise l’objet **Pen** pour dessiner une ellipse texturée.


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



L’illustration suivante montre l’image et l’ellipse texturée.

![Illustration montrant une petite image rectangulaire, puis un segment de ligne elliptique rempli avec l’image d’origine](images/pens7.png)

 

 
