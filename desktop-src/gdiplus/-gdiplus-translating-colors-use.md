---
description: Une traduction ajoute une valeur à un ou plusieurs des quatre composants de couleur. Les entrées de la matrice de couleurs qui représentent des traductions sont indiquées dans le tableau suivant.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Conversion des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c769a24c02e977c3e32ff913852d4b6b8d54441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559308"
---
# <a name="translating-colors"></a><span data-ttu-id="ca22a-104">Conversion des couleurs</span><span class="sxs-lookup"><span data-stu-id="ca22a-104">Translating Colors</span></span>

<span data-ttu-id="ca22a-105">Une traduction ajoute une valeur à un ou plusieurs des quatre composants de couleur.</span><span class="sxs-lookup"><span data-stu-id="ca22a-105">A translation adds a value to one or more of the four color components.</span></span> <span data-ttu-id="ca22a-106">Les entrées de la matrice de couleurs qui représentent des traductions sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ca22a-106">The color matrix entries that represent translations are given in the following table.</span></span>



| <span data-ttu-id="ca22a-107">Composant à traduire</span><span class="sxs-lookup"><span data-stu-id="ca22a-107">Component to be translated</span></span> | <span data-ttu-id="ca22a-108">Entrée de la matrice</span><span class="sxs-lookup"><span data-stu-id="ca22a-108">Matrix entry</span></span> |
|----------------------------|--------------|
| <span data-ttu-id="ca22a-109">Rouge</span><span class="sxs-lookup"><span data-stu-id="ca22a-109">Red</span></span>                        | <span data-ttu-id="ca22a-110">\[4 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="ca22a-110">\[4\]\[0\]</span></span>   |
| <span data-ttu-id="ca22a-111">Vert</span><span class="sxs-lookup"><span data-stu-id="ca22a-111">Green</span></span>                      | <span data-ttu-id="ca22a-112">\[4 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="ca22a-112">\[4\]\[1\]</span></span>   |
| <span data-ttu-id="ca22a-113">Blue</span><span class="sxs-lookup"><span data-stu-id="ca22a-113">Blue</span></span>                       | <span data-ttu-id="ca22a-114">\[4 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="ca22a-114">\[4\]\[2\]</span></span>   |
| <span data-ttu-id="ca22a-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="ca22a-115">Alpha</span></span>                      | <span data-ttu-id="ca22a-116">\[4 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="ca22a-116">\[4\]\[3\]</span></span>   |



 

<span data-ttu-id="ca22a-117">L’exemple suivant construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier ColorBars.bmp.</span><span class="sxs-lookup"><span data-stu-id="ca22a-117">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars.bmp.</span></span> <span data-ttu-id="ca22a-118">Le code ajoute ensuite 0,75 au composant rouge de chaque pixel de l’image.</span><span class="sxs-lookup"><span data-stu-id="ca22a-118">Then the code adds 0.75 to the red component of each pixel in the image.</span></span> <span data-ttu-id="ca22a-119">L’image d’origine est dessinée à côté de l’image transformée.</span><span class="sxs-lookup"><span data-stu-id="ca22a-119">The original image is drawn alongside the transformed image.</span></span>


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



<span data-ttu-id="ca22a-120">L’illustration suivante montre l’image d’origine à gauche et l’image transformée à droite.</span><span class="sxs-lookup"><span data-stu-id="ca22a-120">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![Illustration montrant quatre barres de couleur, puis les mêmes barres avec des couleurs différentes](images/colortrans2.png)

<span data-ttu-id="ca22a-122">Le tableau suivant répertorie les vecteurs de couleur pour les quatre barres avant et après la translation rouge.</span><span class="sxs-lookup"><span data-stu-id="ca22a-122">The following table lists the color vectors for the four bars before and after the red translation.</span></span> <span data-ttu-id="ca22a-123">Notez que, étant donné que la valeur maximale d’un composant de couleur est 1, le composant rouge de la deuxième ligne ne change pas.</span><span class="sxs-lookup"><span data-stu-id="ca22a-123">Note that because the maximum value for a color component is 1, the red component in the second row does not change.</span></span> <span data-ttu-id="ca22a-124">(De même, la valeur minimale d’un composant de couleur est 0.)</span><span class="sxs-lookup"><span data-stu-id="ca22a-124">(Similarly, the minimum value for a color component is 0.)</span></span>



| <span data-ttu-id="ca22a-125">Original</span><span class="sxs-lookup"><span data-stu-id="ca22a-125">Original</span></span>           | <span data-ttu-id="ca22a-126">Traduit</span><span class="sxs-lookup"><span data-stu-id="ca22a-126">Translated</span></span>      |
|--------------------|-----------------|
| <span data-ttu-id="ca22a-127">Noir (0, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca22a-127">Black (0, 0, 0, 1)</span></span> | <span data-ttu-id="ca22a-128">(0.75, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca22a-128">(0.75, 0, 0, 1)</span></span> |
| <span data-ttu-id="ca22a-129">Rouge (1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca22a-129">Red (1, 0, 0, 1)</span></span>   | <span data-ttu-id="ca22a-130">(1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca22a-130">(1, 0, 0, 1)</span></span>    |
| <span data-ttu-id="ca22a-131">Vert (0, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca22a-131">Green (0, 1, 0, 1)</span></span> | <span data-ttu-id="ca22a-132">(0.75, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="ca22a-132">(0.75, 1, 0, 1)</span></span> |
| <span data-ttu-id="ca22a-133">Bleu (0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="ca22a-133">Blue (0, 0, 1, 1)</span></span>  | <span data-ttu-id="ca22a-134">(0.75, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="ca22a-134">(0.75, 0, 1, 1)</span></span> |



 

 

 



