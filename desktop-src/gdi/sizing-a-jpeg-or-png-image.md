---
description: La fonction StretchDIBits copie les données de couleur pour un rectangle de pixels dans un DIB vers le rectangle de destination spécifié.
ms.assetid: d4e3f631-3852-4cee-8e97-2244c39b200e
title: Dimensionnement d’une image JPEG ou PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cd5bf3cbef8bab80d45536d90bfdd10174c26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973094"
---
# <a name="sizing-a-jpeg-or-png-image"></a>Dimensionnement d’une image JPEG ou PNG

La fonction [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) copie les données de couleur pour un rectangle de pixels dans un DIB vers le rectangle de destination spécifié. Si le rectangle de destination est plus grand que le rectangle source, cette fonction étire les lignes et les colonnes de données de couleur en fonction du rectangle de destination. Si le rectangle de destination est plus petit que le rectangle source, **StretchDIBits** compresse les lignes et les colonnes à l’aide de l’opération Raster spécifiée.

[**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) est étendu pour permettre à une image JPEG ou png d’être transmise en tant qu’image source.

Par exemple :


```C++
// pvJpgImage points to a buffer containing the JPEG image 
// nJpgImageSize is the size of the buffer 
// ulJpgWidth is the width of the JPEG image 
// ulJpgHeight is the height of the JPEG image 
// 

// 
// Check if CHECKJPEGFORMAT is supported (device has JPEG support) 
// and use it to verify that device can handle the JPEG image. 
// 

ul = CHECKJPEGFORMAT;

if (
    // Check if CHECKJPEGFORMAT exists: 

    (ExtEscape(hdc, QUERYESCSUPPORT,
               sizeof(ul), &ul, 0, 0) > 0) &&

    // Check if CHECKJPEGFORMAT executed without error: 

    (ExtEscape(hdc, CHECKJPEGFORMAT,
               nJpgImageSize, pvJpgImage, sizeof(ul), &ul) > 0) &&

    // Check status code returned by CHECKJPEGFORMAT: 

    (ul == 1)
   )
{
    // 
    // Initialize the BITMAPINFO. 
    // 

    memset(&bmi, 0, sizeof(bmi));
    bmi.bmiHeader.biSize        = sizeof(BITMAPINFOHEADER);
    bmi.bmiHeader.biWidth       = ulJpgWidth;
    bmi.bmiHeader.biHeight      = -ulJpgHeight; // top-down image 
    bmi.bmiHeader.biPlanes      = 1;
    bmi.bmiHeader.biBitCount    = 0;
    bmi.bmiHeader.biCompression = BI_JPEG;
    bmi.bmiHeader.biSizeImage   = nJpgImageSize;

    // 
    // Do the StretchDIBits. 
    // 

    iRet = StretchDIBits(hdc,
                         // destination rectangle 
                         ulDstX, ulDstY, ulDstWidth, ulDstHeight,
                         // source rectangle 
                         0, 0, ulJpgWidth, ulJpgHeight,
                         pvJpgImage,
                         &bmi,
                         DIB_RGB_COLORS,
                         SRCCOPY);

    if (iRet == GDI_ERROR)
        return FALSE;
}
else
{
    // 
    // Decompress image into a DIB and call StretchDIBits  
    // with the DIB instead. 
    // 
}
```



 

 



