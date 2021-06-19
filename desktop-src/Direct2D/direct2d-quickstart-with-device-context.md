---
title: Démarrage rapide de Direct2D pour Windows 8
description: Résume les étapes requises pour dessiner avec Direct2D pour Windows 8 et fournit un exemple de code. Direct2D est une API de code natif pour la création de graphiques 2D.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, exemple de code de rectangle de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43442e57ed0949bdf39fc05ce1a69fded42b4b3d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406142"
---
# <a name="direct2d-quickstart-for-windows-8"></a><span data-ttu-id="a461d-105">Démarrage rapide de Direct2D pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="a461d-105">Direct2D Quickstart for Windows 8</span></span>

<span data-ttu-id="a461d-106">Direct2D est une API en mode immédiat et en code natif pour la création de graphiques 2D.</span><span class="sxs-lookup"><span data-stu-id="a461d-106">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="a461d-107">Cette rubrique montre comment utiliser Direct2D pour dessiner dans un [**Windows :: UI :: Core :: CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="a461d-107">This topic illustrates how to use Direct2D to draw to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

<span data-ttu-id="a461d-108">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="a461d-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="a461d-109">Dessin d’un rectangle simple</span><span class="sxs-lookup"><span data-stu-id="a461d-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="a461d-110">Étape 1 : inclure l’en-tête Direct2D</span><span class="sxs-lookup"><span data-stu-id="a461d-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="a461d-111">Étape 2 : créer un ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="a461d-111">Step 2: Create an ID2D1Factory1</span></span>](#step-2-create-an-id2d1factory1)
-   [<span data-ttu-id="a461d-112">Étape 3 : créer un ID2D1Device et un ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="a461d-112">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [<span data-ttu-id="a461d-113">Étape 4 : créer un pinceau</span><span class="sxs-lookup"><span data-stu-id="a461d-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="a461d-114">Étape 5 : dessiner le rectangle</span><span class="sxs-lookup"><span data-stu-id="a461d-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="a461d-115">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="a461d-115">Example code</span></span>](#example-code)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="a461d-116">Dessin d’un rectangle simple</span><span class="sxs-lookup"><span data-stu-id="a461d-116">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="a461d-117">Pour dessiner un rectangle à l’aide de [GDI](/windows/desktop/gdi/windows-gdi), vous pouvez gérer le message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="a461d-117">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



<span data-ttu-id="a461d-118">Le code permettant de dessiner le même rectangle avec Direct2D est similaire : il crée des ressources de dessin, décrit une forme à dessiner, dessine la forme, puis libère les ressources de dessin.</span><span class="sxs-lookup"><span data-stu-id="a461d-118">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="a461d-119">Les sections qui suivent décrivent chacune de ces étapes en détail.</span><span class="sxs-lookup"><span data-stu-id="a461d-119">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="a461d-120">Étape 1 : inclure l’en-tête Direct2D</span><span class="sxs-lookup"><span data-stu-id="a461d-120">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="a461d-121">En plus des en-têtes requis pour l’application, incluez les en-têtes d2d1. h et d2d1 \_ 1. h.</span><span class="sxs-lookup"><span data-stu-id="a461d-121">In addition to the headers required for the application, include the d2d1.h and d2d1\_1.h headers.</span></span>

## <a name="step-2-create-an-id2d1factory1"></a><span data-ttu-id="a461d-122">Étape 2 : créer un ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="a461d-122">Step 2: Create an ID2D1Factory1</span></span>

<span data-ttu-id="a461d-123">L’un des premiers éléments d’un exemple Direct2D est la création d’un [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span><span class="sxs-lookup"><span data-stu-id="a461d-123">One of the first things that any Direct2D example does is create an [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span></span>


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



<span data-ttu-id="a461d-124">L’interface [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) est le point de départ pour l’utilisation de Direct2D ; Utilisez un **ID2D1Factory1** pour créer des ressources Direct2D.</span><span class="sxs-lookup"><span data-stu-id="a461d-124">The [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface is the starting point for using Direct2D; use an **ID2D1Factory1** to create Direct2D resources.</span></span>

<span data-ttu-id="a461d-125">Lorsque vous créez une fabrique, vous pouvez spécifier s’il s’agit d’un thread multiple ou d’un thread unique.</span><span class="sxs-lookup"><span data-stu-id="a461d-125">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="a461d-126">(Pour plus d’informations sur les fabriques multithread, consultez les notes sur la [**page de référence ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) Cet exemple crée une fabrique à thread unique.</span><span class="sxs-lookup"><span data-stu-id="a461d-126">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="a461d-127">En général, votre application doit créer la fabrique une seule fois et la conserver pendant toute la durée de vie de l’application.</span><span class="sxs-lookup"><span data-stu-id="a461d-127">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a><span data-ttu-id="a461d-128">Étape 3 : créer un ID2D1Device et un ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="a461d-128">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>

<span data-ttu-id="a461d-129">Après avoir créé une fabrique, utilisez-la pour créer un appareil Direct2D, puis utilisez l’appareil pour créer un contexte de périphérique Direct2D.</span><span class="sxs-lookup"><span data-stu-id="a461d-129">After you create a factory, use it to create a Direct2D device and then use the device to create a Direct2D device context.</span></span> <span data-ttu-id="a461d-130">Pour créer ces objets Direct2D, vous devez disposer d’un [**appareil Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , d’un [**appareil dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)et d’une [**chaîne de permutation dxgi**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span><span class="sxs-lookup"><span data-stu-id="a461d-130">In order to create these Direct2D objects, you must have a [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , a [**DXGI device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice), and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="a461d-131">Pour plus d’informations sur la création des composants requis [, consultez contextes de périphériques et](devices-and-device-contexts.md) de périphériques.</span><span class="sxs-lookup"><span data-stu-id="a461d-131">See [Devices and Device Contexts](devices-and-device-contexts.md) for info on creating the necessary prerequisites.</span></span>


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



<span data-ttu-id="a461d-132">Un contexte de périphérique est un appareil qui peut effectuer des opérations de dessin et créer des ressources de dessin dépendant de l’appareil, telles que des pinceaux.</span><span class="sxs-lookup"><span data-stu-id="a461d-132">A device context is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="a461d-133">Vous utilisez également le contexte de périphérique pour lier un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) à une surface DXGI à utiliser comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="a461d-133">You also use the device context to link a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) to a DXGI surface to use as a render target.</span></span> <span data-ttu-id="a461d-134">Le contexte de périphérique peut être rendu sur différents types de cibles.</span><span class="sxs-lookup"><span data-stu-id="a461d-134">The device context can render to different types of targets.</span></span>

<span data-ttu-id="a461d-135">Le code ci-dessous déclare les propriétés de la bitmap qui établit un lien vers une chaîne de permutation DXGI qui est restituée à un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="a461d-135">The code here declares the properties for bitmap that links to a DXGI swap chain that renders to a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span> <span data-ttu-id="a461d-136">La méthode [**ID2D1DeviceContext :: CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) obtient une surface Direct2D à partir de la surface DXGI.</span><span class="sxs-lookup"><span data-stu-id="a461d-136">The [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method gets a Direct2D surface from the DXGI surface.</span></span> <span data-ttu-id="a461d-137">Ainsi, toute donnée rendue au [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) cible est rendue à la surface de la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="a461d-137">This makes it so anything rendered to the target [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is rendered to the surface of the swap chain.</span></span>

<span data-ttu-id="a461d-138">Une fois que vous avez la surface Direct2D, utilisez la méthode [**ID2D1DeviceContext :: SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) pour la définir en tant que cible de rendu active.</span><span class="sxs-lookup"><span data-stu-id="a461d-138">Once you have the Direct2D surface, use the [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) method to set it as the active render target.</span></span>


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
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

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a><span data-ttu-id="a461d-139">Étape 4 : créer un pinceau</span><span class="sxs-lookup"><span data-stu-id="a461d-139">Step 4: Create a Brush</span></span>

<span data-ttu-id="a461d-140">À l’instar d’une fabrique, un contexte de périphérique peut créer des ressources de dessin.</span><span class="sxs-lookup"><span data-stu-id="a461d-140">Like a factory, a device context can create drawing resources.</span></span> <span data-ttu-id="a461d-141">Dans cet exemple, le contexte de périphérique crée un pinceau.</span><span class="sxs-lookup"><span data-stu-id="a461d-141">In this example, the device context creates a brush.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



<span data-ttu-id="a461d-142">Un pinceau est un objet qui peint une zone, telle que le trait d’une forme ou le remplissage d’une géométrie.</span><span class="sxs-lookup"><span data-stu-id="a461d-142">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="a461d-143">Dans cet exemple, le pinceau peint une zone avec une couleur unie prédéfinie, noire.</span><span class="sxs-lookup"><span data-stu-id="a461d-143">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="a461d-144">Direct2D fournit également d’autres types de pinceaux : les pinceaux de dégradé pour peindre des dégradés linéaires et radiaux, un [**pinceau bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pour peindre avec des bitmaps et des modèles, et à partir de Windows 8, un [**pinceau d’image**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) pour peindre avec une image rendue.</span><span class="sxs-lookup"><span data-stu-id="a461d-144">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, a [**bitmap brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) for painting with bitmaps and patterns, and starting in Windows 8, an [**image brush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) for painting with a rendered image.</span></span>

<span data-ttu-id="a461d-145">Certaines API de dessin fournissent des stylets pour dessiner des contours et des pinceaux pour remplir des formes.</span><span class="sxs-lookup"><span data-stu-id="a461d-145">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="a461d-146">Direct2D est différent : il ne fournit pas d’objet Pen, mais utilise un pinceau pour dessiner des contours et des formes de remplissage.</span><span class="sxs-lookup"><span data-stu-id="a461d-146">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="a461d-147">Lors du dessin de contours, utilisez l’interface [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) , ou à partir de Windows 8, l’interface [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) , avec un pinceau pour contrôler les opérations de traçage de chemin.</span><span class="sxs-lookup"><span data-stu-id="a461d-147">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface, or starting in Windows 8 the [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) interface, with a brush to control path stroking operations.</span></span>

<span data-ttu-id="a461d-148">Un pinceau peut uniquement être utilisé avec la cible de rendu qui l’a créé et avec d’autres cibles de rendu dans le même domaine de ressource.</span><span class="sxs-lookup"><span data-stu-id="a461d-148">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="a461d-149">En général, vous devez créer des pinceaux une seule fois et les conserver pendant toute la durée de vie de la cible de rendu qui les a créés.</span><span class="sxs-lookup"><span data-stu-id="a461d-149">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="a461d-150">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) est l’exception solitaire ; étant donné qu’il est relativement peu coûteux à créer, vous pouvez créer un **ID2D1SolidColorBrush** chaque fois que vous dessinez un cadre, sans toucher aux performances perceptibles.</span><span class="sxs-lookup"><span data-stu-id="a461d-150">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="a461d-151">Vous pouvez également utiliser un seul **ID2D1SolidColorBrush** et modifier sa couleur ou son opacité chaque fois que vous l’utilisez.</span><span class="sxs-lookup"><span data-stu-id="a461d-151">You can also use a single **ID2D1SolidColorBrush** and just change its color or opacity every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="a461d-152">Étape 5 : dessiner le rectangle</span><span class="sxs-lookup"><span data-stu-id="a461d-152">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="a461d-153">Ensuite, utilisez le contexte de périphérique pour dessiner le rectangle.</span><span class="sxs-lookup"><span data-stu-id="a461d-153">Next, use the device context to draw the rectangle.</span></span>


```C++
 
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



<span data-ttu-id="a461d-154">La méthode [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) accepte deux paramètres : le rectangle à dessiner et le pinceau à utiliser pour peindre le contour du rectangle.</span><span class="sxs-lookup"><span data-stu-id="a461d-154">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="a461d-155">Si vous le souhaitez, vous pouvez également spécifier les options largeur du trait, motif des tirets, jointure de ligne et extrémité de fin.</span><span class="sxs-lookup"><span data-stu-id="a461d-155">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="a461d-156">Vous devez appeler la méthode [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) avant d’émettre des commandes de dessin, et vous devez appeler la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) une fois que vous avez terminé d’émettre des commandes de dessin.</span><span class="sxs-lookup"><span data-stu-id="a461d-156">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="a461d-157">La méthode **EndDraw** retourne un **HRESULT** qui indique si les commandes de dessin ont réussi.</span><span class="sxs-lookup"><span data-stu-id="a461d-157">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span> <span data-ttu-id="a461d-158">Si elle échoue, la fonction d’assistance ThrowIfFailed lèvera une exception.</span><span class="sxs-lookup"><span data-stu-id="a461d-158">If it is not successful, the ThrowIfFailed helper function will throw an exception.</span></span>

<span data-ttu-id="a461d-159">La méthode [**IDXGISwapChain ::P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) replaced permute la surface de la mémoire tampon avec la surface de l’écran pour afficher le résultat.</span><span class="sxs-lookup"><span data-stu-id="a461d-159">The [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method swaps the buffer surface with the on screen surface to display the result.</span></span>

## <a name="example-code"></a><span data-ttu-id="a461d-160">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="a461d-160">Example code</span></span>

<span data-ttu-id="a461d-161">Le code de cette rubrique montre les éléments de base d’une application Direct2D.</span><span class="sxs-lookup"><span data-stu-id="a461d-161">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="a461d-162">Par souci de concision, la rubrique omet l’infrastructure d’application et le code de gestion des erreurs qui est caractéristique d’une application bien écrite.</span><span class="sxs-lookup"><span data-stu-id="a461d-162">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span>

 

 