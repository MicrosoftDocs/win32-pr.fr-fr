---
description: La classe Bitmap (qui hérite de la classe image) et la classe ImageAttributes fournissent des fonctionnalités permettant d’obtenir et de définir des valeurs de pixel.
ms.assetid: e3d67431-6098-4b2a-8910-5695a8473216
title: Utilisation d’une matrice de couleurs pour définir des valeurs alpha dans des images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81180b1f09b11e37b322e37106dab1879a00bbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526061"
---
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a>Utilisation d’une matrice de couleurs pour définir des valeurs alpha dans des images

La classe [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) (qui hérite de la classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ) et la classe [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) fournissent des fonctionnalités permettant d’obtenir et de définir des valeurs de pixel. Vous pouvez utiliser la classe **ImageAttributes** pour modifier les valeurs alpha pour une image entière, ou vous pouvez appeler la méthode [**bitmap :: SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) de la classe **bitmap** pour modifier des valeurs de pixel individuelles. Pour plus d’informations sur la définition de valeurs de pixel individuelles, consultez [définition des valeurs alpha de pixels individuels](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).

L’exemple suivant dessine une ligne noire étendue, puis affiche une image opaque qui couvre une partie de cette ligne.


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



L’illustration suivante montre l’image résultante, qui est dessinée à (30, 0). Notez que la ligne noire de largeur ne s’affiche pas dans l’image.

![Illustration montrant qu’une image opaque se chevauche dans un rectangle fin, épais et noir](images/image1.png)

La classe [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) possède de nombreuses propriétés que vous pouvez utiliser pour modifier des images pendant le rendu. Dans l’exemple suivant, un objet **ImageAttributes** est utilisé pour définir toutes les valeurs alpha à 80% de ce qu’ils étaient. Pour ce faire, initialisez une matrice de couleurs et définissez la valeur de mise à l’échelle alpha dans la matrice sur 0,8. L’adresse de la matrice de couleurs est transmise à la méthode [**ImageAttributes :: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) de l’objet **ImageAttributes** , et l’adresse de l’objet **ImageAttributes** est transmise à la méthode [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .


```
// Create a Bitmap object and load it with the texture image.
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// Initialize the color matrix.
// Notice the value 0.8 in row 4, column 4.
ColorMatrix colorMatrix = {1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.8f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
// Create an ImageAttributes object and set its color matrix.
ImageAttributes imageAtt;
imageAtt.SetColorMatrix(&colorMatrix, ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw the semitransparent bitmap image.
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
graphics.DrawImage(
   &bitmap, 
   Rect(30, 0, iWidth, iHeight),  // Destination rectangle
   0,                             // Source rectangle X 
   0,                             // Source rectangle Y
   iWidth,                        // Source rectangle width
   iHeight,                       // Source rectangle height
   UnitPixel, 
   &imageAtt);
```



Pendant le rendu, les valeurs alpha dans le bitmap sont converties en 80 pour cent de ce qu’elles étaient. Une image est alors fusionnée avec l’arrière-plan. Comme le montre l’illustration suivante, l’image bitmap semble transparente ; vous pouvez voir la ligne noire pleine.

![illustration similaire à la précédente, mais l’image est en transparence SEM](images/image2.png)

Lorsque l’image se trouve sur la partie blanche de l’arrière-plan, l’image a été fusionnée avec la couleur blanche. Lorsque l’image dépasse la ligne noire, l’image est fusionnée avec la couleur noire.

 

 



