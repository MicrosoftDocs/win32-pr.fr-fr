---
description: Pour afficher une image raster (bitmap) sur l’écran, vous avez besoin d’un objet image et d’un objet Graphics.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Chargement et affichage des bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: db3ec9e1d586a585380123aa01d9553ad1f57f60efb93c28d2d974f54d56b249
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114999"
---
# <a name="loading-and-displaying-bitmaps"></a>Chargement et affichage des bitmaps

consultez également la [visionneuse WIC GDI+ exemple d’application](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).

Pour afficher une image raster (bitmap) sur l’écran, vous avez besoin d’un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Transmettez le nom d’un fichier (ou d’un pointeur vers un flux) à un constructeur d' **image** . Après avoir créé un objet **image** , transmettez l’adresse de cet objet **image** à la méthode **DrawImage** d’un objet **Graphics** .

L’exemple suivant crée un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir d’un fichier JPEG, puis dessine l’image avec son angle supérieur gauche à (60, 10) :

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

L’illustration suivante montre l’image dessinée à l’emplacement spécifié.

![capture d’écran d’une fenêtre qui contient une image, avec une légende pour le point d’origine ](images/imageposition1.png)

La classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fournit des méthodes de base pour charger et afficher des images pixellisées et des images vectorielles. La classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , qui hérite de la classe **image** , fournit des méthodes plus spécialisées pour le chargement, l’affichage et la manipulation d’images raster. Par exemple, vous pouvez construire un objet **bitmap** à partir d’un handle d’icône (HICON).

L’exemple suivant obtient un handle pour une icône, puis utilise ce handle pour construire un objet [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . Le code affiche l’icône en passant l’adresse de l’objet **bitmap** à la méthode **DrawImage** d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a>Voir aussi

[visionneuse WIC GDI+ exemple d’application](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
