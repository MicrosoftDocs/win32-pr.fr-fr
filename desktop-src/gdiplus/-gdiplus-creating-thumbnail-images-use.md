---
description: Une image miniature est une petite version d’une image. Vous pouvez créer une image miniature en appelant la méthode GetThumbnailImage d’un objet image.
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: Création d’images miniatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ac737a49bad85ecc25eeeef1266a02cdeb408f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413140"
---
# <a name="creating-thumbnail-images"></a>Création d’images miniatures

Une image miniature est une petite version d’une image. Vous pouvez créer une image miniature en appelant la méthode **GetThumbnailImage** d’un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .

L’exemple suivant construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier Compass.bmp. L’image d’origine a une largeur de 640 pixels et une hauteur de 479 pixels. Le code crée une image miniature qui a une largeur de 100 pixels et une hauteur de 100 pixels.


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



L’illustration suivante montre l’image miniature.

![illustration d’un petit graphique montrant une boussole](images/thumbnail1.png)

 

 



