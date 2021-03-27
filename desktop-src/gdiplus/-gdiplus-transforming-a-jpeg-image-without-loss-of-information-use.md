---
title: Transformation sans perte d’une image JPEG
description: Lorsque vous compressez une image JPEG, certaines des informations contenues dans l’image sont perdues.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ea7011f25a97a228c44bdb87ba09ca8b284ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972143"
---
# <a name="lossless-transform-of-a-jpeg-image"></a><span data-ttu-id="4749b-103">Transformation sans perte d’une image JPEG</span><span class="sxs-lookup"><span data-stu-id="4749b-103">Lossless transform of a JPEG image</span></span>

<span data-ttu-id="4749b-104">Lorsque vous compressez une image JPEG, certaines des informations contenues dans l’image sont perdues.</span><span class="sxs-lookup"><span data-stu-id="4749b-104">When you compress a JPEG image, some of the information in the image is lost.</span></span> <span data-ttu-id="4749b-105">Si vous ouvrez un fichier JPEG, que vous modifiez l’image et que vous l’enregistrez dans un autre fichier JPEG, la qualité diminue.</span><span class="sxs-lookup"><span data-stu-id="4749b-105">If you open a JPEG file, alter the image, and save it to another JPEG file, the quality will decrease.</span></span> <span data-ttu-id="4749b-106">Si vous répétez ce processus plusieurs fois, vous verrez une dégradation importante de la qualité de l’image.</span><span class="sxs-lookup"><span data-stu-id="4749b-106">If you repeat that process many times, you will see a substantial degradation in the image quality.</span></span>

<span data-ttu-id="4749b-107">Étant donné que le format JPEG est l’un des formats d’image les plus populaires sur le Web et que les gens aiment souvent modifier des images JPEG, GDI+ fournit les transformations suivantes qui peuvent être effectuées sur des images JPEG sans perte d’informations :</span><span class="sxs-lookup"><span data-stu-id="4749b-107">Because JPEG is one of the most popular image formats on the Web, and because people often like to modify JPEG images, GDI+ provides the following transformations that can be performed on JPEG images without loss of information:</span></span>

-   <span data-ttu-id="4749b-108">Faire pivoter de 90 degrés</span><span class="sxs-lookup"><span data-stu-id="4749b-108">Rotate 90 degrees</span></span>
-   <span data-ttu-id="4749b-109">Faire pivoter de 180 degrés</span><span class="sxs-lookup"><span data-stu-id="4749b-109">Rotate 180 degrees</span></span>
-   <span data-ttu-id="4749b-110">Faire pivoter de 270 degrés</span><span class="sxs-lookup"><span data-stu-id="4749b-110">Rotate 270 degrees</span></span>
-   <span data-ttu-id="4749b-111">Retourner horizontalement</span><span class="sxs-lookup"><span data-stu-id="4749b-111">Flip horizontally</span></span>
-   <span data-ttu-id="4749b-112">Retourner verticalement</span><span class="sxs-lookup"><span data-stu-id="4749b-112">Flip vertically</span></span>

