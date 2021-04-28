---
description: Création d’un processeur vidéo DXVA-HD
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Création d’un processeur vidéo DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89c5a361335f83296eec538a5a6a710b9e19604
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102597"
---
# <a name="creating-a-dxva-hd-video-processor"></a><span data-ttu-id="b6131-103">Création d’un processeur vidéo DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="b6131-103">Creating a DXVA-HD Video Processor</span></span>

<span data-ttu-id="b6131-104">La haute définition de Microsoft DirectX Video Acceleration (DXVA-HD) utilise deux interfaces principales :</span><span class="sxs-lookup"><span data-stu-id="b6131-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) uses two primary interfaces:</span></span>

-   <span data-ttu-id="b6131-105">[**IDXVAHD \_ Appareil**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span><span class="sxs-lookup"><span data-stu-id="b6131-105">[**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device).</span></span> <span data-ttu-id="b6131-106">Représente l’appareil DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="b6131-106">Represents the DXVA-HD device.</span></span> <span data-ttu-id="b6131-107">Utilisez cette interface pour interroger les fonctionnalités de l’appareil et créer le processeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="b6131-107">Use this interface to query the device capabilities and create the video processor.</span></span>
-   <span data-ttu-id="b6131-108">[**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span><span class="sxs-lookup"><span data-stu-id="b6131-108">[**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor).</span></span> <span data-ttu-id="b6131-109">Représente un ensemble de fonctionnalités de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="b6131-109">Represents a set of video processing capabilities.</span></span> <span data-ttu-id="b6131-110">Utilisez cette interface pour effectuer le blit de traitement vidéo.</span><span class="sxs-lookup"><span data-stu-id="b6131-110">Use this interface to perform the video processing blit.</span></span>

<span data-ttu-id="b6131-111">Dans le code qui suit, les variables globales suivantes sont supposées :</span><span class="sxs-lookup"><span data-stu-id="b6131-111">In the code that follows, the following global variables are assumed:</span></span>


```C++
IDirect3D9Ex            *g_pD3D = NULL;     
IDirect3DDevice9Ex      *g_pD3DDevice = NULL;   // Direct3D device.
IDXVAHD_Device          *g_pDXVAHD = NULL;      // DXVA-HD device.
IDXVAHD_VideoProcessor  *g_pDXVAVP = NULL;      // DXVA-HD video processor.
IDirect3DSurface9       *g_pSurface = NULL;     // Video surface.
        
const D3DFORMAT     RENDER_TARGET_FORMAT = D3DFMT_X8R8G8B8;
const D3DFORMAT     VIDEO_FORMAT         = D3DFMT_X8R8G8B8; 
const UINT          VIDEO_FPS            = 60;
const UINT          VIDEO_WIDTH          = 640;
const UINT          VIDEO_HEIGHT         = 480;
```



<span data-ttu-id="b6131-112">Pour créer un processeur vidéo DXVA-HD :</span><span class="sxs-lookup"><span data-stu-id="b6131-112">To create a DXVA-HD video processor:</span></span>

1.  <span data-ttu-id="b6131-113">Remplissez une structure [**\_ \_ desc content DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) avec une description du contenu vidéo.</span><span class="sxs-lookup"><span data-stu-id="b6131-113">Fill in a [**DXVAHD\_CONTENT\_DESC**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) structure with a description of the video content.</span></span> <span data-ttu-id="b6131-114">Le pilote utilise ces informations comme indication pour optimiser les fonctionnalités du processeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="b6131-114">The driver uses this information as a hint to optimize the capabilities of the video processor.</span></span> <span data-ttu-id="b6131-115">La structure ne contient pas de description de format complète.</span><span class="sxs-lookup"><span data-stu-id="b6131-115">The structure does not contain a complete format description.</span></span>
    ```C++
        DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

        DXVAHD_CONTENT_DESC desc;

        desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
        desc.InputFrameRate = fps;
        desc.InputWidth = VIDEO_WIDTH;
        desc.InputHeight = VIDEO_HEIGHT;
        desc.OutputFrameRate = fps;
        desc.OutputWidth = VIDEO_WIDTH;
        desc.OutputHeight = VIDEO_HEIGHT;
    ```

    

2.  <span data-ttu-id="b6131-116">Appelez [**DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) pour créer l’appareil DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="b6131-116">Call [**DXVAHD\_CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) to create the DXVA-HD device.</span></span> <span data-ttu-id="b6131-117">Cette fonction retourne un pointeur vers l’interface de l' [**\_ appareil IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) .</span><span class="sxs-lookup"><span data-stu-id="b6131-117">This function returns a pointer to the [**IDXVAHD\_Device**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) interface.</span></span>
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  <span data-ttu-id="b6131-118">Appelez [**IDXVAHD \_ Device :: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span><span class="sxs-lookup"><span data-stu-id="b6131-118">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps).</span></span> <span data-ttu-id="b6131-119">Cette méthode remplit une structure [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) avec les fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b6131-119">This method fills in a [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure with the device capabilities.</span></span> <span data-ttu-id="b6131-120">Si vous avez besoin de fonctionnalités de traitement vidéo spécifiques, telles que la gestion des luminances ou le filtrage d’images, vérifiez leur disponibilité à l’aide de cette structure.</span><span class="sxs-lookup"><span data-stu-id="b6131-120">If you require specific video processing features, such as luma keying or image filtering, check their availability by using this structure.</span></span>
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  <span data-ttu-id="b6131-121">Vérifiez si l’appareil DXVA-HD prend en charge les formats vidéo d’entrée dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="b6131-121">Check whether the DXVA-HD device supports the input video formats that you require.</span></span> <span data-ttu-id="b6131-122">La rubrique [vérification de la prise en charge des formats DXVA-HD](checking-supported-dxva-hd-formats.md) décrit cette étape plus en détail.</span><span class="sxs-lookup"><span data-stu-id="b6131-122">The topic [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
5.  <span data-ttu-id="b6131-123">Vérifiez si le périphérique DXVA-HD prend en charge le format de sortie dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="b6131-123">Check whether the DXVA-HD device supports the output format that you require.</span></span> <span data-ttu-id="b6131-124">La section [vérification de la prise en charge des formats DXVA-HD](checking-supported-dxva-hd-formats.md) décrit cette étape plus en détail.</span><span class="sxs-lookup"><span data-stu-id="b6131-124">The section [Checking Supported DXVA-HD Formats](checking-supported-dxva-hd-formats.md) describes this step in more detail.</span></span>
6.  <span data-ttu-id="b6131-125">Allouez un tableau de structures [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) .</span><span class="sxs-lookup"><span data-stu-id="b6131-125">Allocate an array of [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structures.</span></span> <span data-ttu-id="b6131-126">Le nombre d’éléments de tableau qui doivent être alloués est donné par le membre **VideoProcessorCount** de la structure [**\_ VPDEVCAPS DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) , obtenu à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="b6131-126">The number of array elements that must be allocated is given by the **VideoProcessorCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure, obtained in step 3.</span></span>
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  <span data-ttu-id="b6131-127">Chaque [**structure \_ VPCAPS DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) représente un processeur vidéo distinct.</span><span class="sxs-lookup"><span data-stu-id="b6131-127">Each [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure represents a distinct video processor.</span></span> <span data-ttu-id="b6131-128">Vous pouvez parcourir ce tableau pour découvrir les fonctionnalités de chaque processeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="b6131-128">You can loop through this array to discover the capabilities of each video processor.</span></span> <span data-ttu-id="b6131-129">La structure comprend des informations sur les fonctionnalités de désentrelacement, de télécinéma et de conversion de la fréquence d’images du processeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="b6131-129">The structure includes information about the deinterlacing, telecine, and frame-rate conversion capabilities of the video processor.</span></span>
8.  <span data-ttu-id="b6131-130">Sélectionnez un processeur vidéo à créer.</span><span class="sxs-lookup"><span data-stu-id="b6131-130">Select a video processor to create.</span></span> <span data-ttu-id="b6131-131">Le membre **VPGuid** de la structure [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) contient un GUID qui identifie de façon unique le processeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="b6131-131">The **VPGuid** member of the [**DXVAHD\_VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) structure contains a GUID that uniquely identifies the video processor.</span></span> <span data-ttu-id="b6131-132">Transmettez ce GUID à la méthode [**IDXVAHD \_ Device :: CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) .</span><span class="sxs-lookup"><span data-stu-id="b6131-132">Pass this GUID to the [**IDXVAHD\_Device::CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) method.</span></span> <span data-ttu-id="b6131-133">La méthode retourne un pointeur [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) .</span><span class="sxs-lookup"><span data-stu-id="b6131-133">The method returns an [**IDXVAHD\_VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) pointer.</span></span>
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  <span data-ttu-id="b6131-134">Vous pouvez également appeler [**IDXVAHD \_ Device :: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) pour créer un tableau de surfaces vidéo d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b6131-134">Optionally, call [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) to create an array of input video surfaces.</span></span>

<span data-ttu-id="b6131-135">L’exemple de code suivant montre la séquence complète des étapes :</span><span class="sxs-lookup"><span data-stu-id="b6131-135">The following code example shows the complete sequence of steps:</span></span>


```C++
// Initializes the DXVA-HD video processor.

// NOTE: The following example makes some simplifying assumptions:
//
// 1. There is a single input stream.
// 2. The input frame rate matches the output frame rate.
// 3. No advanced DXVA-HD features are needed, such as luma keying or IVTC.
// 4. The application uses a single input video surface.

HRESULT InitializeDXVAHD()
{
    if (g_pD3DDevice == NULL)
    {
        return E_FAIL;
    }

    HRESULT hr = S_OK;

    IDXVAHD_Device          *pDXVAHD = NULL;
    IDXVAHD_VideoProcessor  *pDXVAVP = NULL;
    IDirect3DSurface9       *pSurf = NULL;

    DXVAHD_RATIONAL fps = { VIDEO_FPS, 1 }; 

    DXVAHD_CONTENT_DESC desc;

    desc.InputFrameFormat = DXVAHD_FRAME_FORMAT_PROGRESSIVE;
    desc.InputFrameRate = fps;
    desc.InputWidth = VIDEO_WIDTH;
    desc.InputHeight = VIDEO_HEIGHT;
    desc.OutputFrameRate = fps;
    desc.OutputWidth = VIDEO_WIDTH;
    desc.OutputHeight = VIDEO_HEIGHT;

#ifdef USE_SOFTWARE_PLUGIN    
    HMODULE hSWPlugin = LoadLibrary(L"C:\\dxvahdsw.dll");

    PDXVAHDSW_Plugin pSWPlugin = (PDXVAHDSW_Plugin)GetProcAddress(hSWPlugin, "DXVAHDSW_Plugin");

    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc,DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        pSWPlugin, &pDXVAHD);
#else
    hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
        NULL, &pDXVAHD);
#endif
    if (FAILED(hr))
    {
        goto done;
    }

    DXVAHD_VPDEVCAPS caps;

    hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    if (FAILED(hr))
    {
        goto done;
    }

    // Check whether the device supports the input and output formats.

    hr = CheckInputFormatSupport(pDXVAHD, caps, VIDEO_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CheckOutputFormatSupport(pDXVAHD, caps, RENDER_TARGET_FORMAT);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the VP device.
    hr = CreateVPDevice(pDXVAHD, caps, &pDXVAVP);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );

    if (FAILED(hr))
    {
        goto done;
    }


    g_pDXVAHD = pDXVAHD;
    g_pDXVAHD->AddRef();

    g_pDXVAVP = pDXVAVP;
    g_pDXVAVP->AddRef();

    g_pSurface = pSurf;
    g_pSurface->AddRef();

done:
    SafeRelease(&pDXVAHD);
    SafeRelease(&pDXVAVP);
    SafeRelease(&pSurf);
    return hr;
}
```



<span data-ttu-id="b6131-136">La fonction CreateVPDevice illustrée dans cet exemple crée le processeur vidéo (étapes 5 à 7) :</span><span class="sxs-lookup"><span data-stu-id="b6131-136">The CreateVPDevice function show in this example creates the video processor (steps 5–7):</span></span>


```C++
// Creates a DXVA-HD video processor.

HRESULT CreateVPDevice(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    IDXVAHD_VideoProcessor  **ppDXVAVP
    )
{
    // Create the array of video processor caps. 
    
    DXVAHD_VPCAPS *pVPCaps = 
        new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

    if (pVPCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
        caps.VideoProcessorCount, pVPCaps);

    // At this point, an application could loop through the array and examine
    // the capabilities. For purposes of this example, however, we simply
    // create the first video processor in the list.

    if (SUCCEEDED(hr))
    {
        // The VPGuid member contains the GUID that identifies the video 
        // processor.

        hr = pDXVAHD->CreateVideoProcessor(&pVPCaps[0].VPGuid, ppDXVAVP);
    }

    delete [] pVPCaps;
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b6131-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6131-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6131-138">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="b6131-138">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



