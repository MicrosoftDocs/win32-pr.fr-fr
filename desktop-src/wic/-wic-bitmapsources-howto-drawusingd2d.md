---
description: Cette rubrique décrit le processus de dessin d’un IWICBitmapSource à l’aide de Direct2D.
ms.assetid: 11d38c9a-775d-41f7-a193-37b702b29a96
title: Comment dessiner un BitmapSource à l’aide de Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6636bb1d0b0294e7d496ffd8839c645ad046bb256001b2abd1744714eb4c48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668699"
---
# <a name="how-to-draw-a-bitmapsource-using-direct2d"></a>Comment dessiner un BitmapSource à l’aide de Direct2D

Cette rubrique décrit le processus de dessin d’un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à l’aide de Direct2D.

Pour dessiner une source bitmap à l’aide de Direct2D

1.  Décodez une image source et obtenez une source bitmap. Dans cet exemple, une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) est utilisée pour décoder l’image et la première image de l’image est récupérée.

    ```C++
       // Create a decoder
       IWICBitmapDecoder *pDecoder = NULL;

       hr = m_pIWICFactory->CreateDecoderFromFilename(
           szFileName,                      // Image to be decoded
           NULL,                            // Do not prefer a particular vendor
           GENERIC_READ,                    // Desired read access to the file
           WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
           &pDecoder                        // Pointer to the decoder
           );

       // Retrieve the first frame of the image from the decoder
       IWICBitmapFrameDecode *pFrame = NULL;

       if (SUCCEEDED(hr))
       {
           hr = pDecoder->GetFrame(0, &pFrame);
       }
    ```

    

    Pour obtenir d’autres types de sources bitmap à dessiner, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

2.  Convertit la source bitmap en un format de pixel 32bppPBGRA.

    Pour que Direct2D puisse utiliser une image, il doit être converti au format de pixel 32bppPBGRA. Pour convertir le format d’image, utilisez la méthode [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) pour créer un objet [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) . Une fois créé, utilisez la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) pour effectuer la conversion.

    ```C++
       // Format convert the frame to 32bppPBGRA
       if (SUCCEEDED(hr))
       {
           SafeRelease(&m_pConvertedSourceBitmap);
           hr = m_pIWICFactory->CreateFormatConverter(&m_pConvertedSourceBitmap);
       }

       if (SUCCEEDED(hr))
       {
           hr = m_pConvertedSourceBitmap->Initialize(
               pFrame,                          // Input bitmap to convert
               GUID_WICPixelFormat32bppPBGRA,   // Destination pixel format
               WICBitmapDitherTypeNone,         // Specified dither pattern
               NULL,                            // Specify a particular palette 
               0.f,                             // Alpha threshold
               WICBitmapPaletteTypeCustom       // Palette translation type
               );
       }
    ```

    

3.  Créez un objet [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) pour le rendu sur un handle de fenêtre.

    ```C++
       // Create a D2D render target properties
       D2D1_RENDER_TARGET_PROPERTIES renderTargetProperties = D2D1::RenderTargetProperties();

       // Set the DPI to be the default system DPI to allow direct mapping
       // between image pixels and desktop pixels in different system DPI settings
       renderTargetProperties.dpiX = DEFAULT_DPI;
       renderTargetProperties.dpiY = DEFAULT_DPI;

       // Create a D2D render target
       D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

       hr = m_pD2DFactory->CreateHwndRenderTarget(
           renderTargetProperties,
           D2D1::HwndRenderTargetProperties(hWnd, size),
           &m_pRT
           );
    ```

    

    Pour plus d’informations sur les cibles de rendu, consultez [vue d’ensemble des cibles de rendu](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Direct2D.

4.  Créez un objet [ID2D1Bitmap](../direct2d/render-targets-overview.md) à l’aide de la méthode [ID2D1RenderTarget :: CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) .

    ```C++
        // D2DBitmap may have been released due to device loss. 
        // If so, re-create it from the source bitmap
        if (m_pConvertedSourceBitmap && !m_pD2DBitmap)
        {
            m_pRT->CreateBitmapFromWicBitmap(m_pConvertedSourceBitmap, NULL, &m_pD2DBitmap);
        }
    ```

    

5.  Dessinez le [ID2D1Bitmap](../direct2d/render-targets-overview.md) à l’aide de D2D [ID2D1RenderTarget ::D méthode rawbitmap](../direct2d/id2d1rendertarget-drawbitmap.md) .

    ```C++
        // Draws an image and scales it to the current window size
        if (m_pD2DBitmap)
        {
            m_pRT->DrawBitmap(m_pD2DBitmap, rectangle);
        }
    ```

    

Le code a été omis de cet exemple. Pour obtenir le code complet, consultez la [visionneuse d’images WIC à l’aide de l’exemple Direct2D](-wic-sample-d2d-viewer.md).

## <a name="see-also"></a>Voir aussi

[Guide de programmation](-wic-programming-guide.md)


[Référence](-wic-codec-reference.md)


[Exemples](-wic-samples.md)


[Direct2D](../direct2d/direct2d-portal.md)


 

 
