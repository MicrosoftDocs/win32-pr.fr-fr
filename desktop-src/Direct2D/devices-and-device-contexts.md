---
title: Comment effectuer le rendu à l’aide d’un contexte de périphérique Direct2D
description: Dans cette rubrique, vous allez apprendre à créer Direct2D \ 32 ; contexte de périphérique dans Windows 8.
ms.assetid: D4563FEA-767E-4B16-8F3C-3D548A64B206
keywords:
- Appareil Direct2D
- Contexte de périphérique Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2858861956a40bf969309be474105052e4692cde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104568440"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a>Comment effectuer le rendu à l’aide d’un contexte de périphérique Direct2D

Dans cette rubrique, vous allez apprendre à créer un [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](./direct2d-portal.md) dans Windows 8. Ces informations s’appliquent si vous développez des applications du Windows Store ou une application de bureau à l’aide de Direct2D. Cette rubrique décrit l’objectif des objets de contexte de périphérique Direct2D, comment créer cet objet et un guide pas à pas sur le rendu et l’affichage des primitives et des images Direct2D. Vous apprendrez également à basculer les cibles de rendu et à ajouter des effets à votre application.

-   [Qu’est-ce qu’un appareil Direct2D ?](#what-is-a-direct2d-device)
-   [Qu’est-ce qu’un contexte de périphérique Direct2D ?](#what-is-a-direct2d-device-context)
-   [Rendu avec Direct2D sur Windows 8](#rendering-with-direct2d-on-windows-8)
-   [Pourquoi utiliser un contexte de périphérique pour le rendu ?](#why-use-a-device-context-to-render)
-   [Comment créer un contexte de périphérique Direct2D pour le rendu](#how-to-create-a-direct2d-device-context-for-rendering)
-   [Sélection d’une cible](#selecting-a-target)
-   [Comment afficher et afficher](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a>Qu’est-ce qu’un appareil Direct2D ?

Vous avez besoin d’un appareil Direct2D et d’un appareil Direct3D pour créer un contexte de périphérique Direct2D. Un [**appareil Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (expose un pointeur d’interface **ID2D1Device** ) représente un adaptateur d’affichage. Un appareil Direct3D (expose un pointeur d’interface [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) ) est associé à un appareil Direct2D. Chaque application doit avoir un seul **appareil Direct2D**, mais peut avoir plusieurs **appareils**.

## <a name="what-is-a-direct2d-device-context"></a>Qu’est-ce qu’un contexte de périphérique Direct2D ?

Un [](./direct2d-portal.md) [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D (expose un pointeur d’interface **ID2D1DeviceContext** ) représente un ensemble d’États et de mémoires tampons de commande que vous utilisez pour effectuer le rendu sur une cible. Vous pouvez appeler des méthodes sur le contexte de périphérique pour définir l’état du pipeline et générer des commandes de rendu en utilisant les ressources détenues par un appareil.

## <a name="rendering-with-direct2d-on-windows-8"></a>Rendu avec Direct2D sur Windows 8

Sur Windows 7 et les versions antérieures, vous utilisez un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) ou une autre interface cible de rendu pour effectuer un rendu dans une fenêtre ou une surface. À compter de Windows 8, nous ne recommandons pas le rendu à l’aide de méthodes qui reposent sur des interfaces comme **ID2D1HwndRenderTarget** , car elles ne fonctionnent pas avec les applications du Windows Store. Vous pouvez utiliser un [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pour effectuer un rendu sur un HWND si vous souhaitez créer une application de bureau tout en tirant parti des fonctionnalités supplémentaires du **contexte de périphérique** . Toutefois, le **contexte de périphérique** est nécessaire pour restituer le contenu d’une application du Windows Store avec [Direct2D](./direct2d-portal.md).

## <a name="why-use-a-device-context-to-render"></a>Pourquoi utiliser un contexte de périphérique pour le rendu ?

-   Vous pouvez effectuer le rendu pour les applications du Windows Store.
-   Vous pouvez modifier la cible de rendu à tout moment avant, pendant et après le rendu. Le contexte de périphérique garantit que les appels aux méthodes de dessin sont exécutés dans l’ordre et les applique lorsque vous changez la cible de rendu.
-   Vous pouvez utiliser plusieurs types de fenêtre avec un contexte de périphérique. Vous pouvez utiliser un [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) et [**une chaîne de permutation dxgi**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) pour effectuer un rendu direct vers un [**Windows :: UI :: Core :: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) ou un [**Windows :: UI :: XAML :: SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).
-   Vous pouvez utiliser le [](./direct2d-portal.md) [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D pour créer des [effets Direct2D](effects-overview.md) et restituer la sortie d’un graphique effet d’image ou d’effet sur une cible de rendu.
-   Vous pouvez avoir plusieurs [**contextes d’appareil**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), ce qui peut être utile pour améliorer les performances dans une application de thread. Pour plus d’informations, consultez [applications Direct2D multithread](multi-threaded-direct2d-apps.md) .
-   Le [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interagit étroitement avec Direct3D, ce qui vous donne davantage d’accès aux options Direct3D.

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a>Comment créer un contexte de périphérique Direct2D pour le rendu

Le code suivant montre comment créer un appareil Direct3D11, obtenir l’appareil DXGI associé, créer un [**appareil Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device), puis créer le [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D pour le rendu.

Voici un diagramme des appels de méthode et des interfaces que ce code utilise.

![diagramme des appareils et des contextes de périphérique de Direct2D et Direct3D.](images/devicecontextdiagram.png)

> [!Note]  
> Ce code suppose que vous disposez déjà d’un objet [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) , pour plus d’informations, consultez la [**page de référence ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).

 


```C++
    // This flag adds support for surfaces with a different color channel ordering than the API default.
    // You need it for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    
    // This array defines the set of DirectX hardware feature levels this app  supports.
    // The ordering is important and you should  preserve it.
    // Don't forget to declare your app's minimum required feature level in its
    // description.  All apps are assumed to support 9.1 unless otherwise stated.
    D3D_FEATURE_LEVEL featureLevels[] = 
    {
        D3D_FEATURE_LEVEL_11_1,
        D3D_FEATURE_LEVEL_11_0,
        D3D_FEATURE_LEVEL_10_1,
        D3D_FEATURE_LEVEL_10_0,
        D3D_FEATURE_LEVEL_9_3,
        D3D_FEATURE_LEVEL_9_2,
        D3D_FEATURE_LEVEL_9_1
    };

    // Create the DX11 API device object, and get a corresponding context.
    ComPtr<ID3D11Device> device;
    ComPtr<ID3D11DeviceContext> context;

    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of possible feature levels
            D3D11_SDK_VERSION,          
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );

    ComPtr<IDXGIDevice> dxgiDevice;
    // Obtain the underlying DXGI device of the Direct3D11 device.
    DX::ThrowIfFailed(
        device.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // Get Direct2D device's corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



Passons en revue les étapes de l’exemple de code précédent.

1.  Obtient un pointeur d’interface ID3D11Device vous en aurez besoin pour créer le contexte de périphérique.

    -   Déclarez les indicateurs de création pour configurer l’appareil [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) pour la prise en charge de BGRA. [Direct2D](./direct2d-portal.md) requiert l’ordre des couleurs BGRA.
    -   Déclarez un tableau d’entrées de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) représentant le jeu de niveaux de fonctionnalités que votre application prendra en charge.
        > [!Note]  
        > [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) effectue une recherche dans votre liste jusqu’à ce qu’il trouve le niveau de fonctionnalité pris en charge par le système hôte.

         

    -   Utilisez la fonction [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) pour créer un objet [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) , la fonction retournera également un objet [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) , mais cet objet n’est pas nécessaire pour cet exemple.

2.  Interrogez l' [**appareil Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) pour obtenir son interface d' [**appareil dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .
3.  Créez un objet [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) en appelant la méthode [**ID2D1Factory :: CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) et en passant l’objet [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .
4.  Créez un pointeur [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) à l’aide de la méthode [**ID2D1Device :: CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) .

## <a name="selecting-a-target"></a>Sélection d’une cible

Le code ci-dessous montre comment obtenir la [**texture Direct3D unidimensionnelle**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) pour la mémoire tampon d’arrière-plan de la fenêtre et créer une cible bitmap qui établit un lien vers cette texture vers laquelle le [**contexte de périphérique Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) est restitué.


```C++
        // Allocate a descriptor.
        DXGI_SWAP_CHAIN_DESC1 swapChainDesc = {0};
        swapChainDesc.Width = 0;                           // use automatic sizing
        swapChainDesc.Height = 0;
        swapChainDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM; // this is the most common swapchain format
        swapChainDesc.Stereo = false; 
        swapChainDesc.SampleDesc.Count = 1;                // don't use multi-sampling
        swapChainDesc.SampleDesc.Quality = 0;
        swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapChainDesc.BufferCount = 2;                     // use double buffering to enable flip
        swapChainDesc.Scaling = DXGI_SCALING_NONE;
        swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL; // all apps must use this SwapEffect
        swapChainDesc.Flags = 0;

        // Identify the physical adapter (GPU or card) this device is runs on.
        ComPtr<IDXGIAdapter> dxgiAdapter;
        DX::ThrowIfFailed(
            dxgiDevice->GetAdapter(&dxgiAdapter)
            );

        // Get the factory object that created the DXGI device.
        ComPtr<IDXGIFactory2> dxgiFactory;
        DX::ThrowIfFailed(
            dxgiAdapter->GetParent(IID_PPV_ARGS(&dxgiFactory))
            );

        // Get the final swap chain for this window from the DXGI factory.
        DX::ThrowIfFailed(
            dxgiFactory->CreateSwapChainForCoreWindow(
                device.Get(),
                reinterpret_cast<IUnknown*>(m_window),
                &swapChainDesc,
                nullptr,    // allow on all displays
                &m_swapChain
                )
            );

        // Ensure that DXGI doesn't queue more than one frame at a time.
        DX::ThrowIfFailed(
            dxgiDevice->SetMaximumFrameLatency(1)
            );

    // Get the backbuffer for this window which is be the final 3D render target.
    ComPtr<ID3D11Texture2D> backBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&backBuffer))
        );

    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it is directly rendered to the 
    // swap chain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_IGNORE),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // Now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



Passons en revue les étapes de l’exemple de code précédent.

1.  Allouez une structure [**\_ DESC1 de \_ chaîne \_ de permutation dxgi**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) et définissez les paramètres de la [**chaîne de permutation**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).

    Ces paramètres montrent un exemple de création d’une chaîne de permutation qu’une application du Windows Store peut utiliser.

2.  Récupérez l’adaptateur sur lequel l' [**appareil Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) et l' [**appareil dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) sont exécutés et récupérez l’objet [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) qui leur est associé. Vous devez utiliser cette **fabrique dxgi** pour vous assurer que la [**chaîne de permutation**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) est créée sur le même adaptateur.

3.  Appelez la méthode [**IDXGIFactory2 :: CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) pour créer la chaîne de permutation. Utilisez la classe [**Windows :: UI :: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) pour la fenêtre principale d’une application du Windows Store.

    Veillez à définir la latence de trame maximale sur 1 pour réduire la consommation d’énergie.

    Si vous souhaitez restituer du contenu Direct2D dans une application du Windows Store, consultez la méthode [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .

4.  Récupération de la mémoire tampon d’arrière-plan à partir de la [**chaîne de permutation**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain). La mémoire tampon d’arrière-plan expose une interface [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) allouée par la **chaîne de permutation**

5.  Déclarez une structure [**\_ \_ PROPERTIES1 bitmap d2d1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) et définissez les valeurs de propriété. Définissez le format de pixel sur BGRA, car il s’agit du format utilisé par le périphérique [**Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) et l' [**appareil dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .

6.  Obtient la mémoire tampon d’arrière-plan en tant que [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) à passer à Direct2D. Direct2D n’accepte pas directement un [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) .

    Créez un objet [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) à partir de la mémoire tampon d’arrière-plan à l’aide de la méthode [**ID2D1DeviceContext :: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) .

7.  La [**bitmap Direct2D**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) est maintenant liée à la mémoire tampon d’arrière-plan. Définissez la cible sur le [**contexte de périphérique Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) sur la **bitmap**.

## <a name="how-to-render-and-display"></a>Comment afficher et afficher

Maintenant que vous avez une bitmap cible, vous pouvez dessiner des primitives, des images, des effets d’images et du texte à l’aide du [**contexte de périphérique Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext). Le code ci-dessous montre comment dessiner un rectangle.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);

m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



Passons en revue les étapes de l’exemple de code précédent.

1.  Appelez [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) pour créer un pinceau pour peindre le rectangle.
2.  Appelez la méthode [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) avant d’émettre des commandes de dessin.
3.  Appelez la méthode [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) le rectangle à dessiner et le pinceau.
4.  Appelez la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) une fois que vous avez terminé d’émettre des commandes de dessin.
5.  Affichez le résultat en appelant la méthode [**IDXGISwapChain ::P revenons**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) .

Vous pouvez maintenant utiliser le [**contexte de périphérique Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pour dessiner des primitives, des images, des effets d’images et du texte à l’écran.

 

 