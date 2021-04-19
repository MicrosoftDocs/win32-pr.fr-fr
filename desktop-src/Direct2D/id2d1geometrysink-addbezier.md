---
title: Méthodes ID2D1GeometrySink AddBezier (D2d1. h)
description: Crée une courbe de Bézier cubique entre le point actuel et le point de terminaison spécifié et l’ajoute au récepteur de géométrie.
ms.assetid: d1e228eb-dac6-485d-b3c9-69b2bd45e531
keywords:
- Méthodes AddBezier Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b470129350463920583c34bec5f886f60b16485e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543836"
---
# <a name="id2d1geometrysinkaddbezier-methods"></a><span data-ttu-id="99a44-104">ID2D1GeometrySink :: AddBezier, méthodes</span><span class="sxs-lookup"><span data-stu-id="99a44-104">ID2D1GeometrySink::AddBezier methods</span></span>

<span data-ttu-id="99a44-105">Crée une courbe de Bézier cubique entre le point actuel et le point de terminaison spécifié et l’ajoute au récepteur de géométrie.</span><span class="sxs-lookup"><span data-stu-id="99a44-105">Creates a cubic Bezier curve between the current point and the specified end point and adds it to the geometry sink.</span></span>

### <a name="overload-list"></a><span data-ttu-id="99a44-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="99a44-106">Overload list</span></span>



| <span data-ttu-id="99a44-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="99a44-107">Method</span></span>                                                                                            | <span data-ttu-id="99a44-108">Description</span><span class="sxs-lookup"><span data-stu-id="99a44-108">Description</span></span>                                                                                    |
|:--------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="99a44-109">[**AddBezier ( \_ segment de Bézier D2D1 \_&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))</span><span class="sxs-lookup"><span data-stu-id="99a44-109">[**AddBezier(D2D1\_BEZIER\_SEGMENT&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))</span></span>  | <span data-ttu-id="99a44-110">Crée une courbe de Bézier cubique lissée entre le point actuel et le point de fin spécifié.</span><span class="sxs-lookup"><span data-stu-id="99a44-110">Creates a cubic Bezier curve between the current point and the specified end point.</span></span><br/> |
| <span data-ttu-id="99a44-111">[**AddBezier ( \_ segment de Bézier d2d1 \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment))</span><span class="sxs-lookup"><span data-stu-id="99a44-111">[**AddBezier(D2D1\_BEZIER\_SEGMENT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment))</span></span> | <span data-ttu-id="99a44-112">Crée une courbe de Bézier cubique entre le point actuel et le point de terminaison spécifié.</span><span class="sxs-lookup"><span data-stu-id="99a44-112">Creates a cubic Bezier curve between the current point and the specified endpoint.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="99a44-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="99a44-113">Examples</span></span>

<span data-ttu-id="99a44-114">L’exemple suivant crée un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), récupère un récepteur et l’utilise pour définir une forme de sablier.</span><span class="sxs-lookup"><span data-stu-id="99a44-114">The following example creates an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), retrieves a sink, and uses it to define an hourglass shape.</span></span> <span data-ttu-id="99a44-115">Pour obtenir un exemple complet, consultez [Comment dessiner et remplir une forme complexe](how-to-draw-and-fill-a-complex-shape.md).</span><span class="sxs-lookup"><span data-stu-id="99a44-115">For the complete example, see [How to Draw and Fill a Complex Shape](how-to-draw-and-fill-a-complex-shape.md).</span></span>


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





## <a name="requirements"></a><span data-ttu-id="99a44-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99a44-116">Requirements</span></span>



| <span data-ttu-id="99a44-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99a44-117">Requirement</span></span> | <span data-ttu-id="99a44-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="99a44-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="99a44-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="99a44-119">Header</span></span><br/>  | <dl> <span data-ttu-id="99a44-120"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="99a44-120"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="99a44-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99a44-121">Library</span></span><br/> | <dl> <span data-ttu-id="99a44-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99a44-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="99a44-123">DLL</span><span class="sxs-lookup"><span data-stu-id="99a44-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="99a44-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99a44-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99a44-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99a44-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99a44-126">**ID2D1GeometrySink**</span><span class="sxs-lookup"><span data-stu-id="99a44-126">**ID2D1GeometrySink**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)
</dt> </dl>

<span data-ttu-id="99a44-127">�</span><span class="sxs-lookup"><span data-stu-id="99a44-127">�</span></span>

<span data-ttu-id="99a44-128">�</span><span class="sxs-lookup"><span data-stu-id="99a44-128">�</span></span>
