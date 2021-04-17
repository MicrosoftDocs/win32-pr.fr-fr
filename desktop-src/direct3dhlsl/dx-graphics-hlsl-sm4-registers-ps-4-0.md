---
title: Registres-ps_4_0
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de pixels version 4 \_ 0.
ms.assetid: 8b83667f-f599-4105-b68c-0d6aa7c528ab
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3dea9606419f32a168c08cc1efbebb5e285d3815
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379997"
---
# <a name="registers---ps_4_0"></a><span data-ttu-id="fdf21-103">Registres-PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fdf21-103">Registers - ps\_4\_0</span></span>

<span data-ttu-id="fdf21-104">Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de pixels version 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="fdf21-104">This section contains reference information for the input and output registers implemented by pixel shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="fdf21-105">Registres d’entrée</span><span class="sxs-lookup"><span data-stu-id="fdf21-105">Input Registers</span></span>



| <span data-ttu-id="fdf21-106">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="fdf21-106">Register</span></span>      | <span data-ttu-id="fdf21-107">Nom</span><span class="sxs-lookup"><span data-stu-id="fdf21-107">Name</span></span> | <span data-ttu-id="fdf21-108">Count</span><span class="sxs-lookup"><span data-stu-id="fdf21-108">Count</span></span>              | <span data-ttu-id="fdf21-109">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="fdf21-109">R/W</span></span> | <span data-ttu-id="fdf21-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="fdf21-110">Dimension</span></span> | <span data-ttu-id="fdf21-111">Indexable par r\#</span><span class="sxs-lookup"><span data-stu-id="fdf21-111">Indexable by r\#</span></span> | <span data-ttu-id="fdf21-112">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="fdf21-112">Defaults</span></span> | <span data-ttu-id="fdf21-113">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="fdf21-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="fdf21-114">r\#</span><span class="sxs-lookup"><span data-stu-id="fdf21-114">r\#</span></span>           |      | <span data-ttu-id="fdf21-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="fdf21-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="fdf21-116">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="fdf21-116">R/W</span></span> | <span data-ttu-id="fdf21-117">4</span><span class="sxs-lookup"><span data-stu-id="fdf21-117">4</span></span>         | <span data-ttu-id="fdf21-118">Non</span><span class="sxs-lookup"><span data-stu-id="fdf21-118">No</span></span>               | <span data-ttu-id="fdf21-119">None</span><span class="sxs-lookup"><span data-stu-id="fdf21-119">None</span></span>     | <span data-ttu-id="fdf21-120">Oui</span><span class="sxs-lookup"><span data-stu-id="fdf21-120">Yes</span></span>          |
| <span data-ttu-id="fdf21-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="fdf21-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="fdf21-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="fdf21-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="fdf21-123">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="fdf21-123">R/W</span></span> | <span data-ttu-id="fdf21-124">4</span><span class="sxs-lookup"><span data-stu-id="fdf21-124">4</span></span>         | <span data-ttu-id="fdf21-125">Oui</span><span class="sxs-lookup"><span data-stu-id="fdf21-125">Yes</span></span>              | <span data-ttu-id="fdf21-126">None</span><span class="sxs-lookup"><span data-stu-id="fdf21-126">None</span></span>     | <span data-ttu-id="fdf21-127">Oui</span><span class="sxs-lookup"><span data-stu-id="fdf21-127">Yes</span></span>          |
| <span data-ttu-id="fdf21-128">v\#</span><span class="sxs-lookup"><span data-stu-id="fdf21-128">v\#</span></span>           |      | <span data-ttu-id="fdf21-129">32</span><span class="sxs-lookup"><span data-stu-id="fdf21-129">32</span></span>                 | <span data-ttu-id="fdf21-130">R</span><span class="sxs-lookup"><span data-stu-id="fdf21-130">R</span></span>   | <span data-ttu-id="fdf21-131">4</span><span class="sxs-lookup"><span data-stu-id="fdf21-131">4</span></span>         | <span data-ttu-id="fdf21-132">Oui</span><span class="sxs-lookup"><span data-stu-id="fdf21-132">Yes</span></span>              | <span data-ttu-id="fdf21-133">None</span><span class="sxs-lookup"><span data-stu-id="fdf21-133">None</span></span>     | <span data-ttu-id="fdf21-134">Oui</span><span class="sxs-lookup"><span data-stu-id="fdf21-134">Yes</span></span>          |
| <span data-ttu-id="fdf21-135">t\#</span><span class="sxs-lookup"><span data-stu-id="fdf21-135">t\#</span></span>           |      | <span data-ttu-id="fdf21-136">128</span><span class="sxs-lookup"><span data-stu-id="fdf21-136">128</span></span>                | <span data-ttu-id="fdf21-137">R</span><span class="sxs-lookup"><span data-stu-id="fdf21-137">R</span></span>   | <span data-ttu-id="fdf21-138">1</span><span class="sxs-lookup"><span data-stu-id="fdf21-138">1</span></span>         | <span data-ttu-id="fdf21-139">Non</span><span class="sxs-lookup"><span data-stu-id="fdf21-139">No</span></span>               | <span data-ttu-id="fdf21-140">None</span><span class="sxs-lookup"><span data-stu-id="fdf21-140">None</span></span>     | <span data-ttu-id="fdf21-141">Oui</span><span class="sxs-lookup"><span data-stu-id="fdf21-141">Yes</span></span>          |
| <span data-ttu-id="fdf21-142">s\#</span><span class="sxs-lookup"><span data-stu-id="fdf21-142">s\#</span></span>           |      | <span data-ttu-id="fdf21-143">16</span><span class="sxs-lookup"><span data-stu-id="fdf21-143">16</span></span>                 | <span data-ttu-id="fdf21-144">R</span><span class="sxs-lookup"><span data-stu-id="fdf21-144">R</span></span>   | <span data-ttu-id="fdf21-145">1</span><span class="sxs-lookup"><span data-stu-id="fdf21-145">1</span></span>         | <span data-ttu-id="fdf21-146">Non</span><span class="sxs-lookup"><span data-stu-id="fdf21-146">No</span></span>               | <span data-ttu-id="fdf21-147">None</span><span class="sxs-lookup"><span data-stu-id="fdf21-147">None</span></span>     | <span data-ttu-id="fdf21-148">Oui</span><span class="sxs-lookup"><span data-stu-id="fdf21-148">Yes</span></span>          |
| <span data-ttu-id="fdf21-149">\# \[ index CB\]</span><span class="sxs-lookup"><span data-stu-id="fdf21-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="fdf21-150">15</span><span class="sxs-lookup"><span data-stu-id="fdf21-150">15</span></span>                 | <span data-ttu-id="fdf21-151">R</span><span class="sxs-lookup"><span data-stu-id="fdf21-151">R</span></span>   | <span data-ttu-id="fdf21-152">4</span><span class="sxs-lookup"><span data-stu-id="fdf21-152">4</span></span>         | <span data-ttu-id="fdf21-153">Oui (contenu)</span><span class="sxs-lookup"><span data-stu-id="fdf21-153">Yes(Contents)</span></span>    | <span data-ttu-id="fdf21-154">Aucun</span><span class="sxs-lookup"><span data-stu-id="fdf21-154">None</span></span>     | <span data-ttu-id="fdf21-155">Oui</span><span class="sxs-lookup"><span data-stu-id="fdf21-155">Yes</span></span>          |
| <span data-ttu-id="fdf21-156">\[index ICB\]</span><span class="sxs-lookup"><span data-stu-id="fdf21-156">icb\[index\]</span></span>  |      | <span data-ttu-id="fdf21-157">1</span><span class="sxs-lookup"><span data-stu-id="fdf21-157">1</span></span>                  | <span data-ttu-id="fdf21-158">R</span><span class="sxs-lookup"><span data-stu-id="fdf21-158">R</span></span>   | <span data-ttu-id="fdf21-159">4</span><span class="sxs-lookup"><span data-stu-id="fdf21-159">4</span></span>         | <span data-ttu-id="fdf21-160">Oui (contenu)</span><span class="sxs-lookup"><span data-stu-id="fdf21-160">Yes(Contents)</span></span>    | <span data-ttu-id="fdf21-161">Aucun</span><span class="sxs-lookup"><span data-stu-id="fdf21-161">None</span></span>     | <span data-ttu-id="fdf21-162">Oui</span><span class="sxs-lookup"><span data-stu-id="fdf21-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="fdf21-163">Registres de sortie</span><span class="sxs-lookup"><span data-stu-id="fdf21-163">Output Registers</span></span>



