---
title: Registres-gs_4_0
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur Geometry version 4 \_ 0.
ms.assetid: 1f3ebd71-19de-4e26-87f0-4fb5c8e2a343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c5db86ffb797434af4badd6496b71a4ad684583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507263"
---
# <a name="registers---gs_4_0"></a><span data-ttu-id="0e66d-103">Registres-GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0e66d-103">Registers - gs\_4\_0</span></span>

<span data-ttu-id="0e66d-104">Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur Geometry version 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="0e66d-104">This section contains reference information for the input and output registers implemented by geometry shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="0e66d-105">Registres d’entrée</span><span class="sxs-lookup"><span data-stu-id="0e66d-105">Input Registers</span></span>



| <span data-ttu-id="0e66d-106">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="0e66d-106">Register</span></span>                 | <span data-ttu-id="0e66d-107">Nom</span><span class="sxs-lookup"><span data-stu-id="0e66d-107">Name</span></span> | <span data-ttu-id="0e66d-108">Count</span><span class="sxs-lookup"><span data-stu-id="0e66d-108">Count</span></span>              | <span data-ttu-id="0e66d-109">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="0e66d-109">R/W</span></span> | <span data-ttu-id="0e66d-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="0e66d-110">Dimension</span></span>        | <span data-ttu-id="0e66d-111">Indexable par r\#</span><span class="sxs-lookup"><span data-stu-id="0e66d-111">Indexable by r\#</span></span> | <span data-ttu-id="0e66d-112">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="0e66d-112">Defaults</span></span> | <span data-ttu-id="0e66d-113">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="0e66d-113">Requires DCL</span></span> |
|--------------------------|------|--------------------|-----|------------------|------------------|----------|--------------|
| <span data-ttu-id="0e66d-114">r\#</span><span class="sxs-lookup"><span data-stu-id="0e66d-114">r\#</span></span>                      |      | <span data-ttu-id="0e66d-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="0e66d-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="0e66d-116">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="0e66d-116">R/W</span></span> | <span data-ttu-id="0e66d-117">4</span><span class="sxs-lookup"><span data-stu-id="0e66d-117">4</span></span>                | <span data-ttu-id="0e66d-118">Non</span><span class="sxs-lookup"><span data-stu-id="0e66d-118">No</span></span>               | <span data-ttu-id="0e66d-119">None</span><span class="sxs-lookup"><span data-stu-id="0e66d-119">None</span></span>     | <span data-ttu-id="0e66d-120">Oui</span><span class="sxs-lookup"><span data-stu-id="0e66d-120">Yes</span></span>          |
| <span data-ttu-id="0e66d-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="0e66d-121">x\#\[n\]</span></span>                 |      | <span data-ttu-id="0e66d-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="0e66d-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="0e66d-123">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="0e66d-123">R/W</span></span> | <span data-ttu-id="0e66d-124">4</span><span class="sxs-lookup"><span data-stu-id="0e66d-124">4</span></span>                | <span data-ttu-id="0e66d-125">Oui</span><span class="sxs-lookup"><span data-stu-id="0e66d-125">Yes</span></span>              | <span data-ttu-id="0e66d-126">None</span><span class="sxs-lookup"><span data-stu-id="0e66d-126">None</span></span>     | <span data-ttu-id="0e66d-127">Oui</span><span class="sxs-lookup"><span data-stu-id="0e66d-127">Yes</span></span>          |
| <span data-ttu-id="0e66d-128">\# \[ élément sommet \] \[ v\]</span><span class="sxs-lookup"><span data-stu-id="0e66d-128">v\#\[vertex\]\[element\]</span></span> |      | <span data-ttu-id="0e66d-129">32</span><span class="sxs-lookup"><span data-stu-id="0e66d-129">32</span></span>                 | <span data-ttu-id="0e66d-130">R</span><span class="sxs-lookup"><span data-stu-id="0e66d-130">R</span></span>   | <span data-ttu-id="0e66d-131">4 (COMP) \* 6 (vert)</span><span class="sxs-lookup"><span data-stu-id="0e66d-131">4(comp)\*6(vert)</span></span> | <span data-ttu-id="0e66d-132">Oui</span><span class="sxs-lookup"><span data-stu-id="0e66d-132">Yes</span></span>              | <span data-ttu-id="0e66d-133">None</span><span class="sxs-lookup"><span data-stu-id="0e66d-133">None</span></span>     | <span data-ttu-id="0e66d-134">Oui</span><span class="sxs-lookup"><span data-stu-id="0e66d-134">Yes</span></span>          |
| <span data-ttu-id="0e66d-135">vprim</span><span class="sxs-lookup"><span data-stu-id="0e66d-135">vprim</span></span>                    |      | <span data-ttu-id="0e66d-136">1</span><span class="sxs-lookup"><span data-stu-id="0e66d-136">1</span></span>                  | <span data-ttu-id="0e66d-137">R</span><span class="sxs-lookup"><span data-stu-id="0e66d-137">R</span></span>   | <span data-ttu-id="0e66d-138">1</span><span class="sxs-lookup"><span data-stu-id="0e66d-138">1</span></span>                | <span data-ttu-id="0e66d-139">Non</span><span class="sxs-lookup"><span data-stu-id="0e66d-139">No</span></span>               | <span data-ttu-id="0e66d-140">None</span><span class="sxs-lookup"><span data-stu-id="0e66d-140">None</span></span>     | <span data-ttu-id="0e66d-141">Oui</span><span class="sxs-lookup"><span data-stu-id="0e66d-141">Yes</span></span>          |
| <span data-ttu-id="0e66d-142">t\#</span><span class="sxs-lookup"><span data-stu-id="0e66d-142">t\#</span></span>                      |      | <span data-ttu-id="0e66d-143">128</span><span class="sxs-lookup"><span data-stu-id="0e66d-143">128</span></span>                | <span data-ttu-id="0e66d-144">R</span><span class="sxs-lookup"><span data-stu-id="0e66d-144">R</span></span>   | <span data-ttu-id="0e66d-145">1</span><span class="sxs-lookup"><span data-stu-id="0e66d-145">1</span></span>                | <span data-ttu-id="0e66d-146">Non</span><span class="sxs-lookup"><span data-stu-id="0e66d-146">No</span></span>               | <span data-ttu-id="0e66d-147">None</span><span class="sxs-lookup"><span data-stu-id="0e66d-147">None</span></span>     | <span data-ttu-id="0e66d-148">Oui</span><span class="sxs-lookup"><span data-stu-id="0e66d-148">Yes</span></span>          |
| <span data-ttu-id="0e66d-149">s\#</span><span class="sxs-lookup"><span data-stu-id="0e66d-149">s\#</span></span>                      |      | <span data-ttu-id="0e66d-150">16</span><span class="sxs-lookup"><span data-stu-id="0e66d-150">16</span></span>                 | <span data-ttu-id="0e66d-151">R</span><span class="sxs-lookup"><span data-stu-id="0e66d-151">R</span></span>   | <span data-ttu-id="0e66d-152">1</span><span class="sxs-lookup"><span data-stu-id="0e66d-152">1</span></span>                | <span data-ttu-id="0e66d-153">Non</span><span class="sxs-lookup"><span data-stu-id="0e66d-153">No</span></span>               | <span data-ttu-id="0e66d-154">None</span><span class="sxs-lookup"><span data-stu-id="0e66d-154">None</span></span>     | <span data-ttu-id="0e66d-155">Oui</span><span class="sxs-lookup"><span data-stu-id="0e66d-155">Yes</span></span>          |
| <span data-ttu-id="0e66d-156">\# \[ index CB\]</span><span class="sxs-lookup"><span data-stu-id="0e66d-156">cb\#\[index\]</span></span>            |      | <span data-ttu-id="0e66d-157">15</span><span class="sxs-lookup"><span data-stu-id="0e66d-157">15</span></span>                 | <span data-ttu-id="0e66d-158">R</span><span class="sxs-lookup"><span data-stu-id="0e66d-158">R</span></span>   | <span data-ttu-id="0e66d-159">4</span><span class="sxs-lookup"><span data-stu-id="0e66d-159">4</span></span>                | <span data-ttu-id="0e66d-160">Oui (contenu)</span><span class="sxs-lookup"><span data-stu-id="0e66d-160">Yes(Contents)</span></span>    | <span data-ttu-id="0e66d-161">Aucun</span><span class="sxs-lookup"><span data-stu-id="0e66d-161">None</span></span>     | <span data-ttu-id="0e66d-162">Oui</span><span class="sxs-lookup"><span data-stu-id="0e66d-162">Yes</span></span>          |
| <span data-ttu-id="0e66d-163">\[index ICB\]</span><span class="sxs-lookup"><span data-stu-id="0e66d-163">icb\[index\]</span></span>             |      | <span data-ttu-id="0e66d-164">1</span><span class="sxs-lookup"><span data-stu-id="0e66d-164">1</span></span>                  | <span data-ttu-id="0e66d-165">R</span><span class="sxs-lookup"><span data-stu-id="0e66d-165">R</span></span>   | <span data-ttu-id="0e66d-166">4</span><span class="sxs-lookup"><span data-stu-id="0e66d-166">4</span></span>                | <span data-ttu-id="0e66d-167">Oui (contenu)</span><span class="sxs-lookup"><span data-stu-id="0e66d-167">Yes(Contents)</span></span>    | <span data-ttu-id="0e66d-168">Aucun</span><span class="sxs-lookup"><span data-stu-id="0e66d-168">None</span></span>     | <span data-ttu-id="0e66d-169">Oui</span><span class="sxs-lookup"><span data-stu-id="0e66d-169">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="0e66d-170">Registres de sortie</span><span class="sxs-lookup"><span data-stu-id="0e66d-170">Output Registers</span></span>



