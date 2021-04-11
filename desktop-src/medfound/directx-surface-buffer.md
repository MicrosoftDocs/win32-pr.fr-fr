---
description: Mémoire tampon de surface DirectX
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: Mémoire tampon de surface DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02211d268e23bd7185cd480bee4e4dff297293b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111787"
---
# <a name="directx-surface-buffer"></a><span data-ttu-id="4c736-103">Mémoire tampon de surface DirectX</span><span class="sxs-lookup"><span data-stu-id="4c736-103">DirectX Surface Buffer</span></span>

<span data-ttu-id="4c736-104">L’objet de mémoire tampon de surface DirectX est un tampon de média qui gère une surface Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4c736-104">The DirectX surface buffer object is a media buffer that manages a Direct3D surface.</span></span> <span data-ttu-id="4c736-105">Pour créer une instance de cet objet, appelez [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) et transmettez un pointeur vers la surface DirectX.</span><span class="sxs-lookup"><span data-stu-id="4c736-105">To create an instance of this object, call [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) and pass in a pointer to the DirectX surface.</span></span> <span data-ttu-id="4c736-106">La mémoire tampon de surface DirectX expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c736-106">The DirectX surface buffer exposes the following interfaces:</span></span>

-   [<span data-ttu-id="4c736-107">**IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="4c736-107">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [<span data-ttu-id="4c736-108">**IMF2DBuffer**</span><span class="sxs-lookup"><span data-stu-id="4c736-108">**IMF2DBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [<span data-ttu-id="4c736-109">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="4c736-109">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

<span data-ttu-id="4c736-110">Il existe plusieurs façons d’accéder à la mémoire de surface à partir de l’objet buffer :</span><span class="sxs-lookup"><span data-stu-id="4c736-110">There are several ways to access the surface memory from the buffer object:</span></span>

-   <span data-ttu-id="4c736-111">Recommandé : appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4c736-111">Recommended: Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the buffer.</span></span> <span data-ttu-id="4c736-112">Utilisez le **\_ \_ service de mémoire tampon** de l’identificateur de service Mr.</span><span class="sxs-lookup"><span data-stu-id="4c736-112">Use the service identifier **MR\_BUFFER\_SERVICE**.</span></span> <span data-ttu-id="4c736-113">La méthode retourne un pointeur vers la surface Direct3D sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="4c736-113">The method returns a pointer to the underlying Direct3D surface.</span></span>
-   <span data-ttu-id="4c736-114">Appelez [**IMF2DBuffer :: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span><span class="sxs-lookup"><span data-stu-id="4c736-114">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span></span> <span data-ttu-id="4c736-115">Cette méthode appelle **IDirect3DSurface9 :: LockRect** directement sur l’aire de conception.</span><span class="sxs-lookup"><span data-stu-id="4c736-115">This method calls **IDirect3DSurface9::LockRect** directly on the surface.</span></span> <span data-ttu-id="4c736-116">La méthode [**IMF2DBuffer :: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) appelle **UnlockRect** sur l’aire de conception.</span><span class="sxs-lookup"><span data-stu-id="4c736-116">The [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) method calls **UnlockRect** on the surface.</span></span>
-   <span data-ttu-id="4c736-117">Appelez [**IMFMediaBuffer :: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="4c736-117">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="4c736-118">En général, cela n’est pas recommandé, car il force l’objet à copier la mémoire à partir de la surface Direct3D, puis de revenir en arrière.</span><span class="sxs-lookup"><span data-stu-id="4c736-118">Generally this is not recommended, because it forces the object to copy memory from the Direct3D surface and then back again.</span></span> <span data-ttu-id="4c736-119">La méthode [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) est plus efficace.</span><span class="sxs-lookup"><span data-stu-id="4c736-119">The [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method is more efficient.</span></span>

<span data-ttu-id="4c736-120">[**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) et [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) peuvent échouer si la surface sous-jacente n’est pas verrouillable.</span><span class="sxs-lookup"><span data-stu-id="4c736-120">Both [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) can fail if the underlying surface is not lockable.</span></span> <span data-ttu-id="4c736-121">La mémoire tampon de surface DirectX implémente ces deux méthodes principalement pour les composants qui ne sont pas conçus pour fonctionner avec les surfaces Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4c736-121">The DirectX surface buffer implements these two methods primarily for components that are not designed to work with Direct3D surfaces.</span></span>

<span data-ttu-id="4c736-122">Le convertisseur vidéo amélioré (EVR) crée des mémoires tampons de surface DirectX quand le décodeur n’est pas configuré pour l’accélération vidéo DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="4c736-122">The enhanced video renderer (EVR) creates DirectX surface buffers when the decoder is not configured for DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="4c736-123">Pour plus d’informations, consultez [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span><span class="sxs-lookup"><span data-stu-id="4c736-123">For more information, see [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span></span>

### <a name="obtaining-the-direct3d-surface"></a><span data-ttu-id="4c736-124">Obtention de la surface Direct3D</span><span class="sxs-lookup"><span data-stu-id="4c736-124">Obtaining the Direct3D Surface</span></span>

<span data-ttu-id="4c736-125">Pour obtenir une surface Direct3D à partir d’un exemple de vidéo, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4c736-125">To get a Direct3D surface from a video sample, do the following:</span></span>

1.  <span data-ttu-id="4c736-126">Appelez [**IMFSample :: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) avec une valeur d’index égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="4c736-126">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) with an index value of zero.</span></span>
2.  <span data-ttu-id="4c736-127">Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) et spécifiez l’identificateur de service de **\_ mémoire \_ tampon Mr** .</span><span class="sxs-lookup"><span data-stu-id="4c736-127">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and specify the **MR\_BUFFER\_SERVICE** service identifier.</span></span>

<span data-ttu-id="4c736-128">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="4c736-128">The following code shows these steps:</span></span>


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4c736-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c736-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c736-130">Mémoires tampons de média</span><span class="sxs-lookup"><span data-stu-id="4c736-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="4c736-131">Exemples vidéo</span><span class="sxs-lookup"><span data-stu-id="4c736-131">Video Samples</span></span>](video-samples.md)
</dt> </dl>

 

 



