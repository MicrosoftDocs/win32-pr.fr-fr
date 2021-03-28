---
description: Pour afficher une image raster (bitmap) sur l’écran, vous avez besoin d’un objet image et d’un objet Graphics.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Chargement et affichage des bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "104982842"
---
# <a name="loading-and-displaying-bitmaps"></a><span data-ttu-id="9c8cd-103">Chargement et affichage des bitmaps</span><span class="sxs-lookup"><span data-stu-id="9c8cd-103">Loading and displaying bitmaps</span></span>

<span data-ttu-id="9c8cd-104">Consultez également l' [exemple d’application GDI+ de la visionneuse WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span><span class="sxs-lookup"><span data-stu-id="9c8cd-104">Also see the [WIC Viewer GDI+ sample app](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span></span>

<span data-ttu-id="9c8cd-105">Pour afficher une image raster (bitmap) sur l’écran, vous avez besoin d’un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="9c8cd-105">To display a raster image (bitmap) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="9c8cd-106">Transmettez le nom d’un fichier (ou d’un pointeur vers un flux) à un constructeur d' **image** .</span><span class="sxs-lookup"><span data-stu-id="9c8cd-106">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="9c8cd-107">Après avoir créé un objet **image** , transmettez l’adresse de cet objet **image** à la méthode **DrawImage** d’un objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="9c8cd-107">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="9c8cd-108">L’exemple suivant crée un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir d’un fichier JPEG, puis dessine l’image avec son angle supérieur gauche à (60, 10) :</span><span class="sxs-lookup"><span data-stu-id="9c8cd-108">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then draws the image with its upper-left corner at (60, 10):</span></span>

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

<span data-ttu-id="9c8cd-109">L’illustration suivante montre l’image dessinée à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="9c8cd-109">The following illustration shows the image drawn at the specified location.</span></span>

![<span data-ttu-id="9c8cd-110">capture d’écran d’une fenêtre qui contient une image, avec une légende pour le point d’origine</span><span class="sxs-lookup"><span data-stu-id="9c8cd-110">screen shot of a window that contains an image, with a callout for the origin point</span></span> ](images/imageposition1.png)

<span data-ttu-id="9c8cd-111">La classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fournit des méthodes de base pour charger et afficher des images pixellisées et des images vectorielles.</span><span class="sxs-lookup"><span data-stu-id="9c8cd-111">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="9c8cd-112">La classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , qui hérite de la classe **image** , fournit des méthodes plus spécialisées pour le chargement, l’affichage et la manipulation d’images raster.</span><span class="sxs-lookup"><span data-stu-id="9c8cd-112">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class, which inherits from the **Image** class, provides more specialized methods for loading, displaying, and manipulating raster images.</span></span> <span data-ttu-id="9c8cd-113">Par exemple, vous pouvez construire un objet **bitmap** à partir d’un handle d’icône (HICON).</span><span class="sxs-lookup"><span data-stu-id="9c8cd-113">For example, you can construct a **Bitmap** object from an icon handle (HICON).</span></span>

<span data-ttu-id="9c8cd-114">L’exemple suivant obtient un handle pour une icône, puis utilise ce handle pour construire un objet [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="9c8cd-114">The following example obtains a handle to an icon and then uses that handle to construct a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="9c8cd-115">Le code affiche l’icône en passant l’adresse de l’objet **bitmap** à la méthode **DrawImage** d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="9c8cd-115">The code displays the icon by passing the address of the **Bitmap** object to the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a><span data-ttu-id="9c8cd-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c8cd-116">See also</span></span>

[<span data-ttu-id="9c8cd-117">Exemple d’application GDI+ de visionneuse WIC</span><span class="sxs-lookup"><span data-stu-id="9c8cd-117">WIC Viewer GDI+ sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
