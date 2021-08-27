---
title: Rendre sur une surface GDI
description: Rendre sur une surface GDI
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20df241e379e9a133cb662ea141fa27c86a4bb486c8ffba311423cb9afd83fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048489"
---
# <a name="render-to-a-gdi-surface"></a>Rendre sur une surface GDI

Dans certains cas, vous souhaiterez peut-être afficher du texte [DirectWrite](direct-write-portal.md) sur une surface GDI. L’interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsule une bitmap et un contexte de périphérique pour le rendu du texte. Vous créez un **IDWriteBitmapRenderTarget** à l’aide de la méthode [**IDWriteGdiInterop :: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) , comme illustré dans le code suivant.


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



Pour effectuer le rendu avec un [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), vous devez implémenter une interface de rappel de convertisseur de convertisseur de texte personnalisée dérivée de l’interface [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) . Vous devez implémenter des méthodes pour dessiner une exécution de glyphes, un soulignement, un barré, des objets insérés, et ainsi de suite. Pour obtenir la liste complète des méthodes, consultez la page de référence [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) . Toutes les méthodes ne doivent pas être implémentées, elles peuvent simplement retourner **E \_ NOTIMPL** et le dessin se poursuivra.

Vous pouvez ensuite dessiner le texte à l’aide de la méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) et en passant l’interface de rappel que vous avez implémentée en tant que paramètre. La méthode **IDWriteTextLayout ::D RAW** appelle les méthodes du rappel de convertisseur personnalisé que vous fournissez. Les méthodes [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)et [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) effectuent les fonctions de dessin.

Dans votre implémentation de [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), appelez la méthode [**IDWriteBitmapRenderTarget ::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) pour dessiner les glyphes. Le rendu des objets souligné, barré et Inline doit être effectué par votre convertisseur personnalisé.

[**IDWriteBitmapRenderTarget ::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) a un paramètre rect out facultatif qui contient les limites de la zone dans laquelle le texte a été dessiné. Vous pouvez utiliser ces informations pour définir le rectangle englobant du contexte de périphérique à l’aide de la fonction [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) fournie par GDI. Le code suivant est un exemple d’implémentation de la méthode [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) d’un convertisseur personnalisé.


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



L’interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) est rendue en mémoire dans un contexte de périphérique (DC). Vous recevez un handle vers ce contrôleur de périphérique à l’aide de la méthode [**IDWriteBitmapRenderTarget :: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) . Dès que le dessin a été effectué, le DC de mémoire de l’objet **IDWriteBitmapRenderTarget** doit être copié sur la surface GDI de destination.

Vous pouvez récupérer le rectangle englobant à l’aide de la fonction [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) , puis utiliser le rectangle englobant avec la fonction [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) pour copier le texte [DirectWrite](direct-write-portal.md) rendu du DC de la mémoire vers la surface GDI, comme indiqué dans le code suivant.


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



 

 