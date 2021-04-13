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
# <a name="how-to-render-by-using-a-direct2d-device-context"></a><span data-ttu-id="1175d-105">Comment effectuer le rendu à l’aide d’un contexte de périphérique Direct2D</span><span class="sxs-lookup"><span data-stu-id="1175d-105">How to render by using a Direct2D device context</span></span>

<span data-ttu-id="1175d-106">Dans cette rubrique, vous allez apprendre à créer un [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) [Direct2D](./direct2d-portal.md) dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1175d-106">In this topic you will learn about creating [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) in Windows 8.</span></span> <span data-ttu-id="1175d-107">Ces informations s’appliquent si vous développez des applications du Windows Store ou une application de bureau à l’aide de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1175d-107">This information applies to you if you are developing Windows Store apps or a desktop app by using Direct2D.</span></span> <span data-ttu-id="1175d-108">Cette rubrique décrit l’objectif des objets de contexte de périphérique Direct2D, comment créer cet objet et un guide pas à pas sur le rendu et l’affichage des primitives et des images Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1175d-108">This topic describes the purpose of Direct2D device context objects, how to create that object , and a step by step guide about rendering and displaying Direct2D primitives and images.</span></span> <span data-ttu-id="1175d-109">Vous apprendrez également à basculer les cibles de rendu et à ajouter des effets à votre application.</span><span class="sxs-lookup"><span data-stu-id="1175d-109">You will also learn about switching render targets and adding effects to your app.</span></span>

