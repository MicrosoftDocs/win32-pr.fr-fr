---
title: Polygones le pavage
description: Polygones le pavage
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Utilitaire OpenGL (GLU), pavage
- GLU (utilitaire OpenGL), pavage
- Utilitaire OpenGL (GLU), polygones simples
- GLU (utilitaire OpenGL), polygones simples
- polygones simples OpenGL
- Utilitaire OpenGL (GLU), polygones complexes
- GLU (utilitaire OpenGL), polygones complexes
- polygones complexes OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512066"
---
# <a name="tessellating-polygons"></a><span data-ttu-id="70015-111">Polygones le pavage</span><span class="sxs-lookup"><span data-stu-id="70015-111">Tessellating Polygons</span></span>

<span data-ttu-id="70015-112">OpenGL peut afficher directement uniquement les polygones convexes simples.</span><span class="sxs-lookup"><span data-stu-id="70015-112">OpenGL can directly display only simple convex polygons.</span></span> <span data-ttu-id="70015-113">Un polygone est simple dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="70015-113">A polygon is simple if:</span></span>

-   <span data-ttu-id="70015-114">Les bords se croisent uniquement aux sommets.</span><span class="sxs-lookup"><span data-stu-id="70015-114">The edges intersect only at vertices.</span></span>
-   <span data-ttu-id="70015-115">Il n’y a aucun vertex dupliqué.</span><span class="sxs-lookup"><span data-stu-id="70015-115">There are no duplicate vertices.</span></span>
-   <span data-ttu-id="70015-116">Exactement deux bords se rencontrent à n’importe quel vertex.</span><span class="sxs-lookup"><span data-stu-id="70015-116">Exactly two edges meet at any vertex.</span></span>

<span data-ttu-id="70015-117">Pour afficher des polygones simples ou des polygones simples contenant des trous, vous devez d’abord facettiser les polygones (subdivisions en polygones convexes).</span><span class="sxs-lookup"><span data-stu-id="70015-117">To display simple nonconvex polygons or simple polygons containing holes, you must first triangulate the polygons (subdivide them into convex polygons).</span></span> <span data-ttu-id="70015-118">Une telle sous-division est appelée *pavage*.</span><span class="sxs-lookup"><span data-stu-id="70015-118">Such subdivision is called *tessellation*.</span></span> <span data-ttu-id="70015-119">GLU fournit une collection de fonctions qui effectuent le pavage.</span><span class="sxs-lookup"><span data-stu-id="70015-119">GLU provides a collection of functions that perform tessellation.</span></span> <span data-ttu-id="70015-120">Notez que les fonctions de pavage GLU ne peuvent pas gérer les polygones non simples. Il n’existe pas de méthode OpenGL standard pour gérer ces polygones.</span><span class="sxs-lookup"><span data-stu-id="70015-120">Note that the GLU tessellation functions can't handle nonsimple polygons; there is no standard OpenGL method to handle such polygons.</span></span>

<span data-ttu-id="70015-121">Étant donné que la facettisation est souvent requise et peut être plutôt délicate, cette section décrit en détail les fonctions de pavage GLU.</span><span class="sxs-lookup"><span data-stu-id="70015-121">Because tessellation is often required and can be rather tricky, this section describes the GLU tessellation functions in detail.</span></span> <span data-ttu-id="70015-122">Ces fonctions prennent comme des polygones simples en entrée qui peuvent inclure des trous, et elles retournent une combinaison de triangles, de maillages de triangle et de fans de triangle.</span><span class="sxs-lookup"><span data-stu-id="70015-122">These functions take as input arbitrary simple polygons that might include holes, and they return some combination of triangles, triangle meshes, and triangle fans.</span></span> <span data-ttu-id="70015-123">Si vous ne souhaitez pas gérer les maillages ou les ventilateurs, vous pouvez spécifier que les fonctions de pavage retournent uniquement des triangles.</span><span class="sxs-lookup"><span data-stu-id="70015-123">If you don't want to deal with meshes or fans, you can specify that the tessellation functions return only triangles.</span></span> <span data-ttu-id="70015-124">Toutefois, les informations de maillage et de ventilateur améliorent les performances.</span><span class="sxs-lookup"><span data-stu-id="70015-124">However, mesh and fan information improves performance.</span></span> <span data-ttu-id="70015-125">Les fonctions de pavage de polygone triangulent un polygone concave avec un ou plusieurs contourages.</span><span class="sxs-lookup"><span data-stu-id="70015-125">The polygon tessellation functions triangulate a concave polygon with one or more contours.</span></span>

<span data-ttu-id="70015-126">**Pour utiliser le pavage de polygones**</span><span class="sxs-lookup"><span data-stu-id="70015-126">**To use polygon tessellation**</span></span>

1.  <span data-ttu-id="70015-127">Créez un objet polygonalisation avec [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="70015-127">Create a tessellation object with [**gluNewTess**](glunewtess.md).</span></span>
2.  <span data-ttu-id="70015-128">Utilisez [*gluTessCallBack*](glutess.md) pour définir les fonctions de rappel que vous allez utiliser pour traiter les triangles générés par du paveur.</span><span class="sxs-lookup"><span data-stu-id="70015-128">Use [*gluTessCallBack*](glutess.md) to define callback functions you will use to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="70015-129">Avec [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)et [**gluEndPolygon**](gluendpolygon.md), spécifiez le polygone avec des trous ou le polygone concave à défaire.</span><span class="sxs-lookup"><span data-stu-id="70015-129">With [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), specify the polygon with holes or the concave polygon to be tessellated.</span></span>

    <span data-ttu-id="70015-130">Lorsque la description du polygone est terminée, la fonction de pavage appelle vos fonctions de rappel si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="70015-130">When the polygon description is complete, the tessellation facility invokes your callback functions as necessary.</span></span>

    <span data-ttu-id="70015-131">Vous pouvez détruire des objets pavage inutiles avec [**gluDeleteTess**](gludeletetess.md).</span><span class="sxs-lookup"><span data-stu-id="70015-131">You can destroy unneeded tessellation objects with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="70015-132">Pour plus d’informations sur l’enregistrement des données de pavage, consultez [utilisation des fonctions de rappel](using-callback-functions.md).</span><span class="sxs-lookup"><span data-stu-id="70015-132">For more information on saving the tessellation data, see [Using Callback Functions](using-callback-functions.md).</span></span>

 

 




