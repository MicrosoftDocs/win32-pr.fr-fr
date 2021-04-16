---
description: Cette rubrique montre comment obtenir une partie rectangulaire d’un IWICBitmapSource à l’aide d’un composant IWICBitmapClipper.
ms.assetid: c9834827-8e1d-436d-be82-c1a2a2f7ca5c
title: Comment découper une source bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43919e03d5d866d37ad4af203e741d2b10e60889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563556"
---
# <a name="how-to-clip-a-bitmap-source"></a><span data-ttu-id="f987b-103">Comment découper une source bitmap</span><span class="sxs-lookup"><span data-stu-id="f987b-103">How to Clip a Bitmap Source</span></span>

<span data-ttu-id="f987b-104">Cette rubrique montre comment obtenir une partie rectangulaire d’un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à l’aide d’un composant [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="f987b-104">This topic demonstrates how to obtain a rectangular portion of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using an [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) component.</span></span>

<span data-ttu-id="f987b-105">Pour découper une source bitmap</span><span class="sxs-lookup"><span data-stu-id="f987b-105">To clip a bitmap source</span></span>

1.  <span data-ttu-id="f987b-106">Créez un objet [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) pour créer des objets WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="f987b-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="f987b-107">Utilisez la méthode [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) pour créer une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) à partir d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="f987b-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="f987b-108">Obtient le premier [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de l’image.</span><span class="sxs-lookup"><span data-stu-id="f987b-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="f987b-109">Le format de fichier JPEG ne prend en charge qu’une seule trame.</span><span class="sxs-lookup"><span data-stu-id="f987b-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="f987b-110">Étant donné que le fichier de cet exemple est un fichier JPEG, le premier frame ( `0` ) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f987b-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="f987b-111">Pour les formats d’image qui ont plusieurs frames, consultez [Comment récupérer les frames d’une image](-wic-bitmapsources-howto-retrieveimageframes.md) pour accéder à chaque image de l’image.</span><span class="sxs-lookup"><span data-stu-id="f987b-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="f987b-112">Créez le [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) à utiliser pour la capture d’image.</span><span class="sxs-lookup"><span data-stu-id="f987b-112">Create the [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) to use for the image clipping.</span></span>

    ```C++
    IWICBitmapClipper *pIClipper = NULL;

    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapClipper(&pIClipper);
    }
    ```

    

5.  <span data-ttu-id="f987b-113">Initialise l’objet Clipper avec les données d’image dans le rectangle donné du frame bitmap.</span><span class="sxs-lookup"><span data-stu-id="f987b-113">Initialize the clipper object with the image data within the given rectangle of the bitmap frame.</span></span>

    ```C++
    // Create the clipping rectangle.
    WICRect rcClip = { 0, 0, uiWidth/2, uiHeight/2 };

    // Initialize the clipper with the given rectangle of the frame's image data.
    if (SUCCEEDED(hr))
    {
       hr = pIClipper->Initialize(pIDecoderFrame, &rcClip);
    }
    ```

    

6.  <span data-ttu-id="f987b-114">Dessinez ou traitez l’image découpée.</span><span class="sxs-lookup"><span data-stu-id="f987b-114">Draw or process the clipped image.</span></span>

    <span data-ttu-id="f987b-115">L’illustration suivante montre le découpage d’image.</span><span class="sxs-lookup"><span data-stu-id="f987b-115">The following illustration demonstrates imaging clipping.</span></span> <span data-ttu-id="f987b-116">L’image d’origine sur la gauche est de 200 x 130 pixels.</span><span class="sxs-lookup"><span data-stu-id="f987b-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="f987b-117">L’image à droite est l’image d’origine découpée en rectangle défini comme `{20,20,100,100}` .</span><span class="sxs-lookup"><span data-stu-id="f987b-117">The image on the right is the original image clipped to a rectangle defined as `{20,20,100,100}`.</span></span>

    ![illustration du découpage d’image](graphics/cliparegion_axisalignedclip.png)

## <a name="see-also"></a><span data-ttu-id="f987b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f987b-119">See Also</span></span>

[<span data-ttu-id="f987b-120">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="f987b-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="f987b-121">Référence</span><span class="sxs-lookup"><span data-stu-id="f987b-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="f987b-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="f987b-122">Samples</span></span>](-wic-samples.md)


 

 



