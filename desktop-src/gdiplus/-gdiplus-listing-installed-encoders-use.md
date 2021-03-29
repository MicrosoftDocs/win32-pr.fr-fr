---
description: GDI+ fournit la fonction GetImageEncoders pour vous permettre de déterminer les encodeurs d’images disponibles sur votre ordinateur.
ms.assetid: a261cf61-b853-4208-984b-0d5040eb1667
title: Liste des encodeurs installés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f310e9d366cdacde019373724f2b9feb3b94aef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972867"
---
# <a name="listing-installed-encoders"></a>Liste des encodeurs installés

GDI+ fournit la fonction [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) pour vous permettre de déterminer les encodeurs d’images disponibles sur votre ordinateur. **GetImageEncoders** retourne un tableau d’objets [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) . Avant d’appeler **GetImageEncoders**, vous devez allouer une mémoire tampon suffisamment grande pour recevoir ce tableau. Vous pouvez appeler [**GetImageEncodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize) pour déterminer la taille de la mémoire tampon requise.

L’application console suivante répertorie les encodeurs d’images disponibles :


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  num;        // number of image encoders
   UINT  size;       // size, in bytes, of the image encoder array

   ImageCodecInfo* pImageCodecInfo;

   // How many encoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageEncodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageEncoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageEncoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfo, is a pointer to that buffer. 
   GetImageEncoders(num, size, pImageCodecInfo);

   // Display the graphics file format (MimeType)
   // for each ImageCodecInfo object.
   for(UINT j = 0; j < num; ++j)
   { 
      wprintf(L"%s\n", pImageCodecInfo[j].MimeType);   
   }

   free(pImageCodecInfo);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Lorsque vous exécutez l’application console précédente, la sortie est similaire à ce qui suit :


```
image/bmp
image/jpeg
image/gif
image/tiff
image/png
```



 

 
