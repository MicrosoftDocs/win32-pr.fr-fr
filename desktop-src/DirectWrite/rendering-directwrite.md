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
# <a name="rendering-directwrite"></a>Rendu de DirectWrite

## <a name="rendering-options"></a>Options de rendu

Le texte avec une mise en forme décrite par un seul objet [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) peut être rendu avec [Direct2D](../direct2d/direct2d-portal.md), toutefois, il existe quelques options supplémentaires pour le rendu d’un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

La chaîne décrite par un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) peut être rendue à l’aide des méthodes ci-dessous.

## <a name="1-render-using-direct2d"></a>1. rendu à l’aide de Direct2D

Pour afficher un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) à l’aide de Direct2D, utilisez la méthode [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , comme indiqué dans le code suivant.


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



Pour plus d’informations sur le dessin d’un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) à l’aide de [Direct2D](../direct2d/direct2d-portal.md), consultez [prise en main avec DirectWrite](getting-started-with-directwrite.md).

## <a name="2-render-using-a-custom-text-renderer"></a>2. effectuer un rendu à l’aide d’un convertisseur de texte personnalisé.

Vous pouvez effectuer le rendu avec un convertisseur personnalisé à l’aide de la méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , qui prend une interface de rappel dérivée de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) comme argument, comme indiqué dans le code suivant.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



La méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) appelle les méthodes du rappel de convertisseur personnalisé que vous fournissez. Les méthodes [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)et [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) effectuent les fonctions de dessin.

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) déclare des méthodes pour dessiner des objets d’exécution de glyphe, de soulignement, de barré et de ligne. C’est à l’application d’implémenter ces méthodes. La création d’un convertisseur de texte personnalisé permet à l’application d’appliquer des effets supplémentaires lors du rendu de texte, tel qu’un remplissage ou un plan personnalisé. Un exemple de convertisseur de texte personnalisé est inclus dans l' [exemple de Hello World DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="3-render-cleartype-to-a-gdi-surface"></a>3. afficher ClearType sur une surface GDI.

Le rendu sur une surface GDI est en fait un exemple d’utilisation d’un convertisseur de texte personnalisé. Toutefois, une partie du travail est effectuée pour vous sous la forme de l’interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .

Pour créer cette interface, utilisez la méthode [**IDWriteGdiInterop :: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) .

La méthode [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) de votre convertisseur de texte personnalisé appelle la méthode [**IDWriteBitmapRenderTarget ::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) pour dessiner les glyphes. Le rendu des objets souligné, barré et Inline doit être effectué par votre convertisseur personnalisé.

L’interface [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) est rendue en mémoire dans un contexte de périphérique (DC). Vous recevez un handle vers ce contrôleur de périphérique à l’aide de la méthode [**IDWriteBitmapRenderTarget :: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) .


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



Une fois le dessin effectué, le DC de mémoire de l’objet [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) doit être copié sur la surface GDI de destination.

> [!Note]  
> Vous avez également la possibilité de transférer l’image bitmap vers un autre type de surface, par exemple une surface GDI+.

 


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
> Votre application est chargée de rendre tout ce qui se passe dans la fenêtre de fin. Cela comprend le texte et les graphiques. Il y a une baisse des performances. En outre, le rendu sur un DC de mémoire n’est pas l’accélération matérielle GDI.

 

Pour obtenir une vue d’ensemble plus détaillée de l’interopérabilité avec GDI, consultez [interopérabilité avec GDI](interoperating-with-gdi.md).

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a>4. Affichez le texte en nuances de gris en toute transparence sur une surface GDI. (Windows 8 et versions ultérieures)

À partir de Windows 8, vous pouvez restituer du texte en nuances de gris de manière transparente sur une surface GDI pour de meilleures performances. Pour ce faire, vous devez :

1.  Effacez le DC de mémoire pour le rendre transparent.
2.  Restituer du texte sur la mémoire HDC en utilisant l’anticrénelage de nuances de gris (DWRITE \_ Text \_ anticrénelage \_ mode \_ nuances de gris).
3.  Utilisez la fonction [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) pour restituer la mémoire HDC en toute transparence sur le HDC cible final.
4.  Répétez cette opération autant de fois que nécessaire (par exemple une fois par exécution de glyphe) et entre d’autres graphiques peuvent être rendus directement sur le HDC cible final sans être remplacés par la fonction [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) .


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu à l’aide de Direct2D](rendering-by-using-direct2d.md)
</dt> <dt>

[Rendre en utilisant le convertisseur de texte personnalisé](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[Rendre sur une surface GDI](render-to-a-gdi-surface.md)
</dt> <dt>

[Interopérabilité avec GDI](interoperating-with-gdi.md)
</dt> </dl>

 

 