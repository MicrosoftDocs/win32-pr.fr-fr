---
description: Cette rubrique montre comment décoder une image à plusieurs frames et récupérer chaque frame pour traitement.
ms.assetid: e4f69608-7bf1-4d54-b586-b749526700c9
title: Comment récupérer des frames à partir d’une image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeeb19e0a0ac69f75673df0736fd0bd4987b3423
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112862"
---
# <a name="how-to-retrieve-the-frames-from-an-image"></a><span data-ttu-id="678ab-103">Comment récupérer des frames à partir d’une image</span><span class="sxs-lookup"><span data-stu-id="678ab-103">How to Retrieve the Frames from an Image</span></span>

<span data-ttu-id="678ab-104">Cette rubrique montre comment décoder une image à plusieurs frames et récupérer chaque frame pour traitement.</span><span class="sxs-lookup"><span data-stu-id="678ab-104">This topic demonstrates how to decode a multi-frame image and retrieve each frame for processing.</span></span>

<span data-ttu-id="678ab-105">Pour récupérer les frames d’une image</span><span class="sxs-lookup"><span data-stu-id="678ab-105">To retrieve the frames of an image</span></span>

1.  <span data-ttu-id="678ab-106">Créez un [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) pour créer des objets WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="678ab-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="678ab-107">Utilisez la méthode [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) pour créer une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) à partir d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="678ab-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    UINT nFrameCount = 0;
    UINT uiWidth, uiHeight;

    // Create decoder for an image.
    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"creek.tiff",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="678ab-108">Récupérez le nombre de frames dans les images.</span><span class="sxs-lookup"><span data-stu-id="678ab-108">Retrieve the number of frames in the images.</span></span>

    ```C++
    // Retrieve the frame count of the image.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrameCount(&nFrameCount);
    }
    ```

    

4.  <span data-ttu-id="678ab-109">Traitez chaque frame en obtenant un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) pour chaque image de l’image.</span><span class="sxs-lookup"><span data-stu-id="678ab-109">Process each frame by obtaining an [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) for each frame in the image.</span></span>

    ```C++
    // Process each frame in the image.
    for (UINT i=0; i < nFrameCount; i++)
    {
       // Retrieve the next bitmap frame.
       if (SUCCEEDED(hr))
       {
          hr = pIDecoder->GetFrame(i, &pIDecoderFrame);
       }

       // Retrieve the size of the bitmap frame.
       if (SUCCEEDED(hr))
       {
          hr = pIDecoderFrame->GetSize(&uiWidth, &uiHeight);
       }

       // Additional frame processing.
       // ...

       SafeRelease(&pIDecoderFrame);
    }
    ```

    

## <a name="see-also"></a><span data-ttu-id="678ab-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="678ab-110">See Also</span></span>

[<span data-ttu-id="678ab-111">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="678ab-111">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="678ab-112">Référence</span><span class="sxs-lookup"><span data-stu-id="678ab-112">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="678ab-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="678ab-113">Samples</span></span>](-wic-samples.md)


 

 



