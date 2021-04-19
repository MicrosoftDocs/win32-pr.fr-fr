---
title: Chargement d’une image bitmap à partir d’une ressource (Direct2D)
description: Montre comment charger une bitmap Direct2D stockée en tant que ressource d’application.
ms.assetid: 7285e6ea-ebc7-4693-8a77-99bff0b5d0d1
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: fe96ba4e0674392333173df7daeb5a354a379343
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106511528"
---
# <a name="how-to-load-a-bitmap-from-a-resource-direct2d"></a><span data-ttu-id="fc7ea-103">Chargement d’une image bitmap à partir d’une ressource (Direct2D)</span><span class="sxs-lookup"><span data-stu-id="fc7ea-103">How to Load a Bitmap from a Resource (Direct2D)</span></span>

<span data-ttu-id="fc7ea-104">Comme décrit dans [la rubrique chargement d’une image bitmap à partir d’un fichier](how-to-load-a-direct2d-bitmap-from-a-file.md), Direct2D utilise le composant WIC (Windows Imaging Component) pour charger des bitmaps.</span><span class="sxs-lookup"><span data-stu-id="fc7ea-104">As described in [How to Load a Bitmap from a File](how-to-load-a-direct2d-bitmap-from-a-file.md), Direct2D uses the Windows Imaging Component (WIC) to load bitmaps.</span></span> <span data-ttu-id="fc7ea-105">Pour charger une image bitmap à partir d’une ressource, utilisez des objets WIC pour charger l’image et la convertir en un format compatible Direct2D. Ensuite, utilisez la méthode [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) pour créer un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span><span class="sxs-lookup"><span data-stu-id="fc7ea-105">To load a bitmap from a resource, use WIC objects to load the image and to convert it to a Direct2D-compatible format; then, use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

1.  <span data-ttu-id="fc7ea-106">Dans le [fichier de définition de ressource d’application](/windows/desktop/menurc/about-resource-files), définissez la ressource.</span><span class="sxs-lookup"><span data-stu-id="fc7ea-106">In the [application resource definition file](/windows/desktop/menurc/about-resource-files), define the resource.</span></span> <span data-ttu-id="fc7ea-107">L’exemple suivant définit une ressource nommée « SampleImage ».</span><span class="sxs-lookup"><span data-stu-id="fc7ea-107">The following example defines a resource named "SampleImage".</span></span>

    ```C++
    // THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
    // ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
    // THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
    // PARTICULAR PURPOSE.
    //
    // Copyright (c) Microsoft Corporation. All rights reserved
    #include "windows.h"

    SampleImage Image "sampleImage.jpg"
    ```

<span data-ttu-id="fc7ea-108">Cette ressource sera ajoutée au fichier de ressources de l’application lors de la génération de l’application.</span><span class="sxs-lookup"><span data-stu-id="fc7ea-108">This resource will be added to the application's resource file when the application is built.</span></span>

2.  <span data-ttu-id="fc7ea-109">Chargez l’image à partir du fichier de ressources de l’application.</span><span class="sxs-lookup"><span data-stu-id="fc7ea-109">Load the image from the application resource file.</span></span>

    ```C++
    HRESULT DemoApp::LoadResourceBitmap(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR resourceName,
        PCWSTR resourceType,
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

        HRSRC imageResHandle = NULL;
        HGLOBAL imageResDataHandle = NULL;
        void *pImageFile = NULL;
        DWORD imageFileSize = 0;

        // Locate the resource.
        imageResHandle = FindResourceW(HINST_THISCOMPONENT, resourceName, resourceType);
        HRESULT hr = imageResHandle ? S_OK : E_FAIL;
        if (SUCCEEDED(hr))
        {
            // Load the resource.
            imageResDataHandle = LoadResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageResDataHandle ? S_OK : E_FAIL;
        }
    ```

    

3.  <span data-ttu-id="fc7ea-110">Verrouiller la ressource et calculer la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="fc7ea-110">Lock the resource and calculate the image's size.</span></span>
    ```C++
        if (SUCCEEDED(hr))
        {
            // Lock it to get a system memory pointer.
            pImageFile = LockResource(imageResDataHandle);

            hr = pImageFile ? S_OK : E_FAIL;
        }
        if (SUCCEEDED(hr))
        {
            // Calculate the size.
            imageFileSize = SizeofResource(HINST_THISCOMPONENT, imageResHandle);

            hr = imageFileSize ? S_OK : E_FAIL;
            
        }
    ```

    

4.  <span data-ttu-id="fc7ea-111">Utilisez la méthode [**IWICImagingFactory :: CreateStream,**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) pour créer un objet [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="fc7ea-111">Use the [**IWICImagingFactory::CreateStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/win32/api/wincodec/nn-wincodec-iwicstream) object.</span></span>
    ```C++
        if (SUCCEEDED(hr))
        {
              // Create a WIC stream to map onto the memory.
            hr = pIWICFactory->CreateStream(&pStream);
        }
        if (SUCCEEDED(hr))
        {
            // Initialize the stream with the memory pointer and size.
            hr = pStream->InitializeFromMemory(
                reinterpret_cast<BYTE*>(pImageFile),
                imageFileSize
                );
        }
    ```

    

5.  <span data-ttu-id="fc7ea-112">Utilisez la méthode [**IWICImagingFactory :: CreateDecoderFromStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) pour créer [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="fc7ea-112">Use the [**IWICImagingFactory::CreateDecoderFromStream**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method to create an [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create a decoder for the stream.
            hr = pIWICFactory->CreateDecoderFromStream(
                pStream,
                NULL,
                WICDecodeMetadataCacheOnLoad,
                &pDecoder
                );
        }
    ```

    

6.  <span data-ttu-id="fc7ea-113">Récupérez un frame à partir de l’image et stockez-le dans un objet [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="fc7ea-113">Retrieve a frame from the image and store it in an [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

7.  <span data-ttu-id="fc7ea-114">Pour que Direct2D puisse utiliser l’image, elle doit être convertie au format de pixel 32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="fc7ea-114">Before Direct2D can use the image, it must be converted to the 32bppPBGRA pixel format.</span></span> <span data-ttu-id="fc7ea-115">Pour convertir le format d’image, utilisez la méthode [**IWICImagingFactory :: CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) pour créer un objet [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) , puis utilisez la méthode [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) de l’objet **IWICFormatConverter** pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="fc7ea-115">To convert the image format, use the [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) object, then use the **IWICFormatConverter** object's [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>
 
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

    

8.  <span data-ttu-id="fc7ea-116">Enfin, utilisez la méthode [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) pour créer un objet [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) qui peut être dessiné par une cible de rendu et utilisé avec d’autres objets Direct2D.</span><span class="sxs-lookup"><span data-stu-id="fc7ea-116">Finally, use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object that can be drawn by a render target and used with other Direct2D objects.</span></span>
    ```C++
        if (SUCCEEDED(hr))
        {
            //create a Direct2D bitmap from the WIC bitmap.
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

    

<span data-ttu-id="fc7ea-117">Du code a été omis dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="fc7ea-117">Some code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc7ea-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc7ea-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc7ea-119">Chargement d’une image bitmap à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="fc7ea-119">How to Load a Bitmap from a File</span></span>](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

 
