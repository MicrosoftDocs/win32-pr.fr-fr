---
description: Windows GDI+ fournit les classes image et Bitmap pour le stockage et la manipulation d’images.
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: Utilisation d’une matrice de couleurs pour transformer une seule couleur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4de130aef0e30a04c6f7cdad8a669c834357fbc5cd3719671f3529d9ed04c1cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778579"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a>Utilisation d’une matrice de couleurs pour transformer une seule couleur

Windows GDI+ fournit les classes [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) et [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) pour le stockage et la manipulation d’images. Les objets **image** et **bitmap** stockent la couleur de chaque pixel sous la forme d’un nombre de 32 bits : 8 bits chacun pour les couleurs rouge, vert, bleu et alpha. Chacun des quatre composants est un nombre compris entre 0 et 255, avec 0 Représentant aucune intensité et 255 représentant une intensité complète. Le composant alpha spécifie la transparence de la couleur : 0 est entièrement transparent et 255 est entièrement opaque.

Un vecteur de couleur est un tuple à 4 points de la forme (rouge, vert, bleu, alpha). Par exemple, le vecteur de couleur (0, 255, 0, 255) représente une couleur opaque qui n’a pas de rouge ou de bleu, mais qui présente un vert en intensité complète.

Une autre convention pour représenter les couleurs utilise le nombre 1 pour l’intensité maximale et le nombre 0 pour l’intensité minimale. À l’aide de cette Convention, la couleur décrite dans le paragraphe précédent est représentée par le vecteur (0, 1, 0, 1). GDI+ utilise la convention de 1 comme intensité complète lorsqu’il effectue des transformations de couleurs.

Vous pouvez appliquer des transformations linéaires (rotation, mise à l’échelle, etc.) à des vecteurs de couleurs en les multipliant par une matrice 4 × 4. Toutefois, vous ne pouvez pas utiliser une matrice 4 × 4 pour effectuer une traduction (non linéaire). Si vous ajoutez une cinquième coordonnée factice (par exemple, le nombre 1) à chacun des vecteurs de couleur, vous pouvez utiliser une matrice 5 × 5 pour appliquer une combinaison de transformations et de traductions linéaires. Une transformation consistant en une transformation linéaire suivie d’une translation est appelée transformation affine. Une matrice 5 × 5 qui représente une transformation affine est appelée matrice homogène pour une transformation à 4 espaces. L’élément de la cinquième ligne et de la cinquième colonne d’une matrice homogène 5 × 5 doit être 1, et toutes les autres entrées de la cinquième colonne doivent être 0.

Par exemple, supposons que vous souhaitez commencer par la couleur (0,2, 0,0, 0,4, 1,0) et appliquer les transformations suivantes :

1.  Doubler le composant rouge
2.  Ajouter 0,2 aux composants rouge, vert et bleu

La multiplication de matrice suivante effectue la paire de transformations dans l’ordre indiqué.

![Illustration montrant une matrice 5x1 de nombres multipliée par une matrice 5x5 pour créer une nouvelle matrice 5x1](images/recoloring01.png)

Les éléments d’une matrice de couleurs sont indexés (de base zéro) par ligne, puis par colonne. Par exemple, l’entrée de la cinquième ligne et de la troisième colonne de la matrice M est indiquée par M \[ 4 \] \[ 2 \] .

La matrice d’identité 5 × 5 (représentée dans l’illustration ci-dessous) a des 1s sur la diagonale et des 0 partout ailleurs. Si vous multipliez un vecteur de couleur par la matrice d’identité, le vecteur de couleur ne change pas. Un moyen pratique de former la matrice d’une transformation de couleur consiste à commencer par la matrice d’identité et à effectuer une petite modification qui produit la transformation souhaitée.

![Illustration montrant une matrice d’identité 5x5 ; 1 en haut à gauche vers la diagonale inférieure droite et 0 partout ailleurs](images/recoloring02.png)

Pour obtenir une présentation plus détaillée des matrices et des transformations, consultez [systèmes de coordonnées et](-gdiplus-coordinate-systems-and-transformations-about.md)transformations.

L’exemple suivant prend une image qui est une seule couleur (0,2, 0,0, 0,4, 1,0) et applique la transformation décrite dans les paragraphes précédents.


```
Image            image(L"InputColor.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   2.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.2f, 0.2f, 0.2f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10);

graphics.DrawImage(
   &image, 
   Rect(120, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



L’illustration suivante montre l’image d’origine à gauche et l’image transformée à droite.

![Illustration montrant un rectangle rempli d’une couleur unie foncée, puis un rectangle rempli d’une couleur unie plus claire ](images/colortrans1.png)

Le code de l’exemple précédent utilise les étapes suivantes pour effectuer la recoloriage :

1.  Initialise une structure [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .
2.  Créez un objet [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) et transmettez l’adresse de la structure [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) à la méthode [**ImageAttributes :: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) de l’objet **ImageAttributes** .
3.  Transmettez l’adresse de l’objet [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) à la méthode [DrawImage méthodes](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

 

 



