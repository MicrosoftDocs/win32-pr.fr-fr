---
description: Cette rubrique explique comment créer un décodeur bitmap à l’aide d’un nom de fichier image.
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: Comment créer un décodeur à l’aide d’un nom de fichier image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113ea82b741f2a8dab6c92d6391d65eb7d7e99c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520159"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a><span data-ttu-id="1e6c0-103">Comment créer un décodeur à l’aide d’un nom de fichier image</span><span class="sxs-lookup"><span data-stu-id="1e6c0-103">How to Create a Decoder Using an Image Filename</span></span>

<span data-ttu-id="1e6c0-104">Cette rubrique explique comment créer un décodeur bitmap à l’aide d’un nom de fichier image.</span><span class="sxs-lookup"><span data-stu-id="1e6c0-104">This topic describes how to create a bitmap decoder by using an image filename.</span></span>

<span data-ttu-id="1e6c0-105">Pour créer un décodeur bitmap à l’aide d’un nom de fichier image</span><span class="sxs-lookup"><span data-stu-id="1e6c0-105">To create a bitmap decoder by using an image filename</span></span>

1.  <span data-ttu-id="1e6c0-106">Créez un objet [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) pour créer des objets WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="1e6c0-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="1e6c0-107">Utilisez la méthode [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) pour créer une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) à partir d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="1e6c0-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="1e6c0-108">Obtient le premier [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de l’image.</span><span class="sxs-lookup"><span data-stu-id="1e6c0-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="1e6c0-109">Le format de fichier JPEG ne prend en charge qu’une seule trame.</span><span class="sxs-lookup"><span data-stu-id="1e6c0-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="1e6c0-110">Étant donné que le fichier de cet exemple est un fichier JPEG, le premier frame ( `0` ) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1e6c0-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="1e6c0-111">Pour les formats d’image qui ont plusieurs frames, consultez [Comment récupérer les frames d’une image](-wic-bitmapsources-howto-retrieveimageframes.md) pour accéder à chaque image de l’image.</span><span class="sxs-lookup"><span data-stu-id="1e6c0-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="1e6c0-112">Traitez le frame d’image.</span><span class="sxs-lookup"><span data-stu-id="1e6c0-112">Process the image frame.</span></span> <span data-ttu-id="1e6c0-113">Pour plus d’informations sur les objets [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="1e6c0-113">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1e6c0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e6c0-114">See Also</span></span>

[<span data-ttu-id="1e6c0-115">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="1e6c0-115">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="1e6c0-116">Référence</span><span class="sxs-lookup"><span data-stu-id="1e6c0-116">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="1e6c0-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="1e6c0-117">Samples</span></span>](-wic-samples.md)


 

 



