---
description: L’inclinaison augmente ou diminue un composant de couleur d’un montant proportionnel à un autre composant de couleur.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Cisaillement des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115215"
---
# <a name="shearing-colors"></a><span data-ttu-id="f5f77-103">Cisaillement des couleurs</span><span class="sxs-lookup"><span data-stu-id="f5f77-103">Shearing Colors</span></span>

<span data-ttu-id="f5f77-104">L’inclinaison augmente ou diminue un composant de couleur d’un montant proportionnel à un autre composant de couleur.</span><span class="sxs-lookup"><span data-stu-id="f5f77-104">Shearing increases or decreases a color component by an amount proportional to another color component.</span></span> <span data-ttu-id="f5f77-105">Par exemple, considérez la transformation dans laquelle le composant rouge augmente d’une moitié la valeur du composant bleu.</span><span class="sxs-lookup"><span data-stu-id="f5f77-105">For example, consider the transformation where the red component is increased by one half the value of the blue component.</span></span> <span data-ttu-id="f5f77-106">Dans une telle transformation, la couleur (0,2, 0,5, 1) devient (0,7, 0,5, 1).</span><span class="sxs-lookup"><span data-stu-id="f5f77-106">Under such a transformation, the color (0.2, 0.5, 1) would become (0.7, 0.5, 1).</span></span> <span data-ttu-id="f5f77-107">Le nouveau composant rouge est 0,2 + (1/2) (1) = 0,7.</span><span class="sxs-lookup"><span data-stu-id="f5f77-107">The new red component is 0.2 + (1/2)(1) = 0.7.</span></span>

<span data-ttu-id="f5f77-108">L’exemple suivant construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier ColorBars4.bmp.</span><span class="sxs-lookup"><span data-stu-id="f5f77-108">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file ColorBars4.bmp.</span></span> <span data-ttu-id="f5f77-109">Ensuite, le code applique la transformation d’inclinaison décrite dans le paragraphe précédent à chaque pixel de l’image.</span><span class="sxs-lookup"><span data-stu-id="f5f77-109">Then the code applies the shearing transformation described in the preceding paragraph to each pixel in the image.</span></span>


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
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



<span data-ttu-id="f5f77-110">L’illustration suivante montre l’image d’origine à gauche et l’image déformée à droite.</span><span class="sxs-lookup"><span data-stu-id="f5f77-110">The following illustration shows the original image on the left and the sheared image on the right.</span></span>

![Illustration montrant quatre barres de couleur, puis les mêmes barres avec des couleurs différentes](images/colortrans6.png)

<span data-ttu-id="f5f77-112">Le tableau suivant présente les vecteurs de couleur pour les quatre barres avant et après la transformation d’inclinaison.</span><span class="sxs-lookup"><span data-stu-id="f5f77-112">The following table shows the color vectors for the four bars before and after the shearing transformation.</span></span>



| <span data-ttu-id="f5f77-113">Original</span><span class="sxs-lookup"><span data-stu-id="f5f77-113">Original</span></span>           | <span data-ttu-id="f5f77-114">En cisaille</span><span class="sxs-lookup"><span data-stu-id="f5f77-114">Sheared</span></span>            |
|--------------------|--------------------|
| <span data-ttu-id="f5f77-115">(0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="f5f77-115">(0, 0, 1, 1)</span></span>       | <span data-ttu-id="f5f77-116">(0.5, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="f5f77-116">(0.5, 0, 1, 1)</span></span>     |
| <span data-ttu-id="f5f77-117">(0.5, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="f5f77-117">(0.5, 1, 0.5, 1)</span></span>   | <span data-ttu-id="f5f77-118">(0.75, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="f5f77-118">(0.75, 1, 0.5, 1)</span></span>  |
| <span data-ttu-id="f5f77-119">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="f5f77-119">(1, 1, 0, 1)</span></span>       | <span data-ttu-id="f5f77-120">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="f5f77-120">(1, 1, 0, 1)</span></span>       |
| <span data-ttu-id="f5f77-121">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="f5f77-121">(0.4, 0.4, 0.4, 1)</span></span> | <span data-ttu-id="f5f77-122">(0.6, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="f5f77-122">(0.6, 0.4, 0.4, 1)</span></span> |



 

 

 



