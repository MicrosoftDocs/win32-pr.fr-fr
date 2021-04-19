---
description: Cette rubrique explique comment créer un décodeur bitmap à l’aide d’un flux.
ms.assetid: 982d2110-ff2f-43e0-a931-cb2b8146ad0a
title: Comment créer un décodeur à l’aide d’un flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a76badec0e2587f9136cfa6bc3ff041b76592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538376"
---
# <a name="how-to-create-a-decoder-using-a-stream"></a><span data-ttu-id="be75d-103">Comment créer un décodeur à l’aide d’un flux</span><span class="sxs-lookup"><span data-stu-id="be75d-103">How to Create a Decoder Using a Stream</span></span>

<span data-ttu-id="be75d-104">Cette rubrique explique comment créer un décodeur bitmap à l’aide d’un flux.</span><span class="sxs-lookup"><span data-stu-id="be75d-104">This topic describes how to create a bitmap decoder by using a stream.</span></span>

<span data-ttu-id="be75d-105">Pour créer un décodeur bitmap à l’aide d’un flux</span><span class="sxs-lookup"><span data-stu-id="be75d-105">To create a bitmap decoder by using a stream</span></span>

1.  <span data-ttu-id="be75d-106">Charge un fichier image dans un flux.</span><span class="sxs-lookup"><span data-stu-id="be75d-106">Load an image file into a stream.</span></span> <span data-ttu-id="be75d-107">Dans cet exemple, un flux est créé pour une ressource d’application.</span><span class="sxs-lookup"><span data-stu-id="be75d-107">In this example, a stream is created for an application resource.</span></span>

    <span data-ttu-id="be75d-108">Dans le fichier de définition de ressource d’application (. RC), définissez la ressource.</span><span class="sxs-lookup"><span data-stu-id="be75d-108">In the application resource definition (.rc) file, define the resource.</span></span> <span data-ttu-id="be75d-109">L’exemple suivant définit une `Image` ressource nommée `IDR_SAMPLE_IMAGE` .</span><span class="sxs-lookup"><span data-stu-id="be75d-109">The following example defines an `Image` resource named `IDR_SAMPLE_IMAGE`.</span></span>

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    <span data-ttu-id="be75d-110">La ressource sera ajoutée aux ressources de l’application lors de la génération de l’application.</span><span class="sxs-lookup"><span data-stu-id="be75d-110">The resource will be added to the application's resources when the application is built.</span></span>

2.  <span data-ttu-id="be75d-111">Chargez la ressource à partir de l’application.</span><span class="sxs-lookup"><span data-stu-id="be75d-111">Load the resource from the application.</span></span>

    ```C++
    HRESULT hr = S_OK;

    // WIC interface pointers.
    IWICStream *pIWICStream = NULL;
    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame = NULL;

    // Resource management.
    HRSRC imageResHandle = NULL;
    HGLOBAL imageResDataHandle = NULL;
    void *pImageFile = NULL;
    DWORD imageFileSize = 0;

    // Locate the resource in the application's executable.
    imageResHandle = FindResource(
       NULL,             // This component.
       L"SampleImage",   // Resource name.
       L"Image");        // Resource type.

    hr = (imageResHandle ? S_OK : E_FAIL);

    // Load the resource to the HGLOBAL.
    if (SUCCEEDED(hr)){
       imageResDataHandle = LoadResource(NULL, imageResHandle);
       hr = (imageResDataHandle ? S_OK : E_FAIL);
    }
    
    ```

    

3.  <span data-ttu-id="be75d-112">Verrouillez la ressource et récupérez la taille.</span><span class="sxs-lookup"><span data-stu-id="be75d-112">Lock the resource and get the size.</span></span>

    ```C++
    // Lock the resource to retrieve memory pointer.
    if (SUCCEEDED(hr)){
       pImageFile = LockResource(imageResDataHandle);
       hr = (pImageFile ? S_OK : E_FAIL);
    }

    // Calculate the size.
    if (SUCCEEDED(hr)){
       imageFileSize = SizeofResource(NULL, imageResHandle);
       hr = (imageFileSize ? S_OK : E_FAIL);
    }
    
    ```

    

4.  <span data-ttu-id="be75d-113">Créez un [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) pour créer des objets WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="be75d-113">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  <span data-ttu-id="be75d-114">Utilisez la méthode [**CreateStream,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) pour créer un objet [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) et l’initialiser à l’aide du pointeur mémoire d’image.</span><span class="sxs-lookup"><span data-stu-id="be75d-114">Use the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object and initialize it by using the image memory pointer.</span></span>

    ```C++
    // Create a WIC stream to map onto the memory.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateStream(&pIWICStream);
    }

    // Initialize the stream with the memory pointer and size.
    if (SUCCEEDED(hr)){
       hr = pIWICStream->InitializeFromMemory(
             reinterpret_cast<BYTE*>(pImageFile),
             imageFileSize);
    }
    ```

    

6.  <span data-ttu-id="be75d-115">Créez une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) à partir du nouvel objet de flux à l’aide de la méthode [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) .</span><span class="sxs-lookup"><span data-stu-id="be75d-115">Create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from the new stream object using the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

    ```C++
    // Create a decoder for the stream.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateDecoderFromStream(
          pIWICStream,                   // The stream to use to create the decoder
          NULL,                          // Do not prefer a particular vendor
          WICDecodeMetadataCacheOnLoad,  // Cache metadata when needed
          &pIDecoder);                   // Pointer to the decoder
    }
    ```

    

7.  <span data-ttu-id="be75d-116">Obtient le premier [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de l’image.</span><span class="sxs-lookup"><span data-stu-id="be75d-116">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="be75d-117">Le format de fichier JPEG ne prend en charge qu’une seule trame.</span><span class="sxs-lookup"><span data-stu-id="be75d-117">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="be75d-118">Étant donné que le fichier de cet exemple est un fichier JPEG, le premier frame ( `0` ) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="be75d-118">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="be75d-119">Pour les formats d’image qui ont plusieurs frames, consultez [Comment récupérer les frames d’une image](-wic-bitmapsources-howto-retrieveimageframes.md) pour accéder à chaque image de l’image.</span><span class="sxs-lookup"><span data-stu-id="be75d-119">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

8.  <span data-ttu-id="be75d-120">Traitez le frame d’image.</span><span class="sxs-lookup"><span data-stu-id="be75d-120">Process the image frame.</span></span> <span data-ttu-id="be75d-121">Pour plus d’informations sur les objets [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="be75d-121">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="be75d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be75d-122">See Also</span></span>

[<span data-ttu-id="be75d-123">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="be75d-123">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="be75d-124">Référence</span><span class="sxs-lookup"><span data-stu-id="be75d-124">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="be75d-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="be75d-125">Samples</span></span>](-wic-samples.md)


 

 



