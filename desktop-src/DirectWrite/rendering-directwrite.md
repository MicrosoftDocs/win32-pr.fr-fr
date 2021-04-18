---
title: Rendu de DirectWrite
description: Rendu de DirectWrite
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7012bc4861a8befc9beb97c945dc0b03b4e761
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382265"
---
# <a name="rendering-directwrite"></a><span data-ttu-id="251ce-103">Rendu de DirectWrite</span><span class="sxs-lookup"><span data-stu-id="251ce-103">Rendering DirectWrite</span></span>

## <a name="rendering-options"></a><span data-ttu-id="251ce-104">Options de rendu</span><span class="sxs-lookup"><span data-stu-id="251ce-104">Rendering Options</span></span>

<span data-ttu-id="251ce-105">Le texte avec une mise en forme décrite par un seul objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) peut être rendu avec [Direct2D](../direct2d/direct2d-portal.md), toutefois, il existe quelques options supplémentaires pour le rendu d’un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="251ce-105">Text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="251ce-106">La chaîne décrite par un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) peut être rendue à l’aide des méthodes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="251ce-106">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

## <a name="1-render-using-direct2d"></a><span data-ttu-id="251ce-107">1. rendu à l’aide de Direct2D</span><span class="sxs-lookup"><span data-stu-id="251ce-107">1. Render using Direct2D</span></span>

<span data-ttu-id="251ce-108">Pour afficher un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) à l’aide de Direct2D, utilisez la méthode [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="251ce-108">To render an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using Direct2D, use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, as shown in the following code.</span></span>


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



<span data-ttu-id="251ce-109">Pour plus d’informations sur le dessin d’un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) à l’aide de [Direct2D](../direct2d/direct2d-portal.md), consultez [prise en main avec DirectWrite](getting-started-with-directwrite.md).</span><span class="sxs-lookup"><span data-stu-id="251ce-109">For a more in depth look at drawing an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using [Direct2D](../direct2d/direct2d-portal.md), see [Getting Started with DirectWrite](getting-started-with-directwrite.md).</span></span>

## <a name="2-render-using-a-custom-text-renderer"></a><span data-ttu-id="251ce-110">2. effectuer un rendu à l’aide d’un convertisseur de texte personnalisé.</span><span class="sxs-lookup"><span data-stu-id="251ce-110">2. Render using a custom text renderer.</span></span>

<span data-ttu-id="251ce-111">Vous pouvez effectuer le rendu avec un convertisseur personnalisé à l’aide de la méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , qui prend une interface de rappel dérivée de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) comme argument, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="251ce-111">You render with a custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="251ce-112">La méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) appelle les méthodes du rappel de convertisseur personnalisé que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="251ce-112">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="251ce-113">Les méthodes [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)et [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) effectuent les fonctions de dessin.</span><span class="sxs-lookup"><span data-stu-id="251ce-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="251ce-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) déclare des méthodes pour dessiner des objets d’exécution de glyphe, de soulignement, de barré et de ligne.</span><span class="sxs-lookup"><span data-stu-id="251ce-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declares methods for drawing a glyph run, underline, strikethrough, and inline objects.</span></span> <span data-ttu-id="251ce-115">C’est à l’application d’implémenter ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="251ce-115">It is up to the application to implement these methods.</span></span> <span data-ttu-id="251ce-116">La création d’un convertisseur de texte personnalisé permet à l’application d’appliquer des effets supplémentaires lors du rendu de texte, tel qu’un remplissage ou un plan personnalisé.</span><span class="sxs-lookup"><span data-stu-id="251ce-116">Creating a custom text renderer allows the application to apply additional effects when rendering text, such as a custom fill or outline.</span></span> <span data-ttu-id="251ce-117">Un exemple de convertisseur de texte personnalisé est inclus dans l' [exemple de Hello World DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="251ce-117">A sample custom text renderer is included in the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="3-render-cleartype-to-a-gdi-surface"></a><span data-ttu-id="251ce-118">3. afficher ClearType sur une surface GDI.</span><span class="sxs-lookup"><span data-stu-id="251ce-118">3. Render ClearType to a GDI surface.</span></span>

