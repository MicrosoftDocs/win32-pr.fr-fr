---
title: Vue d’ensemble de l’interopérabilité entre Direct2D et Direct3D
description: Vue d’ensemble de l’interopérabilité entre Direct2D et Direct3D
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Direct2D, interopérabilité Direct3D
- Direct2D, interopérabilité
- interopérabilité, Direct2D
- interopérabilité, Direct3D
- Direct3D, interopérabilité
- Direct3D, interopérabilité de Direct2D
- Direct2D, DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cf7cfa41c3decc964492258dad9c6a3a497f504b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089187"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a><span data-ttu-id="24eae-111">Vue d’ensemble de l’interopérabilité entre Direct2D et Direct3D</span><span class="sxs-lookup"><span data-stu-id="24eae-111">Direct2D and Direct3D Interoperability Overview</span></span>

<span data-ttu-id="24eae-112">Les graphiques en 2D et 3D accélérés par le matériel deviennent de plus en plus un élément des applications sans jeu, et la plupart des applications de jeu utilisent des graphiques 2D sous la forme de menus et d’affichages de Heads-Up (HUDs).</span><span class="sxs-lookup"><span data-stu-id="24eae-112">Hardware accelerated 2-D and 3-D graphics are increasingly becoming a part of non-gaming applications, and most gaming applications use 2-D graphics in the form of menus and Heads-Up Displays (HUDs).</span></span> <span data-ttu-id="24eae-113">Un grand nombre de valeurs peuvent être ajoutées en permettant le mélange du rendu 2D traditionnel avec le rendu Direct3D de manière efficace.</span><span class="sxs-lookup"><span data-stu-id="24eae-113">There is lots of value that can be added by enabling traditional 2-D rendering to be mixed with Direct3D rendering in an efficient manner.</span></span>

<span data-ttu-id="24eae-114">Cette rubrique décrit comment intégrer des graphiques 2D et 3D à l’aide de Direct2D et [Direct3D](../graphics-and-multimedia.md).</span><span class="sxs-lookup"><span data-stu-id="24eae-114">This topic describes how to integrate 2-D and 3-D graphics by using Direct2D and [Direct3D](../graphics-and-multimedia.md).</span></span>

<span data-ttu-id="24eae-115">Elle contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="24eae-115">It contains the following sections.</span></span>

