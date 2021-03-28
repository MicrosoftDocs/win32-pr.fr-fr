---
title: Comment créer un appareil de référence
description: Cette rubrique montre comment créer un appareil de référence qui implémente une implémentation logicielle très précise du Runtime.
ms.assetid: 00d3f5f2-02c6-4ff4-82a9-0726ad4a8cb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dec5f3834bf1f10027da2a3f3a8e22acdee742b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380229"
---
# <a name="how-to-create-a-reference-device"></a><span data-ttu-id="efbb0-103">Comment : créer un appareil de référence</span><span class="sxs-lookup"><span data-stu-id="efbb0-103">How To: Create a Reference Device</span></span>

<span data-ttu-id="efbb0-104">Cette rubrique montre comment créer un appareil de référence qui implémente une implémentation logicielle très précise du Runtime.</span><span class="sxs-lookup"><span data-stu-id="efbb0-104">This topic shows how to create a reference device that implements a highly accurate, software implementation of the runtime.</span></span> <span data-ttu-id="efbb0-105">Pour créer un appareil de référence, spécifiez simplement que l’appareil que vous créez utilisera un pilote de référence.</span><span class="sxs-lookup"><span data-stu-id="efbb0-105">To create a reference device, simply specify that the device you are creating will use a reference driver.</span></span> <span data-ttu-id="efbb0-106">Cet exemple crée un appareil et une chaîne de permutation en même temps.</span><span class="sxs-lookup"><span data-stu-id="efbb0-106">This example creates a device and a swap chain at the same time.</span></span>

<span data-ttu-id="efbb0-107">**Pour créer un appareil de référence**</span><span class="sxs-lookup"><span data-stu-id="efbb0-107">**To create a reference device**</span></span>

1.  <span data-ttu-id="efbb0-108">Définissez les paramètres initiaux d’une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="efbb0-108">Define initial parameters for a swap chain.</span></span>
    ```
        DXGI_SWAP_CHAIN_DESC sd;
        ZeroMemory( &sd, sizeof( sd ) );
        sd.BufferCount = 1;
        sd.BufferDesc.Width = 640;
        sd.BufferDesc.Height = 480;
        sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
        sd.BufferDesc.RefreshRate.Numerator = 60;
        sd.BufferDesc.RefreshRate.Denominator = 1;
        sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        sd.OutputWindow = g_hWnd;
        sd.SampleDesc.Count = 1;
        sd.SampleDesc.Quality = 0;
        sd.Windowed = TRUE;
    ```

    

2.  <span data-ttu-id="efbb0-109">Demandez un niveau de fonctionnalité qui implémente les fonctionnalités dont votre application a besoin.</span><span class="sxs-lookup"><span data-stu-id="efbb0-109">Request a feature level that implements the features your application will need.</span></span> <span data-ttu-id="efbb0-110">Un appareil de référence peut être créé avec succès pour le runtime Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="efbb0-110">A reference device can be successfully created for the Direct3D 11 runtime.</span></span>

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_11_0;
    ```

    

    <span data-ttu-id="efbb0-111">En savoir plus sur les niveaux de fonctionnalités dans l’énumération de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="efbb0-111">See more about feature levels in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span>

3.  <span data-ttu-id="efbb0-112">Créez l’appareil en appelant [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="efbb0-112">Create the device by calling [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>


```
    HRESULT hr = S_OK;
    D3D_FEATURE_LEVEL FeatureLevel;

    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_REFERENCE,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



<span data-ttu-id="efbb0-113">Vous devrez fournir l’appel d’API avec le type de pilote de référence à partir de l’énumération de [**\_ \_ type de pilote D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="efbb0-113">You will need to supply the API call with the reference driver type from the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) enumeration.</span></span> <span data-ttu-id="efbb0-114">Une fois la méthode réussie, elle retourne une interface de chaîne d’échange, une interface de périphérique, un pointeur vers le niveau de fonctionnalité accordé par le pilote et une interface de contexte immédiate.</span><span class="sxs-lookup"><span data-stu-id="efbb0-114">After the method succeeds, it will return a swap chain interface, a device interface, a pointer to the feature level that was granted by the driver, and an immediate context interface.</span></span>

<span data-ttu-id="efbb0-115">Pour plus d’informations sur les limitations de la création d’un appareil de référence sur certains niveaux de fonctionnalité, consultez [limitations création de périphériques de déformation et de référence](overviews-direct3d-11-devices-limitations.md). [Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)</span><span class="sxs-lookup"><span data-stu-id="efbb0-115">For information about limitations creating a reference device on certain feature levels, see [Limitations Creating WARP and Reference Devices](overviews-direct3d-11-devices-limitations.md).[How to Use Direct3D 11](how-to-use-direct3d-11.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="efbb0-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="efbb0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efbb0-117">Appareils</span><span class="sxs-lookup"><span data-stu-id="efbb0-117">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="efbb0-118">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="efbb0-118">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




