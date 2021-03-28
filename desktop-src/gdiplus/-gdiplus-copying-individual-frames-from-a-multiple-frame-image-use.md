---
title: Copier des frames individuels à partir d’une image à plusieurs frames
description: L’exemple suivant récupère les frames individuels à partir d’un fichier TIFF à plusieurs frames.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6bdb5668bcebb9babcbcb7d07839694750aec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202430"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a><span data-ttu-id="7aa99-103">Copier des frames individuels à partir d’une image à plusieurs frames</span><span class="sxs-lookup"><span data-stu-id="7aa99-103">Copy individual frames from a multiple-frame image</span></span>

<span data-ttu-id="7aa99-104">L’exemple suivant récupère les frames individuels à partir d’un fichier TIFF à plusieurs frames.</span><span class="sxs-lookup"><span data-stu-id="7aa99-104">The following example retrieves the individual frames from a multiple-frame TIFF file.</span></span> <span data-ttu-id="7aa99-105">Une fois le fichier TIFF créé, les frames individuels ont été ajoutés à la dimension page (consultez [création et enregistrement d’une Image Multiple-Frame](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span><span class="sxs-lookup"><span data-stu-id="7aa99-105">When the TIFF file was created, the individual frames were added to the Page dimension (see [Creating and Saving a Multiple-Frame Image](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span></span> <span data-ttu-id="7aa99-106">Le code affiche chacune des quatre pages et enregistre chaque page dans un fichier de disque PNG distinct.</span><span class="sxs-lookup"><span data-stu-id="7aa99-106">The code displays each of the four pages and saves each page to a separate PNG disk file.</span></span>

<span data-ttu-id="7aa99-107">Le code construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier TIFF à plusieurs frames.</span><span class="sxs-lookup"><span data-stu-id="7aa99-107">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the multiple-frame TIFF file.</span></span> <span data-ttu-id="7aa99-108">Pour récupérer les frames individuels (pages), le code appelle la méthode [**image :: SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) de cet objet **image** .</span><span class="sxs-lookup"><span data-stu-id="7aa99-108">To retrieve the individual frames (pages), the code calls the [**Image::SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) method of that **Image** object.</span></span> <span data-ttu-id="7aa99-109">Le premier argument passé à la méthode **image :: SelectActiveFrame** est l’adresse d’un GUID qui spécifie la dimension dans laquelle les frames ont été précédemment ajoutés au fichier TIFF à plusieurs frames.</span><span class="sxs-lookup"><span data-stu-id="7aa99-109">The first argument passed to the **Image::SelectActiveFrame** method is the address of a GUID that specifies the dimension in which the frames were previously added to the multiple-frame TIFF file.</span></span> <span data-ttu-id="7aa99-110">Le GUID FrameDimensionPage est défini dans Gdiplusimaging. h.</span><span class="sxs-lookup"><span data-stu-id="7aa99-110">The GUID FrameDimensionPage is defined in Gdiplusimaging.h.</span></span> <span data-ttu-id="7aa99-111">Les autres GUID définis dans ce fichier d’en-tête sont FrameDimensionTime et FrameDimensionResolution.</span><span class="sxs-lookup"><span data-stu-id="7aa99-111">Other GUIDs defined in that header file are FrameDimensionTime and FrameDimensionResolution.</span></span> <span data-ttu-id="7aa99-112">Le deuxième argument passé à la méthode **image :: SelectActiveFrame** est l’index de base zéro de la page souhaitée.</span><span class="sxs-lookup"><span data-stu-id="7aa99-112">The second argument passed to the **Image::SelectActiveFrame** method is the zero-based index of the desired page.</span></span>

<span data-ttu-id="7aa99-113">Le code repose sur la fonction d’assistance GetEncoderClsid, qui est indiquée dans [récupération de l’identificateur de classe pour un encodeur](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="7aa99-113">The code relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
GUID   pageGuid = FrameDimensionPage;
CLSID  encoderClsid;
Image  multi(L"Multiframe.tif");

// Get the CLSID of the PNG encoder.
GetEncoderClsid(L"image/png", &encoderClsid);

// Display and save the first page (index 0).
multi.SelectActiveFrame(&pageGuid, 0);
graphics.DrawImage(&multi, 10, 10);
multi.Save(L"Page0.png", &encoderClsid, NULL);

// Display and save the second page.
multi.SelectActiveFrame(&pageGuid, 1);
graphics.DrawImage(&multi, 200, 10);
multi.Save(L"Page1.png", &encoderClsid, NULL);

// Display and save the third page.
multi.SelectActiveFrame(&pageGuid, 2);
graphics.DrawImage(&multi, 10, 150);
multi.Save(L"Page2.png", &encoderClsid, NULL);

// Display and save the fourth page.
multi.SelectActiveFrame(&pageGuid, 3);
graphics.DrawImage(&multi, 200, 150);
multi.Save(L"Page3.png", &encoderClsid, NULL);
```



<span data-ttu-id="7aa99-114">L’illustration suivante montre les pages individuelles affichées par le code précédent.</span><span class="sxs-lookup"><span data-stu-id="7aa99-114">The following illustration shows the individual pages as displayed by the preceding code.</span></span>

![Illustration montrant une forme géométrique, une photo couleur, une photo monochrome et une forme géométrique différente](images/multiframe1.png)

 

 



