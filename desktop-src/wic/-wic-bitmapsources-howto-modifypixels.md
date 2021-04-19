---
description: Cette rubrique montre comment modifier les pixels d’une source bitmap à l’aide des composants IWICBitmap et IWICBitmapLock.
ms.assetid: a08af015-bc42-4a31-af03-106714b08d08
title: Comment modifier les pixels d’une source bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be623d540fcd313476ea5c7ec5e724231d33aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534580"
---
# <a name="how-to-modify-the-pixels-of-a-bitmap-source"></a><span data-ttu-id="678db-103">Comment modifier les pixels d’une source bitmap</span><span class="sxs-lookup"><span data-stu-id="678db-103">How to Modify the Pixels of a Bitmap Source</span></span>

<span data-ttu-id="678db-104">Cette rubrique montre comment modifier les pixels d’une source bitmap à l’aide des composants [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) et [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="678db-104">This topic demonstrates how to modify the pixels of a bitmap source using the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) and [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) components.</span></span>

<span data-ttu-id="678db-105">Pour modifier les pixels d’une source bitmap</span><span class="sxs-lookup"><span data-stu-id="678db-105">To modify the pixels of a bitmap source</span></span>

1.  <span data-ttu-id="678db-106">Créez un objet [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) pour créer des objets WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="678db-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="678db-107">Utilisez la méthode [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) pour créer une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) à partir d’un fichier image.</span><span class="sxs-lookup"><span data-stu-id="678db-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="678db-108">Obtient le premier [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de l’image.</span><span class="sxs-lookup"><span data-stu-id="678db-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="678db-109">Le format de fichier JPEG ne prend en charge qu’une seule trame.</span><span class="sxs-lookup"><span data-stu-id="678db-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="678db-110">Étant donné que le fichier de cet exemple est un fichier JPEG, le premier frame ( `0` ) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="678db-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="678db-111">Pour les formats d’image qui ont plusieurs frames, consultez [Comment récupérer les frames d’une image](-wic-bitmapsources-howto-retrieveimageframes.md) pour accéder à chaque image de l’image.</span><span class="sxs-lookup"><span data-stu-id="678db-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="678db-112">Créez un [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) à partir du frame d’image obtenu précédemment.</span><span class="sxs-lookup"><span data-stu-id="678db-112">Create an [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) from the previously obtained image frame.</span></span>

    ```C++
    IWICBitmap *pIBitmap = NULL;
    IWICBitmapLock *pILock = NULL;

    UINT uiWidth = 10;
    UINT uiHeight = 10;

    WICRect rcLock = { 0, 0, uiWidth, uiHeight };

    // Create the bitmap from the image frame.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFromSource(
          pIDecoderFrame,          // Create a bitmap from the image frame
          WICBitmapCacheOnDemand,  // Cache metadata when needed
          &pIBitmap);              // Pointer to the bitmap
    }
    ```

    

5.  <span data-ttu-id="678db-113">Obtient un [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) pour un rectangle spécifié du [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap).</span><span class="sxs-lookup"><span data-stu-id="678db-113">Obtain an [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) for a specified rectangle of the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap).</span></span>

    ```C++
    if (SUCCEEDED(hr))
    {
       // Obtain a bitmap lock for exclusive write.
       // The lock is for a 10x10 rectangle starting at the top left of the
       // bitmap.
       hr = pIBitmap->Lock(&rcLock, WICBitmapLockWrite, &pILock);
    ```

    

6.  <span data-ttu-id="678db-114">Traitez les données de pixels qui sont maintenant verrouillées par l’objet [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="678db-114">Process the pixel data that is now locked by the [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

    ```C++
       if (SUCCEEDED(hr))
       {
          UINT cbBufferSize = 0;
          BYTE *pv = NULL;

          // Retrieve a pointer to the pixel data.
          if (SUCCEEDED(hr))
          {
             hr = pILock->GetDataPointer(&cbBufferSize, &pv);
          }
          
          // Pixel manipulation using the image data pointer pv.
          // ...

          // Release the bitmap lock.
          SafeRelease(&pILock);
       }
    }
    ```

    

    <span data-ttu-id="678db-115">Pour déverrouiller le [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), appelez [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur tous les objets [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) associés au **IWICBitmap**.</span><span class="sxs-lookup"><span data-stu-id="678db-115">To unlock the [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) objects associated with the **IWICBitmap**.</span></span>

7.  <span data-ttu-id="678db-116">Nettoyez les objets créés.</span><span class="sxs-lookup"><span data-stu-id="678db-116">Clean up created objects.</span></span>

    ```C++
    SafeRelease(&pIBitmap);
    SafeRelease(&pIDecoder);
    SafeRelease(&pIDecoderFrame);
    ```

    

## <a name="see-also"></a><span data-ttu-id="678db-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="678db-117">See Also</span></span>

[<span data-ttu-id="678db-118">Guide de programmation</span><span class="sxs-lookup"><span data-stu-id="678db-118">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="678db-119">Référence</span><span class="sxs-lookup"><span data-stu-id="678db-119">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="678db-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="678db-120">Samples</span></span>](-wic-samples.md)


 

 
