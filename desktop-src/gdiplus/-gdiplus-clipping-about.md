---
description: Le découpage implique la restriction du dessin à une certaine région. L’illustration suivante montre la chaîne &\# 0034 ; Bonjour&\# 0034 ; ajusté à une région en forme de cœur.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Découpage (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57534c5934270374af356956285ad13838630666795d9f06a2623cbd3b453ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067633"
---
# <a name="clipping-gdi"></a>Découpage (GDI+)

Le découpage implique la restriction du dessin à une certaine région. L’illustration suivante montre la chaîne « Hello » découpée en une région en forme de cœur.

![Illustration montrant des parties de la chaîne « Hello » dans un cœur rouge](images/aboutgdip02-art30.png)

Les régions peuvent être construites à partir de chemins d’accès, et les chemins d’accès peuvent contenir des contours de chaînes, ce qui vous permet d’utiliser du texte avec contour pour le découpage. L’illustration suivante montre un ensemble de points de suspension concentriques tronqués à l’intérieur d’une chaîne de texte.

![Illustration montrant la chaîne « Hello » remplie par un modèle de cercles concentriques](images/aboutgdip02-art31.png)

Pour dessiner avec un découpage, créez un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , appelez sa méthode [SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) , puis appelez les méthodes de dessin de ce même objet **Graphics** . L’exemple suivant dessine une ligne découpée dans une zone rectangulaire.


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



L’illustration suivante montre la zone rectangulaire avec la ligne découpée.

![Illustration montrant un rectangle avec une ligne diagonale de haut en bas](images/aboutgdip02-art31a.png)

 

 



