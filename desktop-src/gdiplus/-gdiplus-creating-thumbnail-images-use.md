---
description: Une image miniature est une petite version d’une image. Vous pouvez créer une image miniature en appelant la méthode GetThumbnailImage d’un objet image.
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: Création d’images miniatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ac737a49bad85ecc25eeeef1266a02cdeb408f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563898"
---
# <a name="creating-thumbnail-images"></a><span data-ttu-id="ab23f-104">Création d’images miniatures</span><span class="sxs-lookup"><span data-stu-id="ab23f-104">Creating Thumbnail Images</span></span>

<span data-ttu-id="ab23f-105">Une image miniature est une petite version d’une image.</span><span class="sxs-lookup"><span data-stu-id="ab23f-105">A thumbnail image is a small version of an image.</span></span> <span data-ttu-id="ab23f-106">Vous pouvez créer une image miniature en appelant la méthode **GetThumbnailImage** d’un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="ab23f-106">You can create a thumbnail image by calling the **GetThumbnailImage** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span>

<span data-ttu-id="ab23f-107">L’exemple suivant construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier Compass.bmp.</span><span class="sxs-lookup"><span data-stu-id="ab23f-107">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Compass.bmp.</span></span> <span data-ttu-id="ab23f-108">L’image d’origine a une largeur de 640 pixels et une hauteur de 479 pixels.</span><span class="sxs-lookup"><span data-stu-id="ab23f-108">The original image has a width of 640 pixels and a height of 479 pixels.</span></span> <span data-ttu-id="ab23f-109">Le code crée une image miniature qui a une largeur de 100 pixels et une hauteur de 100 pixels.</span><span class="sxs-lookup"><span data-stu-id="ab23f-109">The code creates a thumbnail image that has a width of 100 pixels and a height of 100 pixels.</span></span>


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



<span data-ttu-id="ab23f-110">L’illustration suivante montre l’image miniature.</span><span class="sxs-lookup"><span data-stu-id="ab23f-110">The following illustration shows the thumbnail image.</span></span>

![illustration d’un petit graphique montrant une boussole](images/thumbnail1.png)

 

 



