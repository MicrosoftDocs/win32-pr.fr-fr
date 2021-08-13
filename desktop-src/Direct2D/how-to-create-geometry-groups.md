---
title: Comment créer des groupes de géométrie
description: Cette rubrique décrit comment créer des groupes géométriques.
ms.assetid: be364440-75ab-4d8f-a359-39da275272fd
keywords:
- Direct2D, exemple de mode de remplissage
- groupes géométriques
- Direct2D, groupes géométriques
- géométries de tracés
- Direct2D, géométries de tracés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5540d96b9befddaa8eb6eef7fcc61e3e6c7665a7319de1ea123c9ce94281f101
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259249"
---
# <a name="how-to-create-geometry-groups"></a>Comment créer des groupes de géométrie

Cette rubrique décrit comment créer des groupes géométriques.

Pour créer un groupe Geometry, appelez la méthode [**ID2D1Factory :: CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) et spécifiez un tableau de géométries et un mode de remplissage.

Lorsque vous combinez des géométries dans un groupe Geometry, assurez-vous que les géométries sont orientées de la même façon. Si vous n’êtes pas sûr de l’orientation des géométries, appelez [**ID2D1Geometry :: Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink)) sur chacun d’eux individuellement, puis insérez les géométries résultantes dans le groupe Geometry.

L’exemple de code suivant illustre la création de quatre cercles concentriques : le premier cercle a un rayon de 25, le deuxième 50, le troisième 75 et le quatrième 100. Le code montre également l’instanciation d’un tableau de géométries, ainsi que les deux appels à [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup).


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr;

    const D2D1_ELLIPSE ellipse1 = D2D1::Ellipse(
        D2D1::Point2F(105.0f, 105.0f),
        25.0f,
        25.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        ellipse1,
        &m_pEllipseGeometry1
        );

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse2 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse2,
            &m_pEllipseGeometry2
            );
    }

    if (SUCCEEDED(hr))
    {

        const D2D1_ELLIPSE ellipse3 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            75.0f,
            75.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse3,
            &m_pEllipseGeometry3
            );
    }

    if (SUCCEEDED(hr))
    {
        const D2D1_ELLIPSE ellipse4 = D2D1::Ellipse(
            D2D1::Point2F(105.0f, 105.0f),
            100.0f,
            100.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(
            ellipse4,
            &m_pEllipseGeometry4
            );
    }

    if (SUCCEEDED(hr))
    {
        ID2D1Geometry *ppGeometries[] =
        {
            m_pEllipseGeometry1,
            m_pEllipseGeometry2,
            m_pEllipseGeometry3,
            m_pEllipseGeometry4
        };

        hr = m_pD2DFactory->CreateGeometryGroup(
            D2D1_FILL_MODE_ALTERNATE,
            ppGeometries,
            ARRAYSIZE(ppGeometries),
            &m_pGeoGroup_AlternateFill
            );

        if (SUCCEEDED(hr))
        {
            hr = m_pD2DFactory->CreateGeometryGroup(
                D2D1_FILL_MODE_WINDING,
                ppGeometries,
                ARRAYSIZE(ppGeometries),
                &m_pGeoGroup_WindingFill
                );
        }

    }
    return hr;
}
```



## <a name="drawing-and-filling-of-geometry-groups"></a>Dessin et remplissage de groupes géométriques

Pour dessiner et remplir un groupe Geometry, utilisez les méthodes [**ID2D1RenderTarget :: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) et [**ID2D1RenderTarget ::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) . L’exemple de code suivant montre comment dessiner et remplir un groupe Geometry.


```C++
HRESULT DemoApp::OnRender()
{
    HRESULT hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_fillModeAlternateText[] = L"D2D1_FILL_MODE_ALTERNATE";
        static const WCHAR sc_fillModeWindingText[] = L"D2D1_FILL_MODE_WINDING";

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, rtSize.width, rtSize.height),
            m_pGridPatternBitmapBrush
            );

        // Centers the text in a layout rectangle.
        hr = m_pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);

        if (SUCCEEDED(hr))
        {
            // Fill the geometry group with D2D1_FILL_MODE_ALTERNATE and
            // then draw the geometries in the group.
            m_pRenderTarget->FillGeometry(m_pGeoGroup_AlternateFill, m_pFillBrush);
            m_pRenderTarget->DrawGeometry(m_pGeoGroup_AlternateFill, m_pStrokeBrush, 1.0f);

            m_pRenderTarget->DrawText(
                sc_fillModeAlternateText,
                ARRAYSIZE(sc_fillModeAlternateText) - 1,
                m_pTextFormat,
                D2D1::RectF(5, 215, 205, 240),
                m_pStrokeBrush,
                D2D1_DRAW_TEXT_OPTIONS_NONE,
                DWRITE_MEASURING_MODE_NATURAL
                );

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

            // Fill the geometry group with D2D1_FILL_MODE_WINDING and
            // then draw the geometries in the group.
            m_pRenderTarget->FillGeometry(m_pGeoGroup_WindingFill, m_pFillBrush);
            m_pRenderTarget->DrawGeometry(m_pGeoGroup_WindingFill, m_pStrokeBrush, 1.0f);

            m_pRenderTarget->DrawText(
                sc_fillModeWindingText,
                ARRAYSIZE(sc_fillModeWindingText) - 1,
                m_pTextFormat,
                D2D1::RectF(5, 215, 205, 240),
                m_pStrokeBrush,
                D2D1_DRAW_TEXT_OPTIONS_NONE,
                DWRITE_MEASURING_MODE_NATURAL
                );

            hr = m_pRenderTarget->EndDraw();

            if (hr == D2DERR_RECREATE_TARGET)
            {
                hr = S_OK;
                DiscardDeviceResources();
            }
        }
    }
    return hr;
}
```



Le code génère la sortie illustrée dans l’illustration suivante.

![illustration de deux jeux de quatre cercles concentriques, un avec les deuxième et quatrième anneaux remplis et un avec tous les anneaux remplis](images/create-geometry-group.png)

 

 