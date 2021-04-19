---
description: L’exemple suivant montre comment recoder une image et ses métadonnées dans un nouveau fichier de même format.
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: Comment recoder une image JPEG avec des métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c023defb760faeab2bc6ea92232fcc916ef15126
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106525317"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a><span data-ttu-id="36135-103">Comment recoder une image JPEG avec des métadonnées</span><span class="sxs-lookup"><span data-stu-id="36135-103">How-to re-encode a JPEG image with metadata</span></span>

<span data-ttu-id="36135-104">L’exemple suivant montre comment recoder une image et ses métadonnées dans un nouveau fichier de même format.</span><span class="sxs-lookup"><span data-stu-id="36135-104">The following example demonstrates how to re-encode an image and its metadata to a new file of the same format.</span></span> <span data-ttu-id="36135-105">En outre, cet exemple ajoute des métadonnées pour illustrer une expression à un seul élément utilisée par un enregistreur de requête.</span><span class="sxs-lookup"><span data-stu-id="36135-105">In addition, this example adds metadata to demonstrate a single-item expression used by a query writer.</span></span>

<span data-ttu-id="36135-106">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="36135-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="36135-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="36135-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="36135-108">Partie 1 : décoder une image</span><span class="sxs-lookup"><span data-stu-id="36135-108">Part 1: Decode an Image</span></span>](#part-1-decode-an-image)
-   [<span data-ttu-id="36135-109">Partie 2 : créer et initialiser l’encodeur d’image</span><span class="sxs-lookup"><span data-stu-id="36135-109">Part 2: Create and Initialize the Image Encoder</span></span>](#part-2-create-and-initialize-the-image-encoder)
-   [<span data-ttu-id="36135-110">Partie 3 : copier les informations de trame décodées</span><span class="sxs-lookup"><span data-stu-id="36135-110">Part 3: Copy Decoded Frame Information</span></span>](#part-3-copy-decoded-frame-information)
-   [<span data-ttu-id="36135-111">Partie 4 : copier les métadonnées</span><span class="sxs-lookup"><span data-stu-id="36135-111">Part 4: Copy the Metadata</span></span>](#part-4-copy-the-metadata)
-   [<span data-ttu-id="36135-112">Partie 5 : ajouter des métadonnées supplémentaires</span><span class="sxs-lookup"><span data-stu-id="36135-112">Part 5: Add Additional Metadata</span></span>](#part-5-add-additional-metadata)
-   [<span data-ttu-id="36135-113">Partie 6 : finaliser l’image encodée</span><span class="sxs-lookup"><span data-stu-id="36135-113">Part 6: Finalize the Encoded Image</span></span>](#part-6-finalize-the-encoded-image)
-   [<span data-ttu-id="36135-114">Exemple de code de recodage JPEG</span><span class="sxs-lookup"><span data-stu-id="36135-114">JPEG Re-encode Example Code</span></span>](#jpeg-re-encode-example-code)
-   [<span data-ttu-id="36135-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36135-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="36135-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="36135-116">Prerequisites</span></span>

<span data-ttu-id="36135-117">Pour comprendre cette rubrique, vous devez être familiarisé avec le système de métadonnées WIC (Windows Imaging Component), comme décrit dans la [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="36135-117">To understand this topic, you should be familiar with the Windows Imaging Component (WIC) metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="36135-118">Vous devez également être familiarisé avec les composants du codec WIC comme décrit dans la [vue d’ensemble du composant de création d’images Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="36135-118">You should also be familiar with the WIC codec components as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="part-1-decode-an-image"></a><span data-ttu-id="36135-119">Partie 1 : décoder une image</span><span class="sxs-lookup"><span data-stu-id="36135-119">Part 1: Decode an Image</span></span>

<span data-ttu-id="36135-120">Avant de pouvoir copier des données image ou des métadonnées dans un nouveau fichier image, vous devez d’abord créer un décodeur pour l’image existante que vous souhaitez recoder.</span><span class="sxs-lookup"><span data-stu-id="36135-120">Before you can copy image data or metadata to a new image file, you must first create a decoder for the existing image that you want to re-encode.</span></span> <span data-ttu-id="36135-121">Le code suivant montre comment créer un décodeur WIC pour le fichier image test.jpg.</span><span class="sxs-lookup"><span data-stu-id="36135-121">The following code demonstrates how to create a WIC decoder for the image file test.jpg.</span></span>


```C++
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }
```



<span data-ttu-id="36135-122">L’appel à **CreateDecoderFromFilename** a utilisé la valeur WICDecodeMetadataCacheOnDemand de l’énumération [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) comme quatrième paramètre.</span><span class="sxs-lookup"><span data-stu-id="36135-122">The call to **CreateDecoderFromFilename** used the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration as the fourth parameter.</span></span> <span data-ttu-id="36135-123">Cela indique au décodeur de mettre en cache les métadonnées lorsque les métadonnées sont nécessaires, soit en obtenant un lecteur de requête, soit en utilisant le lecteur de métadonnées sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="36135-123">This tells the decoder to cache the metadata when the metadata is needed, either by obtaining a query reader or by using the underlying metadata reader.</span></span> <span data-ttu-id="36135-124">L’utilisation de cette option vous permet de conserver le flux vers les métadonnées, ce qui est nécessaire pour effectuer rapidement un encodage des métadonnées et active le décodage et l’encodage sans perte d’images JPEG.</span><span class="sxs-lookup"><span data-stu-id="36135-124">Using this option enables you to retain the stream to the metadata, which is required for performing fast metadata encoding and enables lossless decoding and encoding of JPEG images.</span></span> <span data-ttu-id="36135-125">Vous pouvez également utiliser l’autre valeur **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, qui met en cache les métadonnées de l’image incorporée dès le chargement de l’image.</span><span class="sxs-lookup"><span data-stu-id="36135-125">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

## <a name="part-2-create-and-initialize-the-image-encoder"></a><span data-ttu-id="36135-126">Partie 2 : créer et initialiser l’encodeur d’image</span><span class="sxs-lookup"><span data-stu-id="36135-126">Part 2: Create and Initialize the Image Encoder</span></span>

<span data-ttu-id="36135-127">Le code suivant illustre la création de l’encodeur que vous allez utiliser pour encoder l’image que vous avez décodée précédemment.</span><span class="sxs-lookup"><span data-stu-id="36135-127">The following code demonstrates the creation of the encoder you will use to encode the image you previously decoded.</span></span>


```C++
    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }
```



<span data-ttu-id="36135-128">Un flux de fichier WIC piFileStream est créé et initialisé pour l’écriture dans le fichier image « test2.jpg ».</span><span class="sxs-lookup"><span data-stu-id="36135-128">A WIC file stream piFileStream is created and initialized for writing to the image file "test2.jpg".</span></span> <span data-ttu-id="36135-129">piFileStream est ensuite utilisé pour initialiser l’encodeur, en informant l’encodeur où écrire les bits de l’image lorsque l’encodage est terminé.</span><span class="sxs-lookup"><span data-stu-id="36135-129">piFileStream is then used to initialize the encoder, informing the encoder where to write the image bits when the encoding is complete.</span></span>

## <a name="part-3-copy-decoded-frame-information"></a><span data-ttu-id="36135-130">Partie 3 : copier les informations de trame décodées</span><span class="sxs-lookup"><span data-stu-id="36135-130">Part 3: Copy Decoded Frame Information</span></span>

<span data-ttu-id="36135-131">Le code suivant copie chaque image d’une image vers un nouveau frame de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="36135-131">The following code copies each frame of an image to a new frame of the encoder.</span></span> <span data-ttu-id="36135-132">Cette copie comprend la taille, la résolution et le format de pixel. tout ce qui est nécessaire pour créer un frame valide.</span><span class="sxs-lookup"><span data-stu-id="36135-132">This copy includes size, resolution, and pixel format; all of which are necessary to create a valid frame.</span></span>

> [!Note]  
> <span data-ttu-id="36135-133">Les images JPEG n’ont qu’un seul Frame et la boucle ci-dessous n’est pas techniquement nécessaire, mais elle est incluse pour illustrer l’utilisation de plusieurs frames pour les formats qui la prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="36135-133">JPEG images will only have one frame and the loop below is not technically necessary but is included to demonstrate multi-frame usage for formats that support it.</span></span>

 


```C++
    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }
```



<span data-ttu-id="36135-134">Le code suivant effectue une vérification rapide pour déterminer si les formats d’image source et de destination sont identiques.</span><span class="sxs-lookup"><span data-stu-id="36135-134">The following code performs a quick check to determine whether the source and destination image formats are the same.</span></span> <span data-ttu-id="36135-135">Cela est nécessaire, car la quatrième partie montre une opération qui est uniquement prise en charge lorsque le format source et le format de destination sont identiques.</span><span class="sxs-lookup"><span data-stu-id="36135-135">This is needed as Part 4 shows an operation that is only supported when the source and destination format are the same.</span></span>


```C++
            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }
```



## <a name="part-4-copy-the-metadata"></a><span data-ttu-id="36135-136">Partie 4 : copier les métadonnées</span><span class="sxs-lookup"><span data-stu-id="36135-136">Part 4: Copy the Metadata</span></span>

> [!Note]  
> <span data-ttu-id="36135-137">Le code de cette section est valide uniquement lorsque les formats d’image source et de destination sont identiques.</span><span class="sxs-lookup"><span data-stu-id="36135-137">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="36135-138">Vous ne pouvez pas copier toutes les métadonnées d’une image en une seule opération lors de l’encodage dans un format d’image différent.</span><span class="sxs-lookup"><span data-stu-id="36135-138">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="36135-139">Pour conserver les métadonnées tout en recodant une image au même format d’image, il existe des méthodes permettant de copier toutes les métadonnées en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="36135-139">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="36135-140">Chacune de ces opérations suit un modèle similaire. chaque définit les métadonnées de l’image décodée directement dans le nouveau Frame encodé.</span><span class="sxs-lookup"><span data-stu-id="36135-140">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span> <span data-ttu-id="36135-141">Notez que cette opération est effectuée pour chaque image individuelle.</span><span class="sxs-lookup"><span data-stu-id="36135-141">Note that this is done for each individual image frame.</span></span>

<span data-ttu-id="36135-142">La méthode recommandée pour copier les métadonnées consiste à initialiser le writer de bloc du nouveau Frame avec le lecteur de bloc du frame décodé.</span><span class="sxs-lookup"><span data-stu-id="36135-142">The preferred method for copying metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="36135-143">L’exemple de code suivant illustre cette méthode.</span><span class="sxs-lookup"><span data-stu-id="36135-143">The following code demonstrates this method.</span></span>


```C++
            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }
```



<span data-ttu-id="36135-144">Dans cet exemple, vous obtenez simplement le lecteur de bloc et le writer de bloc à partir du frame source et du frame de destination, respectivement.</span><span class="sxs-lookup"><span data-stu-id="36135-144">In this example, you simply obtain the block reader and block writer from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="36135-145">Le writer de bloc est ensuite initialisé à partir du lecteur de bloc.</span><span class="sxs-lookup"><span data-stu-id="36135-145">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="36135-146">Cela initialise le writer de bloc avec les métadonnées préremplies du lecteur de bloc.</span><span class="sxs-lookup"><span data-stu-id="36135-146">This initializes the block writer with the pre-populated metadata of the block reader.</span></span> <span data-ttu-id="36135-147">Pour découvrir d’autres méthodes de copie des métadonnées, consultez la section écriture de métadonnées dans la [vue d’ensemble de la lecture et de l’écriture de métadonnées d’image](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="36135-147">To learn additional methods for copying metadata, see the Writing Metadata section in the [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="36135-148">Là encore, cette opération fonctionne uniquement lorsque les images source et de destination ont le même format.</span><span class="sxs-lookup"><span data-stu-id="36135-148">Again, this operation works only when the source and destination images have the same format.</span></span> <span data-ttu-id="36135-149">Cela est dû au fait que différents formats d’image stockent les blocs de métadonnées à différents emplacements.</span><span class="sxs-lookup"><span data-stu-id="36135-149">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="36135-150">Par exemple, les formats JPEG et TIFF (Tagged Image File Format) prennent en charge les blocs de métadonnées XMP (Extensible Metadata Platform).</span><span class="sxs-lookup"><span data-stu-id="36135-150">For instance, both JPEG and Tagged Image File Format (TIFF) support Extensible Metadata Platform (XMP) metadata blocks.</span></span> <span data-ttu-id="36135-151">Dans les images JPEG, le bloc XMP se trouve dans le bloc de métadonnées racine, comme illustré dans la [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="36135-151">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="36135-152">Toutefois, dans une image TIFF, le bloc XMP est incorporé dans le bloc IFD racine.</span><span class="sxs-lookup"><span data-stu-id="36135-152">However, in a TIFF image, the XMP block is embedded in the root IFD block.</span></span>

## <a name="part-5-add-additional-metadata"></a><span data-ttu-id="36135-153">Partie 5 : ajouter des métadonnées supplémentaires</span><span class="sxs-lookup"><span data-stu-id="36135-153">Part 5: Add Additional Metadata</span></span>

<span data-ttu-id="36135-154">L’exemple suivant montre comment ajouter des métadonnées à l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="36135-154">The following example demonstrates how to add metadata to the destination image.</span></span> <span data-ttu-id="36135-155">Pour ce faire, appelez la méthode **SetMetadataByName** du writer de requête à l’aide d’une expression de requête et des données stockées dans un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="36135-155">This is done by calling the query writer's **SetMetadataByName** method using a query expression and the data stored in a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span>


```C++
            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
```



<span data-ttu-id="36135-156">Pour plus d’informations sur l’expression de requête, consultez la [vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="36135-156">For more information on the query expression, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="part-6-finalize-the-encoded-image"></a><span data-ttu-id="36135-157">Partie 6 : finaliser l’image encodée</span><span class="sxs-lookup"><span data-stu-id="36135-157">Part 6: Finalize the Encoded Image</span></span>

<span data-ttu-id="36135-158">La dernière étape de la copie de l’image consiste à écrire les données de pixels du frame, à valider le frame sur l’encodeur et à valider l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="36135-158">The final steps for copying the image are to write the pixel data for the frame, commit the frame to the encoder, and commit the encoder.</span></span> <span data-ttu-id="36135-159">La validation de l’encodeur écrit le flux d’image dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="36135-159">Committing the encoder writes the image stream to the file.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
```



<span data-ttu-id="36135-160">La méthode **WriteSource** du frame est utilisée pour écrire les données de pixels de l’image.</span><span class="sxs-lookup"><span data-stu-id="36135-160">The frame's **WriteSource** method is used to write the pixel data for the image.</span></span> <span data-ttu-id="36135-161">Notez que cette opération est effectuée une fois que les métadonnées ont été écrites.</span><span class="sxs-lookup"><span data-stu-id="36135-161">Note that this is done after the metadata has been written.</span></span> <span data-ttu-id="36135-162">Cela est nécessaire pour garantir que les métadonnées disposent d’un espace suffisant dans le fichier image.</span><span class="sxs-lookup"><span data-stu-id="36135-162">This is necessary to ensure that the metadata has enough space within the image file.</span></span> <span data-ttu-id="36135-163">Une fois les données de pixels écrites, le frame est écrit dans le flux à l’aide de la méthode **Commit** du frame.</span><span class="sxs-lookup"><span data-stu-id="36135-163">After the pixel data is written, the frame is written to the stream using the frame's **Commit** method.</span></span> <span data-ttu-id="36135-164">Une fois que tous les frames ont été traités, l’encodeur (et donc l’image) est finalisé à l’aide de la méthode **Commit** de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="36135-164">After all frames have been processed, the encoder (and thus the image) is finalized using the encoder's **Commit** method.</span></span>

<span data-ttu-id="36135-165">Une fois que vous avez validé le frame, vous devez libérer les objets COM créés dans la boucle.</span><span class="sxs-lookup"><span data-stu-id="36135-165">Once you commit the frame, you must release the COM objects created in the loop.</span></span>

## <a name="jpeg-re-encode-example-code"></a><span data-ttu-id="36135-166">Exemple de code de recodage JPEG</span><span class="sxs-lookup"><span data-stu-id="36135-166">JPEG Re-encode Example Code</span></span>

<span data-ttu-id="36135-167">Voici le code des parties 1 à 6 dans un bloc convienient.</span><span class="sxs-lookup"><span data-stu-id="36135-167">The following is the code from Parts 1 through 6 in one convienient block.</span></span>


```C++
#include <Windows.h>
#include <Wincodecsdk.h>

int main()
{
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }

    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }

    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }

            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }

            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }

            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="36135-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36135-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="36135-169">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="36135-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="36135-170">Vue d’ensemble des métadonnées WIC</span><span class="sxs-lookup"><span data-stu-id="36135-170">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="36135-171">Vue d’ensemble du langage de requête de métadonnées</span><span class="sxs-lookup"><span data-stu-id="36135-171">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="36135-172">Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image</span><span class="sxs-lookup"><span data-stu-id="36135-172">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="36135-173">Vue d’ensemble de l’extensibilité des métadonnées</span><span class="sxs-lookup"><span data-stu-id="36135-173">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
