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
# <a name="id2d1factorycreatetransformedgeometry-methods"></a>ID2D1Factory :: CreateTransformedGeometry, méthodes

Transforme la géométrie spécifiée et stocke le résultat sous la forme d’un objet [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                                  | Description                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTransformedGeometry (ID2D1Geometry \* , \_ matrice D2D \_ matrice \_ F \* , ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) | Transforme la géométrie spécifiée et stocke le résultat sous la forme d’un objet [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) . <br/> |
| [**CreateTransformedGeometry (ID2D1Geometry \* , \_ matrice D2D \_ matrice \_ F&, ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))  | Transforme la géométrie spécifiée et stocke le résultat sous la forme d’un objet [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) . <br/> |



## <a name="remarks"></a>Notes

Comme les autres ressources, une géométrie transformée hérite de l’espace de ressources et de la stratégie de thread de la fabrique qui l’a créée. Cet objet est immuable.

Lors du découpage d’une géométrie transformée à l’aide de la méthode [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) , la largeur du trait n’est pas affectée par la transformation appliquée à la géométrie. La largeur du trait est uniquement affectée par la transformation universelle.

## <a name="examples"></a>Exemples

L’exemple suivant crée un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), puis le dessine sans le transformer. Il produit la sortie indiquée dans l’illustration suivante.

![illustration d’un rectangle](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



L’exemple suivant utilise la cible de rendu pour mettre à l’échelle la géométrie d’un facteur de 3, puis la dessine. L’illustration suivante montre le résultat du dessin du rectangle sans la transformation et avec la transformation. indique que le trait est plus épais après la transformation, même si l’épaisseur du trait est 1.

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



L’exemple suivant utilise la méthode **CreateTransformedGeometry** pour mettre à l’échelle la géométrie d’un facteur de 3, puis la dessine. Il produit la sortie indiquée dans l’illustration suivante. Notez que, bien que le rectangle soit plus grand, son trait n’a pas augmenté.

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





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
