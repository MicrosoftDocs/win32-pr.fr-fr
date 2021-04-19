---
description: Cette rubrique décrit le processus de dessin d’un IWICBitmapSource à l’aide de Direct2D.
ms.assetid: 11d38c9a-775d-41f7-a193-37b702b29a96
title: Comment dessiner un BitmapSource à l’aide de Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6dfdddb7cd6f7ab7341eb3c13a9fe40b797f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534277"
---
# <a name="how-to-draw-a-bitmapsource-using-direct2d"></a><span data-ttu-id="4b5e0-103">Comment dessiner un BitmapSource à l’aide de Direct2D</span><span class="sxs-lookup"><span data-stu-id="4b5e0-103">How to Draw a BitmapSource Using Direct2D</span></span>

<span data-ttu-id="4b5e0-104">Cette rubrique décrit le processus de dessin d’un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à l’aide de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-104">This topic demonstrates the process for drawing an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) by using Direct2D.</span></span>

<span data-ttu-id="4b5e0-105">Pour dessiner une source bitmap à l’aide de Direct2D</span><span class="sxs-lookup"><span data-stu-id="4b5e0-105">To draw a bitmap source by using Direct2D</span></span>

1.  <span data-ttu-id="4b5e0-106">Décodez une image source et obtenez une source bitmap.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-106">Decode a source image and obtain a bitmap source.</span></span> <span data-ttu-id="4b5e0-107">Dans cet exemple, une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) est utilisée pour décoder l’image et la première image de l’image est récupérée.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-107">In this example, an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) is used to decode the image and the first image frame is retrieved.</span></span>

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

    

    <span data-ttu-id="4b5e0-108">Pour obtenir d’autres types de sources bitmap à dessiner, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="4b5e0-108">For additional types of bitmap sources to draw, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

2.  <span data-ttu-id="4b5e0-109">Convertit la source bitmap en un format de pixel 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-109">Convert the bitmap source to an 32bppPBGRA pixel format.</span></span>

    <span data-ttu-id="4b5e0-110">Pour que Direct2D puisse utiliser une image, il doit être converti au format de pixel 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-110">Before Direct2D can use an image, it must be converted to the 32bppPBGRA pixel format.</span></span> <span data-ttu-id="4b5e0-111">Pour convertir le format d’image, utilisez la méthode [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) pour créer un objet [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="4b5e0-111">To convert the image format, use the [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span> <span data-ttu-id="4b5e0-112">Une fois créé, utilisez la méthode [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-112">Once created, use the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>

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

    

3.  <span data-ttu-id="4b5e0-113">Créez un objet [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) pour le rendu sur un handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-113">Create an [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) object for rendering to a window handle.</span></span>

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

    

    <span data-ttu-id="4b5e0-114">Pour plus d’informations sur les cibles de rendu, consultez [vue d’ensemble des cibles de rendu](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-114">For more information render targets, see the Direct2D [Render Targets Overview](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span>

4.  <span data-ttu-id="4b5e0-115">Créez un objet [ID2D1Bitmap](../direct2d/render-targets-overview.md) à l’aide de la méthode [ID2D1RenderTarget :: CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) .</span><span class="sxs-lookup"><span data-stu-id="4b5e0-115">Create an [ID2D1Bitmap](../direct2d/render-targets-overview.md) object using the [ID2D1RenderTarget::CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) method.</span></span>

    ```C++
        // D2DBitmap may have been released due to device loss. 
        // If so, re-create it from the source bitmap
        if (m_pConvertedSourceBitmap && !m_pD2DBitmap)
        {
            m_pRT->CreateBitmapFromWicBitmap(m_pConvertedSourceBitmap, NULL, &m_pD2DBitmap);
        }
    ```

    

5.  <span data-ttu-id="4b5e0-116">Dessinez le [ID2D1Bitmap](../direct2d/render-targets-overview.md) à l’aide de D2D [ID2D1RenderTarget ::D méthode rawbitmap](../direct2d/id2d1rendertarget-drawbitmap.md) .</span><span class="sxs-lookup"><span data-stu-id="4b5e0-116">Draw the [ID2D1Bitmap](../direct2d/render-targets-overview.md) using D2D [ID2D1RenderTarget::DrawBitmap](../direct2d/id2d1rendertarget-drawbitmap.md) method.</span></span>

    ```C++
        // Draws an image and scales it to the current window size
        if (m_pD2DBitmap)
        {
            m_pRT->DrawBitmap(m_pD2DBitmap, rectangle);
        }
    ```

    

<span data-ttu-id="4b5e0-117">Le code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-117">Code has been omitted from this example.</span></span> <span data-ttu-id="4b5e0-118">Pour obtenir le code complet, consultez la [visionneuse d’images WIC à l’aide de l’exemple Direct2D](-wic-sample-d2d-viewer.md).</span><span class="sxs-lookup"><span data-stu-id="4b5e0-118">For the complete code, see the [WIC Image Viewer Using Direct2D Sample](-wic-sample-d2d-viewer.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4b5e0-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b5e0-119">See Also</span></span>

[<span data-ttu-id="4b5e0-120">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="4b5e0-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="4b5e0-121">Référence</span><span class="sxs-lookup"><span data-stu-id="4b5e0-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="4b5e0-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="4b5e0-122">Samples</span></span>](-wic-samples.md)


[<span data-ttu-id="4b5e0-123">Direct2D</span><span class="sxs-lookup"><span data-stu-id="4b5e0-123">Direct2D</span></span>](../direct2d/direct2d-portal.md)


 

 
