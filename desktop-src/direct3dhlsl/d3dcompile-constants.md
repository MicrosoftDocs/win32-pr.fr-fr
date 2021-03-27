---
title: Constantes D3DCOMPILE (D3DCompiler. h)
description: Les constantes D3DCOMPILE spécifient la façon dont le compilateur compile le code HLSL.
ms.assetid: 039627DD-D6A4-4EA3-8E91-D2A20770E6FF
topic_type:
- apiref
api_name:
- D3DCOMPILE_DEBUG
- D3DCOMPILE_SKIP_VALIDATION
- D3DCOMPILE_SKIP_OPTIMIZATION
- D3DCOMPILE_PACK_MATRIX_ROW_MAJOR
- D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR
- D3DCOMPILE_PARTIAL_PRECISION
- D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT
- D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT
- D3DCOMPILE_NO_PRESHADER
- D3DCOMPILE_AVOID_FLOW_CONTROL
- D3DCOMPILE_PREFER_FLOW_CONTROL
- D3DCOMPILE_ENABLE_STRICTNESS
- D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY
- D3DCOMPILE_IEEE_STRICTNESS
- D3DCOMPILE_OPTIMIZATION_LEVEL0
- D3DCOMPILE_OPTIMIZATION_LEVEL1
- D3DCOMPILE_OPTIMIZATION_LEVEL2
- D3DCOMPILE_OPTIMIZATION_LEVEL3
- D3DCOMPILE_WARNINGS_ARE_ERRORS
- D3DCOMPILE_RESOURCES_MAY_ALIAS
- D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES
- D3DCOMPILE_ALL_RESOURCES_BOUND
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfd396eef06260ae879a3bb816d0bd89a078ea53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211701"
---
# <a name="d3dcompile-constants"></a><span data-ttu-id="dc566-103">Constantes D3DCOMPILE</span><span class="sxs-lookup"><span data-stu-id="dc566-103">D3DCOMPILE Constants</span></span>

<span data-ttu-id="dc566-104">Les constantes D3DCOMPILE spécifient la façon dont le compilateur compile le code HLSL.</span><span class="sxs-lookup"><span data-stu-id="dc566-104">The D3DCOMPILE constants specify how the compiler compiles the HLSL code.</span></span>

<dl> <dt>

