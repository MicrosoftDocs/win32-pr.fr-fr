---
description: La rotation dans un espace de couleurs à quatre dimensions est difficile à visualiser.
ms.assetid: 099f76a3-2da3-4f2b-8f8d-557d144451dc
title: Rotation des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea322179bd4a46021d181abedd1797d6bdda7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862529"
---
# <a name="rotating-colors"></a><span data-ttu-id="47b67-103">Rotation des couleurs</span><span class="sxs-lookup"><span data-stu-id="47b67-103">Rotating Colors</span></span>

<span data-ttu-id="47b67-104">La rotation dans un espace de couleurs à quatre dimensions est difficile à visualiser.</span><span class="sxs-lookup"><span data-stu-id="47b67-104">Rotation in a four-dimensional color space is difficult to visualize.</span></span> <span data-ttu-id="47b67-105">Nous pouvons faciliter la visualisation de la rotation en acceptant de conserver l’un des composants de couleur fixe.</span><span class="sxs-lookup"><span data-stu-id="47b67-105">We can make it easier to visualize rotation by agreeing to keep one of the color components fixed.</span></span> <span data-ttu-id="47b67-106">Supposons que nous acceptions de conserver le composant alpha fixe à 1 (entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="47b67-106">Suppose we agree to keep the alpha component fixed at 1 (fully opaque).</span></span> <span data-ttu-id="47b67-107">Ensuite, nous pouvons visualiser un espace de couleurs à trois dimensions avec des axes rouge, vert et bleu, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="47b67-107">Then we can visualize a three-dimensional color space with red, green, and blue axes as shown in the following illustration.</span></span>

![illustration d’une vue en perspective d’un espace de couleurs à trois dimensions avec des axes intitulés rouge, vert et bleu](images/recoloring03.png)

<span data-ttu-id="47b67-109">Une couleur peut être considérée comme un point dans l’espace 3D.</span><span class="sxs-lookup"><span data-stu-id="47b67-109">A color can be thought of as a point in 3-D space.</span></span> <span data-ttu-id="47b67-110">Par exemple, le point (1,0, 0) dans l’espace représente la couleur rouge et le point (0, 1, 0) de l’espace représente la couleur verte.</span><span class="sxs-lookup"><span data-stu-id="47b67-110">For example, the point (1, 0, 0) in space represents the color red, and the point (0, 1, 0) in space represents the color green.</span></span>

<span data-ttu-id="47b67-111">L’illustration suivante montre ce que cela signifie pour faire pivoter la couleur (1, 0, 0) à l’aide d’un angle de 60 degrés dans le plan Red-Green.</span><span class="sxs-lookup"><span data-stu-id="47b67-111">The following illustration shows what it means to rotate the color (1, 0, 0) through an angle of 60 degrees in the Red-Green plane.</span></span> <span data-ttu-id="47b67-112">La rotation d’un plan parallèle au plan de Red-Green peut être considérée comme une rotation autour de l’axe bleu.</span><span class="sxs-lookup"><span data-stu-id="47b67-112">Rotation in a plane parallel to the Red-Green plane can be thought of as rotation about the blue axis.</span></span>

![Illustration montrant le point (1, 0, 0) pivoté de 60 degrés à (0,5, 0,866, 0)](images/recoloring04.png)

<span data-ttu-id="47b67-114">L’illustration suivante montre comment initialiser une matrice de couleurs pour effectuer des rotations sur chacun des trois axes de coordonnées (rouge, vert, bleu).</span><span class="sxs-lookup"><span data-stu-id="47b67-114">The following illustration shows how to initialize a color matrix to perform rotations about each of the three coordinate axes (red, green, blue).</span></span>

![Illustration montrant des matrices de couleurs qui effectuent des rotations sur chacun des trois axes de coordonnées](images/recoloring05.png)

<span data-ttu-id="47b67-116">L’exemple suivant prend une image qui est une seule couleur (1, 0, 0,6) et applique une rotation de 60 degrés autour de l’axe bleu.</span><span class="sxs-lookup"><span data-stu-id="47b67-116">The following example takes an image that is all one color (1, 0, 0.6) and applies a 60-degree rotation about the blue axis.</span></span> <span data-ttu-id="47b67-117">L’angle de rotation est balayé dans un plan parallèle au plan de Red-Green.</span><span class="sxs-lookup"><span data-stu-id="47b67-117">The angle of the rotation is swept out in a plane that is parallel to the Red-Green plane.</span></span>


```
Image            image(L"RotationInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
REAL             degrees = 60;
REAL             pi = acos(-1);  // the angle whose cosine is -1.
REAL             r = degrees * pi / 180;  // degrees to radians

ColorMatrix colorMatrix = {
   cos(r),  sin(r), 0.0f, 0.0f, 0.0f,
   -sin(r), cos(r), 0.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   1.0f, 0.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 1.0f, 0.0f,
   0.0f,    0.0f,   0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(130, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="47b67-118">L’illustration suivante montre l’image d’origine sur la gauche et l’image de rotation de couleur à droite.</span><span class="sxs-lookup"><span data-stu-id="47b67-118">The following illustration shows the original image on the left and the color-rotated image on the right.</span></span>

![Illustration montrant des rectangles remplis avec l’image d’origine (rouge violet) et une image de rotation des couleurs (vert marin)](images/colortrans5.png)

<span data-ttu-id="47b67-120">La rotation des couleurs effectuée dans l’exemple de code précédent peut être visualisée comme suit.</span><span class="sxs-lookup"><span data-stu-id="47b67-120">The color rotation performed in the preceding code example can be visualized as follows.</span></span>

![Illustration montrant un espace de couleurs 3D et le point (1, 0, 0,6) pivoté de 60 degrés vers (0,5, 0,866, 0,6)](images/recoloring06.png)

 

 



