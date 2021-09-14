---
title: Vue d’ensemble des géométries
description: Décrit les principes de base des géométries Direct2D, les objets que vous pouvez utiliser pour représenter, manipuler et analyser des formes.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Direct2D, vue d’ensemble des géométries
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cb97b0737bfad391fb9ba2501793a970fcbd9886
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113318"
---
# <a name="geometries-overview"></a>Vue d’ensemble des géométries

Cette vue d’ensemble décrit comment créer et utiliser des objets [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) pour définir et manipuler des figures 2D. Elle contient les sections suivantes.

## <a name="what-is-a-direct2d-geometry"></a>Qu’est-ce qu’une géométrie Direct2D ?

Une géométrie Direct2D est un objet [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) . Cet objet peut être une géométrie simple ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)ou [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), une géométrie de tracé ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) ou une géométrie composite ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) et [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).

Les géométries Direct2D vous permettent de décrire des figures à deux dimensions et offrent de nombreuses utilisations, telles que la définition de régions de test de positionnement, de régions de découpage et même de chemins d’animation.

Les géométries Direct2D sont des ressources immuables et indépendantes des appareils créées par [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory). En règle générale, vous devez créer des géométries une fois et les conserver pendant toute la durée de vie de l’application, ou jusqu’à ce qu’elles soient modifiées. Pour plus d’informations sur les ressources indépendantes des appareils et des appareils, consultez la [vue d’ensemble des ressources](resources-and-resource-domains.md).

Les sections suivantes décrivent les différents genres de géométries.

## <a name="simple-geometries"></a>Géométries simples

Les géométries simples incluent les objets [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)et [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , et peuvent être utilisées pour créer des chiffres géométriques de base, tels que des rectangles, des rectangles arrondis, des cercles et des ellipses.

Pour créer une géométrie simple, utilisez l’une des méthodes [**ID2D1Factory :: create<*GeometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) . Ces méthodes créent un objet du type spécifié. Par exemple, pour créer un rectangle, appelez [**ID2D1Factory :: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), qui retourne un objet [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) ; pour créer un rectangle à coins arrondis, appelez [**ID2D1Factory :: CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), qui retourne un objet [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) , et ainsi de suite.

L’exemple de code suivant appelle la méthode [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) , en passant une structure ellipse avec le *Centre* défini sur (100, 100), *x-RADIUS* à 100 et le *rayon y* sur 50. Ensuite, il appelle [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), en passant la géométrie d’ellipse retournée, un pointeur vers un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)noir et une largeur de trait de 5. L’illustration suivante montre la sortie de l’exemple de code.

![illustration d’une ellipse](images/geometry-ovw-drawstep6.png)


```C++
ID2D1EllipseGeometry *m_pEllipseGeometry;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateEllipseGeometry(
        D2D1::Ellipse(D2D1::Point2F(100.f, 60.f), 100.f, 50.f),
        &m_pEllipseGeometry
        );
}
```




```C++
m_pRenderTarget->DrawGeometry(m_pEllipseGeometry, m_pBlackBrush, 5);
```



Pour dessiner le contour d’une géométrie, utilisez la méthode [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) . Pour peindre son intérieur, utilisez la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .

## <a name="path-geometries"></a>Géométries de tracés

