---
description: Tout comme les vignettes peuvent être placées les unes à côté des autres pour couvrir un étage, les images rectangulaires peuvent être placées les unes à côté les autres pour remplir (juxtaposer) une forme.
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Mosaïque d’une forme avec une image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c0b6e2ce39f5bf5c43b0352b8997202aa7e856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112946"
---
# <a name="tiling-a-shape-with-an-image"></a>Mosaïque d’une forme avec une image

Tout comme les vignettes peuvent être placées les unes à côté des autres pour couvrir un étage, les images rectangulaires peuvent être placées les unes à côté les autres pour remplir (juxtaposer) une forme. Pour effectuer une mosaïque de l’intérieur d’une forme, utilisez un pinceau de texture. Quand vous construisez un objet [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , l’un des arguments que vous transmettez au constructeur est l’adresse d’un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) . Lorsque vous utilisez le pinceau de texture pour peindre l’intérieur d’une forme, la forme est remplie avec des copies répétées de cette image.

La propriété mode Wrap de l’objet [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) détermine la façon dont l’image est orientée, car elle est répétée dans une grille rectangulaire. Vous pouvez faire en sorte que toutes les vignettes de la grille aient la même orientation, ou vous pouvez faire basculer l’image d’une position de grille à la suivante. Le retournement peut être horizontal, vertical ou les deux. Les exemples suivants illustrent la juxtaposition avec différents types de retournement.

## <a name="tiling-an-image"></a>Mosaïque d’une image

Cet exemple utilise l’image 75 × 75 suivante pour juxtaposer un rectangle 200 × 200 :

![illustration utilisée comme base d’autres illustrations de cette rubrique : un bâtiment et une arborescence sur l’arrière-plan et centré dans un rectangle](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



L’illustration suivante montre comment le rectangle est disposé en mosaïque avec l’image. Notez que toutes les vignettes ont la même orientation ; Il n’y a pas de retournement.

![Illustration montrant l’image de base répétée horizontalement et verticalement dans un grand rectangle](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a>Retournement d’une image horizontalement pendant une mosaïque

Cet exemple utilise une image 75 × 75 pour remplir un rectangle 200 × 200. Le mode habillage est défini pour retourner l’image horizontalement.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



L’illustration suivante montre comment le rectangle est disposé en mosaïque avec l’image. Notez que lorsque vous passez d’une vignette à la suivante dans une ligne donnée, l’image est retournée horizontalement.

![Illustration montrant l’image de base répétée horizontalement, mais les instances paires sont inversées horizontalement](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a>Retournement d’une image verticalement pendant la mosaïque

Cet exemple utilise une image 75 × 75 pour remplir un rectangle 200 × 200. Le mode habillage est défini pour retourner l’image verticalement.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



L’illustration suivante montre comment le rectangle est disposé en mosaïque avec l’image. Notez que lorsque vous passez d’une vignette à la suivante dans une colonne donnée, l’image est retournée verticalement.

![Illustration montrant l’image de base répétée horizontalement et verticalement, mais les lignes paires sont inversées verticalement](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a>Retournement d’une image horizontalement et verticalement pendant la mosaïque

Cet exemple utilise une image 75 × 75 pour juxtaposer un rectangle 200 × 200. Le mode habillage est défini pour retourner l’image à la fois horizontalement et verticalement.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



L’illustration suivante montre comment le rectangle est disposé en mosaïque par l’image. Notez que lorsque vous passez d’une vignette à l’autre dans une ligne donnée, l’image est retournée horizontalement et lorsque vous passez d’une vignette à la suivante dans une colonne donnée, l’image est retournée verticalement.

![illustration qui montre les instances de remplacement de l’image de base dans chaque ligne qui sont retournées horizontalement et les lignes alternées verticalement](images/tile5.png)

 

 



