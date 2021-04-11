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
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a><span data-ttu-id="551f9-103">Comment ajouter des effets de dessin client à une disposition de texte</span><span class="sxs-lookup"><span data-stu-id="551f9-103">How to Add Client Drawing Effects to a Text Layout</span></span>

<span data-ttu-id="551f9-104">Fournit un bref didacticiel sur l’ajout d’effets de dessin client à une application [DirectWrite](direct-write-portal.md) qui affiche du texte à l’aide de l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) et d’un convertisseur de texte personnalisé.</span><span class="sxs-lookup"><span data-stu-id="551f9-104">Provides a short tutorial on adding client drawing effects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface and a custom text renderer.</span></span>

<span data-ttu-id="551f9-105">Le produit final de ce didacticiel est une application qui affiche du texte avec des plages de texte avec un effet de dessin de couleur différent sur chaque, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="551f9-105">The end product of this tutorial is an application that displays text that has ranges of text with a different color drawing effect on each, as shown in the following screen shot.</span></span>

![capture d’écran de l' « exemple d’effet de dessin client ! »](images/drawingeffects.png)

> [!Note]  
> <span data-ttu-id="551f9-108">Ce didacticiel est destiné à être un exemple simplifié de la création d’effets de dessin client personnalisés, et non d’un exemple de méthode simple pour dessiner du texte de couleur.</span><span class="sxs-lookup"><span data-stu-id="551f9-108">This tutorial is meant to be a simplified example of how to create custom client drawing effects, not an example of a simple method for drawing color text.</span></span> <span data-ttu-id="551f9-109">Pour plus d’informations, consultez la page de référence de [**IDWriteTextLayout :: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) .</span><span class="sxs-lookup"><span data-stu-id="551f9-109">See the [**IDWriteTextLayout::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) reference page for more information.</span></span>

 

<span data-ttu-id="551f9-110">Ce didacticiel contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="551f9-110">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="551f9-111">Étape 1 : créer une disposition de texte</span><span class="sxs-lookup"><span data-stu-id="551f9-111">Step 1: Create a Text Layout</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="551f9-112">Étape 2 : implémenter une classe d’effet de dessin personnalisée</span><span class="sxs-lookup"><span data-stu-id="551f9-112">Step 2: Implement a Custom Drawing Effect Class</span></span>](#step-2-implement-a-custom-drawing-effect-class)
-   [<span data-ttu-id="551f9-113">Étape 3 : implémenter une classe de convertisseur de texte personnalisée</span><span class="sxs-lookup"><span data-stu-id="551f9-113">Step 3: Implement a Custom Text Renderer Class</span></span>](#step-3-implement-a-custom-text-renderer-class)
    -   [<span data-ttu-id="551f9-114">Le constructeur</span><span class="sxs-lookup"><span data-stu-id="551f9-114">The Constructor</span></span>](#the-constructor)
    -   [<span data-ttu-id="551f9-115">Méthode DrawGlyphRun</span><span class="sxs-lookup"><span data-stu-id="551f9-115">The DrawGlyphRun Method</span></span>](#the-drawglyphrun-method)
    -   [<span data-ttu-id="551f9-116">Destructeur</span><span class="sxs-lookup"><span data-stu-id="551f9-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="551f9-117">Étape 4 : créer le convertisseur de texte</span><span class="sxs-lookup"><span data-stu-id="551f9-117">Step 4: Create the Text Renderer</span></span>](#step-4-create-the-text-renderer)
-   [<span data-ttu-id="551f9-118">Étape 5 : instancier les objets d’effet de dessin de couleur</span><span class="sxs-lookup"><span data-stu-id="551f9-118">Step 5: Instantiate the Color Drawing Effect Objects</span></span>](#step-5-instantiate-the-color-drawing-effect-objects)
-   [<span data-ttu-id="551f9-119">Étape 6 : définir l’effet de dessin pour des plages de texte spécifiques</span><span class="sxs-lookup"><span data-stu-id="551f9-119">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [<span data-ttu-id="551f9-120">Étape 7 : dessiner la disposition du texte à l’aide du convertisseur personnalisé</span><span class="sxs-lookup"><span data-stu-id="551f9-120">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [<span data-ttu-id="551f9-121">Étape 8 : nettoyer</span><span class="sxs-lookup"><span data-stu-id="551f9-121">Step 8: Clean up</span></span>](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="551f9-122">Étape 1 : créer une disposition de texte</span><span class="sxs-lookup"><span data-stu-id="551f9-122">Step 1: Create a Text Layout</span></span>

<span data-ttu-id="551f9-123">Pour commencer, vous aurez besoin d’une application avec un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="551f9-123">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="551f9-124">Si vous disposez déjà d’une application qui affiche du texte avec une disposition de texte ou si vous utilisez l’exemple de code DrawingEffect personnalisé, passez à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="551f9-124">If you already have an application that displays text with a text layout, or you are using the Custom DrawingEffect Example Code, skip to Step 2.</span></span>

<span data-ttu-id="551f9-125">Pour ajouter une disposition de texte, vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="551f9-125">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="551f9-126">Déclarez un pointeur vers une interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en tant que membre de la classe.</span><span class="sxs-lookup"><span data-stu-id="551f9-126">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="551f9-127">À la fin de la méthode **CreateDeviceIndependentResources** , créez un objet d’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) en appelant la méthode [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="551f9-127">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="551f9-128">Enfin, n’oubliez pas de libérer la disposition du texte dans le destructeur.</span><span class="sxs-lookup"><span data-stu-id="551f9-128">Finally, remember to release the text layout in the destructor.</span></span>
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a><span data-ttu-id="551f9-129">Étape 2 : implémenter une classe d’effet de dessin personnalisée</span><span class="sxs-lookup"><span data-stu-id="551f9-129">Step 2: Implement a Custom Drawing Effect Class</span></span>

<span data-ttu-id="551f9-130">En dehors des méthodes héritées de IUnknown, une interface d’effet de dessin client personnalisé n’a aucune exigence quant à ce qu’elle doit implémenter.</span><span class="sxs-lookup"><span data-stu-id="551f9-130">Other than the methods inherited from IUnknown, a custom client drawing effect interface has no requirements as to what it must implement.</span></span> <span data-ttu-id="551f9-131">Dans ce cas, la classe **ColorDrawingEffect** contient simplement une [**valeur \_ \_ F de couleur d2d1**](../direct2d/d2d1-color-f.md) et déclare des méthodes pour obtenir et définir cette valeur, ainsi qu’un constructeur qui peut définir initialement la couleur.</span><span class="sxs-lookup"><span data-stu-id="551f9-131">In this case, the **ColorDrawingEffect** class simply holds a [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value and declares methods to get and set this value, as well as a constructor that can set the color initially.</span></span>

<span data-ttu-id="551f9-132">Après l’application d’un effet de dessin client à une plage de texte dans un objet [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , l’effet de dessin est passé à la méthode [**IDWriteTextRenderer ::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) de toute exécution de glyphes qui doit être rendue.</span><span class="sxs-lookup"><span data-stu-id="551f9-132">After a client drawing effect is applied to a text range in a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, the drawing effect is passed to the [**IDWriteTextRenderer::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of any glyph run that is to be rendered.</span></span> <span data-ttu-id="551f9-133">Les méthodes de l’effet de dessin sont ensuite disponibles pour le convertisseur de texte.</span><span class="sxs-lookup"><span data-stu-id="551f9-133">The methods of the drawing effect are then available to the text renderer.</span></span>

<span data-ttu-id="551f9-134">Un effet de dessin client peut être aussi complexe que vous le souhaitez, en fournissant plus d’informations que dans cet exemple, et en fournissant des méthodes pour modifier des glyphes, créer des objets à utiliser pour le dessin, etc.</span><span class="sxs-lookup"><span data-stu-id="551f9-134">A client drawing effect can be as complex as you want to make it, carrying more information than in this example, as well as providing methods to alter glyphs, create objects to be used for drawing, and so on.</span></span>

## <a name="step-3-implement-a-custom-text-renderer-class"></a><span data-ttu-id="551f9-135">Étape 3 : implémenter une classe de convertisseur de texte personnalisée</span><span class="sxs-lookup"><span data-stu-id="551f9-135">Step 3: Implement a Custom Text Renderer Class</span></span>

<span data-ttu-id="551f9-136">Pour tirer parti d’un effet de dessin client, vous devez implémenter un convertisseur de texte personnalisé.</span><span class="sxs-lookup"><span data-stu-id="551f9-136">In order to take advantage of a client drawing effect, you must implement a custom text renderer.</span></span> <span data-ttu-id="551f9-137">Ce convertisseur de texte applique l’effet de dessin qui lui est transmis par la méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) à l’exécution du glyphe qui est tracée.</span><span class="sxs-lookup"><span data-stu-id="551f9-137">This text renderer will apply the drawing effect passed to it by the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method to the glyph run being drawn.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="551f9-138">Le constructeur</span><span class="sxs-lookup"><span data-stu-id="551f9-138">The Constructor</span></span>

<span data-ttu-id="551f9-139">Le constructeur pour le convertisseur de texte personnalisé stocke l’objet [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) qui sera utilisé pour créer des objets [Direct2D](../direct2d/direct2d-portal.md) , et la cible de rendu Direct2D sur laquelle le texte sera dessiné.</span><span class="sxs-lookup"><span data-stu-id="551f9-139">The constructor for the custom text renderer stores the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create [Direct2D](../direct2d/direct2d-portal.md) objects, and the Direct2D render target that the text will be drawn on to.</span></span>


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



### <a name="the-drawglyphrun-method"></a><span data-ttu-id="551f9-140">Méthode DrawGlyphRun</span><span class="sxs-lookup"><span data-stu-id="551f9-140">The DrawGlyphRun Method</span></span>

<span data-ttu-id="551f9-141">Une exécution de glyphe est un ensemble de glyphes qui partagent le même format, y compris l’effet de dessin client.</span><span class="sxs-lookup"><span data-stu-id="551f9-141">A glyph run is a set of glyphs that share the same format, including the client drawing effect.</span></span> <span data-ttu-id="551f9-142">La méthode [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) s’occupe du rendu de texte pour une exécution de glyphes spécifiée.</span><span class="sxs-lookup"><span data-stu-id="551f9-142">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method takes care of the text rendering for a specified glyph run.</span></span>

<span data-ttu-id="551f9-143">Tout d’abord, créez un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) et un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink), puis récupérez le plan d’exécution de glyphe à l’aide de [**IDWriteFontFace :: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span><span class="sxs-lookup"><span data-stu-id="551f9-143">First, create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink), and then retrieve the glyph run outline by using [**IDWriteFontFace::GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span></span> <span data-ttu-id="551f9-144">Transformez ensuite l’origine de la géométrie à l’aide de la méthode [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory :: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="551f9-144">Then transform the origin of the geometry by using the [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method, as shown in the following code.</span></span>


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



<span data-ttu-id="551f9-145">Ensuite, déclarez un objet pinceau solide [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="551f9-145">Next, declare a [Direct2D](../direct2d/direct2d-portal.md) solid brush object.</span></span>


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



<span data-ttu-id="551f9-146">Si le paramètre *clientDrawingEffect* n’a pas la valeur null, interrogez l’objet pour l’interface **ColorDrawingEffect** .</span><span class="sxs-lookup"><span data-stu-id="551f9-146">If the *clientDrawingEffect* parameter is not NULL, query the object for the **ColorDrawingEffect** interface.</span></span> <span data-ttu-id="551f9-147">Cela fonctionnera, car vous définirez cette classe en tant qu’effet de dessin du client sur les plages de texte de l’objet de mise en page de texte.</span><span class="sxs-lookup"><span data-stu-id="551f9-147">This will work because you will set this class as the client drawing effect on text ranges of the text layout object.</span></span>

<span data-ttu-id="551f9-148">Une fois que vous avez un pointeur vers l’interface **ColorDrawingEffect** , vous pouvez récupérer la valeur F de la [**\_ couleur \_ d2d1**](../direct2d/d2d1-color-f.md) qu’elle stocke à l’aide de la méthode **GetColor** .</span><span class="sxs-lookup"><span data-stu-id="551f9-148">Once you have a pointer to the **ColorDrawingEffect** interface, you can retrieve the [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value that it stores using the **GetColor** method.</span></span> <span data-ttu-id="551f9-149">Ensuite, utilisez la **\_ couleur d2d1 \_ F** pour créer un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) dans cette couleur.</span><span class="sxs-lookup"><span data-stu-id="551f9-149">Then, use the **D2D1\_COLOR\_F** to create a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in that color.</span></span>

<span data-ttu-id="551f9-150">Si le paramètre *clientDrawingEffect* a la **valeur null**, créez simplement un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)noir.</span><span class="sxs-lookup"><span data-stu-id="551f9-150">If the *clientDrawingEffect* parameter is **NULL**, then just create a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


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



<span data-ttu-id="551f9-151">Enfin, dessinez la géométrie du contour et complétez-la à l’aide du pinceau de couleur unie que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="551f9-151">Finally, draw the outline geometry and fill it using the solid color brush that you just created.</span></span>


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



### <a name="the-destructor"></a><span data-ttu-id="551f9-152">Destructeur</span><span class="sxs-lookup"><span data-stu-id="551f9-152">The Destructor</span></span>

<span data-ttu-id="551f9-153">N’oubliez pas de libérer la fabrique [Direct2D](../direct2d/direct2d-portal.md) et la cible de rendu dans le destructeur.</span><span class="sxs-lookup"><span data-stu-id="551f9-153">Don't forget to release the [Direct2D](../direct2d/direct2d-portal.md) factory and render target in the destructor.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a><span data-ttu-id="551f9-154">Étape 4 : créer le convertisseur de texte</span><span class="sxs-lookup"><span data-stu-id="551f9-154">Step 4: Create the Text Renderer</span></span>

<span data-ttu-id="551f9-155">Dans les ressources **CreateDeviceDependent** , créez l’objet de convertisseur de texte personnalisé.</span><span class="sxs-lookup"><span data-stu-id="551f9-155">In the **CreateDeviceDependent** resources, create the custom text renderer object.</span></span> <span data-ttu-id="551f9-156">Elle dépend de l’appareil, car elle utilise le **ID2D1RenderTarget**, qui est lui-même dépendant du périphérique.</span><span class="sxs-lookup"><span data-stu-id="551f9-156">It is device dependent because it uses the **ID2D1RenderTarget**, which is itself device dependent.</span></span>


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a><span data-ttu-id="551f9-157">Étape 5 : instancier les objets d’effet de dessin de couleur</span><span class="sxs-lookup"><span data-stu-id="551f9-157">Step 5: Instantiate the Color Drawing Effect Objects</span></span>

<span data-ttu-id="551f9-158">Instanciez les objets **ColorDrawingEffect** en rouge, vert et bleu.</span><span class="sxs-lookup"><span data-stu-id="551f9-158">Instantiate **ColorDrawingEffect** objects in red, green, and blue.</span></span>


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



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a><span data-ttu-id="551f9-159">Étape 6 : définir l’effet de dessin pour des plages de texte spécifiques</span><span class="sxs-lookup"><span data-stu-id="551f9-159">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>

<span data-ttu-id="551f9-160">Définissez l’effet de dessin pour des plages de texte spécifiques à l’aide de la méthode [**IDWriteTextLayou :: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) et d’un struct de [**\_ \_ plage de texte DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) .</span><span class="sxs-lookup"><span data-stu-id="551f9-160">Set the drawing effect for specific ranges of text by using the [**IDWriteTextLayou::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) method and a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) struct.</span></span>


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



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a><span data-ttu-id="551f9-161">Étape 7 : dessiner la disposition du texte à l’aide du convertisseur personnalisé</span><span class="sxs-lookup"><span data-stu-id="551f9-161">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>

<span data-ttu-id="551f9-162">Vous devez appeler la méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) au lieu des méthodes [**ID2D1RenderTarget ::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) ou [**ID2D1RenderTarget ::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="551f9-162">You must call the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method rather than the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) or [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) methods.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a><span data-ttu-id="551f9-163">Étape 8 : nettoyer</span><span class="sxs-lookup"><span data-stu-id="551f9-163">Step 8: Clean up</span></span>

<span data-ttu-id="551f9-164">Dans le destructeur DemoApp, libérez le convertisseur de texte personnalisé.</span><span class="sxs-lookup"><span data-stu-id="551f9-164">In the DemoApp destructor, release the custom text renderer.</span></span>


```C++
SafeRelease(&pTextRenderer_);
```



<span data-ttu-id="551f9-165">Après cela, ajoutez du code pour libérer les classes d’effet de dessin du client.</span><span class="sxs-lookup"><span data-stu-id="551f9-165">After that, add code to release the client drawing effect classes.</span></span>


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 