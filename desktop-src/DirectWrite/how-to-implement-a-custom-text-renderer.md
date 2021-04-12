---
title: Rendre en utilisant le convertisseur de texte personnalisé
description: Une disposition de texte DirectWrite \ 160 ; peut être dessinée par un convertisseur de texte personnalisé dérivé de IDWriteTextRenderer.
ms.assetid: a5b09733-24b2-408e-a1f9-cf7ad20c5c63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cda56fc5cc38a62e48a2f62066edfec2327e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382240"
---
# <a name="render-using-a-custom-text-renderer"></a>Rendre en utilisant le convertisseur de texte personnalisé

Une [](direct-write-portal.md) [**disposition de texte**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) DirectWrite peut être dessinée par un convertisseur de texte personnalisé dérivé de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer). Un convertisseur personnalisé est nécessaire pour tirer parti de certaines fonctionnalités avancées de DirectWrite, telles que le rendu sur une surface bitmap ou GDI, les objets inline et les effets de dessin client. Ce didacticiel décrit les méthodes de **IDWriteTextRenderer** et fournit un exemple d’implémentation qui utilise [Direct2D](../direct2d/direct2d-portal.md) pour restituer le texte avec un remplissage bitmap.

Ce didacticiel contient les éléments suivants :

-   [Le constructeur](#the-constructor)
-   [DrawGlyphRun ()](#drawglyphrun)
-   [DrawUnderline () et DrawStrikethrough ()](#drawunderline-and-drawstrikethrough)
-   [Accrochage des pixels, pixels par DIP et transformation](#pixel-snapping-pixels-per-dip-and-transform)
    -   [IsPixelSnappingDisabled()](#ispixelsnappingdisabled)
    -   [GetCurrentTransform()](#getcurrenttransform)
    -   [GetPixelsPerDip()](#getpixelsperdip)
-   [DrawInlineObject()](#drawinlineobject)
-   [Destructeur](#the-destructor)
-   [Utilisation du convertisseur de texte personnalisé](#using-the-custom-text-renderer)

Votre convertisseur de texte personnalisé doit implémenter les méthodes héritées de IUnknown en plus des méthodes listées dans la page de référence [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) et ci-dessous.

Pour obtenir le code source complet du convertisseur de texte personnalisé, consultez les fichiers CustomTextRenderer. cpp et CustomTextRenderer. h de l' [exemple DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="the-constructor"></a>Le constructeur

Votre convertisseur de texte personnalisé aura besoin d’un constructeur. Cet exemple utilise à la fois des pinceaux et des pinceaux [Direct2D](../direct2d/direct2d-portal.md) solides et bitmap pour restituer le texte.

Pour cette raison, le constructeur prend les paramètres figurant dans le tableau ci-dessous avec les descriptions.



| Paramètre       | Description                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *pD2DFactory*   | Pointeur vers un objet [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) qui sera utilisé pour créer toutes les ressources Direct2D nécessaires.                                                                                                        |
| *pRT*           | Pointeur vers l’objet [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) dans lequel le texte sera restitué. |
| *pOutlineBrush* | Pointeur vers le [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) qui sera utilisé pour dessiner le contour du texte                                                                                                                     |
| *pFillBrush*    | Pointeur vers le [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) qui sera utilisé pour remplir le texte.                                                                                                                                      |



 

Celles-ci seront stockées par le constructeur comme indiqué dans le code suivant.


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT, 
    ID2D1SolidColorBrush* pOutlineBrush, 
    ID2D1BitmapBrush* pFillBrush
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT), 
pOutlineBrush_(pOutlineBrush), 
pFillBrush_(pFillBrush)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
    pOutlineBrush_->AddRef();
    pFillBrush_->AddRef();
}
```



## <a name="drawglyphrun"></a>DrawGlyphRun ()

La méthode [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) est la méthode de rappel principale du convertisseur de texte. Une série de glyphes est passée pour être rendue en plus des informations telles que l’origine de la ligne de base et le mode de mesure. Il passe également un objet d’effet de dessin client à appliquer à l’exécution du glyphe. Pour plus d’informations, consultez la rubrique [comment ajouter des effets de dessin client à une disposition de texte](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .

Cette implémentation de convertisseur de texte affiche les exécutions de glyphe en les convertissant en géométries [Direct2D](rendering-by-using-direct2d.md) , puis en dessinant et remplissant les géométries. Cela comprend les étapes suivantes.

1.  Créez un objet [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) , puis récupérez l’objet [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) à l’aide de la méthode [**ID2D1PathGeometry :: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .

    ```C++
    // Create the path geometry.
    ID2D1PathGeometry* pPathGeometry = NULL;
    hr = pD2DFactory_->CreatePathGeometry(
            &pPathGeometry
            );

    // Write to the path geometry using the geometry sink.
    ID2D1GeometrySink* pSink = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Open(
            &pSink
            );
    }
    ```

    

2.  L' [**\_ \_ exécution de glyphes DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) transmise à [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contient un objet [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , nommé *fontFace*, qui représente le type de police pour l’exécution de glyphe entière. Placez le contour du glyphe dans le récepteur Geometry à l’aide de la méthode [**IDWriteFontFace :: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , comme indiqué dans le code suivant.

    ```C++
    // Get the glyph run outline geometries back from DirectWrite and place them within the
    // geometry sink.
    if (SUCCEEDED(hr))
    {
        hr = glyphRun->fontFace->GetGlyphRunOutline(
            glyphRun->fontEmSize,
            glyphRun->glyphIndices,
            glyphRun->glyphAdvances,
            glyphRun->glyphOffsets,
            glyphRun->glyphCount,
            glyphRun->isSideways,
            glyphRun->bidiLevel%2,
            pSink
            );
    }
    ```

    

3.  Après avoir rempli le récepteur de géométrie, fermez-le.

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  L’origine de l’exécution du glyphe doit être traduite afin d’être rendue à partir de l’origine de la ligne de base correcte, comme indiqué dans le code suivant.

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    *BaselineOriginX* et *baselineOriginY* sont passés comme paramètres à la méthode de rappel [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .

5.  Créez la géométrie transformée à l’aide de la méthode [**ID2D1Factory :: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) et en passant la géométrie du tracé et la matrice de translation.

    ```C++
    // Create the transformed geometry
    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pPathGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

6.  Enfin, dessinez le contour de la géométrie transformée et remplissez-le à l’aide des méthodes [**ID2D1RenderTarget ::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) et [**ID2D1RenderTarget :: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) et des pinceaux [Direct2D](../direct2d/direct2d-portal.md) stockés en tant que variables membres.

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

7.  Maintenant que vous avez terminé le dessin, n’oubliez pas de nettoyer les objets qui ont été créés dans cette méthode.

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a>DrawUnderline () et DrawStrikethrough ()

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) a également des rappels pour dessiner le trait de soulignement et le barré. Cet exemple dessine un rectangle simple pour un trait de soulignement ou barré, mais d’autres formes peuvent être dessinées.

Le fait de dessiner un soulignement à l’aide de [Direct2D](../direct2d/direct2d-portal.md) comprend les étapes suivantes.

1.  Tout d’abord, créez une structure [**d2d1 \_ rect \_ F**](../direct2d/d2d1-rect-f.md) de la taille et de la forme du soulignement. La structure de [**\_ soulignement DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) transmise à la méthode de rappel [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) fournit le décalage, la largeur et l’épaisseur du soulignement.

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  Ensuite, créez un objet [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) à l’aide de la méthode [**ID2D1Factory :: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) et de la structure [**d2d1 \_ rect \_ F**](../direct2d/d2d1-rect-f.md) initialisée.

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  Comme pour l’exécution de glyphes, l’origine de la géométrie du soulignement doit être traduite en fonction des valeurs d’origine de la ligne de base, à l’aide de la méthode [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) .

    ```C++
    // Initialize a matrix to translate the origin of the underline
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );

    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pRectangleGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

4.  Enfin, dessinez le contour de la géométrie transformée et remplissez-le à l’aide des méthodes [**ID2D1RenderTarget ::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) et [**ID2D1RenderTarget :: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) et des pinceaux [Direct2D](../direct2d/direct2d-portal.md) stockés en tant que variables membres.

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

5.  Maintenant que vous avez terminé le dessin, n’oubliez pas de nettoyer les objets qui ont été créés dans cette méthode.

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

Le processus de dessin d’un barré est le même. Toutefois, le barré aura un décalage différent et probablement une largeur et une épaisseur différentes.

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a>Accrochage des pixels, pixels par DIP et transformation

### <a name="ispixelsnappingdisabled"></a>IsPixelSnappingDisabled()

Cette méthode est appelée pour déterminer si l’alignement des pixels est désactivé. La valeur par défaut recommandée est **false**, ce qui correspond à la sortie de cet exemple.


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a>GetCurrentTransform()

Cet exemple effectue un rendu sur une cible de rendu Direct2D. par conséquent, transférez la transformation à partir de la cible de rendu à l’aide de [**ID2D1RenderTarget :: GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a>GetPixelsPerDip()

Cette méthode est appelée pour récupérer le nombre de pixels par DIP (Device Independent Pixel).


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a>DrawInlineObject()

Un convertisseur de texte personnalisé a également un rappel pour dessiner des objets insérés. Dans cet exemple, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) retourne E \_ NOTIMPL. Ce didacticiel présente en outre une explication sur la façon de dessiner des objets en ligne. Pour plus d’informations, consultez la rubrique [comment ajouter des objets Inline à une disposition de texte](how-to-add-inline-objects-to-a-text-layout.md) .

## <a name="the-destructor"></a>Destructeur

Il est important de libérer tous les pointeurs utilisés par la classe de convertisseur de texte personnalisée.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a>Utilisation du convertisseur de texte personnalisé

Vous le rendez avec le convertisseur personnalisé à l’aide de la méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , qui prend une interface de rappel dérivée de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) comme argument, comme indiqué dans le code suivant.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



La méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) appelle les méthodes du rappel de convertisseur personnalisé que vous fournissez. Les méthodes [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)et [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) décrites ci-dessus effectuent les fonctions de dessin.

 

 