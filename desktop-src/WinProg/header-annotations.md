---
title: Annotations d’en-tête
description: Les annotations d’en-tête décrivent comment une fonction utilise ses paramètres et sa valeur de retour.
ms.assetid: 4f9e42b1-2fe4-4173-946e-ab1805a96b9e
keywords:
- API Windows, annotations de fichier d’en-tête
- annotations du fichier d’en-tête
- Specstrings. h
- langage d’annotation standard (SAL)
- _bcount
- _deref
- _deref_opt
- _ecount
- _full
- _in
- _inout
- _opt
- _out
- _part
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8535118383a97d6c48f19246ad24ce324e8bb528
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513733"
---
# <a name="header-annotations"></a><span data-ttu-id="c3481-117">Annotations d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c3481-117">Header Annotations</span></span>

<span data-ttu-id="c3481-118">\[Cette rubrique décrit les annotations prises en charge dans les en-têtes Windows via Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c3481-118">\[This topic describes the annotations supported in the Windows headers through Windows 7.</span></span> <span data-ttu-id="c3481-119">Si vous développez pour Windows 8, vous devez utiliser les annotations décrites dans les [Annotations SAL]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span><span class="sxs-lookup"><span data-stu-id="c3481-119">If you are developing for Windows 8, you should use the annotations described in [SAL Annotations]( /previous-versions/visualstudio/visual-studio-2013/ms182032(v=vs.120)).\]</span></span>

<span data-ttu-id="c3481-120">Les annotations d’en-tête décrivent comment une fonction utilise ses paramètres et sa valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c3481-120">Header annotations describe how a function uses its parameters and return value.</span></span> <span data-ttu-id="c3481-121">Ces annotations ont été ajoutées à de nombreux fichiers d’en-tête Windows pour vous aider à vous assurer que vous appelez correctement l’API Windows.</span><span class="sxs-lookup"><span data-stu-id="c3481-121">These annotations have been added to many of the Windows header files to help you ensure that you are calling the Windows API correctly.</span></span> <span data-ttu-id="c3481-122">Si vous activez l’analyse du code, qui est disponible à partir de Visual Studio 2005, le compilateur produira des avertissements de niveau 6000 si vous n’appelez pas ces fonctions selon l’utilisation décrite par les annotations.</span><span class="sxs-lookup"><span data-stu-id="c3481-122">If you enable code analysis, which is available starting with the Visual Studio 2005, the compiler will produce level 6000 warnings if you are not calling these functions per the usage described through the annotations.</span></span> <span data-ttu-id="c3481-123">Vous pouvez également ajouter ces annotations dans votre propre code pour vous assurer qu’elles sont appelées correctement.</span><span class="sxs-lookup"><span data-stu-id="c3481-123">You can also add these annotations in your own code to ensure that it is being called correctly.</span></span> <span data-ttu-id="c3481-124">Pour activer l’analyse du code dans Visual Studio, consultez la documentation de votre version de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c3481-124">To enable code analysis in Visual Studio, see the documentation for your version of Visual Studio.</span></span>

<span data-ttu-id="c3481-125">Ces annotations sont définies dans Specstrings. h.</span><span class="sxs-lookup"><span data-stu-id="c3481-125">These annotations are defined in Specstrings.h.</span></span> <span data-ttu-id="c3481-126">Ils reposent sur les primitives qui font partie du langage de l’annotation standard (SAL) et implémentent à l’aide de `_declspec("SAL_*")` .</span><span class="sxs-lookup"><span data-stu-id="c3481-126">They are built on primitives that are part of the Standard Annotation Language (SAL) and implemented using `_declspec("SAL_*")`.</span></span>

<span data-ttu-id="c3481-127">Il existe deux classes d’annotations : les annotations de mémoire tampon et les annotations avancées.</span><span class="sxs-lookup"><span data-stu-id="c3481-127">There are two classes of annotations: buffer annotations and advanced annotations.</span></span>

## <a name="buffer-annotations"></a><span data-ttu-id="c3481-128">Annotations de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="c3481-128">Buffer Annotations</span></span>

<span data-ttu-id="c3481-129">Les annotations de mémoire tampon décrivent comment les fonctions utilisent leurs pointeurs et peuvent être utilisées pour détecter les dépassements de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c3481-129">Buffer annotations describe how functions use their pointers and can be used to detect buffer overruns.</span></span> <span data-ttu-id="c3481-130">Chaque paramètre peut utiliser zéro ou une annotation de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c3481-130">Each parameter may use zero or one buffer annotation.</span></span> <span data-ttu-id="c3481-131">Une annotation de mémoire tampon est construite avec un trait de soulignement de début et les composants décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c3481-131">A buffer annotation is constructed with a leading underscore and the components described in the following sections.</span></span>



| <span data-ttu-id="c3481-132">buffer_size</span><span class="sxs-lookup"><span data-stu-id="c3481-132">Buffer size</span></span>                                                                                  | <span data-ttu-id="c3481-133">Description</span><span class="sxs-lookup"><span data-stu-id="c3481-133">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3481-134"><span id="_size_"></span><span id="_SIZE_"></span>(*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-134"><span id="_size_"></span><span id="_SIZE_"></span>(*size*)</span></span><br/>                        | <span data-ttu-id="c3481-135">Spécifie la taille totale de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c3481-135">Specifies the total size of the buffer.</span></span> <span data-ttu-id="c3481-136">Utilisez avec \_ bcount et \_ ecount ; n’utilisez pas with \_ part.</span><span class="sxs-lookup"><span data-stu-id="c3481-136">Use with \_bcount and \_ecount; do not use with \_part.</span></span> <span data-ttu-id="c3481-137">Cette valeur est l’espace accessible ; Il peut être inférieur à l’espace alloué.</span><span class="sxs-lookup"><span data-stu-id="c3481-137">This value is the accessible space; it may be less than the allocated space.</span></span><br/> |
| <span data-ttu-id="c3481-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-138"><span id="_size_length_"></span><span id="_SIZE_LENGTH_"></span>(*size*,*length*)</span></span><br/> | <span data-ttu-id="c3481-139">Spécifie la taille totale et la longueur initialisée de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c3481-139">Specifies the total size and initialized length of the buffer.</span></span> <span data-ttu-id="c3481-140">Utilisez avec la partie \_ bcount \_ et \_ ecount \_ .</span><span class="sxs-lookup"><span data-stu-id="c3481-140">Use with \_bcount\_part and \_ecount\_part.</span></span> <span data-ttu-id="c3481-141">La taille totale peut être inférieure à l’espace alloué.</span><span class="sxs-lookup"><span data-stu-id="c3481-141">The total size may be less than the allocated space.</span></span><br/>              |



 



| <span data-ttu-id="c3481-142">Unités de taille de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="c3481-142">Buffer size units</span></span>                                                       | <span data-ttu-id="c3481-143">Description</span><span class="sxs-lookup"><span data-stu-id="c3481-143">Description</span></span>                                |
|-------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="c3481-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span><span class="sxs-lookup"><span data-stu-id="c3481-144"><span id="_bcount"></span><span id="_BCOUNT"></span>\_bcount</span></span><br/> | <span data-ttu-id="c3481-145">La taille de la mémoire tampon est en octets.</span><span class="sxs-lookup"><span data-stu-id="c3481-145">The buffer size is in bytes.</span></span><br/>    |
| <span data-ttu-id="c3481-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span><span class="sxs-lookup"><span data-stu-id="c3481-146"><span id="_ecount"></span><span id="_ECOUNT"></span>\_ecount</span></span><br/> | <span data-ttu-id="c3481-147">La taille de la mémoire tampon est dans les éléments.</span><span class="sxs-lookup"><span data-stu-id="c3481-147">The buffer size is in elements.</span></span><br/> |



 



| <span data-ttu-id="c3481-148">Sens</span><span class="sxs-lookup"><span data-stu-id="c3481-148">Direction</span></span>                                                            | <span data-ttu-id="c3481-149">Description</span><span class="sxs-lookup"><span data-stu-id="c3481-149">Description</span></span>                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3481-150"><span id="_in"></span><span id="_IN"></span>\_dans</span><span class="sxs-lookup"><span data-stu-id="c3481-150"><span id="_in"></span><span id="_IN"></span>\_in</span></span><br/>          | <span data-ttu-id="c3481-151">La fonction lit à partir de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c3481-151">The function reads from the buffer.</span></span> <span data-ttu-id="c3481-152">L’appelant fournit la mémoire tampon et l’initialise.</span><span class="sxs-lookup"><span data-stu-id="c3481-152">The caller provides the buffer and initializes it.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="c3481-153"><span id="_inout"></span><span id="_INOUT"></span>\_INOUT</span><span class="sxs-lookup"><span data-stu-id="c3481-153"><span id="_inout"></span><span id="_INOUT"></span>\_inout</span></span><br/> | <span data-ttu-id="c3481-154">La fonction lit et écrit dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c3481-154">The function both reads from and writes to buffer.</span></span> <span data-ttu-id="c3481-155">L’appelant fournit la mémoire tampon et l’initialise.</span><span class="sxs-lookup"><span data-stu-id="c3481-155">The caller provides the buffer and initializes it.</span></span> <span data-ttu-id="c3481-156">S’il est utilisé avec \_ Deref, la mémoire tampon peut être réallouée par la fonction.</span><span class="sxs-lookup"><span data-stu-id="c3481-156">If used with \_deref, the buffer may be reallocated by the function.</span></span><br/>                                      |
| <span data-ttu-id="c3481-157"><span id="_out"></span><span id="_OUT"></span>\_à</span><span class="sxs-lookup"><span data-stu-id="c3481-157"><span id="_out"></span><span id="_OUT"></span>\_out</span></span><br/>       | <span data-ttu-id="c3481-158">La fonction écrit dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c3481-158">The function writes to the buffer.</span></span> <span data-ttu-id="c3481-159">S’il est utilisé sur la valeur de retour ou avec \_ Deref, la fonction fournit la mémoire tampon et l’initialise.</span><span class="sxs-lookup"><span data-stu-id="c3481-159">If used on the return value or with \_deref, the function provides the buffer and initializes it.</span></span> <span data-ttu-id="c3481-160">Dans le cas contraire, l’appelant fournit la mémoire tampon et la fonction l’initialise.</span><span class="sxs-lookup"><span data-stu-id="c3481-160">Otherwise, the caller provides the buffer and the function initializes it.</span></span><br/> |



 



| <span data-ttu-id="c3481-161">Adressage indirect</span><span class="sxs-lookup"><span data-stu-id="c3481-161">Indirection</span></span>                                                                       | <span data-ttu-id="c3481-162">Description</span><span class="sxs-lookup"><span data-stu-id="c3481-162">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3481-163"><span id="_deref"></span><span id="_DEREF"></span>\_Deref</span><span class="sxs-lookup"><span data-stu-id="c3481-163"><span id="_deref"></span><span id="_DEREF"></span>\_deref</span></span><br/>              | <span data-ttu-id="c3481-164">Déréférencez le paramètre pour obtenir le pointeur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c3481-164">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="c3481-165">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="c3481-165">This parameter may not be **NULL**.</span></span><br/> |
| <span data-ttu-id="c3481-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_option \_ Deref</span><span class="sxs-lookup"><span data-stu-id="c3481-166"><span id="_deref_opt"></span><span id="_DEREF_OPT"></span>\_deref\_opt</span></span><br/> | <span data-ttu-id="c3481-167">Déréférencez le paramètre pour obtenir le pointeur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c3481-167">Dereference the parameter to obtain the buffer pointer.</span></span> <span data-ttu-id="c3481-168">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3481-168">This parameter can be **NULL**.</span></span><br/>     |



 



| <span data-ttu-id="c3481-169">Initialisation</span><span class="sxs-lookup"><span data-stu-id="c3481-169">Initialization</span></span>                                                    | <span data-ttu-id="c3481-170">Description</span><span class="sxs-lookup"><span data-stu-id="c3481-170">Description</span></span>                                                                                                              |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3481-171"><span id="_full"></span><span id="_FULL"></span>\_sauvegarde</span><span class="sxs-lookup"><span data-stu-id="c3481-171"><span id="_full"></span><span id="_FULL"></span>\_full</span></span><br/> | <span data-ttu-id="c3481-172">La fonction initialise la mémoire tampon entière.</span><span class="sxs-lookup"><span data-stu-id="c3481-172">The function initializes the entire buffer.</span></span> <span data-ttu-id="c3481-173">À utiliser uniquement avec les mémoires tampons de sortie.</span><span class="sxs-lookup"><span data-stu-id="c3481-173">Use only with output buffers.</span></span><br/>                                     |
| <span data-ttu-id="c3481-174"><span id="_part"></span><span id="_PART"></span>\_étape</span><span class="sxs-lookup"><span data-stu-id="c3481-174"><span id="_part"></span><span id="_PART"></span>\_part</span></span><br/> | <span data-ttu-id="c3481-175">La fonction Initialise une partie de la mémoire tampon et indique explicitement le volume.</span><span class="sxs-lookup"><span data-stu-id="c3481-175">The function initializes part of the buffer, and explicitly indicates how much.</span></span> <span data-ttu-id="c3481-176">À utiliser uniquement avec les mémoires tampons de sortie.</span><span class="sxs-lookup"><span data-stu-id="c3481-176">Use only with output buffers.</span></span><br/> |



 



| <span data-ttu-id="c3481-177">Mémoire tampon obligatoire ou facultative</span><span class="sxs-lookup"><span data-stu-id="c3481-177">Required or optional buffer</span></span>                                    | <span data-ttu-id="c3481-178">Description</span><span class="sxs-lookup"><span data-stu-id="c3481-178">Description</span></span>                                |
|----------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="c3481-179"><span id="_opt"></span><span id="_OPT"></span>\_possibilité</span><span class="sxs-lookup"><span data-stu-id="c3481-179"><span id="_opt"></span><span id="_OPT"></span>\_opt</span></span><br/> | <span data-ttu-id="c3481-180">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3481-180">This parameter can be **NULL**.</span></span><br/> |



 

<span data-ttu-id="c3481-181">L’exemple suivant montre les annotations pour la fonction **GetModuleFileName** .</span><span class="sxs-lookup"><span data-stu-id="c3481-181">The following example shows the annotations for the **GetModuleFileName** function.</span></span> <span data-ttu-id="c3481-182">Le paramètre *HMODULE* est un paramètre d’entrée facultatif.</span><span class="sxs-lookup"><span data-stu-id="c3481-182">The *hModule* parameter is an optional input parameter .</span></span> <span data-ttu-id="c3481-183">Le paramètre *lpFilename* est un paramètre de sortie ; sa taille en caractères est spécifiée par le paramètre *nSize* et sa longueur comprend le caractère de fin **null**.</span><span class="sxs-lookup"><span data-stu-id="c3481-183">The *lpFilename* parameter is an output parameter; its size in characters is specified by the *nSize* parameter and its length includes the **null**-terminating character.</span></span> <span data-ttu-id="c3481-184">Le paramètre *nSize* est un paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c3481-184">The *nSize* parameter is an input parameter.</span></span>


```C++
DWORD
WINAPI
GetModuleFileName(
    __in_opt HMODULE hModule,
    __out_ecount_part(nSize, return + 1) LPTSTR lpFilename,
    __in DWORD nSize
    );
```



<span data-ttu-id="c3481-185">Voici les annotations définies dans Specstrings. h.</span><span class="sxs-lookup"><span data-stu-id="c3481-185">The following are the annotations defined in Specstrings.h.</span></span> <span data-ttu-id="c3481-186">Utilisez les informations des tableaux ci-dessus pour interpréter leur signification.</span><span class="sxs-lookup"><span data-stu-id="c3481-186">Use the information in the tables above to interpret their meaning.</span></span>

<span data-ttu-id="c3481-187">__bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-187">__bcount(*size*)</span></span>  
<span data-ttu-id="c3481-188">__bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-188">__bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-189">__deref_bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-189">__deref_bcount(*size*)</span></span>  
<span data-ttu-id="c3481-190">__deref_bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-190">__deref_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-191">__deref_ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-191">__deref_ecount(*size*)</span></span>  
<span data-ttu-id="c3481-192">__deref_ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-192">__deref_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-193">__deref_in</span><span class="sxs-lookup"><span data-stu-id="c3481-193">__deref_in</span></span>  
<span data-ttu-id="c3481-194">__deref_in_bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-194">__deref_in_bcount(*size*)</span></span>  
<span data-ttu-id="c3481-195">__deref_in_bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-195">__deref_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-196">__deref_in_ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-196">__deref_in_ecount(*size*)</span></span>  
<span data-ttu-id="c3481-197">__deref_in_ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-197">__deref_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-198">__deref_in_opt</span><span class="sxs-lookup"><span data-stu-id="c3481-198">__deref_in_opt</span></span>  
<span data-ttu-id="c3481-199">__deref_inout</span><span class="sxs-lookup"><span data-stu-id="c3481-199">__deref_inout</span></span>  
<span data-ttu-id="c3481-200">__deref_inout_bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-200">__deref_inout_bcount(*size*)</span></span>  
<span data-ttu-id="c3481-201">__deref_inout_bcount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-201">__deref_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="c3481-202">__deref_inout_bcount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-202">__deref_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-203">__deref_inout_bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-203">__deref_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-204">__deref_inout_bcount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-204">__deref_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-205">__deref_inout_bcount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-205">__deref_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-206">__deref_inout_ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-206">__deref_inout_ecount(*size*)</span></span>  
<span data-ttu-id="c3481-207">__deref_inout_ecount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-207">__deref_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="c3481-208">__deref_inout_ecount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-208">__deref_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-209">__deref_inout_ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-209">__deref_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-210">__deref_inout_ecount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-210">__deref_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-211">__deref_inout_ecount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-211">__deref_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-212">__deref_inout_opt</span><span class="sxs-lookup"><span data-stu-id="c3481-212">__deref_inout_opt</span></span>  
<span data-ttu-id="c3481-213">__deref_opt_bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-213">__deref_opt_bcount(*size*)</span></span>  
<span data-ttu-id="c3481-214">__deref_opt_bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-214">__deref_opt_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-215">__deref_opt_ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-215">__deref_opt_ecount(*size*)</span></span>  
<span data-ttu-id="c3481-216">__deref_opt_ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-216">__deref_opt_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-217">__deref_opt_in</span><span class="sxs-lookup"><span data-stu-id="c3481-217">__deref_opt_in</span></span>  
<span data-ttu-id="c3481-218">__deref_opt_in_bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-218">__deref_opt_in_bcount(*size*)</span></span>  
<span data-ttu-id="c3481-219">__deref_opt_in_bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-219">__deref_opt_in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-220">__deref_opt_in_ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-220">__deref_opt_in_ecount(*size*)</span></span>  
<span data-ttu-id="c3481-221">__deref_opt_in_ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-221">__deref_opt_in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-222">__deref_opt_in_opt</span><span class="sxs-lookup"><span data-stu-id="c3481-222">__deref_opt_in_opt</span></span>  
<span data-ttu-id="c3481-223">__deref_opt_inout</span><span class="sxs-lookup"><span data-stu-id="c3481-223">__deref_opt_inout</span></span>  
<span data-ttu-id="c3481-224">__deref_opt_inout_bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-224">__deref_opt_inout_bcount(*size*)</span></span>  
<span data-ttu-id="c3481-225">__deref_opt_inout_bcount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-225">__deref_opt_inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="c3481-226">__deref_opt_inout_bcount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-226">__deref_opt_inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-227">__deref_opt_inout_bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-227">__deref_opt_inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-228">__deref_opt_inout_bcount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-228">__deref_opt_inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-229">__deref_opt_inout_bcount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-229">__deref_opt_inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-230">__deref_opt_inout_ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-230">__deref_opt_inout_ecount(*size*)</span></span>  
<span data-ttu-id="c3481-231">__deref_opt_inout_ecount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-231">__deref_opt_inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="c3481-232">__deref_opt_inout_ecount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-232">__deref_opt_inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-233">__deref_opt_inout_ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-233">__deref_opt_inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-234">__deref_opt_inout_ecount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-234">__deref_opt_inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-235">__deref_opt_inout_ecount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-235">__deref_opt_inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-236">__deref_opt_inout_opt</span><span class="sxs-lookup"><span data-stu-id="c3481-236">__deref_opt_inout_opt</span></span>  
<span data-ttu-id="c3481-237">__deref_opt_out</span><span class="sxs-lookup"><span data-stu-id="c3481-237">__deref_opt_out</span></span>  
<span data-ttu-id="c3481-238">__deref_opt_out_bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-238">__deref_opt_out_bcount(*size*)</span></span>  
<span data-ttu-id="c3481-239">__deref_opt_out_bcount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-239">__deref_opt_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="c3481-240">__deref_opt_out_bcount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-240">__deref_opt_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-241">__deref_opt_out_bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-241">__deref_opt_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-242">__deref_opt_out_bcount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-242">__deref_opt_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-243">__deref_opt_out_bcount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-243">__deref_opt_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-244">__deref_opt_out_ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-244">__deref_opt_out_ecount(*size*)</span></span>  
<span data-ttu-id="c3481-245">__deref_opt_out_ecount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-245">__deref_opt_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="c3481-246">__deref_opt_out_ecount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-246">__deref_opt_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-247">__deref_opt_out_ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-247">__deref_opt_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-248">__deref_opt_out_ecount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-248">__deref_opt_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-249">__deref_opt_out_ecount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-249">__deref_opt_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-250">__deref_opt_out_opt</span><span class="sxs-lookup"><span data-stu-id="c3481-250">__deref_opt_out_opt</span></span>  
<span data-ttu-id="c3481-251">__deref_out</span><span class="sxs-lookup"><span data-stu-id="c3481-251">__deref_out</span></span>  
<span data-ttu-id="c3481-252">__deref_out_bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-252">__deref_out_bcount(*size*)</span></span>  
<span data-ttu-id="c3481-253">__deref_out_bcount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-253">__deref_out_bcount_full(*size*)</span></span>  
<span data-ttu-id="c3481-254">__deref_out_bcount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-254">__deref_out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-255">__deref_out_bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-255">__deref_out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-256">__deref_out_bcount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-256">__deref_out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-257">__deref_out_bcount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-257">__deref_out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-258">__deref_out_ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-258">__deref_out_ecount(*size*)</span></span>  
<span data-ttu-id="c3481-259">__deref_out_ecount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-259">__deref_out_ecount_full(*size*)</span></span>  
<span data-ttu-id="c3481-260">__deref_out_ecount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-260">__deref_out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-261">__deref_out_ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-261">__deref_out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-262">__deref_out_ecount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-262">__deref_out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-263">__deref_out_ecount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-263">__deref_out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-264">__deref_out_opt</span><span class="sxs-lookup"><span data-stu-id="c3481-264">__deref_out_opt</span></span>  
<span data-ttu-id="c3481-265">__ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-265">__ecount(*size*)</span></span>  
<span data-ttu-id="c3481-266">__ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-266">__ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-267">__in</span><span class="sxs-lookup"><span data-stu-id="c3481-267">__in</span></span>  
<span data-ttu-id="c3481-268">__in_bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-268">__in_bcount(*size*)</span></span>  
<span data-ttu-id="c3481-269">__in_bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-269">__in_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-270">__in_ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-270">__in_ecount(*size*)</span></span>  
<span data-ttu-id="c3481-271">__in_ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-271">__in_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-272">__in_opt</span><span class="sxs-lookup"><span data-stu-id="c3481-272">__in_opt</span></span>  
<span data-ttu-id="c3481-273">__inout</span><span class="sxs-lookup"><span data-stu-id="c3481-273">__inout</span></span>  
<span data-ttu-id="c3481-274">__inout_bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-274">__inout_bcount(*size*)</span></span>  
<span data-ttu-id="c3481-275">__inout_bcount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-275">__inout_bcount_full(*size*)</span></span>  
<span data-ttu-id="c3481-276">__inout_bcount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-276">__inout_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-277">__inout_bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-277">__inout_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-278">__inout_bcount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-278">__inout_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-279">__inout_bcount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-279">__inout_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-280">__inout_ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-280">__inout_ecount(*size*)</span></span>  
<span data-ttu-id="c3481-281">__inout_ecount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-281">__inout_ecount_full(*size*)</span></span>  
<span data-ttu-id="c3481-282">__inout_ecount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-282">__inout_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-283">__inout_ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-283">__inout_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-284">__inout_ecount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-284">__inout_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-285">__inout_ecount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-285">__inout_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-286">__inout_opt</span><span class="sxs-lookup"><span data-stu-id="c3481-286">__inout_opt</span></span>  
<span data-ttu-id="c3481-287">__out</span><span class="sxs-lookup"><span data-stu-id="c3481-287">__out</span></span>  
<span data-ttu-id="c3481-288">__out_bcount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-288">__out_bcount(*size*)</span></span>  
<span data-ttu-id="c3481-289">__out_bcount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-289">__out_bcount_full(*size*)</span></span>  
<span data-ttu-id="c3481-290">__out_bcount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-290">__out_bcount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-291">__out_bcount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-291">__out_bcount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-292">__out_bcount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-292">__out_bcount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-293">__out_bcount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-293">__out_bcount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-294">__out_ecount (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-294">__out_ecount(*size*)</span></span>  
<span data-ttu-id="c3481-295">__out_ecount_full (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-295">__out_ecount_full(*size*)</span></span>  
<span data-ttu-id="c3481-296">__out_ecount_full_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-296">__out_ecount_full_opt(*size*)</span></span>  
<span data-ttu-id="c3481-297">__out_ecount_opt (*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-297">__out_ecount_opt(*size*)</span></span>  
<span data-ttu-id="c3481-298">__out_ecount_part (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-298">__out_ecount_part(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-299">__out_ecount_part_opt (*taille*,*longueur*)</span><span class="sxs-lookup"><span data-stu-id="c3481-299">__out_ecount_part_opt(*size*,*length*)</span></span>  
<span data-ttu-id="c3481-300">__out_opt</span><span class="sxs-lookup"><span data-stu-id="c3481-300">__out_opt</span></span>  

## <a name="advanced-annotations"></a><span data-ttu-id="c3481-301">Annotations avancées</span><span class="sxs-lookup"><span data-stu-id="c3481-301">Advanced Annotations</span></span>

<span data-ttu-id="c3481-302">Les annotations avancées fournissent des informations supplémentaires sur le paramètre ou la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c3481-302">Advanced annotations provide additional information about the parameter or return value.</span></span> <span data-ttu-id="c3481-303">Chaque paramètre ou valeur de retour peut utiliser zéro ou une annotation avancée.</span><span class="sxs-lookup"><span data-stu-id="c3481-303">Each parameter or return value may use zero or one advanced annotation.</span></span>



| <span data-ttu-id="c3481-304">Annotation</span><span class="sxs-lookup"><span data-stu-id="c3481-304">Annotation</span></span>                                                                                                                                               | <span data-ttu-id="c3481-305">Description</span><span class="sxs-lookup"><span data-stu-id="c3481-305">Description</span></span>                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3481-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn (*ressource*)</span><span class="sxs-lookup"><span data-stu-id="c3481-306"><span id="__blocksOn_resource_"></span><span id="__blockson_resource_"></span><span id="__BLOCKSON_RESOURCE_"></span>\_\_blocksOn(*resource*)</span></span><br/> | <span data-ttu-id="c3481-307">Les fonctions se bloquent sur la ressource spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c3481-307">The functions blocks on the specified resource.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="c3481-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_rappel</span><span class="sxs-lookup"><span data-stu-id="c3481-308"><span id="__callback"></span><span id="__CALLBACK"></span>\_\_callback</span></span><br/>                                                                        | <span data-ttu-id="c3481-309">La fonction peut être utilisée comme pointeur de fonction.</span><span class="sxs-lookup"><span data-stu-id="c3481-309">The function can be used as a function pointer.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="c3481-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span><span class="sxs-lookup"><span data-stu-id="c3481-310"><span id="__checkReturn"></span><span id="__checkreturn"></span><span id="__CHECKRETURN"></span>\_\_checkReturn</span></span><br/>                               | <span data-ttu-id="c3481-311">Les appelants doivent vérifier la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="c3481-311">Callers must check the return value.</span></span><br/>                                                                                                                                                                                                                                 |
| <span data-ttu-id="c3481-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_chaîne de format \_</span><span class="sxs-lookup"><span data-stu-id="c3481-312"><span id="__format_string"></span><span id="__FORMAT_STRING"></span>\_\_format\_string</span></span><br/>                                                        | <span data-ttu-id="c3481-313">Le paramètre est une chaîne qui contient des marqueurs% de style printf.</span><span class="sxs-lookup"><span data-stu-id="c3481-313">The parameter is a string that contains printf-style % markers.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="c3481-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_dans \_ awcount (*expr*,*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-314"><span id="__in_awcount_expr_size_"></span><span id="__IN_AWCOUNT_EXPR_SIZE_"></span>\_\_in\_awcount(*expr*,*size*)</span></span><br/>                            | <span data-ttu-id="c3481-315">Si l’expression a la valeur true à la sortie, la taille de la mémoire tampon d’entrée est spécifiée en octets.</span><span class="sxs-lookup"><span data-stu-id="c3481-315">If the expression is true at exit, the size of the input buffer is specified in bytes.</span></span> <span data-ttu-id="c3481-316">Si l’expression a la valeur false, la taille est spécifiée dans les éléments.</span><span class="sxs-lookup"><span data-stu-id="c3481-316">If the expression is false, the size is specified in elements.</span></span><br/>                                                                                                                |
| <span data-ttu-id="c3481-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span><span class="sxs-lookup"><span data-stu-id="c3481-317"><span id="__nullnullterminated"></span><span id="__NULLNULLTERMINATED"></span>\_\_nullnullterminated</span></span><br/>                                          | <span data-ttu-id="c3481-318">La mémoire tampon peut être accessible jusqu’à la première séquence de deux caractères ou pointeurs **null** , y compris.</span><span class="sxs-lookup"><span data-stu-id="c3481-318">The buffer may be accessed up to and including the first sequence of two **null** characters or pointers.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="c3481-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_NullTerminated</span><span class="sxs-lookup"><span data-stu-id="c3481-319"><span id="__nullterminated"></span><span id="__NULLTERMINATED"></span>\_\_nullterminated</span></span><br/>                                                      | <span data-ttu-id="c3481-320">La mémoire tampon peut être accessible jusqu’à et y compris le premier caractère ou pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="c3481-320">The buffer may be accessed up to and including the first **null** character or pointer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="c3481-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out \_ awcount (*expr*,*taille*)</span><span class="sxs-lookup"><span data-stu-id="c3481-321"><span id="__out_awcount_expr_size_"></span><span id="__OUT_AWCOUNT_EXPR_SIZE_"></span>\_\_out\_awcount(*expr*,*size*)</span></span><br/>                         | <span data-ttu-id="c3481-322">Si l’expression a la valeur true à la sortie, la taille de la mémoire tampon de sortie est spécifiée en octets.</span><span class="sxs-lookup"><span data-stu-id="c3481-322">If the expression is true at exit, the size of the output buffer is specified in bytes.</span></span> <span data-ttu-id="c3481-323">Si l’expression a la valeur false, la taille est spécifiée dans les éléments.</span><span class="sxs-lookup"><span data-stu-id="c3481-323">If the expression is false, the size is specified in elements.</span></span> <br/>                                                                                                              |
| <span data-ttu-id="c3481-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_remplacer</span><span class="sxs-lookup"><span data-stu-id="c3481-324"><span id="__override"></span><span id="__OVERRIDE"></span>\_\_override</span></span><br/>                                                                        | <span data-ttu-id="c3481-325">Spécifie le comportement de substitution de style C# pour les méthodes virtuelles.</span><span class="sxs-lookup"><span data-stu-id="c3481-325">Specifies C#-style override behavior for virtual methods.</span></span><br/>                                                                                                                                                                                                           |
| <span data-ttu-id="c3481-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_réservé</span><span class="sxs-lookup"><span data-stu-id="c3481-326"><span id="__reserved"></span><span id="__RESERVED"></span>\_\_reserved</span></span><br/>                                                                        | <span data-ttu-id="c3481-327">Le paramètre est réservé pour une utilisation ultérieure et doit être égal à zéro ou **null**.</span><span class="sxs-lookup"><span data-stu-id="c3481-327">The parameter is reserved for future use and must be zero or **NULL**.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="c3481-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_opération réussie (*expr*)</span><span class="sxs-lookup"><span data-stu-id="c3481-328"><span id="__success_expr_"></span><span id="__SUCCESS_EXPR_"></span>\_\_success(*expr*)</span></span><br/>                                                       | <span data-ttu-id="c3481-329">Si l’expression a la valeur true à la sortie, l’appelant peut s’appuyer sur toutes les garanties spécifiées par d’autres annotations.</span><span class="sxs-lookup"><span data-stu-id="c3481-329">If the expression is true at exit, the caller can rely on all guarantees specified by other annotations.</span></span> <span data-ttu-id="c3481-330">Si l’expression a la valeur false, l’appelant ne peut pas compter sur les garanties.</span><span class="sxs-lookup"><span data-stu-id="c3481-330">If the expression is false, the caller cannot rely on the guarantees.</span></span> <span data-ttu-id="c3481-331">Cette annotation est automatiquement ajoutée aux fonctions qui retournent une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3481-331">This annotation is automatically added to functions that return an **HRESULT** value.</span></span><br/> |
| <span data-ttu-id="c3481-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix (*CType*)</span><span class="sxs-lookup"><span data-stu-id="c3481-332"><span id="__typefix_ctype_"></span><span id="__TYPEFIX_CTYPE_"></span>\_\_typefix(*ctype*)</span></span><br/>                                                    | <span data-ttu-id="c3481-333">Traite le paramètre en tant que type spécifié plutôt qu’en tant que type déclaré.</span><span class="sxs-lookup"><span data-stu-id="c3481-333">Treat the parameter as the specified type rather than its declared type.</span></span><br/>                                                                                                                                                                                             |



 

<span data-ttu-id="c3481-334">Les exemples suivants illustrent la mémoire tampon et les annotations avancées pour les fonctions [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa)et [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) .</span><span class="sxs-lookup"><span data-stu-id="c3481-334">The following examples show the buffer and advanced annotations for the [**DeleteTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer), [**FreeEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-freeenvironmentstringsa), and [**UnhandledExceptionFilter**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) functions.</span></span>


```C++
__checkReturn
BOOL
WINAPI
DeleteTimerQueueTimer(
    __in_opt HANDLE TimerQueue,
    __in     HANDLE Timer,
    __in_opt HANDLE CompletionEvent
    );

BOOL
WINAPI
FreeEnvironmentStrings(
    __in __nullnullterminated LPTCH
    );

__callback
LONG
WINAPI
UnhandledExceptionFilter(
    __in struct _EXCEPTION_POINTERS *ExceptionInfo
    );

```



## <a name="related-topics"></a><span data-ttu-id="c3481-335">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3481-335">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3481-336">Annotations SAL</span><span class="sxs-lookup"><span data-stu-id="c3481-336">SAL Annotations</span></span>](/cpp/c-runtime-library/sal-annotations?view=vs-2019)
</dt> <dt>

[<span data-ttu-id="c3481-337">Procédure pas à pas : analyse du code C/C++ pour rechercher les erreurs</span><span class="sxs-lookup"><span data-stu-id="c3481-337">Walkthrough: Analyzing C/C++ Code for Defects</span></span>](/visualstudio/code-quality/walkthrough-analyzing-c-cpp-code-for-defects?view=vs-2015)
</dt> </dl>

 