| <span data-ttu-id="0e66d-171">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="0e66d-171">Register</span></span> | <span data-ttu-id="0e66d-172">Nom</span><span class="sxs-lookup"><span data-stu-id="0e66d-172">Name</span></span>            | <span data-ttu-id="0e66d-173">Count</span><span class="sxs-lookup"><span data-stu-id="0e66d-173">Count</span></span> | <span data-ttu-id="0e66d-174">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="0e66d-174">R/W</span></span> | <span data-ttu-id="0e66d-175">Dimension</span><span class="sxs-lookup"><span data-stu-id="0e66d-175">Dimension</span></span> | <span data-ttu-id="0e66d-176">Indexable par r\#</span><span class="sxs-lookup"><span data-stu-id="0e66d-176">Indexable by r\#</span></span> | <span data-ttu-id="0e66d-177">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="0e66d-177">Defaults</span></span> | <span data-ttu-id="0e66d-178">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="0e66d-178">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="0e66d-179">NULL</span><span class="sxs-lookup"><span data-stu-id="0e66d-179">NULL</span></span>     | <span data-ttu-id="0e66d-180">Ignorer le résultat</span><span class="sxs-lookup"><span data-stu-id="0e66d-180">Discard Result</span></span>  | <span data-ttu-id="0e66d-181">N/A</span><span class="sxs-lookup"><span data-stu-id="0e66d-181">N/A</span></span>   | <span data-ttu-id="0e66d-182">W</span><span class="sxs-lookup"><span data-stu-id="0e66d-182">W</span></span>   | <span data-ttu-id="0e66d-183">N/A</span><span class="sxs-lookup"><span data-stu-id="0e66d-183">N/A</span></span>       | <span data-ttu-id="0e66d-184">N/A</span><span class="sxs-lookup"><span data-stu-id="0e66d-184">N/A</span></span>              | <span data-ttu-id="0e66d-185">N/A</span><span class="sxs-lookup"><span data-stu-id="0e66d-185">N/A</span></span>      | <span data-ttu-id="0e66d-186">Non</span><span class="sxs-lookup"><span data-stu-id="0e66d-186">No</span></span>           |
| <span data-ttu-id="0e66d-187">sorties\#</span><span class="sxs-lookup"><span data-stu-id="0e66d-187">o\#</span></span>      | <span data-ttu-id="0e66d-188">Registre de sortie</span><span class="sxs-lookup"><span data-stu-id="0e66d-188">Output Register</span></span> | <span data-ttu-id="0e66d-189">32</span><span class="sxs-lookup"><span data-stu-id="0e66d-189">32</span></span>    | <span data-ttu-id="0e66d-190">W</span><span class="sxs-lookup"><span data-stu-id="0e66d-190">W</span></span>   | <span data-ttu-id="0e66d-191">N/A</span><span class="sxs-lookup"><span data-stu-id="0e66d-191">N/A</span></span>       | <span data-ttu-id="0e66d-192">N/A</span><span class="sxs-lookup"><span data-stu-id="0e66d-192">N/A</span></span>              | <span data-ttu-id="0e66d-193">4</span><span class="sxs-lookup"><span data-stu-id="0e66d-193">4</span></span>        | <span data-ttu-id="0e66d-194">Oui</span><span class="sxs-lookup"><span data-stu-id="0e66d-194">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="0e66d-195">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0e66d-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e66d-196">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0e66d-196">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




