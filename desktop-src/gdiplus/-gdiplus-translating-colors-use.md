---
description: Une traduction ajoute une valeur à un ou plusieurs des quatre composants de couleur. Les entrées de la matrice de couleurs qui représentent des traductions sont indiquées dans le tableau suivant.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Conversion des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608a0653423d854e6d77bd624949f24ec03cce6c4ed063d4c740dd142b1dfb3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036337"
---
# <a name="translating-colors"></a>Conversion des couleurs

Une traduction ajoute une valeur à un ou plusieurs des quatre composants de couleur. Les entrées de la matrice de couleurs qui représentent des traductions sont indiquées dans le tableau suivant.



| Composant à traduire | Entrée de la matrice |
|----------------------------|--------------|
| Rouge                        | \[4 \] \[ 0\]   |
| Vert                      | \[4 \] \[ 1\]   |
| Bleu                       | \[4 \] \[ 2\]   |
| Alpha                      | \[4 \] \[ 3\]   |



 

L’exemple suivant construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier ColorBars.bmp. Le code ajoute ensuite 0,75 au composant rouge de chaque pixel de l’image. L’image d’origine est dessinée à côté de l’image transformée.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



L’illustration suivante montre l’image d’origine à gauche et l’image transformée à droite.

![Illustration montrant quatre barres de couleur, puis les mêmes barres avec des couleurs différentes](images/colortrans2.png)

Le tableau suivant répertorie les vecteurs de couleur pour les quatre barres avant et après la translation rouge. Notez que, étant donné que la valeur maximale d’un composant de couleur est 1, le composant rouge de la deuxième ligne ne change pas. (De même, la valeur minimale d’un composant de couleur est 0.)



| Original           | Traduit      |
|--------------------|-----------------|
| Noir (0, 0, 0, 1) | (0.75, 0, 0, 1) |
| Rouge (1, 0, 0, 1)   | (1, 0, 0, 1)    |
| Vert (0, 1, 0, 1) | (0.75, 1, 0, 1) |
| Bleu (0, 0, 1, 1)  | (0.75, 0, 1, 1) |



 

 

 



