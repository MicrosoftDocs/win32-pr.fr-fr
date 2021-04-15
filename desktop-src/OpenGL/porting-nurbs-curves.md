---
title: Portage de courbes NURBS
description: Les fonctions OpenGL de dessin des courbes NURBS sont très similaires aux fonctions de l’IRIS dans le GL. Vous spécifiez des séquences de nœuds et des points de contrôle à l’aide d’une fonction gluNurbsCurve, qui doit être contenue dans une paire gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Portage de l’IRIS dans le GL, courbes NURBS
- Portage à partir de IRIS GL, courbes NURBS
- portage vers OpenGL à partir de IRIS GL, courbes NURBS
- Portage OpenGL à partir de IRIS GL, courbes NURBS
- Courbes NURBS
- courbes
- Portage de l’IRIS dans le GL, courbes
- Portage à partir de IRIS GL, courbes
- portage vers OpenGL à partir de IRIS GL, courbes
- Portage OpenGL à partir de IRIS GL, courbes
- NURBS (non-uniform rational B-spline)
- B-spline rationnelle non uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380118"
---
# <a name="porting-nurbs-curves"></a><span data-ttu-id="7f401-116">Portage de courbes NURBS</span><span class="sxs-lookup"><span data-stu-id="7f401-116">Porting NURBS Curves</span></span>

<span data-ttu-id="7f401-117">Les fonctions OpenGL de dessin des courbes NURBS sont très similaires aux fonctions de l’IRIS dans le GL.</span><span class="sxs-lookup"><span data-stu-id="7f401-117">The OpenGL functions for drawing NURBS curves are very similar to the IRIS GL functions.</span></span> <span data-ttu-id="7f401-118">Vous spécifiez des séquences de nœuds et des points de contrôle à l’aide d’une fonction [**gluNurbsCurve**](glunurbscurve.md) , qui doit être contenue dans une paire de [](glubegincurve.md)  /  [**gluEndCurve**](gluendcurve.md) gluBeginCurve.</span><span class="sxs-lookup"><span data-stu-id="7f401-118">You specify knot sequences and control points using a [**gluNurbsCurve**](glunurbscurve.md) function, which must be contained within a [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) pair.</span></span>

