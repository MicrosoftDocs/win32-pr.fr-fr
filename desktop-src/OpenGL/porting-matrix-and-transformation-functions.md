---
title: Fonctions de transformation et de matrice de Portage
description: IRIS GL et OpenGL gèrent les matrices et les transformations de la même manière.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- Portage de l’IRIS dans le GL, matrices
- Portage à partir de IRIS GL, matrices
- portage vers OpenGL à partir de IRIS GL, matrices
- Portage OpenGL à partir de IRIS GL, matrices
- matrices
- Portage de l’IRIS dans le GL, transformations
- Portage à partir de IRIS GL, transformations
- portage vers OpenGL à partir de IRIS GL, transformations
- Portage OpenGL depuis IRIS GL, transformations
- transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310549"
---
# <a name="porting-matrix-and-transformation-functions"></a><span data-ttu-id="9da84-113">Fonctions de transformation et de matrice de Portage</span><span class="sxs-lookup"><span data-stu-id="9da84-113">Porting Matrix and Transformation Functions</span></span>

<span data-ttu-id="9da84-114">IRIS GL et OpenGL gèrent les matrices et les transformations de la même manière.</span><span class="sxs-lookup"><span data-stu-id="9da84-114">IRIS GL and OpenGL handle matrices and transformations in a similar manner.</span></span> <span data-ttu-id="9da84-115">Toutefois, il existe plusieurs différences à garder à l’esprit lors du Portage de code à partir de IRIS GL :</span><span class="sxs-lookup"><span data-stu-id="9da84-115">But there are several differences to keep in mind when porting code from IRIS GL:</span></span>

-   <span data-ttu-id="9da84-116">Dans OpenGL, vous êtes toujours en mode double matrice ; Il n’existe pas de mode à matrice unique.</span><span class="sxs-lookup"><span data-stu-id="9da84-116">In OpenGL you are always in double-matrix mode; there is no single-matrix mode.</span></span>
-   <span data-ttu-id="9da84-117">Les angles sont mesurés en degrés, au lieu de dixièmes de degrés.</span><span class="sxs-lookup"><span data-stu-id="9da84-117">Angles are measured in degrees, instead of tenths of degrees.</span></span>
-   <span data-ttu-id="9da84-118">Les appels de matrice de projection, comme [**glFrustum**](glfrustum.md) et [**glOrtho**](glortho.md), s’multiplient désormais par la matrice actuelle, au lieu d’être chargées dans la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="9da84-118">Projection matrix calls, like [**glFrustum**](glfrustum.md) and [**glOrtho**](glortho.md), now multiply onto the current matrix, instead of being loaded onto the current matrix.</span></span>
-   <span data-ttu-id="9da84-119">La fonction OpenGL, [**glRotate**](glrotate.md), est très différente de la **rotation**.</span><span class="sxs-lookup"><span data-stu-id="9da84-119">The OpenGL function, [**glRotate**](glrotate.md), is very different from **rotate**.</span></span> <span data-ttu-id="9da84-120">Vous pouvez effectuer une rotation autour d’un axe arbitraire, au lieu d’être limité aux axes x, y et z.</span><span class="sxs-lookup"><span data-stu-id="9da84-120">You can rotate around any arbitrary axis, instead of being confined to the x-, y-, and z- axes.</span></span> <span data-ttu-id="9da84-121">Par exemple, vous pouvez traduire :</span><span class="sxs-lookup"><span data-stu-id="9da84-121">For example, you can translate:</span></span>

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    <span data-ttu-id="9da84-122">to:</span><span class="sxs-lookup"><span data-stu-id="9da84-122">to:</span></span>

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    <span data-ttu-id="9da84-123">Lors de la conversion de **Rotate** en **glRotate** , vous basculez vers degrés à partir de dixièmes de degrés et remplacez « z » par un vecteur pour l’axe z.</span><span class="sxs-lookup"><span data-stu-id="9da84-123">When translating from **rotate** to **glRotate** you switch to degrees from tenths of degrees and replace 'z' with a vector for the z-axis.</span></span>

