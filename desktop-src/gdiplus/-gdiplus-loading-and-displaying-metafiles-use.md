---
description: La classe image fournit des méthodes de base pour charger et afficher des images pixellisées et des images vectorielles. La classe Metafile, qui hérite de la classe image, fournit des méthodes plus spécialisées pour l’enregistrement, l’affichage et l’examen d’images vectorielles.
ms.assetid: 79b8df1b-6fc5-455b-9d08-57d64bf6bffa
title: Chargement et affichage des fichiers de présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5dafe6ef92e80e8487b43a22f50b44c5decd360
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012425"
---
# <a name="loading-and-displaying-metafiles"></a>Chargement et affichage des fichiers de présentation

La classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fournit des méthodes de base pour charger et afficher des images pixellisées et des images vectorielles. La classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , qui hérite de la classe **image** , fournit des méthodes plus spécialisées pour l’enregistrement, l’affichage et l’examen d’images vectorielles.

Pour afficher une image vectorielle (métafichier) sur l’écran, vous avez besoin d’un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Transmettez le nom d’un fichier (ou d’un pointeur vers un flux) à un constructeur d' **image** . Après avoir créé un objet **image** , transmettez l’adresse de cet objet **image** à la méthode **DrawImage** d’un objet **Graphics** .

L’exemple suivant crée un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir d’un fichier EMF (métafichier amélioré), puis dessine l’image avec son angle supérieur gauche à (60, 10) :


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



L’illustration suivante montre l’image dessinée à l’emplacement spécifié.

![capture d’écran d’une fenêtre qui contient une image et spécifie le point d’origine](images/imageposition2.png)

 

 