<span data-ttu-id="7f401-119">Le tableau suivant répertorie les fonctions IRIS GL permettant de dessiner des courbes NURBS et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="7f401-119">The following table lists the IRIS GL functions for drawing NURBS curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="7f401-120">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="7f401-120">IRIS GL function</span></span> | <span data-ttu-id="7f401-121">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="7f401-121">OpenGL function</span></span>                        | <span data-ttu-id="7f401-122">Signification</span><span class="sxs-lookup"><span data-stu-id="7f401-122">Meaning</span></span>                     |
|------------------|----------------------------------------|-----------------------------|
| <span data-ttu-id="7f401-123">**bgncurve**</span><span class="sxs-lookup"><span data-stu-id="7f401-123">**bgncurve**</span></span>     | [<span data-ttu-id="7f401-124">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="7f401-124">**gluBeginCurve**</span></span>](glubegincurve.md) | <span data-ttu-id="7f401-125">Commence une définition de courbe.</span><span class="sxs-lookup"><span data-stu-id="7f401-125">Begins a curve definition.</span></span>  |
| <span data-ttu-id="7f401-126">**nurbscurve**</span><span class="sxs-lookup"><span data-stu-id="7f401-126">**nurbscurve**</span></span>   | [<span data-ttu-id="7f401-127">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="7f401-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="7f401-128">Spécifie les attributs de courbe.</span><span class="sxs-lookup"><span data-stu-id="7f401-128">Specifies curve attributes.</span></span> |
| <span data-ttu-id="7f401-129">**endcurve**</span><span class="sxs-lookup"><span data-stu-id="7f401-129">**endcurve**</span></span>     | [<span data-ttu-id="7f401-130">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="7f401-130">**gluEndCurve**</span></span>](gluendcurve.md)     | <span data-ttu-id="7f401-131">Met fin à une définition de courbe.</span><span class="sxs-lookup"><span data-stu-id="7f401-131">Ends a curve definition.</span></span>    |



 

<span data-ttu-id="7f401-132">Associez la position, la texture et les coordonnées de couleur en les présentant comme un **gluNurbsCurve** distinct à l’intérieur de la paire Begin/End.</span><span class="sxs-lookup"><span data-stu-id="7f401-132">Associate position, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** inside the begin/end pair.</span></span> <span data-ttu-id="7f401-133">Vous ne pouvez pas effectuer plus d’un appel à **gluNurbsCurve** pour chaque élément de couleur, de position et de texture dans une paire **gluBeginCurve/gluEndCurve** unique.</span><span class="sxs-lookup"><span data-stu-id="7f401-133">You can make no more than one call to **gluNurbsCurve** for each piece of color, position, and texture data within a single **gluBeginCurve/gluEndCurve** pair.</span></span> <span data-ttu-id="7f401-134">Vous devez effectuer un seul appel pour décrire la position de la courbe (une description du GL \_ Map1 \_ vertex \_ 3 ou du GL \_ Map1 \_ vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="7f401-134">You must make exactly one call to describe the position of the curve (a GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4 description).</span></span> <span data-ttu-id="7f401-135">Quand vous appelez **gluEndCurve**, la courbe est fractionnée en segments de ligne, puis rendue.</span><span class="sxs-lookup"><span data-stu-id="7f401-135">When you call **gluEndCurve**, the curve is tessellated into line segments and then rendered.</span></span>

<span data-ttu-id="7f401-136">Le tableau suivant répertorie les types de courbes NURBS de l’IRIS et de l’OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7f401-136">The following table lists IRIS GL and OpenGL NURBS curve types.</span></span>



| <span data-ttu-id="7f401-137">Type de GL IRIS</span><span class="sxs-lookup"><span data-stu-id="7f401-137">IRIS GL type</span></span> | <span data-ttu-id="7f401-138">Type OpenGL</span><span class="sxs-lookup"><span data-stu-id="7f401-138">OpenGL type</span></span>                  | <span data-ttu-id="7f401-139">Signification</span><span class="sxs-lookup"><span data-stu-id="7f401-139">Meaning</span></span>                                 |
|--------------|------------------------------|-----------------------------------------|
| <span data-ttu-id="7f401-140">N \_ v3d</span><span class="sxs-lookup"><span data-stu-id="7f401-140">N\_V3D</span></span>       | <span data-ttu-id="7f401-141">Map1 du GL- \_ \_ vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="7f401-141">GL\_MAP1\_VERTEX\_3</span></span>          | <span data-ttu-id="7f401-142">Courbe polynomiale.</span><span class="sxs-lookup"><span data-stu-id="7f401-142">Polynomial curve.</span></span>                       |
| <span data-ttu-id="7f401-143">N \_ V3DR</span><span class="sxs-lookup"><span data-stu-id="7f401-143">N\_V3DR</span></span>      | <span data-ttu-id="7f401-144">Map1 du GL- \_ \_ vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="7f401-144">GL\_MAP1\_VERTEX\_4</span></span>          | <span data-ttu-id="7f401-145">Courbe rationnelle.</span><span class="sxs-lookup"><span data-stu-id="7f401-145">Rational curve.</span></span>                         |
|              | <span data-ttu-id="7f401-146">\_Repère de \_ texture \_ Map1 GL\_\*</span><span class="sxs-lookup"><span data-stu-id="7f401-146">GL\_MAP1\_TEXTURE\_COORD\_\*</span></span> | <span data-ttu-id="7f401-147">Les points de contrôle sont des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="7f401-147">Control points are texture coordinates.</span></span> |
|              | <span data-ttu-id="7f401-148">Map1 GL- \_ \_ normal</span><span class="sxs-lookup"><span data-stu-id="7f401-148">GL\_MAP1\_NORMAL</span></span>             | <span data-ttu-id="7f401-149">Les points de contrôle sont normaux.</span><span class="sxs-lookup"><span data-stu-id="7f401-149">Control points are normals.</span></span>             |



 

<span data-ttu-id="7f401-150">Pour plus d’informations sur les types d’évaluateurs disponibles, consultez [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="7f401-150">For more information on available evaluator types, see [**glMap1**](glmap1.md).</span></span>

<span data-ttu-id="7f401-151">??</span><span class="sxs-lookup"><span data-stu-id="7f401-151">??</span></span>

 

 




