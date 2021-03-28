---
description: Windows GDI+ fournit les classes image et bitmap pour le stockage et la manipulation d’images.
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: Utilisation d’une matrice de couleurs pour transformer une seule couleur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568549"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a><span data-ttu-id="e16d9-103">Utilisation d’une matrice de couleurs pour transformer une seule couleur</span><span class="sxs-lookup"><span data-stu-id="e16d9-103">Using a Color Matrix to Transform a Single Color</span></span>

<span data-ttu-id="e16d9-104">Windows GDI+ fournit les classes [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) et [**bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) pour le stockage et la manipulation d’images.</span><span class="sxs-lookup"><span data-stu-id="e16d9-104">Windows GDI+ provides the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) classes for storing and manipulating images.</span></span> <span data-ttu-id="e16d9-105">Les objets **image** et **bitmap** stockent la couleur de chaque pixel sous la forme d’un nombre de 32 bits : 8 bits chacun pour les couleurs rouge, vert, bleu et alpha.</span><span class="sxs-lookup"><span data-stu-id="e16d9-105">**Image** and **Bitmap** objects store the color of each pixel as a 32-bit number: 8 bits each for red, green, blue, and alpha.</span></span> <span data-ttu-id="e16d9-106">Chacun des quatre composants est un nombre compris entre 0 et 255, avec 0 Représentant aucune intensité et 255 représentant une intensité complète.</span><span class="sxs-lookup"><span data-stu-id="e16d9-106">Each of the four components is a number from 0 through 255, with 0 representing no intensity and 255 representing full intensity.</span></span> <span data-ttu-id="e16d9-107">Le composant alpha spécifie la transparence de la couleur : 0 est entièrement transparent et 255 est entièrement opaque.</span><span class="sxs-lookup"><span data-stu-id="e16d9-107">The alpha component specifies the transparency of the color: 0 is fully transparent, and 255 is fully opaque.</span></span>

<span data-ttu-id="e16d9-108">Un vecteur de couleur est un tuple à 4 points de la forme (rouge, vert, bleu, alpha).</span><span class="sxs-lookup"><span data-stu-id="e16d9-108">A color vector is a 4-tuple of the form (red, green, blue, alpha).</span></span> <span data-ttu-id="e16d9-109">Par exemple, le vecteur de couleur (0, 255, 0, 255) représente une couleur opaque qui n’a pas de rouge ou de bleu, mais qui présente un vert en intensité complète.</span><span class="sxs-lookup"><span data-stu-id="e16d9-109">For example, the color vector (0, 255, 0, 255) represents an opaque color that has no red or blue, but has green at full intensity.</span></span>

