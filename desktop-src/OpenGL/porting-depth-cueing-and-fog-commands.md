---
title: Cueing de profondeur de Portage et commandes de brouillard
description: Cueing de profondeur de Portage et commandes de brouillard
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- Portage du GL IRIS, profondeur cueing
- Portage à partir de IRIS GL, profondeur cueing
- portage vers OpenGL à partir de IRIS GL, Depth cueing
- Portage OpenGL à partir de IRIS GL, profondeur cueing
- Portage de l’IRIS dans le GL, brouillard
- Portage à partir de IRIS GL, brouillard
- portage vers OpenGL à partir de IRIS GL, brouillard
- Portage OpenGL depuis IRIS GL, brouillard
- profondeur cueing
- brouillard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197168"
---
# <a name="porting-depth-cueing-and-fog-commands"></a><span data-ttu-id="9f32f-113">Cueing de profondeur de Portage et commandes de brouillard</span><span class="sxs-lookup"><span data-stu-id="9f32f-113">Porting Depth Cueing and Fog Commands</span></span>

<span data-ttu-id="9f32f-114">Lorsque vous portez des cueing de profondeur et des commandes de brouillard, gardez les points suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="9f32f-114">When porting depth-cueing and fog commands, keep the following points in mind:</span></span>

-   <span data-ttu-id="9f32f-115">L’appel IRIS GL, **fogvertex**, définit un mode et les paramètres qui affectent ce mode.</span><span class="sxs-lookup"><span data-stu-id="9f32f-115">The IRIS GL call, **fogvertex**, sets a mode and the parameters affecting that mode.</span></span> <span data-ttu-id="9f32f-116">Dans OpenGL, vous appelez [**glFog**](glfog.md) une fois pour définir le mode, puis de nouveau deux fois ou plus pour définir différents paramètres.</span><span class="sxs-lookup"><span data-stu-id="9f32f-116">In OpenGL, you call [**glFog**](glfog.md) once to set the mode, and then again twice or more to set various parameters.</span></span>
-   <span data-ttu-id="9f32f-117">Dans OpenGL, cueing de profondeur n’est pas une fonctionnalité distincte.</span><span class="sxs-lookup"><span data-stu-id="9f32f-117">In OpenGL, depth cueing is not a separate feature.</span></span> <span data-ttu-id="9f32f-118">Utilisez le brouillard linéaire à la place de Depth cueing.</span><span class="sxs-lookup"><span data-stu-id="9f32f-118">Use linear fog instead of depth cueing.</span></span> <span data-ttu-id="9f32f-119">(Cette section fournit un exemple de la procédure à suivre). Les fonctions de la comptabilité IRIS suivantes n’ont pas d’équivalent OpenGL direct :</span><span class="sxs-lookup"><span data-stu-id="9f32f-119">(This section gives an example of how to do this.) The following IRIS GL functions have no direct OpenGL equivalent:</span></span>

    <span data-ttu-id="9f32f-120">**depthcue**</span><span class="sxs-lookup"><span data-stu-id="9f32f-120">**depthcue**</span></span>

    <span data-ttu-id="9f32f-121">**lRGBrange**</span><span class="sxs-lookup"><span data-stu-id="9f32f-121">**lRGBrange**</span></span>

    <span data-ttu-id="9f32f-122">**lshaderange**</span><span class="sxs-lookup"><span data-stu-id="9f32f-122">**lshaderange**</span></span>

    <span data-ttu-id="9f32f-123">**getdcm**</span><span class="sxs-lookup"><span data-stu-id="9f32f-123">**getdcm**</span></span>

