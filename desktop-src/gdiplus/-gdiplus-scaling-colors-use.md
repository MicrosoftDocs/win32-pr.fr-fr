---
description: Une transformation de mise à l’échelle multiplie un ou plusieurs des quatre composants de couleur par un nombre. Les entrées de la matrice de couleurs qui représentent la mise à l’échelle sont indiquées dans le tableau suivant.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Mise à l’échelle des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370155306f7b1a177358d7cf28d329ebb0d75f8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196868"
---
# <a name="scaling-colors"></a>Mise à l’échelle des couleurs

Une transformation de mise à l’échelle multiplie un ou plusieurs des quatre composants de couleur par un nombre. Les entrées de la matrice de couleurs qui représentent la mise à l’échelle sont indiquées dans le tableau suivant.



| Composant à mettre à l’échelle | Entrée de la matrice |
|------------------------|--------------|
| Rouge                    | \[0 \] \[ 0\]   |
| Vert                  | \[1 \] \[ 1\]   |
| Blue                   | \[2 \] \[ 2\]   |
| Alpha                  | \[3 \] \[ 3\]   |



 

L’exemple suivant construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier ColorBars2.bmp. Ensuite, le code met à l’échelle le composant bleu de chaque pixel de l’image selon un facteur de 2. L’image d’origine est dessinée à côté de l’image transformée.


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



L’illustration suivante montre l’image d’origine à gauche et l’image mise à l’échelle à droite.

![Affiche quatre barres colorées, puis les mêmes barres avec des couleurs différentes.](images/colortrans3.png)

Le tableau suivant présente les vecteurs de couleur pour les quatre barres avant et après la mise à l’échelle bleue. Notez que le composant bleu de la quatrième barre de couleur est passé de 0,8 à 0,6. cela est dû au fait que GDI+ conserve uniquement la partie fractionnaire du résultat. Par exemple, (2) (0,8) = 1,6, et la partie fractionnaire de 1,6 est 0,6. Conserver uniquement la partie fractionnaire garantit que le résultat est toujours \[ compris entre 0 et 1 \] .



| Original           | Montée             |
|--------------------|--------------------|
| (0.4, 0.4, 0.4, 1) | (0.4, 0.4, 0.8, 1) |
| (0.4, 0.2, 0.2, 1) | (0.4, 0.2, 0.4, 1) |
| (0.2, 0.4, 0.2, 1) | (0.2, 0.4, 0.4, 1) |
| (0.4, 0.4, 0.8, 1) | (0.4, 0.4, 0.6, 1) |



 

L’exemple suivant construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier ColorBars2.bmp. Ensuite, le code met à l’échelle les composants rouge, vert et bleu de chaque pixel de l’image. Les composants rouges sont réduits de 25%, les composants verts sont réduits à 35 pour cent et les composants bleus sont réduits de 50%.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



L’illustration suivante montre l’image d’origine à gauche et l’image mise à l’échelle à droite.

![Illustration montrant quatre barres colorées, puis les barres avec des couleurs différentes](images/colortrans4.png)

Le tableau suivant présente les vecteurs de couleur pour les quatre barres avant et après la mise à l’échelle rouge, verte et bleue.



| Original           | Montée               |
|--------------------|----------------------|
| (0.6, 0.6, 0.6, 1) | (0.45, 0.39, 0.3, 1) |
| (0, 1, 1, 1)       | (0, 0.65, 0.5, 1)    |
| (1, 1, 0, 1)       | (0.75, 0.65, 0, 1)   |
| (1, 0, 1, 1)       | (0.75, 0, 0.5, 1)    |



 

 

 



