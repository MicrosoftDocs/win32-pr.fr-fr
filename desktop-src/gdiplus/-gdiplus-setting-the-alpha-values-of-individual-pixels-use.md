---
description: La rubrique utilisation d’une matrice de couleurs pour définir des valeurs alpha dans des images montre une méthode non destructrice permettant de modifier les valeurs alpha d’une image.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Définition des valeurs alpha de pixels individuels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c88c7ef8cc343b99f7a50c3fad012b62ef2a8d79ab38de6988efb6b5643e0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830729"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a>Définition des valeurs alpha de pixels individuels

La rubrique [utilisation d’une matrice de couleurs pour définir des valeurs alpha dans des images](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) montre une méthode non destructrice permettant de modifier les valeurs alpha d’une image. L’exemple de cette rubrique affiche une image semitransparently, mais les données de pixels de la bitmap ne sont pas modifiées. Les valeurs alpha sont modifiées uniquement pendant le rendu.

L’exemple suivant montre comment modifier les valeurs alpha de pixels individuels. Le code de l’exemple modifie en fait les informations alpha dans un objet [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . L’approche est beaucoup plus lente que l’utilisation d’une matrice de couleurs et d’un objet [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , mais elle vous permet de contrôler les pixels individuels dans l’image bitmap.


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



L’illustration suivante montre l’image résultante.

![Illustration montrant une image qui devient plus opaque de gauche à droite, sur un rectangle noir](images/image3.png)

L’exemple de code précédent utilise des boucles imbriquées pour modifier la valeur alpha de chaque pixel de la bitmap. Pour chaque pixel, [**bitmap :: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) obtient la couleur existante, [**Color :: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) crée une couleur temporaire qui contient la nouvelle valeur alpha, puis [**bitmap :: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) définit la nouvelle couleur. La valeur alpha est définie en fonction de la colonne de l’image bitmap. Dans la première colonne, alpha a la valeur 0. Dans la dernière colonne, alpha a la valeur 255. Par conséquent, l’image résultante passe d’une transparence totale (sur le bord gauche) à une image entièrement opaque (sur le bord droit).

[**Bitmap :: GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) et [**bitmap :: SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) vous permettent de contrôler les valeurs de pixel individuelles. Toutefois, l’utilisation de **bitmap :: GetPixel** et **bitmap :: SetPixel** n’est pas aussi rapide que l’utilisation de la classe [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) et de la structure [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .

 

 