-   <span data-ttu-id="9da84-124">OpenGL n’a pas d’équivalent à la fonction **polarview** .</span><span class="sxs-lookup"><span data-stu-id="9da84-124">OpenGL has no equivalent to the **polarview** function.</span></span> <span data-ttu-id="9da84-125">Vous pouvez le remplacer facilement par une traduction et trois rotations.</span><span class="sxs-lookup"><span data-stu-id="9da84-125">You can replace it easily with a translation and three rotations.</span></span> <span data-ttu-id="9da84-126">Par exemple, vous pouvez traduire :</span><span class="sxs-lookup"><span data-stu-id="9da84-126">For example, you can translate:</span></span>

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    <span data-ttu-id="9da84-127">to:</span><span class="sxs-lookup"><span data-stu-id="9da84-127">to:</span></span>

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

<span data-ttu-id="9da84-128">Le tableau suivant répertorie les fonctions de matrice OpenGL et leurs fonctions équivalentes de la comptabilité IRIS.</span><span class="sxs-lookup"><span data-stu-id="9da84-128">The following table lists the OpenGL matrix functions and their equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="9da84-129">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="9da84-129">IRIS GL function</span></span>              | <span data-ttu-id="9da84-130">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="9da84-130">OpenGL function</span></span>                                                                        | <span data-ttu-id="9da84-131">Signification</span><span class="sxs-lookup"><span data-stu-id="9da84-131">Meaning</span></span>                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da84-132">**mmode**</span><span class="sxs-lookup"><span data-stu-id="9da84-132">**mmode**</span></span>                     | [<span data-ttu-id="9da84-133">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="9da84-133">**glMatrixMode**</span></span>](glmatrixmode.md)                                                   | <span data-ttu-id="9da84-134">Définit le mode matrice actuel.</span><span class="sxs-lookup"><span data-stu-id="9da84-134">Sets current matrix mode.</span></span>                                                                                                                                                      |
|                               | [<span data-ttu-id="9da84-135">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="9da84-135">**glLoadIdentity**</span></span>](glloadidentity.md)                                               | <span data-ttu-id="9da84-136">Remplace la matrice actuelle par la matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="9da84-136">Replaces current matrix with the identity matrix.</span></span>                                                                                                                              |
| <span data-ttu-id="9da84-137">**loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="9da84-137">**loadmatrix**</span></span>                | <span data-ttu-id="9da84-138">[**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="9da84-138">[**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)</span></span><br/> | <span data-ttu-id="9da84-139">Remplace la matrice actuelle par la matrice spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9da84-139">Replaces current matrix with the specified matrix.</span></span>                                                                                                                             |
| <span data-ttu-id="9da84-140">**multmatrix**</span><span class="sxs-lookup"><span data-stu-id="9da84-140">**multmatrix**</span></span>                | <span data-ttu-id="9da84-141">[**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="9da84-141">[**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)</span></span><br/> | <span data-ttu-id="9da84-142">Multiplie la matrice actuelle par la matrice spécifiée (Notez que **multmatrix** prémultiplié).</span><span class="sxs-lookup"><span data-stu-id="9da84-142">Post-multiplies current matrix with the specified matrix (note that **multmatrix** pre-multiplied).</span></span>                                                                            |
| <span data-ttu-id="9da84-143">**mapw**, **mapw2**</span><span class="sxs-lookup"><span data-stu-id="9da84-143">**mapw**, **mapw2**</span></span>           | [<span data-ttu-id="9da84-144">**gluUnProject**</span><span class="sxs-lookup"><span data-stu-id="9da84-144">**gluUnProject**</span></span>](gluunproject.md)                                                   | <span data-ttu-id="9da84-145">Projette les coordonnées de l’espace universel dans l’espace de l’objet (voir aussi [**gluProject**](gluproject.md)).</span><span class="sxs-lookup"><span data-stu-id="9da84-145">Projects world-space coordinates to object space (see also [**gluProject**](gluproject.md)).</span></span>                                                                                  |
| <span data-ttu-id="9da84-146">**Ortho**</span><span class="sxs-lookup"><span data-stu-id="9da84-146">**ortho**</span></span>                     | [<span data-ttu-id="9da84-147">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="9da84-147">**glOrtho**</span></span>](glortho.md)                                                             | <span data-ttu-id="9da84-148">Multiplie la matrice actuelle par une matrice de projection orthographique.</span><span class="sxs-lookup"><span data-stu-id="9da84-148">Multiplies current matrix by an orthographic projection matrix.</span></span>                                                                                                                |
| <span data-ttu-id="9da84-149">**ortho2**</span><span class="sxs-lookup"><span data-stu-id="9da84-149">**ortho2**</span></span>                    | [<span data-ttu-id="9da84-150">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="9da84-150">**gluOrtho2D**</span></span>](gluortho2d.md)                                                       | <span data-ttu-id="9da84-151">Définit une matrice de projection orthographique à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="9da84-151">Defines a two-dimensional orthographic projection matrix.</span></span>                                                                                                                      |
| <span data-ttu-id="9da84-152">**perception**</span><span class="sxs-lookup"><span data-stu-id="9da84-152">**perspective**</span></span>               | [<span data-ttu-id="9da84-153">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="9da84-153">**gluPerspective**</span></span>](gluperspective.md)                                               | <span data-ttu-id="9da84-154">Définit une matrice de projection de perspective.</span><span class="sxs-lookup"><span data-stu-id="9da84-154">Defines a perspective projection matrix.</span></span>                                                                                                                                       |
| <span data-ttu-id="9da84-155">**picksize**</span><span class="sxs-lookup"><span data-stu-id="9da84-155">**picksize**</span></span>                  | [<span data-ttu-id="9da84-156">**gluPickMatrix**</span><span class="sxs-lookup"><span data-stu-id="9da84-156">**gluPickMatrix**</span></span>](glupickmatrix.md)                                                 | <span data-ttu-id="9da84-157">Définit une région de prélèvement.</span><span class="sxs-lookup"><span data-stu-id="9da84-157">Defines a picking region.</span></span>                                                                                                                                                      |
| <span data-ttu-id="9da84-158">**popmatrix**</span><span class="sxs-lookup"><span data-stu-id="9da84-158">**popmatrix**</span></span>                 | [<span data-ttu-id="9da84-159">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="9da84-159">**glPopMatrix**</span></span>](glpopmatrix.md)                                                     | <span data-ttu-id="9da84-160">Exécute un pop de la pile de matrice actuelle, en remplaçant la matrice actuelle par celle qui est située au-dessous.</span><span class="sxs-lookup"><span data-stu-id="9da84-160">Pops current matrix stack, replacing the current matrix with the one below it.</span></span>                                                                                                 |
| <span data-ttu-id="9da84-161">**pushmatrix**</span><span class="sxs-lookup"><span data-stu-id="9da84-161">**pushmatrix**</span></span>                | [<span data-ttu-id="9da84-162">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="9da84-162">**glPushMatrix**</span></span>](glpushmatrix.md)                                                   | <span data-ttu-id="9da84-163">Exécute un push de la pile de matrice actuelle d’une unité, en dupliquant la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="9da84-163">Pushes current matrix stack down by one, duplicating the current matrix.</span></span>                                                                                                       |
| <span data-ttu-id="9da84-164">**rotation**,**rot**</span><span class="sxs-lookup"><span data-stu-id="9da84-164">**rotate**,**rot**</span></span><br/> | <span data-ttu-id="9da84-165">[**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)</span><span class="sxs-lookup"><span data-stu-id="9da84-165">[**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)</span></span><br/>                 | <span data-ttu-id="9da84-166">Fait pivoter le système de coordonnées actuel d’après l’origine par rapport au point donné.</span><span class="sxs-lookup"><span data-stu-id="9da84-166">Rotates current coordinate system by the given angle about the vector from the origin through the given point.</span></span> <span data-ttu-id="9da84-167">Notez que la **rotation pivotait** uniquement sur les axes x, y et z.</span><span class="sxs-lookup"><span data-stu-id="9da84-167">Note that **rotate** rotated only about the x-, y-, and z-axes.</span></span> |
| <span data-ttu-id="9da84-168">**scale**</span><span class="sxs-lookup"><span data-stu-id="9da84-168">**scale**</span></span>                     | <span data-ttu-id="9da84-169">[**glScaled**](glscale.md),[**glScalef**](glscale.md)</span><span class="sxs-lookup"><span data-stu-id="9da84-169">[**glScaled**](glscale.md),[**glScalef**](glscale.md)</span></span><br/>                     | <span data-ttu-id="9da84-170">Multiplie la matrice actuelle par une matrice de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="9da84-170">Multiplies current matrix by a scaling matrix.</span></span>                                                                                                                                 |
| <span data-ttu-id="9da84-171">**Traduire**</span><span class="sxs-lookup"><span data-stu-id="9da84-171">**translate**</span></span>                 | <span data-ttu-id="9da84-172">[**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)</span><span class="sxs-lookup"><span data-stu-id="9da84-172">[**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)</span></span><br/>     | <span data-ttu-id="9da84-173">Déplace l’origine du système de coordonnées jusqu’au point spécifié, en multipliant la matrice actuelle par une matrice de translation.</span><span class="sxs-lookup"><span data-stu-id="9da84-173">Moves coordinate-system origin to the point specified, by multiplying the current matrix by a translation matrix.</span></span>                                                              |
| <span data-ttu-id="9da84-174">**fenetre**</span><span class="sxs-lookup"><span data-stu-id="9da84-174">**window**</span></span>                    | [<span data-ttu-id="9da84-175">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="9da84-175">**glFrustum**</span></span>](glfrustum.md)                                                         | <span data-ttu-id="9da84-176">Coordonnées données pour les plans de découpage, multiplie la matrice actuelle par une matrice de perspective.</span><span class="sxs-lookup"><span data-stu-id="9da84-176">Given coordinates for clipping planes, multiplies the current matrix by a perspective matrix.</span></span>                                                                                  |



 

<span data-ttu-id="9da84-177">OpenGL a trois modes de matrice, qui sont définis avec [**glMatrixMode**](glmatrixmode.md).</span><span class="sxs-lookup"><span data-stu-id="9da84-177">OpenGL has three matrix modes, which are set with [**glMatrixMode**](glmatrixmode.md).</span></span> <span data-ttu-id="9da84-178">Le tableau suivant répertorie les modes disponibles en tant que paramètres pour **glMatrixMode**.</span><span class="sxs-lookup"><span data-stu-id="9da84-178">The following table lists the modes available as parameters for **glMatrixMode**.</span></span>



| <span data-ttu-id="9da84-179">Mode matriciel du GL de l’IRIS</span><span class="sxs-lookup"><span data-stu-id="9da84-179">IRIS GL matrix mode</span></span> | <span data-ttu-id="9da84-180">Mode OpenGL</span><span class="sxs-lookup"><span data-stu-id="9da84-180">OpenGL mode</span></span>    | <span data-ttu-id="9da84-181">Signification</span><span class="sxs-lookup"><span data-stu-id="9da84-181">Meaning</span></span>                                  | <span data-ttu-id="9da84-182">Profondeur minimale de la pile</span><span class="sxs-lookup"><span data-stu-id="9da84-182">Min stack depth</span></span> |
|---------------------|----------------|------------------------------------------|-----------------|
| <span data-ttu-id="9da84-183">**MTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="9da84-183">**MTEXTURE**</span></span>        | <span data-ttu-id="9da84-184">\_texture GL</span><span class="sxs-lookup"><span data-stu-id="9da84-184">GL\_TEXTURE</span></span>    | <span data-ttu-id="9da84-185">Opère sur la pile de matrices de texture.</span><span class="sxs-lookup"><span data-stu-id="9da84-185">Operates on the texture matrix stack.</span></span>    | <span data-ttu-id="9da84-186">2</span><span class="sxs-lookup"><span data-stu-id="9da84-186">2</span></span>               |
| <span data-ttu-id="9da84-187">**MVIEWING**</span><span class="sxs-lookup"><span data-stu-id="9da84-187">**MVIEWING**</span></span>        | <span data-ttu-id="9da84-188">\_MODELVIEW GL</span><span class="sxs-lookup"><span data-stu-id="9da84-188">GL\_MODELVIEW</span></span>  | <span data-ttu-id="9da84-189">Opère sur la pile de matrices de la vue de modèle.</span><span class="sxs-lookup"><span data-stu-id="9da84-189">Operates on the model view matrix stack.</span></span> | <span data-ttu-id="9da84-190">32</span><span class="sxs-lookup"><span data-stu-id="9da84-190">32</span></span>              |
| <span data-ttu-id="9da84-191">**MPROJECTION**</span><span class="sxs-lookup"><span data-stu-id="9da84-191">**MPROJECTION**</span></span>     | <span data-ttu-id="9da84-192">\_projection GL</span><span class="sxs-lookup"><span data-stu-id="9da84-192">GL\_PROJECTION</span></span> | <span data-ttu-id="9da84-193">Opère sur la pile de matrice de projection.</span><span class="sxs-lookup"><span data-stu-id="9da84-193">Operates on the projection matrix stack.</span></span> | <span data-ttu-id="9da84-194">2</span><span class="sxs-lookup"><span data-stu-id="9da84-194">2</span></span>               |



 

 

 