<span data-ttu-id="4749b-113">Vous pouvez appliquer l’une des transformations indiquées dans la liste précédente lorsque vous appelez la méthode [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) d’un objet [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="4749b-113">You can apply one of the transformations shown in the preceding list when you call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="4749b-114">Si les conditions suivantes sont remplies, la transformation se poursuivra sans perte d’informations :</span><span class="sxs-lookup"><span data-stu-id="4749b-114">If the following conditions are met, then the transformation will proceed without loss of information:</span></span>

-   <span data-ttu-id="4749b-115">Le fichier utilisé pour construire l’objet [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) est un fichier JPEG.</span><span class="sxs-lookup"><span data-stu-id="4749b-115">The file used to construct the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object is a JPEG file.</span></span>
-   <span data-ttu-id="4749b-116">La largeur et la hauteur de l’image sont des multiples de 16.</span><span class="sxs-lookup"><span data-stu-id="4749b-116">The width and height of the image are both multiples of 16.</span></span>

<span data-ttu-id="4749b-117">Si la largeur et la hauteur de l’image ne sont pas des multiples de 16, GDI+ fera de son mieux pour préserver la qualité de l’image lorsque vous appliquez l’une des transformations de rotation ou de retournement présentées dans la liste précédente.</span><span class="sxs-lookup"><span data-stu-id="4749b-117">If the width and height of the image are not both multiples of 16, GDI+ will do its best to preserve the image quality when you apply one of the rotation or flipping transformations shown in the preceding list.</span></span>

<span data-ttu-id="4749b-118">Pour transformer une image JPEG, initialisez un objet [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) et transmettez l’adresse de cet objet à la méthode [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de la classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="4749b-118">To transform a JPEG image, initialize an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object and pass the address of that object to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="4749b-119">Initialisez l’objet **EncoderParameters** afin qu’il dispose d’un tableau qui se compose d’un objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="4749b-119">Initialize the **EncoderParameters** object so that it has an array that consists of one [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="4749b-120">Initialisez un objet **EncoderParameter** de sorte que son membre de **valeur** pointe vers une variable **ULong** qui contient l’un des éléments suivants de l’énumération [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :</span><span class="sxs-lookup"><span data-stu-id="4749b-120">Initialize that one **EncoderParameter** object so that its **Value** member points to a **ULONG** variable that holds one of the following elements of the [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>

-   <span data-ttu-id="4749b-121">EncoderValueTransformRotate90,</span><span class="sxs-lookup"><span data-stu-id="4749b-121">EncoderValueTransformRotate90,</span></span>
-   <span data-ttu-id="4749b-122">EncoderValueTransformRotate180,</span><span class="sxs-lookup"><span data-stu-id="4749b-122">EncoderValueTransformRotate180,</span></span>
-   <span data-ttu-id="4749b-123">EncoderValueTransformRotate270,</span><span class="sxs-lookup"><span data-stu-id="4749b-123">EncoderValueTransformRotate270,</span></span>
-   <span data-ttu-id="4749b-124">EncoderValueTransformFlipHorizontal,</span><span class="sxs-lookup"><span data-stu-id="4749b-124">EncoderValueTransformFlipHorizontal,</span></span>
-   <span data-ttu-id="4749b-125">EncoderValueTransformFlipVertical</span><span class="sxs-lookup"><span data-stu-id="4749b-125">EncoderValueTransformFlipVertical</span></span>

<span data-ttu-id="4749b-126">Définissez le membre **GUID** de l’objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) sur EncoderTransformation.</span><span class="sxs-lookup"><span data-stu-id="4749b-126">Set the **Guid** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object to EncoderTransformation.</span></span>

<span data-ttu-id="4749b-127">L’application console suivante crée un objet [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) à partir d’un fichier JPEG, puis enregistre l’image dans un nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="4749b-127">The following console application creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then saves the image to a new file.</span></span> <span data-ttu-id="4749b-128">Pendant le processus d’enregistrement, l’image est pivotée de 90 degrés.</span><span class="sxs-lookup"><span data-stu-id="4749b-128">During the save process, the image is rotated 90 degrees.</span></span> <span data-ttu-id="4749b-129">Si la largeur et la hauteur de l’image sont des multiples de 16, le processus de rotation et d’enregistrement de l’image n’entraîne aucune perte d’informations.</span><span class="sxs-lookup"><span data-stu-id="4749b-129">If the width and height of the image are both multiples of 16, the process of rotating and saving the image causes no loss of information.</span></span>

<span data-ttu-id="4749b-130">La fonction main repose sur la fonction d’assistance GetEncoderClsid, qui est indiquée dans [récupération de l’identificateur de classe pour un encodeur](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="4749b-130">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID             encoderClsid;
   EncoderParameters encoderParameters;
   ULONG             transformation;
   UINT              width;
   UINT              height;
   Status            stat;

   // Get a JPEG image from the disk.
   Image* image = new Image(L"Shapes.jpg");

   // Determine whether the width and height of the image 
   // are multiples of 16.
   width = image->GetWidth();
   height = image->GetHeight();

   printf("The width of the image is %u", width);
   if(width / 16.0 - width / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   printf("The height of the image is %u", height);
   if(height / 16.0 - height / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will set that value to EncoderValueTransformRotate90.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderTransformation;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Rotate and save the image.
   transformation = EncoderValueTransformRotate90;
   encoderParameters.Parameter[0].Value = &transformation;
   stat = image->Save(L"ShapesR90.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"ShapesR90.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"ShapesR90.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
