---
title: Portage de polygones et de quadrilatères
description: Gardez les points suivants à l’esprit lors du Portage de polygones et de quadrilatères
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Portage de l’IRIS dans le GL, quadrilatères
- Portage à partir de IRIS GL, quadrangulaires
- portage vers OpenGL à partir de IRIS GL, quadrangulaires
- Portage OpenGL à partir de IRIS GL, quadrangulaires
- fonctions de dessin, quadrilatères
- quadrilatères
- Portage de l’IRIS dans le GL, polygones
- Portage à partir de IRIS GL, polygones
- portage vers OpenGL à partir de IRIS GL, polygones
- Portage OpenGL à partir de IRIS GL, polygones
- fonctions de dessin, polygones
- polygones, Portage à partir de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7900b44051cab9590be11198c8b01af0b7c10244
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908457"
---
# <a name="porting-polygons-and-quadrilaterals"></a><span data-ttu-id="f6f2b-115">Portage de polygones et de quadrilatères</span><span class="sxs-lookup"><span data-stu-id="f6f2b-115">Porting Polygons and Quadrilaterals</span></span>

<span data-ttu-id="f6f2b-116">Gardez les points suivants à l’esprit lors du Portage de polygones et de quadrilatères :</span><span class="sxs-lookup"><span data-stu-id="f6f2b-116">Keep the following points in mind when porting polygons and quadrilaterals:</span></span>

-   <span data-ttu-id="f6f2b-117">Il n’existe aucun équivalent direct pour **concave**(**true**).</span><span class="sxs-lookup"><span data-stu-id="f6f2b-117">There is no direct equivalent for **concave**(**TRUE**).</span></span> <span data-ttu-id="f6f2b-118">Au lieu de cela, vous pouvez utiliser les routines de pavage dans le GLU, décrites dans [polygones le pavage](tessellating-polygons.md).</span><span class="sxs-lookup"><span data-stu-id="f6f2b-118">Instead you can use the tessellation routines in the GLU, described in [Tessellating Polygons](tessellating-polygons.md).</span></span>
-   <span data-ttu-id="f6f2b-119">Les modes de polygone sont définis différemment.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-119">Polygon modes are set differently.</span></span>
-   <span data-ttu-id="f6f2b-120">Ces fonctions de dessin Polygon n’ont pas d’équivalent direct dans OpenGL : **la famille de** routines ; famille de routines **POLF** ; **PMV**, **PDR** et **PCLOS**; **rpmv** et **rpdr**; **SPLF**; et comfermeture.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-120">These polygon drawing functions have no direct equivalents in OpenGL: the **poly** family of routines; the **polf** family of routines; **pmv**, **pdr**, and **pclos**; **rpmv** and **rpdr**; **splf**; and **spclos**.</span></span>

<span data-ttu-id="f6f2b-121">Si votre code IRIS GL utilise ces fonctions, vous devrez réécrire le code à l’aide de [**glBegin**](glbegin.md)( \_ polygone GL).</span><span class="sxs-lookup"><span data-stu-id="f6f2b-121">If your IRIS GL code uses these functions, you'll have to rewrite the code using [**glBegin**](glbegin.md)( GL\_POLYGON ).</span></span>

