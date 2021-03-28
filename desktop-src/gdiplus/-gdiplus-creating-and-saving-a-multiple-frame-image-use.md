---
description: Avec certains formats de fichiers, vous pouvez enregistrer plusieurs images (frames) dans un seul fichier.
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: Création et enregistrement d’une image multiframe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532a8fc8f8fc7e8742651f3d3853e001d493609b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115239"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a>Création et enregistrement d’une image multiframe

Avec certains formats de fichiers, vous pouvez enregistrer plusieurs images (frames) dans un seul fichier. Par exemple, vous pouvez enregistrer plusieurs pages dans un seul fichier TIFF. Pour enregistrer la première page, appelez la méthode [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) de la classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) . Pour enregistrer les pages suivantes, appelez la méthode [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) de la classe **image** .

> [!Note]  
> Vous ne pouvez pas utiliser [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) pour ajouter des frames à un fichier GIF animé.

 

L’application console suivante crée un fichier TIFF avec quatre pages. Les images qui deviennent les pages du fichier TIFF proviennent de quatre fichiers disque : Shapes.bmp, Cereal.gif, Iron.jpg et House.png. Code First construit quatre objets [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) : **multi**, **page2**, **page3** et **page4**. Au début, le **multiple** contient uniquement l’image de Shapes.bmp, mais finit par contenir les quatre images. Au fur et à mesure que les pages individuelles sont ajoutées à l’objet **multi**-**image** , elles sont également ajoutées au fichier disque multiframe. TIF.  

Notez que le code appelle [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (et non [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) pour enregistrer la première page. Le premier argument passé à la méthode Save est le nom du fichier de disque qui peut éventuellement contenir plusieurs frames. Le deuxième argument passé à la méthode Save spécifie l’encodeur qui sera utilisé pour convertir les données de l’objet **multi**-[**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) au format (dans ce cas, TIFF) requis par le fichier disque.   Ce même encodeur est utilisé automatiquement par tous les appels suivants à la méthode SaveAdd de l’objet **multi**-**image** .  

Le troisième argument passé à la méthode [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) est l’adresse d’un objet [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) . L’objet **EncoderParameters** a un tableau qui contient un seul objet [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Le membre **GUID** de cet objet **EncoderParameter** est défini sur EncoderSaveFlag. Le membre **value** de l’objet **EncoderParameter** pointe vers un **ULong** qui contient la valeur EncoderValueMultiFrame.

Le code enregistre les deuxième, troisième et quatrième pages en appelant la méthode [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) de l’objet **multi**-[**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .   Le premier argument passé à la méthode SaveAdd est l’adresse d’un objet **image** . L’image de cet objet **image** est ajoutée à l’objet **multi**-**image** et est également ajoutée au fichier de disque multiframe. TIF.   Le deuxième argument passé à la méthode SaveAdd est l’adresse du même objet [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) qui a été utilisé par la méthode [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) . La différence réside dans le fait que le **ULong** vers lequel pointe le membre **value** contient désormais la valeur EncoderValueFrameDimensionPage.

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

   EncoderParameters encoderParameters;
   ULONG             parameterValue;
   Status            stat;

   // An EncoderParameters object has an array of
   // EncoderParameter objects. In this case, there is only
   // one EncoderParameter object in the array.
   encoderParameters.Count = 1;

   // Initialize the one EncoderParameter object.
   encoderParameters.Parameter[0].Guid = EncoderSaveFlag;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;
   encoderParameters.Parameter[0].Value = &parameterValue;

   // Get the CLSID of the TIFF encoder.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/tiff", &encoderClsid);

   // Create four image objects.
   Image* multi = new Image(L"Shapes.bmp");
   Image* page2 = new Image(L"Cereal.gif");
   Image* page3 = new Image(L"Iron.jpg");
   Image* page4 = new Image(L"House.png");

   // Save the first page (frame).
   parameterValue = EncoderValueMultiFrame;
   stat = multi->Save(L"MultiFrame.tif", &encoderClsid, &encoderParameters);
   if(stat == Ok)
      printf("Page 1 saved successfully.\n");

   // Save the second page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page2, &encoderParameters);
   if(stat == Ok)
      printf("Page 2 saved successfully.\n");

   // Save the third page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page3, &encoderParameters);
   if(stat == Ok)
      printf("Page 3 saved successfully.\n");

   // Save the fourth page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page4, &encoderParameters);
   if(stat == Ok)
      printf("Page 4 saved successfully.\n");

   // Close the multiframe file.
   parameterValue = EncoderValueFlush;
   stat = multi->SaveAdd(&encoderParameters);
   if(stat == Ok)
      printf("File closed successfully.\n");

   delete multi;
   delete page2;
   delete page3;
   delete page4;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
