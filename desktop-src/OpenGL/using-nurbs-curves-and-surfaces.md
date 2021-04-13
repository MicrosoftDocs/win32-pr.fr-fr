---
title: Utilisation des courbes et des surfaces NURBS
description: Les fonctions NURBS B-spline (NURBS) non uniformes fournissent des descriptions générales et puissantes des courbes et des surfaces en deux et trois dimensions, convertissant les courbes et les surfaces en évaluateurs OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- Utilitaire OpenGL (GLU), logique B-spline rationnelle non uniforme (NURBS)
- GLU (utilitaire OpenGL), logique B-spline rationnelle non uniforme (NURBS)
- B-spline rationnelle non uniforme (NURBS) OpenGL
- NURBS (non-uniform rational B-spline) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f85e9a2045c417007c34d714ae6635ebfaf1180
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309641"
---
# <a name="using-nurbs-curves-and-surfaces"></a><span data-ttu-id="68756-107">Utilisation des courbes et des surfaces NURBS</span><span class="sxs-lookup"><span data-stu-id="68756-107">Using NURBS Curves and Surfaces</span></span>

<span data-ttu-id="68756-108">Les fonctions NURBS B-spline (NURBS) non uniformes fournissent des descriptions générales et puissantes des courbes et des surfaces en deux et trois dimensions, convertissant les courbes et les surfaces en évaluateurs OpenGL.</span><span class="sxs-lookup"><span data-stu-id="68756-108">Non-Uniform Rational B-Spline (NURBS) functions provide general and powerful descriptions of curves and surfaces in two and three dimensions, converting the curves and surfaces to OpenGL evaluators.</span></span> <span data-ttu-id="68756-109">Les fonctions NURBS peuvent représenter une géométrie dans de nombreux systèmes de conception mécanique assistée par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="68756-109">The NURBS functions can represent geometry in many computer-aided mechanical design systems.</span></span> <span data-ttu-id="68756-110">Ils peuvent afficher des courbes et des surfaces dans divers styles, et ils peuvent gérer automatiquement la sous-division adaptative qui tessellates le domaine en triangles plus petits dans les régions de bords haute courbure et à proximité des silhouettes.</span><span class="sxs-lookup"><span data-stu-id="68756-110">They can render curves and surfaces in a variety of styles, and they can automatically handle adaptive subdivision that tessellates the domain into smaller triangles in regions of high curvature and near silhouette edges.</span></span> <span data-ttu-id="68756-111">Les fonctions NURBS sont classées dans les catégories suivantes.</span><span class="sxs-lookup"><span data-stu-id="68756-111">NURBS functions fall into the following categories.</span></span>

<span data-ttu-id="68756-112">Pour gérer un objet NURBS, utilisez :</span><span class="sxs-lookup"><span data-stu-id="68756-112">To manage a NURBS object, use:</span></span>

-   <span data-ttu-id="68756-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (créer un objet NURBS)</span><span class="sxs-lookup"><span data-stu-id="68756-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (create a NURBS object)</span></span>
-   <span data-ttu-id="68756-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (supprime un objet NURBS)</span><span class="sxs-lookup"><span data-stu-id="68756-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (deletes a NURBS object)</span></span>
-   <span data-ttu-id="68756-115">[*gluNurbsCallback*](glunurbs.md) (établit une fonction de gestion des erreurs)</span><span class="sxs-lookup"><span data-stu-id="68756-115">[*gluNurbsCallback*](glunurbs.md) (establishes an error-handling function)</span></span>

<span data-ttu-id="68756-116">Pour spécifier les courbes souhaitées, utilisez :</span><span class="sxs-lookup"><span data-stu-id="68756-116">To specify the desired curves, use:</span></span>

-   [<span data-ttu-id="68756-117">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="68756-117">**gluBeginCurve**</span></span>](glubegincurve.md)
-   [<span data-ttu-id="68756-118">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="68756-118">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="68756-119">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="68756-119">**gluEndCurve**</span></span>](gluendcurve.md)

