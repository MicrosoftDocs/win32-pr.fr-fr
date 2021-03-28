---
description: Une transformation de mise à l’échelle multiplie un ou plusieurs des quatre composants de couleur par un nombre. Les entrées de la matrice de couleurs qui représentent la mise à l’échelle sont indiquées dans le tableau suivant.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Mise à l’échelle des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370155306f7b1a177358d7cf28d329ebb0d75f8c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104211160"
---
# <a name="scaling-colors"></a><span data-ttu-id="c10d7-104">Mise à l’échelle des couleurs</span><span class="sxs-lookup"><span data-stu-id="c10d7-104">Scaling Colors</span></span>

<span data-ttu-id="c10d7-105">Une transformation de mise à l’échelle multiplie un ou plusieurs des quatre composants de couleur par un nombre.</span><span class="sxs-lookup"><span data-stu-id="c10d7-105">A scaling transformation multiplies one or more of the four color components by a number.</span></span> <span data-ttu-id="c10d7-106">Les entrées de la matrice de couleurs qui représentent la mise à l’échelle sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c10d7-106">The color matrix entries that represent scaling are given in the following table.</span></span>



| <span data-ttu-id="c10d7-107">Composant à mettre à l’échelle</span><span class="sxs-lookup"><span data-stu-id="c10d7-107">Component to be scaled</span></span> | <span data-ttu-id="c10d7-108">Entrée de la matrice</span><span class="sxs-lookup"><span data-stu-id="c10d7-108">Matrix entry</span></span> |
|------------------------|--------------|
| <span data-ttu-id="c10d7-109">Rouge</span><span class="sxs-lookup"><span data-stu-id="c10d7-109">Red</span></span>                    | <span data-ttu-id="c10d7-110">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="c10d7-110">\[0\]\[0\]</span></span>   |
| <span data-ttu-id="c10d7-111">Vert</span><span class="sxs-lookup"><span data-stu-id="c10d7-111">Green</span></span>                  | <span data-ttu-id="c10d7-112">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="c10d7-112">\[1\]\[1\]</span></span>   |
| <span data-ttu-id="c10d7-113">Blue</span><span class="sxs-lookup"><span data-stu-id="c10d7-113">Blue</span></span>                   | <span data-ttu-id="c10d7-114">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="c10d7-114">\[2\]\[2\]</span></span>   |
| <span data-ttu-id="c10d7-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="c10d7-115">Alpha</span></span>                  | <span data-ttu-id="c10d7-116">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="c10d7-116">\[3\]\[3\]</span></span>   |



 

<span data-ttu-id="c10d7-117">L’exemple suivant construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="c10d7-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="c10d7-118">Ensuite, le code met à l’échelle le composant bleu de chaque pixel de l’image selon un facteur de 2.</span><span class="sxs-lookup"><span data-stu-id="c10d7-118">Then the code scales the blue component of each pixel in the image by a factor of 2.</span></span> <span data-ttu-id="c10d7-119">L’image d’origine est dessinée à côté de l’image transformée.</span><span class="sxs-lookup"><span data-stu-id="c10d7-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
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



<span data-ttu-id="c10d7-120">L’illustration suivante montre l’image d’origine à gauche et l’image mise à l’échelle à droite.</span><span class="sxs-lookup"><span data-stu-id="c10d7-120">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![Affiche quatre barres colorées, puis les mêmes barres avec des couleurs différentes.](images/colortrans3.png)

<span data-ttu-id="c10d7-122">Le tableau suivant présente les vecteurs de couleur pour les quatre barres avant et après la mise à l’échelle bleue.</span><span class="sxs-lookup"><span data-stu-id="c10d7-122">The following table shows the color vectors for the four bars before and after the blue scaling.</span></span> <span data-ttu-id="c10d7-123">Notez que le composant bleu de la quatrième barre de couleur est passé de 0,8 à 0,6.</span><span class="sxs-lookup"><span data-stu-id="c10d7-123">Note that the blue component in the fourth color bar went from 0.8 to 0.6.</span></span> <span data-ttu-id="c10d7-124">Cela est dû au fait que GDI+ conserve uniquement la partie fractionnaire du résultat.</span><span class="sxs-lookup"><span data-stu-id="c10d7-124">That is because GDI+ retains only the fractional part of the result.</span></span> <span data-ttu-id="c10d7-125">Par exemple, (2) (0,8) = 1,6, et la partie fractionnaire de 1,6 est 0,6.</span><span class="sxs-lookup"><span data-stu-id="c10d7-125">For example, (2)(0.8) = 1.6, and the fractional part of 1.6 is 0.6.</span></span> <span data-ttu-id="c10d7-126">Conserver uniquement la partie fractionnaire garantit que le résultat est toujours \[ compris entre 0 et 1 \] .</span><span class="sxs-lookup"><span data-stu-id="c10d7-126">Retaining only the fractional part ensures that the result is always in the interval \[0, 1\].</span></span>



