---
description: Vous pouvez faire pivoter, réfléchir et incliner une image en spécifiant des points de destination pour les angles supérieur gauche, supérieur droit et inférieur gauche de l’image d’origine.
ms.assetid: 1e982d84-8749-451b-89a8-81440fcee439
title: Rotation, réflexion et inclinaison des images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637cb8be0290d96a164042086e997bc878c0227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951694"
---
# <a name="rotating-reflecting-and-skewing-images"></a><span data-ttu-id="f2d46-103">Rotation, réflexion et inclinaison des images</span><span class="sxs-lookup"><span data-stu-id="f2d46-103">Rotating, Reflecting, and Skewing Images</span></span>

<span data-ttu-id="f2d46-104">Vous pouvez faire pivoter, réfléchir et incliner une image en spécifiant des points de destination pour les angles supérieur gauche, supérieur droit et inférieur gauche de l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="f2d46-104">You can rotate, reflect, and skew an image by specifying destination points for the upper-left, upper-right, and lower-left corners of the original image.</span></span> <span data-ttu-id="f2d46-105">Les trois points de destination déterminent une transformation affine qui mappe l’image rectangulaire d’origine à un parallélogramme.</span><span class="sxs-lookup"><span data-stu-id="f2d46-105">The three destination points determine an affine transformation that maps the original rectangular image to a parallelogram.</span></span> <span data-ttu-id="f2d46-106">(Le coin inférieur droit de l’image d’origine est mappé au quatrième angle du parallélogramme, qui est calculé à partir des trois points de destination spécifiés.)</span><span class="sxs-lookup"><span data-stu-id="f2d46-106">(The lower-right corner of the original image is mapped to the fourth corner of the parallelogram, which is calculated from the three specified destination points.)</span></span>

<span data-ttu-id="f2d46-107">Supposons, par exemple, que l’image d’origine soit un rectangle avec l’angle supérieur gauche à (0, 0), le coin supérieur droit à (100, 0) et l’angle inférieur gauche à (0, 50).</span><span class="sxs-lookup"><span data-stu-id="f2d46-107">For example, suppose the original image is a rectangle with upper-left corner at (0, 0), upper-right corner at (100, 0), and lower-left corner at (0, 50).</span></span> <span data-ttu-id="f2d46-108">Supposons à présent que nous puissions mapper ces trois points aux points de destination comme suit.</span><span class="sxs-lookup"><span data-stu-id="f2d46-108">Now suppose we map those three points to destination points as follows.</span></span>



| <span data-ttu-id="f2d46-109">Point d’origine</span><span class="sxs-lookup"><span data-stu-id="f2d46-109">Original point</span></span>       | <span data-ttu-id="f2d46-110">Point de destination</span><span class="sxs-lookup"><span data-stu-id="f2d46-110">Destination point</span></span> |
|----------------------|-------------------|
| <span data-ttu-id="f2d46-111">En haut à gauche (0, 0)</span><span class="sxs-lookup"><span data-stu-id="f2d46-111">Upper-left (0, 0)</span></span>    | <span data-ttu-id="f2d46-112">(200, 20)</span><span class="sxs-lookup"><span data-stu-id="f2d46-112">(200, 20)</span></span>         |
| <span data-ttu-id="f2d46-113">En haut à droite (100, 0)</span><span class="sxs-lookup"><span data-stu-id="f2d46-113">Upper-right (100, 0)</span></span> | <span data-ttu-id="f2d46-114">(110, 100)</span><span class="sxs-lookup"><span data-stu-id="f2d46-114">(110, 100)</span></span>        |
| <span data-ttu-id="f2d46-115">En bas à gauche (0, 50)</span><span class="sxs-lookup"><span data-stu-id="f2d46-115">Lower-left (0, 50)</span></span>   | <span data-ttu-id="f2d46-116">(250, 30)</span><span class="sxs-lookup"><span data-stu-id="f2d46-116">(250, 30)</span></span>         |



 

<span data-ttu-id="f2d46-117">L’illustration suivante montre l’image d’origine et l’image mappée au parallélogramme.</span><span class="sxs-lookup"><span data-stu-id="f2d46-117">The following illustration shows the original image and the image mapped to the parallelogram.</span></span> <span data-ttu-id="f2d46-118">L’image d’origine a été inclinée, reflétée, pivotée et traduite.</span><span class="sxs-lookup"><span data-stu-id="f2d46-118">The original image has been skewed, reflected, rotated, and translated.</span></span> <span data-ttu-id="f2d46-119">L’axe des x le long du bord supérieur de l’image d’origine est mappé à la ligne qui s’exécute via (200, 20) et (110, 100).</span><span class="sxs-lookup"><span data-stu-id="f2d46-119">The x-axis along the top edge of the original image is mapped to the line that runs through (200, 20) and (110, 100).</span></span> <span data-ttu-id="f2d46-120">L’axe des y, le long du bord gauche de l’image d’origine, est mappé à la ligne qui s’exécute via (200, 20) et (250, 30).</span><span class="sxs-lookup"><span data-stu-id="f2d46-120">The y-axis along the left edge of the original image is mapped to the line that runs through (200, 20) and (250, 30).</span></span>

![Illustration montrant des bandes colorées à l’origine des axes de coordonnées et les mêmes rayures inclinées et à un emplacement, une rotation et une taille différents](images/stripes1.png)

<span data-ttu-id="f2d46-122">L’exemple suivant produit les images illustrées dans l’illustration précédente.</span><span class="sxs-lookup"><span data-stu-id="f2d46-122">The following example produces the images shown in the preceding illustration.</span></span>


```
Point destinationPoints[] = {
   Point(200, 20),   // destination for upper-left point of original
   Point(110, 100),  // destination for upper-right point of original
   Point(250, 30)};  // destination for lower-left point of original
Image image(L"Stripes.bmp");
// Draw the image unaltered with its upper-left corner at (0, 0).
graphics.DrawImage(&image, 0, 0);
// Draw the image mapped to the parallelogram.
graphics.DrawImage(&image, destinationPoints, 3); 
```



<span data-ttu-id="f2d46-123">L’illustration suivante montre une transformation similaire appliquée à une image photographique.</span><span class="sxs-lookup"><span data-stu-id="f2d46-123">The following illustration shows a similar transformation applied to a photographic image.</span></span>

![Illustration montrant deux fois la même photo ; la seconde est inversée, inclinée et a une taille, une rotation et un emplacement différents](images/transformedclimber.png)

<span data-ttu-id="f2d46-125">L’illustration suivante montre une transformation similaire appliquée à un métafichier.</span><span class="sxs-lookup"><span data-stu-id="f2d46-125">The following illustration shows a similar transformation applied to a metafile.</span></span>

![Illustration montrant des formes et du texte, puis de nouveau mais inversée, inclinée et avec un emplacement, une rotation et une taille différents](images/transformedmetafile.png)

 

 