-   <span data-ttu-id="9f32f-124">Pour ajuster la qualité du brouillard, utilisez [**glHint**](glhint.md)( \_ indicateur de brouillard GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="9f32f-124">To adjust fog quality, use [**glHint**](glhint.md)( GL\_FOG\_HINT ).</span></span>

<span data-ttu-id="9f32f-125">Le tableau suivant répertorie les fonctions IRIS GL pour la gestion du brouillard et de leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="9f32f-125">The following table lists the IRIS GL functions for managing fog and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="9f32f-126">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="9f32f-126">IRIS GL function</span></span>         | <span data-ttu-id="9f32f-127">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="9f32f-127">OpenGL function</span></span>                                     | <span data-ttu-id="9f32f-128">Signification</span><span class="sxs-lookup"><span data-stu-id="9f32f-128">Meaning</span></span>                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="9f32f-129">**fogvertex**</span><span class="sxs-lookup"><span data-stu-id="9f32f-129">**fogvertex**</span></span>            | [<span data-ttu-id="9f32f-130">**glFog**</span><span class="sxs-lookup"><span data-stu-id="9f32f-130">**glFog**</span></span>](glfog.md)                              | <span data-ttu-id="9f32f-131">Définit différents paramètres de brouillard.</span><span class="sxs-lookup"><span data-stu-id="9f32f-131">Sets various fog parameters.</span></span>      |
| <span data-ttu-id="9f32f-132">**fogvertex**(FG \_ )</span><span class="sxs-lookup"><span data-stu-id="9f32f-132">**fogvertex**( FG\_ON )</span></span>  | <span data-ttu-id="9f32f-133">[**glEnable**](glenable.md) ( \_ voile GL)</span><span class="sxs-lookup"><span data-stu-id="9f32f-133">[**glEnable**](glenable.md) ( GL\_FOG )</span></span>            | <span data-ttu-id="9f32f-134">Active le brouillard.</span><span class="sxs-lookup"><span data-stu-id="9f32f-134">Turns on fog.</span></span>                     |
| <span data-ttu-id="9f32f-135">**fogvertex**(FG \_ désactivé)</span><span class="sxs-lookup"><span data-stu-id="9f32f-135">**fogvertex**( FG\_OFF )</span></span> | <span data-ttu-id="9f32f-136">[**glDisable**](gldisable.md) ( \_ voile GL)</span><span class="sxs-lookup"><span data-stu-id="9f32f-136">[**glDisable**](gldisable.md) ( GL\_FOG )</span></span>          | <span data-ttu-id="9f32f-137">Désactive le brouillard.</span><span class="sxs-lookup"><span data-stu-id="9f32f-137">Turns off fog.</span></span>                    |
| <span data-ttu-id="9f32f-138">**depthcue**</span><span class="sxs-lookup"><span data-stu-id="9f32f-138">**depthcue**</span></span>             | <span data-ttu-id="9f32f-139">[**glFog**](glfog.md) (GL \_ brouillard \_ mod, GL \_ Linear)</span><span class="sxs-lookup"><span data-stu-id="9f32f-139">[**glFog**](glfog.md) ( GL\_FOG\_MOD, GL\_LINEAR )</span></span> | <span data-ttu-id="9f32f-140">Utilise le brouillard linéaire pour la profondeur cueing.</span><span class="sxs-lookup"><span data-stu-id="9f32f-140">Uses linear fog for depth cueing.</span></span> |



 

<span data-ttu-id="9f32f-141">Le tableau suivant répertorie les paramètres que vous pouvez passer à **glFog**.</span><span class="sxs-lookup"><span data-stu-id="9f32f-141">The following table lists the parameters you can pass to **glFog**.</span></span>



| <span data-ttu-id="9f32f-142">Paramètre de brouillard</span><span class="sxs-lookup"><span data-stu-id="9f32f-142">Fog parameter</span></span>    | <span data-ttu-id="9f32f-143">Signification</span><span class="sxs-lookup"><span data-stu-id="9f32f-143">Meaning</span></span>                       | <span data-ttu-id="9f32f-144">Default</span><span class="sxs-lookup"><span data-stu-id="9f32f-144">Default</span></span>                  |
|------------------|-------------------------------|--------------------------|
| <span data-ttu-id="9f32f-145">\_densité de brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="9f32f-145">GL\_FOG\_DENSITY</span></span> | <span data-ttu-id="9f32f-146">Densité de brouillard.</span><span class="sxs-lookup"><span data-stu-id="9f32f-146">Fog density.</span></span>                  | <span data-ttu-id="9f32f-147">1.0</span><span class="sxs-lookup"><span data-stu-id="9f32f-147">1.0</span></span>                      |
| <span data-ttu-id="9f32f-148">\_début du brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="9f32f-148">GL\_FOG\_START</span></span>   | <span data-ttu-id="9f32f-149">Distance proche du brouillard linéaire.</span><span class="sxs-lookup"><span data-stu-id="9f32f-149">Near distance for linear fog.</span></span> | <span data-ttu-id="9f32f-150">0.0</span><span class="sxs-lookup"><span data-stu-id="9f32f-150">0.0</span></span>                      |
| <span data-ttu-id="9f32f-151">\_fin du brouillard comptable \_</span><span class="sxs-lookup"><span data-stu-id="9f32f-151">GL\_FOG\_END</span></span>     | <span data-ttu-id="9f32f-152">Distance éloignée du brouillard linéaire.</span><span class="sxs-lookup"><span data-stu-id="9f32f-152">Far distance for linear fog.</span></span>  | <span data-ttu-id="9f32f-153">1.0</span><span class="sxs-lookup"><span data-stu-id="9f32f-153">1.0</span></span>                      |
| <span data-ttu-id="9f32f-154">\_index de brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="9f32f-154">GL\_FOG\_INDEX</span></span>   | <span data-ttu-id="9f32f-155">Index de couleur de brouillard.</span><span class="sxs-lookup"><span data-stu-id="9f32f-155">Fog color index.</span></span>              | <span data-ttu-id="9f32f-156">0.0</span><span class="sxs-lookup"><span data-stu-id="9f32f-156">0.0</span></span>                      |
| <span data-ttu-id="9f32f-157">\_couleur de brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="9f32f-157">GL\_FOG\_COLOR</span></span>   | <span data-ttu-id="9f32f-158">Couleur de brouillard RVBA.</span><span class="sxs-lookup"><span data-stu-id="9f32f-158">Fog RGBA color.</span></span>               | <span data-ttu-id="9f32f-159">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="9f32f-159">(0, 0, 0, 0)</span></span>             |
| <span data-ttu-id="9f32f-160">\_mode de brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="9f32f-160">GL\_FOG\_MODE</span></span>    | <span data-ttu-id="9f32f-161">Mode de brouillard.</span><span class="sxs-lookup"><span data-stu-id="9f32f-161">Fog mode.</span></span>                     | <span data-ttu-id="9f32f-162">Consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9f32f-162">See the following table.</span></span> |



 

<span data-ttu-id="9f32f-163">Le paramètre de densité de brouillard de OpenGL diffère de celui de l’IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="9f32f-163">The fog-density parameter of OpenGL differs from the one in IRIS GL.</span></span> <span data-ttu-id="9f32f-164">Ils sont liés comme suit :</span><span class="sxs-lookup"><span data-stu-id="9f32f-164">They are related as follows:</span></span>

-   <span data-ttu-id="9f32f-165">Si *fogMode* = EXP2</span><span class="sxs-lookup"><span data-stu-id="9f32f-165">if *fogMode* = EXP2</span></span>
     

    <span data-ttu-id="9f32f-166">*openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** (1/255)))</span><span class="sxs-lookup"><span data-stu-id="9f32f-166">*openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** ( 1 / 255 ) ))</span></span>