<span data-ttu-id="f6f2b-122">Le tableau suivant répertorie les fonctions de dessin de polygones du GL IRIS et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-122">The following table lists the IRIS GL polygon drawing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="f6f2b-123">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="f6f2b-123">IRIS GL function</span></span>         | <span data-ttu-id="f6f2b-124">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="f6f2b-124">OpenGL function</span></span>                                                    | <span data-ttu-id="f6f2b-125">Signification</span><span class="sxs-lookup"><span data-stu-id="f6f2b-125">Meaning</span></span>                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f6f2b-126">**bgnpolygonendpolygon**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-126">**bgnpolygonendpolygon**</span></span> | <span data-ttu-id="f6f2b-127">[**glBegin**](glbegin.md) ( \_ polygone GL)[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="f6f2b-127">[**glBegin**](glbegin.md) ( GL\_POLYGON )[**glEnd**](glend.md)</span></span>   | <span data-ttu-id="f6f2b-128">Les vertex définissent la limite d’un polygone convexe simple.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-128">Vertices define boundary of a simple convex polygon.</span></span>    |
|                          | <span data-ttu-id="f6f2b-129">**glBegin**(GL \_ quads)**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-129">**glBegin**( GL\_QUADS )**glEnd**</span></span><br/>                       | <span data-ttu-id="f6f2b-130">Interprète les quadruples des sommets comme des quadrilatères.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-130">Interprets quadruples of vertices as quadrilaterals.</span></span>    |
| <span data-ttu-id="f6f2b-131">**bgnqstripendqstrip**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-131">**bgnqstripendqstrip**</span></span>   | <span data-ttu-id="f6f2b-132">[**glBegin**](glbegin.md) (GL \_ Quad \_ Strip)**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-132">[**glBegin**](glbegin.md) ( GL\_QUAD\_STRIP )**glEnd**</span></span><br/> | <span data-ttu-id="f6f2b-133">Interprète les vertex comme des bandes liées de quadrilatères.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-133">Interprets vertices as linked strips of quadrilaterals.</span></span> |
|                          | [<span data-ttu-id="f6f2b-134">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="f6f2b-134">glEdgeFlag</span></span>](gledgeflag-functions.md)                             |                                                         |
| <span data-ttu-id="f6f2b-135">**en mode**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-135">**polymode**</span></span>             | [<span data-ttu-id="f6f2b-136">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-136">**glPolygonMode**</span></span>](glpolygonmode.md)                             | <span data-ttu-id="f6f2b-137">Définit le mode dessin de polygone.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-137">Sets polygon drawing mode.</span></span>                              |
| <span data-ttu-id="f6f2b-138">**rectrectf**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-138">**rectrectf**</span></span><br/> | [<span data-ttu-id="f6f2b-139">glRect</span><span class="sxs-lookup"><span data-stu-id="f6f2b-139">glRect</span></span>](glrect-functions.md)                                     | <span data-ttu-id="f6f2b-140">Dessine un rectangle.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-140">Draws a rectangle.</span></span>                                      |
| <span data-ttu-id="f6f2b-141">**sboxsboxf**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-141">**sboxsboxf**</span></span><br/> |                                                                    | <span data-ttu-id="f6f2b-142">Dessine un rectangle aligné à l’écran.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-142">Draws a screen-aligned rectangle.</span></span>                       |



 

<span data-ttu-id="f6f2b-143">??</span><span class="sxs-lookup"><span data-stu-id="f6f2b-143">??</span></span>

## <a name="porting-polygon-modes"></a><span data-ttu-id="f6f2b-144">Portage des modes polygone</span><span class="sxs-lookup"><span data-stu-id="f6f2b-144">Porting Polygon Modes</span></span>

<span data-ttu-id="f6f2b-145">La fonction OpenGL [**glPolygonMode**](glpolygonmode.md) vous permet de spécifier le côté d’un polygone (l’arrière ou l’avant) auquel le mode s’applique.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-145">The OpenGL function [**glPolygonMode**](glpolygonmode.md) lets you specify which side of a polygon (the back or the front) the mode applies to.</span></span> <span data-ttu-id="f6f2b-146">Sa syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f6f2b-146">Its syntax is:</span></span>

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

<span data-ttu-id="f6f2b-147">où visage est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="f6f2b-147">where face is one of:</span></span>



