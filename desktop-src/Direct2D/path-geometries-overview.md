---
title: Vue d’ensemble des géométries de tracés
description: Décrit comment utiliser des géométries de tracés pour définir des formes complexes.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104551472"
---
# <a name="path-geometries-overview"></a>Vue d’ensemble des géométries de tracés

Cette rubrique explique comment utiliser des géométries de tracés Direct2D pour créer des dessins complexes. Elle contient les sections suivantes.

-   [Conditions préalables](#prerequisites)
-   [Géométries de tracés dans Direct2D](#path-geometries-in-direct2d)
-   [Utilisation d’un ID2D1GeometrySink pour remplir une géométrie de tracé](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [Exemple : créer un dessin complexe](#example-create-a-complex-drawing)
    -   [Créer une géométrie de tracé pour la montagne de gauche](#create-a-path-geometry-for-the-left-mountain)
    -   [Créer une géométrie de tracé pour la montagne droite](#create-a-path-geometry-for-the-right-mountain)
    -   [Créer une géométrie de tracé pour le soleil](#create-a-path-geometry-for-the-sun)
    -   [Créer une géométrie de tracé pour la rivière](#create-a-path-geometry-for-the-river)
    -   [Restituer les géométries de tracés sur l’affichage](#render-the-path-geometries-onto-the-display)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Cette vue d’ensemble suppose que vous êtes familiarisé avec la création d’applications Direct2D de base, comme décrit dans [création d’une application Direct2d simple](direct2d-quickstart.md). Elle suppose également que vous êtes familiarisé avec les fonctionnalités de base des géométries Direct2D, comme décrit dans la [vue d’ensemble des géométries](direct2d-geometries-overview.md).

## <a name="path-geometries-in-direct2d"></a>Géométries de tracés dans Direct2D

Les géométries de tracés sont représentées par l’interface [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Pour instancier une géométrie de tracé, appelez la méthode [**ID2D1Factory :: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) . Ces objets peuvent être utilisés pour décrire des chiffres géométriques complexes composés de segments tels que des arcs, des courbes et des lignes. Pour remplir une géométrie de tracé avec des figures et des segments, appelez la méthode [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) pour récupérer un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) et utilisez les méthodes du récepteur Geometry pour ajouter des figures et des segments à la géométrie de tracé.

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a>Utilisation d’un ID2D1GeometrySink pour remplir une géométrie de tracé

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) décrit un tracé géométrique qui peut contenir des lignes, des arcs, des courbes de Bézier cubiques et des courbes de Bézier quadratiques.

Un récepteur de géométrie se compose d’un ou de plusieurs figures. Chaque figure est constituée d’un ou de plusieurs segments de ligne, de courbe ou d’arc. Pour créer une figure, appelez la méthode [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) , en passant le point de départ de la figure, puis utilisez ses méthodes Add (telles que [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) et [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) pour ajouter des segments. Lorsque vous avez terminé d’ajouter des segments, appelez la méthode [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) . Vous pouvez répéter cette séquence pour créer des chiffres supplémentaires. Lorsque vous avez terminé de créer des figures, appelez la méthode [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .

## <a name="example-create-a-complex-drawing"></a>Exemple : créer un dessin complexe

L’illustration suivante montre un dessin complexe avec des courbes, des arcs et des courbes de Bézier. L’exemple de code suivant montre comment créer le dessin à l’aide de quatre objets Geometry, un pour la montagne gauche, un pour la montagne droite, un pour le fleuve et un pour le soleil avec des halos.

![illustration d’une rivière, de montagnes et du soleil, à l’aide de géométries de tracés](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a>Créer une géométrie de tracé pour la montagne de gauche

L’exemple crée d’abord une géométrie de tracé pour le VTT gauche, comme indiqué dans l’illustration suivante.

![Montre un dessin complexe d’un polygone qui affiche une montagne.](images/path-geo-leftmnt.png)

Pour créer la montagne de gauche, l’exemple appelle la méthode [**ID2D1Factory :: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) pour créer un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



L’exemple utilise ensuite la méthode [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) pour obtenir un récepteur Geometry à partir d’un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) et le stocke dans la variable *pSink* .


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



L’exemple appelle ensuite [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), en passant le début de la [**\_ figure d2d1 \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) , qui indique que cette figure est remplie, puis appelle [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), en passant un tableau de points de [**d2d1 \_ point \_ 2F**](d2d1-point-2f.md) , (267, 177), (236, 192), (212, 160), (156, 255) et (346, 255).

Le code suivant montre comment procéder.


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a>Créer une géométrie de tracé pour la montagne droite

L’exemple crée ensuite une autre géométrie de tracé pour la montagne droite avec des points (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) et (575, 263). L’illustration suivante montre l’affichage de la montagne droite.

![illustration d’un polygone montrant une montagne](images/path-geo-rightmnt.png)

Le code suivant montre comment procéder.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a>Créer une géométrie de tracé pour le soleil

L’exemple remplit ensuite une autre géométrie de tracé pour le soleil, comme indiqué dans l’illustration suivante.

![illustration d’un arc et de courbes Bézier montrant le soleil](images/path-geo-sun.png)

Pour ce faire, la géométrie du tracé crée un récepteur et ajoute une figure pour l’arc et une figure pour chaque Halo au récepteur. En répétant la séquence de [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), ses méthodes Add (telles que [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) et [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), plusieurs figures sont ajoutées au récepteur.

Le code suivant montre comment procéder.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a>Créer une géométrie de tracé pour la rivière

L’exemple crée ensuite un autre tracé géométrique pour la rivière qui contient des courbes de Bézier. L’illustration suivante montre comment la rivière est affichée.

![illustration des courbes Bézier montrant une rivière](images/path-geo-river.png)

Le code suivant montre comment procéder.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a>Restituer les géométries de tracés sur l’affichage

Le code suivant montre comment restituer les géométries de tracés remplies sur l’affichage. Il commence par dessiner et peint la géométrie du soleil, puis la géométrie de montagne gauche, la géométrie de la rivière et enfin la bonne géométrie de montagne.


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



L’exemple complet présente l’illustration suivante.

![illustration d’une rivière, de montagnes et du soleil, à l’aide de géométries de tracés](images/path-geo-mnts.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une application Direct2D simple](direct2d-quickstart.md)
</dt> <dt>

[Vue d’ensemble des géométries](direct2d-geometries-overview.md)
</dt> </dl>

 

 