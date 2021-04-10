---
title: Comment combiner des géométries
description: Montre comment combiner deux géométries à l’aide de Direct2D.
ms.assetid: c5413e59-ae73-4797-b4ad-3a78ad700634
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8332421c62f49b60bb2186118ac7f741922fdc7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031566"
---
# <a name="how-to-combine-geometries"></a><span data-ttu-id="9fbcd-103">Comment combiner des géométries</span><span class="sxs-lookup"><span data-stu-id="9fbcd-103">How to Combine Geometries</span></span>

<span data-ttu-id="9fbcd-104">Cette rubrique décrit comment combiner deux géométries.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-104">This topic describes how to combine two geometries.</span></span> <span data-ttu-id="9fbcd-105">Direct2D prend en charge quatre modes pour combiner des géométries : Union, Intersect, XOR et Exclude.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-105">Direct2D supports four modes for combining geometries: Union, Intersect, XOR, and Exclude.</span></span> <span data-ttu-id="9fbcd-106">Ces modes sont spécifiés dans le type d’énumération du [**\_ \_ mode de combinaison d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) .</span><span class="sxs-lookup"><span data-stu-id="9fbcd-106">These modes are specified in the [**D2D1\_COMBINE\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) enum type.</span></span>

<span data-ttu-id="9fbcd-107">**Pour combiner deux géométries à l’aide de l’un des quatre modes**</span><span class="sxs-lookup"><span data-stu-id="9fbcd-107">**To combine two geometries by using any of the four modes**</span></span>

1.  <span data-ttu-id="9fbcd-108">Déclarer une géométrie de tracé : variable de type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) qui stocke le résultat de la combinaison Geometry.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-108">Declare a path geometry: a variable of type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) that will store the result of geometry combination.</span></span>
2.  <span data-ttu-id="9fbcd-109">Déclarer un récepteur de géométrie : variable de type [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) qui stocke la géométrie de tracé.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-109">Declare a geometry sink: a variable of type [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) that will store the path geometry.</span></span>
3.  <span data-ttu-id="9fbcd-110">Créez l’objet de géométrie Path en appelant la méthode [**ID2D1Factory :: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="9fbcd-110">Create the path geometry object by calling the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method.</span></span>
4.  <span data-ttu-id="9fbcd-111">Ouvrez l’objet de récepteur de géométrie en appelant la méthode [**ID2D1PathGeometry :: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .</span><span class="sxs-lookup"><span data-stu-id="9fbcd-111">Open the geometry sink object by calling the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>
5.  <span data-ttu-id="9fbcd-112">Utilisez l’un des quatre modes pour combiner les deux géométries en appelant la méthode [**ID2D1EllipseGeometry :: CombineWithGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) .</span><span class="sxs-lookup"><span data-stu-id="9fbcd-112">Use one of the four modes to combine the two geometries by calling the [**ID2D1EllipseGeometry::CombineWithGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) method.</span></span>
6.  <span data-ttu-id="9fbcd-113">Fermez l’objet de récepteur de géométrie.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-113">Close the geometry sink object.</span></span>

<span data-ttu-id="9fbcd-114">Le code suivant déclare les variables de type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) et **ID2D1GeometrySink**.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-114">The following code declares the variables of type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and **ID2D1GeometrySink**.</span></span>


```C++
    ID2D1PathGeometry *m_pPathGeometryUnion;
    ID2D1PathGeometry *m_pPathGeometryIntersect;
    ID2D1PathGeometry *m_pPathGeometryXOR;
    ID2D1PathGeometry *m_pPathGeometryExclude;
```



<span data-ttu-id="9fbcd-115">Le code suivant utilise chacun des quatre modes pour combiner les deux objets [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) et effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="9fbcd-115">The following code uses each of the four modes to combine the two [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects and performs the following actions:</span></span>

-   <span data-ttu-id="9fbcd-116">Crée deux ellipses, m \_ spEllipseGeometryOne et m \_ spEllipseGeometryTwo.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-116">Creates two ellipses, m\_spEllipseGeometryOne and m\_spEllipseGeometryTwo.</span></span>
-   <span data-ttu-id="9fbcd-117">Crée un objet de géométrie de tracé.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-117">Creates a path geometry object.</span></span>
-   <span data-ttu-id="9fbcd-118">Ouvre un objet récepteur de géométrie.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-118">Opens a geometry sink object.</span></span>
-   <span data-ttu-id="9fbcd-119">Combine les deux ellipses.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-119">Combines the two ellipses.</span></span>
-   <span data-ttu-id="9fbcd-120">Ferme l’objet de récepteur de géométrie.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-120">Closes the geometry sink object.</span></span>


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr = S_OK;
    ID2D1GeometrySink *pGeometrySink = NULL;

    // Create the first ellipse geometry to merge.
    const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
        D2D1::Point2F(75.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        circle1,
        &m_pCircleGeometry1
        );

    if (SUCCEEDED(hr))
    {
        // Create the second ellipse geometry to merge.
        const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
            D2D1::Point2F(125.0f, 75.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
    }


    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryUnion->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_UNION,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_INTERSECT to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryIntersect);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryIntersect->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_INTERSECT,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_XOR to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryXOR);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryXOR->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_XOR,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_EXCLUDE to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryExclude);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryExclude->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_EXCLUDE,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    return hr;
}
```



<span data-ttu-id="9fbcd-121">Ce code produit la sortie indiquée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="9fbcd-121">This code produces the output shown in the following illustration.</span></span>

![illustration de deux géométries et de quatre modes pour combiner les géométries (Union, intersection, XOR et exclure)](images/combine-modes.png)

## <a name="related-topics"></a><span data-ttu-id="9fbcd-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9fbcd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fbcd-124">**\_Mode de combinaison d2d1 \_**</span><span class="sxs-lookup"><span data-stu-id="9fbcd-124">**D2D1\_COMBINE\_MODE**</span></span>](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode)
</dt> <dt>

[<span data-ttu-id="9fbcd-125">**ID2D1EllipseGeometry**</span><span class="sxs-lookup"><span data-stu-id="9fbcd-125">**ID2D1EllipseGeometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)
</dt> <dt>

[<span data-ttu-id="9fbcd-126">**ID2D1PathGeometry**</span><span class="sxs-lookup"><span data-stu-id="9fbcd-126">**ID2D1PathGeometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)
</dt> <dt>

<span data-ttu-id="9fbcd-127">**ID2D1GeometrySink**</span><span class="sxs-lookup"><span data-stu-id="9fbcd-127">**ID2D1GeometrySink**</span></span>
</dt> </dl>

 

 