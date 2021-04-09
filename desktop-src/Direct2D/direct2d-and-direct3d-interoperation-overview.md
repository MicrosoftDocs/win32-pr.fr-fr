---
title: Vue d’ensemble de l’interopérabilité entre Direct2D et Direct3D
description: .
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
ms.openlocfilehash: 6854481ec2a8d869467aa912252e3649e17f2501
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2020
ms.locfileid: "104102512"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a>Vue d’ensemble de l’interopérabilité entre Direct2D et Direct3D

Les graphiques en 2D et 3D accélérés par le matériel deviennent de plus en plus un élément des applications sans jeu, et la plupart des applications de jeu utilisent des graphiques 2D sous la forme de menus et d’affichages de Heads-Up (HUDs). Un grand nombre de valeurs peuvent être ajoutées en permettant le mélange du rendu 2D traditionnel avec le rendu Direct3D de manière efficace.

Cette rubrique décrit comment intégrer des graphiques 2D et 3D à l’aide de Direct2D et [Direct3D](../graphics-and-multimedia.md).

Elle contient les sections suivantes.

-   [Conditions préalables](#prerequisites)
-   [Versions Direct3D prises en charge](#supported-direct3d-versions)
-   [Interopérabilité via DXGI](#interoperability-through-dxgi)
-   [Écriture sur une surface Direct3D avec une cible de rendu de surface DXGI](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [Création d’une surface DXGI](#creating-a-dxgi-surface)
-   [Écriture du contenu Direct2D dans une mémoire tampon de chaîne d’échange](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [Exemple : dessiner un arrière-plan 2D](#example-draw-a-2-d-background)
-   [Utilisation du contenu Direct2D comme texture](#using-direct2d-content-as-a-texture)
    -   [Exemple : utiliser le contenu Direct2D comme une texture](#example-use-direct2d-content-as-a-texture)
-   [Redimensionnement d’une cible de rendu de surface DXGI](#resizing-a-dxgi-surface-render-target)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Cette vue d’ensemble suppose que vous êtes familiarisé avec les opérations de dessin Direct2D de base. Pour obtenir un didacticiel, consultez le Guide de [démarrage rapide de Direct2D](direct2d-quickstart.md). Elle suppose également que vous pouvez programmer à l’aide de [Direct3D 10,1](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="supported-direct3d-versions"></a>Versions Direct3D prises en charge

Avec DirectX 11,0, Direct2D prend en charge l’interopérabilité avec les périphériques Direct3D 10,1 uniquement. Avec DirectX 11,1 ou version ultérieure, Direct2D prend également en charge l’interopérabilité avec Direct3D 11.

## <a name="interoperability-through-dxgi"></a>Interopérabilité via DXGI

À partir de Direct3D 10, le runtime Direct3D utilise [dxgi](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) pour la gestion des ressources. La couche d’exécution DXGI fournit le partage interprocessus des surfaces de la mémoire vidéo et sert de base pour d’autres plateformes d’exécution basées sur la mémoire vidéo. Direct2D utilise DXGI pour interagir avec Direct3D.

Il existe deux façons principales d’utiliser Direct2D et Direct3D ensemble :

-   Vous pouvez écrire du contenu Direct2D dans une surface Direct3D en obtenant un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) et en l’utilisant avec [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) pour créer un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). Vous pouvez ensuite utiliser la cible de rendu pour ajouter une interface à deux dimensions ou un arrière-plan à des graphiques à trois dimensions, ou utiliser un dessin Direct2D comme texture pour un objet en trois dimensions.
-   En utilisant [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) pour créer un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) à partir d’un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), vous pouvez écrire une scène Direct3D dans une image bitmap et la restituer avec Direct2D.

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a>Écriture sur une surface Direct3D avec une cible de rendu de surface DXGI

Pour écrire dans une surface Direct3D, vous obtenez un [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) et le transmettez à la méthode [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) pour créer une cible de rendu de surface DXGI. Vous pouvez ensuite utiliser la cible de rendu de la surface DXGI pour dessiner le contenu 2D sur la surface DXGI.

Une cible de rendu de surface DXGI est un type de [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). Comme les autres cibles de rendu Direct2D, vous pouvez l’utiliser pour créer des ressources et émettre des commandes de dessin.

La cible de rendu de la surface DXGI et la surface DXGI doivent utiliser le même format DXGI. Si vous spécifiez le format [**\_ \_ inconnu au format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) quand vous créez la cible de rendu, elle utilise automatiquement le format de la surface.

La cible de rendu de la surface DXGI n’effectue pas de synchronisation de surface DXGI.

### <a name="creating-a-dxgi-surface"></a>Création d’une surface DXGI

Avec Direct3D 10, il existe plusieurs façons d’obtenir une surface DXGI. Vous pouvez créer un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) pour un appareil, puis utiliser la méthode [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de la chaîne de permutation pour obtenir une surface DXGI. Vous pouvez aussi utiliser un appareil pour créer une texture, puis utiliser cette texture comme surface DXGI.

Quelle que soit la façon dont vous créez la surface DXGI, la surface doit utiliser l’un des formats DXGI pris en charge par les cibles de rendu de surface DXGI. Pour obtenir la liste, consultez [formats de pixel pris en charge et modes alpha](supported-pixel-formats-and-alpha-modes.md).

En outre, le [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associé à la surface DXGI doit prendre en charge les formats dxgi BGRA pour que la surface fonctionne avec Direct2D. Pour garantir cette prise en charge, utilisez l’indicateur de [**\_ \_ \_ \_ prise en charge D3D10 créer un appareil BGRA**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) lorsque vous appelez la méthode [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) pour créer l’appareil.

Le code suivant définit une méthode qui crée un [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1). Il sélectionne le meilleur niveau de fonctionnalité disponible et revient à la [plateforme de rastérisation avancée Windows (Warp)](./installing-the-direct2d-debug-layer.md) lorsque le rendu matériel n’est pas disponible.


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



L’exemple de code suivant utilise la `CreateD3DDevice` méthode illustrée dans l’exemple précédent pour créer un appareil Direct3D qui peut créer des surfaces dxgi à utiliser avec Direct2D.


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



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a>Écriture du contenu Direct2D dans une mémoire tampon de chaîne d’échange

La façon la plus simple d’ajouter du contenu Direct2D à une scène Direct3D consiste à utiliser la méthode [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) d’un [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) pour obtenir une surface DXGI, puis à utiliser la surface avec la méthode [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) pour créer un [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) avec lequel dessiner votre contenu 2D.

Cette approche ne rend pas votre contenu dans trois dimensions ; elle n’aura pas de perspective ou de profondeur. Toutefois, il est utile pour plusieurs tâches courantes :

-   Création d’un arrière-plan 2D pour une scène 3D.
-   Création d’une interface 2D devant une scène 3D.
-   Utilisation de l’échantillonnage multiple Direct3D lors du rendu du contenu Direct2D.

La section suivante montre comment créer un arrière-plan 2D pour une scène 3D.

### <a name="example-draw-a-2-d-background"></a>Exemple : dessiner un arrière-plan 2D

Les étapes suivantes décrivent comment créer une cible de rendu de surface DXGI et l’utiliser pour dessiner un arrière-plan dégradé.

1.  Utilisez la méthode [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) pour créer une chaîne de permutation pour un [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (la variable *m \_ pDevice* ). La chaîne de permutation utilise le format [**dxgi \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) dxgi, l’un des formats dxgi pris en charge par Direct2D.

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

    

2.  Utilisez la méthode [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) de la chaîne de permutation pour obtenir une surface DXGI.

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  Utilisez la surface DXGI pour créer une cible de rendu DXGI.
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



    

4.  Utilisez la cible de rendu pour dessiner un arrière-plan dégradé.

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



    

Le code est omis de cet exemple.

## <a name="using-direct2d-content-as-a-texture"></a>Utilisation du contenu Direct2D comme texture

Une autre façon d’utiliser le contenu Direct2D avec Direct3D consiste à utiliser Direct2D pour générer une texture 2D, puis à appliquer cette texture à un modèle 3D. Pour ce faire, vous devez créer un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtenir une surface DXGI à partir de la texture, puis utiliser la surface pour créer une cible de rendu de surface DXGI. La surface **ID3D10Texture2D** doit utiliser l’indicateur de liaison de la cible de rendu de la [**\_ liaison \_ \_ D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) et utiliser un format dxgi pris en charge par les cibles de rendu de surface DXGI. Pour obtenir la liste des formats DXGI pris en charge, consultez [formats de pixel pris en charge et modes alpha](supported-pixel-formats-and-alpha-modes.md).

### <a name="example-use-direct2d-content-as-a-texture"></a>Exemple : utiliser le contenu Direct2D comme une texture

Les exemples suivants montrent comment créer une cible de rendu de surface DXGI qui effectue un rendu sur une texture 2D (représentée par un [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).

1.  Tout d’abord, utilisez un appareil Direct3D pour créer une texture 2D. La texture utilise les indicateurs de liaison de la [**\_ cible de \_ rendu \_ de liaison D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) et de la **\_ \_ \_ ressource de nuanceur** de liaison D3D10, et utilise le format [**dxgi \_ \_ B8G8R8A8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) UNORM dxgi, l’un des formats dxgi pris en charge par Direct2D.

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

    

2.  Utilisez la texture pour obtenir une surface DXGI.

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  Utilisez la surface avec la méthode [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) pour obtenir une cible de rendu Direct2D.

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



    

Maintenant que vous avez obtenu une cible de rendu Direct2D et que vous l’avez associée à une texture Direct3D, vous pouvez utiliser la cible de rendu pour dessiner du contenu Direct2D sur cette texture, et vous pouvez appliquer cette texture aux primitives Direct3D.

Le code est omis de cet exemple.

## <a name="resizing-a-dxgi-surface-render-target"></a>Redimensionnement d’une cible de rendu de surface DXGI

Les cibles de rendu de surface DXGI ne prennent pas en charge la méthode [**ID2D1RenderTarget :: Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) . Pour redimensionner une cible de rendu de surface DXGI, l’application doit la libérer et la recréer.

Cette opération peut potentiellement créer des problèmes de performances. La cible de rendu peut être la dernière ressource Direct2D active qui conserve une référence au [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associé à la surface DXGI de la cible de rendu. Si l’application libère la cible de rendu et que la référence **ID3D10Device1** est détruite, vous devez recréer une nouvelle.

Vous pouvez éviter cette opération potentiellement coûteuse en conservant au moins une ressource Direct2D créée par la cible de rendu pendant que vous recréez cette cible de rendu. Voici quelques ressources Direct2D qui fonctionnent pour cette approche :

-   [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (qui peut être détenu indirectement par un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

Pour prendre en charge cette approche, votre méthode Resize doit tester pour déterminer si le périphérique Direct3D est disponible. S’il est disponible, libérez et recréez vos cibles de rendu de surface DXGI, mais conservez toutes les ressources qu’ils ont créées précédemment et réutilisez-les. Cela fonctionne parce que, comme décrit dans la [vue d’ensemble des ressources](resources-and-resource-domains.md), les ressources créées par deux cibles de rendu sont compatibles lorsque les deux cibles de rendu sont associées au même appareil Direct3D.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Formats de pixel et modes alpha pris en charge](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))
</dt> <dt>

[Graphiques Windows DirectX](../graphics-and-multimedia.md)
</dt> </dl>

 

 