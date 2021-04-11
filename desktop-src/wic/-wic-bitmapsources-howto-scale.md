---
description: Cette rubrique montre comment mettre à l’échelle un IWICBitmapSource à l’aide du composant IWICBitmapScaler.
ms.assetid: d2c65c9b-6f52-46f7-935d-0c582ca83867
title: Mise à l’échelle d’une source bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737f72014929065bc63ec9c6021b05e38799d06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112859"
---
# <a name="how-to-scale-a-bitmap-source"></a><span data-ttu-id="1c899-103">Mise à l’échelle d’une source bitmap</span><span class="sxs-lookup"><span data-stu-id="1c899-103">How to Scale a Bitmap Source</span></span>

<span data-ttu-id="1c899-104">Cette rubrique montre comment mettre à l’échelle un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à l’aide du composant [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="1c899-104">This topic demonstrates how to scale an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) component.</span></span>

<span data-ttu-id="1c899-105">Pour mettre à l’échelle une source bitmap</span><span class="sxs-lookup"><span data-stu-id="1c899-105">To scale a bitmap source</span></span>

1.  <span data-ttu-id="1c899-106">Créez un objet [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) pour créer des objets WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="1c899-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="1c899-107">Utilisez la méthode [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) pour créer une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) à partir d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="1c899-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapScaler *pIScaler = NULL;


    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="1c899-108">Obtient le premier [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de l’image.</span><span class="sxs-lookup"><span data-stu-id="1c899-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="1c899-109">Le format de fichier JPEG ne prend en charge qu’une seule trame.</span><span class="sxs-lookup"><span data-stu-id="1c899-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="1c899-110">Étant donné que le fichier de cet exemple est un fichier JPEG, le premier frame ( `0` ) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1c899-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="1c899-111">Pour les formats d’image qui ont plusieurs frames, consultez [Comment récupérer les frames d’une image](-wic-bitmapsources-howto-retrieveimageframes.md) pour accéder à chaque image de l’image.</span><span class="sxs-lookup"><span data-stu-id="1c899-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="1c899-112">Créez le [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) à utiliser pour la mise à l’échelle de l’image.</span><span class="sxs-lookup"><span data-stu-id="1c899-112">Create the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) to use for the image scaling.</span></span>

    ```C++
    // Create the scaler.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapScaler(&pIScaler);
    }
    ```

    

5.  <span data-ttu-id="1c899-113">Initialisez l’objet scaler avec les données d’image du frame bitmap à la moitié de la taille.</span><span class="sxs-lookup"><span data-stu-id="1c899-113">Initialize the scaler object with the image data of the bitmap frame at half the size.</span></span>

    ```C++
    // Initialize the scaler to half the size of the original source.
    if (SUCCEEDED(hr))
    {
       hr = pIScaler->Initialize(
          pIDecoderFrame,                    // Bitmap source to scale.
          uiWidth/2,                         // Scale width to half of original.
          uiHeight/2,                        // Scale height to half of original.
          WICBitmapInterpolationModeFant);   // Use Fant mode interpolation.
    }
    ```

    

6.  <span data-ttu-id="1c899-114">Dessinez ou traitez la source bitmap mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="1c899-114">Draw or process the scaled bitmap source.</span></span>

    <span data-ttu-id="1c899-115">L’illustration suivante montre la mise à l’échelle de l’image.</span><span class="sxs-lookup"><span data-stu-id="1c899-115">The following illustration demonstrates imaging scaling.</span></span> <span data-ttu-id="1c899-116">L’image d’origine sur la gauche est de 200 x 130 pixels.</span><span class="sxs-lookup"><span data-stu-id="1c899-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="1c899-117">L’image à droite est l’image d’origine mise à l’échelle à la moitié de la taille.</span><span class="sxs-lookup"><span data-stu-id="1c899-117">The image on the right is the original image scaled to half the size.</span></span>

    ![Illustration montrant la mise à l’échelle d’une image à une taille plus petite](graphics/scaledregion.png)

## <a name="see-also"></a><span data-ttu-id="1c899-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c899-119">See Also</span></span>

[<span data-ttu-id="1c899-120">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="1c899-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="1c899-121">Référence</span><span class="sxs-lookup"><span data-stu-id="1c899-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="1c899-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="1c899-122">Samples</span></span>](-wic-samples.md)


 

 



