---
description: Quand vous dessinez une ligne, vous devez passer l’adresse d’un objet Pen à la méthode DrawLine de la classe Graphics.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Dessin de lignes opaques et semi-transparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f751e5808440c1051b3cd996f7ebcb2df0ccbcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556407"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a>Dessin de lignes opaques et semi-transparentes

Quand vous dessinez une ligne, vous devez passer l’adresse d’un objet [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) à la méthode [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . L’un des paramètres du constructeur **Pen** est un objet [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Pour dessiner une ligne opaque, affectez au composant alpha de la couleur la valeur 255. Pour dessiner une ligne translucide, affectez au composant alpha n'importe quelle valeur comprise entre 1 et 254.

Quand vous dessinez une ligne translucide sur un arrière-plan, la couleur de la ligne est fusionnée avec les couleurs de l'arrière-plan. Le composant alpha spécifie la manière dont les couleurs de ligne et d’arrière-plan sont mélangées ; les valeurs alpha proches de 0 placent plus de poids sur les couleurs d’arrière-plan, tandis que les valeurs alpha proches de 255 placent plus peser sur la couleur de ligne.

L’exemple suivant dessine une image, puis dessine trois lignes qui utilisent l’image comme arrière-plan. La première ligne utilise un composant alpha de 255. Elle est donc opaque. Les deuxième et troisième lignes utilisent un composant alpha de 128 et sont donc translucides. Vous pouvez voir l'image d'arrière-plan sur les lignes. L’appel à [**Graphics :: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) fait en sorte que la fusion pour la troisième ligne soit effectuée conjointement avec la correction gamma.


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



L’illustration suivante montre la sortie du code précédent.

![Illustration montrant une image superposée par trois traits larges : un opaque, un léger et un peu transparent](images/compqualline.png)

 

 



