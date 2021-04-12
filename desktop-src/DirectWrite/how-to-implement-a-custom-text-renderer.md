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
# <a name="render-using-a-custom-text-renderer"></a><span data-ttu-id="70bc8-103">Rendre en utilisant le convertisseur de texte personnalisé</span><span class="sxs-lookup"><span data-stu-id="70bc8-103">Render Using a Custom Text Renderer</span></span>

<span data-ttu-id="70bc8-104">Une [](direct-write-portal.md) [**disposition de texte**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) DirectWrite peut être dessinée par un convertisseur de texte personnalisé dérivé de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span><span class="sxs-lookup"><span data-stu-id="70bc8-104">A [DirectWrite](direct-write-portal.md) [**text layout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) can be drawn by a custom text renderer derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span></span> <span data-ttu-id="70bc8-105">Un convertisseur personnalisé est nécessaire pour tirer parti de certaines fonctionnalités avancées de DirectWrite, telles que le rendu sur une surface bitmap ou GDI, les objets inline et les effets de dessin client.</span><span class="sxs-lookup"><span data-stu-id="70bc8-105">A custom renderer is required to take advantage of some advanced features of DirectWrite, such as rendering to a bitmap or GDI surface, inline objects, and client drawing effects.</span></span> <span data-ttu-id="70bc8-106">Ce didacticiel décrit les méthodes de **IDWriteTextRenderer** et fournit un exemple d’implémentation qui utilise [Direct2D](../direct2d/direct2d-portal.md) pour restituer le texte avec un remplissage bitmap.</span><span class="sxs-lookup"><span data-stu-id="70bc8-106">This tutorial describes the methods of **IDWriteTextRenderer**, and provides an example implementation that uses [Direct2D](../direct2d/direct2d-portal.md) to render text with a bitmap fill.</span></span>

