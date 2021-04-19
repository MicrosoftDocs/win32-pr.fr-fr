---
title: Comment charger une image dans des effets Direct2D à l’aide de FilePicker
description: Montre comment utiliser les sélecteurs de stockage Windows FileOpenPicker pour charger une image dans des effets Direct2D.
ms.assetid: 42158EF0-2FC8-45F3-8C92-E12318D4724F
keywords:
- FileOpenPicker
- FilePicker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4346cc0e337374fa41313cb77debf4faca781669
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510688"
---
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a><span data-ttu-id="90452-105">Comment charger une image dans des effets Direct2D à l’aide de FilePicker</span><span class="sxs-lookup"><span data-stu-id="90452-105">How to load an image into Direct2D effects using the FilePicker</span></span>

<span data-ttu-id="90452-106">Montre comment utiliser [**Windows :: Storage ::P ickers :: FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) pour charger une image dans des [effets Direct2D](effects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="90452-106">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into [Direct2D effects](effects-overview.md).</span></span> <span data-ttu-id="90452-107">Si vous souhaitez permettre à l’utilisateur de sélectionner un fichier image à partir du stockage dans une application du Windows Store, nous vous recommandons d’utiliser [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).</span><span class="sxs-lookup"><span data-stu-id="90452-107">If you want to let the user select an image file from storage in a Windows Store app, we recommend that you use the [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="90452-108">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="90452-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="90452-109">Technologies</span><span class="sxs-lookup"><span data-stu-id="90452-109">Technologies</span></span>

-   [<span data-ttu-id="90452-110">Direct2D</span><span class="sxs-lookup"><span data-stu-id="90452-110">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="90452-111">Effets Direct2D</span><span class="sxs-lookup"><span data-stu-id="90452-111">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="90452-112">**Windows :: Storage ::P ickers :: FileOpenPicker**</span><span class="sxs-lookup"><span data-stu-id="90452-112">**Windows::Storage::Pickers::FileOpenPicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a><span data-ttu-id="90452-113">Prérequis</span><span class="sxs-lookup"><span data-stu-id="90452-113">Prerequisites</span></span>

-   <span data-ttu-id="90452-114">Vous avez besoin d’un objet [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pour créer des effets.</span><span class="sxs-lookup"><span data-stu-id="90452-114">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object for creating effects.</span></span>
-   <span data-ttu-id="90452-115">Vous avez besoin d’un objet [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) pour la création d’objets WIC.</span><span class="sxs-lookup"><span data-stu-id="90452-115">You need an [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) object for creating WIC objects.</span></span>

## <a name="instructions"></a><span data-ttu-id="90452-116">Instructions</span><span class="sxs-lookup"><span data-stu-id="90452-116">Instructions</span></span>

### <a name="step-1-open-the-file-picker"></a><span data-ttu-id="90452-117">Étape 1 : ouvrir le sélecteur de fichiers</span><span class="sxs-lookup"><span data-stu-id="90452-117">Step 1: Open the file picker</span></span>

<span data-ttu-id="90452-118">Créez un objet [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) et définissez *ViewMode*, *SuggestedStartLocation* et *FileTypeFilter* pour la sélection d’images.</span><span class="sxs-lookup"><span data-stu-id="90452-118">Create a [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) object and set the *ViewMode*, *SuggestedStartLocation*, and the *FileTypeFilter* for selecting images.</span></span> <span data-ttu-id="90452-119">Appelez la méthode [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) .</span><span class="sxs-lookup"><span data-stu-id="90452-119">Call the [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) method.</span></span>


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



<span data-ttu-id="90452-120">Une fois le [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) terminé, vous recevez un flux de fichier à partir de l’interface [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) qu’il retourne.</span><span class="sxs-lookup"><span data-stu-id="90452-120">After the [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) completes, you get a file stream from the [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) interface it returns.</span></span>

### <a name="step-2-get-a-file-stream"></a><span data-ttu-id="90452-121">Étape 2 : obtenir un flux de fichier</span><span class="sxs-lookup"><span data-stu-id="90452-121">Step 2: Get a file stream</span></span>

<span data-ttu-id="90452-122">Déclarez un gestionnaire d’achèvement à exécuter après le retour de l’opération Async du sélecteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="90452-122">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="90452-123">Utilisez la méthode [**GetResults**](/previous-versions//br205815(v=vs.85)) pour récupérer le fichier et obtenir l’objet de flux de fichier.</span><span class="sxs-lookup"><span data-stu-id="90452-123">Use the [**GetResults**](/previous-versions//br205815(v=vs.85)) method to retrieve the file and to get the file stream object.</span></span>


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



<span data-ttu-id="90452-124">À l’étape suivante, vous allez convertir l’objet [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) en [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que vous pouvez passer à [WIC](/windows/desktop/wic/-wic-api).</span><span class="sxs-lookup"><span data-stu-id="90452-124">In the next step you convert the [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) object to an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) that you can pass to [WIC](/windows/desktop/wic/-wic-api).</span></span>

### <a name="step-3-convert-the-file-stream"></a><span data-ttu-id="90452-125">Étape 3 : convertir le flux de fichier</span><span class="sxs-lookup"><span data-stu-id="90452-125">Step 3: Convert the file stream</span></span>

<span data-ttu-id="90452-126">Utilisez la fonction [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) pour convertir le flux de fichier.</span><span class="sxs-lookup"><span data-stu-id="90452-126">Use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function to convert the file stream.</span></span> <span data-ttu-id="90452-127">Les API Windows Runtime représentent des flux avec [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), tandis que [WIC](/windows/desktop/wic/-wic-api) consomme [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="90452-127">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while [WIC](/windows/desktop/wic/-wic-api) consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


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
> <span data-ttu-id="90452-128">Pour utiliser la fonction [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) , vous devez inclure *shCore. h* dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="90452-128">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include *shcore.h* in your project.</span></span>

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a><span data-ttu-id="90452-129">Étape 4 : créer un décodeur WIC et obtenir le frame</span><span class="sxs-lookup"><span data-stu-id="90452-129">Step 4: Create a WIC decoder and get the frame</span></span>

<span data-ttu-id="90452-130">Créez un objet [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) à l’aide de la méthode [**IWICImagingFactory :: CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="90452-130">Create an [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) object using the [**IWICImagingFactory::CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>


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



<span data-ttu-id="90452-131">Récupérez le premier frame de l’image à partir du décodeur à l’aide de la méthode [**IWICBitmapDecoder :: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .</span><span class="sxs-lookup"><span data-stu-id="90452-131">Get the first frame of the image from the decoder using the [**IWICBitmapDecoder::GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a><span data-ttu-id="90452-132">Étape 5 : créer un convertisseur WIC et initialiser</span><span class="sxs-lookup"><span data-stu-id="90452-132">Step 5: Create a WIC converter and initialize</span></span>

<span data-ttu-id="90452-133">Convertissez l’image au format de couleur BGRA à l’aide de [WIC](/windows/desktop/wic/-wic-api).</span><span class="sxs-lookup"><span data-stu-id="90452-133">Convert the image to the BGRA color format using [WIC](/windows/desktop/wic/-wic-api).</span></span> <span data-ttu-id="90452-134">[IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) retourne le format de pixel natif de l’image, comme les fichiers JPEG sont stockés dans le GUID \_ WICPixelFormat24bppBGR.</span><span class="sxs-lookup"><span data-stu-id="90452-134">[IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) will return the native pixel format of the image, like JPEGs are stored in GUID\_WICPixelFormat24bppBGR.</span></span> <span data-ttu-id="90452-135">Toutefois, en tant qu’optimisation des performances avec Direct2D, nous vous recommandons de convertir en WICPixelFormat32bppPBGRA.</span><span class="sxs-lookup"><span data-stu-id="90452-135">However, as a performance optimization with Direct2D we recommend that you convert to WICPixelFormat32bppPBGRA.</span></span>

1.  <span data-ttu-id="90452-136">Créez un objet [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) à l’aide de la méthode [**IWICImagingFactory :: CreateFormatConverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="90452-136">Create a [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) object using the [**IWICImagingFactory::CreateFormatConverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  <span data-ttu-id="90452-137">Initialisez le convertisseur de format pour utiliser le WICPixelFormat32bppPBGRA et passer le frame bitmap.</span><span class="sxs-lookup"><span data-stu-id="90452-137">Initialize the format converter to use the WICPixelFormat32bppPBGRA and pass in the bitmap frame.</span></span>

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

    

<span data-ttu-id="90452-138">L’interface [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) est dérivée de l’interface [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) . vous pouvez donc passer le convertisseur à l’effet de [source bitmap](bitmap-source.md) .</span><span class="sxs-lookup"><span data-stu-id="90452-138">The [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) interface is derived from the [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) interface, so you can pass the converter to the [bitmap source](bitmap-source.md) effect.</span></span>

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a><span data-ttu-id="90452-139">Étape 6 : créer un effet et passer un IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="90452-139">Step 6: Create effect and pass in an IWICBitmapSource</span></span>

<span data-ttu-id="90452-140">Utilisez la méthode [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) pour créer un objet [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) [source bitmap](bitmap-source.md) à l’aide du [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](getting-started-with-direct2d.md) .</span><span class="sxs-lookup"><span data-stu-id="90452-140">Use the [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method to create a [bitmap source](bitmap-source.md) [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object using the [Direct2D](getting-started-with-direct2d.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span>

<span data-ttu-id="90452-141">Utilisez la méthode [**ID2D1Effect :: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) pour définir la propriété source de la *\_ \_ \_ \_ \_ source bitmap d2d1 BITMAPSOURCE prop* avec le [**convertisseur de format**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) [WIC](/windows/desktop/wic/-wic-api) .</span><span class="sxs-lookup"><span data-stu-id="90452-141">Use the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method to set the *D2D1\_BITMAPSOURCE\_PROP\_WIC\_BITMAP\_SOURCE* property to the [WIC](/windows/desktop/wic/-wic-api) [**format converter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter).</span></span>

> [!Note]  
> <span data-ttu-id="90452-142">L’effet de [source bitmap](bitmap-source.md) ne prend pas d’entrée de la méthode [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) comme de nombreux [effets Direct2D](effects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="90452-142">The [bitmap source](bitmap-source.md) effect doesn't take an input from the [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method like many [Direct2D effects](effects-overview.md).</span></span> <span data-ttu-id="90452-143">Au lieu de cela, l’objet [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) est spécifié en tant que propriété.</span><span class="sxs-lookup"><span data-stu-id="90452-143">Instead, the [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) object is specified as a property.</span></span>

 


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



<span data-ttu-id="90452-144">Maintenant que vous avez l’effet de [source bitmap](bitmap-source.md) , vous pouvez l’utiliser comme entrée pour n’importe quel [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) et créer un graphique d’effet.</span><span class="sxs-lookup"><span data-stu-id="90452-144">Now that you have the [bitmap source](bitmap-source.md) effect, you can use it as input to any [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) and create an effect graph.</span></span>

## <a name="complete-example"></a><span data-ttu-id="90452-145">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="90452-145">Complete example</span></span>

<span data-ttu-id="90452-146">Voici le code complet de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="90452-146">Here is the full code for this example.</span></span>


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



 

 