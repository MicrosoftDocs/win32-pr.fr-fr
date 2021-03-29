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
# <a name="sizing-a-jpeg-or-png-image"></a><span data-ttu-id="12b7d-103">Dimensionnement d’une image JPEG ou PNG</span><span class="sxs-lookup"><span data-stu-id="12b7d-103">Sizing a JPEG or PNG Image</span></span>

<span data-ttu-id="12b7d-104">La fonction [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) copie les données de couleur pour un rectangle de pixels dans un DIB vers le rectangle de destination spécifié.</span><span class="sxs-lookup"><span data-stu-id="12b7d-104">The [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) function copies the color data for a rectangle of pixels in a DIB to the specified destination rectangle.</span></span> <span data-ttu-id="12b7d-105">Si le rectangle de destination est plus grand que le rectangle source, cette fonction étire les lignes et les colonnes de données de couleur en fonction du rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="12b7d-105">If the destination rectangle is larger than the source rectangle, this function stretches the rows and columns of color data to fit the destination rectangle.</span></span> <span data-ttu-id="12b7d-106">Si le rectangle de destination est plus petit que le rectangle source, **StretchDIBits** compresse les lignes et les colonnes à l’aide de l’opération Raster spécifiée.</span><span class="sxs-lookup"><span data-stu-id="12b7d-106">If the destination rectangle is smaller than the source rectangle, **StretchDIBits** compresses the rows and columns by using the specified raster operation.</span></span>

<span data-ttu-id="12b7d-107">[**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) est étendu pour permettre à une image JPEG ou png d’être transmise en tant qu’image source.</span><span class="sxs-lookup"><span data-stu-id="12b7d-107">[**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) is extended to allow a JPEG or PNG image to be passed as the source image.</span></span>

<span data-ttu-id="12b7d-108">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="12b7d-108">For example:</span></span>


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



 

 



