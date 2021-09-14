---
description: Le remappage est le processus de conversion des couleurs d’une image en fonction d’une table de remappage des couleurs. La table de remappage des couleurs est un tableau de structures ColorMap. Chaque structure ColorMap du tableau a un membre oldColor et un membre newColor.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Utilisation d’une table de remappage des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1c07bc0a67a02ea07aeaa3931e661af5665e33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414299"
---
# <a name="using-a-color-remap-table"></a>Utilisation d’une table de remappage des couleurs

Le remappage est le processus de conversion des couleurs d’une image en fonction d’une table de remappage des couleurs. La table de remappage des couleurs est un tableau de structures [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) . Chaque structure **ColorMap** du tableau a un membre **oldColor** et un membre **NewColor** .

quand GDI+ dessine une image, chaque pixel de l’image est comparé au tableau des anciennes couleurs. Si la couleur d’un pixel correspond à une ancienne couleur, sa couleur est remplacée par la nouvelle couleur correspondante. Les couleurs sont modifiées uniquement pour le rendu : les valeurs de couleur de l’image elle-même (stockées dans une [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ou un objet [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) ) ne sont pas modifiées.

Pour dessiner une image remappée, initialisez un tableau de structures [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) . Transmettez l’adresse de ce tableau à la méthode [**ImageAttributes :: SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) d’un objet [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , puis transmettez l’adresse de l’objet **ImageAttributes** à la méthode [DrawImage des méthodes](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

L’exemple suivant crée un objet [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier RemapInput.bmp. Le code crée une table de remappage des couleurs qui se compose d’une structure [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) unique. Le membre **oldColor** de la structure **ColorMap** est rouge et le membre **NewColor** est bleu. L’image est dessinée une seule fois sans remappage et une fois avec le remappage. Le processus de remappage remplace tous les pixels rouges par le bleu.


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

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



L’illustration suivante montre l’image d’origine à gauche et l’image remappée à droite.

![Illustration montrant deux versions d’une image multicolore ; la région rouge de la première version est bleue dans la deuxième version](images/colortrans7.png)

 

 



