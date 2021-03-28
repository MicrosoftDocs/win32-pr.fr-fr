---
title: Registres-vs_4_0
description: Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de sommets version 4 \_ 0.
ms.assetid: f471df6a-06f6-4783-ba8f-cf0a3b43727f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 425fc4174b1c4a103fc7db15b5f05ae2b6dd95e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990616"
---
# <a name="registers---vs_4_0"></a><span data-ttu-id="c6ec8-103">Registres-vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c6ec8-103">Registers - vs\_4\_0</span></span>

<span data-ttu-id="c6ec8-104">Cette section contient des informations de référence pour les registres d’entrée et de sortie implémentés par le nuanceur de sommets version 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="c6ec8-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_0.</span></span>

## <a name="input-registers"></a><span data-ttu-id="c6ec8-105">Registres d’entrée</span><span class="sxs-lookup"><span data-stu-id="c6ec8-105">Input Registers</span></span>



| <span data-ttu-id="c6ec8-106">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="c6ec8-106">Register</span></span>      | <span data-ttu-id="c6ec8-107">Nom</span><span class="sxs-lookup"><span data-stu-id="c6ec8-107">Name</span></span> | <span data-ttu-id="c6ec8-108">Count</span><span class="sxs-lookup"><span data-stu-id="c6ec8-108">Count</span></span>              | <span data-ttu-id="c6ec8-109">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="c6ec8-109">R/W</span></span> | <span data-ttu-id="c6ec8-110">Dimension</span><span class="sxs-lookup"><span data-stu-id="c6ec8-110">Dimension</span></span> | <span data-ttu-id="c6ec8-111">Indexable par r\#</span><span class="sxs-lookup"><span data-stu-id="c6ec8-111">Indexable by r\#</span></span> | <span data-ttu-id="c6ec8-112">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="c6ec8-112">Defaults</span></span> | <span data-ttu-id="c6ec8-113">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="c6ec8-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="c6ec8-114">r\#</span><span class="sxs-lookup"><span data-stu-id="c6ec8-114">r\#</span></span>           |      | <span data-ttu-id="c6ec8-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="c6ec8-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="c6ec8-116">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="c6ec8-116">R/W</span></span> | <span data-ttu-id="c6ec8-117">4</span><span class="sxs-lookup"><span data-stu-id="c6ec8-117">4</span></span>         | <span data-ttu-id="c6ec8-118">Non</span><span class="sxs-lookup"><span data-stu-id="c6ec8-118">No</span></span>               | <span data-ttu-id="c6ec8-119">None</span><span class="sxs-lookup"><span data-stu-id="c6ec8-119">None</span></span>     | <span data-ttu-id="c6ec8-120">Oui</span><span class="sxs-lookup"><span data-stu-id="c6ec8-120">Yes</span></span>          |
| <span data-ttu-id="c6ec8-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="c6ec8-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="c6ec8-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="c6ec8-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="c6ec8-123">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="c6ec8-123">R/W</span></span> | <span data-ttu-id="c6ec8-124">4</span><span class="sxs-lookup"><span data-stu-id="c6ec8-124">4</span></span>         | <span data-ttu-id="c6ec8-125">Oui</span><span class="sxs-lookup"><span data-stu-id="c6ec8-125">Yes</span></span>              | <span data-ttu-id="c6ec8-126">None</span><span class="sxs-lookup"><span data-stu-id="c6ec8-126">None</span></span>     | <span data-ttu-id="c6ec8-127">Oui</span><span class="sxs-lookup"><span data-stu-id="c6ec8-127">Yes</span></span>          |
| <span data-ttu-id="c6ec8-128">v\#</span><span class="sxs-lookup"><span data-stu-id="c6ec8-128">v\#</span></span>           |      | <span data-ttu-id="c6ec8-129">16</span><span class="sxs-lookup"><span data-stu-id="c6ec8-129">16</span></span>                 | <span data-ttu-id="c6ec8-130">R</span><span class="sxs-lookup"><span data-stu-id="c6ec8-130">R</span></span>   | <span data-ttu-id="c6ec8-131">4</span><span class="sxs-lookup"><span data-stu-id="c6ec8-131">4</span></span>         | <span data-ttu-id="c6ec8-132">Oui</span><span class="sxs-lookup"><span data-stu-id="c6ec8-132">Yes</span></span>              | <span data-ttu-id="c6ec8-133">None</span><span class="sxs-lookup"><span data-stu-id="c6ec8-133">None</span></span>     | <span data-ttu-id="c6ec8-134">Oui</span><span class="sxs-lookup"><span data-stu-id="c6ec8-134">Yes</span></span>          |
| <span data-ttu-id="c6ec8-135">t\#</span><span class="sxs-lookup"><span data-stu-id="c6ec8-135">t\#</span></span>           |      | <span data-ttu-id="c6ec8-136">128</span><span class="sxs-lookup"><span data-stu-id="c6ec8-136">128</span></span>                | <span data-ttu-id="c6ec8-137">R</span><span class="sxs-lookup"><span data-stu-id="c6ec8-137">R</span></span>   | <span data-ttu-id="c6ec8-138">1</span><span class="sxs-lookup"><span data-stu-id="c6ec8-138">1</span></span>         | <span data-ttu-id="c6ec8-139">Non</span><span class="sxs-lookup"><span data-stu-id="c6ec8-139">No</span></span>               | <span data-ttu-id="c6ec8-140">None</span><span class="sxs-lookup"><span data-stu-id="c6ec8-140">None</span></span>     | <span data-ttu-id="c6ec8-141">Oui</span><span class="sxs-lookup"><span data-stu-id="c6ec8-141">Yes</span></span>          |
| <span data-ttu-id="c6ec8-142">s\#</span><span class="sxs-lookup"><span data-stu-id="c6ec8-142">s\#</span></span>           |      | <span data-ttu-id="c6ec8-143">16</span><span class="sxs-lookup"><span data-stu-id="c6ec8-143">16</span></span>                 | <span data-ttu-id="c6ec8-144">R</span><span class="sxs-lookup"><span data-stu-id="c6ec8-144">R</span></span>   | <span data-ttu-id="c6ec8-145">1</span><span class="sxs-lookup"><span data-stu-id="c6ec8-145">1</span></span>         | <span data-ttu-id="c6ec8-146">Non</span><span class="sxs-lookup"><span data-stu-id="c6ec8-146">No</span></span>               | <span data-ttu-id="c6ec8-147">None</span><span class="sxs-lookup"><span data-stu-id="c6ec8-147">None</span></span>     | <span data-ttu-id="c6ec8-148">Oui</span><span class="sxs-lookup"><span data-stu-id="c6ec8-148">Yes</span></span>          |
| <span data-ttu-id="c6ec8-149">\# \[ index CB\]</span><span class="sxs-lookup"><span data-stu-id="c6ec8-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="c6ec8-150">15</span><span class="sxs-lookup"><span data-stu-id="c6ec8-150">15</span></span>                 | <span data-ttu-id="c6ec8-151">R</span><span class="sxs-lookup"><span data-stu-id="c6ec8-151">R</span></span>   | <span data-ttu-id="c6ec8-152">4</span><span class="sxs-lookup"><span data-stu-id="c6ec8-152">4</span></span>         | <span data-ttu-id="c6ec8-153">Oui (contenu)</span><span class="sxs-lookup"><span data-stu-id="c6ec8-153">Yes(Contents)</span></span>    | <span data-ttu-id="c6ec8-154">Aucun</span><span class="sxs-lookup"><span data-stu-id="c6ec8-154">None</span></span>     | <span data-ttu-id="c6ec8-155">Oui</span><span class="sxs-lookup"><span data-stu-id="c6ec8-155">Yes</span></span>          |
| <span data-ttu-id="c6ec8-156">\[index ICB\]</span><span class="sxs-lookup"><span data-stu-id="c6ec8-156">icb\[index\]</span></span>  |      | <span data-ttu-id="c6ec8-157">1</span><span class="sxs-lookup"><span data-stu-id="c6ec8-157">1</span></span>                  | <span data-ttu-id="c6ec8-158">R</span><span class="sxs-lookup"><span data-stu-id="c6ec8-158">R</span></span>   | <span data-ttu-id="c6ec8-159">4</span><span class="sxs-lookup"><span data-stu-id="c6ec8-159">4</span></span>         | <span data-ttu-id="c6ec8-160">Oui (contenu)</span><span class="sxs-lookup"><span data-stu-id="c6ec8-160">Yes(Contents)</span></span>    | <span data-ttu-id="c6ec8-161">Aucun</span><span class="sxs-lookup"><span data-stu-id="c6ec8-161">None</span></span>     | <span data-ttu-id="c6ec8-162">Oui</span><span class="sxs-lookup"><span data-stu-id="c6ec8-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="c6ec8-163">Registres de sortie</span><span class="sxs-lookup"><span data-stu-id="c6ec8-163">Output Registers</span></span>