Les géométries de tracés sont représentées par l’interface [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Ces objets peuvent être utilisés pour décrire des chiffres géométriques complexes composés de segments tels que des arcs, des courbes et des lignes. L’illustration suivante montre un dessin créé à l’aide d’une géométrie de tracé.

![illustration d’une rivière, de montagnes et du soleil](images/path-geo-mnts.png)

Pour plus d’informations et d’exemples, consultez [vue d’ensemble des géométries de tracés](path-geometries-overview.md).

## <a name="composite-geometries"></a>Géométries composites

Une géométrie composite est une géométrie regroupée ou associée à un autre objet Geometry, ou à une transformation. Les géométries composites incluent les objets [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) et [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) .

### <a name="geometry-groups"></a>Groupes géométriques

Les groupes géométriques sont un moyen pratique de regrouper plusieurs géométries en même temps, de sorte que toutes les figures de plusieurs géométries distinctes sont concaténées en une seule. Pour créer un objet [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) , appelez la méthode [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) sur l’objet [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , en passant le *fillMode* avec les valeurs possibles du mode de [**remplissage de \_ \_ \_ remplacement**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternative) et l' **\_ \_ \_ enroulement du mode de remplissage d2d1**, un tableau d’objets Geometry à ajouter au groupe Geometry et le nombre d’éléments de ce tableau.

L’exemple de code suivant déclare tout d’abord un tableau d’objets Geometry. Ces objets sont quatre cercles concentriques ayant les rayons suivants : 25, 50, 75 et 100. Appelez ensuite [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) sur l’objet [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , en passant le [**mode de \_ remplissage d2d1 \_ \_ alternatif**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), un tableau d’objets Geometry à ajouter au groupe Geometry, et le nombre d’éléments de ce tableau.


```C++
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
```

L’illustration suivante montre les résultats du rendu des deux géométries de groupe à partir de l’exemple.

![illustration de deux jeux de quatre cercles concentriques, un avec des anneaux de remplacement pleins et un avec tous les anneaux remplis](images/create-geometry-group.png)

### <a name="transformed-geometries"></a>Géométries transformées

Il existe plusieurs façons de transformer une géométrie. Vous pouvez utiliser la méthode [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) d’une cible de rendu pour transformer tout ce que la cible de rendu dessine, ou vous pouvez associer une transformation directement à une géométrie à l’aide de la méthode [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) pour créer un [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).

La méthode que vous devez utiliser dépend de l’effet que vous souhaitez. Lorsque vous utilisez la cible de rendu pour transformer puis restituer une géométrie, la transformation affecte tout sur la géométrie, y compris la largeur de tout trait que vous avez appliqué. En revanche, lorsque vous utilisez un [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), la transformation affecte uniquement les coordonnées qui décrivent la forme. La transformation n’affecte pas l’épaisseur du trait quand la géométrie est dessinée.

> [!Note]  
> à partir de Windows 8 la transformation universelle n’affecte pas l’épaisseur du trait des traits avec le type de transformation de trait [**D2D1 \_ \_ \_ \_ fixe**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)ou le [**\_ type de transformation de trait \_ \_ \_ D2D1**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type). Vous devez utiliser ces types de transformation pour obtenir des traits indépendants de transformation

 

L’exemple suivant crée un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), puis le dessine sans le transformer. Il produit la sortie indiquée dans l’illustration suivante.

![illustration d’un rectangle](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```




```C++
// Draw the untransformed rectangle geometry.
m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



L’exemple suivant utilise la cible de rendu pour mettre à l’échelle la géométrie d’un facteur de 3, puis la dessine. L’illustration suivante montre le résultat du dessin du rectangle sans la transformation et avec la transformation. Notez que le trait est plus épais après la transformation, même si l’épaisseur du trait est 1.

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



L’exemple suivant utilise la méthode [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) pour mettre à l’échelle la géométrie d’un facteur de 3, puis la dessine. Il produit la sortie indiquée dans l’illustration suivante. Notez que, bien que le rectangle soit plus grand, son trait n’a pas augmenté.

![illustration d’un rectangle plus petit à l’intérieur d’un rectangle plus grand avec la même épaisseur de trait](images/transformedgeometry2-step3.png)


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
```




```C++
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```



## <a name="geometries-as-masks"></a>Géométries comme masques

Vous pouvez utiliser un objet [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) comme masque géométrique lorsque vous appelez la méthode [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) . Le masque géométrique spécifie la zone de la couche qui est composite dans la cible de rendu. Pour plus d’informations, consultez la section masques géométriques de la [vue d’ensemble des couches](direct2d-layers-overview.md).

## <a name="geometric-operations"></a>Opérations géométriques

L’interface [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) fournit plusieurs opérations géométriques que vous pouvez utiliser pour manipuler et mesurer des figures géométriques. Par exemple, vous pouvez les utiliser pour calculer et retourner leurs limites, comparer pour voir comment une géométrie est liée de manière spatiale à une autre (utile pour le test de positionnement), calculer les zones et les longueurs, et bien plus encore. Le tableau suivant décrit les opérations géométriques courantes.



| Opération                                                   | Méthode                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Combiner                                                     | [**CombineWithGeometry**](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| Limites/limites étendues/limites de récupération, mise à jour de la région modifiée | [**Widening**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)                             |
| Test des résultats                                                 | [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                             |
| Trait                                                      | [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| Comparaison                                                  | [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| Simplification (supprime les arcs et les courbes de Bézier quadratiques)   | [**Ainsi**](id2d1geometry-simplify.md)                                                                                                                                 |
| Pavage                                                | [**Paver**](id2d1geometry-tessellate.md)                                                                                                                             |
| Contour (supprimer l’intersection)                               | [**Plan**](id2d1geometry-outline.md)                                                                                                                                   |
| Calculer la zone ou la longueur d’une géométrie                  | [**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) |



 

> [!Note]  
> à partir de Windows 8, vous pouvez utiliser la méthode [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) sur [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) pour calculer la zone ou la longueur d’une géométrie.

 

### <a name="combining-geometries"></a>Combinaison de géométries

Pour associer une géométrie à une autre, appelez la méthode [**ID2D1Geometry :: CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) . Lorsque vous combinez les géométries, vous spécifiez l’une des quatre méthodes d’exécution de l’opération combiner : [**d2d1 \_ combine \_ mode \_ Union**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Union), [**d2d1 \_ combine \_ mode \_ Intersect**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Intersect), [**d2d1 \_ combine \_ mode \_ Xor**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (XOR) et [**d2d1 \_ \_ mode combine \_ Exclude**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Exclude). L’exemple de code suivant montre deux cercles combinés à l’aide du mode de combinaison Union, où le premier cercle a le point central (75, 75) et le rayon de 50, et le deuxième cercle a le point central de (125, 75) et le rayon de 50.


```C++
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
```



L’illustration suivante montre deux cercles combinés avec un mode combiné d’Union.

![illustration de deux cercles se chevauchant combinés dans une Union](images/combine-mode-union.png)

Pour obtenir des illustrations de tous les modes combinés, consultez l' [**\_ \_ énumération du mode de combinaison d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).

### <a name="widen"></a>Élargi

La méthode [**Widening**](id2d1geometry-widen.md) génère une nouvelle géométrie dont le remplissage est équivalent au contour de la géométrie existante, puis écrit le résultat dans l’objet [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) spécifié. L’exemple de code suivant appelle [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) sur l’objet [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Si l' **ouverture** est réussie, elle appelle **Widening** sur l’objet Geometry.


```C++
ID2D1GeometrySink *pGeometrySink = NULL;
hr = pPathGeometry->Open(&pGeometrySink);
if (SUCCEEDED(hr))
{
    hr = pGeometry->Widen(
            strokeWidth,
            pIStrokeStyle,
            pWorldTransform,
            pGeometrySink
            );
```



### <a name="tessellate"></a>Paver

La méthode [**paver**](id2d1geometry-tessellate.md) crée un ensemble de triangles enroulés dans le sens des aiguilles d’une montre qui couvrent la géométrie après sa transformation à l’aide de la matrice spécifiée et aplatie à l’aide de la tolérance spécifiée. L’exemple de code suivant utilise **paver** pour créer une liste de triangles représentant *pPathGeometry*. Les triangles sont stockés dans un [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, puis transférés à un membre de classe, *m \_ pStrokeMesh*, pour une utilisation ultérieure lors du rendu.


```C++
ID2D1Mesh *pMesh = NULL;
hr = m_pRT->CreateMesh(&pMesh);
if (SUCCEEDED(hr))
{
    ID2D1TessellationSink *pSink = NULL;
    hr = pMesh->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Tessellate(
                NULL, // world transform (already handled in Widen)
                pSink
                );
        if (SUCCEEDED(hr))
        {
            hr = pSink->Close();
            if (SUCCEEDED(hr))
            {
                SafeReplace(&m_pStrokeMesh, pMesh);
            }
        }
        pSink->Release();
    }
    pMesh->Release();
}
```



### <a name="fillcontainspoint-and-strokecontainspoint"></a>FillContainsPoint et StrokeContainsPoint

La méthode [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) indique si la zone remplie par la géométrie contient le point spécifié. Vous pouvez utiliser cette méthode pour effectuer un test de positionnement. L’exemple de code suivant appelle **FillContainsPoint** sur un objet [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , en passant un point à (0,0) et une matrice d' [**identité**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) .


```C++
BOOL containsPoint1;
hr = m_pCircleGeometry1->FillContainsPoint(
    D2D1::Point2F(0,0),
    D2D1::Matrix3x2F::Identity(),
    &containsPoint1
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



La méthode [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) détermine si le trait de la géométrie contient le point spécifié. Vous pouvez utiliser cette méthode pour effectuer un test de positionnement. L’exemple de code suivant utilise **StrokeContainsPoint**.


```C++
BOOL containsPoint;

hr = m_pCircleGeometry1->StrokeContainsPoint(
    D2D1::Point2F(0,0),
    10,     // stroke width
    NULL,   // stroke style
    NULL,   // world transform
    &containsPoint
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



### <a name="simplify"></a>Simplifier 

La méthode [**simplifier**](id2d1geometry-simplify.md) supprime les arcs et les courbes de Bézier quadratiques d’une géométrie spécifiée. Ainsi, la géométrie résultante contient uniquement des lignes et, éventuellement, des courbes de Bézier cubiques. L’exemple de code suivant utilise **simplifier** pour transformer une géométrie avec des courbes de Bézier en une géométrie qui contient uniquement des segments de ligne.


```C++
HRESULT D2DFlatten(
    ID2D1Geometry *pGeometry,
    float flatteningTolerance,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES,
                    NULL, // world transform
                    flatteningTolerance,
                    pSink
                    );

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="computelength-and-computearea"></a>ComputeLength et ComputeArea

La méthode [**ComputeLength**](id2d1geometry-computelength.md) calcule la longueur de la géométrie spécifiée si chaque segment a été déroulé dans une ligne. Cela comprend le segment fermant implicite si la géométrie est fermée. L’exemple de code suivant utilise **ComputeLength** pour calculer la longueur d’un cercle spécifié (**m \_ pCircleGeometry1**).


```C++
float length;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeLength(
    D2D1::IdentityMatrix(),
    &length
    );

if (SUCCEEDED(hr))
{
    // Process the length of the geometry.
}
```



La méthode [**ComputeArea**](id2d1geometry-computearea.md) calcule la zone de la géométrie spécifiée. L’exemple de code suivant utilise **ComputeArea** pour calculer la zone d’un cercle spécifié (**m \_ pCircleGeometry1**).


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a>CompareWithGeometry

La méthode [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) décrit l’intersection entre la géométrie qui appelle cette méthode et la géométrie spécifiée. Les valeurs possibles pour l’intersection incluent la relation [**d2d1 \_ Geometry \_ \_ disjointe**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (disjointe), la **\_ relation Geometry d2d1 \_ \_ est \_ contenue** (est contenue), la **\_ relation Geometry d2d1 \_ \_ contient** (Contains) et le **\_ \_ \_ chevauchement de la relation Geometry d2d1** (chevauchement). « disjointe » signifie que deux remplissages de géométrie ne se croisent pas du tout. « est contenu » signifie que la géométrie est entièrement contenue dans la géométrie spécifiée. « Contains » signifie que la géométrie contient entièrement la géométrie spécifiée, et « se chevauchent » signifie que les deux géométries se chevauchent, mais ne contiennent pas complètement l’autre.

L’exemple de code suivant montre comment comparer deux cercles qui ont le même rayon de 50, mais qui sont décalés de 50.


```C++
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

```




```C++
D2D1_GEOMETRY_RELATION result = D2D1_GEOMETRY_RELATION_UNKNOWN;

// Compare circle1 with circle2
hr = m_pCircleGeometry1->CompareWithGeometry(
    m_pCircleGeometry2,
    D2D1::IdentityMatrix(),
    0.1f,
    &result
    );

if (SUCCEEDED(hr))
{
    static const WCHAR szGeometryRelation[] = L"Two circles overlap.";
    m_pRenderTarget->SetTransform(D2D1::IdentityMatrix());
    if (result == D2D1_GEOMETRY_RELATION_OVERLAP)
    {
        m_pRenderTarget->DrawText(
            szGeometryRelation,
            ARRAYSIZE(szGeometryRelation) - 1,
            m_pTextFormat,
            D2D1::RectF(25.0f, 160.0f, 200.0f, 300.0f),
            m_pTextBrush
            );
    }
}
```



### <a name="outline"></a>Plan

La méthode [**Outline**](id2d1geometry-outline.md) calcule le contour de la géométrie (une version de la géométrie dans laquelle aucune figure n’entre elle-même ou une autre figure) et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). L’exemple de code suivant utilise **Outline** pour construire une géométrie équivalente sans aucune auto-intersection. Elle utilise la tolérance d’aplatissement par défaut.


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="getbounds-and-getwidenedbounds"></a>GetBounds et GetWidenedBounds

La méthode [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) récupère les limites de la géométrie. L’exemple de code suivant utilise **GetBounds** pour récupérer les limites d’un cercle spécifié (**m \_ pCircleGeometry1**).


```C++
D2D1_RECT_F bounds;

hr = m_pCircleGeometry1->GetBounds(
      D2D1::IdentityMatrix(),
      &bounds
     );

if (SUCCEEDED(hr))
{
    // Retrieve the bounds.
}
```



La méthode [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) récupère les limites de la géométrie après qu’elle a été élargie par la largeur et le style de trait spécifiés et transformée par la matrice spécifiée. L’exemple de code suivant utilise **GetWidenedBounds** pour récupérer les limites d’un cercle spécifié (**m \_ pCircleGeometry1**) après qu’il a été élargi par la largeur de trait spécifiée.


```C++
float dashes[] = {1.f, 1.f, 2.f, 3.f, 5.f};

m_pD2DFactory->CreateStrokeStyle(
    D2D1::StrokeStyleProperties(
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_ROUND,
        D2D1_LINE_JOIN_ROUND,   // lineJoin
        10.f,   //miterLimit
        D2D1_DASH_STYLE_CUSTOM,
        0.f     //dashOffset
        ),
     dashes,
     ARRAYSIZE(dashes)-1,
     &m_pStrokeStyle
     );
```




```C++
D2D1_RECT_F bounds1;
hr = m_pCircleGeometry1->GetWidenedBounds(
      5.0,
      m_pStrokeStyle,
      D2D1::IdentityMatrix(),
      &bounds1
     );
if (SUCCEEDED(hr))
{
    // Retrieve the widened bounds.
}
```



### <a name="computepointatlength"></a>ComputePointAtLength

La méthode [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) calcule le vecteur de point et de tangente à la distance spécifiée le long de la géométrie. L’exemple de code suivant utilise **ComputePointAtLength**.


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des géométries de tracés](path-geometries-overview.md)
</dt> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 