| <span data-ttu-id="fdf21-164">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="fdf21-164">Register</span></span> | <span data-ttu-id="fdf21-165">Nom</span><span class="sxs-lookup"><span data-stu-id="fdf21-165">Name</span></span>            | <span data-ttu-id="fdf21-166">Count</span><span class="sxs-lookup"><span data-stu-id="fdf21-166">Count</span></span> | <span data-ttu-id="fdf21-167">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="fdf21-167">R/W</span></span> | <span data-ttu-id="fdf21-168">Dimension</span><span class="sxs-lookup"><span data-stu-id="fdf21-168">Dimension</span></span> | <span data-ttu-id="fdf21-169">Indexable par r\#</span><span class="sxs-lookup"><span data-stu-id="fdf21-169">Indexable by r\#</span></span> | <span data-ttu-id="fdf21-170">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="fdf21-170">Defaults</span></span> | <span data-ttu-id="fdf21-171">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="fdf21-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="fdf21-172">NULL</span><span class="sxs-lookup"><span data-stu-id="fdf21-172">NULL</span></span>     | <span data-ttu-id="fdf21-173">Ignorer le résultat</span><span class="sxs-lookup"><span data-stu-id="fdf21-173">Discard Result</span></span>  | <span data-ttu-id="fdf21-174">N/A</span><span class="sxs-lookup"><span data-stu-id="fdf21-174">N/A</span></span>   | <span data-ttu-id="fdf21-175">W</span><span class="sxs-lookup"><span data-stu-id="fdf21-175">W</span></span>   | <span data-ttu-id="fdf21-176">N/A</span><span class="sxs-lookup"><span data-stu-id="fdf21-176">N/A</span></span>       | <span data-ttu-id="fdf21-177">N/A</span><span class="sxs-lookup"><span data-stu-id="fdf21-177">N/A</span></span>              | <span data-ttu-id="fdf21-178">N/A</span><span class="sxs-lookup"><span data-stu-id="fdf21-178">N/A</span></span>      | <span data-ttu-id="fdf21-179">Non</span><span class="sxs-lookup"><span data-stu-id="fdf21-179">No</span></span>           |
| <span data-ttu-id="fdf21-180">sorties\#</span><span class="sxs-lookup"><span data-stu-id="fdf21-180">o\#</span></span>      | <span data-ttu-id="fdf21-181">Registre de sortie</span><span class="sxs-lookup"><span data-stu-id="fdf21-181">Output Register</span></span> | <span data-ttu-id="fdf21-182">8</span><span class="sxs-lookup"><span data-stu-id="fdf21-182">8</span></span>     | <span data-ttu-id="fdf21-183">W</span><span class="sxs-lookup"><span data-stu-id="fdf21-183">W</span></span>   | <span data-ttu-id="fdf21-184">N/A</span><span class="sxs-lookup"><span data-stu-id="fdf21-184">N/A</span></span>       | <span data-ttu-id="fdf21-185">N/A</span><span class="sxs-lookup"><span data-stu-id="fdf21-185">N/A</span></span>              | <span data-ttu-id="fdf21-186">4</span><span class="sxs-lookup"><span data-stu-id="fdf21-186">4</span></span>        | <span data-ttu-id="fdf21-187">Non</span><span class="sxs-lookup"><span data-stu-id="fdf21-187">No</span></span>           |
| <span data-ttu-id="fdf21-188">oDepth</span><span class="sxs-lookup"><span data-stu-id="fdf21-188">oDepth</span></span>   | <span data-ttu-id="fdf21-189">Profondeur de sortie</span><span class="sxs-lookup"><span data-stu-id="fdf21-189">Output Depth</span></span>    | <span data-ttu-id="fdf21-190">1</span><span class="sxs-lookup"><span data-stu-id="fdf21-190">1</span></span>     | <span data-ttu-id="fdf21-191">W</span><span class="sxs-lookup"><span data-stu-id="fdf21-191">W</span></span>   | <span data-ttu-id="fdf21-192">N/A</span><span class="sxs-lookup"><span data-stu-id="fdf21-192">N/A</span></span>       | <span data-ttu-id="fdf21-193">N/A</span><span class="sxs-lookup"><span data-stu-id="fdf21-193">N/A</span></span>              | <span data-ttu-id="fdf21-194">1</span><span class="sxs-lookup"><span data-stu-id="fdf21-194">1</span></span>        | <span data-ttu-id="fdf21-195">N/A</span><span class="sxs-lookup"><span data-stu-id="fdf21-195">N/A</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="fdf21-196">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fdf21-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdf21-197">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="fdf21-197">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