<span data-ttu-id="e16d9-110">Une autre convention pour représenter les couleurs utilise le nombre 1 pour l’intensité maximale et le nombre 0 pour l’intensité minimale.</span><span class="sxs-lookup"><span data-stu-id="e16d9-110">Another convention for representing colors uses the number 1 for maximum intensity and the number 0 for minimum intensity.</span></span> <span data-ttu-id="e16d9-111">À l’aide de cette Convention, la couleur décrite dans le paragraphe précédent est représentée par le vecteur (0, 1, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="e16d9-111">Using that convention, the color described in the preceding paragraph would be represented by the vector (0, 1, 0, 1).</span></span> <span data-ttu-id="e16d9-112">GDI+ utilise la Convention de 1 comme intensité complète lorsqu’il effectue des transformations de couleurs.</span><span class="sxs-lookup"><span data-stu-id="e16d9-112">GDI+ uses the convention of 1 as full intensity when it performs color transformations.</span></span>

<span data-ttu-id="e16d9-113">Vous pouvez appliquer des transformations linéaires (rotation, mise à l’échelle, etc.) à des vecteurs de couleurs en les multipliant par une matrice 4 × 4.</span><span class="sxs-lookup"><span data-stu-id="e16d9-113">You can apply linear transformations (rotation, scaling, and the like) to color vectors by multiplying by a 4 ×4 matrix.</span></span> <span data-ttu-id="e16d9-114">Toutefois, vous ne pouvez pas utiliser une matrice 4 × 4 pour effectuer une traduction (non linéaire).</span><span class="sxs-lookup"><span data-stu-id="e16d9-114">However, you cannot use a 4 ×4 matrix to perform a translation (nonlinear).</span></span> <span data-ttu-id="e16d9-115">Si vous ajoutez une cinquième coordonnée factice (par exemple, le nombre 1) à chacun des vecteurs de couleur, vous pouvez utiliser une matrice 5 × 5 pour appliquer une combinaison de transformations et de traductions linéaires.</span><span class="sxs-lookup"><span data-stu-id="e16d9-115">If you add a dummy fifth coordinate (for example, the number 1) to each of the color vectors, you can use a 5 ×5 matrix to apply any combination of linear transformations and translations.</span></span> <span data-ttu-id="e16d9-116">Une transformation consistant en une transformation linéaire suivie d’une translation est appelée transformation affine.</span><span class="sxs-lookup"><span data-stu-id="e16d9-116">A transformation consisting of a linear transformation followed by a translation is called an affine transformation.</span></span> <span data-ttu-id="e16d9-117">Une matrice 5 × 5 qui représente une transformation affine est appelée matrice homogène pour une transformation à 4 espaces.</span><span class="sxs-lookup"><span data-stu-id="e16d9-117">A 5 ×5 matrix that represents an affine transformation is called a homogeneous matrix for a 4-space transformation.</span></span> <span data-ttu-id="e16d9-118">L’élément de la cinquième ligne et de la cinquième colonne d’une matrice homogène 5 × 5 doit être 1, et toutes les autres entrées de la cinquième colonne doivent être 0.</span><span class="sxs-lookup"><span data-stu-id="e16d9-118">The element in the fifth row and fifth column of a 5 ×5 homogeneous matrix must be 1, and all of the other entries in the fifth column must be 0.</span></span>

<span data-ttu-id="e16d9-119">Par exemple, supposons que vous souhaitez commencer par la couleur (0,2, 0,0, 0,4, 1,0) et appliquer les transformations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e16d9-119">For example, suppose you want to start with the color (0.2, 0.0, 0.4, 1.0) and apply the following transformations:</span></span>

1.  <span data-ttu-id="e16d9-120">Doubler le composant rouge</span><span class="sxs-lookup"><span data-stu-id="e16d9-120">Double the red component</span></span>
2.  <span data-ttu-id="e16d9-121">Ajouter 0,2 aux composants rouge, vert et bleu</span><span class="sxs-lookup"><span data-stu-id="e16d9-121">Add 0.2 to the red, green, and blue components</span></span>

<span data-ttu-id="e16d9-122">La multiplication de matrice suivante effectue la paire de transformations dans l’ordre indiqué.</span><span class="sxs-lookup"><span data-stu-id="e16d9-122">The following matrix multiplication will perform the pair of transformations in the order listed.</span></span>

![Illustration montrant une matrice 5x1 de nombres multipliée par une matrice 5x5 pour créer une nouvelle matrice 5x1](images/recoloring01.png)

<span data-ttu-id="e16d9-124">Les éléments d’une matrice de couleurs sont indexés (de base zéro) par ligne, puis par colonne.</span><span class="sxs-lookup"><span data-stu-id="e16d9-124">The elements of a color matrix are indexed (zero-based) by row and then column.</span></span> <span data-ttu-id="e16d9-125">Par exemple, l’entrée de la cinquième ligne et de la troisième colonne de la matrice M est indiquée par M \[ 4 \] \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="e16d9-125">For example, the entry in the fifth row and third column of matrix M is denoted by M\[4\]\[2\].</span></span>

<span data-ttu-id="e16d9-126">La matrice d’identité 5 × 5 (représentée dans l’illustration ci-dessous) a des 1s sur la diagonale et des 0 partout ailleurs.</span><span class="sxs-lookup"><span data-stu-id="e16d9-126">The 5 ×5 identity matrix (shown in the following illustration) has 1s on the diagonal and 0s everywhere else.</span></span> <span data-ttu-id="e16d9-127">Si vous multipliez un vecteur de couleur par la matrice d’identité, le vecteur de couleur ne change pas.</span><span class="sxs-lookup"><span data-stu-id="e16d9-127">If you multiply a color vector by the identity matrix, the color vector does not change.</span></span> <span data-ttu-id="e16d9-128">Un moyen pratique de former la matrice d’une transformation de couleur consiste à commencer par la matrice d’identité et à effectuer une petite modification qui produit la transformation souhaitée.</span><span class="sxs-lookup"><span data-stu-id="e16d9-128">A convenient way to form the matrix of a color transformation is to start with the identity matrix and make a small change that produces the desired transformation.</span></span>

![Illustration montrant une matrice d’identité 5x5 ; 1 en haut à gauche vers la diagonale inférieure droite et 0 partout ailleurs](images/recoloring02.png)

<span data-ttu-id="e16d9-130">Pour obtenir une présentation plus détaillée des matrices et des transformations, consultez [systèmes de coordonnées et](-gdiplus-coordinate-systems-and-transformations-about.md)transformations.</span><span class="sxs-lookup"><span data-stu-id="e16d9-130">For a more detailed discussion of matrices and transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="e16d9-131">L’exemple suivant prend une image qui est une seule couleur (0,2, 0,0, 0,4, 1,0) et applique la transformation décrite dans les paragraphes précédents.</span><span class="sxs-lookup"><span data-stu-id="e16d9-131">The following example takes an image that is all one color (0.2, 0.0, 0.4, 1.0) and applies the transformation described in the preceding paragraphs.</span></span>


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



<span data-ttu-id="e16d9-132">L’illustration suivante montre l’image d’origine à gauche et l’image transformée à droite.</span><span class="sxs-lookup"><span data-stu-id="e16d9-132">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![<span data-ttu-id="e16d9-133">Illustration montrant un rectangle rempli d’une couleur unie foncée, puis un rectangle rempli d’une couleur unie plus claire</span><span class="sxs-lookup"><span data-stu-id="e16d9-133">illustration showing a rectangle filled by a dark solid color and then one filled by a lighter solid color</span></span> ](images/colortrans1.png)

<span data-ttu-id="e16d9-134">Le code de l’exemple précédent utilise les étapes suivantes pour effectuer la recoloriage :</span><span class="sxs-lookup"><span data-stu-id="e16d9-134">The code in the preceding example uses the following steps to perform the recoloring:</span></span>

1.  <span data-ttu-id="e16d9-135">Initialise une structure [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .</span><span class="sxs-lookup"><span data-stu-id="e16d9-135">Initialize a [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>
2.  <span data-ttu-id="e16d9-136">Créez un objet [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) et transmettez l’adresse de la structure [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) à la méthode [**ImageAttributes :: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) de l’objet **ImageAttributes** .</span><span class="sxs-lookup"><span data-stu-id="e16d9-136">Create an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object and pass the address of the [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object.</span></span>
3.  <span data-ttu-id="e16d9-137">Transmettez l’adresse de l’objet [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) à la méthode [DrawImage méthodes](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) d’un objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="e16d9-137">Pass the address of the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

 

 



