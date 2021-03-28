---
description: Vous pouvez remplir une forme fermée avec une texture à l’aide de la classe image et de la classe TextureBrush.
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: Remplissage d’une forme avec une texture d’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f1bf6ba04311310ab1985de1d1aaccd45db43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115226"
---
# <a name="filling-a-shape-with-an-image-texture"></a><span data-ttu-id="a879a-103">Remplissage d’une forme avec une texture d’image</span><span class="sxs-lookup"><span data-stu-id="a879a-103">Filling a Shape with an Image Texture</span></span>

<span data-ttu-id="a879a-104">Vous pouvez remplir une forme fermée avec une texture à l’aide de la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et de la classe [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .</span><span class="sxs-lookup"><span data-stu-id="a879a-104">You can fill a closed shape with a texture by using the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) class.</span></span>

<span data-ttu-id="a879a-105">L’exemple suivant remplit une ellipse avec une image.</span><span class="sxs-lookup"><span data-stu-id="a879a-105">The following example fills an ellipse with an image.</span></span> <span data-ttu-id="a879a-106">Le code construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , puis passe l’adresse de cet objet **image** comme argument à un constructeur [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .</span><span class="sxs-lookup"><span data-stu-id="a879a-106">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, and then passes the address of that **Image** object as an argument to a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) constructor.</span></span> <span data-ttu-id="a879a-107">La troisième instruction de code met à l’échelle l’image, et la quatrième instruction remplit l’ellipse avec des copies répétées de l’image mise à l’échelle :</span><span class="sxs-lookup"><span data-stu-id="a879a-107">The third code statement scales the image, and the fourth statement fills the ellipse with repeated copies of the scaled image:</span></span>


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



<span data-ttu-id="a879a-108">Dans l’exemple de code précédent, la méthode [**TextureBrush :: setTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) définit la transformation qui est appliquée à l’image avant qu’elle ne soit dessinée.</span><span class="sxs-lookup"><span data-stu-id="a879a-108">In the preceding code example, the [**TextureBrush::SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) method sets the transformation that is applied to the image before it is drawn.</span></span> <span data-ttu-id="a879a-109">Supposons que l’image d’origine a une largeur de 640 pixels et une hauteur de 480 pixels.</span><span class="sxs-lookup"><span data-stu-id="a879a-109">Assume that the original image has a width of 640 pixels and a height of 480 pixels.</span></span> <span data-ttu-id="a879a-110">La transformation réduit l’image à 75 × 75, en définissant les valeurs de mise à l’échelle horizontale et verticale.</span><span class="sxs-lookup"><span data-stu-id="a879a-110">The transform shrinks the image to 75 ×75, by setting the horizontal and vertical scaling values.</span></span>

> [!Note]  
> <span data-ttu-id="a879a-111">Dans l’exemple précédent, la taille de l’image est de 75 × 75, et la taille de l’ellipse est 150 × 250.</span><span class="sxs-lookup"><span data-stu-id="a879a-111">In the preceding example, the image size is 75 ×75, and the ellipse size is 150 ×250.</span></span> <span data-ttu-id="a879a-112">Étant donné que l’image est plus petite que l’ellipse qu’elle remplit, l’ellipse est en mosaïque avec l’image.</span><span class="sxs-lookup"><span data-stu-id="a879a-112">Because the image is smaller than the ellipse it is filling, the ellipse is tiled with the image.</span></span> <span data-ttu-id="a879a-113">La mosaïque signifie que l’image est répétée horizontalement et verticalement jusqu’à ce que la limite de la forme soit atteinte.</span><span class="sxs-lookup"><span data-stu-id="a879a-113">Tiling means that the image is repeated horizontally and vertically until the boundary of the shape is reached.</span></span> <span data-ttu-id="a879a-114">Pour plus d’informations sur la mosaïque, consultez [juxtaposition d’une forme avec une image](-gdiplus-tiling-a-shape-with-an-image-use.md).</span><span class="sxs-lookup"><span data-stu-id="a879a-114">For more information on tiling, see [Tiling a Shape with an Image](-gdiplus-tiling-a-shape-with-an-image-use.md).</span></span>

 

 

 



