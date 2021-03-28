---
title: Registres-gs_4_1
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par les versions de nuanceur Geometry 4 \_ 0 et 4 \_ 1.
ms.assetid: 0312707D-11D0-45D0-9E8C-8BD2BC65352C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a01f200bd4183843b1cfd2892fde5da442ca8d36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196960"
---
# <a name="registers---gs_4_1"></a><span data-ttu-id="0e94b-103">Registres-GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0e94b-103">Registers - gs\_4\_1</span></span>

<span data-ttu-id="0e94b-104">Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par les versions de nuanceur Geometry 4 \_ 0 et 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="0e94b-104">This section contains reference information for the input and output registers implemented by geometry shader versions 4\_0 and 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="0e94b-105">Registres d’entrée</span><span class="sxs-lookup"><span data-stu-id="0e94b-105">Input Registers</span></span>



| <span data-ttu-id="0e94b-106">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="0e94b-106">Register</span></span>                 | <span data-ttu-id="0e94b-107">Nom</span><span class="sxs-lookup"><span data-stu-id="0e94b-107">Name</span></span> | <span data-ttu-id="0e94b-108">Count</span><span class="sxs-lookup"><span data-stu-id="0e94b-108">Count</span></span>              | <span data-ttu-id="0e94b-109">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="0e94b-109">R/W</span></span> | <span data-ttu-id="0e94b-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="0e94b-110">Dimension</span></span>        | <span data-ttu-id="0e94b-111">Indexable par r\#</span><span class="sxs-lookup"><span data-stu-id="0e94b-111">Indexable by r\#</span></span> | <span data-ttu-id="0e94b-112">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="0e94b-112">Defaults</span></span> | <span data-ttu-id="0e94b-113">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="0e94b-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="0e94b-114">r\#</span><span class="sxs-lookup"><span data-stu-id="0e94b-114">r\#</span></span>                      |      | <span data-ttu-id="0e94b-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="0e94b-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="0e94b-116">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="0e94b-116">R/W</span></span> | <span data-ttu-id="0e94b-117">4</span><span class="sxs-lookup"><span data-stu-id="0e94b-117">4</span></span>                | <span data-ttu-id="0e94b-118">Non</span><span class="sxs-lookup"><span data-stu-id="0e94b-118">No</span></span>               | <span data-ttu-id="0e94b-119">None</span><span class="sxs-lookup"><span data-stu-id="0e94b-119">None</span></span>     | <span data-ttu-id="0e94b-120">Oui</span><span class="sxs-lookup"><span data-stu-id="0e94b-120">Yes</span></span>          |
| <span data-ttu-id="0e94b-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="0e94b-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="0e94b-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="0e94b-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="0e94b-123">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="0e94b-123">R/W</span></span> | <span data-ttu-id="0e94b-124">4</span><span class="sxs-lookup"><span data-stu-id="0e94b-124">4</span></span>                | <span data-ttu-id="0e94b-125">Oui</span><span class="sxs-lookup"><span data-stu-id="0e94b-125">Yes</span></span>              | <span data-ttu-id="0e94b-126">None</span><span class="sxs-lookup"><span data-stu-id="0e94b-126">None</span></span>     | <span data-ttu-id="0e94b-127">Oui</span><span class="sxs-lookup"><span data-stu-id="0e94b-127">Yes</span></span>          |
| <span data-ttu-id="0e94b-128">\# \[ élément sommet \] \[ v\]</span><span class="sxs-lookup"><span data-stu-id="0e94b-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="0e94b-129">32</span><span class="sxs-lookup"><span data-stu-id="0e94b-129">32</span></span>                 | <span data-ttu-id="0e94b-130">R</span><span class="sxs-lookup"><span data-stu-id="0e94b-130">R</span></span>   | <span data-ttu-id="0e94b-131">4 (COMP) \* 6 (vert)</span><span class="sxs-lookup"><span data-stu-id="0e94b-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="0e94b-132">Oui</span><span class="sxs-lookup"><span data-stu-id="0e94b-132">Yes</span></span>              | <span data-ttu-id="0e94b-133">None</span><span class="sxs-lookup"><span data-stu-id="0e94b-133">None</span></span>     | <span data-ttu-id="0e94b-134">Oui</span><span class="sxs-lookup"><span data-stu-id="0e94b-134">Yes</span></span>          |
| <span data-ttu-id="0e94b-135">vprim</span><span class="sxs-lookup"><span data-stu-id="0e94b-135">vprim</span></span>                    |      | <span data-ttu-id="0e94b-136">1</span><span class="sxs-lookup"><span data-stu-id="0e94b-136">1</span></span>                  | <span data-ttu-id="0e94b-137">R</span><span class="sxs-lookup"><span data-stu-id="0e94b-137">R</span></span>   | <span data-ttu-id="0e94b-138">1</span><span class="sxs-lookup"><span data-stu-id="0e94b-138">1</span></span>                | <span data-ttu-id="0e94b-139">Non</span><span class="sxs-lookup"><span data-stu-id="0e94b-139">No</span></span>               | <span data-ttu-id="0e94b-140">None</span><span class="sxs-lookup"><span data-stu-id="0e94b-140">None</span></span>     | <span data-ttu-id="0e94b-141">Oui</span><span class="sxs-lookup"><span data-stu-id="0e94b-141">Yes</span></span>          |
| <span data-ttu-id="0e94b-142">t\#</span><span class="sxs-lookup"><span data-stu-id="0e94b-142">t\#</span></span>                      |      | <span data-ttu-id="0e94b-143">128</span><span class="sxs-lookup"><span data-stu-id="0e94b-143">128</span></span>                | <span data-ttu-id="0e94b-144">R</span><span class="sxs-lookup"><span data-stu-id="0e94b-144">R</span></span>   | <span data-ttu-id="0e94b-145">1</span><span class="sxs-lookup"><span data-stu-id="0e94b-145">1</span></span>                | <span data-ttu-id="0e94b-146">Non</span><span class="sxs-lookup"><span data-stu-id="0e94b-146">No</span></span>               | <span data-ttu-id="0e94b-147">None</span><span class="sxs-lookup"><span data-stu-id="0e94b-147">None</span></span>     | <span data-ttu-id="0e94b-148">Oui</span><span class="sxs-lookup"><span data-stu-id="0e94b-148">Yes</span></span>          |
| <span data-ttu-id="0e94b-149">s\#</span><span class="sxs-lookup"><span data-stu-id="0e94b-149">s\#</span></span>                      |      | <span data-ttu-id="0e94b-150">16</span><span class="sxs-lookup"><span data-stu-id="0e94b-150">16</span></span>                 | <span data-ttu-id="0e94b-151">R</span><span class="sxs-lookup"><span data-stu-id="0e94b-151">R</span></span>   | <span data-ttu-id="0e94b-152">1</span><span class="sxs-lookup"><span data-stu-id="0e94b-152">1</span></span>                | <span data-ttu-id="0e94b-153">Non</span><span class="sxs-lookup"><span data-stu-id="0e94b-153">No</span></span>               | <span data-ttu-id="0e94b-154">None</span><span class="sxs-lookup"><span data-stu-id="0e94b-154">None</span></span>     | <span data-ttu-id="0e94b-155">Oui</span><span class="sxs-lookup"><span data-stu-id="0e94b-155">Yes</span></span>          |
| <span data-ttu-id="0e94b-156">\# \[ index CB\]</span><span class="sxs-lookup"><span data-stu-id="0e94b-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="0e94b-157">15</span><span class="sxs-lookup"><span data-stu-id="0e94b-157">15</span></span>                 | <span data-ttu-id="0e94b-158">R</span><span class="sxs-lookup"><span data-stu-id="0e94b-158">R</span></span>   | <span data-ttu-id="0e94b-159">4</span><span class="sxs-lookup"><span data-stu-id="0e94b-159">4</span></span>                | <span data-ttu-id="0e94b-160">Oui (contenu)</span><span class="sxs-lookup"><span data-stu-id="0e94b-160">Yes(Contents)</span></span>    | <span data-ttu-id="0e94b-161">Aucun</span><span class="sxs-lookup"><span data-stu-id="0e94b-161">None</span></span>     | <span data-ttu-id="0e94b-162">Oui</span><span class="sxs-lookup"><span data-stu-id="0e94b-162">Yes</span></span>          |
| <span data-ttu-id="0e94b-163">\[index ICB\]</span><span class="sxs-lookup"><span data-stu-id="0e94b-163">icb\[index\]</span></span>             |      | <span data-ttu-id="0e94b-164">1</span><span class="sxs-lookup"><span data-stu-id="0e94b-164">1</span></span>                  | <span data-ttu-id="0e94b-165">R</span><span class="sxs-lookup"><span data-stu-id="0e94b-165">R</span></span>   | <span data-ttu-id="0e94b-166">4</span><span class="sxs-lookup"><span data-stu-id="0e94b-166">4</span></span>                | <span data-ttu-id="0e94b-167">Oui (contenu)</span><span class="sxs-lookup"><span data-stu-id="0e94b-167">Yes(Contents)</span></span>    | <span data-ttu-id="0e94b-168">Aucun</span><span class="sxs-lookup"><span data-stu-id="0e94b-168">None</span></span>     | <span data-ttu-id="0e94b-169">Oui</span><span class="sxs-lookup"><span data-stu-id="0e94b-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="0e94b-170">Registres de sortie</span><span class="sxs-lookup"><span data-stu-id="0e94b-170">Output Registers</span></span>



