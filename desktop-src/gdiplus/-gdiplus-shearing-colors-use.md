---
description: L’inclinaison augmente ou diminue un composant de couleur d’un montant proportionnel à un autre composant de couleur.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Cisaillement des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413136"
---
# <a name="shearing-colors"></a>Cisaillement des couleurs

L’inclinaison augmente ou diminue un composant de couleur d’un montant proportionnel à un autre composant de couleur. Par exemple, considérez la transformation dans laquelle le composant rouge augmente d’une moitié la valeur du composant bleu. Dans une telle transformation, la couleur (0,2, 0,5, 1) devient (0,7, 0,5, 1). Le nouveau composant rouge est 0,2 + (1/2) (1) = 0,7.

L’exemple suivant construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier ColorBars4.bmp. Ensuite, le code applique la transformation d’inclinaison décrite dans le paragraphe précédent à chaque pixel de l’image.


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
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



L’illustration suivante montre l’image d’origine à gauche et l’image déformée à droite.

![Illustration montrant quatre barres de couleur, puis les mêmes barres avec des couleurs différentes](images/colortrans6.png)

Le tableau suivant présente les vecteurs de couleur pour les quatre barres avant et après la transformation d’inclinaison.



| Original           | En cisaille            |
|--------------------|--------------------|
| (0, 0, 1, 1)       | (0.5, 0, 1, 1)     |
| (0.5, 1, 0.5, 1)   | (0.75, 1, 0.5, 1)  |
| (1, 1, 0, 1)       | (1, 1, 0, 1)       |
| (0.4, 0.4, 0.4, 1) | (0.6, 0.4, 0.4, 1) |



 

 

 