-   [<span data-ttu-id="24eae-116">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="24eae-116">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="24eae-117">Versions Direct3D prises en charge</span><span class="sxs-lookup"><span data-stu-id="24eae-117">Supported Direct3D Versions</span></span>](#supported-direct3d-versions)
-   [<span data-ttu-id="24eae-118">Interopérabilité via DXGI</span><span class="sxs-lookup"><span data-stu-id="24eae-118">Interoperability Through DXGI</span></span>](#interoperability-through-dxgi)
-   [<span data-ttu-id="24eae-119">Écriture sur une surface Direct3D avec une cible de rendu de surface DXGI</span><span class="sxs-lookup"><span data-stu-id="24eae-119">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [<span data-ttu-id="24eae-120">Création d’une surface DXGI</span><span class="sxs-lookup"><span data-stu-id="24eae-120">Creating a DXGI Surface</span></span>](#creating-a-dxgi-surface)
-   [<span data-ttu-id="24eae-121">Écriture du contenu Direct2D dans une mémoire tampon de chaîne d’échange</span><span class="sxs-lookup"><span data-stu-id="24eae-121">Writing Direct2D Content to a Swap Chain Buffer</span></span>](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [<span data-ttu-id="24eae-122">Exemple : dessiner un arrière-plan 2D</span><span class="sxs-lookup"><span data-stu-id="24eae-122">Example: Draw a 2-D Background</span></span>](#example-draw-a-2-d-background)
-   [<span data-ttu-id="24eae-123">Utilisation du contenu Direct2D comme texture</span><span class="sxs-lookup"><span data-stu-id="24eae-123">Using Direct2D Content as a Texture</span></span>](#using-direct2d-content-as-a-texture)
    -   [<span data-ttu-id="24eae-124">Exemple : utiliser le contenu Direct2D comme une texture</span><span class="sxs-lookup"><span data-stu-id="24eae-124">Example: Use Direct2D Content as a Texture</span></span>](#example-use-direct2d-content-as-a-texture)
-   [<span data-ttu-id="24eae-125">Redimensionnement d’une cible de rendu de surface DXGI</span><span class="sxs-lookup"><span data-stu-id="24eae-125">Resizing a DXGI Surface Render Target</span></span>](#resizing-a-dxgi-surface-render-target)
-   [<span data-ttu-id="24eae-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24eae-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="24eae-127">Prérequis</span><span class="sxs-lookup"><span data-stu-id="24eae-127">Prerequisites</span></span>

<span data-ttu-id="24eae-128">Cette vue d’ensemble suppose que vous êtes familiarisé avec les opérations de dessin Direct2D de base.</span><span class="sxs-lookup"><span data-stu-id="24eae-128">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="24eae-129">Pour obtenir un didacticiel, consultez le Guide de [démarrage rapide de Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="24eae-129">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="24eae-130">Elle suppose également que vous pouvez programmer à l’aide de [Direct3D 10,1](/windows/desktop/direct3d10/d3d10-graphics).</span><span class="sxs-lookup"><span data-stu-id="24eae-130">It also assumes that you can program by using [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

## <a name="supported-direct3d-versions"></a><span data-ttu-id="24eae-131">Versions Direct3D prises en charge</span><span class="sxs-lookup"><span data-stu-id="24eae-131">Supported Direct3D Versions</span></span>

<span data-ttu-id="24eae-132">Avec DirectX 11,0, Direct2D prend en charge l’interopérabilité avec les périphériques Direct3D 10,1 uniquement.</span><span class="sxs-lookup"><span data-stu-id="24eae-132">With DirectX 11.0, Direct2D supports interoperability with Direct3D 10.1 devices only.</span></span> <span data-ttu-id="24eae-133">Avec DirectX 11,1 ou version ultérieure, Direct2D prend également en charge l’interopérabilité avec Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="24eae-133">With DirectX 11.1 or later, Direct2D supports interoperability with Direct3D 11 as well.</span></span>

## <a name="interoperability-through-dxgi"></a><span data-ttu-id="24eae-134">Interopérabilité via DXGI</span><span class="sxs-lookup"><span data-stu-id="24eae-134">Interoperability Through DXGI</span></span>

<span data-ttu-id="24eae-135">À partir de Direct3D 10, le runtime Direct3D utilise [dxgi](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) pour la gestion des ressources.</span><span class="sxs-lookup"><span data-stu-id="24eae-135">As of Direct3D 10, the Direct3D runtime uses [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) for resource management.</span></span> <span data-ttu-id="24eae-136">La couche d’exécution DXGI fournit le partage interprocessus des surfaces de la mémoire vidéo et sert de base pour d’autres plateformes d’exécution basées sur la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="24eae-136">The DXGI runtime layer provides cross-process sharing of video memory surfaces and serves as the foundation for other video memory-based runtime platforms.</span></span> <span data-ttu-id="24eae-137">Direct2D utilise DXGI pour interagir avec Direct3D.</span><span class="sxs-lookup"><span data-stu-id="24eae-137">Direct2D uses DXGI to interoperate with Direct3D.</span></span>

<span data-ttu-id="24eae-138">Il existe deux façons principales d’utiliser Direct2D et Direct3D ensemble :</span><span class="sxs-lookup"><span data-stu-id="24eae-138">There are two primary ways to use Direct2D and Direct3D together:</span></span>

-   <span data-ttu-id="24eae-139">Vous pouvez écrire du contenu Direct2D dans une surface Direct3D en obtenant un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) et en l’utilisant avec [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) pour créer un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span><span class="sxs-lookup"><span data-stu-id="24eae-139">You can write Direct2D content to a Direct3D surface by obtaining an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and using it with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="24eae-140">Vous pouvez ensuite utiliser la cible de rendu pour ajouter une interface à deux dimensions ou un arrière-plan à des graphiques à trois dimensions, ou utiliser un dessin Direct2D comme texture pour un objet en trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="24eae-140">You can then use the render target to add a two-dimensional interface or background to three-dimensional graphics, or use a Direct2D drawing as a texture for a three dimensional object.</span></span>
-   <span data-ttu-id="24eae-141">En utilisant [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) pour créer un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) à partir d’un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), vous pouvez écrire une scène Direct3D dans une image bitmap et la restituer avec Direct2D.</span><span class="sxs-lookup"><span data-stu-id="24eae-141">By using [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) from an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), you can write a Direct3D scene to a bitmap and render it with Direct2D.</span></span>

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a><span data-ttu-id="24eae-142">Écriture sur une surface Direct3D avec une cible de rendu de surface DXGI</span><span class="sxs-lookup"><span data-stu-id="24eae-142">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>

<span data-ttu-id="24eae-143">Pour écrire dans une surface Direct3D, vous obtenez un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) et le transmettez à la méthode [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) pour créer une cible de rendu de surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-143">To write to a Direct3D surface, you obtain an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and pass it to the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create a DXGI surface render target.</span></span> <span data-ttu-id="24eae-144">Vous pouvez ensuite utiliser la cible de rendu de la surface DXGI pour dessiner le contenu 2D sur la surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-144">You can then use the DXGI surface render target to draw 2-D content to the DXGI surface.</span></span>

<span data-ttu-id="24eae-145">Une cible de rendu de surface DXGI est un type de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span><span class="sxs-lookup"><span data-stu-id="24eae-145">A DXGI surface render target is a kind of [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="24eae-146">Comme les autres cibles de rendu Direct2D, vous pouvez l’utiliser pour créer des ressources et émettre des commandes de dessin.</span><span class="sxs-lookup"><span data-stu-id="24eae-146">Like other Direct2D render targets, you can use it to create resources and issue drawing commands.</span></span>

<span data-ttu-id="24eae-147">La cible de rendu de la surface DXGI et la surface DXGI doivent utiliser le même format DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-147">The DXGI surface render target and the DXGI surface must use the same DXGI format.</span></span> <span data-ttu-id="24eae-148">Si vous spécifiez le format [**\_ \_ inconnu au format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) quand vous créez la cible de rendu, elle utilise automatiquement le format de la surface.</span><span class="sxs-lookup"><span data-stu-id="24eae-148">If you specify the [**DXGI\_FORMAT\_UNKOWN**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format when you create the render target, it will automatically use the surface's format.</span></span>

<span data-ttu-id="24eae-149">La cible de rendu de la surface DXGI n’effectue pas de synchronisation de surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-149">The DXGI surface render target does not perform DXGI surface synchronization.</span></span>

### <a name="creating-a-dxgi-surface"></a><span data-ttu-id="24eae-150">Création d’une surface DXGI</span><span class="sxs-lookup"><span data-stu-id="24eae-150">Creating a DXGI Surface</span></span>

<span data-ttu-id="24eae-151">Avec Direct3D 10, il existe plusieurs façons d’obtenir une surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-151">With Direct3D 10, there are several ways to obtain a DXGI surface.</span></span> <span data-ttu-id="24eae-152">Vous pouvez créer un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) pour un appareil, puis utiliser la méthode [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de la chaîne de permutation pour obtenir une surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-152">You can create an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) for a device, then use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span> <span data-ttu-id="24eae-153">Vous pouvez aussi utiliser un appareil pour créer une texture, puis utiliser cette texture comme surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-153">Or, you can use a device to create a texture, then use that texture as a DXGI surface.</span></span>

<span data-ttu-id="24eae-154">Quelle que soit la façon dont vous créez la surface DXGI, la surface doit utiliser l’un des formats DXGI pris en charge par les cibles de rendu de surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-154">Regardless of how you create the DXGI surface, the surface must use one of the DXGI formats supported by DXGI surface render targets.</span></span> <span data-ttu-id="24eae-155">Pour obtenir la liste, consultez [formats de pixel pris en charge et modes alpha](supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="24eae-155">For a list, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="24eae-156">En outre, le [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associé à la surface DXGI doit prendre en charge les formats dxgi BGRA pour que la surface fonctionne avec Direct2D.</span><span class="sxs-lookup"><span data-stu-id="24eae-156">Additionally, the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the DXGI surface must support BGRA DXGI formats for the surface to work with Direct2D.</span></span> <span data-ttu-id="24eae-157">Pour garantir cette prise en charge, utilisez l’indicateur de [**\_ \_ \_ \_ prise en charge D3D10 créer un appareil BGRA**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) lorsque vous appelez la méthode [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) pour créer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="24eae-157">To ensure this support, use the [**D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag when you call the [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) method to create the device.</span></span>

<span data-ttu-id="24eae-158">Le code suivant définit une méthode qui crée un [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span><span class="sxs-lookup"><span data-stu-id="24eae-158">The following code defines a method that creates an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span></span> <span data-ttu-id="24eae-159">Il sélectionne le meilleur niveau de fonctionnalité disponible et revient à la [plateforme de rastérisation avancée Windows (Warp)](./installing-the-direct2d-debug-layer.md) lorsque le rendu matériel n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="24eae-159">It selects the best feature level available and falls back to [Windows Advanced Rasterization Platform (WARP)](./installing-the-direct2d-debug-layer.md) when hardware rendering is not available.</span></span>


```C++
HRESULT DXGISampleApp::CreateD3DDevice(
    IDXGIAdapter *pAdapter,
    D3D10_DRIVER_TYPE driverType,
    UINT flags,
    ID3D10Device1 **ppDevice
    )
{
    HRESULT hr = S_OK;

    static const D3D10_FEATURE_LEVEL1 levelAttempts[] =
    {
        D3D10_FEATURE_LEVEL_10_0,
        D3D10_FEATURE_LEVEL_9_3,
        D3D10_FEATURE_LEVEL_9_2,
        D3D10_FEATURE_LEVEL_9_1,
    };

    for (UINT level = 0; level < ARRAYSIZE(levelAttempts); level++)
    {
        ID3D10Device1 *pDevice = NULL;
        hr = D3D10CreateDevice1(
            pAdapter,
            driverType,
            NULL,
            flags,
            levelAttempts[level],
            D3D10_1_SDK_VERSION,
            &pDevice
            );

        if (SUCCEEDED(hr))
        {
            // transfer reference
            *ppDevice = pDevice;
            pDevice = NULL;
            break;
        }

    }

    return hr;
}
```



<span data-ttu-id="24eae-160">L’exemple de code suivant utilise la `CreateD3DDevice` méthode illustrée dans l’exemple précédent pour créer un appareil Direct3D qui peut créer des surfaces dxgi à utiliser avec Direct2D.</span><span class="sxs-lookup"><span data-stu-id="24eae-160">The next code example uses the `CreateD3DDevice` method shown in the previous example to create a Direct3D device that can create DXGI surfaces for use with Direct2D.</span></span>


```C++
// Create device
hr = CreateD3DDevice(
    NULL,
    D3D10_DRIVER_TYPE_HARDWARE,
    nDeviceFlags,
    &pDevice
    );

if (FAILED(hr))
{
    hr = CreateD3DDevice(
        NULL,
        D3D10_DRIVER_TYPE_WARP,
        nDeviceFlags,
        &pDevice
        );
}
```



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a><span data-ttu-id="24eae-161">Écriture du contenu Direct2D dans une mémoire tampon de chaîne d’échange</span><span class="sxs-lookup"><span data-stu-id="24eae-161">Writing Direct2D Content to a Swap Chain Buffer</span></span>

<span data-ttu-id="24eae-162">La façon la plus simple d’ajouter du contenu Direct2D à une scène Direct3D consiste à utiliser la méthode [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) d’un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) pour obtenir une surface DXGI, puis à utiliser la surface avec la méthode [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) pour créer un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) avec lequel dessiner votre contenu 2D.</span><span class="sxs-lookup"><span data-stu-id="24eae-162">The simplest way to add Direct2D content to a Direct3D scene is to use the [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method of an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) to obtain a DXGI surface, then use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) with which to draw your 2-D content.</span></span>

<span data-ttu-id="24eae-163">Cette approche ne rend pas votre contenu dans trois dimensions ; elle n’aura pas de perspective ou de profondeur.</span><span class="sxs-lookup"><span data-stu-id="24eae-163">This approach does not render your content in three dimensions; it will not have perspective or depth.</span></span> <span data-ttu-id="24eae-164">Toutefois, il est utile pour plusieurs tâches courantes :</span><span class="sxs-lookup"><span data-stu-id="24eae-164">However, it is useful for several common tasks:</span></span>

-   <span data-ttu-id="24eae-165">Création d’un arrière-plan 2D pour une scène 3D.</span><span class="sxs-lookup"><span data-stu-id="24eae-165">Creating a 2-D background for a 3-D scene.</span></span>
-   <span data-ttu-id="24eae-166">Création d’une interface 2D devant une scène 3D.</span><span class="sxs-lookup"><span data-stu-id="24eae-166">Creating a 2-D interface in front of a 3-D scene.</span></span>
-   <span data-ttu-id="24eae-167">Utilisation de l’échantillonnage multiple Direct3D lors du rendu du contenu Direct2D.</span><span class="sxs-lookup"><span data-stu-id="24eae-167">Using Direct3D multisampling when rendering Direct2D content.</span></span>

<span data-ttu-id="24eae-168">La section suivante montre comment créer un arrière-plan 2D pour une scène 3D.</span><span class="sxs-lookup"><span data-stu-id="24eae-168">The next section shows how to create a 2-D background for a 3-D scene.</span></span>

### <a name="example-draw-a-2-d-background"></a><span data-ttu-id="24eae-169">Exemple : dessiner un arrière-plan 2D</span><span class="sxs-lookup"><span data-stu-id="24eae-169">Example: Draw a 2-D Background</span></span>

<span data-ttu-id="24eae-170">Les étapes suivantes décrivent comment créer une cible de rendu de surface DXGI et l’utiliser pour dessiner un arrière-plan dégradé.</span><span class="sxs-lookup"><span data-stu-id="24eae-170">The following steps describe how to create a DXGI surface render target and use it to draw a gradient background.</span></span>

1.  <span data-ttu-id="24eae-171">Utilisez la méthode [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) pour créer une chaîne de permutation pour un [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (la variable *m \_ pDevice* ).</span><span class="sxs-lookup"><span data-stu-id="24eae-171">Use the [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) method to create a swap chain for an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (the *m\_pDevice* variable).</span></span> <span data-ttu-id="24eae-172">La chaîne de permutation utilise le format [**dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) dxgi, l’un des formats dxgi pris en charge par Direct2D.</span><span class="sxs-lookup"><span data-stu-id="24eae-172">The swap chain uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

```C++
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&m_pDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&pDXGIDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDXGIDevice->GetAdapter(&pAdapter);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAdapter->GetParent(IID_PPV_ARGS(&pDXGIFactory));
    }
    if (SUCCEEDED(hr))
    {
        DXGI_SWAP_CHAIN_DESC swapDesc;
        ::ZeroMemory(&swapDesc, sizeof(swapDesc));

        swapDesc.BufferDesc.Width = nWidth;
        swapDesc.BufferDesc.Height = nHeight;
        swapDesc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
        swapDesc.BufferDesc.RefreshRate.Numerator = 60;
        swapDesc.BufferDesc.RefreshRate.Denominator = 1;
        swapDesc.SampleDesc.Count = 1;
        swapDesc.SampleDesc.Quality = 0;
        swapDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapDesc.BufferCount = 1;
        swapDesc.OutputWindow = m_hwnd;
        swapDesc.Windowed = TRUE;

        hr = pDXGIFactory->CreateSwapChain(m_pDevice, &swapDesc, &m_pSwapChain);
    }
```

    

2.  <span data-ttu-id="24eae-173">Utilisez la méthode [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de la chaîne de permutation pour obtenir une surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-173">Use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span>

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  <span data-ttu-id="24eae-174">Utilisez la surface DXGI pour créer une cible de rendu DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-174">Use the DXGI surface to create a DXGI render target.</span></span>
```C++
    // Create the DXGI Surface Render Target.
    FLOAT dpiX;
    FLOAT dpiY;
    m_pD2DFactory->GetDesktopDpi(&dpiX, &dpiY);

    D2D1_RENDER_TARGET_PROPERTIES props =
        D2D1::RenderTargetProperties(
            D2D1_RENDER_TARGET_TYPE_DEFAULT,
            D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
            dpiX,
            dpiY
            );

    // Create a Direct2D render target which can draw into the surface in the swap chain

    
hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pBackBuffer,
        &props,
        &m_pBackBufferRT
        );
    
```



    

4.  <span data-ttu-id="24eae-175">Utilisez la cible de rendu pour dessiner un arrière-plan dégradé.</span><span class="sxs-lookup"><span data-stu-id="24eae-175">Use the render target to draw a gradient background.</span></span>

```C++
    // Swap chain will tell us how big the back buffer is
    DXGI_SWAP_CHAIN_DESC swapDesc;
    hr = m_pSwapChain->GetDesc(&swapDesc);

    if (SUCCEEDED(hr))
    {

    
// Draw a gradient background.
    if (m_pBackBufferRT)
    {
        D2D1_SIZE_F targetSize = m_pBackBufferRT->GetSize();

        m_pBackBufferRT->BeginDraw();

        m_pBackBufferGradientBrush->SetTransform(
            D2D1::Matrix3x2F::Scale(targetSize)
            );

        D2D1_RECT_F rect = D2D1::RectF(
            0.0f,
            0.0f,
            targetSize.width,
            targetSize.height
            );

        m_pBackBufferRT->FillRectangle(&rect, m_pBackBufferGradientBrush);

        hr = m_pBackBufferRT->EndDraw();
    }
```



    

<span data-ttu-id="24eae-176">Le code est omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="24eae-176">Code is omitted from this sample.</span></span>

## <a name="using-direct2d-content-as-a-texture"></a><span data-ttu-id="24eae-177">Utilisation du contenu Direct2D comme texture</span><span class="sxs-lookup"><span data-stu-id="24eae-177">Using Direct2D Content as a Texture</span></span>

<span data-ttu-id="24eae-178">Une autre façon d’utiliser le contenu Direct2D avec Direct3D consiste à utiliser Direct2D pour générer une texture 2D, puis à appliquer cette texture à un modèle 3D.</span><span class="sxs-lookup"><span data-stu-id="24eae-178">Another way to use Direct2D content with Direct3D is to use Direct2D to generate a 2-D texture and then apply that texture to a 3-D model.</span></span> <span data-ttu-id="24eae-179">Pour ce faire, vous devez créer un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtenir une surface DXGI à partir de la texture, puis utiliser la surface pour créer une cible de rendu de surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-179">You do this by creating an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtaining a DXGI surface from the texture, and then using the surface to create a DXGI surface render target.</span></span> <span data-ttu-id="24eae-180">La surface **ID3D10Texture2D** doit utiliser l’indicateur de liaison de la cible de rendu de la [**\_ liaison \_ \_ D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) et utiliser un format dxgi pris en charge par les cibles de rendu de surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-180">The **ID3D10Texture2D** surface must use the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) bind flag and use a DXGI format supported by DXGI surface render targets.</span></span> <span data-ttu-id="24eae-181">Pour obtenir la liste des formats DXGI pris en charge, consultez [formats de pixel pris en charge et modes alpha](supported-pixel-formats-and-alpha-modes.md).</span><span class="sxs-lookup"><span data-stu-id="24eae-181">For a list of supported DXGI formats, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

### <a name="example-use-direct2d-content-as-a-texture"></a><span data-ttu-id="24eae-182">Exemple : utiliser le contenu Direct2D comme une texture</span><span class="sxs-lookup"><span data-stu-id="24eae-182">Example: Use Direct2D Content as a Texture</span></span>

<span data-ttu-id="24eae-183">Les exemples suivants montrent comment créer une cible de rendu de surface DXGI qui effectue un rendu sur une texture 2D (représentée par un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span><span class="sxs-lookup"><span data-stu-id="24eae-183">The following examples show how to create a DXGI surface render target that renders to a 2-D texture (represented by an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span></span>

1.  <span data-ttu-id="24eae-184">Tout d’abord, utilisez un appareil Direct3D pour créer une texture 2D.</span><span class="sxs-lookup"><span data-stu-id="24eae-184">First, use a Direct3D device to create a 2-D texture.</span></span> <span data-ttu-id="24eae-185">La texture utilise les indicateurs de liaison de la [**\_ cible de \_ rendu \_ de liaison D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) et de la **\_ \_ \_ ressource de nuanceur** de liaison D3D10, et utilise le format [**dxgi \_ \_ B8G8R8A8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) UNORM dxgi, l’un des formats dxgi pris en charge par Direct2D.</span><span class="sxs-lookup"><span data-stu-id="24eae-185">The texture uses the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) and **D3D10\_BIND\_SHADER\_RESOURCE** bind flags, and it uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

```C++
    // Allocate a offscreen D3D surface for D2D to render our 2D content into
    D3D10_TEXTURE2D_DESC texDesc;
    texDesc.ArraySize = 1;
    texDesc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
    texDesc.CPUAccessFlags = 0;
    texDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
    texDesc.Height = 512;
    texDesc.Width = 512;
    texDesc.MipLevels = 1;
    texDesc.MiscFlags = 0;
    texDesc.SampleDesc.Count = 1;
    texDesc.SampleDesc.Quality = 0;
    texDesc.Usage = D3D10_USAGE_DEFAULT;

    hr = m_pDevice->CreateTexture2D(&texDesc, NULL, &m_pOffscreenTexture);
```

    

2.  <span data-ttu-id="24eae-186">Utilisez la texture pour obtenir une surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="24eae-186">Use the texture to obtain a DXGI surface.</span></span>

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  <span data-ttu-id="24eae-187">Utilisez la surface avec la méthode [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) pour obtenir une cible de rendu Direct2D.</span><span class="sxs-lookup"><span data-stu-id="24eae-187">Use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to obtain a Direct2D render target.</span></span>

```C++
    if (SUCCEEDED(hr))
    {
        // Create a D2D render target which can draw into our offscreen D3D
        // surface. Given that we use a constant size for the texture, we
        // fix the DPI at 96.
        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_DEFAULT,
                D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
                96,
                96
                );

    
    hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
            pDxgiSurface,
            &props,
            &m_pRenderTarget
            );
    }
```



    

<span data-ttu-id="24eae-188">Maintenant que vous avez obtenu une cible de rendu Direct2D et que vous l’avez associée à une texture Direct3D, vous pouvez utiliser la cible de rendu pour dessiner du contenu Direct2D sur cette texture, et vous pouvez appliquer cette texture aux primitives Direct3D.</span><span class="sxs-lookup"><span data-stu-id="24eae-188">Now that you have obtained a Direct2D render target and associated it with a Direct3D texture, you can use the render target to draw Direct2D content to that texture, and you can apply that texture to Direct3D primitives.</span></span>

<span data-ttu-id="24eae-189">Le code est omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="24eae-189">Code is omitted from this sample.</span></span>

## <a name="resizing-a-dxgi-surface-render-target"></a><span data-ttu-id="24eae-190">Redimensionnement d’une cible de rendu de surface DXGI</span><span class="sxs-lookup"><span data-stu-id="24eae-190">Resizing a DXGI Surface Render Target</span></span>

<span data-ttu-id="24eae-191">Les cibles de rendu de surface DXGI ne prennent pas en charge la méthode [**ID2D1RenderTarget :: Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) .</span><span class="sxs-lookup"><span data-stu-id="24eae-191">DXGI surface render targets do not support the [**ID2D1RenderTarget::Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) method.</span></span> <span data-ttu-id="24eae-192">Pour redimensionner une cible de rendu de surface DXGI, l’application doit la libérer et la recréer.</span><span class="sxs-lookup"><span data-stu-id="24eae-192">To resize a DXGI surface render target, the application must release and re-create it.</span></span>

<span data-ttu-id="24eae-193">Cette opération peut potentiellement créer des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="24eae-193">This operation can potentially create performance issues.</span></span> <span data-ttu-id="24eae-194">La cible de rendu peut être la dernière ressource Direct2D active qui conserve une référence au [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associé à la surface DXGI de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="24eae-194">The render target might be the last active Direct2D resource that keeps a reference to the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the render target's DXGI surface.</span></span> <span data-ttu-id="24eae-195">Si l’application libère la cible de rendu et que la référence **ID3D10Device1** est détruite, vous devez recréer une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="24eae-195">If the application releases the render target and the **ID3D10Device1** reference is destroyed, a new one must be recreated.</span></span>

<span data-ttu-id="24eae-196">Vous pouvez éviter cette opération potentiellement coûteuse en conservant au moins une ressource Direct2D créée par la cible de rendu pendant que vous recréez cette cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="24eae-196">You can avoid this potentially expensive operation by keeping at least one Direct2D resource that was created by the render target while you re-create that render target.</span></span> <span data-ttu-id="24eae-197">Voici quelques ressources Direct2D qui fonctionnent pour cette approche :</span><span class="sxs-lookup"><span data-stu-id="24eae-197">The following are some Direct2D resources that work for this approach:</span></span>

-   <span data-ttu-id="24eae-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (qui peut être détenu indirectement par un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))</span><span class="sxs-lookup"><span data-stu-id="24eae-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (which may be held indirectly by an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))</span></span>
-   [<span data-ttu-id="24eae-199">**ID2D1Layer**</span><span class="sxs-lookup"><span data-stu-id="24eae-199">**ID2D1Layer**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [<span data-ttu-id="24eae-200">**ID2D1Mesh**</span><span class="sxs-lookup"><span data-stu-id="24eae-200">**ID2D1Mesh**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

<span data-ttu-id="24eae-201">Pour prendre en charge cette approche, votre méthode Resize doit tester pour déterminer si le périphérique Direct3D est disponible.</span><span class="sxs-lookup"><span data-stu-id="24eae-201">To accommodate this approach, your resize method should test to see whether the Direct3D device is available.</span></span> <span data-ttu-id="24eae-202">S’il est disponible, libérez et recréez vos cibles de rendu de surface DXGI, mais conservez toutes les ressources qu’ils ont créées précédemment et réutilisez-les.</span><span class="sxs-lookup"><span data-stu-id="24eae-202">If it is available, release and re-create your DXGI surface render targets, but keep all the resources that they created previously and reuse them.</span></span> <span data-ttu-id="24eae-203">Cela fonctionne parce que, comme décrit dans la [vue d’ensemble des ressources](resources-and-resource-domains.md), les ressources créées par deux cibles de rendu sont compatibles lorsque les deux cibles de rendu sont associées au même appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="24eae-203">This works because, as described in the [Resources Overview](resources-and-resource-domains.md), resources created by two render targets are compatible when both render targets are associated with the same Direct3D device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24eae-204">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24eae-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24eae-205">Formats de pixel et modes alpha pris en charge</span><span class="sxs-lookup"><span data-stu-id="24eae-205">Supported Pixel Formats and Alpha Modes</span></span>](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

<span data-ttu-id="24eae-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="24eae-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span></span>
</dt> <dt>

[<span data-ttu-id="24eae-207">Graphiques Windows DirectX</span><span class="sxs-lookup"><span data-stu-id="24eae-207">Windows DirectX Graphics</span></span>](../graphics-and-multimedia.md)
</dt> </dl>

 

 
