---
title: Chargement d’une image bitmap à partir d’un fichier
description: Montre comment charger une bitmap Direct2D à partir d’un fichier image.
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: c9590e799e71e92056157b75573565cf79b9236b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728900"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a><span data-ttu-id="0b016-103">Chargement d’une image bitmap à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="0b016-103">How to Load a Bitmap from a File</span></span>

<span data-ttu-id="0b016-104">Direct2D utilise le WIC (Windows Imaging Component) pour charger des bitmaps.</span><span class="sxs-lookup"><span data-stu-id="0b016-104">Direct2D uses the Windows Imaging Component (WIC) to load bitmaps.</span></span> <span data-ttu-id="0b016-105">Pour charger une image bitmap à partir d’un fichier, utilisez d’abord les objets WIC pour charger l’image et la convertir en un format compatible Direct2D, puis utilisez la méthode [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) pour créer un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="0b016-105">To load a bitmap from a file, first use WIC objects to load the image and to convert it to a Direct2D-compatible format, then use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

1.  <span data-ttu-id="0b016-106">Créez une [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) à l’aide de la méthode [**IWICImagingFactory :: CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .</span><span class="sxs-lookup"><span data-stu-id="0b016-106">Create an [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) by using the [**IWICImagingFactory::CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

    ```C++
    HRESULT DemoApp::LoadBitmapFromFile(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR uri,
        UINT destinationWidth,
        UINT destinationHeight,
        ID2D1Bitmap **ppBitmap
        )
    {
        IWICBitmapDecoder *pDecoder = NULL;
        IWICBitmapFrameDecode *pSource = NULL;
        IWICStream *pStream = NULL;
        IWICFormatConverter *pConverter = NULL;
        IWICBitmapScaler *pScaler = NULL;

        HRESULT hr = pIWICFactory->CreateDecoderFromFilename(
            uri,
            NULL,
            GENERIC_READ,
            WICDecodeMetadataCacheOnLoad,
            &pDecoder
            );
            
    ```

    

2.  <span data-ttu-id="0b016-107">Récupérez un frame à partir de l’image et stockez le frame dans un objet [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="0b016-107">Retrieve a frame from the image and store the frame in an [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  <span data-ttu-id="0b016-108">La bitmap doit être convertie dans un format que Direct2D peut utiliser, ce qui permet de convertir le format de pixel de l’image en 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="0b016-108">The bitmap must be converted to a format that Direct2D can use, so convert the image's pixel format to 32bppPBGRA.</span></span> <span data-ttu-id="0b016-109">(Pour obtenir la liste des formats pris en charge, consultez [formats de pixel et modes alpha](supported-pixel-formats-and-alpha-modes.md).)</span><span class="sxs-lookup"><span data-stu-id="0b016-109">(For a list of supported formats, see [Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).).</span></span> <span data-ttu-id="0b016-110">Appelez la méthode [**IWICImagingFactory :: CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) pour créer un objet [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) , puis appelez la méthode [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) de l’objet **IWICFormatConverter** pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="0b016-110">Call the [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) object, then call the **IWICFormatConverter** object's [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>
    ```C++
        if (SUCCEEDED(hr))
        {

            // Convert the image format to 32bppPBGRA
            // (DXGI_FORMAT_B8G8R8A8_UNORM + D2D1_ALPHA_MODE_PREMULTIPLIED).
            hr = pIWICFactory->CreateFormatConverter(&pConverter);

        }
     
     
        if (SUCCEEDED(hr))
        {
            hr = pConverter->Initialize(
                pSource,
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                NULL,
                0.f,
                WICBitmapPaletteTypeMedianCut
                );
    ```

    

4.  <span data-ttu-id="0b016-111">Appelez la méthode [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) pour créer un objet [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) qui peut être dessiné par une cible de rendu et utilisé avec d’autres objets Direct2D.</span><span class="sxs-lookup"><span data-stu-id="0b016-111">Call the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object that can be drawn by a render target and used with other Direct2D objects.</span></span>
    ```C++
        if (SUCCEEDED(hr))
        {
        
            // Create a Direct2D bitmap from the WIC bitmap.
            hr = pRenderTarget->CreateBitmapFromWicBitmap(
                pConverter,
                NULL,
                ppBitmap
                );
        }

        SafeRelease(&pDecoder);
        SafeRelease(&pSource);
        SafeRelease(&pStream);
        SafeRelease(&pConverter);
        SafeRelease(&pScaler);

        return hr;
    }
    ```

    

<span data-ttu-id="0b016-112">Du code a été omis dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="0b016-112">Some code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b016-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b016-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b016-114">**ID2D1Bitmap**</span><span class="sxs-lookup"><span data-stu-id="0b016-114">**ID2D1Bitmap**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[<span data-ttu-id="0b016-115">**CreateBitmapFromWicBitmap**</span><span class="sxs-lookup"><span data-stu-id="0b016-115">**CreateBitmapFromWicBitmap**</span></span>](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[<span data-ttu-id="0b016-116">Chargement d’une image bitmap à partir d’une ressource</span><span class="sxs-lookup"><span data-stu-id="0b016-116">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 