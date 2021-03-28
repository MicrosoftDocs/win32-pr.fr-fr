---
description: La classe image fournit des méthodes de base pour charger et afficher des images pixellisées et des images vectorielles. La classe Metafile, qui hérite de la classe image, fournit des méthodes plus spécialisées pour l’enregistrement, l’affichage et l’examen d’images vectorielles.
ms.assetid: 79b8df1b-6fc5-455b-9d08-57d64bf6bffa
title: Chargement et affichage des fichiers de présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5dafe6ef92e80e8487b43a22f50b44c5decd360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033966"
---
# <a name="loading-and-displaying-metafiles"></a><span data-ttu-id="dae6e-104">Chargement et affichage des fichiers de présentation</span><span class="sxs-lookup"><span data-stu-id="dae6e-104">Loading and Displaying Metafiles</span></span>

<span data-ttu-id="dae6e-105">La classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fournit des méthodes de base pour charger et afficher des images pixellisées et des images vectorielles.</span><span class="sxs-lookup"><span data-stu-id="dae6e-105">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="dae6e-106">La classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , qui hérite de la classe **image** , fournit des méthodes plus spécialisées pour l’enregistrement, l’affichage et l’examen d’images vectorielles.</span><span class="sxs-lookup"><span data-stu-id="dae6e-106">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the **Image** class, provides more specialized methods for recording, displaying, and examining vector images.</span></span>

<span data-ttu-id="dae6e-107">Pour afficher une image vectorielle (métafichier) sur l’écran, vous avez besoin d’un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="dae6e-107">To display a vector image (metafile) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="dae6e-108">Transmettez le nom d’un fichier (ou d’un pointeur vers un flux) à un constructeur d' **image** .</span><span class="sxs-lookup"><span data-stu-id="dae6e-108">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="dae6e-109">Après avoir créé un objet **image** , transmettez l’adresse de cet objet **image** à la méthode **DrawImage** d’un objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="dae6e-109">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="dae6e-110">L’exemple suivant crée un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir d’un fichier EMF (métafichier amélioré), puis dessine l’image avec son angle supérieur gauche à (60, 10) :</span><span class="sxs-lookup"><span data-stu-id="dae6e-110">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from an EMF (enhanced metafile) file and then draws the image with its upper-left corner at (60, 10):</span></span>


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



<span data-ttu-id="dae6e-111">L’illustration suivante montre l’image dessinée à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="dae6e-111">The following illustration shows the image drawn at the specified location.</span></span>

![capture d’écran d’une fenêtre qui contient une image et spécifie le point d’origine](images/imageposition2.png)

 

 



