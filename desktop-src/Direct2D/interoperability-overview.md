---
title: Vue d'ensemble de l'interopérabilité
description: Résume les différentes technologies que vous pouvez utiliser avec Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D, interopérabilité GDI
- Direct2D, interopérabilité GDI+
- Direct2D, interopérabilité
- Direct2D, interopérabilité de DirectWrite
- interopérabilité, Direct2D
- interopérabilité, Direct3D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interopérabilité, Graphics Device Interface (GDI)
- interopérabilité, GDI+
- Interopérabilité de DirectWrite
- interopérabilité, DirectWrite
- Composant Imagerie Windows (WIC)
- WIC (composant de création d’images Windows)
- interopérabilité, WIC (Windows Imaging Component)
- Direct2D, interopérabilité WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382129"
---
# <a name="interoperability-overview"></a><span data-ttu-id="50b7c-119">Vue d'ensemble de l'interopérabilité</span><span class="sxs-lookup"><span data-stu-id="50b7c-119">Interoperability Overview</span></span>

<span data-ttu-id="50b7c-120">L’une des fonctionnalités clés de Direct2d est l’activation de l’interopérabilité entre Direct2D et d’autres plateformes de rendu afin que les développeurs puissent utiliser les points forts spécifiques de chaque plateforme sans être forcés à compromettre en choisissant une plate-forme pour tous les besoins.</span><span class="sxs-lookup"><span data-stu-id="50b7c-120">One of Direct2D's key features is enabling interoperability between Direct2D and other rendering platforms so that developers can use the specific strengths of each platform without being forced into compromises by choosing one platform for all needs.</span></span> <span data-ttu-id="50b7c-121">Cette rubrique résume les différentes plateformes avec lesquelles Direct2D est interopérable.</span><span class="sxs-lookup"><span data-stu-id="50b7c-121">This topic summarizes the different platforms with which Direct2D is interoperable.</span></span> <span data-ttu-id="50b7c-122">Elle contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="50b7c-122">It contains the following sections.</span></span>

