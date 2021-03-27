---
description: La fonction SetDIBitsToDevice utilise des données de couleur d’un DIB pour définir les pixels du rectangle spécifié sur l’appareil associé au contexte de périphérique de destination.
ms.assetid: 7cbb2b7a-2d95-4352-9e75-aa814e8f01bd
title: Test d’une imprimante pour la prise en charge JPEG ou PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151251a99d23913b2a515a36def6172c997ac31c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951719"
---
# <a name="testing-a-printer-for-jpeg-or-png-support"></a><span data-ttu-id="b7fac-103">Test d’une imprimante pour la prise en charge JPEG ou PNG</span><span class="sxs-lookup"><span data-stu-id="b7fac-103">Testing a Printer for JPEG or PNG Support</span></span>

<span data-ttu-id="b7fac-104">La fonction [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) utilise des données de couleur d’un DIB pour définir les pixels du rectangle spécifié sur l’appareil associé au contexte de périphérique de destination.</span><span class="sxs-lookup"><span data-stu-id="b7fac-104">The [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) function uses color data from a DIB to set the pixels in the specified rectangle on the device that is associated with the destination device context.</span></span>

<span data-ttu-id="b7fac-105">[**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) est étendu pour permettre à une image JPEG ou png d’être transmise en tant qu’image source.</span><span class="sxs-lookup"><span data-stu-id="b7fac-105">[**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) is extended to allow a JPEG or PNG image to be passed as the source image.</span></span>

<span data-ttu-id="b7fac-106">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b7fac-106">For example:</span></span>


```C++
// 
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
               pvJpgImage, nJpgImageSize, sizeof(ul), &ul) > 0) &&

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
    // Do the SetDIBitsToDevice. 
    // 

    iRet = SetDIBitsToDevice(hdc,
                             ulDstX, ulDstY,
                             ulDstWidth, ulDstHeight,
                             0, 0,
                             0, ulJpgHeight,
                             pvJpgImage,
                             &bmi,
                             DIB_RGB_COLORS);

    if (iRet == GDI_ERROR)
        return FALSE;
}
else
{
    // 
    // Decompress image into a DIB and call SetDIBitsToDevice  
    // with the DIB instead. 
    // 
}
```



 

 



