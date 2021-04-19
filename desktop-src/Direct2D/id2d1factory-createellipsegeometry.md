---
title: Méthodes ID2D1Factory CreateEllipseGeometry (D2d1. h)
description: Crée un ID2D1EllipseGeometry.
ms.assetid: 4c03bb0b-74fe-456a-aa26-5449d758c0ea
keywords:
- Méthodes CreateEllipseGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ca991732b9a80fd93e3df3c2b72493f5195ea0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534773"
---
# <a name="id2d1factorycreateellipsegeometry-methods"></a><span data-ttu-id="64af7-104">ID2D1Factory :: CreateEllipseGeometry, méthodes</span><span class="sxs-lookup"><span data-stu-id="64af7-104">ID2D1Factory::CreateEllipseGeometry methods</span></span>

<span data-ttu-id="64af7-105">Crée un [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span><span class="sxs-lookup"><span data-stu-id="64af7-105">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span>

### <a name="overload-list"></a><span data-ttu-id="64af7-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="64af7-106">Overload list</span></span>



| <span data-ttu-id="64af7-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="64af7-107">Method</span></span>                                                                                                                                                      | <span data-ttu-id="64af7-108">Description</span><span class="sxs-lookup"><span data-stu-id="64af7-108">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="64af7-109">[**CreateEllipseGeometry (D2D1 \_ ELLIPSE&, ID2D1EllipseGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry))</span><span class="sxs-lookup"><span data-stu-id="64af7-109">[**CreateEllipseGeometry(D2D1\_ELLIPSE&,ID2D1EllipseGeometry\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry))</span></span>  | <span data-ttu-id="64af7-110">Crée un [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span><span class="sxs-lookup"><span data-stu-id="64af7-110">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span> <br/> |
| <span data-ttu-id="64af7-111">[**CreateEllipseGeometry (D2D1 \_ ellipse \* , ID2D1EllipseGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371265(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64af7-111">[**CreateEllipseGeometry(D2D1\_ELLIPSE\*,ID2D1EllipseGeometry\*\*)**](/previous-versions/windows/desktop/legacy/dd371265(v=vs.85))</span></span> | <span data-ttu-id="64af7-112">Crée un [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span><span class="sxs-lookup"><span data-stu-id="64af7-112">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="64af7-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="64af7-113">Examples</span></span>

<span data-ttu-id="64af7-114">Le code suivant crée deux objets [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) et les combine à l’aide des différents modes de combinaison Geometry.</span><span class="sxs-lookup"><span data-stu-id="64af7-114">The following creates two [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects and combines them using the different geometry combine modes.</span></span>


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



<span data-ttu-id="64af7-115">Ce code produit la sortie indiquée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="64af7-115">This code produces the output shown in the following illustration.</span></span>

![illustration de deux ellipses combinées à l’aide de quatre modes de combinaison Geometry (Union, Intersect, XOR et Exclude)](images/combine-modes.png)

## <a name="requirements"></a><span data-ttu-id="64af7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64af7-117">Requirements</span></span>



| <span data-ttu-id="64af7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64af7-118">Requirement</span></span> | <span data-ttu-id="64af7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="64af7-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="64af7-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="64af7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="64af7-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="64af7-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="64af7-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="64af7-122">Library</span></span><br/> | <dl> <span data-ttu-id="64af7-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64af7-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="64af7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="64af7-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="64af7-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64af7-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64af7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64af7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64af7-127">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="64af7-127">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
