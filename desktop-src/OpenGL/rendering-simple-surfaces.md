---
title: Rendu de surfaces simples
description: La bibliothèque GLU comprend un ensemble de fonctions permettant de dessiner différentes surfaces simples (sphères, cylindres, disques et parties de disques) dans divers styles et orientations. Ces fonctions sont décrites en détail dans le manuel de référence OpenGL.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- Utilitaire OpenGL (GLU), surfaces simples
- GLU (utilitaire OpenGL), surfaces simples
- surfaces simples OpenGL
- Utilitaire OpenGL (GLU), sphères
- GLU (utilitaire OpenGL), sphères
- sphère OpenGL
- Utilitaire OpenGL (GLU), cylindres
- GLU (utilitaire OpenGL), cylindres
- cylindres OpenGL
- Utilitaire OpenGL (GLU), disques
- GLU (utilitaire OpenGL), disques
- disques OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380417"
---
# <a name="rendering-simple-surfaces"></a><span data-ttu-id="98f40-116">Rendu de surfaces simples</span><span class="sxs-lookup"><span data-stu-id="98f40-116">Rendering Simple Surfaces</span></span>

<span data-ttu-id="98f40-117">La bibliothèque GLU comprend un ensemble de fonctions permettant de dessiner différentes surfaces simples (sphères, cylindres, disques et parties de disques) dans divers styles et orientations.</span><span class="sxs-lookup"><span data-stu-id="98f40-117">The GLU library includes a set of functions for drawing various simple surfaces (spheres, cylinders, disks, and parts of disks) in a variety of styles and orientations.</span></span> <span data-ttu-id="98f40-118">Ces fonctions sont décrites en détail dans le *Manuel de référence OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="98f40-118">These functions are described in detail in the *OpenGL Reference Manual*.</span></span>

<span data-ttu-id="98f40-119">**Pour afficher des surfaces simples**</span><span class="sxs-lookup"><span data-stu-id="98f40-119">**To render simple surfaces**</span></span>

1.  <span data-ttu-id="98f40-120">Créez un objet quadric avec [**gluNewQuadric**](glunewquadric.md).</span><span class="sxs-lookup"><span data-stu-id="98f40-120">Create a quadric object with [**gluNewQuadric**](glunewquadric.md).</span></span>

    <span data-ttu-id="98f40-121">Pour supprimer cet objet une fois que vous avez fini de l’utiliser, utilisez [**gluDeleteQuadric**](gludeletequadric.md).</span><span class="sxs-lookup"><span data-stu-id="98f40-121">To destroy this object when you're finished with it, use [**gluDeleteQuadric**](gludeletequadric.md).</span></span>

2.  <span data-ttu-id="98f40-122">Spécifiez le style de rendu souhaité, comme indiqué ci-dessous, avec la fonction appropriée (sauf si vous êtes satisfait des valeurs par défaut) :</span><span class="sxs-lookup"><span data-stu-id="98f40-122">Specify the desired rendering style, as listed below, with the appropriate function (unless you're satisfied with the default values):</span></span>
    -   <span data-ttu-id="98f40-123">Indique si les normales de surface doivent être générées et, le cas échéant, s’il doit y avoir une normale par vertex ou une normale par face : [ **gluQuadricNormals**](gluquadricnormals.md)</span><span class="sxs-lookup"><span data-stu-id="98f40-123">Whether surface normals should be generated, and if so, whether there should be one normal per vertex or one normal per face: [**gluQuadricNormals**](gluquadricnormals.md)</span></span>
    -   <span data-ttu-id="98f40-124">Indique si des coordonnées de texture doivent être générées : [ **gluQuadricTexture**](gluquadrictexture.md)</span><span class="sxs-lookup"><span data-stu-id="98f40-124">Whether texture coordinates should be generated: [**gluQuadricTexture**](gluquadrictexture.md)</span></span>
    -   <span data-ttu-id="98f40-125">Le côté de la quadric doit être considéré comme extérieur et l’intérieur : [ **gluQuadricOrientation**](gluquadricorientation.md)</span><span class="sxs-lookup"><span data-stu-id="98f40-125">Which side of the quadric should be considered the outside and which the inside: [**gluQuadricOrientation**](gluquadricorientation.md)</span></span>
    -   <span data-ttu-id="98f40-126">Indique si le quadric doit être dessiné sous la forme d’un ensemble de polygones, de lignes ou de points : [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span><span class="sxs-lookup"><span data-stu-id="98f40-126">Whether the quadric should be drawn as a set of polygons, lines, or points: [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span></span>
3.  <span data-ttu-id="98f40-127">Après avoir spécifié le style de rendu, appelez la fonction de rendu pour le type souhaité d’objet quadric : [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md)ou [**gluPartialDisk**](glupartialdisk.md).</span><span class="sxs-lookup"><span data-stu-id="98f40-127">After specifying the rendering style, invoke the rendering function for the desired type of quadric object: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md), or [**gluPartialDisk**](glupartialdisk.md).</span></span>

    <span data-ttu-id="98f40-128">Si une erreur se produit pendant le rendu, la fonction de gestion des erreurs que vous avez spécifiée avec [*gluQuadricCallBack*](gluquadric.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="98f40-128">If an error occurs during rendering, the error-handling function you've specified with [*gluQuadricCallBack*](gluquadric.md) is invoked.</span></span>

<span data-ttu-id="98f40-129">Utilisez les arguments *\* RADIUS*, *Height* et similaires plutôt que la fonction [**glScale**](glscale.md) pour mettre à l’échelle les Quadrics, afin de ne pas avoir à renormaliser les normales de longueur d’unité générées.</span><span class="sxs-lookup"><span data-stu-id="98f40-129">Use the *\*Radius*, *height*, and similar arguments, rather than the [**glScale**](glscale.md) function, to scale the quadrics, so that you don't have to renormalize any unit-length normals that are generated.</span></span> <span data-ttu-id="98f40-130">Pour forcer les calculs d’éclairage à une granularité plus fine, en particulier si le matériau specularity est élevé, affectez aux *boucles* et aux arguments des *piles* des valeurs autres que 1.</span><span class="sxs-lookup"><span data-stu-id="98f40-130">To force lighting calculations at a finer granularity, especially if the material specularity is high, set the *loops* and *stacks* arguments to values other than 1.</span></span>

 

 




