---
title: Comment charger une image dans des effets Direct2D à l’aide de FilePicker
description: montre comment utiliser les sélecteurs de Windows Stockage FileOpenPicker pour charger une image dans des effets Direct2D.
ms.assetid: 42158EF0-2FC8-45F3-8C92-E12318D4724F
keywords:
- FileOpenPicker
- FilePicker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bb23faf2b9d50f12219f3b99c07ec835558addc55e67d4843dee049946a60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160530"
---
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a>Comment charger une image dans des effets Direct2D à l’aide de FilePicker

montre comment utiliser l' [**Windows :: Stockage ::P ickers :: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) pour charger une image dans des [effets Direct2D](effects-overview.md). si vous souhaitez permettre à l’utilisateur de sélectionner un fichier image à partir du stockage dans une application Windows Store, nous vous recommandons d’utiliser [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Direct2D](./direct2d-portal.md)
-   [Effets Direct2D](effects-overview.md)
-   [**Windows :: Stockage ::P ickers :: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a>Prérequis

-   Vous avez besoin d’un objet [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pour créer des effets.
-   Vous avez besoin d’un objet [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) pour la création d’objets WIC.

## <a name="instructions"></a>Instructions

### <a name="step-1-open-the-file-picker"></a>Étape 1 : ouvrir le sélecteur de fichiers

Créez un objet [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) et définissez *ViewMode*, *SuggestedStartLocation* et *FileTypeFilter* pour la sélection d’images. Appelez la méthode [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) .


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



Une fois le [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) terminé, vous recevez un flux de fichier à partir de l’interface [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) qu’il retourne.

### <a name="step-2-get-a-file-stream"></a>Étape 2 : obtenir un flux de fichier

Déclarez un gestionnaire d’achèvement à exécuter après le retour de l’opération Async du sélecteur de fichiers. Utilisez la méthode [**GetResults**](/previous-versions//br205815(v=vs.85)) pour récupérer le fichier et obtenir l’objet de flux de fichier.


```C++
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file) // If file == nullptr, the user did not select a file.
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
```



À l’étape suivante, vous allez convertir l’objet [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) en [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que vous pouvez passer à [WIC](/windows/desktop/wic/-wic-api).

### <a name="step-3-convert-the-file-stream"></a>Étape 3 : convertir le flux de fichier

Utilisez la fonction [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) pour convertir le flux de fichier. Windows Les API de Runtime représentent des flux avec [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), tandis que [WIC](/windows/desktop/wic/-wic-api) consomme [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).


```C++
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
        reinterpret_cast<IUnknown*>(fileStream),
        IID_PPV_ARGS(&istream)
        )
    );
```



> [!Note]  
> Pour utiliser la fonction [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , vous devez inclure *shCore. h* dans votre projet.

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a>Étape 4 : créer un décodeur WIC et obtenir le frame

Créez un objet [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) à l’aide de la méthode [**IWICImagingFactory :: CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .


```C++
    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );
```



Récupérez le premier frame de l’image à partir du décodeur à l’aide de la méthode [**IWICBitmapDecoder :: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a>Étape 5 : créer un convertisseur WIC et initialiser

Convertissez l’image au format de couleur BGRA à l’aide de [WIC](/windows/desktop/wic/-wic-api). [IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) retourne le format de pixel natif de l’image, comme les fichiers JPEG sont stockés dans le GUID \_ WICPixelFormat24bppBGR. Toutefois, en tant qu’optimisation des performances avec Direct2D, nous vous recommandons de convertir en WICPixelFormat32bppPBGRA.

1.  Créez un objet [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) à l’aide de la méthode [**IWICImagingFactory :: CreateFormatConverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  Initialisez le convertisseur de format pour utiliser le WICPixelFormat32bppPBGRA et passer le frame bitmap.

    ```C++
       DX::ThrowIfFailed(
            converter->Initialize(
                frame.Get(),
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                nullptr,
                0.0f,
                WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
                )
            );
    ```

    

L’interface [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) est dérivée de l’interface [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) . vous pouvez donc passer le convertisseur à l’effet de [source bitmap](bitmap-source.md) .

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a>Étape 6 : créer un effet et passer un IWICBitmapSource

Utilisez la méthode [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) pour créer un objet [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) [source bitmap](bitmap-source.md) à l’aide du [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](getting-started-with-direct2d.md) .

Utilisez la méthode [**ID2D1Effect :: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) pour définir la propriété source de la *\_ \_ \_ \_ \_ source bitmap d2d1 BITMAPSOURCE prop* avec le [**convertisseur de format**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) [WIC](/windows/desktop/wic/-wic-api) .

> [!Note]  
> L’effet de [source bitmap](bitmap-source.md) ne prend pas d’entrée de la méthode [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) comme de nombreux [effets Direct2D](effects-overview.md). Au lieu de cela, l’objet [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) est spécifié en tant que propriété.

 


```C++
    ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
```



Maintenant que vous avez l’effet de [source bitmap](bitmap-source.md) , vous pouvez l’utiliser comme entrée pour n’importe quel [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) et créer un graphique d’effet.

## <a name="complete-example"></a>Exemple complet

Voici le code complet de cet exemple.


```C++
ComPtr<ID2D1Effect> bitmapSourceEffect;

void OpenFilePicker()
{
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
    
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file)
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
}

void OpenFile(Windows::Storage::Streams::IRandomAccessStream^ fileStream)
{
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
            reinterpret_cast<IUnknown*>(fileStream),
            IID_PPV_ARGS(&istream)
            )
        );

    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );

    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );

    ComPtr<IWICFormatConverter> converter;
    DX::ThrowIfFailed(
        m_wicFactory->CreateFormatConverter(&converter)
        );

    DX::ThrowIfFailed(
        converter->Initialize(
            frame.Get(),
            GUID_WICPixelFormat32bppPBGRA,
            WICBitmapDitherTypeNone,
            nullptr,
            0.0f,
            WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
            )
        );

       ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
}
```



 

 