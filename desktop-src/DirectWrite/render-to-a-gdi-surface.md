---
title: Rendre sur une surface GDI
description: Rendre sur une surface GDI
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff292feb2250a4dd81abeb62d8ee48ebfb4488b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382695"
---
# <a name="render-to-a-gdi-surface"></a><span data-ttu-id="e61e3-103">Rendre sur une surface GDI</span><span class="sxs-lookup"><span data-stu-id="e61e3-103">Render to a GDI Surface</span></span>

<span data-ttu-id="e61e3-104">Dans certains cas, vous souhaiterez peut-être afficher du texte [DirectWrite](direct-write-portal.md) sur une surface GDI.</span><span class="sxs-lookup"><span data-stu-id="e61e3-104">In some cases, you may want to be able to display [DirectWrite](direct-write-portal.md) text on a GDI surface.</span></span> <span data-ttu-id="e61e3-105">L’interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsule une bitmap et un contexte de périphérique pour le rendu du texte.</span><span class="sxs-lookup"><span data-stu-id="e61e3-105">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface encapsulates a bitmap and device context to render text onto.</span></span> <span data-ttu-id="e61e3-106">Vous créez un **IDWriteBitmapRenderTarget** à l’aide de la méthode [**IDWriteGdiInterop :: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) , comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e61e3-106">You create an **IDWriteBitmapRenderTarget** by using the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method, as shown in the following code.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



<span data-ttu-id="e61e3-107">Pour effectuer le rendu avec un [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), vous devez implémenter une interface de rappel de convertisseur de convertisseur de texte personnalisée dérivée de l’interface [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) .</span><span class="sxs-lookup"><span data-stu-id="e61e3-107">To render with an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), you must implement a custom text renderer callback interface derived from the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) interface.</span></span> <span data-ttu-id="e61e3-108">Vous devez implémenter des méthodes pour dessiner une exécution de glyphes, un soulignement, un barré, des objets insérés, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e61e3-108">You must implement methods for drawing a glyph run, underline, strikethrough, inline objects, and so on.</span></span> <span data-ttu-id="e61e3-109">Pour obtenir la liste complète des méthodes, consultez la page de référence [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) .</span><span class="sxs-lookup"><span data-stu-id="e61e3-109">For a complete list of the methods, see the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page.</span></span> <span data-ttu-id="e61e3-110">Toutes les méthodes ne doivent pas être implémentées, elles peuvent simplement retourner **E \_ NOTIMPL** et le dessin se poursuivra.</span><span class="sxs-lookup"><span data-stu-id="e61e3-110">Not every method must be implemented, they can just return **E\_NOTIMPL**, and drawing will continue.</span></span>

<span data-ttu-id="e61e3-111">Vous pouvez ensuite dessiner le texte à l’aide de la méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) et en passant l’interface de rappel que vous avez implémentée en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="e61e3-111">You can then draw the text by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method and passing the callback interface that you implemented as a parameter.</span></span> <span data-ttu-id="e61e3-112">La méthode **IDWriteTextLayout ::D RAW** appelle les méthodes du rappel de convertisseur personnalisé que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="e61e3-112">The **IDWriteTextLayout::Draw** method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="e61e3-113">Les méthodes [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)et [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) effectuent les fonctions de dessin.</span><span class="sxs-lookup"><span data-stu-id="e61e3-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="e61e3-114">Dans votre implémentation de [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), appelez la méthode [**IDWriteBitmapRenderTarget ::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) pour dessiner les glyphes.</span><span class="sxs-lookup"><span data-stu-id="e61e3-114">In your implementation of [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), call the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="e61e3-115">Le rendu des objets souligné, barré et Inline doit être effectué par votre convertisseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e61e3-115">The rendering of the underline, strikethrough and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="e61e3-116">[**IDWriteBitmapRenderTarget ::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) a un paramètre rect out facultatif qui contient les limites de la zone dans laquelle le texte a été dessiné.</span><span class="sxs-lookup"><span data-stu-id="e61e3-116">[**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) has an optional RECT out parameter that contains the bounds of the area where the text was drawn.</span></span> <span data-ttu-id="e61e3-117">Vous pouvez utiliser ces informations pour définir le rectangle englobant du contexte de périphérique à l’aide de la fonction [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) fournie par GDI.</span><span class="sxs-lookup"><span data-stu-id="e61e3-117">You can use this information to set the bounding rectangle for the device context with the [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) function that is provided by GDI.</span></span> <span data-ttu-id="e61e3-118">Le code suivant est un exemple d’implémentation de la méthode [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) d’un convertisseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e61e3-118">The following code is an example implementation of the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of a custom renderer.</span></span>


```C++
STDMETHODIMP GdiTextRenderer::DrawGlyphRun(
    __maybenull void* clientDrawingContext,
    FLOAT baselineOriginX,
    FLOAT baselineOriginY,
    DWRITE_MEASURING_MODE measuringMode,
    __in DWRITE_GLYPH_RUN const* glyphRun,
    __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
    IUnknown* clientDrawingEffect
    )
{
    HRESULT hr = S_OK;

    // Pass on the drawing call to the render target to do the real work.
    RECT dirtyRect = {0};

    hr = pRenderTarget_->DrawGlyphRun(
        baselineOriginX,
        baselineOriginY,
        measuringMode,
        glyphRun,
        pRenderingParams_,
        RGB(0,200,255),
        &dirtyRect
        );
    

    return hr;
}
```



<span data-ttu-id="e61e3-119">L’interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) est rendue en mémoire dans un contexte de périphérique (DC).</span><span class="sxs-lookup"><span data-stu-id="e61e3-119">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="e61e3-120">Vous recevez un handle vers ce contrôleur de périphérique à l’aide de la méthode [**IDWriteBitmapRenderTarget :: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .</span><span class="sxs-lookup"><span data-stu-id="e61e3-120">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span> <span data-ttu-id="e61e3-121">Dès que le dessin a été effectué, le DC de mémoire de l’objet **IDWriteBitmapRenderTarget** doit être copié sur la surface GDI de destination.</span><span class="sxs-lookup"><span data-stu-id="e61e3-121">As soon as the drawing has been performed, the memory DC of the **IDWriteBitmapRenderTarget** object must be copied to the destination GDI surface.</span></span>

<span data-ttu-id="e61e3-122">Vous pouvez récupérer le rectangle englobant à l’aide de la fonction [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) , puis utiliser le rectangle englobant avec la fonction [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) pour copier le texte [DirectWrite](direct-write-portal.md) rendu du DC de la mémoire vers la surface GDI, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e61e3-122">You can retrieve the bounding rectangle by using the [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) function, then use the bounding rectangle with the [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) function to copy the rendered [DirectWrite](direct-write-portal.md) text from the memory DC to the GDI surface as shown in the following code.</span></span>


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



 

 