| <span data-ttu-id="c10d7-127">Original</span><span class="sxs-lookup"><span data-stu-id="c10d7-127">Original</span></span>           | <span data-ttu-id="c10d7-128">Montée</span><span class="sxs-lookup"><span data-stu-id="c10d7-128">Scaled</span></span>             |
|--------------------|--------------------|
| <span data-ttu-id="c10d7-129">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-129">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="c10d7-130">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-130">(0.4, 0.4, 0.8, 1)</span></span> |
| <span data-ttu-id="c10d7-131">(0.4, 0.2, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-131">(0.4, 0.2, 0.2, 1)</span></span> | <span data-ttu-id="c10d7-132">(0.4, 0.2, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-132">(0.4, 0.2, 0.4, 1)</span></span> |
| <span data-ttu-id="c10d7-133">(0.2, 0.4, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-133">(0.2, 0.4, 0.2, 1)</span></span> | <span data-ttu-id="c10d7-134">(0.2, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-134">(0.2, 0.4, 0.4, 1)</span></span> |
| <span data-ttu-id="c10d7-135">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-135">(0.4, 0.4, 0.8, 1)</span></span> | <span data-ttu-id="c10d7-136">(0.4, 0.4, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-136">(0.4, 0.4, 0.6, 1)</span></span> |



 

<span data-ttu-id="c10d7-137">L’exemple suivant construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="c10d7-137">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="c10d7-138">Ensuite, le code met à l’échelle les composants rouge, vert et bleu de chaque pixel de l’image.</span><span class="sxs-lookup"><span data-stu-id="c10d7-138">Then the code scales the red, green, and blue components of each pixel in the image.</span></span> <span data-ttu-id="c10d7-139">Les composants rouges sont réduits de 25%, les composants verts sont réduits à 35 pour cent et les composants bleus sont réduits de 50%.</span><span class="sxs-lookup"><span data-stu-id="c10d7-139">The red components are scaled down 25 percent, the green components are scaled down 35 percent, and the blue components are scaled down 50 percent.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="c10d7-140">L’illustration suivante montre l’image d’origine à gauche et l’image mise à l’échelle à droite.</span><span class="sxs-lookup"><span data-stu-id="c10d7-140">The following illustration shows the original image on the left and the scaled image on the right.</span></span>

![Illustration montrant quatre barres colorées, puis les barres avec des couleurs différentes](images/colortrans4.png)

<span data-ttu-id="c10d7-142">Le tableau suivant présente les vecteurs de couleur pour les quatre barres avant et après la mise à l’échelle rouge, verte et bleue.</span><span class="sxs-lookup"><span data-stu-id="c10d7-142">The following table shows the color vectors for the four bars before and after the red, green and blue scaling.</span></span>



| <span data-ttu-id="c10d7-143">Original</span><span class="sxs-lookup"><span data-stu-id="c10d7-143">Original</span></span>           | <span data-ttu-id="c10d7-144">Montée</span><span class="sxs-lookup"><span data-stu-id="c10d7-144">Scaled</span></span>               |
|--------------------|----------------------|
| <span data-ttu-id="c10d7-145">(0.6, 0.6, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-145">(0.6, 0.6, 0.6, 1)</span></span> | <span data-ttu-id="c10d7-146">(0.45, 0.39, 0.3, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-146">(0.45, 0.39, 0.3, 1)</span></span> |
| <span data-ttu-id="c10d7-147">(0, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-147">(0, 1, 1, 1)</span></span>       | <span data-ttu-id="c10d7-148">(0, 0.65, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-148">(0, 0.65, 0.5, 1)</span></span>    |
| <span data-ttu-id="c10d7-149">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-149">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="c10d7-150">(0.75, 0.65, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-150">(0.75, 0.65, 0, 1)</span></span>   |
| <span data-ttu-id="c10d7-151">(1, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-151">(1, 0, 1, 1)</span></span>       | <span data-ttu-id="c10d7-152">(0.75, 0, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="c10d7-152">(0.75, 0, 0.5, 1)</span></span>    |



 

 

 