<span data-ttu-id="dc566-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**Débogage D3DCOMPILE \_**</span><span class="sxs-lookup"><span data-stu-id="dc566-105"><span id="D3DCOMPILE_DEBUG"></span><span id="d3dcompile_debug"></span>**D3DCOMPILE\_DEBUG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="dc566-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-107">Indique au compilateur d’insérer les informations de fichier de débogage/ligne/type/symbole dans le code de sortie.</span><span class="sxs-lookup"><span data-stu-id="dc566-107">Directs the compiler to insert debug file/line/type/symbol information into the output code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE \_ ignorer la \_ validation**</span><span class="sxs-lookup"><span data-stu-id="dc566-108"><span id="D3DCOMPILE_SKIP_VALIDATION"></span><span id="d3dcompile_skip_validation"></span>**D3DCOMPILE\_SKIP\_VALIDATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-109">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="dc566-109">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-110">Indique au compilateur de ne pas valider le code généré par rapport aux capacités et contraintes connues.</span><span class="sxs-lookup"><span data-stu-id="dc566-110">Directs the compiler not to validate the generated code against known capabilities and constraints.</span></span> <span data-ttu-id="dc566-111">Nous vous recommandons d’utiliser cette constante uniquement avec les nuanceurs qui ont été compilés avec succès par le passé.</span><span class="sxs-lookup"><span data-stu-id="dc566-111">We recommend that you use this constant only with shaders that have been successfully compiled in the past.</span></span> <span data-ttu-id="dc566-112">DirectX valide toujours les nuanceurs avant de les définir sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="dc566-112">DirectX always validates shaders before it sets them to a device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE \_ ignorer l' \_ optimisation**</span><span class="sxs-lookup"><span data-stu-id="dc566-113"><span id="D3DCOMPILE_SKIP_OPTIMIZATION"></span><span id="d3dcompile_skip_optimization"></span>**D3DCOMPILE\_SKIP\_OPTIMIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-114">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="dc566-114">(1 << 2)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-115">Indique au compilateur d’ignorer les étapes d’optimisation pendant la génération de code.</span><span class="sxs-lookup"><span data-stu-id="dc566-115">Directs the compiler to skip optimization steps during code generation.</span></span> <span data-ttu-id="dc566-116">Nous vous recommandons de définir cette constante uniquement à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="dc566-116">We recommend that you set this constant for debug purposes only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**\_ \_ \_ Colonne \_ principale de la matrice D3DCOMPILE Pack**</span><span class="sxs-lookup"><span data-stu-id="dc566-117"><span id="D3DCOMPILE_PACK_MATRIX_ROW_MAJOR"></span><span id="d3dcompile_pack_matrix_row_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_ROW\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-118">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="dc566-118">(1 << 3)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-119">Indique au compilateur d’empaqueter les matrices dans l’ordre ligne-principal de l’entrée et de la sortie du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="dc566-119">Directs the compiler to pack matrices in row-major order on input and output from the shader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**\_ \_ \_ Colonne \_ principale de la matrice D3DCOMPILE Pack**</span><span class="sxs-lookup"><span data-stu-id="dc566-120"><span id="D3DCOMPILE_PACK_MATRIX_COLUMN_MAJOR"></span><span id="d3dcompile_pack_matrix_column_major"></span>**D3DCOMPILE\_PACK\_MATRIX\_COLUMN\_MAJOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-121">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="dc566-121">(1 << 4)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-122">Indique au compilateur d’empaqueter les matrices dans l’ordre des colonnes-major sur l’entrée et la sortie du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="dc566-122">Directs the compiler to pack matrices in column-major order on input and output from the shader.</span></span> <span data-ttu-id="dc566-123">Ce type de compression est généralement plus efficace, car une série de produits scalaires peut ensuite effectuer une multiplication de matrice vectorielle.</span><span class="sxs-lookup"><span data-stu-id="dc566-123">This type of packing is generally more efficient because a series of dot-products can then perform vector-matrix multiplication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**\_Précision partielle \_ D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="dc566-124"><span id="D3DCOMPILE_PARTIAL_PRECISION"></span><span id="d3dcompile_partial_precision"></span>**D3DCOMPILE\_PARTIAL\_PRECISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-125">(1 << 5)</span><span class="sxs-lookup"><span data-stu-id="dc566-125">(1 << 5)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-126">Indique au compilateur d’effectuer tous les calculs avec une précision partielle.</span><span class="sxs-lookup"><span data-stu-id="dc566-126">Directs the compiler to perform all computations with partial precision.</span></span> <span data-ttu-id="dc566-127">Si vous définissez cette constante, le code compilé peut s’exécuter plus rapidement sur du matériel.</span><span class="sxs-lookup"><span data-stu-id="dc566-127">If you set this constant, the compiled code might run faster on some hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE \_ force \_ / \_ logiciel \_ non \_ opt**</span><span class="sxs-lookup"><span data-stu-id="dc566-128"><span id="D3DCOMPILE_FORCE_VS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_vs_software_no_opt"></span>**D3DCOMPILE\_FORCE\_VS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-129">(1 << 6)</span><span class="sxs-lookup"><span data-stu-id="dc566-129">(1 << 6)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-130">Indique au compilateur de compiler un nuanceur de sommets pour le profil de nuanceur le plus élevé suivant.</span><span class="sxs-lookup"><span data-stu-id="dc566-130">Directs the compiler to compile a vertex shader for the next highest shader profile.</span></span> <span data-ttu-id="dc566-131">Cette constante désactive le débogage et les optimisations.</span><span class="sxs-lookup"><span data-stu-id="dc566-131">This constant turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE \_ forcer \_ le \_ logiciel PS \_ non \_ opt**</span><span class="sxs-lookup"><span data-stu-id="dc566-132"><span id="D3DCOMPILE_FORCE_PS_SOFTWARE_NO_OPT"></span><span id="d3dcompile_force_ps_software_no_opt"></span>**D3DCOMPILE\_FORCE\_PS\_SOFTWARE\_NO\_OPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-133">(1 << 7)</span><span class="sxs-lookup"><span data-stu-id="dc566-133">(1 << 7)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-134">Indique au compilateur de compiler un nuanceur de pixels pour le profil de nuanceur suivant le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="dc566-134">Directs the compiler to compile a pixel shader for the next highest shader profile.</span></span> <span data-ttu-id="dc566-135">Cette constante désactive également le débogage et les optimisations.</span><span class="sxs-lookup"><span data-stu-id="dc566-135">This constant also turns debugging on and optimizations off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE \_ aucun \_ prénuanceur**</span><span class="sxs-lookup"><span data-stu-id="dc566-136"><span id="D3DCOMPILE_NO_PRESHADER"></span><span id="d3dcompile_no_preshader"></span>**D3DCOMPILE\_NO\_PRESHADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-137">(1 << 8)</span><span class="sxs-lookup"><span data-stu-id="dc566-137">(1 << 8)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-138">Indique au compilateur de désactiver les prénuanceurs.</span><span class="sxs-lookup"><span data-stu-id="dc566-138">Directs the compiler to disable Preshaders.</span></span> <span data-ttu-id="dc566-139">Si vous définissez cette constante, le compilateur n’extrait pas l’expression statique à des fins d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="dc566-139">If you set this constant, the compiler does not pull out static expression for evaluation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE \_ éviter \_ \_ le contrôle de workflow**</span><span class="sxs-lookup"><span data-stu-id="dc566-140"><span id="D3DCOMPILE_AVOID_FLOW_CONTROL"></span><span id="d3dcompile_avoid_flow_control"></span>**D3DCOMPILE\_AVOID\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-141">(1 << 9)</span><span class="sxs-lookup"><span data-stu-id="dc566-141">(1 << 9)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-142">Indique au compilateur de ne pas utiliser les constructions de contrôle de Flow dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="dc566-142">Directs the compiler to not use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE \_ préférer \_ \_ le contrôle de Flow**</span><span class="sxs-lookup"><span data-stu-id="dc566-143"><span id="D3DCOMPILE_PREFER_FLOW_CONTROL"></span><span id="d3dcompile_prefer_flow_control"></span>**D3DCOMPILE\_PREFER\_FLOW\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-144">(1 << 10)</span><span class="sxs-lookup"><span data-stu-id="dc566-144">(1 << 10)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-145">Indique au compilateur d’utiliser des constructions de contrôle de Flow dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="dc566-145">Directs the compiler to use flow-control constructs where possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE \_ activer la \_ rigueur**</span><span class="sxs-lookup"><span data-stu-id="dc566-146"><span id="D3DCOMPILE_ENABLE_STRICTNESS"></span><span id="d3dcompile_enable_strictness"></span>**D3DCOMPILE\_ENABLE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-147">(1 << 11)</span><span class="sxs-lookup"><span data-stu-id="dc566-147">(1 << 11)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-148">Force la compilation stricte, qui peut ne pas autoriser la syntaxe héritée.</span><span class="sxs-lookup"><span data-stu-id="dc566-148">Forces strict compile, which might not allow for legacy syntax.</span></span>

