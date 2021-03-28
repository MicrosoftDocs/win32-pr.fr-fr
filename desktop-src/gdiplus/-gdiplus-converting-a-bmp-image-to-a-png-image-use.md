---
description: Pour enregistrer une image dans un fichier sur disque, appelez la méthode Save de la classe image.
ms.assetid: a95fa3ea-2013-45d5-bdec-61eddcefc2fa
title: Conversion d’une image BMP en image PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d165809bb4cfa7f37685b8b130e2b895b35c0ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991369"
---
# <a name="converting-a-bmp-image-to-a-png-image"></a><span data-ttu-id="7f31c-103">Conversion d’une image BMP en image PNG</span><span class="sxs-lookup"><span data-stu-id="7f31c-103">Converting a BMP Image to a PNG Image</span></span>

<span data-ttu-id="7f31c-104">Pour enregistrer une image dans un fichier sur disque, appelez la méthode [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de la classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="7f31c-104">To save an image to a disk file, call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="7f31c-105">L’application console suivante charge une image BMP à partir d’un fichier sur disque, convertit l’image au format PNG et enregistre l’image convertie dans un nouveau fichier de disque.</span><span class="sxs-lookup"><span data-stu-id="7f31c-105">The following console application loads a BMP image from a disk file, converts the image to the PNG format, and saves the converted image to a new disk file.</span></span> <span data-ttu-id="7f31c-106">La fonction main repose sur la fonction d’assistance GetEncoderClsid, qui est indiquée dans [récupération de l’identificateur de classe pour un encodeur](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="7f31c-106">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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

   CLSID   encoderClsid;
   Status  stat;
   Image*   image = new Image(L"Bird.bmp");

   // Get the CLSID of the PNG encoder.
   GetEncoderClsid(L"image/png", &encoderClsid);

   stat = image->Save(L"Bird.png", &encoderClsid, NULL);

   if(stat == Ok)
      printf("Bird.png was saved successfully\n");
   else
      printf("Failure: stat = %d\n", stat); 

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 



