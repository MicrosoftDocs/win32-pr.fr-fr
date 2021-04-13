---
title: Portage des commandes de point de terminaison/fin
description: IRIS GL utilise le paradigme Begin/End mais a une fonction différente pour chaque primitive graphique.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- Le portage du GL IRIS, commandes BGN/fin
- Portage à partir de commandes IRIS GL, BGN/fin
- portage vers OpenGL à partir des commandes IRIS GL, BGN/fin
- Portage OpenGL à partir des commandes IRIS GL, BGN/fin
- fonctions de dessin, commandes BGN/fin
- commandes BGN/fin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380264"
---
# <a name="porting-bgnend-commands"></a><span data-ttu-id="8cb82-109">Portage des commandes de point de terminaison/fin</span><span class="sxs-lookup"><span data-stu-id="8cb82-109">Porting bgn/end Commands</span></span>

<span data-ttu-id="8cb82-110">IRIS GL utilise le paradigme Begin/End mais a une fonction différente pour chaque primitive graphique.</span><span class="sxs-lookup"><span data-stu-id="8cb82-110">IRIS GL uses the begin/end paradigm but has a different function for each graphics primitive.</span></span> <span data-ttu-id="8cb82-111">Par exemple, vous utilisez probablement **bgnpolygon** et **endpolygon** pour dessiner des polygones, et **bgnline** et **lignefin** pour dessiner des lignes.</span><span class="sxs-lookup"><span data-stu-id="8cb82-111">For example, you probably use **bgnpolygon** and **endpolygon** to draw polygons, and **bgnline** and **endline** to draw lines.</span></span> <span data-ttu-id="8cb82-112">Dans OpenGL, vous utilisez la [](glbegin.md)  /  structure [**glEnd**](glend.md) glBegin pour les deux.</span><span class="sxs-lookup"><span data-stu-id="8cb82-112">In OpenGL, you use the [**glBegin**](glbegin.md) / [**glEnd**](glend.md) structure for both.</span></span> <span data-ttu-id="8cb82-113">Dans OpenGL, vous dessinez la plupart des objets géométriques en encadrant une série de fonctions qui spécifient des vertex, des normales, des textures et des couleurs entre les paires d’appels **glBegin** et **glEnd** .</span><span class="sxs-lookup"><span data-stu-id="8cb82-113">In OpenGL you draw most geometric objects by enclosing a series of functions that specify vertices, normals, textures, and colors between pairs of **glBegin** and **glEnd** calls.</span></span> <span data-ttu-id="8cb82-114">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8cb82-114">For example:</span></span>

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

<span data-ttu-id="8cb82-115">La fonction **glBegin** accepte un paramètre unique qui spécifie le mode dessin, et donc la primitive.</span><span class="sxs-lookup"><span data-stu-id="8cb82-115">The **glBegin** function takes a single parameter that specifies the drawing mode, and thus the primitive.</span></span> <span data-ttu-id="8cb82-116">Voici un exemple de code OpenGL qui dessine un polygone, puis une ligne :</span><span class="sxs-lookup"><span data-stu-id="8cb82-116">Here's an OpenGL code sample that draws a polygon and then a line:</span></span>

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

