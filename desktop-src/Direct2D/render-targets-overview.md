---
title: Vue d’ensemble des cibles de rendu
description: Décrit les différents types de cibles de rendu Direct2D et comment les utiliser.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, cibles de rendu
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941118"
---
# <a name="render-targets-overview"></a><span data-ttu-id="4dd7a-104">Vue d’ensemble des cibles de rendu</span><span class="sxs-lookup"><span data-stu-id="4dd7a-104">Render Targets Overview</span></span>

<span data-ttu-id="4dd7a-105">Une cible de rendu est une ressource qui hérite de l’interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="4dd7a-105">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="4dd7a-106">Une cible de rendu crée des ressources pour dessiner et effectue des opérations de dessin réelles.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-106">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="4dd7a-107">Cette rubrique décrit les différents types de cibles de rendu Direct2D et comment les utiliser.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-107">This topic describes the different types of Direct2D render targets and how to use them.</span></span>

-   [<span data-ttu-id="4dd7a-108">Cibles de rendu</span><span class="sxs-lookup"><span data-stu-id="4dd7a-108">Render Targets</span></span>](#render-targets-overview)
    -   [<span data-ttu-id="4dd7a-109">Fonctionnalités de la cible de rendu</span><span class="sxs-lookup"><span data-stu-id="4dd7a-109">Render Target Features</span></span>](#render-target-features)
    -   [<span data-ttu-id="4dd7a-110">Afficher les ressources cibles</span><span class="sxs-lookup"><span data-stu-id="4dd7a-110">Render Target Resources</span></span>](#render-target-resources)
    -   [<span data-ttu-id="4dd7a-111">Commandes de dessin</span><span class="sxs-lookup"><span data-stu-id="4dd7a-111">Drawing Commands</span></span>](#drawing-commands)
    -   [<span data-ttu-id="4dd7a-112">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="4dd7a-112">Error Handling</span></span>](#error-handling)
-   [<span data-ttu-id="4dd7a-113">Exemple : afficher le contenu dans une fenêtre</span><span class="sxs-lookup"><span data-stu-id="4dd7a-113">Example: Render Content to a Window</span></span>](#example-render-content-to-a-window)

## <a name="render-targets"></a><span data-ttu-id="4dd7a-114">Cibles de rendu</span><span class="sxs-lookup"><span data-stu-id="4dd7a-114">Render Targets</span></span>

<span data-ttu-id="4dd7a-115">Une cible de rendu est une ressource qui hérite de l’interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="4dd7a-115">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="4dd7a-116">Une cible de rendu crée des ressources pour dessiner et effectue des opérations de dessin réelles.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-116">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="4dd7a-117">Il existe plusieurs types de cibles de rendu qui peuvent être utilisées pour restituer des graphiques des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="4dd7a-117">There are several kinds of render targets that can be used to render graphics in the following ways:</span></span>

-   <span data-ttu-id="4dd7a-118">Les objets [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) affichent le contenu dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-118">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) objects render content to a window.</span></span>
-   <span data-ttu-id="4dd7a-119">Les objets [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) sont rendus dans un contexte de périphérique GDI.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-119">[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) objects render to a GDI device context.</span></span>
-   <span data-ttu-id="4dd7a-120">Les objets cibles de rendu bitmap affichent le contenu dans une image bitmap hors écran.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-120">Bitmap render target objects render content to an off-screen bitmap.</span></span>
-   <span data-ttu-id="4dd7a-121">Les objets cibles de rendu DXGI sont rendus sur une surface DXGI pour une utilisation avec Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-121">DXGI render target objects render to a DXGI surface for use with Direct3D.</span></span>

<span data-ttu-id="4dd7a-122">Étant donné qu’une cible de rendu est associée à un appareil de rendu particulier, il s’agit d’une ressource dépendante de l’appareil qui cesse de fonctionner si l’appareil est supprimé.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-122">Because a render target is associated with a particular rendering device, it is a device-dependent resource and ceases to function if the device is removed.</span></span>

### <a name="render-target-features"></a><span data-ttu-id="4dd7a-123">Fonctionnalités de la cible de rendu</span><span class="sxs-lookup"><span data-stu-id="4dd7a-123">Render Target Features</span></span>

<span data-ttu-id="4dd7a-124">Vous pouvez spécifier si une cible de rendu utilise l’accélération matérielle et si l’affichage à distance est rendu par un ordinateur local ou distant.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-124">You can specify whether a render target uses hardware acceleration and whether remote display is rendered by a local or a remote computer.</span></span> <span data-ttu-id="4dd7a-125">Les cibles de rendu peuvent être configurées pour le rendu avec ou sans alias.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-125">Render targets can be set up for aliased or antialiased rendering.</span></span> <span data-ttu-id="4dd7a-126">Pour le rendu des scènes avec un grand nombre de primitives, un développeur peut également restituer des graphiques 2D en mode alias et utiliser l’anticrénelage à plusieurs échantillons D3D pour obtenir une plus grande évolutivité.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-126">For rendering scenes with a large number of primitives, a developer can also render 2-D graphics in aliased mode and use D3D multisample antialiasing to achieve greater scalability.</span></span>

<span data-ttu-id="4dd7a-127">Les cibles de rendu peuvent également regrouper des opérations de dessin dans des couches représentées par l’interface [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) .</span><span class="sxs-lookup"><span data-stu-id="4dd7a-127">Render targets can also group drawing operations into layers represented by the [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) interface.</span></span> <span data-ttu-id="4dd7a-128">Les couches sont utiles pour la collecte des opérations de dessin à combiner lors du rendu d’un frame.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-128">Layers are useful for collecting drawing operations to be composited together when rendering a frame.</span></span> <span data-ttu-id="4dd7a-129">Pour certains scénarios, il peut s’agir d’une alternative utile au rendu d’une cible de rendu bitmap, puis de la réutilisation du contenu de l’image bitmap, car les coûts d’allocation pour la superposition sont inférieurs à ceux d’un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="4dd7a-129">For some scenarios, this can be a useful alternative to rendering to a bitmap render target, and then reusing the bitmap contents, as allocation costs for layering are lower than for an [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span></span>

<span data-ttu-id="4dd7a-130">Les cibles de rendu peuvent créer de nouvelles cibles de rendu qui sont compatibles avec elles-mêmes, ce qui est utile pour le rendu non-écran intermédiaire tout en conservant les diverses propriétés de cible de rendu qui ont été définies sur le d’origine.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-130">Render targets can create new render targets that are compatible with themselves, which is useful for intermediate off-screen rendering while retaining the various render-target properties that were set on the original.</span></span>

<span data-ttu-id="4dd7a-131">Il est également possible d’effectuer un rendu à l’aide de GDI sur une cible de rendu Direct2D en appelant [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur une cible de rendu pour [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), qui contient des méthodes [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) et [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) qui peuvent être utilisées pour récupérer un contexte de périphérique GDI.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-131">It is also possible to render using GDI on a Direct2D render target by calling [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a render target for [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which has [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) and [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) methods on it that can be used to retrieve a GDI device context.</span></span> <span data-ttu-id="4dd7a-132">Le rendu via GDI est possible uniquement si la cible de rendu a été créée avec l’indicateur de [**\_ \_ \_ \_ \_ compatibilité GDI**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) de l’utilisation de la cible de rendu d2d1 définie.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-132">Rendering via GDI is possible only if the render target was created with the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag set.</span></span> <span data-ttu-id="4dd7a-133">Cela est utile pour les applications qui sont principalement rendues avec Direct2D, mais qui ont un modèle d’extensibilité ou tout autre contenu hérité qui requiert la possibilité d’effectuer un rendu avec GDI.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-133">This is useful for applications that are primarily rendering with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span> <span data-ttu-id="4dd7a-134">Pour plus d’informations, consultez [vue d’ensemble de l’interopérabilité Direct2D et GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4dd7a-134">For more information, see the [Direct2D and GDI Interoperation Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

### <a name="render-target-resources"></a><span data-ttu-id="4dd7a-135">Afficher les ressources cibles</span><span class="sxs-lookup"><span data-stu-id="4dd7a-135">Render Target Resources</span></span>

<span data-ttu-id="4dd7a-136">À l’instar d’une fabrique, une cible de rendu peut créer des ressources de dessin.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-136">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="4dd7a-137">Toutes les ressources créées par une cible de rendu sont des ressources dépendantes de l’appareil (tout comme la cible de rendu).</span><span class="sxs-lookup"><span data-stu-id="4dd7a-137">Any resources created by a render target are device-dependent resources (just like the render target).</span></span> <span data-ttu-id="4dd7a-138">Une cible de rendu peut créer les types de ressources suivants :</span><span class="sxs-lookup"><span data-stu-id="4dd7a-138">A render target can create the following types of resources:</span></span>

-   <span data-ttu-id="4dd7a-139">Images bitmap</span><span class="sxs-lookup"><span data-stu-id="4dd7a-139">Bitmaps</span></span>
-   <span data-ttu-id="4dd7a-140">Pinceaux</span><span class="sxs-lookup"><span data-stu-id="4dd7a-140">Brushes</span></span>
-   <span data-ttu-id="4dd7a-141">Calques</span><span class="sxs-lookup"><span data-stu-id="4dd7a-141">Layers</span></span>
-   <span data-ttu-id="4dd7a-142">Maillages</span><span class="sxs-lookup"><span data-stu-id="4dd7a-142">Meshes</span></span>

### <a name="drawing-commands"></a><span data-ttu-id="4dd7a-143">Commandes de dessin</span><span class="sxs-lookup"><span data-stu-id="4dd7a-143">Drawing Commands</span></span>

<span data-ttu-id="4dd7a-144">Pour afficher le contenu, vous utilisez les méthodes de dessin de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-144">To render content, you use the render target drawing methods.</span></span> <span data-ttu-id="4dd7a-145">Avant de commencer à dessiner, vous appelez la méthode [**ID2D1RenderTarget :: BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) .</span><span class="sxs-lookup"><span data-stu-id="4dd7a-145">Before you begin drawing, you call the [**ID2D1RenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method.</span></span> <span data-ttu-id="4dd7a-146">Une fois que vous avez terminé le dessin, vous appelez la méthode [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="4dd7a-146">After you finished drawing, you call the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="4dd7a-147">Entre ces appels, vous utilisez des méthodes de dessin et de remplissage pour restituer les ressources de dessin.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-147">Between these calls, you use Draw and Fill methods to render drawing resources.</span></span> <span data-ttu-id="4dd7a-148">La plupart des méthodes de dessin et de remplissage prennent une forme (une primitive ou une géométrie) et un pinceau pour remplir ou mettre en relief la forme.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-148">Most Draw and Fill methods take a shape (either a primitive or a geometry) and a brush for filling or outlining the shape.</span></span>

<span data-ttu-id="4dd7a-149">Les cibles de rendu fournissent des méthodes pour le découpage, l’application de masques d’opacité et la transformation de l’espace de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-149">Render targets provide methods for clipping, applying opacity masks, and transforming the coordinate space.</span></span>

<span data-ttu-id="4dd7a-150">Direct2D utilise un système de coordonnées gauche : les valeurs positives de l’axe des x continuent à droite et les valeurs positives de l’axe des y s’effectuent vers le bas.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-150">Direct2D uses a left-handed coordinate system: positive x-axis values proceed to the right and positive y-axis values proceed downward.</span></span>

### <a name="error-handling"></a><span data-ttu-id="4dd7a-151">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="4dd7a-151">Error Handling</span></span>

<span data-ttu-id="4dd7a-152">Les commandes de dessin de la cible de rendu n’indiquent pas si l’opération demandée a réussi.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-152">Render target drawing commands do not indicate whether the requested operation was successful.</span></span> <span data-ttu-id="4dd7a-153">Pour déterminer s’il existe des erreurs de dessin, appelez la méthode de [**vidage**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) de la cible de rendu ou la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) pour obtenir un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-153">To find out whether there are drawing errors, call the render target [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) method or [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method to obtain an **HRESULT**.</span></span>

## <a name="example-render-content-to-a-window"></a><span data-ttu-id="4dd7a-154">Exemple : afficher le contenu dans une fenêtre</span><span class="sxs-lookup"><span data-stu-id="4dd7a-154">Example: Render Content to a Window</span></span>

<span data-ttu-id="4dd7a-155">L’exemple suivant utilise la méthode [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) pour créer un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span><span class="sxs-lookup"><span data-stu-id="4dd7a-155">The following example uses the [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) method to create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



<span data-ttu-id="4dd7a-156">L’exemple suivant utilise le [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) pour dessiner du texte dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-156">The next example uses the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) to draw text to the window.</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



<span data-ttu-id="4dd7a-157">Le code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-157">Code has been omitted from this example.</span></span>

 

 