<span data-ttu-id="70bc8-107">Ce didacticiel contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="70bc8-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="70bc8-108">Le constructeur</span><span class="sxs-lookup"><span data-stu-id="70bc8-108">The Constructor</span></span>](#the-constructor)
-   [<span data-ttu-id="70bc8-109">DrawGlyphRun ()</span><span class="sxs-lookup"><span data-stu-id="70bc8-109">DrawGlyphRun()</span></span>](#drawglyphrun)
-   [<span data-ttu-id="70bc8-110">DrawUnderline () et DrawStrikethrough ()</span><span class="sxs-lookup"><span data-stu-id="70bc8-110">DrawUnderline() and DrawStrikethrough()</span></span>](#drawunderline-and-drawstrikethrough)
-   [<span data-ttu-id="70bc8-111">Accrochage des pixels, pixels par DIP et transformation</span><span class="sxs-lookup"><span data-stu-id="70bc8-111">Pixel Snapping, Pixels per DIP, and Transform</span></span>](#pixel-snapping-pixels-per-dip-and-transform)
    -   [<span data-ttu-id="70bc8-112">IsPixelSnappingDisabled()</span><span class="sxs-lookup"><span data-stu-id="70bc8-112">IsPixelSnappingDisabled()</span></span>](#ispixelsnappingdisabled)
    -   [<span data-ttu-id="70bc8-113">GetCurrentTransform()</span><span class="sxs-lookup"><span data-stu-id="70bc8-113">GetCurrentTransform()</span></span>](#getcurrenttransform)
    -   [<span data-ttu-id="70bc8-114">GetPixelsPerDip()</span><span class="sxs-lookup"><span data-stu-id="70bc8-114">GetPixelsPerDip()</span></span>](#getpixelsperdip)
-   [<span data-ttu-id="70bc8-115">DrawInlineObject()</span><span class="sxs-lookup"><span data-stu-id="70bc8-115">DrawInlineObject()</span></span>](#drawinlineobject)
-   [<span data-ttu-id="70bc8-116">Destructeur</span><span class="sxs-lookup"><span data-stu-id="70bc8-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="70bc8-117">Utilisation du convertisseur de texte personnalisé</span><span class="sxs-lookup"><span data-stu-id="70bc8-117">Using the Custom Text Renderer</span></span>](#using-the-custom-text-renderer)

<span data-ttu-id="70bc8-118">Votre convertisseur de texte personnalisé doit implémenter les méthodes héritées de IUnknown en plus des méthodes listées dans la page de référence [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) et ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="70bc8-118">Your custom text renderer must implement the methods inherited from IUnknown in addition to the methods listed on the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page and below.</span></span>

<span data-ttu-id="70bc8-119">Pour obtenir le code source complet du convertisseur de texte personnalisé, consultez les fichiers CustomTextRenderer. cpp et CustomTextRenderer. h de l' [exemple DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="70bc8-119">For the full source code for the custom text renderer, see the CustomTextRenderer.cpp and CustomTextRenderer.h files of the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="the-constructor"></a><span data-ttu-id="70bc8-120">Le constructeur</span><span class="sxs-lookup"><span data-stu-id="70bc8-120">The Constructor</span></span>

<span data-ttu-id="70bc8-121">Votre convertisseur de texte personnalisé aura besoin d’un constructeur.</span><span class="sxs-lookup"><span data-stu-id="70bc8-121">Your custom text renderer will need a constructor.</span></span> <span data-ttu-id="70bc8-122">Cet exemple utilise à la fois des pinceaux et des pinceaux [Direct2D](../direct2d/direct2d-portal.md) solides et bitmap pour restituer le texte.</span><span class="sxs-lookup"><span data-stu-id="70bc8-122">This example uses both solid and bitmap [Direct2D](../direct2d/direct2d-portal.md) brushes to render the text.</span></span>

<span data-ttu-id="70bc8-123">Pour cette raison, le constructeur prend les paramètres figurant dans le tableau ci-dessous avec les descriptions.</span><span class="sxs-lookup"><span data-stu-id="70bc8-123">Because of this, the constructor takes the parameters found in the table below with descriptions.</span></span>



| <span data-ttu-id="70bc8-124">Paramètre</span><span class="sxs-lookup"><span data-stu-id="70bc8-124">Parameter</span></span>       | <span data-ttu-id="70bc8-125">Description</span><span class="sxs-lookup"><span data-stu-id="70bc8-125">Description</span></span>                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70bc8-126">*pD2DFactory*</span><span class="sxs-lookup"><span data-stu-id="70bc8-126">*pD2DFactory*</span></span>   | <span data-ttu-id="70bc8-127">Pointeur vers un objet [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) qui sera utilisé pour créer toutes les ressources Direct2D nécessaires.</span><span class="sxs-lookup"><span data-stu-id="70bc8-127">A pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create any Direct2D resources that are needed.</span></span>                                                                                                        |
| <span data-ttu-id="70bc8-128">*pRT*</span><span class="sxs-lookup"><span data-stu-id="70bc8-128">*pRT*</span></span>           | <span data-ttu-id="70bc8-129">Pointeur vers l’objet [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) dans lequel le texte sera restitué.</span><span class="sxs-lookup"><span data-stu-id="70bc8-129">A pointer to the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object that the text will be rendered to.</span></span> |
| <span data-ttu-id="70bc8-130">*pOutlineBrush*</span><span class="sxs-lookup"><span data-stu-id="70bc8-130">*pOutlineBrush*</span></span> | <span data-ttu-id="70bc8-131">Pointeur vers le [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) qui sera utilisé pour dessiner le contour du texte</span><span class="sxs-lookup"><span data-stu-id="70bc8-131">A pointer to the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) that will be use to draw outline of the text</span></span>                                                                                                                     |
| <span data-ttu-id="70bc8-132">*pFillBrush*</span><span class="sxs-lookup"><span data-stu-id="70bc8-132">*pFillBrush*</span></span>    | <span data-ttu-id="70bc8-133">Pointeur vers le [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) qui sera utilisé pour remplir le texte.</span><span class="sxs-lookup"><span data-stu-id="70bc8-133">A pointer to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that will be used to fill the text.</span></span>                                                                                                                                      |



 

<span data-ttu-id="70bc8-134">Celles-ci seront stockées par le constructeur comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="70bc8-134">These will be stored by the constructor as shown in the following code.</span></span>


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



## <a name="drawglyphrun"></a><span data-ttu-id="70bc8-135">DrawGlyphRun ()</span><span class="sxs-lookup"><span data-stu-id="70bc8-135">DrawGlyphRun()</span></span>

<span data-ttu-id="70bc8-136">La méthode [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) est la méthode de rappel principale du convertisseur de texte.</span><span class="sxs-lookup"><span data-stu-id="70bc8-136">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method is the main callback method of the text renderer.</span></span> <span data-ttu-id="70bc8-137">Une série de glyphes est passée pour être rendue en plus des informations telles que l’origine de la ligne de base et le mode de mesure.</span><span class="sxs-lookup"><span data-stu-id="70bc8-137">It is passed a run of glyphs to be rendered in addition to information such as the baseline origin and measuring mode.</span></span> <span data-ttu-id="70bc8-138">Il passe également un objet d’effet de dessin client à appliquer à l’exécution du glyphe.</span><span class="sxs-lookup"><span data-stu-id="70bc8-138">It also passes a client drawing effect object to be applied to the glyph run.</span></span> <span data-ttu-id="70bc8-139">Pour plus d’informations, consultez la rubrique [comment ajouter des effets de dessin client à une disposition de texte](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="70bc8-139">For more information, see the [How to Add Client Drawing Effects to a Text Layout](how-to-add-custom-drawing-efffects-to-a-text-layout.md) topic.</span></span>

<span data-ttu-id="70bc8-140">Cette implémentation de convertisseur de texte affiche les exécutions de glyphe en les convertissant en géométries [Direct2D](rendering-by-using-direct2d.md) , puis en dessinant et remplissant les géométries.</span><span class="sxs-lookup"><span data-stu-id="70bc8-140">This text renderer implementation renders glyph runs by converting them to [Direct2D](rendering-by-using-direct2d.md) geometries and then drawing and filling the geometries.</span></span> <span data-ttu-id="70bc8-141">Cela comprend les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="70bc8-141">This consists of the following steps.</span></span>

1.  <span data-ttu-id="70bc8-142">Créez un objet [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) , puis récupérez l’objet [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) à l’aide de la méthode [**ID2D1PathGeometry :: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .</span><span class="sxs-lookup"><span data-stu-id="70bc8-142">Create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object, and then retrieve the [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) object by using the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>

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

    

2.  <span data-ttu-id="70bc8-143">L' [**\_ \_ exécution de glyphes DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) transmise à [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contient un objet [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , nommé *fontFace*, qui représente le type de police pour l’exécution de glyphe entière.</span><span class="sxs-lookup"><span data-stu-id="70bc8-143">The [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) that is passed to [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contains a [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object, named *fontFace*, that represents the font face for the whole glyph run.</span></span> <span data-ttu-id="70bc8-144">Placez le contour du glyphe dans le récepteur Geometry à l’aide de la méthode [**IDWriteFontFace :: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="70bc8-144">Put the outline of the glyph run into the geometry sink by using the [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) method, as shown in the following code.</span></span>

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

    

3.  <span data-ttu-id="70bc8-145">Après avoir rempli le récepteur de géométrie, fermez-le.</span><span class="sxs-lookup"><span data-stu-id="70bc8-145">After filling the geometry sink, close it.</span></span>

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  <span data-ttu-id="70bc8-146">L’origine de l’exécution du glyphe doit être traduite afin d’être rendue à partir de l’origine de la ligne de base correcte, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="70bc8-146">The origin of the glyph run must be translated so that it is rendered from the correct baseline origin, as shown in the following code.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    <span data-ttu-id="70bc8-147">*BaselineOriginX* et *baselineOriginY* sont passés comme paramètres à la méthode de rappel [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="70bc8-147">The *baselineOriginX* and *baselineOriginY* are passed as parameters to the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback method.</span></span>

5.  <span data-ttu-id="70bc8-148">Créez la géométrie transformée à l’aide de la méthode [**ID2D1Factory :: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) et en passant la géométrie du tracé et la matrice de translation.</span><span class="sxs-lookup"><span data-stu-id="70bc8-148">Create the transformed geometry by using the [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method and passing the path geometry and the translation matrix.</span></span>

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

    

6.  <span data-ttu-id="70bc8-149">Enfin, dessinez le contour de la géométrie transformée et remplissez-le à l’aide des méthodes [**ID2D1RenderTarget ::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) et [**ID2D1RenderTarget :: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) et des pinceaux [Direct2D](../direct2d/direct2d-portal.md) stockés en tant que variables membres.</span><span class="sxs-lookup"><span data-stu-id="70bc8-149">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

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

    

7.  <span data-ttu-id="70bc8-150">Maintenant que vous avez terminé le dessin, n’oubliez pas de nettoyer les objets qui ont été créés dans cette méthode.</span><span class="sxs-lookup"><span data-stu-id="70bc8-150">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a><span data-ttu-id="70bc8-151">DrawUnderline () et DrawStrikethrough ()</span><span class="sxs-lookup"><span data-stu-id="70bc8-151">DrawUnderline() and DrawStrikethrough()</span></span>

<span data-ttu-id="70bc8-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) a également des rappels pour dessiner le trait de soulignement et le barré.</span><span class="sxs-lookup"><span data-stu-id="70bc8-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) also has callbacks for drawing the underline and strikethrough.</span></span> <span data-ttu-id="70bc8-153">Cet exemple dessine un rectangle simple pour un trait de soulignement ou barré, mais d’autres formes peuvent être dessinées.</span><span class="sxs-lookup"><span data-stu-id="70bc8-153">This example draws a simple rectangle for an underline or strikethrough, but other shapes can be drawn.</span></span>

<span data-ttu-id="70bc8-154">Le fait de dessiner un soulignement à l’aide de [Direct2D](../direct2d/direct2d-portal.md) comprend les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="70bc8-154">Drawing an underline by using [Direct2D](../direct2d/direct2d-portal.md) consists of the following steps.</span></span>

1.  <span data-ttu-id="70bc8-155">Tout d’abord, créez une structure [**d2d1 \_ rect \_ F**](../direct2d/d2d1-rect-f.md) de la taille et de la forme du soulignement.</span><span class="sxs-lookup"><span data-stu-id="70bc8-155">First, create a [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure of the size and shape of the underline.</span></span> <span data-ttu-id="70bc8-156">La structure de [**\_ soulignement DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) transmise à la méthode de rappel [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) fournit le décalage, la largeur et l’épaisseur du soulignement.</span><span class="sxs-lookup"><span data-stu-id="70bc8-156">The [**DWRITE\_UNDERLINE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) structure that is passed to the [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) callback method provides the offset, width, and thickness of the underline.</span></span>

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  <span data-ttu-id="70bc8-157">Ensuite, créez un objet [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) à l’aide de la méthode [**ID2D1Factory :: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) et de la structure [**d2d1 \_ rect \_ F**](../direct2d/d2d1-rect-f.md) initialisée.</span><span class="sxs-lookup"><span data-stu-id="70bc8-157">Next, create an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object by using the [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) method and the initialized [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure.</span></span>

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  <span data-ttu-id="70bc8-158">Comme pour l’exécution de glyphes, l’origine de la géométrie du soulignement doit être traduite en fonction des valeurs d’origine de la ligne de base, à l’aide de la méthode [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) .</span><span class="sxs-lookup"><span data-stu-id="70bc8-158">As with the glyph run, the origin of the underline geometry must be translated, based on the baseline origin values, by using the [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method.</span></span>

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

    

4.  <span data-ttu-id="70bc8-159">Enfin, dessinez le contour de la géométrie transformée et remplissez-le à l’aide des méthodes [**ID2D1RenderTarget ::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) et [**ID2D1RenderTarget :: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) et des pinceaux [Direct2D](../direct2d/direct2d-portal.md) stockés en tant que variables membres.</span><span class="sxs-lookup"><span data-stu-id="70bc8-159">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

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

    

5.  <span data-ttu-id="70bc8-160">Maintenant que vous avez terminé le dessin, n’oubliez pas de nettoyer les objets qui ont été créés dans cette méthode.</span><span class="sxs-lookup"><span data-stu-id="70bc8-160">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

<span data-ttu-id="70bc8-161">Le processus de dessin d’un barré est le même.</span><span class="sxs-lookup"><span data-stu-id="70bc8-161">The process for drawing a strikethrough is the same.</span></span> <span data-ttu-id="70bc8-162">Toutefois, le barré aura un décalage différent et probablement une largeur et une épaisseur différentes.</span><span class="sxs-lookup"><span data-stu-id="70bc8-162">However, the strikethrough will have a different offset, and likely a different width and thickness.</span></span>

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a><span data-ttu-id="70bc8-163">Accrochage des pixels, pixels par DIP et transformation</span><span class="sxs-lookup"><span data-stu-id="70bc8-163">Pixel Snapping, Pixels per DIP, and Transform</span></span>

### <a name="ispixelsnappingdisabled"></a><span data-ttu-id="70bc8-164">IsPixelSnappingDisabled()</span><span class="sxs-lookup"><span data-stu-id="70bc8-164">IsPixelSnappingDisabled()</span></span>

<span data-ttu-id="70bc8-165">Cette méthode est appelée pour déterminer si l’alignement des pixels est désactivé.</span><span class="sxs-lookup"><span data-stu-id="70bc8-165">This method is called to determine whether pixel snapping is disabled.</span></span> <span data-ttu-id="70bc8-166">La valeur par défaut recommandée est **false**, ce qui correspond à la sortie de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="70bc8-166">The recommended default is **FALSE**, and that is the output of this example.</span></span>


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a><span data-ttu-id="70bc8-167">GetCurrentTransform()</span><span class="sxs-lookup"><span data-stu-id="70bc8-167">GetCurrentTransform()</span></span>

<span data-ttu-id="70bc8-168">Cet exemple effectue un rendu sur une cible de rendu Direct2D. par conséquent, transférez la transformation à partir de la cible de rendu à l’aide de [**ID2D1RenderTarget :: GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span><span class="sxs-lookup"><span data-stu-id="70bc8-168">This example renders to a Direct2D render target, so forward the transform from the render target using [**ID2D1RenderTarget::GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span></span>


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a><span data-ttu-id="70bc8-169">GetPixelsPerDip()</span><span class="sxs-lookup"><span data-stu-id="70bc8-169">GetPixelsPerDip()</span></span>

<span data-ttu-id="70bc8-170">Cette méthode est appelée pour récupérer le nombre de pixels par DIP (Device Independent Pixel).</span><span class="sxs-lookup"><span data-stu-id="70bc8-170">This method is called to get the number of pixels per Device Independent Pixel (DIP).</span></span>


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a><span data-ttu-id="70bc8-171">DrawInlineObject()</span><span class="sxs-lookup"><span data-stu-id="70bc8-171">DrawInlineObject()</span></span>

<span data-ttu-id="70bc8-172">Un convertisseur de texte personnalisé a également un rappel pour dessiner des objets insérés.</span><span class="sxs-lookup"><span data-stu-id="70bc8-172">A custom text renderer also has a callback for drawing inline objects.</span></span> <span data-ttu-id="70bc8-173">Dans cet exemple, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="70bc8-173">In this example, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) returns E\_NOTIMPL.</span></span> <span data-ttu-id="70bc8-174">Ce didacticiel présente en outre une explication sur la façon de dessiner des objets en ligne.</span><span class="sxs-lookup"><span data-stu-id="70bc8-174">An explanation of how to draw inline objects is beyond the scope of this tutorial.</span></span> <span data-ttu-id="70bc8-175">Pour plus d’informations, consultez la rubrique [comment ajouter des objets Inline à une disposition de texte](how-to-add-inline-objects-to-a-text-layout.md) .</span><span class="sxs-lookup"><span data-stu-id="70bc8-175">For more information, see the [How to Add Inline Objects to a Text Layout](how-to-add-inline-objects-to-a-text-layout.md) topic.</span></span>

## <a name="the-destructor"></a><span data-ttu-id="70bc8-176">Destructeur</span><span class="sxs-lookup"><span data-stu-id="70bc8-176">The Destructor</span></span>

<span data-ttu-id="70bc8-177">Il est important de libérer tous les pointeurs utilisés par la classe de convertisseur de texte personnalisée.</span><span class="sxs-lookup"><span data-stu-id="70bc8-177">It is important to release any pointers that were used by the custom text renderer class.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a><span data-ttu-id="70bc8-178">Utilisation du convertisseur de texte personnalisé</span><span class="sxs-lookup"><span data-stu-id="70bc8-178">Using the Custom Text Renderer</span></span>

<span data-ttu-id="70bc8-179">Vous le rendez avec le convertisseur personnalisé à l’aide de la méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , qui prend une interface de rappel dérivée de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) comme argument, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="70bc8-179">You render with the custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="70bc8-180">La méthode [**IDWriteTextLayout ::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) appelle les méthodes du rappel de convertisseur personnalisé que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="70bc8-180">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="70bc8-181">Les méthodes [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)et [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) décrites ci-dessus effectuent les fonctions de dessin.</span><span class="sxs-lookup"><span data-stu-id="70bc8-181">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods described above perform the drawing functions.</span></span>

 

 