<span data-ttu-id="8cb82-117">Avec OpenGL, vous dessinez différents objets géométriques en spécifiant des paramètres différents pour [**glBegin**](glbegin.md).</span><span class="sxs-lookup"><span data-stu-id="8cb82-117">With OpenGL, you draw different geometric objects by specifying different parameters for [**glBegin**](glbegin.md).</span></span> <span data-ttu-id="8cb82-118">Le tableau suivant répertorie les paramètres **GlBegin** OpenGL qui correspondent aux fonctions d’IRIS GL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="8cb82-118">The following table lists the OpenGL **glBegin** parameters that correspond to equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="8cb82-119">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="8cb82-119">IRIS GL function</span></span>  | <span data-ttu-id="8cb82-120">Valeur du mode glBegin</span><span class="sxs-lookup"><span data-stu-id="8cb82-120">Value of glBegin mode</span></span> | <span data-ttu-id="8cb82-121">Signification</span><span class="sxs-lookup"><span data-stu-id="8cb82-121">Meaning</span></span>                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb82-122">**bgnpoint**</span><span class="sxs-lookup"><span data-stu-id="8cb82-122">**bgnpoint**</span></span>      | <span data-ttu-id="8cb82-123">POINTS du GL \_</span><span class="sxs-lookup"><span data-stu-id="8cb82-123">GL\_POINTS</span></span>            | <span data-ttu-id="8cb82-124">Points individuels.</span><span class="sxs-lookup"><span data-stu-id="8cb82-124">Individual points.</span></span>                                                                       |
| <span data-ttu-id="8cb82-125">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="8cb82-125">**bgnline**</span></span>       | <span data-ttu-id="8cb82-126">\_bande de lignes GL \_</span><span class="sxs-lookup"><span data-stu-id="8cb82-126">GL\_LINE\_STRIP</span></span>       | <span data-ttu-id="8cb82-127">Série de segments de ligne connectés.</span><span class="sxs-lookup"><span data-stu-id="8cb82-127">Series of connected line segments.</span></span>                                                       |
| <span data-ttu-id="8cb82-128">**bgnclosedline**</span><span class="sxs-lookup"><span data-stu-id="8cb82-128">**bgnclosedline**</span></span> | <span data-ttu-id="8cb82-129">\_boucle de lignes GL \_</span><span class="sxs-lookup"><span data-stu-id="8cb82-129">GL\_LINE\_LOOP</span></span>        | <span data-ttu-id="8cb82-130">Série de segments de ligne connectés, avec un segment ajouté entre le premier et le dernier vertex.</span><span class="sxs-lookup"><span data-stu-id="8cb82-130">Series of connected line segments, with a segment added between first and last vertices.</span></span> |
|                   | <span data-ttu-id="8cb82-131">\_lignes GL</span><span class="sxs-lookup"><span data-stu-id="8cb82-131">GL\_LINES</span></span>             | <span data-ttu-id="8cb82-132">Paires de vertex interprétées comme des segments de ligne individuels.</span><span class="sxs-lookup"><span data-stu-id="8cb82-132">Pairs of vertices interpreted as individual line segments.</span></span>                               |
| <span data-ttu-id="8cb82-133">**bgnpolygon**</span><span class="sxs-lookup"><span data-stu-id="8cb82-133">**bgnpolygon**</span></span>    | <span data-ttu-id="8cb82-134">Polygone du GL \_</span><span class="sxs-lookup"><span data-stu-id="8cb82-134">GL\_POLYGON</span></span>           | <span data-ttu-id="8cb82-135">Limite d’un polygone convexe simple.</span><span class="sxs-lookup"><span data-stu-id="8cb82-135">Boundary of a simple convex polygon.</span></span>                                                     |
|                   | <span data-ttu-id="8cb82-136">\_TRIangles GL</span><span class="sxs-lookup"><span data-stu-id="8cb82-136">GL\_TRIANGLES</span></span>         | <span data-ttu-id="8cb82-137">Triples de vertex interprétés comme des triangles.</span><span class="sxs-lookup"><span data-stu-id="8cb82-137">Triples of vertices interpreted as triangles.</span></span>                                            |
| <span data-ttu-id="8cb82-138">**bgntmesh**</span><span class="sxs-lookup"><span data-stu-id="8cb82-138">**bgntmesh**</span></span>      | <span data-ttu-id="8cb82-139">\_bande triangulaire GL \_</span><span class="sxs-lookup"><span data-stu-id="8cb82-139">GL\_TRIANGLE\_STRIP</span></span>   | <span data-ttu-id="8cb82-140">Bandes liées de triangles.</span><span class="sxs-lookup"><span data-stu-id="8cb82-140">Linked strips of triangles.</span></span>                                                              |
|                   | <span data-ttu-id="8cb82-141">\_ventilateur à triangles GL \_</span><span class="sxs-lookup"><span data-stu-id="8cb82-141">GL\_TRIANGLE\_FAN</span></span>     | <span data-ttu-id="8cb82-142">Ventilateurs liés d’un triangle.</span><span class="sxs-lookup"><span data-stu-id="8cb82-142">Linked fans of triangles.</span></span>                                                                |
|                   | <span data-ttu-id="8cb82-143">à \_ quatre processeurs GL</span><span class="sxs-lookup"><span data-stu-id="8cb82-143">GL\_QUADS</span></span>             | <span data-ttu-id="8cb82-144">Quadruples de vertex interprétés comme quadrangulaires.</span><span class="sxs-lookup"><span data-stu-id="8cb82-144">Quadruples of vertices interpreted as quadrilaterals.</span></span>                                    |
| <span data-ttu-id="8cb82-145">**bgnqstrip**</span><span class="sxs-lookup"><span data-stu-id="8cb82-145">**bgnqstrip**</span></span>     | <span data-ttu-id="8cb82-146">à \_ quatre \_ bandes GL</span><span class="sxs-lookup"><span data-stu-id="8cb82-146">GL\_QUAD\_STRIP</span></span>       | <span data-ttu-id="8cb82-147">Bandes liées de quadrilatères.</span><span class="sxs-lookup"><span data-stu-id="8cb82-147">Linked strips of quadrilaterals.</span></span>                                                         |



 