-   [<span data-ttu-id="50b7c-123">Interopérabilité GDI</span><span class="sxs-lookup"><span data-stu-id="50b7c-123">GDI Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="50b7c-124">Interopérabilité GDI+</span><span class="sxs-lookup"><span data-stu-id="50b7c-124">GDI+ Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="50b7c-125">Interopérabilité Direct3D</span><span class="sxs-lookup"><span data-stu-id="50b7c-125">Direct3D Interoperability</span></span>](#direct3d-interoperability)
-   [<span data-ttu-id="50b7c-126">Interopérabilité de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="50b7c-126">DirectWrite Interoperability</span></span>](#directwrite-interoperability)
-   [<span data-ttu-id="50b7c-127">Interopérabilité du composant WIC (Windows Imaging Component)</span><span class="sxs-lookup"><span data-stu-id="50b7c-127">Windows Imaging Component (WIC) Interoperability</span></span>](#windows-imaging-component-wic-interoperability)
-   [<span data-ttu-id="50b7c-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50b7c-128">Related topics</span></span>](#related-topics)

<span data-ttu-id="50b7c-129">Le diagramme suivant résume les différentes plateformes avec lesquelles Direct2D est interopérable et répertorie des méthodes et des interfaces qui fournissent une interopérabilité.</span><span class="sxs-lookup"><span data-stu-id="50b7c-129">The following diagram summarizes the different platforms with which Direct2D is interoperable and lists some methods and interfaces that provide interoperability.</span></span>

![diagramme des plateformes avec lesquelles Direct2D interagit, y compris Direct3D 10,1, DirectWrite, WIC, GDI+ et GDI](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a><span data-ttu-id="50b7c-131">Interopérabilité GDI</span><span class="sxs-lookup"><span data-stu-id="50b7c-131">GDI Interoperability</span></span>

<span data-ttu-id="50b7c-132">Direct2D active l’interopérabilité bidirectionnelle avec GDI.</span><span class="sxs-lookup"><span data-stu-id="50b7c-132">Direct2D enables two-way interoperability with GDI.</span></span> <span data-ttu-id="50b7c-133">Vous pouvez utiliser un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) pour écrire du contenu Direct2D dans un [contexte de périphérique](/windows/desktop/gdi/device-contexts) (DC) GDI, ou vous pouvez utiliser [**ID2D1GDIINTEROPRENDERTARGET**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) pour obtenir une représentation DC d’une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="50b7c-133">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to a GDI [device context](/windows/desktop/gdi/device-contexts) (DC), or you can use [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to obtain a DC representation of a render target.</span></span>

<span data-ttu-id="50b7c-134">Pour plus d’informations et d’exemples, consultez [vue d’ensemble de l’interopérabilité de Direct2D et GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="50b7c-134">For more information and examples, see the [Direct2D and GDI Interoperability Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="50b7c-135">Interopérabilité GDI+</span><span class="sxs-lookup"><span data-stu-id="50b7c-135">GDI+ Interoperability</span></span>

<span data-ttu-id="50b7c-136">Vous pouvez utiliser GDI+ avec Direct2D de la même manière que GDI.</span><span class="sxs-lookup"><span data-stu-id="50b7c-136">You can use GDI+ with Direct2D in the same manner as GDI.</span></span> <span data-ttu-id="50b7c-137">Vous pouvez utiliser un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) pour écrire du contenu Direct2D sur le même contrôleur de périphérique que votre contenu GDI+.</span><span class="sxs-lookup"><span data-stu-id="50b7c-137">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to the same DC as your GDI+ content.</span></span> <span data-ttu-id="50b7c-138">Cette approche vous permet de commencer à ajouter du contenu Direct2D aux applications qui sont principalement rendues à l’aide de GDI+.</span><span class="sxs-lookup"><span data-stu-id="50b7c-138">This approach enables you to start adding Direct2D content to applications that primarily render by using GDI+.</span></span>

<span data-ttu-id="50b7c-139">Vous pouvez également utiliser un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) pour fournir l’accès à un contrôleur de contexte GDI qui écrit à l’aide de Direct2D, puis utiliser la méthode [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) pour créer un objet.</span><span class="sxs-lookup"><span data-stu-id="50b7c-139">You can also use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to provide access to a GDI DC that writes by using Direct2D, and then use the [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) method to create a object.</span></span> <span data-ttu-id="50b7c-140">Cette approche est utile pour les applications qui s’affichent principalement avec Direct2D, mais qui ont un modèle d’extensibilité ou tout autre contenu hérité qui requiert la possibilité d’effectuer un rendu avec GDI+.</span><span class="sxs-lookup"><span data-stu-id="50b7c-140">This approach is useful for applications that primarily render with Direct2D, but have an extensibility model or other legacy content that requires the ability to render with GDI+.</span></span>

## <a name="direct3d-interoperability"></a><span data-ttu-id="50b7c-141">Interopérabilité Direct3D</span><span class="sxs-lookup"><span data-stu-id="50b7c-141">Direct3D Interoperability</span></span>

<span data-ttu-id="50b7c-142">Direct2D peut utiliser une cible de rendu de surface DXGI (créée par la méthode [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ) pour écrire dans un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span><span class="sxs-lookup"><span data-stu-id="50b7c-142">Direct2D can use a DXGI surface render target (created by the [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method) to write to an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span></span> <span data-ttu-id="50b7c-143">Cette action vous permet d’ajouter des interfaces et des arrière-plans 2D à des scènes 3D et d’utiliser le contenu Direct2D comme texture pour un modèle 3D.</span><span class="sxs-lookup"><span data-stu-id="50b7c-143">This action enables you to add 2-D backgrounds and interfaces to 3-D scenes and use Direct2D content as a texture for a 3-D model.</span></span> <span data-ttu-id="50b7c-144">Direct2D peut également prendre un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) et utiliser la méthode [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) pour créer une représentation bitmap.</span><span class="sxs-lookup"><span data-stu-id="50b7c-144">Direct2D can also take an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) and use the [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) method to create a bitmap representation.</span></span>

<span data-ttu-id="50b7c-145">Pour plus d’informations et d’exemples, consultez [vue d’ensemble de l’interopérabilité de Direct2D et Direct3D](direct2d-and-direct3d-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="50b7c-145">For more information and examples, see the [Direct2D and Direct3D Interoperability Overview](direct2d-and-direct3d-interoperation-overview.md).</span></span>

## <a name="directwrite-interoperability"></a><span data-ttu-id="50b7c-146">Interopérabilité de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="50b7c-146">DirectWrite Interoperability</span></span>

<span data-ttu-id="50b7c-147">Direct2D est étroitement intégré à DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="50b7c-147">Direct2D is tightly integrated with DirectWrite.</span></span> <span data-ttu-id="50b7c-148">Direct2D facilite le rendu du contenu DirectWrite en fournissant les méthodes [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)et [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="50b7c-148">Direct2D makes it easy to render DirectWrite content by providing the [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), and [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) methods.</span></span>

## <a name="windows-imaging-component-wic-interoperability"></a><span data-ttu-id="50b7c-149">Interopérabilité du composant WIC (Windows Imaging Component)</span><span class="sxs-lookup"><span data-stu-id="50b7c-149">Windows Imaging Component (WIC) Interoperability</span></span>

<span data-ttu-id="50b7c-150">Direct2D fournit les méthodes [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)et [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) pour manipuler les bitmaps WIC.</span><span class="sxs-lookup"><span data-stu-id="50b7c-150">Direct2D provides the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap), and [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) methods for manipulating WIC bitmaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50b7c-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50b7c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50b7c-152">Vue d’ensemble de l’interopérabilité de Direct2D et GDI</span><span class="sxs-lookup"><span data-stu-id="50b7c-152">Direct2D and GDI Interoperability Overview</span></span>](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[<span data-ttu-id="50b7c-153">Vue d’ensemble de l’interopérabilité entre Direct2D et Direct3D</span><span class="sxs-lookup"><span data-stu-id="50b7c-153">Direct2D and Direct3D Interoperability Overview</span></span>](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 