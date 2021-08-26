---
description: La fonction GetEncoderClsid de l’exemple suivant reçoit le type MIME d’un encodeur et retourne l’identificateur de classe (CLSID) de cet encodeur.
ms.assetid: f78dac7c-4bc1-4614-8a26-d99d5619399a
title: Récupération de l’identificateur de classe pour un encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a40c31c7ad997ed3e7525ff247019f6a41c681b9523dc523105bd5ba6c7ca6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014709"
---
# <a name="retrieving-the-class-identifier-for-an-encoder"></a>Récupération de l’identificateur de classe pour un encodeur

La fonction GetEncoderClsid de l’exemple suivant reçoit le type MIME d’un encodeur et retourne l’identificateur de classe (**CLSID**) de cet encodeur. les types MIME des encodeurs intégrés à Windows GDI+ sont les suivants :

-   image/bmp
-   image/jpeg
-   image/gif
-   image/tiff
-   image/png

La fonction appelle [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) pour récupérer un tableau d’objets [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) . Si l’un des objets **ImageCodecInfo** de ce tableau représente l’encodeur demandé, la fonction retourne l’index de l’objet **ImageCodecInfo** et copie le **CLSID** dans la variable vers laquelle pointe **pClsid**. Si la fonction échoue, elle retourne-1.


```
int GetEncoderClsid(const WCHAR* format, CLSID* pClsid)
{
   UINT  num = 0;          // number of image encoders
   UINT  size = 0;         // size of the image encoder array in bytes

   ImageCodecInfo* pImageCodecInfo = NULL;

   GetImageEncodersSize(&num, &size);
   if(size == 0)
      return -1;  // Failure

   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));
   if(pImageCodecInfo == NULL)
      return -1;  // Failure

   GetImageEncoders(num, size, pImageCodecInfo);

   for(UINT j = 0; j < num; ++j)
   {
      if( wcscmp(pImageCodecInfo[j].MimeType, format) == 0 )
      {
         *pClsid = pImageCodecInfo[j].Clsid;
         free(pImageCodecInfo);
         return j;  // Success
      }    
   }

   free(pImageCodecInfo);
   return -1;  // Failure
}
```



L’application console suivante appelle la fonction GetEncoderClsid pour déterminer le **CLSID** de l’encodeur png :


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

#include "GdiplusHelperFunctions.h"

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID  encoderClsid;
   INT    result;
   WCHAR  strGuid[39];

   result = GetEncoderClsid(L"image/png", &encoderClsid);

   if(result < 0)
   {
      printf("The PNG encoder is not installed.\n");
   }
   else
   {
      StringFromGUID2(encoderClsid, strGuid, 39);
      printf("An ImageCodecInfo object representing the PNG encoder\n");
      printf("was found at position %d in the array.\n", result);
      wprintf(L"The CLSID of the PNG encoder is %s.\n", strGuid);
   }

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Lorsque vous exécutez l’application console précédente, vous recevez une sortie similaire à ce qui suit :


```
An ImageCodecInfo object representing the PNG encoder
was found at position 4 in the array.
The CLSID of the PNG encoder is {557CF406-1A04-11D3-9A73-0000F81EF32E}.
```



 

 