<span data-ttu-id="dc566-149">Par défaut, le compilateur désactive la rigueur sur la syntaxe déconseillée.</span><span class="sxs-lookup"><span data-stu-id="dc566-149">By default, the compiler disables strictness on deprecated syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE \_ activer la \_ compatibilité descendante \_**</span><span class="sxs-lookup"><span data-stu-id="dc566-150"><span id="D3DCOMPILE_ENABLE_BACKWARDS_COMPATIBILITY"></span><span id="d3dcompile_enable_backwards_compatibility"></span>**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-151">(1 << 12)</span><span class="sxs-lookup"><span data-stu-id="dc566-151">(1 << 12)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-152">Indique au compilateur d’activer les nuanceurs plus anciens pour compiler sur des cibles de 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="dc566-152">Directs the compiler to enable older shaders to compile to 5\_0 targets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE \_ IEEE \_ strict**</span><span class="sxs-lookup"><span data-stu-id="dc566-153"><span id="D3DCOMPILE_IEEE_STRICTNESS"></span><span id="d3dcompile_ieee_strictness"></span>**D3DCOMPILE\_IEEE\_STRICTNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-154">(1 << 13)</span><span class="sxs-lookup"><span data-stu-id="dc566-154">(1 << 13)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-155">Force la compilation stricte de la norme IEEE.</span><span class="sxs-lookup"><span data-stu-id="dc566-155">Forces the IEEE strict compile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**\_Niveau0 d’optimisation D3DCOMPILE \_**</span><span class="sxs-lookup"><span data-stu-id="dc566-156"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL0"></span><span id="d3dcompile_optimization_level0"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-157">(1 << 14)</span><span class="sxs-lookup"><span data-stu-id="dc566-157">(1 << 14)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-158">Indique au compilateur d’utiliser le niveau d’optimisation le plus bas.</span><span class="sxs-lookup"><span data-stu-id="dc566-158">Directs the compiler to use the lowest optimization level.</span></span> <span data-ttu-id="dc566-159">Si vous définissez cette constante, le compilateur peut générer du code plus lent, mais produit le code plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="dc566-159">If you set this constant, the compiler might produce slower code but produces the code more quickly.</span></span> <span data-ttu-id="dc566-160">Définissez cette constante lorsque vous développez le nuanceur de manière itérative.</span><span class="sxs-lookup"><span data-stu-id="dc566-160">Set this constant when you develop the shader iteratively.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE \_ optimisation du \_ niveau1**</span><span class="sxs-lookup"><span data-stu-id="dc566-161"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL1"></span><span id="d3dcompile_optimization_level1"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-162">0</span><span class="sxs-lookup"><span data-stu-id="dc566-162">0</span></span>
</dt> <dt>