| <span data-ttu-id="c6ec8-164">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="c6ec8-164">Register</span></span> | <span data-ttu-id="c6ec8-165">Nom</span><span class="sxs-lookup"><span data-stu-id="c6ec8-165">Name</span></span>            | <span data-ttu-id="c6ec8-166">Count</span><span class="sxs-lookup"><span data-stu-id="c6ec8-166">Count</span></span> | <span data-ttu-id="c6ec8-167">R/W (Lecture/écriture)</span><span class="sxs-lookup"><span data-stu-id="c6ec8-167">R/W</span></span> | <span data-ttu-id="c6ec8-168">Dimension</span><span class="sxs-lookup"><span data-stu-id="c6ec8-168">Dimension</span></span> | <span data-ttu-id="c6ec8-169">Indexable par r\#</span><span class="sxs-lookup"><span data-stu-id="c6ec8-169">Indexable by r\#</span></span> | <span data-ttu-id="c6ec8-170">Valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="c6ec8-170">Defaults</span></span> | <span data-ttu-id="c6ec8-171">DCL obligatoire</span><span class="sxs-lookup"><span data-stu-id="c6ec8-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="c6ec8-172">NULL</span><span class="sxs-lookup"><span data-stu-id="c6ec8-172">NULL</span></span>     | <span data-ttu-id="c6ec8-173">Ignorer le résultat</span><span class="sxs-lookup"><span data-stu-id="c6ec8-173">Discard Result</span></span>  | <span data-ttu-id="c6ec8-174">N/A</span><span class="sxs-lookup"><span data-stu-id="c6ec8-174">N/A</span></span>   | <span data-ttu-id="c6ec8-175">W</span><span class="sxs-lookup"><span data-stu-id="c6ec8-175">W</span></span>   | <span data-ttu-id="c6ec8-176">N/A</span><span class="sxs-lookup"><span data-stu-id="c6ec8-176">N/A</span></span>       | <span data-ttu-id="c6ec8-177">N/A</span><span class="sxs-lookup"><span data-stu-id="c6ec8-177">N/A</span></span>              | <span data-ttu-id="c6ec8-178">N/A</span><span class="sxs-lookup"><span data-stu-id="c6ec8-178">N/A</span></span>      | <span data-ttu-id="c6ec8-179">Non</span><span class="sxs-lookup"><span data-stu-id="c6ec8-179">No</span></span>           |
| <span data-ttu-id="c6ec8-180">sorties\#</span><span class="sxs-lookup"><span data-stu-id="c6ec8-180">o\#</span></span>      | <span data-ttu-id="c6ec8-181">Registre de sortie</span><span class="sxs-lookup"><span data-stu-id="c6ec8-181">Output Register</span></span> | <span data-ttu-id="c6ec8-182">16</span><span class="sxs-lookup"><span data-stu-id="c6ec8-182">16</span></span>    | <span data-ttu-id="c6ec8-183">W</span><span class="sxs-lookup"><span data-stu-id="c6ec8-183">W</span></span>   | <span data-ttu-id="c6ec8-184">N/A</span><span class="sxs-lookup"><span data-stu-id="c6ec8-184">N/A</span></span>       | <span data-ttu-id="c6ec8-185">N/A</span><span class="sxs-lookup"><span data-stu-id="c6ec8-185">N/A</span></span>              | <span data-ttu-id="c6ec8-186">4</span><span class="sxs-lookup"><span data-stu-id="c6ec8-186">4</span></span>        | <span data-ttu-id="c6ec8-187">Oui</span><span class="sxs-lookup"><span data-stu-id="c6ec8-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="c6ec8-188">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c6ec8-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6ec8-189">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="c6ec8-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




