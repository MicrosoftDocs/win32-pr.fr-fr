---
description: 'Les méthodes image :: Save et image :: SaveAdd méthodes de la classe image reçoivent un objet EncoderParameters qui contient un tableau d’objets EncoderParameter.'
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Constantes d’encodeur d’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a47f533a490fe3428964c9e469df6fbe89800f95bfe89daf7bf05d6c49a75c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248883"
---
# <a name="image-encoder-constants"></a>Constantes d’encodeur d’image

Les méthodes [image :: Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) et [image :: SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) méthodes de la classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) reçoivent un objet [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) qui contient un tableau d’objets [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Chaque objet **EncoderParameter** a un membre de données GUID qui spécifie la catégorie de paramètre. Les constantes suivantes, définies dans Gdiplusimaging. h, représentent des GUID qui spécifient les différentes catégories de paramètres.

-   EncoderChrominanceTable
-   EncoderColorDepth
-   EncoderColorSpace
-   EncoderCompression
-   EncoderLuminanceTable
-   EncoderQuality
-   EncoderRenderMethod
-   EncoderSaveFlag
-   EncoderScanMethod
-   EncoderTransformation
-   EncoderVersion
-   EncoderImageItems
-   EncoderSaveAsCMYK

 

 