<span data-ttu-id="dc566-163">Indique au compilateur d’utiliser le deuxième niveau d’optimisation le plus bas.</span><span class="sxs-lookup"><span data-stu-id="dc566-163">Directs the compiler to use the second lowest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE d' \_ optimisation du \_ d’isolement2**</span><span class="sxs-lookup"><span data-stu-id="dc566-164"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL2"></span><span id="d3dcompile_optimization_level2"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-165">((1 << 14) \| (1 << 15))</span><span class="sxs-lookup"><span data-stu-id="dc566-165">((1 << 14) \| (1 << 15))</span></span>
</dt> <dt>



<span data-ttu-id="dc566-166">Indique au compilateur d’utiliser le deuxième niveau d’optimisation le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="dc566-166">Directs the compiler to use the second highest optimization level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**\_Niveau3 d’optimisation D3DCOMPILE \_**</span><span class="sxs-lookup"><span data-stu-id="dc566-167"><span id="D3DCOMPILE_OPTIMIZATION_LEVEL3"></span><span id="d3dcompile_optimization_level3"></span>**D3DCOMPILE\_OPTIMIZATION\_LEVEL3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-168">(1 << 15)</span><span class="sxs-lookup"><span data-stu-id="dc566-168">(1 << 15)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-169">Indique au compilateur d’utiliser le niveau d’optimisation le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="dc566-169">Directs the compiler to use the highest optimization level.</span></span> <span data-ttu-id="dc566-170">Si vous définissez cette constante, le compilateur produit le meilleur code possible, mais peut prendre beaucoup plus de temps.</span><span class="sxs-lookup"><span data-stu-id="dc566-170">If you set this constant, the compiler produces the best possible code but might take significantly longer to do so.</span></span> <span data-ttu-id="dc566-171">Définissez cette constante pour les versions finales d’une application lorsque les performances sont le facteur le plus important.</span><span class="sxs-lookup"><span data-stu-id="dc566-171">Set this constant for final builds of an application when performance is the most important factor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**\_Les avertissements D3DCOMPILE \_ sont des \_ Erreurs**</span><span class="sxs-lookup"><span data-stu-id="dc566-172"><span id="D3DCOMPILE_WARNINGS_ARE_ERRORS"></span><span id="d3dcompile_warnings_are_errors"></span>**D3DCOMPILE\_WARNINGS\_ARE\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-173">(1 << 18)</span><span class="sxs-lookup"><span data-stu-id="dc566-173">(1 << 18)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-174">Indique au compilateur de traiter tous les avertissements comme des erreurs lors de la compilation du code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="dc566-174">Directs the compiler to treat all warnings as errors when it compiles the shader code.</span></span> <span data-ttu-id="dc566-175">Nous vous recommandons d’utiliser cette constante pour le nouveau code de nuanceur, afin de pouvoir résoudre tous les avertissements et réduire le nombre de défauts de code difficiles à trouver.</span><span class="sxs-lookup"><span data-stu-id="dc566-175">We recommend that you use this constant for new shader code, so that you can resolve all warnings and lower the number of hard-to-find code defects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**Les \_ ressources D3DCOMPILE \_ peuvent avoir un \_ alias**</span><span class="sxs-lookup"><span data-stu-id="dc566-176"><span id="D3DCOMPILE_RESOURCES_MAY_ALIAS"></span><span id="d3dcompile_resources_may_alias"></span>**D3DCOMPILE\_RESOURCES\_MAY\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-177">(1 << 19)</span><span class="sxs-lookup"><span data-stu-id="dc566-177">(1 << 19)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-178">Indique au compilateur de supposer que les vues d’accès non ordonnées (UAVs) et les vues des ressources de nuanceur (SRVs) peuvent avoir un alias pour CS \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="dc566-178">Directs the compiler to assume that unordered access views (UAVs) and shader resource views (SRVs) may alias for cs\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="dc566-179">Cette constante de compilateur est nouvelle à partir de la \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="dc566-179">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE \_ activer les \_ tables de \_ descripteurs non liées \_**</span><span class="sxs-lookup"><span data-stu-id="dc566-180"><span id="D3DCOMPILE_ENABLE_UNBOUNDED_DESCRIPTOR_TABLES"></span><span id="d3dcompile_enable_unbounded_descriptor_tables"></span>**D3DCOMPILE\_ENABLE\_UNBOUNDED\_DESCRIPTOR\_TABLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-181">(1 << 20)</span><span class="sxs-lookup"><span data-stu-id="dc566-181">(1 << 20)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-182">Indique au compilateur d’activer les tables de descripteurs non liées.</span><span class="sxs-lookup"><span data-stu-id="dc566-182">Directs the compiler to enable unbounded descriptor tables.</span></span>

