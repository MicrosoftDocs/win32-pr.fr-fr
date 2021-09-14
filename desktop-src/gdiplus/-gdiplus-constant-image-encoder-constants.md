---
description: 'Les méthodes image :: Save et image :: SaveAdd méthodes de la classe image reçoivent un objet EncoderParameters qui contient un tableau d’objets EncoderParameter.'
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Constantes d’encodeur d’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8130b90ad7f1d559ca480a581a0b157ff152fc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120222"
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

 

 
