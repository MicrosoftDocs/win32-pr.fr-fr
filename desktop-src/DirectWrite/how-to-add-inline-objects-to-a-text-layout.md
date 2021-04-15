---
title: Comment ajouter des objets intralignes à une disposition de texte
description: Fournit un bref didacticiel sur l’ajout d’objets en ligne à une application DirectWrite qui affiche du texte à l’aide de l’interface IDWriteTextLayout.
ms.assetid: 6aa9d17c-ee30-497f-9c73-ec2fa079222b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d9ef34e38ec9b84afd887e565e76efb9618b88
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104569352"
---
# <a name="how-to-add-inline-objects-to-a-text-layout"></a>Comment ajouter des objets intralignes à une disposition de texte

Fournit un bref didacticiel sur l’ajout d’objets en ligne à une application [DirectWrite](direct-write-portal.md) qui affiche du texte à l’aide de l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Le produit final de ce didacticiel est une application qui affiche du texte avec une image incluse incorporée, comme illustré dans la capture d’écran suivante.

![capture d’écran d’un « exemple d’objet Inline » avec une image incorporée](images/inlineobject.png)

Ce didacticiel contient les éléments suivants :

-   [Étape 1 : créer une disposition de texte.](#step-1-create-a-text-layout)
-   [Étape 2 : définissez une classe dérivée de l’interface IDWriteInlineObject.](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [Étape 3 : implémenter la classe d’objet Inline.](#step-3-implement-the-inline-object-class)
    -   [Constructeur.](#the-constructor)
    -   [Méthode Draw.](#the-draw-method)
    -   [Méthode GetMetrics.](#the-getmetrics-method)
    -   [Méthode GetOverhangMetrics.](#the-getoverhangmetrics-method)
    -   [Méthode GetBreakConditions.](#the-getbreakconditions-method)
-   [Étape 4 : créez une instance de la classe InlineImage et ajoutez-la à la disposition du texte.](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a>Étape 1 : créer une disposition de texte.

Pour commencer, vous aurez besoin d’une application avec un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Si vous disposez déjà d’une application qui affiche du texte avec une disposition de texte, passez à l’étape 2.

Pour ajouter une disposition de texte, vous devez effectuer les opérations suivantes :

1.  Déclarez un pointeur vers une interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en tant que membre de la classe.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  À la fin de la méthode CreateDeviceIndependentResources, créez un objet d’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en appelant la méthode [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .
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

    

3.  Ensuite, vous devez remplacer l’appel à la méthode [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) par [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), comme indiqué dans le code suivant.
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a>Étape 2 : définissez une classe dérivée de l’interface IDWriteInlineObject.

La prise en charge des objets inline dans [DirectWrite](direct-write-portal.md) est assurée par l’interface [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) . Pour utiliser des objets Inline, vous devez implémenter cette interface. Il gère le dessin de l’objet Inline, ainsi que la fourniture de métriques et d’autres informations au convertisseur.

Créez un nouveau fichier d’en-tête et déclarez une interface appelée InlineImage, dérivée de [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).

En plus de QueryInterface, AddRef et Release hérités de IUnknown, cette classe doit avoir les méthodes suivantes :

-   [**Dessin**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md)
-   [**GetBreakConditions**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a>Étape 3 : implémenter la classe d’objet Inline.

Créez un nouveau fichier C++, nommé InlineImage. cpp, pour l’implémentation de la classe. En plus de la méthode LoadBitmapFromFile et des méthodes héritées de l’interface IUnknown, la classe InlineImage est constituée des méthodes suivantes.

### <a name="the-constructor"></a>Constructeur.


```C++
InlineImage::InlineImage(
    ID2D1RenderTarget *pRenderTarget, 
    IWICImagingFactory *pIWICFactory,
    PCWSTR uri
    )
{
    // Save the render target for later.
    pRT_ = pRenderTarget;

    pRT_->AddRef();

    // Load the bitmap from a file.
    LoadBitmapFromFile(
        pRenderTarget,
        pIWICFactory,
        uri,
        &pBitmap_
        );
}
```



Le premier argument du constructeur est le ID2D1RenderTarget dans lequel l’image Inline sera restituée. Il est stocké pour une utilisation ultérieure lors du dessin.

La cible de rendu, IWICImagingFactory et l’URI de nom de fichier sont tous passés à la méthode LoadBitmapFromFile qui charge le bitmap et stocke la taille de la bitmap (largeur et hauteur) dans la \_ variable de membre Rect.

### <a name="the-draw-method"></a>Méthode Draw.

La méthode [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) est un rappel qui est appelé par l’objet [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) lorsque l’objet Inline doit être dessiné. La disposition du texte n’appelle pas cette méthode directement.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::Draw(
    __maybenull void* clientDrawingContext,
    IDWriteTextRenderer* renderer,
    FLOAT originX,
    FLOAT originY,
    BOOL isSideways,
    BOOL isRightToLeft,
    IUnknown* clientDrawingEffect
    )
{
    float height    = rect_.bottom - rect_.top;
    float width     = rect_.right  - rect_.left;
    D2D1_RECT_F destRect  = {originX, originY, originX + width, originY + height};

    pRT_->DrawBitmap(pBitmap_, destRect);

    return S_OK;
}
```



Dans ce cas, le dessin de l’image bitmap s’effectue à l’aide de la méthode [**ID2D1RenderTarget ::D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) ; Toutefois, vous pouvez utiliser n’importe quelle méthode de dessin.

### <a name="the-getmetrics-method"></a>Méthode GetMetrics.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetMetrics(
    __out DWRITE_INLINE_OBJECT_METRICS* metrics
    )
{
    DWRITE_INLINE_OBJECT_METRICS inlineMetrics = {};
    inlineMetrics.width     = rect_.right  - rect_.left;
    inlineMetrics.height    = rect_.bottom - rect_.top;
    inlineMetrics.baseline  = baseline_;
    *metrics = inlineMetrics;
    return S_OK;
}
```



Pour la méthode [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) , stockez la largeur, la hauteur et la ligne de base dans une structure de [**\_ \_ \_ métriques d’objets Inline DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) . [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) appelle cette fonction de rappel pour récupérer la mesure de l’objet Inline.

### <a name="the-getoverhangmetrics-method"></a>Méthode GetOverhangMetrics.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetOverhangMetrics(
    __out DWRITE_OVERHANG_METRICS* overhangs
    )
{
    overhangs->left      = 0;
    overhangs->top       = 0;
    overhangs->right     = 0;
    overhangs->bottom    = 0;
    return S_OK;
}
```



Dans ce cas, aucun dépassement n’est nécessaire, de sorte que la méthode [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) retourne tous les zéros.

### <a name="the-getbreakconditions-method"></a>Méthode GetBreakConditions.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetBreakConditions(
    __out DWRITE_BREAK_CONDITION* breakConditionBefore,
    __out DWRITE_BREAK_CONDITION* breakConditionAfter
    )
{
    *breakConditionBefore = DWRITE_BREAK_CONDITION_NEUTRAL;
    *breakConditionAfter  = DWRITE_BREAK_CONDITION_NEUTRAL;
    return S_OK;
}
```



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a>Étape 4 : créez une instance de la classe InlineImage et ajoutez-la à la disposition du texte.

Enfin, dans la méthode CreateDeviceDependentResources, créez une instance de la classe InlineImage et ajoutez-la à la disposition du texte. Étant donné qu’il contient une référence à [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), qui est une ressource dépendante de l’appareil, et que le [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) est créé à l’aide de la cible de rendu, le InlineImage est également dépendant du périphérique et doit être recréé si la cible de rendu est recréée.


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



La méthode [**IDWriteTextLayout :: SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) prend une structure de plage de texte. L’objet s’applique à la plage spécifiée ici, et tout texte de la plage sera supprimé. Si la longueur de la plage de texte est 0, l’objet ne sera pas dessiné.

Dans cet exemple, il y a un astérisque ( \* ) comme espace réservé à l’emplacement où l’image sera affichée.


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



Étant donné que la classe InlineImage dépend du [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), vous devez la libérer quand vous libérez la cible de rendu.


```C++
SafeRelease(&pInlineImage_);
```



 

 