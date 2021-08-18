---
title: Transformation sans perte d’une image JPEG
description: Lorsque vous compressez une image JPEG, certaines des informations contenues dans l’image sont perdues.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67152084f95220db3fe7afecfa4be07b366a92b31eb713ec192a2805ecb42ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977289"
---
# <a name="lossless-transform-of-a-jpeg-image"></a>Transformation sans perte d’une image JPEG

Lorsque vous compressez une image JPEG, certaines des informations contenues dans l’image sont perdues. Si vous ouvrez un fichier JPEG, que vous modifiez l’image et que vous l’enregistrez dans un autre fichier JPEG, la qualité diminue. Si vous répétez ce processus plusieurs fois, vous verrez une dégradation importante de la qualité de l’image.

étant donné que le format JPEG est l’un des formats d’image les plus populaires sur le Web et que les gens aiment souvent modifier des images jpeg, GDI+ fournit les transformations suivantes qui peuvent être effectuées sur des images jpeg sans perte d’informations :

-   Faire pivoter de 90 degrés
-   Faire pivoter de 180 degrés
-   Faire pivoter de 270 degrés
-   Retourner horizontalement
-   Retourner verticalement

Vous pouvez appliquer l’une des transformations indiquées dans la liste précédente lorsque vous appelez la méthode [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) d’un objet [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Si les conditions suivantes sont remplies, la transformation se poursuivra sans perte d’informations :

-   Le fichier utilisé pour construire l’objet [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) est un fichier JPEG.
-   La largeur et la hauteur de l’image sont des multiples de 16.

si la largeur et la hauteur de l’image ne sont pas des multiples de 16, GDI+ fait de son mieux pour préserver la qualité de l’image lorsque vous appliquez l’une des transformations de rotation ou de retournement présentées dans la liste précédente.

Pour transformer une image JPEG, initialisez un objet [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) et transmettez l’adresse de cet objet à la méthode [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de la classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Initialisez l’objet **EncoderParameters** afin qu’il dispose d’un tableau qui se compose d’un objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Initialisez un objet **EncoderParameter** de sorte que son membre de **valeur** pointe vers une variable **ULong** qui contient l’un des éléments suivants de l’énumération [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) :

-   EncoderValueTransformRotate90,
-   EncoderValueTransformRotate180,
-   EncoderValueTransformRotate270,
-   EncoderValueTransformFlipHorizontal,
-   EncoderValueTransformFlipVertical

Définissez le membre **GUID** de l’objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) sur EncoderTransformation.

L’application console suivante crée un objet [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) à partir d’un fichier JPEG, puis enregistre l’image dans un nouveau fichier. Pendant le processus d’enregistrement, l’image est pivotée de 90 degrés. Si la largeur et la hauteur de l’image sont des multiples de 16, le processus de rotation et d’enregistrement de l’image n’entraîne aucune perte d’informations.

La fonction main repose sur la fonction d’assistance GetEncoderClsid, qui est indiquée dans [récupération de l’identificateur de classe pour un encodeur](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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



 

 