| <span data-ttu-id="0e94b-171">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="0e94b-171">Register</span></span> | <span data-ttu-id="0e94b-172">Nom</span><span class="sxs-lookup"><span data-stu-id="0e94b-172">Name</span></span>            | <span data-ttu-id="0e94b-173">Count</span><span class="sxs-lookup"><span data-stu-id="0e94b-173">Count</span></span> | <span data-ttu-id="0e94b-174">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="0e94b-174">R/W</span></span> | <span data-ttu-id="0e94b-175">Dimension</span><span class="sxs-lookup"><span data-stu-id="0e94b-175">Dimension</span></span> | <span data-ttu-id="0e94b-176">Indexable par r\#</span><span class="sxs-lookup"><span data-stu-id="0e94b-176">Indexable by r\#</span></span> | <span data-ttu-id="0e94b-177">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="0e94b-177">Defaults</span></span> | <span data-ttu-id="0e94b-178">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="0e94b-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="0e94b-179">NULL</span><span class="sxs-lookup"><span data-stu-id="0e94b-179">NULL</span></span>     | <span data-ttu-id="0e94b-180">Ignorer le résultat</span><span class="sxs-lookup"><span data-stu-id="0e94b-180">Discard Result</span></span>  | <span data-ttu-id="0e94b-181">N/A</span><span class="sxs-lookup"><span data-stu-id="0e94b-181">N/A</span></span>   | <span data-ttu-id="0e94b-182">W</span><span class="sxs-lookup"><span data-stu-id="0e94b-182">W</span></span>   | <span data-ttu-id="0e94b-183">N/A</span><span class="sxs-lookup"><span data-stu-id="0e94b-183">N/A</span></span>       | <span data-ttu-id="0e94b-184">N/A</span><span class="sxs-lookup"><span data-stu-id="0e94b-184">N/A</span></span>              | <span data-ttu-id="0e94b-185">N/A</span><span class="sxs-lookup"><span data-stu-id="0e94b-185">N/A</span></span>      | <span data-ttu-id="0e94b-186">Non</span><span class="sxs-lookup"><span data-stu-id="0e94b-186">No</span></span>           |
| <span data-ttu-id="0e94b-187">sorties\#</span><span class="sxs-lookup"><span data-stu-id="0e94b-187">o\#</span></span>      | <span data-ttu-id="0e94b-188">Registre de sortie</span><span class="sxs-lookup"><span data-stu-id="0e94b-188">Output Register</span></span> | <span data-ttu-id="0e94b-189">32</span><span class="sxs-lookup"><span data-stu-id="0e94b-189">32</span></span>    | <span data-ttu-id="0e94b-190">W</span><span class="sxs-lookup"><span data-stu-id="0e94b-190">W</span></span>   | <span data-ttu-id="0e94b-191">N/A</span><span class="sxs-lookup"><span data-stu-id="0e94b-191">N/A</span></span>       | <span data-ttu-id="0e94b-192">N/A</span><span class="sxs-lookup"><span data-stu-id="0e94b-192">N/A</span></span>              | <span data-ttu-id="0e94b-193">4</span><span class="sxs-lookup"><span data-stu-id="0e94b-193">4</span></span>        | <span data-ttu-id="0e94b-194">Oui</span><span class="sxs-lookup"><span data-stu-id="0e94b-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="0e94b-195">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e94b-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e94b-196">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0e94b-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




