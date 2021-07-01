---
title: Instruction do (ocidl. h)
description: Exécuter une série d’instructions en continu jusqu’à ce que l’expression conditionnelle échoue.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- Instruction do HLSL
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f019af77ef0021ad0574bf703ff2a2a52ac0f6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118784"
---
# <a name="do-statement"></a><span data-ttu-id="96201-104">Instruction do</span><span class="sxs-lookup"><span data-stu-id="96201-104">do Statement</span></span>

<span data-ttu-id="96201-105">Exécuter une série d’instructions en continu jusqu’à ce que l’expression conditionnelle échoue.</span><span class="sxs-lookup"><span data-stu-id="96201-105">Execute a series of statements continuously until the conditional expression fails.</span></span>

<span data-ttu-id="96201-106">\[*Attribut* \] { *bloc d’instructions*;} while ( *conditionnel* );</span><span class="sxs-lookup"><span data-stu-id="96201-106">\[*Attribute*\] do {   *Statement Block*; } while( *Conditional* );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="96201-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96201-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96201-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*</span><span class="sxs-lookup"><span data-stu-id="96201-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="96201-109">Paramètre facultatif qui contrôle la façon dont l’instruction est compilée.</span><span class="sxs-lookup"><span data-stu-id="96201-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="96201-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="96201-110">Attribute</span></span> | <span data-ttu-id="96201-111">Description</span><span class="sxs-lookup"><span data-stu-id="96201-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96201-112">fastopt</span><span class="sxs-lookup"><span data-stu-id="96201-112">fastopt</span></span>   | <span data-ttu-id="96201-113">Réduit le temps de compilation, mais produit des optimisations moins agressives.</span><span class="sxs-lookup"><span data-stu-id="96201-113">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="96201-114">Si vous utilisez cet attribut, le compilateur ne déroulera pas les boucles.</span><span class="sxs-lookup"><span data-stu-id="96201-114">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="96201-115">Cet attribut affecte uniquement les cibles de modèle Shader qui prennent en charge les instructions [break](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="96201-115">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="96201-116">Cet attribut est disponible dans le modèle de nuanceur [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) et le [nuanceur modèle 3](dx-graphics-hlsl-sm3.md) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="96201-116">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="96201-117">Elle est particulièrement utile dans le [nuanceur modèle 4](dx-graphics-hlsl-sm4.md) et versions ultérieures lorsque le compilateur compile des boucles.</span><span class="sxs-lookup"><span data-stu-id="96201-117">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="96201-118">Le compilateur simule par défaut des boucles pour déterminer s’il peut les dérouler.</span><span class="sxs-lookup"><span data-stu-id="96201-118">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="96201-119">Si vous ne souhaitez pas que le compilateur dérouler les boucles, utilisez cet attribut pour réduire le temps de compilation.</span><span class="sxs-lookup"><span data-stu-id="96201-119">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="96201-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloc d’instructions*</span><span class="sxs-lookup"><span data-stu-id="96201-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="96201-121">Une ou plusieurs [instructions](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="96201-121">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> <dt>

<span data-ttu-id="96201-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditionnel*</span><span class="sxs-lookup"><span data-stu-id="96201-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="96201-123">[Expression](dx-graphics-hlsl-expressions.md)conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="96201-123">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="96201-124">Le bloc d’instructions est exécuté avant l’évaluation de l’expression.</span><span class="sxs-lookup"><span data-stu-id="96201-124">The statement block is executed before the expression is evaluated.</span></span> <span data-ttu-id="96201-125">La boucle est abandonnée lorsque l’expression prend la valeur false.</span><span class="sxs-lookup"><span data-stu-id="96201-125">The loop is exited when the expression evaluates to false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96201-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="96201-126">Requirements</span></span>



| <span data-ttu-id="96201-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96201-127">Requirement</span></span> | <span data-ttu-id="96201-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="96201-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96201-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="96201-129">Header</span></span><br/> | <dl> <span data-ttu-id="96201-130"><dt>Ocidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="96201-130"><dt>Ocidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96201-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96201-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96201-132">Contrôle de Flow</span><span class="sxs-lookup"><span data-stu-id="96201-132">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





