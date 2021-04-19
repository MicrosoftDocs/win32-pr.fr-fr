---
title: Portage de l’écran et des commandes de vidage de la mémoire tampon
description: OpenGL remplace toute une série de fonctions d’IRIS du GL en clair (telles que zclear, aclear, sclear, etc.) par une seule fonction, glClear. Spécifiez exactement ce que vous souhaitez effacer en transmettant des masques à glClear.
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- Le portage du GL IRIS, fonctions Clear
- Portage à partir de IRIS GL, fonctions Clear
- portage vers OpenGL à partir de IRIS GL, fonctions Clear
- Portage OpenGL à partir de IRIS GL, fonctions Clear
- fonctions Clear
- Portage des commandes d’affichage de l’écran
- Portage à partir de IRIS GL, commandes d’effacement d’écran
- portage vers OpenGL à partir de l’IRIS GL, commandes d’effacement d’écran
- Portage OpenGL à partir de IRIS GL, commandes d’effacement d’écran
- commandes d’effacement d’écran
- Portage de l’IRIS dans le GL, commandes de vidage de la mémoire tampon
- Portage à partir de IRIS GL, commandes de vidage de mémoire tampon
- portage vers OpenGL à partir de l’IRIS GL, commandes de vidage de la mémoire tampon
- Portage OpenGL à partir de IRIS GL, commandes de vidage de mémoire tampon
- commandes de vidage de la mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513477"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a><span data-ttu-id="03aa4-119">Portage de l’écran et des commandes de vidage de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="03aa4-119">Porting Screen and Buffer Clearing Commands</span></span>

<span data-ttu-id="03aa4-120">OpenGL remplace toute une série de fonctions d’IRIS du GL en **clair** (telles que **zclear**, **aclear**, **sclear**, etc.) par une seule fonction, [**glClear**](glclear.md).</span><span class="sxs-lookup"><span data-stu-id="03aa4-120">OpenGL replaces a variety of IRIS GL **clear** functions (such as **zclear**, **aclear**, **sclear**, and so on) with a single function, [**glClear**](glclear.md).</span></span> <span data-ttu-id="03aa4-121">Spécifiez exactement ce que vous souhaitez effacer en transmettant des masques à **glClear**.</span><span class="sxs-lookup"><span data-stu-id="03aa4-121">Specify exactly what you want to clear by passing masks to **glClear**.</span></span>

<span data-ttu-id="03aa4-122">Gardez les points suivants à l’esprit lors du Portage des commandes de mémoire tampon et d’écran :</span><span class="sxs-lookup"><span data-stu-id="03aa4-122">Keep the following points in mind when porting screen and buffer commands:</span></span>

-   <span data-ttu-id="03aa4-123">OpenGL gère l’effacement des couleurs séparément des couleurs de dessin, avec des appels tels que [**glClearColor**](glclearcolor.md) et [**glClearIndex**](glclearindex.md).</span><span class="sxs-lookup"><span data-stu-id="03aa4-123">OpenGL maintains clearing colors separately from drawing colors, with calls like [**glClearColor**](glclearcolor.md) and [**glClearIndex**](glclearindex.md).</span></span> <span data-ttu-id="03aa4-124">Veillez à définir la couleur d’effacement pour chaque mémoire tampon avant l’effacement.</span><span class="sxs-lookup"><span data-stu-id="03aa4-124">Be sure to set the clear color for each buffer before clearing.</span></span>
-   <span data-ttu-id="03aa4-125">Au lieu d’utiliser l’un des nombreux appels Clear nommés différemment, vous désactivez maintenant plusieurs mémoires tampons avec un appel, [**glClear**](glclear.md), par **ou** ING.</span><span class="sxs-lookup"><span data-stu-id="03aa4-125">Instead of using one of several differently named clear calls, you now clear several buffers with one call, [**glClear**](glclear.md), by **OR** ing together buffer masks.</span></span> <span data-ttu-id="03aa4-126">Par exemple, **czclear** est remplacé par :</span><span class="sxs-lookup"><span data-stu-id="03aa4-126">For example, **czclear** is replaced by:</span></span>

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   <span data-ttu-id="03aa4-127">IRIS GL fait référence au polygone stipple et à la couleur writemask.</span><span class="sxs-lookup"><span data-stu-id="03aa4-127">IRIS GL references the polygon stipple and the color writemask.</span></span> <span data-ttu-id="03aa4-128">OpenGL ignore le polygone stipple mais référence la couleur writemask.</span><span class="sxs-lookup"><span data-stu-id="03aa4-128">OpenGL ignores the polygon stipple but references the color writemask.</span></span> <span data-ttu-id="03aa4-129">(La fonction **czclear** ignore les deux polygones stipple et Color writemask.)</span><span class="sxs-lookup"><span data-stu-id="03aa4-129">(The **czclear** function ignores both the polygon stipple and the color writemask.)</span></span>

