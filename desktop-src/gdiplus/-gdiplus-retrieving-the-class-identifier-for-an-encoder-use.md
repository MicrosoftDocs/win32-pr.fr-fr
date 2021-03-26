---
description: La fonction GetEncoderClsid de l’exemple suivant reçoit le type MIME d’un encodeur et retourne l’identificateur de classe (CLSID) de cet encodeur.
ms.assetid: f78dac7c-4bc1-4614-8a26-d99d5619399a
title: Récupération de l’identificateur de classe pour un encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03193bfa9f2e86e92f66a649280828f12d4807c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972846"
---
# <a name="retrieving-the-class-identifier-for-an-encoder"></a><span data-ttu-id="1c232-103">Récupération de l’identificateur de classe pour un encodeur</span><span class="sxs-lookup"><span data-stu-id="1c232-103">Retrieving the Class Identifier for an Encoder</span></span>

<span data-ttu-id="1c232-104">La fonction GetEncoderClsid de l’exemple suivant reçoit le type MIME d’un encodeur et retourne l’identificateur de classe (**CLSID**) de cet encodeur.</span><span class="sxs-lookup"><span data-stu-id="1c232-104">The function GetEncoderClsid in the following example receives the MIME type of an encoder and returns the class identifier (**CLSID**) of that encoder.</span></span> <span data-ttu-id="1c232-105">Les types MIME des encodeurs intégrés à Windows GDI+ sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="1c232-105">The MIME types of the encoders built into Windows GDI+ are as follows:</span></span>

-   <span data-ttu-id="1c232-106">image/bmp</span><span class="sxs-lookup"><span data-stu-id="1c232-106">image/bmp</span></span>
-   <span data-ttu-id="1c232-107">image/jpeg</span><span class="sxs-lookup"><span data-stu-id="1c232-107">image/jpeg</span></span>
-   <span data-ttu-id="1c232-108">image/gif</span><span class="sxs-lookup"><span data-stu-id="1c232-108">image/gif</span></span>
-   <span data-ttu-id="1c232-109">image/tiff</span><span class="sxs-lookup"><span data-stu-id="1c232-109">image/tiff</span></span>
-   <span data-ttu-id="1c232-110">image/png</span><span class="sxs-lookup"><span data-stu-id="1c232-110">image/png</span></span>

<span data-ttu-id="1c232-111">La fonction appelle [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) pour récupérer un tableau d’objets [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="1c232-111">The function calls [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) to get an array of [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) objects.</span></span> <span data-ttu-id="1c232-112">Si l’un des objets **ImageCodecInfo** de ce tableau représente l’encodeur demandé, la fonction retourne l’index de l’objet **ImageCodecInfo** et copie le **CLSID** dans la variable vers laquelle pointe **pClsid**.</span><span class="sxs-lookup"><span data-stu-id="1c232-112">If one of the **ImageCodecInfo** objects in that array represents the requested encoder, the function returns the index of the **ImageCodecInfo** object and copies the **CLSID** into the variable pointed to by **pClsid**.</span></span> <span data-ttu-id="1c232-113">Si la fonction échoue, elle retourne-1.</span><span class="sxs-lookup"><span data-stu-id="1c232-113">If the function fails, it returns –1.</span></span>


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



<span data-ttu-id="1c232-114">L’application console suivante appelle la fonction GetEncoderClsid pour déterminer le **CLSID** de l’encodeur png :</span><span class="sxs-lookup"><span data-stu-id="1c232-114">The following console application calls the GetEncoderClsid function to determine the **CLSID** of the PNG encoder:</span></span>


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



<span data-ttu-id="1c232-115">Lorsque vous exécutez l’application console précédente, vous recevez une sortie similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="1c232-115">When you run the preceding console application, you get an output similar to the following:</span></span>


```
An ImageCodecInfo object representing the PNG encoder
was found at position 4 in the array.
The CLSID of the PNG encoder is {557CF406-1A04-11D3-9A73-0000F81EF32E}.
```



 

 