<span data-ttu-id="8cb82-148">Pour plus d’informations sur les différences entre les maillages de triangle, les bandes et les fans, consultez [Portage des triangles](porting-triangles.md).</span><span class="sxs-lookup"><span data-stu-id="8cb82-148">For a detailed discussion of the differences between triangle meshes, strips, and fans, see [Porting Triangles](porting-triangles.md).</span></span>

<span data-ttu-id="8cb82-149">Il n’existe pas de limite au nombre de vertex que vous pouvez spécifier entre une paire [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) .</span><span class="sxs-lookup"><span data-stu-id="8cb82-149">There is no limit to the number of vertices you can specify between a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair.</span></span>

<span data-ttu-id="8cb82-150">En plus de spécifier des vertex à l’intérieur d’une paire **glBegin**  /  **glEnd** , vous pouvez spécifier une valeur normale actuelle, des coordonnées de texture actuelles et une couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="8cb82-150">In addition to specifying vertices inside a **glBegin** / **glEnd** pair, you can specify a current normal, current texture coordinates, and a current color.</span></span> <span data-ttu-id="8cb82-151">Le tableau suivant répertorie les commandes valides à l’intérieur d’une paire **glBegin**  /  **glEnd** .</span><span class="sxs-lookup"><span data-stu-id="8cb82-151">The following table lists the commands valid inside a **glBegin** / **glEnd** pair.</span></span>



