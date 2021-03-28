---
title: Instruction for
description: Exécute itérativement une série d’instructions, en fonction de l’évaluation de l’expression conditionnelle.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- pour l’instruction HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100889"
---
# <a name="for-statement"></a><span data-ttu-id="5546a-104">Instruction for</span><span class="sxs-lookup"><span data-stu-id="5546a-104">for Statement</span></span>

<span data-ttu-id="5546a-105">Exécute itérativement une série d’instructions, en fonction de l’évaluation de l’expression conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="5546a-105">Iteratively executes a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                                                       |
|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5546a-106">\[*Attribut* \] pour ( *initialiseur ; Conditionnel Iterator* ) { *bloc d’instructions*;}</span><span class="sxs-lookup"><span data-stu-id="5546a-106">\[*Attribute*\] for ( *Initializer; Conditional; Iterator* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="5546a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5546a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5546a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*</span><span class="sxs-lookup"><span data-stu-id="5546a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="5546a-109">Paramètre facultatif qui contrôle la façon dont l’instruction est compilée.</span><span class="sxs-lookup"><span data-stu-id="5546a-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="5546a-110">Quand aucun attribut n’est spécifié, le compilateur tente d’abord d’émettre une version restaurée de la boucle, et en cas d’échec, ou si certaines opérations sont plus faciles si la boucle a été déroulée, revient à une version non terminée de la boucle.</span><span class="sxs-lookup"><span data-stu-id="5546a-110">When no attribute is specified the compiler will first attempt to emit a rolled version of the loop, and if that fails, or if some operations would be easier if the loop was unrolled, will fall back to an unrolled version of the loop.</span></span>



| <span data-ttu-id="5546a-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="5546a-111">Attribute</span></span>             | <span data-ttu-id="5546a-112">Description</span><span class="sxs-lookup"><span data-stu-id="5546a-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5546a-113">dérouler (x)</span><span class="sxs-lookup"><span data-stu-id="5546a-113">unroll(x)</span></span>             | <span data-ttu-id="5546a-114">Dérouler la boucle jusqu’à ce qu’elle cesse de s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="5546a-114">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="5546a-115">Peut éventuellement spécifier le nombre maximal de fois où la boucle doit s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="5546a-115">Can optionally specify the maximum number of times the loop is to execute.</span></span> <span data-ttu-id="5546a-116">Non compatible avec l’attribut de **\[ boucle \]** .</span><span class="sxs-lookup"><span data-stu-id="5546a-116">Not compatible with the **\[loop\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="5546a-117">loop</span><span class="sxs-lookup"><span data-stu-id="5546a-117">loop</span></span>                  | <span data-ttu-id="5546a-118">Générez du code qui utilise le contrôle de Flow pour exécuter chaque itération de la boucle.</span><span class="sxs-lookup"><span data-stu-id="5546a-118">Generate code that uses flow control to execute each iteration of the loop.</span></span> <span data-ttu-id="5546a-119">Non compatible avec l’attribut **\[ Unroll \]** .</span><span class="sxs-lookup"><span data-stu-id="5546a-119">Not compatible with the **\[unroll\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="5546a-120">fastopt</span><span class="sxs-lookup"><span data-stu-id="5546a-120">fastopt</span></span>               | <span data-ttu-id="5546a-121">Réduit le temps de compilation, mais produit des optimisations moins agressives.</span><span class="sxs-lookup"><span data-stu-id="5546a-121">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="5546a-122">Si vous utilisez cet attribut, le compilateur ne déroulera pas les boucles.</span><span class="sxs-lookup"><span data-stu-id="5546a-122">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="5546a-123">Cet attribut affecte uniquement les cibles de modèle Shader qui prennent en charge les instructions [break](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="5546a-123">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="5546a-124">Cet attribut est disponible dans le modèle de nuanceur [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) et le [nuanceur modèle 3](dx-graphics-hlsl-sm3.md) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5546a-124">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="5546a-125">Elle est particulièrement utile dans le [nuanceur modèle 4](dx-graphics-hlsl-sm4.md) et versions ultérieures lorsque le compilateur compile des boucles.</span><span class="sxs-lookup"><span data-stu-id="5546a-125">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="5546a-126">Le compilateur simule par défaut des boucles pour déterminer s’il peut les dérouler.</span><span class="sxs-lookup"><span data-stu-id="5546a-126">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="5546a-127">Si vous ne souhaitez pas que le compilateur dérouler les boucles, utilisez cet attribut pour réduire le temps de compilation.</span><span class="sxs-lookup"><span data-stu-id="5546a-127">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span> <br/> |
| <span data-ttu-id="5546a-128">autoriser \_ la \_ condition UAV</span><span class="sxs-lookup"><span data-stu-id="5546a-128">allow\_uav\_condition</span></span> | <span data-ttu-id="5546a-129">Permet à une condition d’arrêt de boucle Compute Shader de se baser sur une lecture UAV.</span><span class="sxs-lookup"><span data-stu-id="5546a-129">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="5546a-130">La boucle ne doit pas contenir d’intrinsèques de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="5546a-130">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="5546a-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initialiseur*</span><span class="sxs-lookup"><span data-stu-id="5546a-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span></span>
</dt> <dd>

<span data-ttu-id="5546a-132">Valeur initiale du compteur de boucle.</span><span class="sxs-lookup"><span data-stu-id="5546a-132">The initial value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="5546a-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditionnel*</span><span class="sxs-lookup"><span data-stu-id="5546a-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="5546a-134">[Expression](dx-graphics-hlsl-expressions.md)conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="5546a-134">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="5546a-135">Si l’expression conditionnelle prend la valeur true, le bloc d’instructions est exécuté.</span><span class="sxs-lookup"><span data-stu-id="5546a-135">If the conditional expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="5546a-136">La boucle se termine lorsque l’expression prend la valeur false.</span><span class="sxs-lookup"><span data-stu-id="5546a-136">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="5546a-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Répétiteur*</span><span class="sxs-lookup"><span data-stu-id="5546a-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span></span>
</dt> <dd>

<span data-ttu-id="5546a-138">Mettez à jour la valeur du compteur de boucle.</span><span class="sxs-lookup"><span data-stu-id="5546a-138">Update the value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="5546a-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloc d’instructions*</span><span class="sxs-lookup"><span data-stu-id="5546a-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="5546a-140">Une ou plusieurs [instructions HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="5546a-140">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5546a-141">Notes</span><span class="sxs-lookup"><span data-stu-id="5546a-141">Remarks</span></span>

<span data-ttu-id="5546a-142">Les attributs de **\[ boucle \]** et de **\[ déroulabilité \]** s’excluent mutuellement et génèrent des erreurs de compilation lorsque les deux sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="5546a-142">The **\[unroll\]** and **\[loop\]** attributes are mutually exclusive and will generate compiler errors when both are specified.</span></span>

<span data-ttu-id="5546a-143">Les attributs de **\[ \_ \_ condition \]** **\[ \] fastopt** et allow UAV sont ignorés si **\[ Unroll \]** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="5546a-143">The **\[fastopt\]** and **\[allow\_uav\_condition\]** attributes are ignored if **\[unroll\]** is specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="5546a-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5546a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5546a-145">Contrôle de Flow</span><span class="sxs-lookup"><span data-stu-id="5546a-145">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





