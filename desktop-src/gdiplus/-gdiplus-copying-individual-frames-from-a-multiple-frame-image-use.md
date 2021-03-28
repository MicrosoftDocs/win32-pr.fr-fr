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
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a>Copier des frames individuels à partir d’une image à plusieurs frames

L’exemple suivant récupère les frames individuels à partir d’un fichier TIFF à plusieurs frames. Une fois le fichier TIFF créé, les frames individuels ont été ajoutés à la dimension page (consultez [création et enregistrement d’une Image Multiple-Frame](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)). Le code affiche chacune des quatre pages et enregistre chaque page dans un fichier de disque PNG distinct.

Le code construit un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier TIFF à plusieurs frames. Pour récupérer les frames individuels (pages), le code appelle la méthode [**image :: SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) de cet objet **image** . Le premier argument passé à la méthode **image :: SelectActiveFrame** est l’adresse d’un GUID qui spécifie la dimension dans laquelle les frames ont été précédemment ajoutés au fichier TIFF à plusieurs frames. Le GUID FrameDimensionPage est défini dans Gdiplusimaging. h. Les autres GUID définis dans ce fichier d’en-tête sont FrameDimensionTime et FrameDimensionResolution. Le deuxième argument passé à la méthode **image :: SelectActiveFrame** est l’index de base zéro de la page souhaitée.

Le code repose sur la fonction d’assistance GetEncoderClsid, qui est indiquée dans [récupération de l’identificateur de classe pour un encodeur](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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



L’illustration suivante montre les pages individuelles affichées par le code précédent.

![Illustration montrant une forme géométrique, une photo couleur, une photo monochrome et une forme géométrique différente](images/multiframe1.png)

 

 



