---
description: Windows GDI+ fournit la classe image et la classe Bitmap pour le stockage des images en mémoire et la manipulation d’images en mémoire.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Utilisation d’encodeurs et de décodeurs d’images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112935"
---
# <a name="using-image-encoders-and-decoders"></a><span data-ttu-id="b2773-103">Utilisation d’encodeurs et de décodeurs d’images</span><span class="sxs-lookup"><span data-stu-id="b2773-103">Using Image Encoders and Decoders</span></span>

<span data-ttu-id="b2773-104">Windows GDI+ fournit la classe [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) et la classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) pour le stockage des images en mémoire et la manipulation d’images en mémoire.</span><span class="sxs-lookup"><span data-stu-id="b2773-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class for storing images in memory and manipulating images in memory.</span></span> <span data-ttu-id="b2773-105">GDI+ écrit des images dans des fichiers sur disque à l’aide d’encodeurs d’images et charge des images à partir de fichiers disque à l’aide de décodeurs d’image.</span><span class="sxs-lookup"><span data-stu-id="b2773-105">GDI+ writes images to disk files with the help of image encoders and loads images from disk files with the help of image decoders.</span></span> <span data-ttu-id="b2773-106">Un encodeur convertit les données d’un objet **image** ou **bitmap** en un format de fichier de disque désigné.</span><span class="sxs-lookup"><span data-stu-id="b2773-106">An encoder translates the data in an **Image** or **Bitmap** object into a designated disk file format.</span></span> <span data-ttu-id="b2773-107">Un décodeur convertit les données d’un fichier de disque au format requis par les objets **image** et **bitmap** .</span><span class="sxs-lookup"><span data-stu-id="b2773-107">A decoder translates the data in a disk file to the format required by the **Image** and **Bitmap** objects.</span></span> <span data-ttu-id="b2773-108">GDI+ contient des encodeurs et des décodeurs intégrés qui prennent en charge les types de fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="b2773-108">GDI+ has built-in encoders and decoders that support the following file types:</span></span>

-   <span data-ttu-id="b2773-109">BMP</span><span class="sxs-lookup"><span data-stu-id="b2773-109">BMP</span></span>
-   <span data-ttu-id="b2773-110">GIF</span><span class="sxs-lookup"><span data-stu-id="b2773-110">GIF</span></span>
-   <span data-ttu-id="b2773-111">JPEG</span><span class="sxs-lookup"><span data-stu-id="b2773-111">JPEG</span></span>
-   <span data-ttu-id="b2773-112">PNG</span><span class="sxs-lookup"><span data-stu-id="b2773-112">PNG</span></span>
-   <span data-ttu-id="b2773-113">TIFF</span><span class="sxs-lookup"><span data-stu-id="b2773-113">TIFF</span></span>

<span data-ttu-id="b2773-114">GDI+ possède également des décodeurs intégrés qui prennent en charge les types de fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="b2773-114">GDI+ also has built-in decoders that support the following file types:</span></span>

-   <span data-ttu-id="b2773-115">WMF</span><span class="sxs-lookup"><span data-stu-id="b2773-115">WMF</span></span>
-   <span data-ttu-id="b2773-116">EMF</span><span class="sxs-lookup"><span data-stu-id="b2773-116">EMF</span></span>
-   <span data-ttu-id="b2773-117">ICON</span><span class="sxs-lookup"><span data-stu-id="b2773-117">ICON</span></span>

<span data-ttu-id="b2773-118">Les rubriques suivantes décrivent plus en détail les encodeurs et les décodeurs :</span><span class="sxs-lookup"><span data-stu-id="b2773-118">The following topics discuss encoders and decoders in more detail:</span></span>

-   [<span data-ttu-id="b2773-119">Liste des encodeurs installés</span><span class="sxs-lookup"><span data-stu-id="b2773-119">Listing Installed Encoders</span></span>](-gdiplus-listing-installed-encoders-use.md)
-   [<span data-ttu-id="b2773-120">Liste des décodeurs installés</span><span class="sxs-lookup"><span data-stu-id="b2773-120">Listing Installed Decoders</span></span>](-gdiplus-listing-installed-decoders-use.md)
-   [<span data-ttu-id="b2773-121">Récupération de l’identificateur de classe pour un encodeur</span><span class="sxs-lookup"><span data-stu-id="b2773-121">Retrieving the Class Identifier for an Encoder</span></span>](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [<span data-ttu-id="b2773-122">Détermination des paramètres pris en charge par un encodeur</span><span class="sxs-lookup"><span data-stu-id="b2773-122">Determining the Parameters Supported by an Encoder</span></span>](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [<span data-ttu-id="b2773-123">Conversion d’une image BMP en image PNG</span><span class="sxs-lookup"><span data-stu-id="b2773-123">Converting a BMP Image to a PNG Image</span></span>](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [<span data-ttu-id="b2773-124">Définition du niveau de compression JPEG</span><span class="sxs-lookup"><span data-stu-id="b2773-124">Setting JPEG Compression Level</span></span>](-gdiplus-setting-jpeg-compression-level-use.md)
-   [<span data-ttu-id="b2773-125">Transformation d’une image JPEG sans perte d’informations</span><span class="sxs-lookup"><span data-stu-id="b2773-125">Transforming a JPEG Image Without Loss of Information</span></span>](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [<span data-ttu-id="b2773-126">Création et enregistrement d’une image multiframe</span><span class="sxs-lookup"><span data-stu-id="b2773-126">Creating and Saving a Multiple-Frame Image</span></span>](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [<span data-ttu-id="b2773-127">Copie de frames individuels à partir d’une image Multiple-Frame</span><span class="sxs-lookup"><span data-stu-id="b2773-127">Copying Individual Frames from a Multiple-Frame Image</span></span>](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



