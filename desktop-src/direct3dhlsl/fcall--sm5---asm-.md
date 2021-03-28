---
title: FCALL (SM5-ASM)
description: Appel de fonction d’interface.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381221"
---
# <a name="fcall-sm5---asm"></a><span data-ttu-id="3427d-103">FCALL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="3427d-103">fcall (sm5 - asm)</span></span>

<span data-ttu-id="3427d-104">Appel de fonction d’interface.</span><span class="sxs-lookup"><span data-stu-id="3427d-104">Interface function call.</span></span>



| <span data-ttu-id="3427d-105">FCALL FP \# \[ arrayIndex \] \[ callSite\]</span><span class="sxs-lookup"><span data-stu-id="3427d-105">fcall fp\#\[arrayIndex\]\[callSite\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="3427d-106">Élément</span><span class="sxs-lookup"><span data-stu-id="3427d-106">Item</span></span>                                                                                                           | <span data-ttu-id="3427d-107">Description</span><span class="sxs-lookup"><span data-stu-id="3427d-107">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3427d-108"><span id="fp_"></span><span id="FP_"></span>*ép\#*</span><span class="sxs-lookup"><span data-stu-id="3427d-108"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/>                                                  | <span data-ttu-id="3427d-109">\[dans \] le pointeur de fonction.</span><span class="sxs-lookup"><span data-stu-id="3427d-109">\[in\] The function pointer.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3427d-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span><span class="sxs-lookup"><span data-stu-id="3427d-110"><span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*</span></span><br/> | <span data-ttu-id="3427d-111">\[\]facultatif.</span><span class="sxs-lookup"><span data-stu-id="3427d-111">\[in\] Optional.</span></span> <span data-ttu-id="3427d-112">Spécifie un décalage dans le tableau de pointeurs de fonction.</span><span class="sxs-lookup"><span data-stu-id="3427d-112">Specifies an offset into the function pointer array.</span></span> <span data-ttu-id="3427d-113">Ce paramètre doit être un entier non signé littéral si FP \# n’a pas été déclaré comme indexable.</span><span class="sxs-lookup"><span data-stu-id="3427d-113">This parameter must be a literal unsigned integer if fp\# was not declared as indexable.</span></span> <span data-ttu-id="3427d-114">Sinon, arrayIndex peut être de la forme littérale base + offset à partir d’un registre de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3427d-114">Otherwise, arrayIndex may be of the form literal base + offset from a shader register.</span></span> <span data-ttu-id="3427d-115">Par exemple, FCALL FP1 \[ R1. w + 0 \] \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="3427d-115">For example, fcall fp1\[r1.w + 0\]\[0\] .</span></span><br/> |
| <span data-ttu-id="3427d-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*callSite*</span><span class="sxs-lookup"><span data-stu-id="3427d-116"><span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span> *callSite*</span></span><br/>     | <span data-ttu-id="3427d-117">\[\]facultatif.</span><span class="sxs-lookup"><span data-stu-id="3427d-117">\[in\] Optional.</span></span> <span data-ttu-id="3427d-118">Offset d’entier non signé littéral dans la table de fonctions sélectionnée, en sélectionnant un corps \# de fonction FB à exécuter.</span><span class="sxs-lookup"><span data-stu-id="3427d-118">A literal unsigned integer offset into the selected function table, selecting a function body fb\# to execute.</span></span> <br/>                                                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="3427d-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3427d-119">Remarks</span></span>

<span data-ttu-id="3427d-120">*mode \# FP* \[  \] \[ arrayIndex \] correspond à une table de fonctions particulière, sélectionnée à partir de l’API en dehors du nuanceur, à partir des choix de la table de fonctions figurant dans la déclaration de *FP \#*.</span><span class="sxs-lookup"><span data-stu-id="3427d-120">*fp\#*\[*arrayIndex*\]\[\] resolves to a particular function table, selected from the API outside the shader from the function table choices listed in the declaration of *fp\#*.</span></span>

<span data-ttu-id="3427d-121">La somme de \# en *FP \#* et *arrayIndex* sélectionne la table de fonctions.</span><span class="sxs-lookup"><span data-stu-id="3427d-121">The sum of \# in *fp\#* and *arrayIndex* select the function table.</span></span> <span data-ttu-id="3427d-122">Par exemple, si une interface est déclarée en tant que FP4 \[ 4 \] \[ 3 \] (taille de tableau de 4), les **FCALL** s suivants sont équivalents : FCALL FP4 \[ 2 \] \[ 3 \] et FP5 \[ 1 \] \[ 3 \] , car 4 + 2 = 5 + 1.</span><span class="sxs-lookup"><span data-stu-id="3427d-122">For example, if an interface is declared as fp4\[4\]\[3\] (array size of 4), the following **fcall** s are equivalent: fcall fp4\[2\]\[3\] and fp5\[1\]\[3\], because 4+2 = 5+1.</span></span>

