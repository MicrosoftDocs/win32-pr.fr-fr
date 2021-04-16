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
# <a name="how-to-draw-and-fill-a-basic-shape"></a>Comment dessiner et remplir une forme de base

Cette rubrique explique comment dessiner une forme de base. L’interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) fournit des méthodes pour le mode plan et le remplissage des ellipses, des rectangles et des lignes. Les exemples suivants montrent comment créer et dessiner une ellipse.

Cette rubrique contient les sections suivantes :

-   [Dessiner le contour d’une ellipse avec un trait plein](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [Dessiner une ellipse avec un trait en pointillés](#draw-an-ellipse-with-a-dashed-stroke)
-   [Dessiner et remplir une ellipse](#draw-and-fill-an-ellipse)
-   [Dessin de formes plus complexes](#drawing-more-complex-shapes)
-   [Rubriques connexes](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a>Dessiner le contour d’une ellipse avec un trait plein

Pour dessiner le contour d’une ellipse, vous définissez un pinceau (tel qu’un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ou [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) pour peindre le contour et une [**\_ ellipse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) pour décrire la position et les dimensions de l’ellipse, puis passer ces objets à la méthode [**ID2D1RenderTarget ::D rawellipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) . L’exemple suivant crée un pinceau de couleur unie noir et le stocke dans le membre de la \_ classe m spBlackBrush.


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



L’exemple suivant définit une [**\_ ellipse d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) et l’utilise avec le pinceau défini dans l’exemple précédent pour dessiner le contour d’une ellipse. Cet exemple produit la sortie représentée dans l’illustration suivante.

![illustration d’une ellipse avec un trait plein](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a>Dessiner une ellipse avec un trait en pointillés

L’exemple précédent utilisait un trait simple. Vous pouvez modifier l’apparence d’un trait de plusieurs façons en créant un [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle). Le **ID2D1StrokeStyle** vous permet de spécifier la forme au début et à la fin d’un trait, s’il a un modèle de tiret, et ainsi de suite. L’exemple suivant crée un **ID2D1StrokeStyle** qui décrit un trait en pointillés. Cet exemple utilise un modèle tiret prédéfini, d2d1 Dash [**\_ \_ style \_ tiret \_ point \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style)point, mais vous pouvez également spécifier le vôtre.


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



L’exemple suivant utilise le style Stroke avec la méthode [**DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) . Cet exemple produit la sortie représentée dans l’illustration suivante.

![illustration d’une ellipse avec un trait en pointillés](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a>Dessiner et remplir une ellipse

Pour peindre l’intérieur d’une ellipse, vous utilisez la méthode [**FillEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) . L’exemple suivant utilise la méthode [**DrawEllipse**]/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse (constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) pour dessiner l’ellipse, puis utilise la méthode **FillEllipse** pour peindre son intérieur. Cet exemple produit la sortie représentée dans l’illustration suivante.

![illustration d’une ellipse avec un trait en pointillés, puis remplie d’une couleur grise unie](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



L’exemple suivant remplit d’abord l’ellipse, puis dessine son contour. Cet exemple produit la sortie représentée dans l’illustration suivante.

![illustration d’une Ellipse remplie d’une couleur grise unie, puis délimitée par un trait en pointillés](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



Le code a été omis dans ces exemples.

## <a name="drawing-more-complex-shapes"></a>Dessin de formes plus complexes

Pour dessiner des formes plus complexes, vous définissez des objets ID2D1Geometry et vous les utilisez avec les méthodes [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) et [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) . Pour plus d’informations, consultez [vue d’ensemble des géométries](direct2d-geometries-overview.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des géométries](direct2d-geometries-overview.md)
</dt> <dt>

[Vue d’ensemble des pinceaux](direct2d-brushes-overview.md)
</dt> </dl>

 

 