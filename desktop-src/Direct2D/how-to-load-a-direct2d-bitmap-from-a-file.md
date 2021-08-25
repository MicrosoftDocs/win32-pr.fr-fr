---
title: Chargement d’une image bitmap à partir d’un fichier
description: Montre comment charger une bitmap Direct2D à partir d’un fichier image.
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: a330f0e32ee4abf62eb7df1c1d6a00b3f217e6f04502cebae6c489aa01eaaa9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824559"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a>Chargement d’une image bitmap à partir d’un fichier

Direct2D utilise le composant WIC (Windows Imaging Component) pour charger les bitmaps. Pour charger une image bitmap à partir d’un fichier, utilisez d’abord les objets WIC pour charger l’image et la convertir en un format compatible Direct2D, puis utilisez la méthode [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) pour créer un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).

1.  Créez une [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) à l’aide de la méthode [**IWICImagingFactory :: CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .

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

    

2.  Récupérez un frame à partir de l’image et stockez le frame dans un objet [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) .

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  La bitmap doit être convertie dans un format que Direct2D peut utiliser, ce qui permet de convertir le format de pixel de l’image en 32bppPBGRA. (Pour obtenir la liste des formats pris en charge, consultez [formats de pixel et modes alpha](supported-pixel-formats-and-alpha-modes.md).) Appelez la méthode [**IWICImagingFactory :: CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) pour créer un objet [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) , puis appelez la méthode [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) de l’objet **IWICFormatConverter** pour effectuer la conversion.
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

    

4.  Appelez la méthode [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) pour créer un objet [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) qui peut être dessiné par une cible de rendu et utilisé avec d’autres objets Direct2D.
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

    

Du code a été omis dans cet exemple.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[Chargement d’une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 