|<span data-ttu-id="f6f2b-148">Valeur GLenum</span><span class="sxs-lookup"><span data-stu-id="f6f2b-148">GLenum value</span></span>                      |  <span data-ttu-id="f6f2b-149">Signification</span><span class="sxs-lookup"><span data-stu-id="f6f2b-149">Meaning</span></span>                                                          |
|----------------------|------------------------------------------------------------|
| <span data-ttu-id="f6f2b-150">GL \_ frontal</span><span class="sxs-lookup"><span data-stu-id="f6f2b-150">GL\_FRONT</span></span>            | <span data-ttu-id="f6f2b-151">mode qui s’applique aux polygones frontaux</span><span class="sxs-lookup"><span data-stu-id="f6f2b-151">mode which applies to front-facing polygons</span></span>                |
| <span data-ttu-id="f6f2b-152">Back. du GL \_</span><span class="sxs-lookup"><span data-stu-id="f6f2b-152">GL\_BACK</span></span>             | <span data-ttu-id="f6f2b-153">mode qui s’applique aux polygones de l’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="f6f2b-153">mode which applies to back-facing polygons</span></span>                 |
| <span data-ttu-id="f6f2b-154">\_recto \_ et \_ Back GL</span><span class="sxs-lookup"><span data-stu-id="f6f2b-154">GL\_FRONT\_AND\_BACK</span></span> | <span data-ttu-id="f6f2b-155">mode qui s’applique aux polygones avant et arrière</span><span class="sxs-lookup"><span data-stu-id="f6f2b-155">mode which applies to both front- and back-facing polygons</span></span> |



 

<span data-ttu-id="f6f2b-156">Le \_ mode recto \_ et \_ verso GL est équivalent à la fonction Iris GL **polymode** .</span><span class="sxs-lookup"><span data-stu-id="f6f2b-156">The GL\_FRONT\_AND\_BACK mode is equivalent to the IRIS GL **polymode** function.</span></span> <span data-ttu-id="f6f2b-157">Le tableau suivant répertorie les modes de polygone du GL d’IRIS et leurs modes OpenGL équivalents.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-157">The following table lists IRIS GL polygon modes and their equivalent OpenGL modes.</span></span>



| <span data-ttu-id="f6f2b-158">Mode de l’IRIS du GL</span><span class="sxs-lookup"><span data-stu-id="f6f2b-158">IRIS GL mode</span></span> | <span data-ttu-id="f6f2b-159">Mode OpenGL</span><span class="sxs-lookup"><span data-stu-id="f6f2b-159">OpenGL mode</span></span> | <span data-ttu-id="f6f2b-160">Signification</span><span class="sxs-lookup"><span data-stu-id="f6f2b-160">Meaning</span></span>                                       |
|--------------|-------------|-----------------------------------------------|
| <span data-ttu-id="f6f2b-161">\_point Pym</span><span class="sxs-lookup"><span data-stu-id="f6f2b-161">PYM\_POINT</span></span>   | <span data-ttu-id="f6f2b-162">\_point GL</span><span class="sxs-lookup"><span data-stu-id="f6f2b-162">GL\_POINT</span></span>   | <span data-ttu-id="f6f2b-163">Dessine des vertex en tant que points.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-163">Draws vertices as points.</span></span>                     |
| <span data-ttu-id="f6f2b-164">\_ligne Pym</span><span class="sxs-lookup"><span data-stu-id="f6f2b-164">PYM\_LINE</span></span>    | <span data-ttu-id="f6f2b-165">\_ligne GL</span><span class="sxs-lookup"><span data-stu-id="f6f2b-165">GL\_LINE</span></span>    | <span data-ttu-id="f6f2b-166">Dessine des arêtes limites sous forme de segments de ligne.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-166">Draws boundary edges as line segments.</span></span>        |
| <span data-ttu-id="f6f2b-167">PYM \_ remplissage</span><span class="sxs-lookup"><span data-stu-id="f6f2b-167">PYM\_FILL</span></span>    | <span data-ttu-id="f6f2b-168">remplissage du GL \_</span><span class="sxs-lookup"><span data-stu-id="f6f2b-168">GL\_FILL</span></span>    | <span data-ttu-id="f6f2b-169">Dessine l’intérieur du polygone rempli.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-169">Draws polygon interior filled.</span></span>                |
| <span data-ttu-id="f6f2b-170">PYM \_ creux</span><span class="sxs-lookup"><span data-stu-id="f6f2b-170">PYM\_HOLLOW</span></span>  |             | <span data-ttu-id="f6f2b-171">Remplit uniquement les pixels intérieurs aux limites.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-171">Fills only interior pixels at the boundaries.</span></span> |



 

