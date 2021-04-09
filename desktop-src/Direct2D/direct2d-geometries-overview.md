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
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734572"
---
# <a name="geometries-overview"></a><span data-ttu-id="c751a-104">Vue d’ensemble des géométries</span><span class="sxs-lookup"><span data-stu-id="c751a-104">Geometries overview</span></span>

<span data-ttu-id="c751a-105">Cette vue d’ensemble décrit comment créer et utiliser des objets [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) pour définir et manipuler des figures 2D.</span><span class="sxs-lookup"><span data-stu-id="c751a-105">This overview describes how to create and use [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) objects to define and manipulate 2D figures.</span></span> <span data-ttu-id="c751a-106">Elle contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c751a-106">It contains the following sections.</span></span>

## <a name="what-is-a-direct2d-geometry"></a><span data-ttu-id="c751a-107">Qu’est-ce qu’une géométrie Direct2D ?</span><span class="sxs-lookup"><span data-stu-id="c751a-107">What is a Direct2D geometry?</span></span>

<span data-ttu-id="c751a-108">Une géométrie Direct2D est un objet [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) .</span><span class="sxs-lookup"><span data-stu-id="c751a-108">A Direct2D geometry is an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object.</span></span> <span data-ttu-id="c751a-109">Cet objet peut être une géométrie simple ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)ou [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), une géométrie de tracé ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) ou une géométrie composite ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) et [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span><span class="sxs-lookup"><span data-stu-id="c751a-109">This object can be a simple geometry ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), or [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), a path geometry ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)), or a composite geometry ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) and [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).</span></span>

<span data-ttu-id="c751a-110">Les géométries Direct2D vous permettent de décrire des figures à deux dimensions et offrent de nombreuses utilisations, telles que la définition de régions de test de positionnement, de régions de découpage et même de chemins d’animation.</span><span class="sxs-lookup"><span data-stu-id="c751a-110">Direct2D geometries enable you to describe two-dimensional figures and offer many uses, such as defining hit-test regions, clip regions, and even animation paths.</span></span>