-   [<span data-ttu-id="1175d-110">Qu’est-ce qu’un appareil Direct2D ?</span><span class="sxs-lookup"><span data-stu-id="1175d-110">What is a Direct2D device?</span></span>](#what-is-a-direct2d-device)
-   [<span data-ttu-id="1175d-111">Qu’est-ce qu’un contexte de périphérique Direct2D ?</span><span class="sxs-lookup"><span data-stu-id="1175d-111">What is a Direct2D device context?</span></span>](#what-is-a-direct2d-device-context)
-   [<span data-ttu-id="1175d-112">Rendu avec Direct2D sur Windows 8</span><span class="sxs-lookup"><span data-stu-id="1175d-112">Rendering with Direct2D on Windows 8</span></span>](#rendering-with-direct2d-on-windows-8)
-   [<span data-ttu-id="1175d-113">Pourquoi utiliser un contexte de périphérique pour le rendu ?</span><span class="sxs-lookup"><span data-stu-id="1175d-113">Why use a device context to render?</span></span>](#why-use-a-device-context-to-render)
-   [<span data-ttu-id="1175d-114">Comment créer un contexte de périphérique Direct2D pour le rendu</span><span class="sxs-lookup"><span data-stu-id="1175d-114">How to create a Direct2D device context for rendering</span></span>](#how-to-create-a-direct2d-device-context-for-rendering)
-   [<span data-ttu-id="1175d-115">Sélection d’une cible</span><span class="sxs-lookup"><span data-stu-id="1175d-115">Selecting a target</span></span>](#selecting-a-target)
-   [<span data-ttu-id="1175d-116">Comment afficher et afficher</span><span class="sxs-lookup"><span data-stu-id="1175d-116">How to render and display</span></span>](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a><span data-ttu-id="1175d-117">Qu’est-ce qu’un appareil Direct2D ?</span><span class="sxs-lookup"><span data-stu-id="1175d-117">What is a Direct2D device?</span></span>

<span data-ttu-id="1175d-118">Vous avez besoin d’un appareil Direct2D et d’un appareil Direct3D pour créer un contexte de périphérique Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1175d-118">You need a Direct2D device and a Direct3D device to create a Direct2D device context.</span></span> <span data-ttu-id="1175d-119">Un [**appareil Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (expose un pointeur d’interface **ID2D1Device** ) représente un adaptateur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="1175d-119">A [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (exposes an **ID2D1Device** interface pointer) represents a display adapter.</span></span> <span data-ttu-id="1175d-120">Un appareil Direct3D (expose un pointeur d’interface [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) ) est associé à un appareil Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1175d-120">A Direct3D device (exposes an [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) interface pointer) is associated with a Direct2D device.</span></span> <span data-ttu-id="1175d-121">Chaque application doit avoir un seul **appareil Direct2D**, mais peut avoir plusieurs **appareils**.</span><span class="sxs-lookup"><span data-stu-id="1175d-121">Each app must have one **Direct2D device**, but can have more than one **device**.</span></span>

## <a name="what-is-a-direct2d-device-context"></a><span data-ttu-id="1175d-122">Qu’est-ce qu’un contexte de périphérique Direct2D ?</span><span class="sxs-lookup"><span data-stu-id="1175d-122">What is a Direct2D device context?</span></span>

<span data-ttu-id="1175d-123">Un [](./direct2d-portal.md) [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D (expose un pointeur d’interface **ID2D1DeviceContext** ) représente un ensemble d’États et de mémoires tampons de commande que vous utilisez pour effectuer le rendu sur une cible.</span><span class="sxs-lookup"><span data-stu-id="1175d-123">A [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (exposes an **ID2D1DeviceContext** interface pointer) represents a set of state and command buffers that you use to render to a target.</span></span> <span data-ttu-id="1175d-124">Vous pouvez appeler des méthodes sur le contexte de périphérique pour définir l’état du pipeline et générer des commandes de rendu en utilisant les ressources détenues par un appareil.</span><span class="sxs-lookup"><span data-stu-id="1175d-124">You can call methods on the device context to set pipeline state and generate rendering commands by using the resources owned by a device.</span></span>

## <a name="rendering-with-direct2d-on-windows-8"></a><span data-ttu-id="1175d-125">Rendu avec Direct2D sur Windows 8</span><span class="sxs-lookup"><span data-stu-id="1175d-125">Rendering with Direct2D on Windows 8</span></span>

<span data-ttu-id="1175d-126">Sur Windows 7 et les versions antérieures, vous utilisez un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) ou une autre interface cible de rendu pour effectuer un rendu dans une fenêtre ou une surface.</span><span class="sxs-lookup"><span data-stu-id="1175d-126">On Windows 7 and earlier, you use a [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) or another render target interface to render to a window or surface.</span></span> <span data-ttu-id="1175d-127">À compter de Windows 8, nous ne recommandons pas le rendu à l’aide de méthodes qui reposent sur des interfaces comme **ID2D1HwndRenderTarget** , car elles ne fonctionnent pas avec les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1175d-127">Starting with Windows 8, we do not recommend rendering by using methods that rely on interfaces like **ID2D1HwndRenderTarget** because they won't work with Windows Store apps.</span></span> <span data-ttu-id="1175d-128">Vous pouvez utiliser un [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pour effectuer un rendu sur un HWND si vous souhaitez créer une application de bureau tout en tirant parti des fonctionnalités supplémentaires du **contexte de périphérique** .</span><span class="sxs-lookup"><span data-stu-id="1175d-128">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to render to an Hwnd if you want to make a desktop app and still take advantage of the **device context's** additional features.</span></span> <span data-ttu-id="1175d-129">Toutefois, le **contexte de périphérique** est nécessaire pour restituer le contenu d’une application du Windows Store avec [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="1175d-129">However, the **device context** is required to render content in a Windows Store apps with [Direct2D](./direct2d-portal.md).</span></span>

## <a name="why-use-a-device-context-to-render"></a><span data-ttu-id="1175d-130">Pourquoi utiliser un contexte de périphérique pour le rendu ?</span><span class="sxs-lookup"><span data-stu-id="1175d-130">Why use a device context to render?</span></span>

-   <span data-ttu-id="1175d-131">Vous pouvez effectuer le rendu pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1175d-131">You can render for Windows Store apps.</span></span>
-   <span data-ttu-id="1175d-132">Vous pouvez modifier la cible de rendu à tout moment avant, pendant et après le rendu.</span><span class="sxs-lookup"><span data-stu-id="1175d-132">You can change the render target at any time before, during, and after rendering.</span></span> <span data-ttu-id="1175d-133">Le contexte de périphérique garantit que les appels aux méthodes de dessin sont exécutés dans l’ordre et les applique lorsque vous changez la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="1175d-133">The device context ensures that the calls to drawing methods are executed in order and applies them when you switch the render target.</span></span>
-   <span data-ttu-id="1175d-134">Vous pouvez utiliser plusieurs types de fenêtre avec un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="1175d-134">You can use more than one type of window with a device context.</span></span> <span data-ttu-id="1175d-135">Vous pouvez utiliser un [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) et [**une chaîne de permutation dxgi**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) pour effectuer un rendu direct vers un [**Windows :: UI :: Core :: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) ou un [**Windows :: UI :: XAML :: SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span><span class="sxs-lookup"><span data-stu-id="1175d-135">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) to render directly to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) or a [**Windows::UI::XAML::SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span></span>
-   <span data-ttu-id="1175d-136">Vous pouvez utiliser le [](./direct2d-portal.md) [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D pour créer des [effets Direct2D](effects-overview.md) et restituer la sortie d’un graphique effet d’image ou d’effet sur une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="1175d-136">You can use the [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to create [Direct2D effects](effects-overview.md) and to render the output of an image effect or effect graph to a render target.</span></span>
-   <span data-ttu-id="1175d-137">Vous pouvez avoir plusieurs [**contextes d’appareil**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), ce qui peut être utile pour améliorer les performances dans une application de thread.</span><span class="sxs-lookup"><span data-stu-id="1175d-137">You can have multiple [**device contexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), which can be helpful for improving performance in a threaded app.</span></span> <span data-ttu-id="1175d-138">Pour plus d’informations, consultez [applications Direct2D multithread](multi-threaded-direct2d-apps.md) .</span><span class="sxs-lookup"><span data-stu-id="1175d-138">See [Multithreaded Direct2D apps](multi-threaded-direct2d-apps.md) for more information.</span></span>
-   <span data-ttu-id="1175d-139">Le [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interagit étroitement avec Direct3D, ce qui vous donne davantage d’accès aux options Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1175d-139">The [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interoperates closely with Direct3D, giving you more access to Direct3D options.</span></span>

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a><span data-ttu-id="1175d-140">Comment créer un contexte de périphérique Direct2D pour le rendu</span><span class="sxs-lookup"><span data-stu-id="1175d-140">How to create a Direct2D device context for rendering</span></span>

<span data-ttu-id="1175d-141">Le code suivant montre comment créer un appareil Direct3D11, obtenir l’appareil DXGI associé, créer un [**appareil Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device), puis créer le [**contexte de périphérique**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Direct2D pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="1175d-141">The code here shows you how to create a Direct3D11 device, get the associated DXGI device, create a [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device), and then finally create the Direct2D [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) for rendering.</span></span>

<span data-ttu-id="1175d-142">Voici un diagramme des appels de méthode et des interfaces que ce code utilise.</span><span class="sxs-lookup"><span data-stu-id="1175d-142">Here is a diagram of the method calls and the interfaces this code uses.</span></span>

![diagramme des appareils et des contextes de périphérique de Direct2D et Direct3D.](images/devicecontextdiagram.png)

> [!Note]  
> <span data-ttu-id="1175d-144">Ce code suppose que vous disposez déjà d’un objet [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) , pour plus d’informations, consultez la [**page de référence ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="1175d-144">This code assumes you already have an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) object, for more information see the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>

 


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



<span data-ttu-id="1175d-145">Passons en revue les étapes de l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="1175d-145">Let's walk through the steps in the preceding code sample.</span></span>

1.  <span data-ttu-id="1175d-146">Obtient un pointeur d’interface ID3D11Device vous en aurez besoin pour créer le contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="1175d-146">Get an ID3D11Device interface pointer you will need this to create the device context.</span></span>

    -   <span data-ttu-id="1175d-147">Déclarez les indicateurs de création pour configurer l’appareil [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) pour la prise en charge de BGRA.</span><span class="sxs-lookup"><span data-stu-id="1175d-147">Declare the creation flags to set up the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) device for BGRA support.</span></span> <span data-ttu-id="1175d-148">[Direct2D](./direct2d-portal.md) requiert l’ordre des couleurs BGRA.</span><span class="sxs-lookup"><span data-stu-id="1175d-148">[Direct2D](./direct2d-portal.md) requires BGRA color order.</span></span>
    -   <span data-ttu-id="1175d-149">Déclarez un tableau d’entrées de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) représentant le jeu de niveaux de fonctionnalités que votre application prendra en charge.</span><span class="sxs-lookup"><span data-stu-id="1175d-149">Declare an array of [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) entries representing the set of feature levels that your app will support.</span></span>
        > [!Note]  
        > <span data-ttu-id="1175d-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) effectue une recherche dans votre liste jusqu’à ce qu’il trouve le niveau de fonctionnalité pris en charge par le système hôte.</span><span class="sxs-lookup"><span data-stu-id="1175d-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) searches your list until it finds the feature level supported by the host system.</span></span>

         

    -   <span data-ttu-id="1175d-151">Utilisez la fonction [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) pour créer un objet [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) , la fonction retournera également un objet [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) , mais cet objet n’est pas nécessaire pour cet exemple.</span><span class="sxs-lookup"><span data-stu-id="1175d-151">Use the [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) function to create an [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) object, the function will also return an [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) object, but that object is not needed for this example.</span></span>

2.  <span data-ttu-id="1175d-152">Interrogez l' [**appareil Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) pour obtenir son interface d' [**appareil dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="1175d-152">Query the [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) for its [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) interface.</span></span>
3.  <span data-ttu-id="1175d-153">Créez un objet [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) en appelant la méthode [**ID2D1Factory :: CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) et en passant l’objet [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="1175d-153">Create an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) object by calling the [**ID2D1Factory::CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) method and passing in the [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) object.</span></span>
4.  <span data-ttu-id="1175d-154">Créez un pointeur [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) à l’aide de la méthode [**ID2D1Device :: CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) .</span><span class="sxs-lookup"><span data-stu-id="1175d-154">Create an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pointer using the [**ID2D1Device::CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) method.</span></span>

## <a name="selecting-a-target"></a><span data-ttu-id="1175d-155">Sélection d’une cible</span><span class="sxs-lookup"><span data-stu-id="1175d-155">Selecting a target</span></span>

<span data-ttu-id="1175d-156">Le code ci-dessous montre comment obtenir la [**texture Direct3D unidimensionnelle**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) pour la mémoire tampon d’arrière-plan de la fenêtre et créer une cible bitmap qui établit un lien vers cette texture vers laquelle le [**contexte de périphérique Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) est restitué.</span><span class="sxs-lookup"><span data-stu-id="1175d-156">The code here shows you how to get the [**2 dimensional Direct3D texture**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) for the window back buffer and create a bitmap target that links to this texture to which the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) renders.</span></span>


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



<span data-ttu-id="1175d-157">Passons en revue les étapes de l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="1175d-157">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="1175d-158">Allouez une structure [**\_ DESC1 de \_ chaîne \_ de permutation dxgi**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) et définissez les paramètres de la [**chaîne de permutation**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="1175d-158">Allocate a [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and define the settings for the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

    <span data-ttu-id="1175d-159">Ces paramètres montrent un exemple de création d’une chaîne de permutation qu’une application du Windows Store peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="1175d-159">These settings show an example of how to create a swap chain that a Windows Store app can use.</span></span>

2.  <span data-ttu-id="1175d-160">Récupérez l’adaptateur sur lequel l' [**appareil Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) et l' [**appareil dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) sont exécutés et récupérez l’objet [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) qui leur est associé.</span><span class="sxs-lookup"><span data-stu-id="1175d-160">Get the adapter that the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) are running on and get the [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) object associated with them.</span></span> <span data-ttu-id="1175d-161">Vous devez utiliser cette **fabrique dxgi** pour vous assurer que la [**chaîne de permutation**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) est créée sur le même adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1175d-161">You must use this **DXGI factory** to ensure the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) is created on the same adapter.</span></span>

3.  <span data-ttu-id="1175d-162">Appelez la méthode [**IDXGIFactory2 :: CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) pour créer la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="1175d-162">Call the [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) method to create the swap chain.</span></span> <span data-ttu-id="1175d-163">Utilisez la classe [**Windows :: UI :: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) pour la fenêtre principale d’une application du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1175d-163">Use the [**Windows::UI::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) class for the main window of a Windows Store app.</span></span>

    <span data-ttu-id="1175d-164">Veillez à définir la latence de trame maximale sur 1 pour réduire la consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="1175d-164">Make sure to set the maximum frame latency to 1 to minimize power consumption.</span></span>

    <span data-ttu-id="1175d-165">Si vous souhaitez restituer du contenu Direct2D dans une application du Windows Store, consultez la méthode [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .</span><span class="sxs-lookup"><span data-stu-id="1175d-165">If you want to render Direct2D content in a Windows Store app, see the [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method.</span></span>

4.  <span data-ttu-id="1175d-166">Récupération de la mémoire tampon d’arrière-plan à partir de la [**chaîne de permutation**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span><span class="sxs-lookup"><span data-stu-id="1175d-166">Get the back buffer from the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span> <span data-ttu-id="1175d-167">La mémoire tampon d’arrière-plan expose une interface [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) allouée par la **chaîne de permutation**</span><span class="sxs-lookup"><span data-stu-id="1175d-167">The back buffer exposes an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) interface allocated by the **swap chain**</span></span>

5.  <span data-ttu-id="1175d-168">Déclarez une structure [**\_ \_ PROPERTIES1 bitmap d2d1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) et définissez les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="1175d-168">Declare a [**D2D1\_BITMAP\_PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct and set the property values.</span></span> <span data-ttu-id="1175d-169">Définissez le format de pixel sur BGRA, car il s’agit du format utilisé par le périphérique [**Direct3D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) et l' [**appareil dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) .</span><span class="sxs-lookup"><span data-stu-id="1175d-169">Set the pixel format to BGRA because this is the format the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) use.</span></span>

6.  <span data-ttu-id="1175d-170">Obtient la mémoire tampon d’arrière-plan en tant que [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) à passer à Direct2D.</span><span class="sxs-lookup"><span data-stu-id="1175d-170">Get the back buffer as an [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) to pass to Direct2D.</span></span> <span data-ttu-id="1175d-171">Direct2D n’accepte pas directement un [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) .</span><span class="sxs-lookup"><span data-stu-id="1175d-171">Direct2D doesn't accept an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) directly.</span></span>

    <span data-ttu-id="1175d-172">Créez un objet [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) à partir de la mémoire tampon d’arrière-plan à l’aide de la méthode [**ID2D1DeviceContext :: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) .</span><span class="sxs-lookup"><span data-stu-id="1175d-172">Create a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object from the back buffer using the [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method.</span></span>

7.  <span data-ttu-id="1175d-173">La [**bitmap Direct2D**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) est maintenant liée à la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="1175d-173">Now the [**Direct2D bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is linked to the back buffer.</span></span> <span data-ttu-id="1175d-174">Définissez la cible sur le [**contexte de périphérique Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) sur la **bitmap**.</span><span class="sxs-lookup"><span data-stu-id="1175d-174">Set the target on the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to the **bitmap**.</span></span>

## <a name="how-to-render-and-display"></a><span data-ttu-id="1175d-175">Comment afficher et afficher</span><span class="sxs-lookup"><span data-stu-id="1175d-175">How to render and display</span></span>

<span data-ttu-id="1175d-176">Maintenant que vous avez une bitmap cible, vous pouvez dessiner des primitives, des images, des effets d’images et du texte à l’aide du [**contexte de périphérique Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span><span class="sxs-lookup"><span data-stu-id="1175d-176">Now that you have a target bitmap, you can draw primitives, images, image effects, and text to it using the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span> <span data-ttu-id="1175d-177">Le code ci-dessous montre comment dessiner un rectangle.</span><span class="sxs-lookup"><span data-stu-id="1175d-177">The code here shows you how to draw a rectangle.</span></span>


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



<span data-ttu-id="1175d-178">Passons en revue les étapes de l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="1175d-178">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="1175d-179">Appelez [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) pour créer un pinceau pour peindre le rectangle.</span><span class="sxs-lookup"><span data-stu-id="1175d-179">Call the [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) to create a brush to paint the rectangle.</span></span>
2.  <span data-ttu-id="1175d-180">Appelez la méthode [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) avant d’émettre des commandes de dessin.</span><span class="sxs-lookup"><span data-stu-id="1175d-180">Call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands.</span></span>
3.  <span data-ttu-id="1175d-181">Appelez la méthode [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) le rectangle à dessiner et le pinceau.</span><span class="sxs-lookup"><span data-stu-id="1175d-181">Call the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method the rectangle to be drawn and the brush.</span></span>
4.  <span data-ttu-id="1175d-182">Appelez la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) une fois que vous avez terminé d’émettre des commandes de dessin.</span><span class="sxs-lookup"><span data-stu-id="1175d-182">Call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span>
5.  <span data-ttu-id="1175d-183">Affichez le résultat en appelant la méthode [**IDXGISwapChain ::P revenons**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) .</span><span class="sxs-lookup"><span data-stu-id="1175d-183">Display the result by calling the [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method.</span></span>

<span data-ttu-id="1175d-184">Vous pouvez maintenant utiliser le [**contexte de périphérique Direct2D**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pour dessiner des primitives, des images, des effets d’images et du texte à l’écran.</span><span class="sxs-lookup"><span data-stu-id="1175d-184">Now you can use the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) draw primitives, images, image effects, and text to the screen.</span></span>

 

 