## <a name="porting-polygon-stipples"></a><span data-ttu-id="f6f2b-172">Portage du polygone stipples</span><span class="sxs-lookup"><span data-stu-id="f6f2b-172">Porting Polygon Stipples</span></span>

<span data-ttu-id="f6f2b-173">Lorsque vous portagez IRIS GL Polygon stipples, gardez les points suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="f6f2b-173">When porting IRIS GL polygon stipples, keep the following points in mind:</span></span>

-   <span data-ttu-id="f6f2b-174">OpenGL n’utilise pas de tables pour Polygon stipples ; un seul modèle stipple est conservé.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-174">OpenGL doesn't use tables for polygon stipples; only one stipple pattern is kept.</span></span> <span data-ttu-id="f6f2b-175">Vous pouvez utiliser des listes d’affichage pour stocker différents modèles stipple.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-175">You can use display lists to store different stipple patterns.</span></span>
-   <span data-ttu-id="f6f2b-176">La taille de l’image bitmap OpenGL Polygon stipple est toujours un modèle 32 x 32.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-176">The OpenGL polygon stipple bitmap size is always a 32x32 bit pattern.</span></span>
-   <span data-ttu-id="f6f2b-177">L’encodage stipple est affecté par [**glPixelStore**](glpixelstore-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f6f2b-177">Stipple encoding is affected by [**glPixelStore**](glpixelstore-functions.md).</span></span>

<span data-ttu-id="f6f2b-178">Pour plus d’informations sur le portage des stipples Polygon, consultez [Portage d’opérations de pixels](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="f6f2b-178">For more information on porting polygon stipples, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="f6f2b-179">Le tableau suivant répertorie les fonctions stipple et les fonctions OpenGL équivalentes de l’IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-179">The following table lists IRIS GL polygon stipple functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="f6f2b-180">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="f6f2b-180">IRIS GL function</span></span> | <span data-ttu-id="f6f2b-181">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="f6f2b-181">OpenGL function</span></span>                                    | <span data-ttu-id="f6f2b-182">Signification</span><span class="sxs-lookup"><span data-stu-id="f6f2b-182">Meaning</span></span>                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="f6f2b-183">**defpattern**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-183">**defpattern**</span></span>   | [<span data-ttu-id="f6f2b-184">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-184">**glPolygonStipple**</span></span>](glpolygonstipple.md)       | <span data-ttu-id="f6f2b-185">Définit le modèle stipple.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-185">Sets the stipple pattern.</span></span>                             |
| <span data-ttu-id="f6f2b-186">**setpattern**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-186">**setpattern**</span></span>   |                                                    | <span data-ttu-id="f6f2b-187">OpenGL conserve un seul modèle Polygon stipple.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-187">OpenGL keeps only one polygon stipple pattern.</span></span>        |
| <span data-ttu-id="f6f2b-188">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-188">**getpattern**</span></span>   | [<span data-ttu-id="f6f2b-189">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-189">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | <span data-ttu-id="f6f2b-190">Retourne la bitmap stipple (utilisée pour retourner un index).</span><span class="sxs-lookup"><span data-stu-id="f6f2b-190">Returns the stipple bitmap (used to return an index).</span></span> |



 

<span data-ttu-id="f6f2b-191">Dans OpenGL, vous activez et désactivez Polygon stippling en transmettant GL \_ Polygon \_ STIPPLE en tant que paramètre pour [**glEnable**](glenable.md) et [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="f6f2b-191">In OpenGL, you enable and disable polygon stippling by passing GL\_POLYGON\_STIPPLE as a parameter for [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="f6f2b-192">L’exemple de code OpenGL suivant illustre stippling Polygon :</span><span class="sxs-lookup"><span data-stu-id="f6f2b-192">The following OpenGL code sample demonstrates polygon stippling:</span></span>


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a><span data-ttu-id="f6f2b-193">Portage de polygones fractionnés</span><span class="sxs-lookup"><span data-stu-id="f6f2b-193">Porting Tessellated Polygons</span></span>

<span data-ttu-id="f6f2b-194">Dans IRIS GL, vous utilisez **concave**(**true**), puis **bgnpolygon** pour dessiner des polygones concave.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-194">In IRIS GL, you use **concave**(**TRUE**) and then **bgnpolygon** to draw concave polygons.</span></span> <span data-ttu-id="f6f2b-195">Le GLU OpenGL comprend des fonctions que vous pouvez utiliser pour dessiner des polygones concave.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-195">The OpenGL GLU includes functions you can use to draw concave polygons.</span></span>

<span data-ttu-id="f6f2b-196">**Pour dessiner un polygone concave avec OpenGL**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-196">**To draw a concave polygon with OpenGL**</span></span>

1.  <span data-ttu-id="f6f2b-197">Créez un objet de pavage.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-197">Create a tessellation object.</span></span>
2.  <span data-ttu-id="f6f2b-198">Définissez les rappels qui seront utilisés pour traiter les triangles générés par le du paveur.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-198">Define callbacks that will be used to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="f6f2b-199">Spécifiez le polygone concave à fractionnér.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-199">Specify the concave polygon to be tessellated.</span></span>

<span data-ttu-id="f6f2b-200">Le tableau suivant répertorie les fonctions OpenGL permettant de dessiner des polygones fractionnés.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-200">The following table lists the OpenGL functions for drawing tessellated polygons.</span></span>



| <span data-ttu-id="f6f2b-201">Fonction OpenGL GLU</span><span class="sxs-lookup"><span data-stu-id="f6f2b-201">OpenGL GLU function</span></span>                        | <span data-ttu-id="f6f2b-202">Signification</span><span class="sxs-lookup"><span data-stu-id="f6f2b-202">Meaning</span></span>                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="f6f2b-203">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-203">**gluNewTess**</span></span>](glunewtess.md)           | <span data-ttu-id="f6f2b-204">Crée un objet de pavage.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-204">Creates a new tessellation object.</span></span>                                 |
| [<span data-ttu-id="f6f2b-205">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-205">**gluDeleteTess**</span></span>](gludeletetess.md)     | <span data-ttu-id="f6f2b-206">Supprime un objet de pavage.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-206">Deletes a tessellation object.</span></span>                                     |
| [<span data-ttu-id="f6f2b-207">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="f6f2b-207">*gluTessCallback*</span></span>](glutess.md)           |                                                                    |
| [<span data-ttu-id="f6f2b-208">**gluBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-208">**gluBeginPolygon**</span></span>](glubeginpolygon.md) | <span data-ttu-id="f6f2b-209">Commence la spécification du polygone.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-209">Begins the polygon specification.</span></span>                                  |
| [<span data-ttu-id="f6f2b-210">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-210">**gluTessVertex**</span></span>](glutessvertex.md)     | <span data-ttu-id="f6f2b-211">Spécifie un sommet de polygone dans un contour.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-211">Specifies a polygon vertex in a contour.</span></span>                           |
| [<span data-ttu-id="f6f2b-212">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-212">**gluNextContour**</span></span>](glunextcontour.md)   | <span data-ttu-id="f6f2b-213">Indique que la série de vertex suivante décrit un nouveau contour.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-213">Indicates that the next series of vertices describe a new contour.</span></span> |
| [<span data-ttu-id="f6f2b-214">**gluEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="f6f2b-214">**gluEndPolygon**</span></span>](gluendpolygon.md)     | <span data-ttu-id="f6f2b-215">Met fin à la spécification Polygon.</span><span class="sxs-lookup"><span data-stu-id="f6f2b-215">Ends the polygon specification.</span></span>                                    |



 

 

 





