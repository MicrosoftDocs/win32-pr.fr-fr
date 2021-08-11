---
description: Lorsque vous remplissez une forme, vous devez passer l’adresse d’un objet Brush à l’une des méthodes de remplissage de la classe Graphics.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Dessiner avec des pinceaux opaques et translucides
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce5bb89c460c9769f805fb33af9eb91e9d8207448e702476aff4d25dec33a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248873"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a>Dessiner avec des pinceaux opaques et translucides

Lorsque vous remplissez une forme, vous devez passer l’adresse d’un objet [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) à l’une des méthodes de remplissage de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Le paramètre un du constructeur [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) est un objet [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) . Pour remplir une forme opaque, affectez au composant alpha de la couleur la valeur 255. Pour remplir une forme translucide, affectez au composant alpha n'importe quelle valeur comprise entre 1 et 254.

Quand vous remplissez une forme translucide, la couleur de la forme est fusionnée avec les couleurs d'arrière-plan. Le composant alpha spécifie comment les couleurs de forme et d’arrière-plan sont mélangées. les valeurs alpha proches de 0 placent plus de poids sur les couleurs d’arrière-plan, tandis que les valeurs alpha proches de 255 placent plus peser sur la couleur de la forme.

L’exemple suivant dessine une image, puis remplit trois points de suspension qui chevauchent l’image. La première ellipse utilise un composant alpha de 255. Elle est donc opaque. Les deuxième et troisième ellipses utilisent un composant alpha de 128 et sont donc translucides. Vous pouvez voir l'image d'arrière-plan à travers les ellipses. L’appel à [**Graphics :: SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) fait en sorte que la fusion de la troisième ellipse soit effectuée conjointement avec la correction gamma.


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



L’illustration suivante montre la sortie du code précédent.

![Illustration montrant une image superposée par trois ellipses : une opaque, une légèrement transparente, une très transparente](images/compqualellipse.png)

 

 