<span data-ttu-id="c751a-111">Les géométries Direct2D sont des ressources immuables et indépendantes des appareils créées par [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span><span class="sxs-lookup"><span data-stu-id="c751a-111">Direct2D geometries are immutable and device-independent resources created by [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span> <span data-ttu-id="c751a-112">En règle générale, vous devez créer des géométries une fois et les conserver pendant toute la durée de vie de l’application, ou jusqu’à ce qu’elles soient modifiées.</span><span class="sxs-lookup"><span data-stu-id="c751a-112">Generally, you should create geometries one time and keep them for the life of the application, or until they have to be changed.</span></span> <span data-ttu-id="c751a-113">Pour plus d’informations sur les ressources indépendantes des appareils et des appareils, consultez la [vue d’ensemble des ressources](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="c751a-113">For more information about device-independent and device-dependent resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="c751a-114">Les sections suivantes décrivent les différents genres de géométries.</span><span class="sxs-lookup"><span data-stu-id="c751a-114">The following sections describe the different kinds of geometries.</span></span>

## <a name="simple-geometries"></a><span data-ttu-id="c751a-115">Géométries simples</span><span class="sxs-lookup"><span data-stu-id="c751a-115">Simple geometries</span></span>

<span data-ttu-id="c751a-116">Les géométries simples incluent les objets [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)et [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , et peuvent être utilisées pour créer des chiffres géométriques de base, tels que des rectangles, des rectangles arrondis, des cercles et des ellipses.</span><span class="sxs-lookup"><span data-stu-id="c751a-116">Simple geometries include [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry), and [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects, and can be used to create basic geometric figures, such as rectangles, rounded rectangles, circles, and ellipses.</span></span>

<span data-ttu-id="c751a-117">Pour créer une géométrie simple, utilisez l’une des méthodes [**ID2D1Factory :: create<*GeometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="c751a-117">To create a simple geometry, use one of the [**ID2D1Factory::Create<*geometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) methods.</span></span> <span data-ttu-id="c751a-118">Ces méthodes créent un objet du type spécifié.</span><span class="sxs-lookup"><span data-stu-id="c751a-118">These methods create an object of the specified type.</span></span> <span data-ttu-id="c751a-119">Par exemple, pour créer un rectangle, appelez [**ID2D1Factory :: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), qui retourne un objet [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) ; pour créer un rectangle à coins arrondis, appelez [**ID2D1Factory :: CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), qui retourne un objet [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) , et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="c751a-119">For example, to create a rectangle, call [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), which returns an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object; to create a rounded rectangle, call [**ID2D1Factory::CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), which returns an [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) object, and so on.</span></span>

<span data-ttu-id="c751a-120">L’exemple de code suivant appelle la méthode [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) , en passant une structure ellipse avec le *Centre* défini sur (100, 100), *x-RADIUS* à 100 et le *rayon y* sur 50.</span><span class="sxs-lookup"><span data-stu-id="c751a-120">The following code example calls the [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) method, passing in an ellipse structure with the *center* set to (100, 100), *x-radius* to 100, and *y-radius* to 50.</span></span> <span data-ttu-id="c751a-121">Ensuite, il appelle [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), en passant la géométrie d’ellipse retournée, un pointeur vers un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)noir et une largeur de trait de 5.</span><span class="sxs-lookup"><span data-stu-id="c751a-121">Then, it calls [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), passing in the returned ellipse geometry, a pointer to a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), and a stroke width of 5.</span></span> <span data-ttu-id="c751a-122">L’illustration suivante montre la sortie de l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="c751a-122">The following illustration shows the output from the code example.</span></span>

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



<span data-ttu-id="c751a-124">Pour dessiner le contour d’une géométrie, utilisez la méthode [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) .</span><span class="sxs-lookup"><span data-stu-id="c751a-124">To draw the outline of any geometry, use the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method.</span></span> <span data-ttu-id="c751a-125">Pour peindre son intérieur, utilisez la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .</span><span class="sxs-lookup"><span data-stu-id="c751a-125">To paint its interior, use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

## <a name="path-geometries"></a><span data-ttu-id="c751a-126">Géométries de tracés</span><span class="sxs-lookup"><span data-stu-id="c751a-126">Path geometries</span></span>

<span data-ttu-id="c751a-127">Les géométries de tracés sont représentées par l’interface [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="c751a-127">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="c751a-128">Ces objets peuvent être utilisés pour décrire des chiffres géométriques complexes composés de segments tels que des arcs, des courbes et des lignes.</span><span class="sxs-lookup"><span data-stu-id="c751a-128">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="c751a-129">L’illustration suivante montre un dessin créé à l’aide d’une géométrie de tracé.</span><span class="sxs-lookup"><span data-stu-id="c751a-129">The following illustration shows a drawing created by using path geometry.</span></span>

![illustration d’une rivière, de montagnes et du soleil](images/path-geo-mnts.png)

<span data-ttu-id="c751a-131">Pour plus d’informations et d’exemples, consultez [vue d’ensemble des géométries de tracés](path-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c751a-131">For more information and examples, see the [Path Geometries Overview](path-geometries-overview.md).</span></span>

## <a name="composite-geometries"></a><span data-ttu-id="c751a-132">Géométries composites</span><span class="sxs-lookup"><span data-stu-id="c751a-132">Composite geometries</span></span>

<span data-ttu-id="c751a-133">Une géométrie composite est une géométrie regroupée ou associée à un autre objet Geometry, ou à une transformation.</span><span class="sxs-lookup"><span data-stu-id="c751a-133">A composite geometry is a geometry grouped or combined with another geometry object, or with a transform.</span></span> <span data-ttu-id="c751a-134">Les géométries composites incluent les objets [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) et [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) .</span><span class="sxs-lookup"><span data-stu-id="c751a-134">Composite geometries include [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) and [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) objects.</span></span>

### <a name="geometry-groups"></a><span data-ttu-id="c751a-135">Groupes géométriques</span><span class="sxs-lookup"><span data-stu-id="c751a-135">Geometry groups</span></span>

<span data-ttu-id="c751a-136">Les groupes géométriques sont un moyen pratique de regrouper plusieurs géométries en même temps, de sorte que toutes les figures de plusieurs géométries distinctes sont concaténées en une seule.</span><span class="sxs-lookup"><span data-stu-id="c751a-136">Geometry groups are a convenient way to group several geometries at the same time so all figures of several distinct geometries are concatenated into one.</span></span> <span data-ttu-id="c751a-137">Pour créer un objet [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) , appelez la méthode [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) sur l’objet [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , en passant le *fillMode* avec les valeurs possibles du mode de [**remplissage de \_ \_ \_ remplacement**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternative) et l' **\_ \_ \_ enroulement du mode de remplissage d2d1**, un tableau d’objets Geometry à ajouter au groupe Geometry et le nombre d’éléments de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="c751a-137">To create a [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) object, call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) method on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in the *fillMode* with possible values of [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternate) and **D2D1\_FILL\_MODE\_WINDING**, an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>

<span data-ttu-id="c751a-138">L’exemple de code suivant déclare tout d’abord un tableau d’objets Geometry.</span><span class="sxs-lookup"><span data-stu-id="c751a-138">The following code example first declares an array of geometry objects.</span></span> <span data-ttu-id="c751a-139">Ces objets sont quatre cercles concentriques ayant les rayons suivants : 25, 50, 75 et 100.</span><span class="sxs-lookup"><span data-stu-id="c751a-139">These objects are four concentric circles that have the following radii: 25, 50, 75, and 100.</span></span> <span data-ttu-id="c751a-140">Appelez ensuite [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) sur l’objet [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , en passant le [**mode de \_ remplissage d2d1 \_ \_ alternatif**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), un tableau d’objets Geometry à ajouter au groupe Geometry, et le nombre d’éléments de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="c751a-140">Then call the [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) on the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, passing in [**D2D1\_FILL\_MODE\_ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), an array of geometry objects to add to the geometry group, and the number of elements in this array.</span></span>


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

<span data-ttu-id="c751a-141">L’illustration suivante montre les résultats du rendu des deux géométries de groupe à partir de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c751a-141">The following illustration shows the results of rendering the two group geometries from the example.</span></span>

![illustration de deux jeux de quatre cercles concentriques, un avec des anneaux de remplacement pleins et un avec tous les anneaux remplis](images/create-geometry-group.png)

### <a name="transformed-geometries"></a><span data-ttu-id="c751a-143">Géométries transformées</span><span class="sxs-lookup"><span data-stu-id="c751a-143">Transformed geometries</span></span>

<span data-ttu-id="c751a-144">Il existe plusieurs façons de transformer une géométrie.</span><span class="sxs-lookup"><span data-stu-id="c751a-144">There are multiple ways to transform a geometry.</span></span> <span data-ttu-id="c751a-145">Vous pouvez utiliser la méthode [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) d’une cible de rendu pour transformer tout ce que la cible de rendu dessine, ou vous pouvez associer une transformation directement à une géométrie à l’aide de la méthode [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) pour créer un [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c751a-145">You can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of a render target to transform everything that the render target draws, or you can associate a transform directly with a geometry by using the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) method to create an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).</span></span>

<span data-ttu-id="c751a-146">La méthode que vous devez utiliser dépend de l’effet que vous souhaitez.</span><span class="sxs-lookup"><span data-stu-id="c751a-146">The method that you should use depends on the effect that you want.</span></span> <span data-ttu-id="c751a-147">Lorsque vous utilisez la cible de rendu pour transformer puis restituer une géométrie, la transformation affecte tout sur la géométrie, y compris la largeur de tout trait que vous avez appliqué.</span><span class="sxs-lookup"><span data-stu-id="c751a-147">When you use the render target to transform and then render a geometry, the transform affects everything about the geometry, including the width of any stroke that you have applied.</span></span> <span data-ttu-id="c751a-148">En revanche, lorsque vous utilisez un [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), la transformation affecte uniquement les coordonnées qui décrivent la forme.</span><span class="sxs-lookup"><span data-stu-id="c751a-148">On the other hand, when you use an [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), the transform affects only the coordinates that describe the shape.</span></span> <span data-ttu-id="c751a-149">La transformation n’affecte pas l’épaisseur du trait quand la géométrie est dessinée.</span><span class="sxs-lookup"><span data-stu-id="c751a-149">The transformation will not affect the stroke thickness when the geometry is drawn.</span></span>

> [!Note]  
> <span data-ttu-id="c751a-150">À compter de Windows 8, la transformation universelle n’affecte pas l’épaisseur du trait des traits avec le type de transformation de trait [**d2d1 \_ \_ \_ \_ fixe**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)ou le [**\_ type de transformation de trait \_ \_ \_ d2d1**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span><span class="sxs-lookup"><span data-stu-id="c751a-150">Starting with Windows 8 the world transform will not affect the stroke thickness of strokes with [**D2D1\_STROKE\_TRANSFORM\_TYPE\_FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)or [**D2D1\_STROKE\_TRANSFORM\_TYPE\_HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span></span> <span data-ttu-id="c751a-151">Vous devez utiliser ces types de transformation pour obtenir des traits indépendants de transformation</span><span class="sxs-lookup"><span data-stu-id="c751a-151">You should use these transform types to achieve transform independent strokes</span></span>

 

<span data-ttu-id="c751a-152">L’exemple suivant crée un [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), puis le dessine sans le transformer.</span><span class="sxs-lookup"><span data-stu-id="c751a-152">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), then draws it without transforming it.</span></span> <span data-ttu-id="c751a-153">Il produit la sortie indiquée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="c751a-153">It produces the output shown in the following illustration.</span></span>

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



<span data-ttu-id="c751a-155">L’exemple suivant utilise la cible de rendu pour mettre à l’échelle la géométrie d’un facteur de 3, puis la dessine.</span><span class="sxs-lookup"><span data-stu-id="c751a-155">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="c751a-156">L’illustration suivante montre le résultat du dessin du rectangle sans la transformation et avec la transformation.</span><span class="sxs-lookup"><span data-stu-id="c751a-156">The following illustration shows the result of drawing the rectangle without the transform and with the transform.</span></span> <span data-ttu-id="c751a-157">Notez que le trait est plus épais après la transformation, même si l’épaisseur du trait est 1.</span><span class="sxs-lookup"><span data-stu-id="c751a-157">Notice that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

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



<span data-ttu-id="c751a-159">L’exemple suivant utilise la méthode [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) pour mettre à l’échelle la géométrie d’un facteur de 3, puis la dessine.</span><span class="sxs-lookup"><span data-stu-id="c751a-159">The next example uses the [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="c751a-160">Il produit la sortie indiquée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="c751a-160">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="c751a-161">Notez que, bien que le rectangle soit plus grand, son trait n’a pas augmenté.</span><span class="sxs-lookup"><span data-stu-id="c751a-161">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

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



## <a name="geometries-as-masks"></a><span data-ttu-id="c751a-163">Géométries comme masques</span><span class="sxs-lookup"><span data-stu-id="c751a-163">Geometries as masks</span></span>

<span data-ttu-id="c751a-164">Vous pouvez utiliser un objet [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) comme masque géométrique lorsque vous appelez la méthode [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="c751a-164">You can use an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object as a geometric mask when you call the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="c751a-165">Le masque géométrique spécifie la zone de la couche qui est composite dans la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="c751a-165">The geometric mask specifies the area of the layer that is composited into the render target.</span></span> <span data-ttu-id="c751a-166">Pour plus d’informations, consultez la section masques géométriques de la [vue d’ensemble des couches](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c751a-166">For more information, see the Geometric Masks section of the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="geometric-operations"></a><span data-ttu-id="c751a-167">Opérations géométriques</span><span class="sxs-lookup"><span data-stu-id="c751a-167">Geometric operations</span></span>

<span data-ttu-id="c751a-168">L’interface [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) fournit plusieurs opérations géométriques que vous pouvez utiliser pour manipuler et mesurer des figures géométriques.</span><span class="sxs-lookup"><span data-stu-id="c751a-168">The [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) interface provides several geometric operations that you can use to manipulate and measure geometric figures.</span></span> <span data-ttu-id="c751a-169">Par exemple, vous pouvez les utiliser pour calculer et retourner leurs limites, comparer pour voir comment une géométrie est liée de manière spatiale à une autre (utile pour le test de positionnement), calculer les zones et les longueurs, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="c751a-169">For example, you can use them to calculate and return their bounds, compare to see how one geometry is spatially related to another (useful for hit testing), calculate the areas and lengths, and more.</span></span> <span data-ttu-id="c751a-170">Le tableau suivant décrit les opérations géométriques courantes.</span><span class="sxs-lookup"><span data-stu-id="c751a-170">The following table describes the common geometric operations.</span></span>



| <span data-ttu-id="c751a-171">Opération</span><span class="sxs-lookup"><span data-stu-id="c751a-171">Operation</span></span>                                                   | <span data-ttu-id="c751a-172">Méthode</span><span class="sxs-lookup"><span data-stu-id="c751a-172">Method</span></span>                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c751a-173">Combiner</span><span class="sxs-lookup"><span data-stu-id="c751a-173">Combine</span></span>                                                     | [<span data-ttu-id="c751a-174">**CombineWithGeometry**</span><span class="sxs-lookup"><span data-stu-id="c751a-174">**CombineWithGeometry**</span></span>](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| <span data-ttu-id="c751a-175">Limites/limites étendues/limites de récupération, mise à jour de la région modifiée</span><span class="sxs-lookup"><span data-stu-id="c751a-175">Bounds/ Widened Bounds/Retrieve Bounds, Dirty Region update</span></span> | <span data-ttu-id="c751a-176">[**Widening**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span><span class="sxs-lookup"><span data-stu-id="c751a-176">[**Widen**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)</span></span>                             |
| <span data-ttu-id="c751a-177">Test des résultats</span><span class="sxs-lookup"><span data-stu-id="c751a-177">Hit Testing</span></span>                                                 | <span data-ttu-id="c751a-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span><span class="sxs-lookup"><span data-stu-id="c751a-178">[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)</span></span>                                             |
| <span data-ttu-id="c751a-179">Trait</span><span class="sxs-lookup"><span data-stu-id="c751a-179">Stroke</span></span>                                                      | [<span data-ttu-id="c751a-180">**StrokeContainsPoint**</span><span class="sxs-lookup"><span data-stu-id="c751a-180">**StrokeContainsPoint**</span></span>](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| <span data-ttu-id="c751a-181">Comparaison</span><span class="sxs-lookup"><span data-stu-id="c751a-181">Comparison</span></span>                                                  | [<span data-ttu-id="c751a-182">**CompareWithGeometry**</span><span class="sxs-lookup"><span data-stu-id="c751a-182">**CompareWithGeometry**</span></span>](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| <span data-ttu-id="c751a-183">Simplification (supprime les arcs et les courbes de Bézier quadratiques)</span><span class="sxs-lookup"><span data-stu-id="c751a-183">Simplification (removes arcs and quadratic Bezier curves)</span></span>   | [<span data-ttu-id="c751a-184">**Ainsi**</span><span class="sxs-lookup"><span data-stu-id="c751a-184">**Simplify**</span></span>](id2d1geometry-simplify.md)                                                                                                                                 |
| <span data-ttu-id="c751a-185">Pavage</span><span class="sxs-lookup"><span data-stu-id="c751a-185">Tessellation</span></span>                                                | [<span data-ttu-id="c751a-186">**Paver**</span><span class="sxs-lookup"><span data-stu-id="c751a-186">**Tessellate**</span></span>](id2d1geometry-tessellate.md)                                                                                                                             |
| <span data-ttu-id="c751a-187">Contour (supprimer l’intersection)</span><span class="sxs-lookup"><span data-stu-id="c751a-187">Outline (remove intersection)</span></span>                               | [<span data-ttu-id="c751a-188">**Décrire**</span><span class="sxs-lookup"><span data-stu-id="c751a-188">**Outline**</span></span>](id2d1geometry-outline.md)                                                                                                                                   |
| <span data-ttu-id="c751a-189">Calculer la zone ou la longueur d’une géométrie</span><span class="sxs-lookup"><span data-stu-id="c751a-189">Calculate the area or length of a geometry</span></span>                  | <span data-ttu-id="c751a-190">[**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span><span class="sxs-lookup"><span data-stu-id="c751a-190">[**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md)</span></span> |



 

> [!Note]  
> <span data-ttu-id="c751a-191">À partir de Windows 8, vous pouvez utiliser la méthode [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) sur le [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) pour calculer la zone ou la longueur d’une géométrie.</span><span class="sxs-lookup"><span data-stu-id="c751a-191">Starting in Windows 8, you can use the [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) method on the [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) to calculate the area or length of a geometry.</span></span>

 

### <a name="combining-geometries"></a><span data-ttu-id="c751a-192">Combinaison de géométries</span><span class="sxs-lookup"><span data-stu-id="c751a-192">Combining geometries</span></span>

<span data-ttu-id="c751a-193">Pour associer une géométrie à une autre, appelez la méthode [**ID2D1Geometry :: CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) .</span><span class="sxs-lookup"><span data-stu-id="c751a-193">To combine one geometry with another, call the [**ID2D1Geometry::CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) method.</span></span> <span data-ttu-id="c751a-194">Lorsque vous combinez les géométries, vous spécifiez l’une des quatre méthodes d’exécution de l’opération combiner : [**d2d1 \_ combine \_ mode \_ Union**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Union), [**d2d1 \_ combine \_ mode \_ Intersect**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Intersect), [**d2d1 \_ combine \_ mode \_ Xor**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (XOR) et [**d2d1 \_ \_ mode combine \_ Exclude**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Exclude).</span><span class="sxs-lookup"><span data-stu-id="c751a-194">When you combine the geometries, you specify one of the four ways to perform the combine operation: [**D2D1\_COMBINE\_MODE\_UNION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (union), [**D2D1\_COMBINE\_MODE\_INTERSECT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (intersect), [**D2D1\_COMBINE\_MODE\_XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (xor), and [**D2D1\_COMBINE\_MODE\_EXCLUDE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (exclude).</span></span> <span data-ttu-id="c751a-195">L’exemple de code suivant montre deux cercles combinés à l’aide du mode de combinaison Union, où le premier cercle a le point central (75, 75) et le rayon de 50, et le deuxième cercle a le point central de (125, 75) et le rayon de 50.</span><span class="sxs-lookup"><span data-stu-id="c751a-195">The following code example shows two circles that are combined by using the union combine mode, where the first circle has the center point of (75, 75) and the radius of 50, and the second circle has the center point of (125, 75) and the radius of 50.</span></span>


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



<span data-ttu-id="c751a-196">L’illustration suivante montre deux cercles combinés avec un mode combiné d’Union.</span><span class="sxs-lookup"><span data-stu-id="c751a-196">The following illustration shows two circles combined with a combine mode of union.</span></span>

![illustration de deux cercles se chevauchant combinés dans une Union](images/combine-mode-union.png)

<span data-ttu-id="c751a-198">Pour obtenir des illustrations de tous les modes combinés, consultez l' [**\_ \_ énumération du mode de combinaison d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span><span class="sxs-lookup"><span data-stu-id="c751a-198">For illustrations of all the combine modes, see the [**D2D1\_COMBINE\_MODE enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).</span></span>

### <a name="widen"></a><span data-ttu-id="c751a-199">Élargi</span><span class="sxs-lookup"><span data-stu-id="c751a-199">Widen</span></span>

<span data-ttu-id="c751a-200">La méthode [**Widening**](id2d1geometry-widen.md) génère une nouvelle géométrie dont le remplissage est équivalent au contour de la géométrie existante, puis écrit le résultat dans l’objet [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) spécifié.</span><span class="sxs-lookup"><span data-stu-id="c751a-200">The [**Widen**](id2d1geometry-widen.md) method generates a new geometry whose fill is equivalent to stroking the existing geometry, and then writes the result to the specified [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) object.</span></span> <span data-ttu-id="c751a-201">L’exemple de code suivant appelle [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) sur l’objet [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="c751a-201">The following code example calls [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) on the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object.</span></span> <span data-ttu-id="c751a-202">Si l' **ouverture** est réussie, elle appelle **Widening** sur l’objet Geometry.</span><span class="sxs-lookup"><span data-stu-id="c751a-202">If **Open** succeeds, it calls **Widen** on the geometry object.</span></span>


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



### <a name="tessellate"></a><span data-ttu-id="c751a-203">Paver</span><span class="sxs-lookup"><span data-stu-id="c751a-203">Tessellate</span></span>

<span data-ttu-id="c751a-204">La méthode [**paver**](id2d1geometry-tessellate.md) crée un ensemble de triangles enroulés dans le sens des aiguilles d’une montre qui couvrent la géométrie après sa transformation à l’aide de la matrice spécifiée et aplatie à l’aide de la tolérance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c751a-204">The [**Tessellate**](id2d1geometry-tessellate.md) method creates a set of clockwise-wound triangles that cover the geometry after it is transformed by using the specified matrix and flattened by using the specified tolerance.</span></span> <span data-ttu-id="c751a-205">L’exemple de code suivant utilise **paver** pour créer une liste de triangles représentant *pPathGeometry*.</span><span class="sxs-lookup"><span data-stu-id="c751a-205">The following code example uses **Tessellate** to create a list of triangles that represent *pPathGeometry*.</span></span> <span data-ttu-id="c751a-206">Les triangles sont stockés dans un [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, puis transférés à un membre de classe, *m \_ pStrokeMesh*, pour une utilisation ultérieure lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="c751a-206">The triangles are stored in an [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh*, then transferred to a class member, *m\_pStrokeMesh*, for later use when rendering.</span></span>


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



### <a name="fillcontainspoint-and-strokecontainspoint"></a><span data-ttu-id="c751a-207">FillContainsPoint et StrokeContainsPoint</span><span class="sxs-lookup"><span data-stu-id="c751a-207">FillContainsPoint and StrokeContainsPoint</span></span>

<span data-ttu-id="c751a-208">La méthode [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) indique si la zone remplie par la géométrie contient le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="c751a-208">The [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) method indicates whether the area filled by the geometry contains the specified point.</span></span> <span data-ttu-id="c751a-209">Vous pouvez utiliser cette méthode pour effectuer un test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="c751a-209">You can use this method to do hit testing.</span></span> <span data-ttu-id="c751a-210">L’exemple de code suivant appelle **FillContainsPoint** sur un objet [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , en passant un point à (0,0) et une matrice d' [**identité**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) .</span><span class="sxs-lookup"><span data-stu-id="c751a-210">The following code example calls **FillContainsPoint** on an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) object, passing in a point at (0,0) and an [**Identity**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) matrix.</span></span>


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



<span data-ttu-id="c751a-211">La méthode [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) détermine si le trait de la géométrie contient le point spécifié.</span><span class="sxs-lookup"><span data-stu-id="c751a-211">The [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) method determines whether the geometry's stroke contains the specified point.</span></span> <span data-ttu-id="c751a-212">Vous pouvez utiliser cette méthode pour effectuer un test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="c751a-212">You can use this method to do hit testing.</span></span> <span data-ttu-id="c751a-213">L’exemple de code suivant utilise **StrokeContainsPoint**.</span><span class="sxs-lookup"><span data-stu-id="c751a-213">The following code example uses **StrokeContainsPoint**.</span></span>


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



### <a name="simplify"></a><span data-ttu-id="c751a-214">Simplifier </span><span class="sxs-lookup"><span data-stu-id="c751a-214">Simplify</span></span>

<span data-ttu-id="c751a-215">La méthode [**simplifier**](id2d1geometry-simplify.md) supprime les arcs et les courbes de Bézier quadratiques d’une géométrie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c751a-215">The [**Simplify**](id2d1geometry-simplify.md) method removes arcs and quadratic Bezier curves from a specified geometry.</span></span> <span data-ttu-id="c751a-216">Ainsi, la géométrie résultante contient uniquement des lignes et, éventuellement, des courbes de Bézier cubiques.</span><span class="sxs-lookup"><span data-stu-id="c751a-216">So, the resulting geometry contains only lines and, optionally, cubic Bezier curves.</span></span> <span data-ttu-id="c751a-217">L’exemple de code suivant utilise **simplifier** pour transformer une géométrie avec des courbes de Bézier en une géométrie qui contient uniquement des segments de ligne.</span><span class="sxs-lookup"><span data-stu-id="c751a-217">The following code example uses **Simplify** to transform a geometry with Bezier curves into a geometry that contains only line segments.</span></span>


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



### <a name="computelength-and-computearea"></a><span data-ttu-id="c751a-218">ComputeLength et ComputeArea</span><span class="sxs-lookup"><span data-stu-id="c751a-218">ComputeLength and ComputeArea</span></span>

<span data-ttu-id="c751a-219">La méthode [**ComputeLength**](id2d1geometry-computelength.md) calcule la longueur de la géométrie spécifiée si chaque segment a été déroulé dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="c751a-219">The [**ComputeLength**](id2d1geometry-computelength.md) method calculates the length of the specified geometry if each segment were unrolled into a line.</span></span> <span data-ttu-id="c751a-220">Cela comprend le segment fermant implicite si la géométrie est fermée.</span><span class="sxs-lookup"><span data-stu-id="c751a-220">This includes the implicit closing segment if the geometry is closed.</span></span> <span data-ttu-id="c751a-221">L’exemple de code suivant utilise **ComputeLength** pour calculer la longueur d’un cercle spécifié (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="c751a-221">The following code example uses **ComputeLength** to compute the length of a specified circle (**m\_pCircleGeometry1**).</span></span>


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



<span data-ttu-id="c751a-222">La méthode [**ComputeArea**](id2d1geometry-computearea.md) calcule la zone de la géométrie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c751a-222">The [**ComputeArea**](id2d1geometry-computearea.md) method calculates the area of the specified geometry.</span></span> <span data-ttu-id="c751a-223">L’exemple de code suivant utilise **ComputeArea** pour calculer la zone d’un cercle spécifié (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="c751a-223">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a><span data-ttu-id="c751a-224">CompareWithGeometry</span><span class="sxs-lookup"><span data-stu-id="c751a-224">CompareWithGeometry</span></span>

<span data-ttu-id="c751a-225">La méthode [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) décrit l’intersection entre la géométrie qui appelle cette méthode et la géométrie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c751a-225">The [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) method describes the intersection between the geometry that calls this method and the specified geometry.</span></span> <span data-ttu-id="c751a-226">Les valeurs possibles pour l’intersection incluent la relation [**d2d1 \_ Geometry \_ \_ disjointe**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (disjointe), la **\_ relation Geometry d2d1 \_ \_ est \_ contenue** (est contenue), la **\_ relation Geometry d2d1 \_ \_ contient** (Contains) et le **\_ \_ \_ chevauchement de la relation Geometry d2d1** (chevauchement).</span><span class="sxs-lookup"><span data-stu-id="c751a-226">The possible values for intersection include [**D2D1\_GEOMETRY\_RELATION\_DISJOINT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (disjoint), **D2D1\_GEOMETRY\_RELATION\_IS\_CONTAINED** (is contained), **D2D1\_GEOMETRY\_RELATION\_CONTAINS** (contains), and **D2D1\_GEOMETRY\_RELATION\_OVERLAP** (overlap).</span></span> <span data-ttu-id="c751a-227">« disjointe » signifie que deux remplissages de géométrie ne se croisent pas du tout.</span><span class="sxs-lookup"><span data-stu-id="c751a-227">"disjoint" means that two geometry fills do not intersect at all.</span></span> <span data-ttu-id="c751a-228">« est contenu » signifie que la géométrie est entièrement contenue dans la géométrie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c751a-228">"is contained" means that the geometry is completely contained by the specified geometry.</span></span> <span data-ttu-id="c751a-229">« Contains » signifie que la géométrie contient entièrement la géométrie spécifiée, et « se chevauchent » signifie que les deux géométries se chevauchent, mais ne contiennent pas complètement l’autre.</span><span class="sxs-lookup"><span data-stu-id="c751a-229">"contains" means that the geometry completely contains the specified geometry, and "overlap" means the two geometries overlap but neither completely contains the other.</span></span>

<span data-ttu-id="c751a-230">L’exemple de code suivant montre comment comparer deux cercles qui ont le même rayon de 50, mais qui sont décalés de 50.</span><span class="sxs-lookup"><span data-stu-id="c751a-230">The following code example shows how to compare two circles that have the same radius of 50 but are offset by 50.</span></span>


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



### <a name="outline"></a><span data-ttu-id="c751a-231">Contour</span><span class="sxs-lookup"><span data-stu-id="c751a-231">Outline</span></span>

<span data-ttu-id="c751a-232">La méthode [**Outline**](id2d1geometry-outline.md) calcule le contour de la géométrie (une version de la géométrie dans laquelle aucune figure n’entre elle-même ou une autre figure) et écrit le résultat dans un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span><span class="sxs-lookup"><span data-stu-id="c751a-232">The [**Outline**](id2d1geometry-outline.md) method computes the outline of the geometry (a version of the geometry in which no figure crosses itself or any other figure) and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span> <span data-ttu-id="c751a-233">L’exemple de code suivant utilise **Outline** pour construire une géométrie équivalente sans aucune auto-intersection.</span><span class="sxs-lookup"><span data-stu-id="c751a-233">The following code example uses **Outline** to construct an equivalent geometry without any self-intersections.</span></span> <span data-ttu-id="c751a-234">Elle utilise la tolérance d’aplatissement par défaut.</span><span class="sxs-lookup"><span data-stu-id="c751a-234">It uses the default flattening tolerance.</span></span>


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



### <a name="getbounds-and-getwidenedbounds"></a><span data-ttu-id="c751a-235">GetBounds et GetWidenedBounds</span><span class="sxs-lookup"><span data-stu-id="c751a-235">GetBounds and GetWidenedBounds</span></span>

<span data-ttu-id="c751a-236">La méthode [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) récupère les limites de la géométrie.</span><span class="sxs-lookup"><span data-stu-id="c751a-236">The [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) method retrieves the bounds of the geometry.</span></span> <span data-ttu-id="c751a-237">L’exemple de code suivant utilise **GetBounds** pour récupérer les limites d’un cercle spécifié (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="c751a-237">The following code example uses **GetBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**).</span></span>


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



<span data-ttu-id="c751a-238">La méthode [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) récupère les limites de la géométrie après qu’elle a été élargie par la largeur et le style de trait spécifiés et transformée par la matrice spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c751a-238">The [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) method retrieves the bounds of the geometry after it is widened by the specified stroke width and style and transformed by the specified matrix.</span></span> <span data-ttu-id="c751a-239">L’exemple de code suivant utilise **GetWidenedBounds** pour récupérer les limites d’un cercle spécifié (**m \_ pCircleGeometry1**) après qu’il a été élargi par la largeur de trait spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c751a-239">The following code example uses **GetWidenedBounds** to retrieve the bounds of a specified circle (**m\_pCircleGeometry1**) after it is widened by the specified stroke width.</span></span>


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



### <a name="computepointatlength"></a><span data-ttu-id="c751a-240">ComputePointAtLength</span><span class="sxs-lookup"><span data-stu-id="c751a-240">ComputePointAtLength</span></span>

<span data-ttu-id="c751a-241">La méthode [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) calcule le vecteur de point et de tangente à la distance spécifiée le long de la géométrie.</span><span class="sxs-lookup"><span data-stu-id="c751a-241">The [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) method calculates the point and tangent vector at the specified distance along the geometry.</span></span> <span data-ttu-id="c751a-242">L’exemple de code suivant utilise **ComputePointAtLength**.</span><span class="sxs-lookup"><span data-stu-id="c751a-242">The following code example uses **ComputePointAtLength**.</span></span>


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a><span data-ttu-id="c751a-243">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c751a-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c751a-244">Vue d’ensemble des géométries de tracés</span><span class="sxs-lookup"><span data-stu-id="c751a-244">Path Geometries Overview</span></span>](path-geometries-overview.md)
</dt> <dt>

[<span data-ttu-id="c751a-245">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="c751a-245">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 