---
description: Windows GDI+ fournit la classe image permettant d’utiliser des images raster (bitmaps) et des images vectorielles (sous-fichiers).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Utilisation d’images, de bitmaps et de reformateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445b37caa488fa4b83bcfb7792eb83f6ee1e6e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034352"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="368d4-103">Utilisation d’images, de bitmaps et de reformateurs</span><span class="sxs-lookup"><span data-stu-id="368d4-103">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="368d4-104">Windows GDI+ fournit la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) permettant d’utiliser des images raster (bitmaps) et des images vectorielles (sous-fichiers).</span><span class="sxs-lookup"><span data-stu-id="368d4-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="368d4-105">La classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) et la classe [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) héritent toutes deux de la classe **image** .</span><span class="sxs-lookup"><span data-stu-id="368d4-105">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="368d4-106">La classe **bitmap** développe les fonctionnalités de la classe **image** en fournissant des méthodes supplémentaires pour le chargement, l’enregistrement et la manipulation d’images raster.</span><span class="sxs-lookup"><span data-stu-id="368d4-106">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="368d4-107">La classe **Metafile** développe les fonctionnalités de la classe **image** en fournissant des méthodes supplémentaires pour l’enregistrement et l’examen d’images vectorielles.</span><span class="sxs-lookup"><span data-stu-id="368d4-107">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="368d4-108">Les rubriques suivantes couvrent plus en détail les classes [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)et [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) :</span><span class="sxs-lookup"><span data-stu-id="368d4-108">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="368d4-109">Chargement et affichage des bitmaps</span><span class="sxs-lookup"><span data-stu-id="368d4-109">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="368d4-110">Chargement et affichage des fichiers de présentation</span><span class="sxs-lookup"><span data-stu-id="368d4-110">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="368d4-111">Enregistrement des fichiers de sous-fichier</span><span class="sxs-lookup"><span data-stu-id="368d4-111">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="368d4-112">Rognage et mise à l’échelle d’images</span><span class="sxs-lookup"><span data-stu-id="368d4-112">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="368d4-113">Rotation, réflexion et inclinaison des images</span><span class="sxs-lookup"><span data-stu-id="368d4-113">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="368d4-114">Utilisation du mode d’interpolation pour contrôler la qualité d’image pendant la mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="368d4-114">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="368d4-115">Création d’images miniatures</span><span class="sxs-lookup"><span data-stu-id="368d4-115">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="368d4-116">Utilisation d’une image bitmap mise en cache pour améliorer les performances</span><span class="sxs-lookup"><span data-stu-id="368d4-116">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="368d4-117">Amélioration des performances en évitant la mise à l’échelle automatique</span><span class="sxs-lookup"><span data-stu-id="368d4-117">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="368d4-118">Lecture et écriture de métadonnées</span><span class="sxs-lookup"><span data-stu-id="368d4-118">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



