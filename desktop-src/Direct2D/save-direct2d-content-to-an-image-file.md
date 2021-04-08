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
# <a name="how-to-save-direct2d-content-to-an-image-file"></a><span data-ttu-id="f1fb4-103">Guide pratique pour enregistrer le contenu Direct2D dans un fichier image</span><span class="sxs-lookup"><span data-stu-id="f1fb4-103">How to save Direct2D content to an image file</span></span>

<span data-ttu-id="f1fb4-104">Cette rubrique montre comment utiliser [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) pour enregistrer du contenu sous la forme d’un [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) dans un fichier image encodé comme JPEG.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-104">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span> <span data-ttu-id="f1fb4-105">Si vous écrivez une application Windows Store, vous pouvez demander à l’utilisateur de sélectionner un fichier de destination à l’aide de [**Windows :: Storage ::P ickers :: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span><span class="sxs-lookup"><span data-stu-id="f1fb4-105">If you are writing a Windows Store app, you can have the user select a destination file using [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f1fb4-106">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="f1fb4-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f1fb4-107">Technologies</span><span class="sxs-lookup"><span data-stu-id="f1fb4-107">Technologies</span></span>

-   [<span data-ttu-id="f1fb4-108">Direct2D</span><span class="sxs-lookup"><span data-stu-id="f1fb4-108">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="f1fb4-109">Effets Direct2D</span><span class="sxs-lookup"><span data-stu-id="f1fb4-109">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="f1fb4-110">**Windows :: Storage ::P ickers :: FileSavePicker**</span><span class="sxs-lookup"><span data-stu-id="f1fb4-110">**Windows::Storage::Pickers::FileSavePicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a><span data-ttu-id="f1fb4-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="f1fb4-111">Prerequisites</span></span>

-   <span data-ttu-id="f1fb4-112">Vous avez besoin d’un objet [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) et d’un objet contenant du contenu [Direct2D](./direct2d-portal.md) qui implémente [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) comme [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) ou [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span><span class="sxs-lookup"><span data-stu-id="f1fb4-112">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object and an object containing [Direct2D](./direct2d-portal.md) content that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) such as [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) or [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span></span>

## <a name="instructions"></a><span data-ttu-id="f1fb4-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="f1fb4-113">Instructions</span></span>

### <a name="step-1-get-a-destination-file-and-stream"></a><span data-ttu-id="f1fb4-114">Étape 1 : obtenir un fichier de destination et un flux</span><span class="sxs-lookup"><span data-stu-id="f1fb4-114">Step 1: Get a destination file and stream</span></span>

<span data-ttu-id="f1fb4-115">Si vous souhaitez autoriser l’utilisateur à sélectionner un fichier de destination, vous pouvez utiliser [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), ouvrir le fichier retourné et obtenir un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) à utiliser avec WIC.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-115">If you want to allow the user to select a destination file, you can use [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), open the returned file, and obtain an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) to use with WIC.</span></span>

<span data-ttu-id="f1fb4-116">Créez un fichier [**Windows :: Storage ::P ickers :: FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) et définissez ses paramètres pour les fichiers image.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-116">Create a [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) and set its parameters for image files.</span></span> <span data-ttu-id="f1fb4-117">Appelez la méthode [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) .</span><span class="sxs-lookup"><span data-stu-id="f1fb4-117">Call the [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) method.</span></span>


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



<span data-ttu-id="f1fb4-118">Déclarez un gestionnaire d’achèvement à exécuter après le retour de l’opération Async du sélecteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-118">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="f1fb4-119">Utilisez la méthode [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) pour récupérer le fichier et obtenir l’objet de flux de fichier.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-119">Use the [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) method to retrieve the file and to get the file stream object.</span></span>


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



<span data-ttu-id="f1fb4-120">Obtenez un [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) en appelant [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) sur le fichier et en obtenant le résultat de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-120">Obtain an [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) by calling [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) on the file and getting the result of the async operation.</span></span>


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



<span data-ttu-id="f1fb4-121">Enfin, utilisez la méthode [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) pour convertir le flux de fichier.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-121">Finally, use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) method to convert the file stream.</span></span> <span data-ttu-id="f1fb4-122">Les API Windows Runtime représentent des flux avec [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), tandis que WIC consomme [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="f1fb4-122">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while WIC consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> <span data-ttu-id="f1fb4-123">Pour utiliser la fonction [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , vous devez inclure **shCore. h** dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-123">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include **shcore.h** in your project.</span></span>

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a><span data-ttu-id="f1fb4-124">Étape 2 : obtenir la bitmap WIC et l’encodeur de trame</span><span class="sxs-lookup"><span data-stu-id="f1fb4-124">Step 2: Get the WIC bitmap and frame encoder</span></span>

<span data-ttu-id="f1fb4-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) et [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) fournissent les fonctionnalités permettant d’enregistrer les données d’acquisition d’images dans un format de fichier encodé.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) provide the functionality to save imaging data to an encoded file format.</span></span>

<span data-ttu-id="f1fb4-126">Créez et initialisez les objets de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-126">Create and initialize the encoder objects.</span></span>


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



### <a name="step-3-get-an-iwicimageencoder"></a><span data-ttu-id="f1fb4-127">Étape 3 : obtenir un IWICImageEncoder</span><span class="sxs-lookup"><span data-stu-id="f1fb4-127">Step 3: Get an IWICImageEncoder</span></span>

<span data-ttu-id="f1fb4-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) est une nouvelle interface dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) is a new interface in Windows 8.</span></span> <span data-ttu-id="f1fb4-129">Il peut être créé à partir de [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), qui étend **IWICImagingFactory** et est également nouveau pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-129">It can be created from [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), which extends **IWICImagingFactory** and is also new for Windows 8.</span></span>


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



<span data-ttu-id="f1fb4-130">Appelez [**IWICImagingFactory2 :: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span><span class="sxs-lookup"><span data-stu-id="f1fb4-130">Call [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span> <span data-ttu-id="f1fb4-131">Le premier paramètre est un [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) et doit être l’appareil sur lequel l’image que vous souhaitez Encoder a été créée. vous ne pouvez pas mélanger des images provenant de différents domaines de ressources au sein d’un même [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span><span class="sxs-lookup"><span data-stu-id="f1fb4-131">The first parameter is an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) and must be the device on which the image you want to encode was created – you cannot mix images from different resource domains within a single [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span></span>


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a><span data-ttu-id="f1fb4-132">Étape 4 : écrire le contenu Direct2D à l’aide de IWICImageEncoder</span><span class="sxs-lookup"><span data-stu-id="f1fb4-132">Step 4: Write the Direct2D content using IWICImageEncoder</span></span>

<span data-ttu-id="f1fb4-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) peut écrire une image [Direct2D](./direct2d-portal.md) dans un frame d’image, une miniature de cadre ou la miniature de conteneur.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) can write a [Direct2D](./direct2d-portal.md) image into an image frame, a frame thumbnail, or the container thumbnail.</span></span> <span data-ttu-id="f1fb4-134">Vous pouvez ensuite utiliser [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) et [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) pour encoder les données d’acquisition d’images dans un fichier comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-134">You can then use [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) to encode the imaging data to a file as normal.</span></span>

<span data-ttu-id="f1fb4-135">Écrivez l’image [Direct2D](./direct2d-portal.md) dans le frame.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-135">Write the [Direct2D](./direct2d-portal.md) image to the frame.</span></span> <span data-ttu-id="f1fb4-136">Dans cet extrait de code, nous écrivons un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) qui contient le contenu Direct2D pixellisé.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-136">In this snippet we write an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) that contains rasterized Direct2D content.</span></span> <span data-ttu-id="f1fb4-137">Toutefois, vous pouvez fournir une interface qui implémente [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span><span class="sxs-lookup"><span data-stu-id="f1fb4-137">However, you can provide any interface that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span></span>


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
> <span data-ttu-id="f1fb4-138">Le paramètre [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) doit avoir été créé sur le [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) qui a été passé dans [**IWICImagingFactory2 :: CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span><span class="sxs-lookup"><span data-stu-id="f1fb4-138">The [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) parameter must have been created on the [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) that was passed into [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span>

 

<span data-ttu-id="f1fb4-139">Validez le WIC et les ressources de flux pour finaliser l’opération.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-139">Commit the WIC and stream resources to finalize the operation.</span></span>


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
> <span data-ttu-id="f1fb4-140">Certaines implémentations de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) n’implémentent pas la méthode [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) et retournent **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-140">Some implementations of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) do not implement the [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) method and return **E\_NOTIMPL**.</span></span>

 

<span data-ttu-id="f1fb4-141">Vous avez maintenant un fichier qui contient l’image [Direct2D](./direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f1fb4-141">Now you have a file containing the [Direct2D](./direct2d-portal.md) image.</span></span>

## <a name="complete-example"></a><span data-ttu-id="f1fb4-142">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="f1fb4-142">Complete example</span></span>

<span data-ttu-id="f1fb4-143">Voici le code complet de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="f1fb4-143">Here the full code for this example.</span></span>

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



 

 