---
title: Comment transformer une géométrie
description: Montre comment transformer une géométrie à l’aide de Direct2D.
ms.assetid: de434615-14b1-4b66-b09b-e90468e03d58
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ae15d0b1da304f9dfe24ff5de33a9f1582e2ca05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509871"
---
# <a name="how-to-transform-a-geometry"></a><span data-ttu-id="ccbe0-103">Comment transformer une géométrie</span><span class="sxs-lookup"><span data-stu-id="ccbe0-103">How to Transform a Geometry</span></span>

<span data-ttu-id="ccbe0-104">Pour transformer une géométrie, vous pouvez appliquer la transformation à la cible de rendu en appelant [**setTransform**](id2d1rendertarget-settransform.md) ou appliquer la transformation à la géométrie en appelant [**CreateTransformedGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)).</span><span class="sxs-lookup"><span data-stu-id="ccbe0-104">To transform a geometry, you can either apply the transform to the render target by calling [**SetTransform**](id2d1rendertarget-settransform.md) or apply the transform to the geometry by calling [**CreateTransformedGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)).</span></span> <span data-ttu-id="ccbe0-105">Bien que les deux approches transforment une géométrie, elles présentent des différences fondamentales.</span><span class="sxs-lookup"><span data-stu-id="ccbe0-105">Although both approaches transform a geometry, they have some fundamental differences.</span></span> <span data-ttu-id="ccbe0-106">**CreateTransformedGeometry** affecte le remplissage, mais n’affecte pas la largeur du trait.</span><span class="sxs-lookup"><span data-stu-id="ccbe0-106">**CreateTransformedGeometry** affects the fill, but does not affect the stroke width.</span></span> <span data-ttu-id="ccbe0-107">En outre, **CreateTransformedGeometry** transforme la géométrie seule sans affecter les autres formes sur la cible de rendu, tandis que [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) applique la transformation à toutes les formes sur la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="ccbe0-107">Further, **CreateTransformedGeometry** transforms the geometry alone without impacting other shapes on the render target, whereas [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) applies the transform to all shapes on the render target.</span></span>

<span data-ttu-id="ccbe0-108">Cette rubrique de procédure explique comment transformer une géométrie en appelant [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)).</span><span class="sxs-lookup"><span data-stu-id="ccbe0-108">This how-to topic describes how to transform a geometry by calling [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)).</span></span>

<span data-ttu-id="ccbe0-109">**Pour transformer une géométrie**</span><span class="sxs-lookup"><span data-stu-id="ccbe0-109">**To transform a geometry**</span></span>

1.  <span data-ttu-id="ccbe0-110">Déclarez une variable [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) .</span><span class="sxs-lookup"><span data-stu-id="ccbe0-110">Declare an [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) variable.</span></span>
2.  <span data-ttu-id="ccbe0-111">Appelez la méthode [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) pour créer une géométrie transformée.</span><span class="sxs-lookup"><span data-stu-id="ccbe0-111">Call the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) method to create a transformed geometry.</span></span>

<span data-ttu-id="ccbe0-112">Le code suivant montre comment créer un sablier, transformer le verre des heures et dessiner les lunettes d’heure d’origine et de résultat.</span><span class="sxs-lookup"><span data-stu-id="ccbe0-112">The following code shows how to create an hour glass, transform the hour glass, and draw the original and resulting hour glasses.</span></span>


```C++
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

if (SUCCEEDED(hr))
{
    // Create a transformed geometry which is tilted at an angle to the previous geometry
    hr = m_pD2DFactory->CreateTransformedGeometry(
        m_pPathGeometry,
        D2D1::Matrix3x2F::Rotation(
            45.f,
            D2D1::Point2F(100, 100)),
        &m_pTransformedGeometry
        );
}
```



 

 