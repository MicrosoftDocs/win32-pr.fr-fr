---
title: Vue d’ensemble des géométries de tracés
description: Décrit comment utiliser des géométries de tracés pour définir des formes complexes.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104551472"
---
# <a name="path-geometries-overview"></a><span data-ttu-id="973fc-103">Vue d’ensemble des géométries de tracés</span><span class="sxs-lookup"><span data-stu-id="973fc-103">Path Geometries Overview</span></span>

<span data-ttu-id="973fc-104">Cette rubrique explique comment utiliser des géométries de tracés Direct2D pour créer des dessins complexes.</span><span class="sxs-lookup"><span data-stu-id="973fc-104">This topic describes how to use Direct2D path geometries to create complex drawings.</span></span> <span data-ttu-id="973fc-105">Elle contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="973fc-105">It contains the following sections.</span></span>

-   [<span data-ttu-id="973fc-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="973fc-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="973fc-107">Géométries de tracés dans Direct2D</span><span class="sxs-lookup"><span data-stu-id="973fc-107">Path Geometries in Direct2D</span></span>](#path-geometries-in-direct2d)
-   [<span data-ttu-id="973fc-108">Utilisation d’un ID2D1GeometrySink pour remplir une géométrie de tracé</span><span class="sxs-lookup"><span data-stu-id="973fc-108">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [<span data-ttu-id="973fc-109">Exemple : créer un dessin complexe</span><span class="sxs-lookup"><span data-stu-id="973fc-109">Example: Create a Complex Drawing</span></span>](#example-create-a-complex-drawing)
    -   [<span data-ttu-id="973fc-110">Créer une géométrie de tracé pour la montagne de gauche</span><span class="sxs-lookup"><span data-stu-id="973fc-110">Create a Path Geometry for the Left Mountain</span></span>](#create-a-path-geometry-for-the-left-mountain)
    -   [<span data-ttu-id="973fc-111">Créer une géométrie de tracé pour la montagne droite</span><span class="sxs-lookup"><span data-stu-id="973fc-111">Create a Path Geometry for the Right Mountain</span></span>](#create-a-path-geometry-for-the-right-mountain)
    -   [<span data-ttu-id="973fc-112">Créer une géométrie de tracé pour le soleil</span><span class="sxs-lookup"><span data-stu-id="973fc-112">Create a Path Geometry for the Sun</span></span>](#create-a-path-geometry-for-the-sun)
    -   [<span data-ttu-id="973fc-113">Créer une géométrie de tracé pour la rivière</span><span class="sxs-lookup"><span data-stu-id="973fc-113">Create a Path Geometry for the River</span></span>](#create-a-path-geometry-for-the-river)
    -   [<span data-ttu-id="973fc-114">Restituer les géométries de tracés sur l’affichage</span><span class="sxs-lookup"><span data-stu-id="973fc-114">Render the Path Geometries onto the Display</span></span>](#render-the-path-geometries-onto-the-display)
-   [<span data-ttu-id="973fc-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="973fc-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="973fc-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="973fc-116">Prerequisites</span></span>

<span data-ttu-id="973fc-117">Cette vue d’ensemble suppose que vous êtes familiarisé avec la création d’applications Direct2D de base, comme décrit dans [création d’une application Direct2d simple](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="973fc-117">This overview assumes that you are familiar with creating basic Direct2D applications, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span> <span data-ttu-id="973fc-118">Elle suppose également que vous êtes familiarisé avec les fonctionnalités de base des géométries Direct2D, comme décrit dans la [vue d’ensemble des géométries](direct2d-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="973fc-118">It also assumes that you are familiar with the basic features of Direct2D geometries, as described in the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="path-geometries-in-direct2d"></a><span data-ttu-id="973fc-119">Géométries de tracés dans Direct2D</span><span class="sxs-lookup"><span data-stu-id="973fc-119">Path Geometries in Direct2D</span></span>

<span data-ttu-id="973fc-120">Les géométries de tracés sont représentées par l’interface [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="973fc-120">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="973fc-121">Pour instancier une géométrie de tracé, appelez la méthode [**ID2D1Factory :: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="973fc-121">To instantiate a path geometry, call the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method.</span></span> <span data-ttu-id="973fc-122">Ces objets peuvent être utilisés pour décrire des chiffres géométriques complexes composés de segments tels que des arcs, des courbes et des lignes.</span><span class="sxs-lookup"><span data-stu-id="973fc-122">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="973fc-123">Pour remplir une géométrie de tracé avec des figures et des segments, appelez la méthode [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) pour récupérer un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) et utilisez les méthodes du récepteur Geometry pour ajouter des figures et des segments à la géométrie de tracé.</span><span class="sxs-lookup"><span data-stu-id="973fc-123">To populate a path geometry with figures and segments, call the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to retrieve an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) and use the geometry sink's methods to add figures and segments to the path geometry.</span></span>

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a><span data-ttu-id="973fc-124">Utilisation d’un ID2D1GeometrySink pour remplir une géométrie de tracé</span><span class="sxs-lookup"><span data-stu-id="973fc-124">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>

<span data-ttu-id="973fc-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) décrit un tracé géométrique qui peut contenir des lignes, des arcs, des courbes de Bézier cubiques et des courbes de Bézier quadratiques.</span><span class="sxs-lookup"><span data-stu-id="973fc-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) describes a geometric path that can contain lines, arcs, cubic Bezier curves, and quadratic Bezier curves.</span></span>

<span data-ttu-id="973fc-126">Un récepteur de géométrie se compose d’un ou de plusieurs figures.</span><span class="sxs-lookup"><span data-stu-id="973fc-126">A geometry sink consists of one or more figures.</span></span> <span data-ttu-id="973fc-127">Chaque figure est constituée d’un ou de plusieurs segments de ligne, de courbe ou d’arc.</span><span class="sxs-lookup"><span data-stu-id="973fc-127">Each figure is made up of one or more line, curve, or arc segments.</span></span> <span data-ttu-id="973fc-128">Pour créer une figure, appelez la méthode [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) , en passant le point de départ de la figure, puis utilisez ses méthodes Add (telles que [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) et [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) pour ajouter des segments.</span><span class="sxs-lookup"><span data-stu-id="973fc-128">To create a figure, call the [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) method, passing in the figure's starting point, and then use its Add methods (such as [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) and [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to add segments.</span></span> <span data-ttu-id="973fc-129">Lorsque vous avez terminé d’ajouter des segments, appelez la méthode [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) .</span><span class="sxs-lookup"><span data-stu-id="973fc-129">When you are finished adding segments, call the [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) method.</span></span> <span data-ttu-id="973fc-130">Vous pouvez répéter cette séquence pour créer des chiffres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="973fc-130">You can repeat this sequence to create additional figures.</span></span> <span data-ttu-id="973fc-131">Lorsque vous avez terminé de créer des figures, appelez la méthode [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .</span><span class="sxs-lookup"><span data-stu-id="973fc-131">When you are finished creating figures, call the [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) method.</span></span>

## <a name="example-create-a-complex-drawing"></a><span data-ttu-id="973fc-132">Exemple : créer un dessin complexe</span><span class="sxs-lookup"><span data-stu-id="973fc-132">Example: Create a Complex Drawing</span></span>

<span data-ttu-id="973fc-133">L’illustration suivante montre un dessin complexe avec des courbes, des arcs et des courbes de Bézier.</span><span class="sxs-lookup"><span data-stu-id="973fc-133">The following illustration shows a complex drawing with lines, arcs, and Bezier curves.</span></span> <span data-ttu-id="973fc-134">L’exemple de code suivant montre comment créer le dessin à l’aide de quatre objets Geometry, un pour la montagne gauche, un pour la montagne droite, un pour le fleuve et un pour le soleil avec des halos.</span><span class="sxs-lookup"><span data-stu-id="973fc-134">The code example that follows shows how to create the drawing by using four path geometry objects, one for the left mountain, one for the right mountain, one for the river, and one for the sun with flares.</span></span>

![illustration d’une rivière, de montagnes et du soleil, à l’aide de géométries de tracés](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a><span data-ttu-id="973fc-136">Créer une géométrie de tracé pour la montagne de gauche</span><span class="sxs-lookup"><span data-stu-id="973fc-136">Create a Path Geometry for the Left Mountain</span></span>

<span data-ttu-id="973fc-137">L’exemple crée d’abord une géométrie de tracé pour le VTT gauche, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="973fc-137">The example first creates a path geometry for the left mountain as shown in the following illustration.</span></span>

![Montre un dessin complexe d’un polygone qui affiche une montagne.](images/path-geo-leftmnt.png)

<span data-ttu-id="973fc-139">Pour créer la montagne de gauche, l’exemple appelle la méthode [**ID2D1Factory :: CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) pour créer un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).</span><span class="sxs-lookup"><span data-stu-id="973fc-139">To create the left mountain, the example calls the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



<span data-ttu-id="973fc-140">L’exemple utilise ensuite la méthode [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) pour obtenir un récepteur Geometry à partir d’un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) et le stocke dans la variable *pSink* .</span><span class="sxs-lookup"><span data-stu-id="973fc-140">The example then uses the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to obtain a geometry sink from an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and stores it in the *pSink* variable.</span></span>


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



<span data-ttu-id="973fc-141">L’exemple appelle ensuite [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), en passant le début de la [**\_ figure d2d1 \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) , qui indique que cette figure est remplie, puis appelle [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), en passant un tableau de points de [**d2d1 \_ point \_ 2F**](d2d1-point-2f.md) , (267, 177), (236, 192), (212, 160), (156, 255) et (346, 255).</span><span class="sxs-lookup"><span data-stu-id="973fc-141">The example then calls [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), passing in [**D2D1\_FIGURE\_BEGIN\_FILLED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) that indicates this figure is filled, then calls [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), passing in an array of [**D2D1\_POINT\_2F**](d2d1-point-2f.md) points, (267, 177), (236, 192), (212, 160), (156, 255) and (346, 255).</span></span>

<span data-ttu-id="973fc-142">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="973fc-142">The following code shows how to do this.</span></span>


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a><span data-ttu-id="973fc-143">Créer une géométrie de tracé pour la montagne droite</span><span class="sxs-lookup"><span data-stu-id="973fc-143">Create a Path Geometry for the Right Mountain</span></span>

<span data-ttu-id="973fc-144">L’exemple crée ensuite une autre géométrie de tracé pour la montagne droite avec des points (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) et (575, 263).</span><span class="sxs-lookup"><span data-stu-id="973fc-144">The example then creates another path geometry for the right mountain with points (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263), and (575, 263).</span></span> <span data-ttu-id="973fc-145">L’illustration suivante montre l’affichage de la montagne droite.</span><span class="sxs-lookup"><span data-stu-id="973fc-145">The following illustration shows how the right mountain is displayed.</span></span>

![illustration d’un polygone montrant une montagne](images/path-geo-rightmnt.png)

<span data-ttu-id="973fc-147">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="973fc-147">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a><span data-ttu-id="973fc-148">Créer une géométrie de tracé pour le soleil</span><span class="sxs-lookup"><span data-stu-id="973fc-148">Create a Path Geometry for the Sun</span></span>

<span data-ttu-id="973fc-149">L’exemple remplit ensuite une autre géométrie de tracé pour le soleil, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="973fc-149">The example then populates another path geometry for the sun as shown in the following illustration.</span></span>

![illustration d’un arc et de courbes Bézier montrant le soleil](images/path-geo-sun.png)

<span data-ttu-id="973fc-151">Pour ce faire, la géométrie du tracé crée un récepteur et ajoute une figure pour l’arc et une figure pour chaque Halo au récepteur.</span><span class="sxs-lookup"><span data-stu-id="973fc-151">To do this, the path geometry creates a sink, and adds a figure for the arc and a figure for each flare to the sink.</span></span> <span data-ttu-id="973fc-152">En répétant la séquence de [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), ses méthodes Add (telles que [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) et [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), plusieurs figures sont ajoutées au récepteur.</span><span class="sxs-lookup"><span data-stu-id="973fc-152">By repeating the sequence of [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), its Add (such as [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) methods, and [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), multiple figures are added to the sink.</span></span>

<span data-ttu-id="973fc-153">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="973fc-153">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a><span data-ttu-id="973fc-154">Créer une géométrie de tracé pour la rivière</span><span class="sxs-lookup"><span data-stu-id="973fc-154">Create a Path Geometry for the River</span></span>

<span data-ttu-id="973fc-155">L’exemple crée ensuite un autre tracé géométrique pour la rivière qui contient des courbes de Bézier.</span><span class="sxs-lookup"><span data-stu-id="973fc-155">The example then creates another geometry path for the river that contains Bezier curves.</span></span> <span data-ttu-id="973fc-156">L’illustration suivante montre comment la rivière est affichée.</span><span class="sxs-lookup"><span data-stu-id="973fc-156">The following illustration shows how the river is displayed.</span></span>

![illustration des courbes Bézier montrant une rivière](images/path-geo-river.png)

<span data-ttu-id="973fc-158">Le code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="973fc-158">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a><span data-ttu-id="973fc-159">Restituer les géométries de tracés sur l’affichage</span><span class="sxs-lookup"><span data-stu-id="973fc-159">Render the Path Geometries onto the Display</span></span>

<span data-ttu-id="973fc-160">Le code suivant montre comment restituer les géométries de tracés remplies sur l’affichage.</span><span class="sxs-lookup"><span data-stu-id="973fc-160">The following code shows how to render the populated path geometries on the display.</span></span> <span data-ttu-id="973fc-161">Il commence par dessiner et peint la géométrie du soleil, puis la géométrie de montagne gauche, la géométrie de la rivière et enfin la bonne géométrie de montagne.</span><span class="sxs-lookup"><span data-stu-id="973fc-161">It first draws and paints the sun geometry, next the left mountain geometry, then the river geometry, and finally the right mountain geometry.</span></span>


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



<span data-ttu-id="973fc-162">L’exemple complet présente l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="973fc-162">The complete example outputs the following illustration.</span></span>

![illustration d’une rivière, de montagnes et du soleil, à l’aide de géométries de tracés](images/path-geo-mnts.png)

## <a name="related-topics"></a><span data-ttu-id="973fc-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="973fc-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="973fc-165">Création d’une application Direct2D simple</span><span class="sxs-lookup"><span data-stu-id="973fc-165">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> <dt>

[<span data-ttu-id="973fc-166">Vue d’ensemble des géométries</span><span class="sxs-lookup"><span data-stu-id="973fc-166">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> </dl>

 

 