-   <span data-ttu-id="9f32f-167">Si *fogMode* = exp</span><span class="sxs-lookup"><span data-stu-id="9f32f-167">if *fogMode* = EXP</span></span>
     

    <span data-ttu-id="9f32f-168">*openGLfogDensity* = (*irisGLfogDensity* ) ( **log** (1/255))</span><span class="sxs-lookup"><span data-stu-id="9f32f-168">*openGLfogDensity* = (*irisGLfogDensity* ) ( **log** ( 1 / 255 ) )</span></span>

<span data-ttu-id="9f32f-169">où **sqrt** est l’opération racine carrée, **log** est le logarithme népérien, *irisGLfogDensity* est la densité de brouillard du GL d’IRIS et *openGLfogDensity* est la densité de brouillard OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9f32f-169">where **sqrt** is the square root operation, **log** is the natural logarithm, *irisGLfogDensity* is the IRIS GL fog density, and *openGLfogDensity* is the OpenGL fog density.</span></span>

<span data-ttu-id="9f32f-170">Pour basculer entre le calcul du brouillard en mode par pixel et le mode par vertex, utilisez [**glHint**](glhint.md)( \_ indicateur de brouillard GL \_ , *hintMode*).</span><span class="sxs-lookup"><span data-stu-id="9f32f-170">To switch between calculating fog in per-pixel mode and per-vertex mode, use [**glHint**](glhint.md)( GL\_FOG\_HINT, *hintMode*).</span></span> <span data-ttu-id="9f32f-171">Deux modes d’indication sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="9f32f-171">Two hint modes are available:</span></span>

