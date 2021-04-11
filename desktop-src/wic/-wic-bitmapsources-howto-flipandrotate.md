---
description: Cette rubrique montre comment faire pivoter un IWICBitmapSource à l’aide d’un composant IWICBitmapFlipRotator.
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: Comment retourner et faire pivoter une source bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f6a805144025f185a4f4793fc4fafb27d7695a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112863"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a><span data-ttu-id="954fd-103">Comment retourner et faire pivoter une source bitmap</span><span class="sxs-lookup"><span data-stu-id="954fd-103">How to Flip and Rotate a Bitmap Source</span></span>

<span data-ttu-id="954fd-104">Cette rubrique montre comment faire pivoter un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à l’aide d’un composant [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="954fd-104">This topic demonstrates how to rotate an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) by using an [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) component.</span></span>

<span data-ttu-id="954fd-105">Pour retourner et faire pivoter une source bitmap</span><span class="sxs-lookup"><span data-stu-id="954fd-105">To flip and rotate a bitmap source</span></span>

1.  <span data-ttu-id="954fd-106">Créez un objet [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) pour créer des objets WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="954fd-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="954fd-107">Utilisez la méthode [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) pour créer une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) à partir d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="954fd-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapFlipRotator *pIFlipRotator = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="954fd-108">Obtient le premier [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de l’image.</span><span class="sxs-lookup"><span data-stu-id="954fd-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="954fd-109">Le format de fichier JPEG ne prend en charge qu’une seule trame.</span><span class="sxs-lookup"><span data-stu-id="954fd-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="954fd-110">Étant donné que le fichier de cet exemple est un fichier JPEG, le premier frame ( `0` ) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="954fd-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="954fd-111">Pour les formats d’image qui ont plusieurs frames, consultez [Comment récupérer les frames d’une image](-wic-bitmapsources-howto-retrieveimageframes.md) pour accéder à chaque image de l’image.</span><span class="sxs-lookup"><span data-stu-id="954fd-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="954fd-112">Créez le [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) à utiliser pour le retournement de l’image.</span><span class="sxs-lookup"><span data-stu-id="954fd-112">Create the [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) to use for flipping the image.</span></span>

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  <span data-ttu-id="954fd-113">Initialise l’objet Flip/Rotate avec les données image du frame bitmap retourné horizontalement (le long de l’axe vertical y).</span><span class="sxs-lookup"><span data-stu-id="954fd-113">Initialize the flip/rotator object with the image data of the bitmap frame flipped horizontally (along the vertical y-axis).</span></span>

    ```C++
    // Initialize the flip/rotator to flip the original source horizontally.
    if (SUCCEEDED(hr))
    {
       hr = pIFlipRotator->Initialize(
          pIDecoderFrame,                     // Bitmap source to flip.
          WICBitmapTransformFlipHorizontal);  // Flip the pixels along the 
                                              //  vertical y-axis.
    }
    ```

    

    <span data-ttu-id="954fd-114">Consultez [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) pour obtenir des rotations et des options de retournement supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="954fd-114">See [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) for additional rotations and flipping options.</span></span>

6.  <span data-ttu-id="954fd-115">Dessinez ou traitez la source bitmap retournée.</span><span class="sxs-lookup"><span data-stu-id="954fd-115">Draw or process the flipped bitmap source.</span></span>

    > [!Note]  
    > <span data-ttu-id="954fd-116">L’interface [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) hérite de l’interface [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) . vous pouvez donc utiliser l’objet Flip/Rotate initialisé n’importe où qui accepte un **IWICBitmapSource**.</span><span class="sxs-lookup"><span data-stu-id="954fd-116">The [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) interface inherits from the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, so you can use the initialized flip/rotator object anywhere that accepts a **IWICBitmapSource**.</span></span>

     

    <span data-ttu-id="954fd-117">L’illustration suivante montre le basculement d’une image horizontale (le long de l’axe vertical x).</span><span class="sxs-lookup"><span data-stu-id="954fd-117">The following illustration demonstrates flipping an imaging horizontally (along the vertical x-axis).</span></span>

    ![Illustration montrant un retournement horizontal (le long de l’axe x de vérité) d’une image](graphics/fliphorizontal.png)

## <a name="see-also"></a><span data-ttu-id="954fd-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="954fd-119">See Also</span></span>

[<span data-ttu-id="954fd-120">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="954fd-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="954fd-121">Référence</span><span class="sxs-lookup"><span data-stu-id="954fd-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="954fd-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="954fd-122">Samples</span></span>](-wic-samples.md)


 

 



