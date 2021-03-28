---
description: Si vous transmettez uniquement l’angle supérieur gauche d’une image à la méthode DrawImage, Windows GDI+ peut mettre à l’échelle l’image, ce qui réduit les performances.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Amélioration des performances en évitant la mise à l’échelle automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972875"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a><span data-ttu-id="1cdba-103">Amélioration des performances en évitant la mise à l’échelle automatique</span><span class="sxs-lookup"><span data-stu-id="1cdba-103">Improving Performance by Avoiding Automatic Scaling</span></span>

<span data-ttu-id="1cdba-104">Si vous transmettez uniquement l’angle supérieur gauche d’une image à la méthode **DrawImage** , Windows GDI+ peut mettre à l’échelle l’image, ce qui réduit les performances.</span><span class="sxs-lookup"><span data-stu-id="1cdba-104">If you pass only the upper-left corner of an image to the **DrawImage** method, Windows GDI+ might scale the image, which would decrease performance.</span></span>

<span data-ttu-id="1cdba-105">L’appel suivant à la méthode **DrawImage** spécifie un angle supérieur gauche de (50, 30), mais ne spécifie pas de rectangle de destination :</span><span class="sxs-lookup"><span data-stu-id="1cdba-105">The following call to the **DrawImage** method specifies an upper-left corner of (50, 30) but does not specify a destination rectangle:</span></span>


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



<span data-ttu-id="1cdba-106">Bien qu’il s’agisse de la version la plus simple de la méthode **DrawImage** en ce qui concerne le nombre d’arguments requis, elle n’est pas nécessairement la plus efficace.</span><span class="sxs-lookup"><span data-stu-id="1cdba-106">Although this is the easiest version of the **DrawImage** method in terms of the number of required arguments, it is not necessarily the most efficient.</span></span> <span data-ttu-id="1cdba-107">Si le nombre de points par pouce sur le périphérique d’affichage actuel est différent du nombre de points par pouce sur le périphérique où l’image a été créée, GDI+ met à l’échelle l’image afin que sa taille physique sur le périphérique d’affichage actuel soit aussi proche que possible de sa taille physique sur l’appareil où elle a été créée.</span><span class="sxs-lookup"><span data-stu-id="1cdba-107">If the number of dots per inch on the current display device is different than the number of dots per inch on the device where the image was created, GDI+ scales the image so that its physical size on the current display device is as close as possible to its physical size on the device where it was created.</span></span>

<span data-ttu-id="1cdba-108">Si vous souhaitez empêcher une telle mise à l’échelle, transmettez la largeur et la hauteur d’un rectangle de destination à la méthode **DrawImage** .</span><span class="sxs-lookup"><span data-stu-id="1cdba-108">If you want to prevent such scaling, pass the width and height of a destination rectangle to the **DrawImage** method.</span></span> <span data-ttu-id="1cdba-109">L’exemple suivant dessine la même image deux fois.</span><span class="sxs-lookup"><span data-stu-id="1cdba-109">The following example draws the same image twice.</span></span> <span data-ttu-id="1cdba-110">Dans le premier cas, la largeur et la hauteur du rectangle de destination ne sont pas spécifiées, et l’image est mise à l’échelle automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1cdba-110">In the first case, the width and height of the destination rectangle are not specified, and the image is automatically scaled.</span></span> <span data-ttu-id="1cdba-111">Dans le deuxième cas, la largeur et la hauteur (mesurées en pixels) du rectangle de destination sont spécifiées comme étant identiques à la largeur et à la hauteur de l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="1cdba-111">In the second case, the width and height (measured in pixels) of the destination rectangle are specified to be the same as the width and height of the original image.</span></span>


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



<span data-ttu-id="1cdba-112">L’illustration suivante montre l’image rendue deux fois.</span><span class="sxs-lookup"><span data-stu-id="1cdba-112">The following illustration shows the image rendered twice.</span></span>

![capture d’écran d’une fenêtre qui contient deux versions d’une image à des échelles différentes](images/scaledtexture1.png)

 

 



