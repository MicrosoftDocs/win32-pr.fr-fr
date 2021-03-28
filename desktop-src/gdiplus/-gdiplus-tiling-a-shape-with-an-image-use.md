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
# <a name="tiling-a-shape-with-an-image"></a><span data-ttu-id="49742-103">Mosaïque d’une forme avec une image</span><span class="sxs-lookup"><span data-stu-id="49742-103">Tiling a Shape with an Image</span></span>

<span data-ttu-id="49742-104">Tout comme les vignettes peuvent être placées les unes à côté des autres pour couvrir un étage, les images rectangulaires peuvent être placées les unes à côté les autres pour remplir (juxtaposer) une forme.</span><span class="sxs-lookup"><span data-stu-id="49742-104">Just as tiles can be placed next to each other to cover a floor, rectangular images can be placed next to each other to fill (tile) a shape.</span></span> <span data-ttu-id="49742-105">Pour effectuer une mosaïque de l’intérieur d’une forme, utilisez un pinceau de texture.</span><span class="sxs-lookup"><span data-stu-id="49742-105">To tile the interior of a shape, use a texture brush.</span></span> <span data-ttu-id="49742-106">Quand vous construisez un objet [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , l’un des arguments que vous transmettez au constructeur est l’adresse d’un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="49742-106">When you construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, one of the arguments you pass to the constructor is the address of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="49742-107">Lorsque vous utilisez le pinceau de texture pour peindre l’intérieur d’une forme, la forme est remplie avec des copies répétées de cette image.</span><span class="sxs-lookup"><span data-stu-id="49742-107">When you use the texture brush to paint the interior of a shape, the shape is filled with repeated copies of this image.</span></span>

<span data-ttu-id="49742-108">La propriété mode Wrap de l’objet [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) détermine la façon dont l’image est orientée, car elle est répétée dans une grille rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="49742-108">The wrap mode property of the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object determines how the image is oriented as it is repeated in a rectangular grid.</span></span> <span data-ttu-id="49742-109">Vous pouvez faire en sorte que toutes les vignettes de la grille aient la même orientation, ou vous pouvez faire basculer l’image d’une position de grille à la suivante.</span><span class="sxs-lookup"><span data-stu-id="49742-109">You can make all the tiles in the grid have the same orientation, or you can make the image flip from one grid position to the next.</span></span> <span data-ttu-id="49742-110">Le retournement peut être horizontal, vertical ou les deux.</span><span class="sxs-lookup"><span data-stu-id="49742-110">The flipping can be horizontal, vertical, or both.</span></span> <span data-ttu-id="49742-111">Les exemples suivants illustrent la juxtaposition avec différents types de retournement.</span><span class="sxs-lookup"><span data-stu-id="49742-111">The following examples demonstrate tiling with different types of flipping.</span></span>

## <a name="tiling-an-image"></a><span data-ttu-id="49742-112">Mosaïque d’une image</span><span class="sxs-lookup"><span data-stu-id="49742-112">Tiling an Image</span></span>

<span data-ttu-id="49742-113">Cet exemple utilise l’image 75 × 75 suivante pour juxtaposer un rectangle 200 × 200 :</span><span class="sxs-lookup"><span data-stu-id="49742-113">This example uses the following 75 ×75 image to tile a 200 ×200 rectangle:</span></span>

![illustration utilisée comme base d’autres illustrations de cette rubrique : un bâtiment et une arborescence sur l’arrière-plan et centré dans un rectangle](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="49742-115">L’illustration suivante montre comment le rectangle est disposé en mosaïque avec l’image.</span><span class="sxs-lookup"><span data-stu-id="49742-115">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="49742-116">Notez que toutes les vignettes ont la même orientation ; Il n’y a pas de retournement.</span><span class="sxs-lookup"><span data-stu-id="49742-116">Note that all tiles have the same orientation; there is no flipping.</span></span>

![Illustration montrant l’image de base répétée horizontalement et verticalement dans un grand rectangle](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a><span data-ttu-id="49742-118">Retournement d’une image horizontalement pendant une mosaïque</span><span class="sxs-lookup"><span data-stu-id="49742-118">Flipping an Image Horizontally While Tiling</span></span>

<span data-ttu-id="49742-119">Cet exemple utilise une image 75 × 75 pour remplir un rectangle 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="49742-119">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="49742-120">Le mode habillage est défini pour retourner l’image horizontalement.</span><span class="sxs-lookup"><span data-stu-id="49742-120">The wrap mode is set to flip the image horizontally.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="49742-121">L’illustration suivante montre comment le rectangle est disposé en mosaïque avec l’image.</span><span class="sxs-lookup"><span data-stu-id="49742-121">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="49742-122">Notez que lorsque vous passez d’une vignette à la suivante dans une ligne donnée, l’image est retournée horizontalement.</span><span class="sxs-lookup"><span data-stu-id="49742-122">Note that as you move from one tile to the next in a given row, the image is flipped horizontally.</span></span>

![Illustration montrant l’image de base répétée horizontalement, mais les instances paires sont inversées horizontalement](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a><span data-ttu-id="49742-124">Retournement d’une image verticalement pendant la mosaïque</span><span class="sxs-lookup"><span data-stu-id="49742-124">Flipping an Image Vertically While Tiling</span></span>

<span data-ttu-id="49742-125">Cet exemple utilise une image 75 × 75 pour remplir un rectangle 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="49742-125">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="49742-126">Le mode habillage est défini pour retourner l’image verticalement.</span><span class="sxs-lookup"><span data-stu-id="49742-126">The wrap mode is set to flip the image vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="49742-127">L’illustration suivante montre comment le rectangle est disposé en mosaïque avec l’image.</span><span class="sxs-lookup"><span data-stu-id="49742-127">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="49742-128">Notez que lorsque vous passez d’une vignette à la suivante dans une colonne donnée, l’image est retournée verticalement.</span><span class="sxs-lookup"><span data-stu-id="49742-128">Note that as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![Illustration montrant l’image de base répétée horizontalement et verticalement, mais les lignes paires sont inversées verticalement](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a><span data-ttu-id="49742-130">Retournement d’une image horizontalement et verticalement pendant la mosaïque</span><span class="sxs-lookup"><span data-stu-id="49742-130">Flipping an Image Horizontally and Vertically While Tiling</span></span>

<span data-ttu-id="49742-131">Cet exemple utilise une image 75 × 75 pour juxtaposer un rectangle 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="49742-131">This example uses a 75 ×75 image to tile a 200 ×200 rectangle.</span></span> <span data-ttu-id="49742-132">Le mode habillage est défini pour retourner l’image à la fois horizontalement et verticalement.</span><span class="sxs-lookup"><span data-stu-id="49742-132">The wrap mode is set to flip the image both horizontally and vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="49742-133">L’illustration suivante montre comment le rectangle est disposé en mosaïque par l’image.</span><span class="sxs-lookup"><span data-stu-id="49742-133">The following illustration shows how the rectangle is tiled by the image.</span></span> <span data-ttu-id="49742-134">Notez que lorsque vous passez d’une vignette à l’autre dans une ligne donnée, l’image est retournée horizontalement et lorsque vous passez d’une vignette à la suivante dans une colonne donnée, l’image est retournée verticalement.</span><span class="sxs-lookup"><span data-stu-id="49742-134">Note that as you move from one tile to the next in a given row, the image is flipped horizontally, and as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![illustration qui montre les instances de remplacement de l’image de base dans chaque ligne qui sont retournées horizontalement et les lignes alternées verticalement](images/tile5.png)

 

 



