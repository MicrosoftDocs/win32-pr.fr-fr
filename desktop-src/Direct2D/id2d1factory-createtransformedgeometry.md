---
title: Méthodes ID2D1Factory CreateTransformedGeometry (D2d1. h)
description: Transforme la géométrie spécifiée et stocke le résultat sous la forme d’un objet ID2D1TransformedGeometry.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- Méthodes CreateTransformedGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5da3b548c3118209c915714e03fe9e4061c77e96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537402"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a><span data-ttu-id="7c42a-104">ID2D1Factory :: CreateTransformedGeometry, méthodes</span><span class="sxs-lookup"><span data-stu-id="7c42a-104">ID2D1Factory::CreateTransformedGeometry methods</span></span>

<span data-ttu-id="7c42a-105">Transforme la géométrie spécifiée et stocke le résultat sous la forme d’un objet [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7c42a-105">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="7c42a-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="7c42a-106">Overload list</span></span>



| <span data-ttu-id="7c42a-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="7c42a-107">Method</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="7c42a-108">Description</span><span class="sxs-lookup"><span data-stu-id="7c42a-108">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c42a-109">[**CreateTransformedGeometry (ID2D1Geometry \* , \_ matrice D2D \_ matrice \_ F \* , ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7c42a-109">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F\*,ID2D1TransformedGeometry\*\*)**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span></span> | <span data-ttu-id="7c42a-110">Transforme la géométrie spécifiée et stocke le résultat sous la forme d’un objet [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7c42a-110">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |
| <span data-ttu-id="7c42a-111">[**CreateTransformedGeometry (ID2D1Geometry \* , \_ matrice D2D \_ matrice \_ F&, ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span><span class="sxs-lookup"><span data-stu-id="7c42a-111">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F&,ID2D1TransformedGeometry\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span></span>  | <span data-ttu-id="7c42a-112">Transforme la géométrie spécifiée et stocke le résultat sous la forme d’un objet [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7c42a-112">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="7c42a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7c42a-113">Remarks</span></span>

<span data-ttu-id="7c42a-114">Comme les autres ressources, une géométrie transformée hérite de l’espace de ressources et de la stratégie de thread de la fabrique qui l’a créée.</span><span class="sxs-lookup"><span data-stu-id="7c42a-114">Like other resources, a transformed geometry inherits the resource space and threading policy of the factory that created it.</span></span> <span data-ttu-id="7c42a-115">Cet objet est immuable.</span><span class="sxs-lookup"><span data-stu-id="7c42a-115">This object is immutable.</span></span>

<span data-ttu-id="7c42a-116">Lors du découpage d’une géométrie transformée à l’aide de la méthode [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) , la largeur du trait n’est pas affectée par la transformation appliquée à la géométrie.</span><span class="sxs-lookup"><span data-stu-id="7c42a-116">When stroking a transformed geometry with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method, the stroke width is not affected by the transform applied to the geometry.</span></span> <span data-ttu-id="7c42a-117">La largeur du trait est uniquement affectée par la transformation universelle.</span><span class="sxs-lookup"><span data-stu-id="7c42a-117">The stroke width is only affected by the world transform.</span></span>

## <a name="examples"></a><span data-ttu-id="7c42a-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="7c42a-118">Examples</span></span>

<span data-ttu-id="7c42a-119">L’exemple suivant crée un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), puis le dessine sans le transformer.</span><span class="sxs-lookup"><span data-stu-id="7c42a-119">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), then draws it without transforming it.</span></span> <span data-ttu-id="7c42a-120">Il produit la sortie indiquée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="7c42a-120">It produces the output shown in the following illustration.</span></span>

![illustration d’un rectangle](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



<span data-ttu-id="7c42a-122">L’exemple suivant utilise la cible de rendu pour mettre à l’échelle la géométrie d’un facteur de 3, puis la dessine.</span><span class="sxs-lookup"><span data-stu-id="7c42a-122">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="7c42a-123">L’illustration suivante montre le résultat du dessin du rectangle sans la transformation et avec la transformation. indique que le trait est plus épais après la transformation, même si l’épaisseur du trait est 1.</span><span class="sxs-lookup"><span data-stu-id="7c42a-123">The following illustration shows the result of drawing the rectangle without the transform and with the transform; notices that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![illustration d’un rectangle plus petit à l’intérieur d’un rectangle plus grand avec un trait plus épais](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="7c42a-125">L’exemple suivant utilise la méthode **CreateTransformedGeometry** pour mettre à l’échelle la géométrie d’un facteur de 3, puis la dessine.</span><span class="sxs-lookup"><span data-stu-id="7c42a-125">The next example uses the **CreateTransformedGeometry** method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="7c42a-126">Il produit la sortie indiquée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="7c42a-126">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="7c42a-127">Notez que, bien que le rectangle soit plus grand, son trait n’a pas augmenté.</span><span class="sxs-lookup"><span data-stu-id="7c42a-127">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![illustration d’un rectangle plus petit à l’intérieur d’un rectangle plus grand avec le même trait](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a><span data-ttu-id="7c42a-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c42a-129">Requirements</span></span>



| <span data-ttu-id="7c42a-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c42a-130">Requirement</span></span> | <span data-ttu-id="7c42a-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c42a-131">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7c42a-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c42a-132">Header</span></span><br/>  | <dl> <span data-ttu-id="7c42a-133"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c42a-133"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c42a-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c42a-134">Library</span></span><br/> | <dl> <span data-ttu-id="7c42a-135"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c42a-135"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c42a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7c42a-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="7c42a-137"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c42a-137"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c42a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c42a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c42a-139">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="7c42a-139">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
