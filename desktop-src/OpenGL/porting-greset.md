---
title: Portage greset
description: OpenGL remplace la fonction IRIS GL, greset, par les fonctions, glPushAttrib et glPopAttrib.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- Portage du grand livre de l’IRIS, variables d’État
- Portage à partir de IRIS GL, variables d’État
- portage vers OpenGL à partir de IRIS GL, variables d’État
- Portage OpenGL à partir de IRIS GL, variables d’État
- variables d’État
- Portage de l’IRIS dans le GL, fonction greset
- Portage à partir de IRIS GL, fonction greset
- portage vers OpenGL à partir de l’IRIS GL, fonction greset
- Portage OpenGL depuis IRIS GL, fonction greset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380123"
---
# <a name="porting-greset"></a><span data-ttu-id="a83f2-112">Portage greset</span><span class="sxs-lookup"><span data-stu-id="a83f2-112">Porting greset</span></span>

<span data-ttu-id="a83f2-113">OpenGL remplace la fonction IRIS GL, **greset**, par les fonctions, [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="a83f2-113">OpenGL replaces the IRIS GL function, **greset**, with the functions, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="a83f2-114">Utilisez ces fonctions pour enregistrer et restaurer des groupes de variables d’État.</span><span class="sxs-lookup"><span data-stu-id="a83f2-114">Use these functions to save and restore groups of state variables.</span></span> <span data-ttu-id="a83f2-115">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="a83f2-115">For example,</span></span>

``` syntax
void glPushAttrib( GLbitfield mask );
```

<span data-ttu-id="a83f2-116">Cet exemple prend une opération or au niveau du bit des constantes symboliques, indiquant les groupes de variables d’État à envoyer dans une pile d’attributs.</span><span class="sxs-lookup"><span data-stu-id="a83f2-116">This example takes a bitwise OR of symbolic constants, indicating which groups of state variables to push onto an attribute stack.</span></span> <span data-ttu-id="a83f2-117">Chaque constante fait référence à un groupe de variables d’État.</span><span class="sxs-lookup"><span data-stu-id="a83f2-117">Each constant refers to a group of state variables.</span></span> <span data-ttu-id="a83f2-118">Le tableau suivant montre les groupes d’attributs avec leurs noms de constantes symboliques équivalents.</span><span class="sxs-lookup"><span data-stu-id="a83f2-118">The following table shows the attribute groups with their equivalent symbolic constant names.</span></span> <span data-ttu-id="a83f2-119">Pour obtenir la liste complète des variables d’État OpenGL associées à chaque constante, consultez [**glPushAttrib**](glpushattrib.md).</span><span class="sxs-lookup"><span data-stu-id="a83f2-119">For a complete list of the OpenGL state variables associated with each constant, see [**glPushAttrib**](glpushattrib.md).</span></span>



| <span data-ttu-id="a83f2-120">Attribut</span><span class="sxs-lookup"><span data-stu-id="a83f2-120">Attribute</span></span>                       | <span data-ttu-id="a83f2-121">Constante</span><span class="sxs-lookup"><span data-stu-id="a83f2-121">Constant</span></span>                  |
|---------------------------------|---------------------------|
| <span data-ttu-id="a83f2-122">valeur effacée de la mémoire tampon d’accumulation</span><span class="sxs-lookup"><span data-stu-id="a83f2-122">accumulation buffer clear value</span></span> | <span data-ttu-id="a83f2-123">\_bit de tampon amort \_ \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-123">GL\_ACCUM\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="a83f2-124">mémoire tampon de couleur</span><span class="sxs-lookup"><span data-stu-id="a83f2-124">color buffer</span></span>                    | <span data-ttu-id="a83f2-125">\_bit de \_ mémoire tampon de couleur GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-125">GL\_COLOR\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="a83f2-126">actuels</span><span class="sxs-lookup"><span data-stu-id="a83f2-126">current</span></span>                         | <span data-ttu-id="a83f2-127">\_bit actuel du GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-127">GL\_CURRENT\_BIT</span></span>          |
| <span data-ttu-id="a83f2-128">mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="a83f2-128">depth buffer</span></span>                    | <span data-ttu-id="a83f2-129">\_bit de \_ mémoire tampon de profondeur GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-129">GL\_DEPTH\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="a83f2-130">enable</span><span class="sxs-lookup"><span data-stu-id="a83f2-130">enable</span></span>                          | <span data-ttu-id="a83f2-131">\_bit d’activation du GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-131">GL\_ENABLE\_BIT</span></span>           |
| <span data-ttu-id="a83f2-132">évaluateurs</span><span class="sxs-lookup"><span data-stu-id="a83f2-132">evaluators</span></span>                      | <span data-ttu-id="a83f2-133">EGL \_ Val \_ bit</span><span class="sxs-lookup"><span data-stu-id="a83f2-133">EGL\_VAL\_BIT</span></span>             |
| <span data-ttu-id="a83f2-134">brouillard</span><span class="sxs-lookup"><span data-stu-id="a83f2-134">fog</span></span>                             | <span data-ttu-id="a83f2-135">\_bit de brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-135">GL\_FOG\_BIT</span></span>              |
| <span data-ttu-id="a83f2-136">Paramètre de base de la \_ liste GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-136">GL\_LIST\_BASE setting</span></span>          | <span data-ttu-id="a83f2-137">\_bit de liste GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-137">GL\_LIST\_BIT</span></span>             |
| <span data-ttu-id="a83f2-138">variables d’indicateur</span><span class="sxs-lookup"><span data-stu-id="a83f2-138">hint variables</span></span>                  | <span data-ttu-id="a83f2-139">\_bit indicateur \_ GL</span><span class="sxs-lookup"><span data-stu-id="a83f2-139">GL\_HINT\_BIT</span></span>             |
| <span data-ttu-id="a83f2-140">variables d’éclairage</span><span class="sxs-lookup"><span data-stu-id="a83f2-140">lighting variables</span></span>              | <span data-ttu-id="a83f2-141">\_bit d’éclairage GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-141">GL\_LIGHTING\_BIT</span></span>         |
| <span data-ttu-id="a83f2-142">mode dessin en courbes</span><span class="sxs-lookup"><span data-stu-id="a83f2-142">line drawing mode</span></span>               | <span data-ttu-id="a83f2-143">\_bit de ligne GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-143">GL\_LINE\_BIT</span></span>             |
| <span data-ttu-id="a83f2-144">variables en mode pixel</span><span class="sxs-lookup"><span data-stu-id="a83f2-144">pixel mode variables</span></span>            | <span data-ttu-id="a83f2-145">\_bit du \_ mode de pixel GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-145">GL\_PIXEL\_MODE\_BIT</span></span>      |
| <span data-ttu-id="a83f2-146">variables point</span><span class="sxs-lookup"><span data-stu-id="a83f2-146">point variables</span></span>                 | <span data-ttu-id="a83f2-147">\_bit de point GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-147">GL\_POINT\_BIT</span></span>            |
| <span data-ttu-id="a83f2-148">polygon</span><span class="sxs-lookup"><span data-stu-id="a83f2-148">polygon</span></span>                         | <span data-ttu-id="a83f2-149">\_bit de polygone GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-149">GL\_POLYGON\_BIT</span></span>          |
| <span data-ttu-id="a83f2-150">Polygone stipple</span><span class="sxs-lookup"><span data-stu-id="a83f2-150">polygon stipple</span></span>                 | <span data-ttu-id="a83f2-151">\_STIPPLE- \_ \_ bit de polygone de GL</span><span class="sxs-lookup"><span data-stu-id="a83f2-151">GL\_POLYGON\_STIPPLE\_BIT</span></span> |
| <span data-ttu-id="a83f2-152">ciseaux</span><span class="sxs-lookup"><span data-stu-id="a83f2-152">scissor</span></span>                         | <span data-ttu-id="a83f2-153">\_bit de ciseaux de GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-153">GL\_SCISSOR\_BIT</span></span>          |
| <span data-ttu-id="a83f2-154">tampon de stencil</span><span class="sxs-lookup"><span data-stu-id="a83f2-154">stencil buffer</span></span>                  | <span data-ttu-id="a83f2-155">\_bit de \_ tampon de stencil du GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-155">GL\_STENCIL\_BUFFER\_BIT</span></span>  |
| <span data-ttu-id="a83f2-156">texture</span><span class="sxs-lookup"><span data-stu-id="a83f2-156">texture</span></span>                         | <span data-ttu-id="a83f2-157">\_bit de texture GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-157">GL\_TEXTURE\_BIT</span></span>          |
| <span data-ttu-id="a83f2-158">transformation</span><span class="sxs-lookup"><span data-stu-id="a83f2-158">transform</span></span>                       | <span data-ttu-id="a83f2-159">\_bit de transformation GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-159">GL\_TRANSFORM\_BIT</span></span>        |
| <span data-ttu-id="a83f2-160">fenêtre d'affichage</span><span class="sxs-lookup"><span data-stu-id="a83f2-160">viewport</span></span>                        | <span data-ttu-id="a83f2-161">\_bit de fenêtre d’affichage GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-161">GL\_VIEWPORT\_BIT</span></span>         |
|                                 | <span data-ttu-id="a83f2-162">\_bits de tous les \_ attributs du GL \_</span><span class="sxs-lookup"><span data-stu-id="a83f2-162">GL\_ALL\_ATTRIB\_BITS</span></span>     |



 

<span data-ttu-id="a83f2-163">Pour restaurer les valeurs des variables d’État à celles enregistrées avec le dernier [**glPushAttrib**](glpushattrib.md), il vous suffit d’appeler [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="a83f2-163">To restore the values of the state variables to those saved with the last [**glPushAttrib**](glpushattrib.md), simply call [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="a83f2-164">Les variables que vous n’avez pas enregistrées resteront inchangées.</span><span class="sxs-lookup"><span data-stu-id="a83f2-164">The variables you didn't save will remain unchanged.</span></span> <span data-ttu-id="a83f2-165">La pile d’attributs a une profondeur finie d’au moins 16.</span><span class="sxs-lookup"><span data-stu-id="a83f2-165">The attribute stack has a finite depth of at least 16.</span></span>

 

 