> [!Note]  
> <span data-ttu-id="dc566-183">Cette constante de compilateur est nouvelle à partir de la \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="dc566-183">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="dc566-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE \_ toutes les \_ ressources \_ liées**</span><span class="sxs-lookup"><span data-stu-id="dc566-184"><span id="D3DCOMPILE_ALL_RESOURCES_BOUND"></span><span id="d3dcompile_all_resources_bound"></span>**D3DCOMPILE\_ALL\_RESOURCES\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc566-185">(1 << 21)</span><span class="sxs-lookup"><span data-stu-id="dc566-185">(1 << 21)</span></span>
</dt> <dt>



<span data-ttu-id="dc566-186">Indique au compilateur de s’assurer que toutes les ressources sont liées.</span><span class="sxs-lookup"><span data-stu-id="dc566-186">Directs the compiler to ensure all resources are bound.</span></span>

> [!Note]  
> <span data-ttu-id="dc566-187">Cette constante de compilateur est nouvelle à partir de la \_47.dll D3dcompiler.</span><span class="sxs-lookup"><span data-stu-id="dc566-187">This compiler constant is new starting with the D3dcompiler\_47.dll.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc566-188">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dc566-188">Requirements</span></span>



| <span data-ttu-id="dc566-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc566-189">Requirement</span></span> | <span data-ttu-id="dc566-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc566-190">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc566-191">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc566-191">Header</span></span><br/> | <dl> <span data-ttu-id="dc566-192"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc566-192"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc566-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc566-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc566-194">Constantes D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="dc566-194">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

 





