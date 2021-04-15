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
# <a name="how-to-add-inline-objects-to-a-text-layout"></a><span data-ttu-id="d4c54-103">Comment ajouter des objets intralignes à une disposition de texte</span><span class="sxs-lookup"><span data-stu-id="d4c54-103">How to Add Inline Objects to a Text Layout</span></span>

<span data-ttu-id="d4c54-104">Fournit un bref didacticiel sur l’ajout d’objets en ligne à une application [DirectWrite](direct-write-portal.md) qui affiche du texte à l’aide de l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="d4c54-104">Provides a short tutorial on adding inline objects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="d4c54-105">Le produit final de ce didacticiel est une application qui affiche du texte avec une image incluse incorporée, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="d4c54-105">The end product of this tutorial is an application that displays text with an inline image embedded in it, as shown in the following screen shot.</span></span>

![capture d’écran d’un « exemple d’objet Inline » avec une image incorporée](images/inlineobject.png)

<span data-ttu-id="d4c54-107">Ce didacticiel contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d4c54-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="d4c54-108">Étape 1 : créer une disposition de texte.</span><span class="sxs-lookup"><span data-stu-id="d4c54-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="d4c54-109">Étape 2 : définissez une classe dérivée de l’interface IDWriteInlineObject.</span><span class="sxs-lookup"><span data-stu-id="d4c54-109">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [<span data-ttu-id="d4c54-110">Étape 3 : implémenter la classe d’objet Inline.</span><span class="sxs-lookup"><span data-stu-id="d4c54-110">Step 3: Implement the Inline Object Class.</span></span>](#step-3-implement-the-inline-object-class)
    -   [<span data-ttu-id="d4c54-111">Constructeur.</span><span class="sxs-lookup"><span data-stu-id="d4c54-111">The Constructor.</span></span>](#the-constructor)
    -   [<span data-ttu-id="d4c54-112">Méthode Draw.</span><span class="sxs-lookup"><span data-stu-id="d4c54-112">The Draw Method.</span></span>](#the-draw-method)
    -   [<span data-ttu-id="d4c54-113">Méthode GetMetrics.</span><span class="sxs-lookup"><span data-stu-id="d4c54-113">The GetMetrics Method.</span></span>](#the-getmetrics-method)
    -   [<span data-ttu-id="d4c54-114">Méthode GetOverhangMetrics.</span><span class="sxs-lookup"><span data-stu-id="d4c54-114">The GetOverhangMetrics Method.</span></span>](#the-getoverhangmetrics-method)
    -   [<span data-ttu-id="d4c54-115">Méthode GetBreakConditions.</span><span class="sxs-lookup"><span data-stu-id="d4c54-115">The GetBreakConditions Method.</span></span>](#the-getbreakconditions-method)
-   [<span data-ttu-id="d4c54-116">Étape 4 : créez une instance de la classe InlineImage et ajoutez-la à la disposition du texte.</span><span class="sxs-lookup"><span data-stu-id="d4c54-116">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="d4c54-117">Étape 1 : créer une disposition de texte.</span><span class="sxs-lookup"><span data-stu-id="d4c54-117">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="d4c54-118">Pour commencer, vous aurez besoin d’une application avec un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="d4c54-118">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="d4c54-119">Si vous disposez déjà d’une application qui affiche du texte avec une disposition de texte, passez à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="d4c54-119">If you already have an application that displays text with a text layout, skip to Step 2.</span></span>

<span data-ttu-id="d4c54-120">Pour ajouter une disposition de texte, vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c54-120">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="d4c54-121">Déclarez un pointeur vers une interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en tant que membre de la classe.</span><span class="sxs-lookup"><span data-stu-id="d4c54-121">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="d4c54-122">À la fin de la méthode CreateDeviceIndependentResources, créez un objet d’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en appelant la méthode [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="d4c54-122">At the end of the CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="d4c54-123">Ensuite, vous devez remplacer l’appel à la méthode [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) par [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="d4c54-123">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), as shown in the following code.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a><span data-ttu-id="d4c54-124">Étape 2 : définissez une classe dérivée de l’interface IDWriteInlineObject.</span><span class="sxs-lookup"><span data-stu-id="d4c54-124">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>

<span data-ttu-id="d4c54-125">La prise en charge des objets inline dans [DirectWrite](direct-write-portal.md) est assurée par l’interface [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) .</span><span class="sxs-lookup"><span data-stu-id="d4c54-125">Support for inline objects in [DirectWrite](direct-write-portal.md) is provided by the [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) interface.</span></span> <span data-ttu-id="d4c54-126">Pour utiliser des objets Inline, vous devez implémenter cette interface.</span><span class="sxs-lookup"><span data-stu-id="d4c54-126">To use inline objects, you must implement this interface.</span></span> <span data-ttu-id="d4c54-127">Il gère le dessin de l’objet Inline, ainsi que la fourniture de métriques et d’autres informations au convertisseur.</span><span class="sxs-lookup"><span data-stu-id="d4c54-127">It handles the drawing of the inline object, as well as providing metrics and other information to the renderer.</span></span>

<span data-ttu-id="d4c54-128">Créez un nouveau fichier d’en-tête et déclarez une interface appelée InlineImage, dérivée de [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span><span class="sxs-lookup"><span data-stu-id="d4c54-128">Create a new header file and declare an interface called InlineImage, derived from [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span></span>

<span data-ttu-id="d4c54-129">En plus de QueryInterface, AddRef et Release hérités de IUnknown, cette classe doit avoir les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c54-129">In addition to QueryInterface, AddRef, and Release inherited from IUnknown, this class must have the following methods:</span></span>

-   [<span data-ttu-id="d4c54-130">**Dessin**</span><span class="sxs-lookup"><span data-stu-id="d4c54-130">**Draw**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [<span data-ttu-id="d4c54-131">**GetMetrics**</span><span class="sxs-lookup"><span data-stu-id="d4c54-131">**GetMetrics**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [<span data-ttu-id="d4c54-132">**GetOverhangMetrics**</span><span class="sxs-lookup"><span data-stu-id="d4c54-132">**GetOverhangMetrics**</span></span>](idwriteinlineobject-getoverhangmetrics.md)
-   [<span data-ttu-id="d4c54-133">**GetBreakConditions**</span><span class="sxs-lookup"><span data-stu-id="d4c54-133">**GetBreakConditions**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a><span data-ttu-id="d4c54-134">Étape 3 : implémenter la classe d’objet Inline.</span><span class="sxs-lookup"><span data-stu-id="d4c54-134">Step 3: Implement the Inline Object Class.</span></span>

<span data-ttu-id="d4c54-135">Créez un nouveau fichier C++, nommé InlineImage. cpp, pour l’implémentation de la classe.</span><span class="sxs-lookup"><span data-stu-id="d4c54-135">Create a new C++ file, named InlineImage.cpp, for the class implementation.</span></span> <span data-ttu-id="d4c54-136">En plus de la méthode LoadBitmapFromFile et des méthodes héritées de l’interface IUnknown, la classe InlineImage est constituée des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d4c54-136">In addition to the LoadBitmapFromFile method and the methods inherited from the IUnknown interface, the InlineImage class is made up of the following methods.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="d4c54-137">Constructeur.</span><span class="sxs-lookup"><span data-stu-id="d4c54-137">The Constructor.</span></span>


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



<span data-ttu-id="d4c54-138">Le premier argument du constructeur est le ID2D1RenderTarget dans lequel l’image Inline sera restituée.</span><span class="sxs-lookup"><span data-stu-id="d4c54-138">The first argument of the constructor is the ID2D1RenderTarget that the inline image will be rendered to.</span></span> <span data-ttu-id="d4c54-139">Il est stocké pour une utilisation ultérieure lors du dessin.</span><span class="sxs-lookup"><span data-stu-id="d4c54-139">This is stored for use later when drawing.</span></span>

<span data-ttu-id="d4c54-140">La cible de rendu, IWICImagingFactory et l’URI de nom de fichier sont tous passés à la méthode LoadBitmapFromFile qui charge le bitmap et stocke la taille de la bitmap (largeur et hauteur) dans la \_ variable de membre Rect.</span><span class="sxs-lookup"><span data-stu-id="d4c54-140">The render target, IWICImagingFactory, and the filename uri are all passed to the LoadBitmapFromFile method that loads the bitmap and stores the bitmap size (width and height) in the rect\_ member variable.</span></span>

### <a name="the-draw-method"></a><span data-ttu-id="d4c54-141">Méthode Draw.</span><span class="sxs-lookup"><span data-stu-id="d4c54-141">The Draw Method.</span></span>

<span data-ttu-id="d4c54-142">La méthode [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) est un rappel qui est appelé par l’objet [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) lorsque l’objet Inline doit être dessiné.</span><span class="sxs-lookup"><span data-stu-id="d4c54-142">The [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) method is a callback that is called by the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) object when the inline object needs to be drawn.</span></span> <span data-ttu-id="d4c54-143">La disposition du texte n’appelle pas cette méthode directement.</span><span class="sxs-lookup"><span data-stu-id="d4c54-143">The text layout does not call this method directly.</span></span>


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



<span data-ttu-id="d4c54-144">Dans ce cas, le dessin de l’image bitmap s’effectue à l’aide de la méthode [**ID2D1RenderTarget ::D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) ; Toutefois, vous pouvez utiliser n’importe quelle méthode de dessin.</span><span class="sxs-lookup"><span data-stu-id="d4c54-144">In this case, drawing the bitmap is done by using the [**ID2D1RenderTarget::DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) method; however, any method for drawing can be used.</span></span>

### <a name="the-getmetrics-method"></a><span data-ttu-id="d4c54-145">Méthode GetMetrics.</span><span class="sxs-lookup"><span data-stu-id="d4c54-145">The GetMetrics Method.</span></span>


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



<span data-ttu-id="d4c54-146">Pour la méthode [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) , stockez la largeur, la hauteur et la ligne de base dans une structure de [**\_ \_ \_ métriques d’objets Inline DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) .</span><span class="sxs-lookup"><span data-stu-id="d4c54-146">For the [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) method, store the width, height and baseline in an [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) structure.</span></span> <span data-ttu-id="d4c54-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) appelle cette fonction de rappel pour récupérer la mesure de l’objet Inline.</span><span class="sxs-lookup"><span data-stu-id="d4c54-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the measurement of the inline object.</span></span>

### <a name="the-getoverhangmetrics-method"></a><span data-ttu-id="d4c54-148">Méthode GetOverhangMetrics.</span><span class="sxs-lookup"><span data-stu-id="d4c54-148">The GetOverhangMetrics Method.</span></span>


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



<span data-ttu-id="d4c54-149">Dans ce cas, aucun dépassement n’est nécessaire, de sorte que la méthode [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) retourne tous les zéros.</span><span class="sxs-lookup"><span data-stu-id="d4c54-149">In this case, no overhang is necessary, so the [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) method returns all zeros.</span></span>

### <a name="the-getbreakconditions-method"></a><span data-ttu-id="d4c54-150">Méthode GetBreakConditions.</span><span class="sxs-lookup"><span data-stu-id="d4c54-150">The GetBreakConditions Method.</span></span>


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



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a><span data-ttu-id="d4c54-151">Étape 4 : créez une instance de la classe InlineImage et ajoutez-la à la disposition du texte.</span><span class="sxs-lookup"><span data-stu-id="d4c54-151">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>

<span data-ttu-id="d4c54-152">Enfin, dans la méthode CreateDeviceDependentResources, créez une instance de la classe InlineImage et ajoutez-la à la disposition du texte.</span><span class="sxs-lookup"><span data-stu-id="d4c54-152">Finally, in the CreateDeviceDependentResources method, create an instance of the InlineImage class and add it to the text layout.</span></span> <span data-ttu-id="d4c54-153">Étant donné qu’il contient une référence à [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), qui est une ressource dépendante de l’appareil, et que le [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) est créé à l’aide de la cible de rendu, le InlineImage est également dépendant du périphérique et doit être recréé si la cible de rendu est recréée.</span><span class="sxs-lookup"><span data-stu-id="d4c54-153">Because it holds a reference to the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), which is a device dependent resource, and the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is created by using the render target, the InlineImage is also device dependent and must be recreated if the render target is recreated.</span></span>


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



<span data-ttu-id="d4c54-154">La méthode [**IDWriteTextLayout :: SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) prend une structure de plage de texte.</span><span class="sxs-lookup"><span data-stu-id="d4c54-154">The [**IDWriteTextLayout::SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) method takes a text range structure.</span></span> <span data-ttu-id="d4c54-155">L’objet s’applique à la plage spécifiée ici, et tout texte de la plage sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="d4c54-155">The object applies to the range specified here, and any text in the range will be suppressed.</span></span> <span data-ttu-id="d4c54-156">Si la longueur de la plage de texte est 0, l’objet ne sera pas dessiné.</span><span class="sxs-lookup"><span data-stu-id="d4c54-156">If the length of the text range is 0, the object will not be drawn.</span></span>

<span data-ttu-id="d4c54-157">Dans cet exemple, il y a un astérisque ( \* ) comme espace réservé à l’emplacement où l’image sera affichée.</span><span class="sxs-lookup"><span data-stu-id="d4c54-157">In this example, there is an asterisk (\*) as a place holder in the position where the image will be displayed.</span></span>


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



<span data-ttu-id="d4c54-158">Étant donné que la classe InlineImage dépend du [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), vous devez la libérer quand vous libérez la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="d4c54-158">Since the InlineImage class is dependent on the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), you must release it when you release the render target.</span></span>


```C++
SafeRelease(&pInlineImage_);
```



 

 