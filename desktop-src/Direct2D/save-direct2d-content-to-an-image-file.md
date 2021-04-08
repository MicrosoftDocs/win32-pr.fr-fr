---
title: Guide pratique pour enregistrer le contenu Direct2D dans un fichier image
description: Cette rubrique montre comment utiliser IWICImageEncoder pour enregistrer du contenu sous la forme d’un ID2D1Image dans un fichier image encodé comme JPEG.
ms.assetid: F0D8BFC7-723A-4577-B2DF-4D656A18E2FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19146d838474046fd634cb5524ddf2367fd1d6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842386"
---
# <a name="how-to-save-direct2d-content-to-an-image-file"></a>Guide pratique pour enregistrer le contenu Direct2D dans un fichier image

Cette rubrique montre comment utiliser [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) pour enregistrer du contenu sous la forme d’un [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) dans un fichier image encodé comme JPEG. Si vous écrivez une application Windows Store, vous pouvez demander à l’utilisateur de sélectionner un fichier de destination à l’aide de [**Windows :: Storage ::P ickers :: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Direct2D](./direct2d-portal.md)
-   [Effets Direct2D](effects-overview.md)
-   [**Windows :: Storage ::P ickers :: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a>Prérequis

-   Vous avez besoin d’un objet [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) et d’un objet contenant du contenu [Direct2D](./direct2d-portal.md) qui implémente [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) comme [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) ou [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).

## <a name="instructions"></a>Instructions

### <a name="step-1-get-a-destination-file-and-stream"></a>Étape 1 : obtenir un fichier de destination et un flux

Si vous souhaitez autoriser l’utilisateur à sélectionner un fichier de destination, vous pouvez utiliser [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), ouvrir le fichier retourné et obtenir un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) à utiliser avec WIC.

Créez un fichier [**Windows :: Storage ::P ickers :: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) et définissez ses paramètres pour les fichiers image. Appelez la méthode [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) .


```C++
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    savePicker->DefaultFileExtension = ".jpg";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
```



Déclarez un gestionnaire d’achèvement à exécuter après le retour de l’opération Async du sélecteur de fichiers. Utilisez la méthode [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) pour récupérer le fichier et obtenir l’objet de flux de fichier.


```C++
    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }
```



Obtenez un [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) en appelant [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) sur le fichier et en obtenant le résultat de l’opération asynchrone.


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



Enfin, utilisez la méthode [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) pour convertir le flux de fichier. Les API Windows Runtime représentent des flux avec [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), tandis que WIC consomme [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> Pour utiliser la fonction [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , vous devez inclure **shCore. h** dans votre projet.

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a>Étape 2 : obtenir la bitmap WIC et l’encodeur de trame

[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) et [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) fournissent les fonctionnalités permettant d’enregistrer les données d’acquisition d’images dans un format de fichier encodé.

Créez et initialisez les objets de l’encodeur.


```C++
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );
```



### <a name="step-3-get-an-iwicimageencoder"></a>Étape 3 : obtenir un IWICImageEncoder

[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) est une nouvelle interface dans Windows 8. Il peut être créé à partir de [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), qui étend **IWICImagingFactory** et est également nouveau pour Windows 8.


```C++
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );
```



Appelez [**IWICImagingFactory2 :: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder). Le premier paramètre est un [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) et doit être l’appareil sur lequel l’image que vous souhaitez Encoder a été créée. vous ne pouvez pas mélanger des images provenant de différents domaines de ressources au sein d’un même [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a>Étape 4 : écrire le contenu Direct2D à l’aide de IWICImageEncoder

[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) peut écrire une image [Direct2D](./direct2d-portal.md) dans un frame d’image, une miniature de cadre ou la miniature de conteneur. Vous pouvez ensuite utiliser [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) et [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) pour encoder les données d’acquisition d’images dans un fichier comme d’habitude.

Écrivez l’image [Direct2D](./direct2d-portal.md) dans le frame. Dans cet extrait de code, nous écrivons un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) qui contient le contenu Direct2D pixellisé. Toutefois, vous pouvez fournir une interface qui implémente [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).


```C++
    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );
```



> [!Note]  
> Le paramètre [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) doit avoir été créé sur le [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) qui a été passé dans [**IWICImagingFactory2 :: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).

 

Validez le WIC et les ressources de flux pour finaliser l’opération.


```C++
    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
```



> [!Note]  
> Certaines implémentations de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) n’implémentent pas la méthode [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) et retournent **E \_ NOTIMPL**.

 

Vous avez maintenant un fichier qui contient l’image [Direct2D](./direct2d-portal.md) .

## <a name="complete-example"></a>Exemple complet

Voici le code complet de cet exemple.

```cpp
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );

void SaveAsImageFile::SaveBitmapToFile()
{
    // Prepare a file picker for customers to input image file name.
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto pngExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    auto bmpExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    bmpExtensions->Append(".bmp");
    savePicker->FileTypeChoices->Insert("BMP file", bmpExtensions);
    savePicker->DefaultFileExtension = ".png";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            m_imageFileName = file->Name;
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".bmp")
            {
                wicFormat = GUID_ContainerFormatBmp;
            }
            else if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }

            // Retrieve a stream from the file.
            task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
            createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
                // Convert the RandomAccessStream to an IStream.
                ComPtr<IStream> stream;
                DX::ThrowIfFailed(
                    CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
                    );

                SaveBitmapToStream(m_d2dTargetBitmap, m_wicFactory, m_d2dContext, wicFormat, stream.Get());
            });
        }
    });
}

// Save render target bitmap to a stream using WIC.
void SaveAsImageFile::SaveBitmapToStream(
    _In_ ComPtr<ID2D1Bitmap1> d2dBitmap,
    _In_ ComPtr<IWICImagingFactory2> wicFactory2,
    _In_ ComPtr<ID2D1DeviceContext> d2dContext,
    _In_ REFGUID wicFormat,
    _In_ IStream* stream
    )
{
    // Create and initialize WIC Bitmap Encoder.
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    // Create and initialize WIC Frame Encoder.
    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );

    // Retrieve D2D Device.
    ComPtr<ID2D1Device> d2dDevice;
    d2dContext->GetDevice(&d2dDevice);

    // Create IWICImageEncoder.
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );

    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
}

```



 

 