---
title: Démarrage rapide de Direct2D
description: Résume les étapes requises pour dessiner avec Direct2D et fournit un exemple de code.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, exemple de code de rectangle de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101693"
---
# <a name="direct2d-quickstart"></a><span data-ttu-id="6ff75-104">Démarrage rapide de Direct2D</span><span class="sxs-lookup"><span data-stu-id="6ff75-104">Direct2D QuickStart</span></span>

<span data-ttu-id="6ff75-105">Direct2D est une API en mode immédiat et en code natif pour la création de graphiques 2D.</span><span class="sxs-lookup"><span data-stu-id="6ff75-105">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="6ff75-106">Cette rubrique montre comment utiliser Direct2D dans une application Win32 classique pour dessiner sur un **HWND**.</span><span class="sxs-lookup"><span data-stu-id="6ff75-106">This topic illustrates how to use Direct2D within a typical Win32 application to draw to an **HWND**.</span></span>

> [!Note]  
> <span data-ttu-id="6ff75-107">Si vous souhaitez créer une application du Windows Store qui utilise Direct2D, consultez la rubrique [Direct2d QuickStart pour Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="6ff75-107">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="6ff75-108">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ff75-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="6ff75-109">Dessin d’un rectangle simple</span><span class="sxs-lookup"><span data-stu-id="6ff75-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="6ff75-110">Étape 1 : inclure l’en-tête Direct2D</span><span class="sxs-lookup"><span data-stu-id="6ff75-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="6ff75-111">Étape 2 : créer un ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="6ff75-111">Step 2: Create an ID2D1Factory</span></span>](#step-2-create-an-id2d1factory)
-   [<span data-ttu-id="6ff75-112">Étape 3 : créer un ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="6ff75-112">Step 3: Create an ID2D1HwndRenderTarget</span></span>](#step-3-create-an-id2d1hwndrendertarget)
-   [<span data-ttu-id="6ff75-113">Étape 4 : créer un pinceau</span><span class="sxs-lookup"><span data-stu-id="6ff75-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="6ff75-114">Étape 5 : dessiner le rectangle</span><span class="sxs-lookup"><span data-stu-id="6ff75-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="6ff75-115">Étape 6 : libérer des ressources</span><span class="sxs-lookup"><span data-stu-id="6ff75-115">Step 6: Release Resources</span></span>](#step-6-release-resources)
-   [<span data-ttu-id="6ff75-116">Créer une application Direct2D simple</span><span class="sxs-lookup"><span data-stu-id="6ff75-116">Create a Simple Direct2D Application</span></span>](#create-a-simple-direct2d-application)
-   [<span data-ttu-id="6ff75-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ff75-117">Related topics</span></span>](#related-topics)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="6ff75-118">Dessin d’un rectangle simple</span><span class="sxs-lookup"><span data-stu-id="6ff75-118">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="6ff75-119">Pour dessiner un rectangle à l’aide de [GDI](/windows/desktop/gdi/windows-gdi), vous pouvez gérer le message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="6ff75-119">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


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



<span data-ttu-id="6ff75-120">Le code permettant de dessiner le même rectangle avec Direct2D est similaire : il crée des ressources de dessin, décrit une forme à dessiner, dessine la forme, puis libère les ressources de dessin.</span><span class="sxs-lookup"><span data-stu-id="6ff75-120">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="6ff75-121">Les sections qui suivent décrivent chacune de ces étapes en détail.</span><span class="sxs-lookup"><span data-stu-id="6ff75-121">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="6ff75-122">Étape 1 : inclure l’en-tête Direct2D</span><span class="sxs-lookup"><span data-stu-id="6ff75-122">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="6ff75-123">En plus des en-têtes requis pour une application Win32, incluez l’en-tête d2d1. h.</span><span class="sxs-lookup"><span data-stu-id="6ff75-123">In addition to the headers required for a Win32 application, include the d2d1.h header.</span></span>

## <a name="step-2-create-an-id2d1factory"></a><span data-ttu-id="6ff75-124">Étape 2 : créer un ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="6ff75-124">Step 2: Create an ID2D1Factory</span></span>

<span data-ttu-id="6ff75-125">L’un des premiers éléments d’un exemple Direct2D est la création d’un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="6ff75-125">One of the first things that any Direct2D example does is create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



<span data-ttu-id="6ff75-126">L’interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) est le point de départ pour l’utilisation de Direct2D ; Utilisez un **ID2D1Factory** pour créer des ressources Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6ff75-126">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface is the starting point for using Direct2D; use an **ID2D1Factory** to create Direct2D resources.</span></span>

<span data-ttu-id="6ff75-127">Lorsque vous créez une fabrique, vous pouvez spécifier s’il s’agit d’un thread multiple ou d’un thread unique.</span><span class="sxs-lookup"><span data-stu-id="6ff75-127">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="6ff75-128">(Pour plus d’informations sur les fabriques multithread, consultez les notes sur la [**page de référence ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) Cet exemple crée une fabrique à thread unique.</span><span class="sxs-lookup"><span data-stu-id="6ff75-128">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="6ff75-129">En général, votre application doit créer la fabrique une seule fois et la conserver pendant toute la durée de vie de l’application.</span><span class="sxs-lookup"><span data-stu-id="6ff75-129">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1hwndrendertarget"></a><span data-ttu-id="6ff75-130">Étape 3 : créer un ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="6ff75-130">Step 3: Create an ID2D1HwndRenderTarget</span></span>

<span data-ttu-id="6ff75-131">Une fois que vous avez créé une fabrique, utilisez-la pour créer une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="6ff75-131">After you create a factory, use it to create a render target.</span></span>


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



<span data-ttu-id="6ff75-132">Une cible de rendu est un appareil qui peut effectuer des opérations de dessin et créer des ressources de dessin dépendantes de l’appareil, telles que des pinceaux.</span><span class="sxs-lookup"><span data-stu-id="6ff75-132">A render target is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="6ff75-133">Les différents types de cibles de rendu sont rendus sur différents appareils.</span><span class="sxs-lookup"><span data-stu-id="6ff75-133">Different types of render targets render to different devices.</span></span> <span data-ttu-id="6ff75-134">L’exemple précédent utilise un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), qui s’affiche sur une partie de l’écran.</span><span class="sxs-lookup"><span data-stu-id="6ff75-134">The preceding example uses an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), which renders to a portion of the screen.</span></span>

<span data-ttu-id="6ff75-135">Lorsque cela est possible, une cible de rendu utilise le GPU pour accélérer les opérations de rendu et créer des ressources de dessin.</span><span class="sxs-lookup"><span data-stu-id="6ff75-135">When possible, a render target uses the GPU to accelerate rendering operations and create drawing resources.</span></span> <span data-ttu-id="6ff75-136">Dans le cas contraire, la cible de rendu utilise le processeur pour traiter les instructions de rendu et créer des ressources.</span><span class="sxs-lookup"><span data-stu-id="6ff75-136">Otherwise, the render target uses the CPU to process rendering instructions and create resources.</span></span> <span data-ttu-id="6ff75-137">(Vous pouvez modifier ce comportement en utilisant les indicateurs de [**\_ type de \_ cible \_ de rendu d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) quand vous créez la cible de rendu.)</span><span class="sxs-lookup"><span data-stu-id="6ff75-137">(You can modify this behavior by using the [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) flags when you create the render target.)</span></span>

<span data-ttu-id="6ff75-138">La méthode [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) accepte trois paramètres.</span><span class="sxs-lookup"><span data-stu-id="6ff75-138">The [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method takes three parameters.</span></span> <span data-ttu-id="6ff75-139">Le premier paramètre, un struct de [**\_ Propriétés de \_ cible \_ de rendu d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , spécifie les options d’affichage à distance, s’il faut forcer la cible de rendu à être rendue sur un logiciel ou un matériel, et la résolution PPP.</span><span class="sxs-lookup"><span data-stu-id="6ff75-139">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) struct, specifies remote display options, whether to force the render target to render to software or hardware, and the DPI.</span></span> <span data-ttu-id="6ff75-140">Le code de cet exemple utilise la fonction d’assistance [**d2d1 :: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) pour accepter les propriétés de la cible de rendu par défaut.</span><span class="sxs-lookup"><span data-stu-id="6ff75-140">The code in this example uses the [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) helper function to accept default render target properties.</span></span>

<span data-ttu-id="6ff75-141">Le deuxième paramètre, une structure de [**Propriétés de \_ \_ \_ cible \_ de rendu HWND d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) , spécifie le **HWND** vers lequel le contenu est restitué, la taille initiale de la cible de rendu (en pixels) et ses [**options de présentation**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span><span class="sxs-lookup"><span data-stu-id="6ff75-141">The second parameter, a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) struct, specifies the **HWND** to which content is rendered, the initial size of the render target (in pixels), and its [**presentation options**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span></span> <span data-ttu-id="6ff75-142">Cet exemple utilise la fonction d’assistance [**d2d1 :: HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) pour spécifier un HWND et une taille initiale.</span><span class="sxs-lookup"><span data-stu-id="6ff75-142">This example uses the [**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) helper function to specify an HWND and initial size.</span></span> <span data-ttu-id="6ff75-143">Il utilise les options de présentation par défaut.</span><span class="sxs-lookup"><span data-stu-id="6ff75-143">It uses default presentation options.</span></span>

<span data-ttu-id="6ff75-144">Le troisième paramètre est l’adresse du pointeur qui reçoit la référence de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="6ff75-144">The third parameter is the address of the pointer that receives the render target reference.</span></span>

<span data-ttu-id="6ff75-145">Lorsque vous créez une cible de rendu et que l’accélération matérielle est disponible, vous allouez des ressources sur le GPU de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6ff75-145">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="6ff75-146">En créant une cible de rendu une fois et en la conservant le plus longtemps possible, vous obtenez des avantages en matière de performances.</span><span class="sxs-lookup"><span data-stu-id="6ff75-146">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="6ff75-147">Votre application doit créer des cibles de rendu une seule fois pour la durée de vie de l’application ou jusqu’à la réception de l’erreur de [**\_ recréation de la \_ cible D2DERR**](direct2d-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6ff75-147">Your application should create render targets once and hold on to them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="6ff75-148">Lorsque vous recevez cette erreur, vous devez recréer la cible de rendu (et toutes les ressources qu’elle a créées).</span><span class="sxs-lookup"><span data-stu-id="6ff75-148">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="step-4-create-a-brush"></a><span data-ttu-id="6ff75-149">Étape 4 : créer un pinceau</span><span class="sxs-lookup"><span data-stu-id="6ff75-149">Step 4: Create a Brush</span></span>

<span data-ttu-id="6ff75-150">À l’instar d’une fabrique, une cible de rendu peut créer des ressources de dessin.</span><span class="sxs-lookup"><span data-stu-id="6ff75-150">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="6ff75-151">Dans cet exemple, la cible de rendu crée un pinceau.</span><span class="sxs-lookup"><span data-stu-id="6ff75-151">In this example, the render target creates a brush.</span></span>


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



<span data-ttu-id="6ff75-152">Un pinceau est un objet qui peint une zone, telle que le trait d’une forme ou le remplissage d’une géométrie.</span><span class="sxs-lookup"><span data-stu-id="6ff75-152">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="6ff75-153">Dans cet exemple, le pinceau peint une zone avec une couleur unie prédéfinie, noire.</span><span class="sxs-lookup"><span data-stu-id="6ff75-153">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="6ff75-154">Direct2D fournit également d’autres types de pinceaux : les pinceaux de dégradé pour peindre des dégradés linéaires et radiaux, et un pinceau bitmap pour peindre avec des bitmaps et des modèles.</span><span class="sxs-lookup"><span data-stu-id="6ff75-154">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, and a bitmap brush for painting with bitmaps and patterns.</span></span>

<span data-ttu-id="6ff75-155">Certaines API de dessin fournissent des stylets pour dessiner des contours et des pinceaux pour remplir des formes.</span><span class="sxs-lookup"><span data-stu-id="6ff75-155">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="6ff75-156">Direct2D est différent : il ne fournit pas d’objet Pen, mais utilise un pinceau pour dessiner des contours et des formes de remplissage.</span><span class="sxs-lookup"><span data-stu-id="6ff75-156">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="6ff75-157">Lors du dessin de contours, utilisez l’interface [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) avec un pinceau pour contrôler les opérations de traçage de chemin.</span><span class="sxs-lookup"><span data-stu-id="6ff75-157">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface with a brush to control path stroking operations.</span></span>

<span data-ttu-id="6ff75-158">Un pinceau peut uniquement être utilisé avec la cible de rendu qui l’a créé et avec d’autres cibles de rendu dans le même domaine de ressource.</span><span class="sxs-lookup"><span data-stu-id="6ff75-158">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="6ff75-159">En général, vous devez créer des pinceaux une seule fois et les conserver pendant toute la durée de vie de la cible de rendu qui les a créés.</span><span class="sxs-lookup"><span data-stu-id="6ff75-159">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="6ff75-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) est l’exception solitaire ; étant donné qu’il est relativement peu coûteux à créer, vous pouvez créer un **ID2D1SolidColorBrush** chaque fois que vous dessinez un cadre, sans toucher aux performances perceptibles.</span><span class="sxs-lookup"><span data-stu-id="6ff75-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="6ff75-161">Vous pouvez également utiliser une seule **ID2D1SolidColorBrush** et modifier simplement sa couleur à chaque fois que vous l’utilisez.</span><span class="sxs-lookup"><span data-stu-id="6ff75-161">You can also use a single **ID2D1SolidColorBrush** and just change its color every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="6ff75-162">Étape 5 : dessiner le rectangle</span><span class="sxs-lookup"><span data-stu-id="6ff75-162">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="6ff75-163">Ensuite, utilisez la cible de rendu pour dessiner le rectangle.</span><span class="sxs-lookup"><span data-stu-id="6ff75-163">Next, use the render target to draw the rectangle.</span></span>


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



<span data-ttu-id="6ff75-164">La méthode [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) accepte deux paramètres : le rectangle à dessiner et le pinceau à utiliser pour peindre le contour du rectangle.</span><span class="sxs-lookup"><span data-stu-id="6ff75-164">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="6ff75-165">Si vous le souhaitez, vous pouvez également spécifier les options largeur du trait, motif des tirets, jointure de ligne et extrémité de fin.</span><span class="sxs-lookup"><span data-stu-id="6ff75-165">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="6ff75-166">Vous devez appeler la méthode [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) avant d’émettre des commandes de dessin, et vous devez appeler la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) une fois que vous avez terminé d’émettre des commandes de dessin.</span><span class="sxs-lookup"><span data-stu-id="6ff75-166">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="6ff75-167">La méthode **EndDraw** retourne un **HRESULT** qui indique si les commandes de dessin ont réussi.</span><span class="sxs-lookup"><span data-stu-id="6ff75-167">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span>

## <a name="step-6-release-resources"></a><span data-ttu-id="6ff75-168">Étape 6 : libérer des ressources</span><span class="sxs-lookup"><span data-stu-id="6ff75-168">Step 6: Release Resources</span></span>

<span data-ttu-id="6ff75-169">Lorsqu’il n’y a plus de frames à dessiner ou lorsque vous recevez l’erreur de [**\_ recréation de la \_ cible D2DERR**](direct2d-error-codes.md) , libérez la cible de rendu et les appareils qu’elle a créés.</span><span class="sxs-lookup"><span data-stu-id="6ff75-169">When there are no more frames to draw, or when you receive the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error, release the render target and any devices it created.</span></span>


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



<span data-ttu-id="6ff75-170">Lorsque votre application a terminé d’utiliser des ressources Direct2D (par exemple, quand elle est sur le point de quitter), libérez la fabrique Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6ff75-170">When your application has finished using Direct2D resources (such as when it is about to exit), release the Direct2D factory.</span></span>


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a><span data-ttu-id="6ff75-171">Créer une application Direct2D simple</span><span class="sxs-lookup"><span data-stu-id="6ff75-171">Create a Simple Direct2D Application</span></span>

<span data-ttu-id="6ff75-172">Le code de cette rubrique montre les éléments de base d’une application Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6ff75-172">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="6ff75-173">Par souci de concision, la rubrique omet l’infrastructure d’application et le code de gestion des erreurs qui est caractéristique d’une application bien écrite.</span><span class="sxs-lookup"><span data-stu-id="6ff75-173">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span> <span data-ttu-id="6ff75-174">Pour une procédure pas à pas détaillée qui montre le code complet pour la création d’une application Direct2D simple et présente les meilleures pratiques de conception, consultez [création d’une application Direct2d simple](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="6ff75-174">For a more detailed walk-through that shows the complete code for creating a simple Direct2D application and demonstrates best design practices, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ff75-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ff75-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ff75-176">Création d’une application Direct2D simple</span><span class="sxs-lookup"><span data-stu-id="6ff75-176">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

 

 