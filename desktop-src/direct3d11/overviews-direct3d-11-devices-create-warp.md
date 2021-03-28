---
title: Comment créer un appareil WARP
description: Cette rubrique montre comment créer un appareil de distorsion qui implémente un rastériseur logiciel à grande vitesse.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990965"
---
# <a name="how-to-create-a-warp-device"></a><span data-ttu-id="5ad14-103">Comment : créer un appareil WARP</span><span class="sxs-lookup"><span data-stu-id="5ad14-103">How To: Create a WARP Device</span></span>

<span data-ttu-id="5ad14-104">Cette rubrique montre comment créer un appareil de distorsion qui implémente un rastériseur logiciel à grande vitesse.</span><span class="sxs-lookup"><span data-stu-id="5ad14-104">This topic shows how to create a WARP device that implements a high speed software rasterizer.</span></span> <span data-ttu-id="5ad14-105">Pour créer un périphérique WARP, spécifiez simplement que l’appareil que vous créez utilisera un pilote WARP.</span><span class="sxs-lookup"><span data-stu-id="5ad14-105">To create a WARP device, simply specify that the device you are creating will use a WARP driver.</span></span> <span data-ttu-id="5ad14-106">Cet exemple crée un appareil et une chaîne de permutation en même temps.</span><span class="sxs-lookup"><span data-stu-id="5ad14-106">This example creates a device and a swap chain at the same time.</span></span>

<span data-ttu-id="5ad14-107">**Pour créer un appareil WARP**</span><span class="sxs-lookup"><span data-stu-id="5ad14-107">**To create a WARP device**</span></span>

1.  <span data-ttu-id="5ad14-108">Définissez les paramètres initiaux d’une chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="5ad14-108">Define initial parameters for a swap chain.</span></span>
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

    

2.  <span data-ttu-id="5ad14-109">Demandez un niveau de fonctionnalité qui implémente les fonctionnalités dont votre application a besoin.</span><span class="sxs-lookup"><span data-stu-id="5ad14-109">Request a feature level that implements the features your application will need.</span></span> <span data-ttu-id="5ad14-110">Un appareil de distorsion peut être créé pour les niveaux de fonctionnalités de la **fonctionnalité D3D de \_ \_ niveau \_ 9 \_ 1** à la **\_ fonctionnalité D3D \_ \_ 10 \_ 1** et à partir de Windows 8 pour tous les niveaux de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="5ad14-110">A WARP device can be successfully created for feature levels **D3D\_FEATURE\_LEVEL\_9\_1** through **D3D\_FEATURE\_LEVEL\_10\_1** and starting with Windows 8 for all feature levels.</span></span>

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    <span data-ttu-id="5ad14-111">En savoir plus sur les niveaux de fonctionnalités dans l’énumération de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="5ad14-111">See more about feature levels in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span>

3.  <span data-ttu-id="5ad14-112">Créez l’appareil en appelant [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="5ad14-112">Create the device by calling [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
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



<span data-ttu-id="5ad14-113">Vous devrez fournir l’appel d’API avec le type de pilote WARP à partir de l’énumération de [**\_ \_ type de pilote D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="5ad14-113">You will need to supply the API call with the WARP driver type from the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) enumeration.</span></span> <span data-ttu-id="5ad14-114">Une fois la méthode réussie, elle retourne une interface de chaîne d’échange, une interface de périphérique, un pointeur vers le niveau de fonctionnalité accordé par le pilote et une interface de contexte immédiate.</span><span class="sxs-lookup"><span data-stu-id="5ad14-114">After the method succeeds, it will return a swap chain interface, a device interface, a pointer to the feature level that was granted by the driver, and an immediate context interface.</span></span>

<span data-ttu-id="5ad14-115">Pour plus d’informations sur les limitations de la création d’un périphérique WARP sur certains niveaux de fonctionnalité, consultez [limitations création de périphériques de déformation et de référence](overviews-direct3d-11-devices-limitations.md).</span><span class="sxs-lookup"><span data-stu-id="5ad14-115">For information about limitations creating a WARP device on certain feature levels, see [Limitations Creating WARP and Reference Devices](overviews-direct3d-11-devices-limitations.md).</span></span>

## <a name="new-for-windows-8"></a><span data-ttu-id="5ad14-116">Nouveauté de Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ad14-116">New for Windows 8</span></span>

<span data-ttu-id="5ad14-117">Quand la carte d’affichage principale d’un ordinateur est la « carte d’affichage de base Microsoft » (adaptateur de déviation), cet ordinateur possède également un deuxième adaptateur.</span><span class="sxs-lookup"><span data-stu-id="5ad14-117">When a computer's primary display adapter is the "Microsoft Basic Display Adapter" (WARP adapter), that computer also has a second adapter.</span></span> <span data-ttu-id="5ad14-118">Ce deuxième adaptateur est le périphérique de rendu uniquement qui n’a pas de sortie d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5ad14-118">This second adapter is the render-only device that has no display outputs.</span></span> <span data-ttu-id="5ad14-119">Pour plus d’informations sur l’appareil de rendu uniquement, consultez [nouvelles informations dans Windows 8 sur l’énumération des adaptateurs](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span><span class="sxs-lookup"><span data-stu-id="5ad14-119">For more info about the render-only device, see [new info in Windows 8 about enumerating adapters](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ad14-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ad14-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ad14-121">Appareils</span><span class="sxs-lookup"><span data-stu-id="5ad14-121">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="5ad14-122">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5ad14-122">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 