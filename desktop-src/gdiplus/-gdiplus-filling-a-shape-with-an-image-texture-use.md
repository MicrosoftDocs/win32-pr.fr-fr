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
# <a name="filling-a-shape-with-an-image-texture"></a>Remplissage d’une forme avec une texture d’image

Vous pouvez remplir une forme fermée avec une texture à l’aide de la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et de la classe [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .

L’exemple suivant remplit une ellipse avec une image. Le code construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , puis passe l’adresse de cet objet **image** comme argument à un constructeur [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) . La troisième instruction de code met à l’échelle l’image, et la quatrième instruction remplit l’ellipse avec des copies répétées de l’image mise à l’échelle :


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



Dans l’exemple de code précédent, la méthode [**TextureBrush :: setTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) définit la transformation qui est appliquée à l’image avant qu’elle ne soit dessinée. Supposons que l’image d’origine a une largeur de 640 pixels et une hauteur de 480 pixels. La transformation réduit l’image à 75 × 75, en définissant les valeurs de mise à l’échelle horizontale et verticale.

> [!Note]  
> Dans l’exemple précédent, la taille de l’image est de 75 × 75, et la taille de l’ellipse est 150 × 250. Étant donné que l’image est plus petite que l’ellipse qu’elle remplit, l’ellipse est en mosaïque avec l’image. La mosaïque signifie que l’image est répétée horizontalement et verticalement jusqu’à ce que la limite de la forme soit atteinte. Pour plus d’informations sur la mosaïque, consultez [juxtaposition d’une forme avec une image](-gdiplus-tiling-a-shape-with-an-image-use.md).

 

 

 