| <span data-ttu-id="8cb82-152">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="8cb82-152">IRIS GL function</span></span>        | <span data-ttu-id="8cb82-153">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="8cb82-153">OpenGL function</span></span>                                                      | <span data-ttu-id="8cb82-154">Signification</span><span class="sxs-lookup"><span data-stu-id="8cb82-154">Meaning</span></span>                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="8cb82-155">**v2**, **v3**, **v4**</span><span class="sxs-lookup"><span data-stu-id="8cb82-155">**v2**, **v3**, **v4**</span></span>  | [<span data-ttu-id="8cb82-156">glVertex</span><span class="sxs-lookup"><span data-stu-id="8cb82-156">glVertex</span></span>](glvertex-functions.md)                                   | <span data-ttu-id="8cb82-157">Définit les coordonnées des sommets.</span><span class="sxs-lookup"><span data-stu-id="8cb82-157">Sets vertex coordinates.</span></span>                         |
| <span data-ttu-id="8cb82-158">**RGBColor**, **cpack**</span><span class="sxs-lookup"><span data-stu-id="8cb82-158">**RGBcolor**, **cpack**</span></span> | [<span data-ttu-id="8cb82-159">glColor</span><span class="sxs-lookup"><span data-stu-id="8cb82-159">glColor</span></span>](glcolor-functions.md)                                     | <span data-ttu-id="8cb82-160">Définit la couleur actuelle.</span><span class="sxs-lookup"><span data-stu-id="8cb82-160">Sets current color.</span></span>                              |
| <span data-ttu-id="8cb82-161">**color**</span><span class="sxs-lookup"><span data-stu-id="8cb82-161">**color**</span></span>               | [<span data-ttu-id="8cb82-162">glIndex</span><span class="sxs-lookup"><span data-stu-id="8cb82-162">glIndex</span></span>](glindex-functions.md)                                     | <span data-ttu-id="8cb82-163">Définit l’index de couleur actuel.</span><span class="sxs-lookup"><span data-stu-id="8cb82-163">Sets current color index.</span></span>                        |
| <span data-ttu-id="8cb82-164">**n3f**</span><span class="sxs-lookup"><span data-stu-id="8cb82-164">**n3f**</span></span>                 | [<span data-ttu-id="8cb82-165">glNormal</span><span class="sxs-lookup"><span data-stu-id="8cb82-165">glNormal</span></span>](glnormal-functions.md)                                   | <span data-ttu-id="8cb82-166">Définit les coordonnées du vecteur normal.</span><span class="sxs-lookup"><span data-stu-id="8cb82-166">Sets normal vector coordinates.</span></span>                  |
|                         | [<span data-ttu-id="8cb82-167">glEvalCoord</span><span class="sxs-lookup"><span data-stu-id="8cb82-167">glEvalCoord</span></span>](glevalcoord-functions.md)                             | <span data-ttu-id="8cb82-168">Évalue les mappages à un et à deux dimensions activés.</span><span class="sxs-lookup"><span data-stu-id="8cb82-168">Evaluates enabled one- and two-dimensional maps.</span></span> |
| <span data-ttu-id="8cb82-169">**callobj**</span><span class="sxs-lookup"><span data-stu-id="8cb82-169">**callobj**</span></span>             | <span data-ttu-id="8cb82-170">[**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="8cb82-170">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="8cb82-171">Exécute une ou plusieurs listes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="8cb82-171">Executes display list(s).</span></span>                        |
| <span data-ttu-id="8cb82-172">**H2**</span><span class="sxs-lookup"><span data-stu-id="8cb82-172">**t2**</span></span>                  | [<span data-ttu-id="8cb82-173">glTexCoord</span><span class="sxs-lookup"><span data-stu-id="8cb82-173">glTexCoord</span></span>](gltexcoord-functions.md)                               | <span data-ttu-id="8cb82-174">Définit les coordonnées de la texture.</span><span class="sxs-lookup"><span data-stu-id="8cb82-174">Sets texture coordinates.</span></span>                        |
|                         | [<span data-ttu-id="8cb82-175">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="8cb82-175">glEdgeFlag</span></span>](gledgeflag-functions.md)                               | <span data-ttu-id="8cb82-176">Contrôle les bords du dessin.</span><span class="sxs-lookup"><span data-stu-id="8cb82-176">Controls drawing edges.</span></span>                          |
| <span data-ttu-id="8cb82-177">**lmbind**</span><span class="sxs-lookup"><span data-stu-id="8cb82-177">**lmbind**</span></span>              | [<span data-ttu-id="8cb82-178">glMaterial</span><span class="sxs-lookup"><span data-stu-id="8cb82-178">glMaterial</span></span>](glmaterial-functions.md)                               | <span data-ttu-id="8cb82-179">Définit les propriétés de matériau.</span><span class="sxs-lookup"><span data-stu-id="8cb82-179">Sets material properties.</span></span>                        |



 

> [!Note]
>
> <span data-ttu-id="8cb82-180">Si vous utilisez une fonction OpenGL différente de celle indiquée dans le tableau précédent à l’intérieur d’une paire [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) , vous obtiendrez des résultats imprévisibles ou éventuellement une erreur.</span><span class="sxs-lookup"><span data-stu-id="8cb82-180">If you use any OpenGL function other than those listed in the preceding table inside a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair, you'll get unpredictable results, or possibly an error.</span></span>

 

 

 




