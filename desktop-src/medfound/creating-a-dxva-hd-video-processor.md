---
description: .
ms.assetid: 43a97dc8-19b3-412c-a015-339099bf4f6c
title: Création d’un processeur vidéo DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee524681cad43a8e140421e8e6eff30d44cabcc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527599"
---
# <a name="creating-a-dxva-hd-video-processor"></a>Création d’un processeur vidéo DXVA-HD

La haute définition de Microsoft DirectX Video Acceleration (DXVA-HD) utilise deux interfaces principales :

-   [**IDXVAHD \_ Appareil**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device). Représente l’appareil DXVA-HD. Utilisez cette interface pour interroger les fonctionnalités de l’appareil et créer le processeur vidéo.
-   [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor). Représente un ensemble de fonctionnalités de traitement vidéo. Utilisez cette interface pour effectuer le blit de traitement vidéo.

Dans le code qui suit, les variables globales suivantes sont supposées :


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



Pour créer un processeur vidéo DXVA-HD :

1.  Remplissez une structure [**\_ \_ desc content DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_content_desc) avec une description du contenu vidéo. Le pilote utilise ces informations comme indication pour optimiser les fonctionnalités du processeur vidéo. La structure ne contient pas de description de format complète.
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

    

2.  Appelez [**DXVAHD \_ CreateDevice**](/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice) pour créer l’appareil DXVA-HD. Cette fonction retourne un pointeur vers l’interface de l' [**\_ appareil IDXVAHD**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device) .
    ```C++
        hr = DXVAHD_CreateDevice(g_pD3DDevice, &desc, DXVAHD_DEVICE_USAGE_PLAYBACK_NORMAL,
            NULL, &pDXVAHD);
    ```

    

3.  Appelez [**IDXVAHD \_ Device :: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps). Cette méthode remplit une structure [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) avec les fonctionnalités de l’appareil. Si vous avez besoin de fonctionnalités de traitement vidéo spécifiques, telles que la gestion des luminances ou le filtrage d’images, vérifiez leur disponibilité à l’aide de cette structure.
    ```C++
        DXVAHD_VPDEVCAPS caps;

        hr = pDXVAHD->GetVideoProcessorDeviceCaps(&caps);
    ```

    

4.  Vérifiez si l’appareil DXVA-HD prend en charge les formats vidéo d’entrée dont vous avez besoin. La rubrique [vérification de la prise en charge des formats DXVA-HD](checking-supported-dxva-hd-formats.md) décrit cette étape plus en détail.
5.  Vérifiez si le périphérique DXVA-HD prend en charge le format de sortie dont vous avez besoin. La section [vérification de la prise en charge des formats DXVA-HD](checking-supported-dxva-hd-formats.md) décrit cette étape plus en détail.
6.  Allouez un tableau de structures [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) . Le nombre d’éléments de tableau qui doivent être alloués est donné par le membre **VideoProcessorCount** de la structure [**\_ VPDEVCAPS DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) , obtenu à l’étape 3.
    ```C++
        // Create the array of video processor caps. 
        
        DXVAHD_VPCAPS *pVPCaps = 
            new (std::nothrow) DXVAHD_VPCAPS[ caps.VideoProcessorCount ];

        if (pVPCaps == NULL)
        {
            return E_OUTOFMEMORY;
        }
    ```

    

7.  Chaque [**structure \_ VPCAPS DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) représente un processeur vidéo distinct. Vous pouvez parcourir ce tableau pour découvrir les fonctionnalités de chaque processeur vidéo. La structure comprend des informations sur les fonctionnalités de désentrelacement, de télécinéma et de conversion de la fréquence d’images du processeur vidéo.
8.  Sélectionnez un processeur vidéo à créer. Le membre **VPGuid** de la structure [**DXVAHD \_ VPCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpcaps) contient un GUID qui identifie de façon unique le processeur vidéo. Transmettez ce GUID à la méthode [**IDXVAHD \_ Device :: CreateVideoProcessor**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor) . La méthode retourne un pointeur [**IDXVAHD \_ VideoProcessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor) .
    ```C++
        HRESULT hr = pDXVAHD->GetVideoProcessorCaps(
            caps.VideoProcessorCount, pVPCaps);
    ```

    

9.  Vous pouvez également appeler [**IDXVAHD \_ Device :: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) pour créer un tableau de surfaces vidéo d’entrée.

L’exemple de code suivant montre la séquence complète des étapes :


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



La fonction CreateVPDevice illustrée dans cet exemple crée le processeur vidéo (étapes 5 à 7) :


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



