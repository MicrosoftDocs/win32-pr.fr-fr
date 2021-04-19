---
title: Comment dessiner et remplir une forme complexe
description: Direct2D fournit l’interface ID2D1PathGeometry pour décrire des formes complexes pouvant contenir des courbes, des arcs et des lignes. Cette rubrique décrit comment définir et restituer une géométrie de tracé.
ms.assetid: d7aad487-04e0-448d-bedf-b8dfadc7bbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a163e85d76a65f6b807ad1e4a9c9f740a32bf1
ms.sourcegitcommit: 4859402a45b9928c3e1354ded06b1d6a682a0be9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "106533287"
---
# <a name="how-to-draw-and-fill-a-complex-shape"></a>Comment dessiner et remplir une forme complexe

Direct2D fournit l’interface [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) pour décrire des formes complexes pouvant contenir des courbes, des arcs et des lignes. Cette rubrique décrit comment définir et restituer une géométrie de tracé.

Pour définir une géométrie de tracé, utilisez d’abord la méthode [**ID2D1Factory :: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) pour créer la géométrie du tracé, puis utilisez la méthode [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) de la géométrie du tracé pour récupérer un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink). Vous pouvez ensuite ajouter des lignes, des courbes et des arcs en appelant les différentes méthodes Add du récepteur.

L’exemple suivant crée un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), récupère un récepteur et l’utilise pour définir une forme de sablier.


```C++
ID2D1GeometrySink *pSink = NULL;

// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}
```

Notez qu’un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) est une ressource indépendante du périphérique et peut, par conséquent, être créé une fois et conservé pendant toute la durée de vie de l’application. (Pour plus d’informations sur les différents types de ressources, consultez la [vue d’ensemble des ressources](resources-and-resource-domains.md).)

L’exemple suivant crée deux pinceaux qui seront utilisés pour peindre le contour et le remplissage de la géométrie de tracé.


```C++
if (SUCCEEDED(hr))
{
    // Create a black brush.
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &m_pBlackBrush
        );
}

if (SUCCEEDED(hr))
{
    // Create a linear gradient.
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 0.25f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = m_pRenderTarget->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(100, 0),
                D2D1::Point2F(100, 200)),
            D2D1::BrushProperties(),
            pGradientStops,
            &m_pLGBrush
            );
    }

    SafeRelease(&pGradientStops);
}
```



Le dernier exemple utilise les méthodes [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) et [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) pour peindre le contour et l’intérieur de la géométrie. Cet exemple produit la sortie représentée dans l’illustration suivante.

![illustration d’une géométrie en forme de sablier](images/transformgeometryexample-1.png)


```C++
void DemoApp::RenderGeometryExample()
{
    // Translate subsequent drawings by 20 device-independent pixels.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Translation(20.f, 20.f)
        );

    // Draw the hour glass geometry at the upper left corner of the client area.
    m_pRenderTarget->DrawGeometry(m_pPathGeometry, m_pBlackBrush, 10.f);
    m_pRenderTarget->FillGeometry(m_pPathGeometry, m_pLGBrush);
}
```

Le code a été omis de cet exemple. Pour plus d’informations sur les géométries, consultez [vue d’ensemble des géométries](direct2d-geometries-overview.md).