<span data-ttu-id="251ce-119">Le rendu sur une surface GDI est en fait un exemple d’utilisation d’un convertisseur de texte personnalisé.</span><span class="sxs-lookup"><span data-stu-id="251ce-119">Rendering to a GDI surface is actually an example of using a custom text renderer.</span></span> <span data-ttu-id="251ce-120">Toutefois, une partie du travail est effectuée pour vous sous la forme de l’interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="251ce-120">However, some of the work is done for you in the form of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface.</span></span>

<span data-ttu-id="251ce-121">Pour créer cette interface, utilisez la méthode [**IDWriteGdiInterop :: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="251ce-121">To create this interface, use the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method.</span></span>

<span data-ttu-id="251ce-122">La méthode [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) de votre convertisseur de texte personnalisé appelle la méthode [**IDWriteBitmapRenderTarget ::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) pour dessiner les glyphes.</span><span class="sxs-lookup"><span data-stu-id="251ce-122">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of your custom text renderer calls the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="251ce-123">Le rendu des objets souligné, barré et Inline doit être effectué par votre convertisseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="251ce-123">The rendering of the underline, strikethrough, and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="251ce-124">L’interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) est rendue en mémoire dans un contexte de périphérique (DC).</span><span class="sxs-lookup"><span data-stu-id="251ce-124">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="251ce-125">Vous recevez un handle vers ce contrôleur de périphérique à l’aide de la méthode [**IDWriteBitmapRenderTarget :: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .</span><span class="sxs-lookup"><span data-stu-id="251ce-125">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span>


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



<span data-ttu-id="251ce-126">Une fois le dessin effectué, le DC de mémoire de l’objet [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) doit être copié sur la surface GDI de destination.</span><span class="sxs-lookup"><span data-stu-id="251ce-126">Once the drawing has been performed, the memory DC of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object must be copied to the destination GDI surface.</span></span>

> [!Note]  
> <span data-ttu-id="251ce-127">Vous avez également la possibilité de transférer l’image bitmap vers un autre type de surface, par exemple une surface GDI+.</span><span class="sxs-lookup"><span data-stu-id="251ce-127">You also have the option of transferring the bitmap to another type of surface, such as a GDI+ surface.</span></span>

 


```C++
// Transfer from DWrite's rendering target to the window.
BitBlt(
    hdc,
    0, 0,
    size.cx, size.cy,
    memoryHdc,
    0, 0, 
    SRCCOPY | NOMIRRORBITMAP
    );
```



> [!Note]  
> <span data-ttu-id="251ce-128">Votre application est chargée de rendre tout ce qui se passe dans la fenêtre de fin.</span><span class="sxs-lookup"><span data-stu-id="251ce-128">Your app has the responsibility to render everything to the window in the end.</span></span> <span data-ttu-id="251ce-129">Cela comprend le texte et les graphiques.</span><span class="sxs-lookup"><span data-stu-id="251ce-129">This includes text and graphics.</span></span> <span data-ttu-id="251ce-130">Il y a une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="251ce-130">There is a performance penalty to this.</span></span> <span data-ttu-id="251ce-131">En outre, le rendu sur un DC de mémoire n’est pas l’accélération matérielle GDI.</span><span class="sxs-lookup"><span data-stu-id="251ce-131">Additionally, rendering to a memory DC is not GDI hardware accelerated.</span></span>

 

<span data-ttu-id="251ce-132">Pour obtenir une vue d’ensemble plus détaillée de l’interopérabilité avec GDI, consultez [interopérabilité avec GDI](interoperating-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="251ce-132">For a more detailed overview of interoperating with GDI see [Interoperating with GDI](interoperating-with-gdi.md).</span></span>

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a><span data-ttu-id="251ce-133">4. Affichez le texte en nuances de gris en toute transparence sur une surface GDI.</span><span class="sxs-lookup"><span data-stu-id="251ce-133">4. Render Grayscale Text Transparently to a GDI Surface.</span></span> <span data-ttu-id="251ce-134">(Windows 8 et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="251ce-134">(Windows 8 and later)</span></span>

<span data-ttu-id="251ce-135">À partir de Windows 8, vous pouvez restituer du texte en nuances de gris de manière transparente sur une surface GDI pour de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="251ce-135">Starting in Windows 8, you can render grayscale text transparently to a GDI surface for better performance.</span></span> <span data-ttu-id="251ce-136">Pour ce faire, vous devez :</span><span class="sxs-lookup"><span data-stu-id="251ce-136">To do this you need to:</span></span>

1.  <span data-ttu-id="251ce-137">Effacez le DC de mémoire pour le rendre transparent.</span><span class="sxs-lookup"><span data-stu-id="251ce-137">Clear the memory DC to transparent.</span></span>
2.  <span data-ttu-id="251ce-138">Restituer du texte sur la mémoire HDC en utilisant l’anticrénelage de nuances de gris (DWRITE \_ Text \_ anticrénelage \_ mode \_ nuances de gris).</span><span class="sxs-lookup"><span data-stu-id="251ce-138">Render text to the memory HDC using grayscale antialiasing (DWRITE\_TEXT\_ANTIALIAS\_MODE\_GRAYSCALE).</span></span>
3.  <span data-ttu-id="251ce-139">Utilisez la fonction [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) pour restituer la mémoire HDC en toute transparence sur le HDC cible final.</span><span class="sxs-lookup"><span data-stu-id="251ce-139">Use the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function to render the memory HDC transparently on top of the final target HDC.</span></span>
4.  <span data-ttu-id="251ce-140">Répétez cette opération autant de fois que nécessaire (par exemple une fois par exécution de glyphe) et entre d’autres graphiques peuvent être rendus directement sur le HDC cible final sans être remplacés par la fonction [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .</span><span class="sxs-lookup"><span data-stu-id="251ce-140">Repeat as many times as necessary (say, once per glyph run) and in between other graphics may be rendered directly to the final target HDC without being overwritten by the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>


```C++
pRT_->SetTextAntialiasMode(DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE);

pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

BLENDFUNCTION blendFunction = { 0 };  
blendFunction.BlendOp = AC_SRC_OVER;  
blendFunction.SourceConstantAlpha = 255;  
blendFunction.AlphaFormat = AC_SRC_ALPHA;

AlphaBlend(  
        hdc,  
        0, 0,  
        width, height,  
        pRT_->GetMemoryDC(),  
        0, 0,  
        width, height,  
        blendFunction  
        );

```



## <a name="related-topics"></a><span data-ttu-id="251ce-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="251ce-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="251ce-142">Rendu à l’aide de Direct2D</span><span class="sxs-lookup"><span data-stu-id="251ce-142">Render Using Direct2D</span></span>](rendering-by-using-direct2d.md)
</dt> <dt>

[<span data-ttu-id="251ce-143">Rendre en utilisant le convertisseur de texte personnalisé</span><span class="sxs-lookup"><span data-stu-id="251ce-143">Render Using a Custom Text Renderer</span></span>](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[<span data-ttu-id="251ce-144">Rendre sur une surface GDI</span><span class="sxs-lookup"><span data-stu-id="251ce-144">Render to a GDI surface</span></span>](render-to-a-gdi-surface.md)
</dt> <dt>

[<span data-ttu-id="251ce-145">Interopérabilité avec GDI</span><span class="sxs-lookup"><span data-stu-id="251ce-145">Interoperating with GDI</span></span>](interoperating-with-gdi.md)
</dt> </dl>

 

 