---
title: Registres-vs_4_1
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de sommets version 4 \_ 1.
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df2254c111303129327d255f94727a5e42ac1c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196959"
---
# <a name="registers---vs_4_1"></a><span data-ttu-id="99e05-103">Registres-vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="99e05-103">Registers - vs\_4\_1</span></span>

<span data-ttu-id="99e05-104">Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de sommets version 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="99e05-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="99e05-105">Registres d’entrée</span><span class="sxs-lookup"><span data-stu-id="99e05-105">Input Registers</span></span>



| <span data-ttu-id="99e05-106">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="99e05-106">Register</span></span>      | <span data-ttu-id="99e05-107">Nom</span><span class="sxs-lookup"><span data-stu-id="99e05-107">Name</span></span> | <span data-ttu-id="99e05-108">Count</span><span class="sxs-lookup"><span data-stu-id="99e05-108">Count</span></span>              | <span data-ttu-id="99e05-109">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="99e05-109">R/W</span></span> | <span data-ttu-id="99e05-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="99e05-110">Dimension</span></span> | <span data-ttu-id="99e05-111">Indexable par r\#</span><span class="sxs-lookup"><span data-stu-id="99e05-111">Indexable by r\#</span></span> | <span data-ttu-id="99e05-112">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="99e05-112">Defaults</span></span> | <span data-ttu-id="99e05-113">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="99e05-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="99e05-114">r\#</span><span class="sxs-lookup"><span data-stu-id="99e05-114">r\#</span></span>           |      | <span data-ttu-id="99e05-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="99e05-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="99e05-116">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="99e05-116">R/W</span></span> | <span data-ttu-id="99e05-117">4</span><span class="sxs-lookup"><span data-stu-id="99e05-117">4</span></span>         | <span data-ttu-id="99e05-118">Non</span><span class="sxs-lookup"><span data-stu-id="99e05-118">No</span></span>               | <span data-ttu-id="99e05-119">None</span><span class="sxs-lookup"><span data-stu-id="99e05-119">None</span></span>     | <span data-ttu-id="99e05-120">Oui</span><span class="sxs-lookup"><span data-stu-id="99e05-120">Yes</span></span>          |
| <span data-ttu-id="99e05-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="99e05-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="99e05-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="99e05-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="99e05-123">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="99e05-123">R/W</span></span> | <span data-ttu-id="99e05-124">4</span><span class="sxs-lookup"><span data-stu-id="99e05-124">4</span></span>         | <span data-ttu-id="99e05-125">Oui</span><span class="sxs-lookup"><span data-stu-id="99e05-125">Yes</span></span>              | <span data-ttu-id="99e05-126">None</span><span class="sxs-lookup"><span data-stu-id="99e05-126">None</span></span>     | <span data-ttu-id="99e05-127">Oui</span><span class="sxs-lookup"><span data-stu-id="99e05-127">Yes</span></span>          |
| <span data-ttu-id="99e05-128">v\#</span><span class="sxs-lookup"><span data-stu-id="99e05-128">v\#</span></span>           |      | <span data-ttu-id="99e05-129">32</span><span class="sxs-lookup"><span data-stu-id="99e05-129">32</span></span>                 | <span data-ttu-id="99e05-130">R</span><span class="sxs-lookup"><span data-stu-id="99e05-130">R</span></span>   | <span data-ttu-id="99e05-131">4</span><span class="sxs-lookup"><span data-stu-id="99e05-131">4</span></span>         | <span data-ttu-id="99e05-132">Oui</span><span class="sxs-lookup"><span data-stu-id="99e05-132">Yes</span></span>              | <span data-ttu-id="99e05-133">None</span><span class="sxs-lookup"><span data-stu-id="99e05-133">None</span></span>     | <span data-ttu-id="99e05-134">Oui</span><span class="sxs-lookup"><span data-stu-id="99e05-134">Yes</span></span>          |
| <span data-ttu-id="99e05-135">t\#</span><span class="sxs-lookup"><span data-stu-id="99e05-135">t\#</span></span>           |      | <span data-ttu-id="99e05-136">128</span><span class="sxs-lookup"><span data-stu-id="99e05-136">128</span></span>                | <span data-ttu-id="99e05-137">R</span><span class="sxs-lookup"><span data-stu-id="99e05-137">R</span></span>   | <span data-ttu-id="99e05-138">1</span><span class="sxs-lookup"><span data-stu-id="99e05-138">1</span></span>         | <span data-ttu-id="99e05-139">Non</span><span class="sxs-lookup"><span data-stu-id="99e05-139">No</span></span>               | <span data-ttu-id="99e05-140">None</span><span class="sxs-lookup"><span data-stu-id="99e05-140">None</span></span>     | <span data-ttu-id="99e05-141">Oui</span><span class="sxs-lookup"><span data-stu-id="99e05-141">Yes</span></span>          |
| <span data-ttu-id="99e05-142">s\#</span><span class="sxs-lookup"><span data-stu-id="99e05-142">s\#</span></span>           |      | <span data-ttu-id="99e05-143">16</span><span class="sxs-lookup"><span data-stu-id="99e05-143">16</span></span>                 | <span data-ttu-id="99e05-144">R</span><span class="sxs-lookup"><span data-stu-id="99e05-144">R</span></span>   | <span data-ttu-id="99e05-145">1</span><span class="sxs-lookup"><span data-stu-id="99e05-145">1</span></span>         | <span data-ttu-id="99e05-146">Non</span><span class="sxs-lookup"><span data-stu-id="99e05-146">No</span></span>               | <span data-ttu-id="99e05-147">None</span><span class="sxs-lookup"><span data-stu-id="99e05-147">None</span></span>     | <span data-ttu-id="99e05-148">Oui</span><span class="sxs-lookup"><span data-stu-id="99e05-148">Yes</span></span>          |
| <span data-ttu-id="99e05-149">\# \[ index CB\]</span><span class="sxs-lookup"><span data-stu-id="99e05-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="99e05-150">15</span><span class="sxs-lookup"><span data-stu-id="99e05-150">15</span></span>                 | <span data-ttu-id="99e05-151">R</span><span class="sxs-lookup"><span data-stu-id="99e05-151">R</span></span>   | <span data-ttu-id="99e05-152">4</span><span class="sxs-lookup"><span data-stu-id="99e05-152">4</span></span>         | <span data-ttu-id="99e05-153">Oui (contenu)</span><span class="sxs-lookup"><span data-stu-id="99e05-153">Yes(Contents)</span></span>    | <span data-ttu-id="99e05-154">Aucun</span><span class="sxs-lookup"><span data-stu-id="99e05-154">None</span></span>     | <span data-ttu-id="99e05-155">Oui</span><span class="sxs-lookup"><span data-stu-id="99e05-155">Yes</span></span>          |
| <span data-ttu-id="99e05-156">\[index ICB\]</span><span class="sxs-lookup"><span data-stu-id="99e05-156">icb\[index\]</span></span>  |      | <span data-ttu-id="99e05-157">1</span><span class="sxs-lookup"><span data-stu-id="99e05-157">1</span></span>                  | <span data-ttu-id="99e05-158">R</span><span class="sxs-lookup"><span data-stu-id="99e05-158">R</span></span>   | <span data-ttu-id="99e05-159">4</span><span class="sxs-lookup"><span data-stu-id="99e05-159">4</span></span>         | <span data-ttu-id="99e05-160">Oui (contenu)</span><span class="sxs-lookup"><span data-stu-id="99e05-160">Yes(Contents)</span></span>    | <span data-ttu-id="99e05-161">Aucun</span><span class="sxs-lookup"><span data-stu-id="99e05-161">None</span></span>     | <span data-ttu-id="99e05-162">Oui</span><span class="sxs-lookup"><span data-stu-id="99e05-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="99e05-163">Registres de sortie</span><span class="sxs-lookup"><span data-stu-id="99e05-163">Output Registers</span></span>