<span data-ttu-id="68756-120">Pour spécifier les surfaces souhaitées, utilisez :</span><span class="sxs-lookup"><span data-stu-id="68756-120">To specify the desired surfaces, use:</span></span>

-   [<span data-ttu-id="68756-121">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="68756-121">**gluBeginSurface**</span></span>](glubeginsurface.md)
-   [<span data-ttu-id="68756-122">**gluNurbsSurface**</span><span class="sxs-lookup"><span data-stu-id="68756-122">**gluNurbsSurface**</span></span>](glunurbssurface.md)
-   [<span data-ttu-id="68756-123">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="68756-123">**gluEndSurface**</span></span>](gluendsurface.md)

<span data-ttu-id="68756-124">Vous pouvez également spécifier une zone de suppression, qui définit un sous-ensemble du domaine de la surface NURBS à évaluer afin de pouvoir créer des surfaces qui ont des limites lissées ou qui contiennent des trous.</span><span class="sxs-lookup"><span data-stu-id="68756-124">You can also specify a trimming region, which defines a subset of the NURBS surface domain to be evaluated so you can create surfaces that have smooth boundaries or that contain holes.</span></span>

<span data-ttu-id="68756-125">Pour spécifier la région de suppression, utilisez :</span><span class="sxs-lookup"><span data-stu-id="68756-125">To specify the trimming region, use:</span></span>

-   [<span data-ttu-id="68756-126">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="68756-126">**gluBeginTrim**</span></span>](glubegintrim.md)
-   [<span data-ttu-id="68756-127">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="68756-127">**gluPwlCurve**</span></span>](glupwlcurve.md)
-   [<span data-ttu-id="68756-128">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="68756-128">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="68756-129">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="68756-129">**gluEndTrim**</span></span>](gluendtrim.md)

<span data-ttu-id="68756-130">Comme avec les objets quadric, vous pouvez contrôler le rendu des courbes et des surfaces NURBS.</span><span class="sxs-lookup"><span data-stu-id="68756-130">As with quadric objects, you can control how NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="68756-131">Vous pouvez déterminer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="68756-131">You can determine:</span></span>

-   <span data-ttu-id="68756-132">Indique s’il faut ignorer une courbe ou une surface dont le Polyhedron de contrôle se trouve en dehors de la fenêtre d’affichage actuelle.</span><span class="sxs-lookup"><span data-stu-id="68756-132">Whether to discard a curve or surface whose control polyhedron lies outside the current viewport.</span></span>
-   <span data-ttu-id="68756-133">Longueur maximale (en pixels) des bords des polygones utilisés pour le rendu des courbes et des surfaces.</span><span class="sxs-lookup"><span data-stu-id="68756-133">The maximum length (in pixels) of edges of polygons used to render curves and surfaces.</span></span>
-   <span data-ttu-id="68756-134">Si vous allez utiliser la matrice de projection, la matrice modelview et la fenêtre d’affichage du serveur OpenGL ou les fournir explicitement avec [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).</span><span class="sxs-lookup"><span data-stu-id="68756-134">Whether you will take the projection matrix, modelview matrix, and viewport from the OpenGL server or supply them explictly with [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).</span></span>

<span data-ttu-id="68756-135">Utilisez [**gluNurbsProperty**](glunurbsproperty.md) pour définir ces propriétés, ou utilisez les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="68756-135">Use [**gluNurbsProperty**](glunurbsproperty.md) to set these properties, or use the default values.</span></span> <span data-ttu-id="68756-136">Vous pouvez interroger un objet NURBS sur son style de rendu avec [**gluGetNurbsProperty**](glugetnurbsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="68756-136">You can query a NURBS object about its rendering style with [**gluGetNurbsProperty**](glugetnurbsproperty.md).</span></span>

 

 