### <a name="restrictions"></a><span data-ttu-id="3427d-123">Restrictions</span><span class="sxs-lookup"><span data-stu-id="3427d-123">Restrictions</span></span>

-   <span data-ttu-id="3427d-124">Si *arrayIndex* utilise l’indexation dynamique, le comportement n’est pas défini si *arrayIndex* divergent sur les appels de nuanceur adjacents, qui pourraient s’exécuter dans échelons.</span><span class="sxs-lookup"><span data-stu-id="3427d-124">If *arrayIndex* uses dynamic indexing, behavior is undefined if *arrayIndex* diverges on adjacent shader invocations, which could be executing in lockstep.</span></span> <span data-ttu-id="3427d-125">Le compilateur HLSL tentera d’interdire ce cas de figure.</span><span class="sxs-lookup"><span data-stu-id="3427d-125">The HLSL compiler will attempt to disallow this case.</span></span>

    <span data-ttu-id="3427d-126">Les appels adjacents peuvent être inactifs en raison du contrôle de Flow, car il n’interrompt pas l’exécution de échelons.</span><span class="sxs-lookup"><span data-stu-id="3427d-126">Adjacent invocations can be inactive due to flow control, because it doesn t break lockstep execution.</span></span>

-   <span data-ttu-id="3427d-127">Si *FP \#*  +  *arrayIndex* spécifie un index hors limites, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="3427d-127">If *fp\#* + *arrayIndex* specifies an out of bounds index, behavior is undefined.</span></span>
-   <span data-ttu-id="3427d-128">Pour les cas non définis décrits ici, cela signifie que le comportement de l’appareil D3D actuel devient non défini, y compris la possibilité de perte de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3427d-128">For the undefined cases described here, it means the behavior of the current D3D device becomes undefined, including the possibility of Device Lost.</span></span> <span data-ttu-id="3427d-129">Toutefois, aucune mémoire en dehors de l’appareil D3D actif n’est accessible ou exécutée en tant que code.</span><span class="sxs-lookup"><span data-stu-id="3427d-129">However no memory outside the current D3D device will be accessed or executed as code.</span></span>

<span data-ttu-id="3427d-130">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="3427d-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3427d-131">Sommet</span><span class="sxs-lookup"><span data-stu-id="3427d-131">Vertex</span></span> | <span data-ttu-id="3427d-132">Forme</span><span class="sxs-lookup"><span data-stu-id="3427d-132">Hull</span></span> | <span data-ttu-id="3427d-133">Domain</span><span class="sxs-lookup"><span data-stu-id="3427d-133">Domain</span></span> | <span data-ttu-id="3427d-134">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3427d-134">Geometry</span></span> | <span data-ttu-id="3427d-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="3427d-135">Pixel</span></span> | <span data-ttu-id="3427d-136">Compute</span><span class="sxs-lookup"><span data-stu-id="3427d-136">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3427d-137">X</span><span class="sxs-lookup"><span data-stu-id="3427d-137">X</span></span>      | <span data-ttu-id="3427d-138">X</span><span class="sxs-lookup"><span data-stu-id="3427d-138">X</span></span>    | <span data-ttu-id="3427d-139">X</span><span class="sxs-lookup"><span data-stu-id="3427d-139">X</span></span>      | <span data-ttu-id="3427d-140">X</span><span class="sxs-lookup"><span data-stu-id="3427d-140">X</span></span>        | <span data-ttu-id="3427d-141">X</span><span class="sxs-lookup"><span data-stu-id="3427d-141">X</span></span>     | <span data-ttu-id="3427d-142">X</span><span class="sxs-lookup"><span data-stu-id="3427d-142">X</span></span>       |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="3427d-143">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3427d-143">Minimum Shader Model</span></span>

<span data-ttu-id="3427d-144">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="3427d-144">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="3427d-145">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3427d-145">Shader Model</span></span>                                              | <span data-ttu-id="3427d-146">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3427d-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3427d-147">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3427d-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3427d-148">Oui</span><span class="sxs-lookup"><span data-stu-id="3427d-148">yes</span></span>       |
| [<span data-ttu-id="3427d-149">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="3427d-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3427d-150">non</span><span class="sxs-lookup"><span data-stu-id="3427d-150">no</span></span>        |
| [<span data-ttu-id="3427d-151">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="3427d-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3427d-152">non</span><span class="sxs-lookup"><span data-stu-id="3427d-152">no</span></span>        |
| [<span data-ttu-id="3427d-153">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3427d-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3427d-154">non</span><span class="sxs-lookup"><span data-stu-id="3427d-154">no</span></span>        |
| [<span data-ttu-id="3427d-155">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3427d-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3427d-156">non</span><span class="sxs-lookup"><span data-stu-id="3427d-156">no</span></span>        |
| [<span data-ttu-id="3427d-157">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3427d-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3427d-158">non</span><span class="sxs-lookup"><span data-stu-id="3427d-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3427d-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3427d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3427d-160">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3427d-160">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