-   <span data-ttu-id="9f32f-172">\_Calcul de brouillard par pixel le plus agréable</span><span class="sxs-lookup"><span data-stu-id="9f32f-172">GL\_NICEST per-pixel fog calculation</span></span>
-   <span data-ttu-id="9f32f-173">\_Calcul du brouillard par vertex le plus rapide</span><span class="sxs-lookup"><span data-stu-id="9f32f-173">GL\_FASTEST per-vertex fog calculation</span></span>

<span data-ttu-id="9f32f-174">Le tableau suivant répertorie les modes de brouillard d’IRIS GL et leurs équivalents OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9f32f-174">The following table lists the IRIS GL fog modes and their OpenGL equivalents.</span></span>



| <span data-ttu-id="9f32f-175">Mode de brouillard du GL IRIS</span><span class="sxs-lookup"><span data-stu-id="9f32f-175">IRIS GL fog mode</span></span>                       | <span data-ttu-id="9f32f-176">Mode de brouillard OpenGL</span><span class="sxs-lookup"><span data-stu-id="9f32f-176">OpenGL fog mode</span></span> | <span data-ttu-id="9f32f-177">Mode Hint</span><span class="sxs-lookup"><span data-stu-id="9f32f-177">Hint mode</span></span>                         | <span data-ttu-id="9f32f-178">Signification</span><span class="sxs-lookup"><span data-stu-id="9f32f-178">Meaning</span></span>                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| <span data-ttu-id="9f32f-179">FG \_ VTX \_ exp, FG \_ pix \_ exp</span><span class="sxs-lookup"><span data-stu-id="9f32f-179">FG\_VTX\_EXP,FG\_PIX\_EXP</span></span><br/>   | <span data-ttu-id="9f32f-180">GL \_ exp</span><span class="sxs-lookup"><span data-stu-id="9f32f-180">GL\_EXP</span></span>         | <span data-ttu-id="9f32f-181">GL \_ plus rapide, grand livre \_</span><span class="sxs-lookup"><span data-stu-id="9f32f-181">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="9f32f-182">Mode de brouillard lourd (par défaut).</span><span class="sxs-lookup"><span data-stu-id="9f32f-182">Heavy fog mode (default).</span></span>                |
| <span data-ttu-id="9f32f-183">FG \_ VTX \_ EXP2, FG \_ pix \_ EXP2</span><span class="sxs-lookup"><span data-stu-id="9f32f-183">FG\_VTX\_EXP2,FG\_PIX\_EXP2</span></span><br/> | <span data-ttu-id="9f32f-184">\_EXP2 GL</span><span class="sxs-lookup"><span data-stu-id="9f32f-184">GL\_EXP2</span></span>        | <span data-ttu-id="9f32f-185">GL \_ plus rapide, grand livre \_</span><span class="sxs-lookup"><span data-stu-id="9f32f-185">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="9f32f-186">Mode voilé.</span><span class="sxs-lookup"><span data-stu-id="9f32f-186">Haze mode.</span></span>                               |
| <span data-ttu-id="9f32f-187">FG \_ VTX \_ lin, FG \_ pix \_ lin</span><span class="sxs-lookup"><span data-stu-id="9f32f-187">FG\_VTX\_LIN,FG\_PIX\_LIN</span></span><br/>   | <span data-ttu-id="9f32f-188">linéaire du GL \_</span><span class="sxs-lookup"><span data-stu-id="9f32f-188">GL\_LINEAR</span></span>      | <span data-ttu-id="9f32f-189">GL \_ plus rapide, grand livre \_</span><span class="sxs-lookup"><span data-stu-id="9f32f-189">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="9f32f-190">Mode de brouillard linéaire.</span><span class="sxs-lookup"><span data-stu-id="9f32f-190">Linear fog mode.</span></span> <span data-ttu-id="9f32f-191">(À utiliser pour la profondeur cueing.)</span><span class="sxs-lookup"><span data-stu-id="9f32f-191">(Use for depth cueing.)</span></span> |



 

<span data-ttu-id="9f32f-192">L’exemple de code suivant illustre la profondeur cueing dans OpenGL :</span><span class="sxs-lookup"><span data-stu-id="9f32f-192">The following code example demonstrates depth cueing in OpenGL:</span></span>


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