<span data-ttu-id="03aa4-130">Le tableau suivant répertorie les différentes fonctions IRIS GL Clear avec leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="03aa4-130">The following table lists the various IRIS GL clear functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="03aa4-131">Appel du GL IRIS</span><span class="sxs-lookup"><span data-stu-id="03aa4-131">IRIS GL call</span></span>         | <span data-ttu-id="03aa4-132">Appel OpenGL</span><span class="sxs-lookup"><span data-stu-id="03aa4-132">OpenGL call</span></span>                                                               | <span data-ttu-id="03aa4-133">Signification</span><span class="sxs-lookup"><span data-stu-id="03aa4-133">Meaning</span></span>                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="03aa4-134">**acbuf**(AC \_ Clear)</span><span class="sxs-lookup"><span data-stu-id="03aa4-134">**acbuf**(AC\_CLEAR)</span></span> | <span data-ttu-id="03aa4-135">**glClear**( \_ bit de tampon amort GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="03aa4-135">**glClear**( GL\_ACCUM\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="03aa4-136">Effacez la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="03aa4-136">Clear the accumulation buffer.</span></span>                    |
|                      | <span data-ttu-id="03aa4-137">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="03aa4-137">**glClearColor**</span></span>                                                          | <span data-ttu-id="03aa4-138">Définissez la couleur d’effacement RVBA.</span><span class="sxs-lookup"><span data-stu-id="03aa4-138">Set the RGBA clear color.</span></span>                         |
|                      | <span data-ttu-id="03aa4-139">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="03aa4-139">**glClearIndex**</span></span>                                                          | <span data-ttu-id="03aa4-140">Définissez l’index Clear-Color.</span><span class="sxs-lookup"><span data-stu-id="03aa4-140">Set the clear-color index.</span></span>                        |
| <span data-ttu-id="03aa4-141">**clear**</span><span class="sxs-lookup"><span data-stu-id="03aa4-141">**clear**</span></span>            | <span data-ttu-id="03aa4-142">**glClear**( \_ bits de \_ mémoire tampon de couleur GL \_ )</span><span class="sxs-lookup"><span data-stu-id="03aa4-142">**glClear**( GL\_COLOR\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="03aa4-143">Effacez la mémoire tampon de couleur.</span><span class="sxs-lookup"><span data-stu-id="03aa4-143">Clear the color buffer.</span></span>                           |
|                      | <span data-ttu-id="03aa4-144">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="03aa4-144">**glClearDepth**</span></span>                                                          | <span data-ttu-id="03aa4-145">Spécifiez la valeur Clear pour la mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="03aa4-145">Specify the clear value for the depth buffer.</span></span>     |
| <span data-ttu-id="03aa4-146">**zclear**</span><span class="sxs-lookup"><span data-stu-id="03aa4-146">**zclear**</span></span>           | <span data-ttu-id="03aa4-147">**glClear**(bits de la \_ mémoire tampon de profondeur GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="03aa4-147">**glClear**( GL\_DEPTH\_BUFFER\_BIT )</span></span>                                     | <span data-ttu-id="03aa4-148">Effacez le tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="03aa4-148">Clear the depth buffer.</span></span>                           |
| <span data-ttu-id="03aa4-149">**czclear**</span><span class="sxs-lookup"><span data-stu-id="03aa4-149">**czclear**</span></span>          | <span data-ttu-id="03aa4-150">**glClear**(bits de la mémoire tampon de la couleur GL- \_ \_ bit de \_ \| \_ mémoire tampon de profondeur GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="03aa4-150">**glClear**( GL\_COLOR\_BUFFER\_BIT \|GL\_DEPTH\_BUFFER\_BIT )</span></span><br/> | <span data-ttu-id="03aa4-151">Effacez la mémoire tampon de couleur et la mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="03aa4-151">Clear the color buffer and the depth buffer.</span></span>      |
|                      | <span data-ttu-id="03aa4-152">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="03aa4-152">**glClearAccum**</span></span>                                                          | <span data-ttu-id="03aa4-153">Spécifiez des valeurs claires pour la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="03aa4-153">Specify clear values for the accumulation buffer.</span></span> |
|                      | <span data-ttu-id="03aa4-154">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="03aa4-154">**glClearStencil**</span></span>                                                        | <span data-ttu-id="03aa4-155">Spécifiez la valeur Clear pour la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="03aa4-155">Specify the clear value for the stencil buffer.</span></span>   |
| <span data-ttu-id="03aa4-156">**sclear**</span><span class="sxs-lookup"><span data-stu-id="03aa4-156">**sclear**</span></span>           | <span data-ttu-id="03aa4-157">**glClear**(bits de tampon de stencil du GL \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="03aa4-157">**glClear**( GL\_STENCIL\_BUFFER\_BIT )</span></span>                                   | <span data-ttu-id="03aa4-158">Effacez la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="03aa4-158">Clear the stencil buffer.</span></span>                         |



 

<span data-ttu-id="03aa4-159">Lorsque votre code de la comptabilité IRIS utilise à la fois **gclear** et **sclear**, vous pouvez les combiner en un seul appel **glClear** . peut améliorer les performances de votre programme.</span><span class="sxs-lookup"><span data-stu-id="03aa4-159">When your IRIS GL code uses both **gclear** and **sclear**, you can combine them into a single **glClear** call; can improve your program's performance.</span></span>

 

 





