---
title: Comment dessiner et remplir une forme de base
description: Cette rubrique explique comment dessiner une forme de base.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6b6b5a6fb08ac962475c2f0aa2812b4c3ae5da03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104559819"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a><span data-ttu-id="d7773-103">Comment dessiner et remplir une forme de base</span><span class="sxs-lookup"><span data-stu-id="d7773-103">How to Draw and Fill a Basic Shape</span></span>

<span data-ttu-id="d7773-104">Cette rubrique explique comment dessiner une forme de base.</span><span class="sxs-lookup"><span data-stu-id="d7773-104">This topic describes how to draw a basic shape.</span></span> <span data-ttu-id="d7773-105">L’interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) fournit des méthodes pour le mode plan et le remplissage des ellipses, des rectangles et des lignes.</span><span class="sxs-lookup"><span data-stu-id="d7773-105">The [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface provides methods for outlining and filling ellipses, rectangles, and lines.</span></span> <span data-ttu-id="d7773-106">Les exemples suivants montrent comment créer et dessiner une ellipse.</span><span class="sxs-lookup"><span data-stu-id="d7773-106">The following examples show how to create and draw an ellipse.</span></span>

<span data-ttu-id="d7773-107">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7773-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d7773-108">Dessiner le contour d’une ellipse avec un trait plein</span><span class="sxs-lookup"><span data-stu-id="d7773-108">Draw the Outline of an Ellipse with a Solid Stroke</span></span>](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [<span data-ttu-id="d7773-109">Dessiner une ellipse avec un trait en pointillés</span><span class="sxs-lookup"><span data-stu-id="d7773-109">Draw an Ellipse with a Dashed Stroke</span></span>](#draw-an-ellipse-with-a-dashed-stroke)
-   [<span data-ttu-id="d7773-110">Dessiner et remplir une ellipse</span><span class="sxs-lookup"><span data-stu-id="d7773-110">Draw and Fill an Ellipse</span></span>](#draw-and-fill-an-ellipse)
-   [<span data-ttu-id="d7773-111">Dessin de formes plus complexes</span><span class="sxs-lookup"><span data-stu-id="d7773-111">Drawing More Complex Shapes</span></span>](#drawing-more-complex-shapes)
-   [<span data-ttu-id="d7773-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d7773-112">Related topics</span></span>](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a><span data-ttu-id="d7773-113">Dessiner le contour d’une ellipse avec un trait plein</span><span class="sxs-lookup"><span data-stu-id="d7773-113">Draw the Outline of an Ellipse with a Solid Stroke</span></span>

<span data-ttu-id="d7773-114">Pour dessiner le contour d’une ellipse, vous définissez un pinceau (tel qu’un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ou [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) pour peindre le contour et une [**\_ ellipse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) pour décrire la position et les dimensions de l’ellipse, puis passer ces objets à la méthode [**ID2D1RenderTarget ::D rawellipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) .</span><span class="sxs-lookup"><span data-stu-id="d7773-114">To draw the outline of an ellipse, you define a brush (such as a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) for painting the outline and a [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) for describing the ellipse's position and dimensions, then pass these objects to the [**ID2D1RenderTarget::DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="d7773-115">L’exemple suivant crée un pinceau de couleur unie noir et le stocke dans le membre de la \_ classe m spBlackBrush.</span><span class="sxs-lookup"><span data-stu-id="d7773-115">The following example creates a black solid color brush and stores it in the m\_spBlackBrush class member.</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



<span data-ttu-id="d7773-116">L’exemple suivant définit une [**\_ ellipse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) et l’utilise avec le pinceau défini dans l’exemple précédent pour dessiner le contour d’une ellipse.</span><span class="sxs-lookup"><span data-stu-id="d7773-116">The next example defines an [**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) and uses it with the brush defined in the previous example to draw the outline of an ellipse.</span></span> <span data-ttu-id="d7773-117">Cet exemple produit la sortie représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d7773-117">This example produces the output shown in the following illustration.</span></span>

![illustration d’une ellipse avec un trait plein](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a><span data-ttu-id="d7773-119">Dessiner une ellipse avec un trait en pointillés</span><span class="sxs-lookup"><span data-stu-id="d7773-119">Draw an Ellipse with a Dashed Stroke</span></span>

<span data-ttu-id="d7773-120">L’exemple précédent utilisait un trait simple.</span><span class="sxs-lookup"><span data-stu-id="d7773-120">The preceding example used a plain stroke.</span></span> <span data-ttu-id="d7773-121">Vous pouvez modifier l’apparence d’un trait de plusieurs façons en créant un [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span><span class="sxs-lookup"><span data-stu-id="d7773-121">You can modify the look of a stroke in several ways by creating an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle).</span></span> <span data-ttu-id="d7773-122">Le **ID2D1StrokeStyle** vous permet de spécifier la forme au début et à la fin d’un trait, s’il a un modèle de tiret, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d7773-122">The **ID2D1StrokeStyle** lets you specify the shape at the beginning and end of a stroke, whether it has a dash pattern, and so on.</span></span> <span data-ttu-id="d7773-123">L’exemple suivant crée un **ID2D1StrokeStyle** qui décrit un trait en pointillés.</span><span class="sxs-lookup"><span data-stu-id="d7773-123">The following example creates an **ID2D1StrokeStyle** that describes a dashed stroke.</span></span> <span data-ttu-id="d7773-124">Cet exemple utilise un modèle tiret prédéfini, d2d1 Dash [**\_ \_ style \_ tiret \_ point \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style)point, mais vous pouvez également spécifier le vôtre.</span><span class="sxs-lookup"><span data-stu-id="d7773-124">This example uses a predefined dash pattern, [**D2D1\_DASH\_STYLE\_DASH\_DOT\_DOT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), but you can also specify your own.</span></span>


```C++
D2D1_STROKE_STYLE_PROPERTIES strokeStyleProperties = D2D1::StrokeStyleProperties(
    D2D1_CAP_STYLE_FLAT,  // The start cap.
    D2D1_CAP_STYLE_FLAT,  // The end cap.
    D2D1_CAP_STYLE_TRIANGLE, // The dash cap.
    D2D1_LINE_JOIN_MITER, // The line join.
    10.0f, // The miter limit.
    D2D1_DASH_STYLE_DASH_DOT_DOT, // The dash style.
    0.0f // The dash offset.
    );

hr = m_pDirect2dFactory->CreateStrokeStyle(strokeStyleProperties, NULL, 0, &m_pStrokeStyle);

```



<span data-ttu-id="d7773-125">L’exemple suivant utilise le style Stroke avec la méthode [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) .</span><span class="sxs-lookup"><span data-stu-id="d7773-125">The next example uses the stroke style with the [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method.</span></span> <span data-ttu-id="d7773-126">Cet exemple produit la sortie représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d7773-126">This example produces the output shown in the following illustration.</span></span>

![illustration d’une ellipse avec un trait en pointillés](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a><span data-ttu-id="d7773-128">Dessiner et remplir une ellipse</span><span class="sxs-lookup"><span data-stu-id="d7773-128">Draw and Fill an Ellipse</span></span>

<span data-ttu-id="d7773-129">Pour peindre l’intérieur d’une ellipse, vous utilisez la méthode [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) .</span><span class="sxs-lookup"><span data-stu-id="d7773-129">To paint the interior of an ellipse, you use the [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method.</span></span> <span data-ttu-id="d7773-130">L’exemple suivant utilise la méthode [**DrawEllipse**]/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse (constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) pour dessiner l’ellipse, puis utilise la méthode **FillEllipse** pour peindre son intérieur.</span><span class="sxs-lookup"><span data-stu-id="d7773-130">The following example uses the [**DrawEllipse**]/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) method to outline the ellipse, then uses the **FillEllipse** method to paint its interior.</span></span> <span data-ttu-id="d7773-131">Cet exemple produit la sortie représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d7773-131">This example produces the output shown in the following illustration.</span></span>

![illustration d’une ellipse avec un trait en pointillés, puis remplie d’une couleur grise unie](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



<span data-ttu-id="d7773-133">L’exemple suivant remplit d’abord l’ellipse, puis dessine son contour.</span><span class="sxs-lookup"><span data-stu-id="d7773-133">The next example fills the ellipse first, then draws its outline.</span></span> <span data-ttu-id="d7773-134">Cet exemple produit la sortie représentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d7773-134">This example produces the output shown in the following illustration.</span></span>

![illustration d’une Ellipse remplie d’une couleur grise unie, puis délimitée par un trait en pointillés](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



<span data-ttu-id="d7773-136">Le code a été omis dans ces exemples.</span><span class="sxs-lookup"><span data-stu-id="d7773-136">Code has been omitted from these examples.</span></span>

## <a name="drawing-more-complex-shapes"></a><span data-ttu-id="d7773-137">Dessin de formes plus complexes</span><span class="sxs-lookup"><span data-stu-id="d7773-137">Drawing More Complex Shapes</span></span>

<span data-ttu-id="d7773-138">Pour dessiner des formes plus complexes, vous définissez des objets ID2D1Geometry et vous les utilisez avec les méthodes [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) et [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="d7773-138">To draw more complex shapes, you define ID2D1Geometry objects and use them with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods.</span></span> <span data-ttu-id="d7773-139">Pour plus d’informations, consultez [vue d’ensemble des géométries](direct2d-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d7773-139">For more information, see the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7773-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d7773-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7773-141">Vue d’ensemble des géométries</span><span class="sxs-lookup"><span data-stu-id="d7773-141">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="d7773-142">Vue d’ensemble des pinceaux</span><span class="sxs-lookup"><span data-stu-id="d7773-142">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

 

 