| <span data-ttu-id="99e05-164">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="99e05-164">Register</span></span> | <span data-ttu-id="99e05-165">Nom</span><span class="sxs-lookup"><span data-stu-id="99e05-165">Name</span></span>            | <span data-ttu-id="99e05-166">Count</span><span class="sxs-lookup"><span data-stu-id="99e05-166">Count</span></span> | <span data-ttu-id="99e05-167">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="99e05-167">R/W</span></span> | <span data-ttu-id="99e05-168">Dimension</span><span class="sxs-lookup"><span data-stu-id="99e05-168">Dimension</span></span> | <span data-ttu-id="99e05-169">Indexable par r\#</span><span class="sxs-lookup"><span data-stu-id="99e05-169">Indexable by r\#</span></span> | <span data-ttu-id="99e05-170">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="99e05-170">Defaults</span></span> | <span data-ttu-id="99e05-171">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="99e05-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="99e05-172">NULL</span><span class="sxs-lookup"><span data-stu-id="99e05-172">NULL</span></span>     | <span data-ttu-id="99e05-173">Ignorer le résultat</span><span class="sxs-lookup"><span data-stu-id="99e05-173">Discard Result</span></span>  | <span data-ttu-id="99e05-174">N/A</span><span class="sxs-lookup"><span data-stu-id="99e05-174">N/A</span></span>   | <span data-ttu-id="99e05-175">W</span><span class="sxs-lookup"><span data-stu-id="99e05-175">W</span></span>   | <span data-ttu-id="99e05-176">N/A</span><span class="sxs-lookup"><span data-stu-id="99e05-176">N/A</span></span>       | <span data-ttu-id="99e05-177">N/A</span><span class="sxs-lookup"><span data-stu-id="99e05-177">N/A</span></span>              | <span data-ttu-id="99e05-178">N/A</span><span class="sxs-lookup"><span data-stu-id="99e05-178">N/A</span></span>      | <span data-ttu-id="99e05-179">Non</span><span class="sxs-lookup"><span data-stu-id="99e05-179">No</span></span>           |
| <span data-ttu-id="99e05-180">sorties\#</span><span class="sxs-lookup"><span data-stu-id="99e05-180">o\#</span></span>      | <span data-ttu-id="99e05-181">Registre de sortie</span><span class="sxs-lookup"><span data-stu-id="99e05-181">Output Register</span></span> | <span data-ttu-id="99e05-182">32</span><span class="sxs-lookup"><span data-stu-id="99e05-182">32</span></span>    | <span data-ttu-id="99e05-183">W</span><span class="sxs-lookup"><span data-stu-id="99e05-183">W</span></span>   | <span data-ttu-id="99e05-184">N/A</span><span class="sxs-lookup"><span data-stu-id="99e05-184">N/A</span></span>       | <span data-ttu-id="99e05-185">N/A</span><span class="sxs-lookup"><span data-stu-id="99e05-185">N/A</span></span>              | <span data-ttu-id="99e05-186">4</span><span class="sxs-lookup"><span data-stu-id="99e05-186">4</span></span>        | <span data-ttu-id="99e05-187">Oui</span><span class="sxs-lookup"><span data-stu-id="99e05-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="99e05-188">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99e05-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99e05-189">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="99e05-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




