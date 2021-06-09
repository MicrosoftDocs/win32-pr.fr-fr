---
title: Instruction while
description: Exécute un bloc d’instructions jusqu’à ce que l’expression conditionnelle échoue.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- while, instruction HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bf1f0049ac474e7840753a8cfe05c972aa346c1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826672"
---
# <a name="while-statement"></a><span data-ttu-id="e171f-104">Instruction while</span><span class="sxs-lookup"><span data-stu-id="e171f-104">while Statement</span></span>

<span data-ttu-id="e171f-105">Exécute un bloc d’instructions jusqu’à ce que l’expression conditionnelle échoue.</span><span class="sxs-lookup"><span data-stu-id="e171f-105">Executes a statement block until the conditional expression fails.</span></span>

<span data-ttu-id="e171f-106">\[*Attribut* \] while ( *conditionnel* ) { *bloc d’instructions*;}</span><span class="sxs-lookup"><span data-stu-id="e171f-106">\[*Attribute*\] while ( *Conditional* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="e171f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e171f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e171f-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*</span><span class="sxs-lookup"><span data-stu-id="e171f-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="e171f-109">Paramètre facultatif qui contrôle la façon dont l’instruction est compilée.</span><span class="sxs-lookup"><span data-stu-id="e171f-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="e171f-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="e171f-110">Attribute</span></span>             | <span data-ttu-id="e171f-111">Description</span><span class="sxs-lookup"><span data-stu-id="e171f-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e171f-112">dérouler (x)</span><span class="sxs-lookup"><span data-stu-id="e171f-112">unroll(x)</span></span>             | <span data-ttu-id="e171f-113">Dérouler la boucle jusqu’à ce qu’elle cesse de s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="e171f-113">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="e171f-114">Si vous le souhaitez, vous pouvez spécifier le nombre maximal de fois que la boucle peut s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="e171f-114">Optionally, you can specify the maximum number of times the loop can execute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="e171f-115">loop</span><span class="sxs-lookup"><span data-stu-id="e171f-115">loop</span></span>                  | <span data-ttu-id="e171f-116">Utilisez les instructions de contrôle de Flow dans le nuanceur compilé ; n’annulez pas la boucle.</span><span class="sxs-lookup"><span data-stu-id="e171f-116">Use flow-control statements in the compiled shader; do not unroll the loop.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e171f-117">fastopt</span><span class="sxs-lookup"><span data-stu-id="e171f-117">fastopt</span></span>               | <span data-ttu-id="e171f-118">Réduit le temps de compilation, mais produit des optimisations moins agressives.</span><span class="sxs-lookup"><span data-stu-id="e171f-118">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="e171f-119">Si vous utilisez cet attribut, le compilateur ne déroulera pas les boucles.</span><span class="sxs-lookup"><span data-stu-id="e171f-119">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="e171f-120">Cet attribut affecte uniquement les cibles de modèle Shader qui prennent en charge les instructions [break](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="e171f-120">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="e171f-121">Cet attribut est disponible dans le modèle de nuanceur [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) et le [nuanceur modèle 3](dx-graphics-hlsl-sm3.md) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e171f-121">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="e171f-122">Elle est particulièrement utile dans le [nuanceur modèle 4](dx-graphics-hlsl-sm4.md) et versions ultérieures lorsque le compilateur compile des boucles.</span><span class="sxs-lookup"><span data-stu-id="e171f-122">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="e171f-123">Le compilateur simule par défaut des boucles pour déterminer s’il peut les dérouler.</span><span class="sxs-lookup"><span data-stu-id="e171f-123">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="e171f-124">Si vous ne souhaitez pas que le compilateur dérouler les boucles, utilisez cet attribut pour réduire le temps de compilation.</span><span class="sxs-lookup"><span data-stu-id="e171f-124">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |
| <span data-ttu-id="e171f-125">autoriser \_ la \_ condition UAV</span><span class="sxs-lookup"><span data-stu-id="e171f-125">allow\_uav\_condition</span></span> | <span data-ttu-id="e171f-126">Permet à une condition d’arrêt de boucle Compute Shader de se baser sur une lecture UAV.</span><span class="sxs-lookup"><span data-stu-id="e171f-126">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="e171f-127">La boucle ne doit pas contenir d’intrinsèques de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="e171f-127">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="e171f-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditionnel*</span><span class="sxs-lookup"><span data-stu-id="e171f-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="e171f-129">[Expression](dx-graphics-hlsl-expressions.md)conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="e171f-129">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="e171f-130">Si l’expression prend la valeur true, le bloc d’instructions est exécuté.</span><span class="sxs-lookup"><span data-stu-id="e171f-130">If the expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="e171f-131">La boucle se termine lorsque l’expression prend la valeur false.</span><span class="sxs-lookup"><span data-stu-id="e171f-131">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="e171f-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloc d’instructions*</span><span class="sxs-lookup"><span data-stu-id="e171f-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="e171f-133">Une ou plusieurs [instructions](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="e171f-133">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="e171f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e171f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e171f-135">Contrôle de Flow</span><span class="sxs-lookup"><span data-stu-id="e171f-135">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





