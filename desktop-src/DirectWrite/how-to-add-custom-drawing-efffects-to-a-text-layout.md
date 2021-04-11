---
title: Comment ajouter des effets de dessin client à une disposition de texte
description: Fournit un bref didacticiel sur l’ajout d’effets de dessin client à une application DirectWrite qui affiche du texte à l’aide de l’interface IDWriteTextLayout et d’un convertisseur de texte personnalisé.
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338dc1a720bde80c1daf2b4baf7c7a4bad6d2cff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031495"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a>Comment ajouter des effets de dessin client à une disposition de texte

Fournit un bref didacticiel sur l’ajout d’effets de dessin client à une application [DirectWrite](direct-write-portal.md) qui affiche du texte à l’aide de l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) et d’un convertisseur de texte personnalisé.

Le produit final de ce didacticiel est une application qui affiche du texte avec des plages de texte avec un effet de dessin de couleur différent sur chaque, comme illustré dans la capture d’écran suivante.

![capture d’écran de l' « exemple d’effet de dessin client ! » dans différentes couleurs](images/drawingeffects.png)

> [!Note]  
> Ce didacticiel est destiné à être un exemple simplifié de la création d’effets de dessin client personnalisés, et non d’un exemple de méthode simple pour dessiner du texte de couleur. Pour plus d’informations, consultez la page de référence de [**IDWriteTextLayout :: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) .

 

Ce didacticiel contient les éléments suivants :

-   [Étape 1 : créer une disposition de texte](#step-1-create-a-text-layout)
-   [Étape 2 : implémenter une classe d’effet de dessin personnalisée](#step-2-implement-a-custom-drawing-effect-class)
-   [Étape 3 : implémenter une classe de convertisseur de texte personnalisée](#step-3-implement-a-custom-text-renderer-class)
    -   [Le constructeur](#the-constructor)
    -   [Méthode DrawGlyphRun](#the-drawglyphrun-method)
    -   [Destructeur](#the-destructor)
-   [Étape 4 : créer le convertisseur de texte](#step-4-create-the-text-renderer)
-   [Étape 5 : instancier les objets d’effet de dessin de couleur](#step-5-instantiate-the-color-drawing-effect-objects)
-   [Étape 6 : définir l’effet de dessin pour des plages de texte spécifiques](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [Étape 7 : dessiner la disposition du texte à l’aide du convertisseur personnalisé](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [Étape 8 : nettoyer](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a>Étape 1 : créer une disposition de texte

Pour commencer, vous aurez besoin d’une application avec un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Si vous disposez déjà d’une application qui affiche du texte avec une disposition de texte ou si vous utilisez l’exemple de code DrawingEffect personnalisé, passez à l’étape 2.

Pour ajouter une disposition de texte, vous devez effectuer les opérations suivantes :

1.  Déclarez un pointeur vers une interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en tant que membre de la classe.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  À la fin de la méthode **CreateDeviceIndependentResources** , créez un objet d’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en appelant la méthode [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

3.  Enfin, n’oubliez pas de libérer la disposition du texte dans le destructeur.
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a>Étape 2 : implémenter une classe d’effet de dessin personnalisée

En dehors des méthodes héritées de IUnknown, une interface d’effet de dessin client personnalisé n’a aucune exigence quant à ce qu’elle doit implémenter. Dans ce cas, la classe **ColorDrawingEffect** contient simplement une [**valeur \_ \_ F de couleur d2d1**](../direct2d/d2d1-color-f.md) et déclare des méthodes pour obtenir et définir cette valeur, ainsi qu’un constructeur qui peut définir initialement la couleur.

Après l’application d’un effet de dessin client à une plage de texte dans un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , l’effet de dessin est passé à la méthode [**IDWriteTextRenderer ::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) de toute exécution de glyphes qui doit être rendue. Les méthodes de l’effet de dessin sont ensuite disponibles pour le convertisseur de texte.

Un effet de dessin client peut être aussi complexe que vous le souhaitez, en fournissant plus d’informations que dans cet exemple, et en fournissant des méthodes pour modifier des glyphes, créer des objets à utiliser pour le dessin, etc.

## <a name="step-3-implement-a-custom-text-renderer-class"></a>Étape 3 : implémenter une classe de convertisseur de texte personnalisée

Pour tirer parti d’un effet de dessin client, vous devez implémenter un convertisseur de texte personnalisé. Ce convertisseur de texte applique l’effet de dessin qui lui est transmis par la méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) à l’exécution du glyphe qui est tracée.

### <a name="the-constructor"></a>Le constructeur

Le constructeur pour le convertisseur de texte personnalisé stocke l’objet [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) qui sera utilisé pour créer des objets [Direct2D](../direct2d/direct2d-portal.md) , et la cible de rendu Direct2D sur laquelle le texte sera dessiné.


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
}
```



### <a name="the-drawglyphrun-method"></a>Méthode DrawGlyphRun

Une exécution de glyphe est un ensemble de glyphes qui partagent le même format, y compris l’effet de dessin client. La méthode [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) s’occupe du rendu de texte pour une exécution de glyphes spécifiée.

Tout d’abord, créez un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) et un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink), puis récupérez le plan d’exécution de glyphe à l’aide de [**IDWriteFontFace :: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline). Transformez ensuite l’origine de la géométrie à l’aide de la méthode [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory :: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) , comme indiqué dans le code suivant.


```C++
HRESULT hr = S_OK;

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

// Close the geometry sink
if (SUCCEEDED(hr))
{
    hr = pSink->Close();
}

// Initialize a matrix to translate the origin of the glyph run.
D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
    1.0f, 0.0f,
    0.0f, 1.0f,
    baselineOriginX, baselineOriginY
    );

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



Ensuite, déclarez un objet pinceau solide [Direct2D](../direct2d/direct2d-portal.md) .


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



Si le paramètre *clientDrawingEffect* n’a pas la valeur null, interrogez l’objet pour l’interface **ColorDrawingEffect** . Cela fonctionnera, car vous définirez cette classe en tant qu’effet de dessin du client sur les plages de texte de l’objet de mise en page de texte.

Une fois que vous avez un pointeur vers l’interface **ColorDrawingEffect** , vous pouvez récupérer la valeur F de la [**\_ couleur \_ d2d1**](../direct2d/d2d1-color-f.md) qu’elle stocke à l’aide de la méthode **GetColor** . Ensuite, utilisez la **\_ couleur d2d1 \_ F** pour créer un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) dans cette couleur.

Si le paramètre *clientDrawingEffect* a la **valeur null**, créez simplement un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)noir.


```C++
// If there is a drawing effect create a color brush using it, otherwise create a black brush.
if (clientDrawingEffect != NULL)
{
    // Go from IUnknown to ColorDrawingEffect.
    ColorDrawingEffect *colorDrawingEffect;

    clientDrawingEffect->QueryInterface(__uuidof(ColorDrawingEffect), reinterpret_cast<void**>(&colorDrawingEffect));

    // Get the color from the ColorDrawingEffect object.
    D2D1_COLOR_F color;

    colorDrawingEffect->GetColor(&color);

    // Create the brush using the color pecified by our ColorDrawingEffect object.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            color,
            &pBrush);
    }

    SafeRelease(&colorDrawingEffect);
}
else
{
    // Create a black brush.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            D2D1::ColorF(
            D2D1::ColorF::Black
            ),
            &pBrush);
    }
}
```



Enfin, dessinez la géométrie du contour et complétez-la à l’aide du pinceau de couleur unie que vous venez de créer.


```C++
if (SUCCEEDED(hr))
{
    // Draw the outline of the glyph run
    pRT_->DrawGeometry(
        pTransformedGeometry,
        pBrush
        );

    // Fill in the glyph run
    pRT_->FillGeometry(
        pTransformedGeometry,
        pBrush
        );
}
```



### <a name="the-destructor"></a>Destructeur

N’oubliez pas de libérer la fabrique [Direct2D](../direct2d/direct2d-portal.md) et la cible de rendu dans le destructeur.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a>Étape 4 : créer le convertisseur de texte

Dans les ressources **CreateDeviceDependent** , créez l’objet de convertisseur de texte personnalisé. Elle dépend de l’appareil, car elle utilise le **ID2D1RenderTarget**, qui est lui-même dépendant du périphérique.


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a>Étape 5 : instancier les objets d’effet de dessin de couleur

Instanciez les objets **ColorDrawingEffect** en rouge, vert et bleu.


```C++
// Instantiate some custom color drawing effects.
redDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Red
        )
    );

blueDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Blue
        )
    );

greenDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Green
        )
    );
```



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a>Étape 6 : définir l’effet de dessin pour des plages de texte spécifiques

Définissez l’effet de dessin pour des plages de texte spécifiques à l’aide de la méthode [**IDWriteTextLayou :: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) et d’un struct de [**\_ \_ plage de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) .


```C++
// Set the drawing effects.

// Red.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {0,
                                   14};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(redDrawingEffect_, textRange);
    }
}

// Blue.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {14,
                                   7};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(blueDrawingEffect_, textRange);
    }
}

// Green.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {21,
                                   8};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(greenDrawingEffect_, textRange);
    }
}
```



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a>Étape 7 : dessiner la disposition du texte à l’aide du convertisseur personnalisé

Vous devez appeler la méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) au lieu des méthodes [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) ou [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) .


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a>Étape 8 : nettoyer

Dans le destructeur DemoApp, libérez le convertisseur de texte personnalisé.


```C++
SafeRelease(&pTextRenderer_);
```



Après cela, ajoutez du code pour libérer les classes d’effet de dessin du client.


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 