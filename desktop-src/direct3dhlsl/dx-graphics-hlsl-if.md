---
title: if, instruction
description: Exécuter de manière conditionnelle une série d’instructions, en fonction de l’évaluation de l’expression conditionnelle.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- Instruction if (HLSL)
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e8a3c20e73b9783d39b4f4cbdb7c0be5b75fcda
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104030738"
---
# <a name="if-statement"></a><span data-ttu-id="681db-104">if, instruction</span><span class="sxs-lookup"><span data-stu-id="681db-104">if Statement</span></span>

<span data-ttu-id="681db-105">Exécuter de manière conditionnelle une série d’instructions, en fonction de l’évaluation de l’expression conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="681db-105">Conditionally execute a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                               |
|---------------------------------------------------------------|
| <span data-ttu-id="681db-106">\[*Attribut* \] if ( *conditionnel* ) { *bloc d’instructions*;}</span><span class="sxs-lookup"><span data-stu-id="681db-106">\[*Attribute*\] if ( *Conditional* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="681db-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="681db-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="681db-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribut*</span><span class="sxs-lookup"><span data-stu-id="681db-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="681db-109">Paramètre facultatif qui contrôle la façon dont l’instruction est compilée.</span><span class="sxs-lookup"><span data-stu-id="681db-109">An optional parameter that controls how the statement is compiled.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="681db-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="681db-110">Attribute</span></span></th>
<th><span data-ttu-id="681db-111">Description</span><span class="sxs-lookup"><span data-stu-id="681db-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="681db-112">branche</span><span class="sxs-lookup"><span data-stu-id="681db-112">branch</span></span></td>
<td><span data-ttu-id="681db-113">Évaluez un seul côté de l’instruction if en fonction de la condition donnée.</span><span class="sxs-lookup"><span data-stu-id="681db-113">Evaluate only one side of the if statement depending on the given condition.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="681db-114">Lorsque vous utilisez le modèle de <a href="dx-graphics-hlsl-sm2.md">nuanceur 2. x</a> ou le <a href="dx-graphics-hlsl-sm3.md">modèle de nuanceur 3,0</a>, chaque fois que vous utilisez la création de branche dynamique, vous consommez des ressources.</span><span class="sxs-lookup"><span data-stu-id="681db-114">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="681db-115">Ainsi, si vous utilisez la création de branche dynamique de façon excessive lorsque vous ciblez ces profils, vous pouvez recevoir des erreurs de compilation.</span><span class="sxs-lookup"><span data-stu-id="681db-115">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="681db-116">aplatir</span><span class="sxs-lookup"><span data-stu-id="681db-116">flatten</span></span></td>
<td><span data-ttu-id="681db-117">Évaluez les deux côtés de l’instruction if et choisissez entre les deux valeurs résultantes.</span><span class="sxs-lookup"><span data-stu-id="681db-117">Evaluate both sides of the if statement and choose between the two resulting values.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="681db-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditionnel*</span><span class="sxs-lookup"><span data-stu-id="681db-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="681db-119">[Expression](dx-graphics-hlsl-expressions.md)conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="681db-119">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="681db-120">L’expression est évaluée et, si la valeur est true, le bloc d’instructions est exécuté.</span><span class="sxs-lookup"><span data-stu-id="681db-120">The expression is evaluated, and if true, the statement block is executed.</span></span>

</dd> <dt>

<span data-ttu-id="681db-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloc d’instructions*</span><span class="sxs-lookup"><span data-stu-id="681db-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="681db-122">Une ou plusieurs [instructions HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="681db-122">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="681db-123">Notes</span><span class="sxs-lookup"><span data-stu-id="681db-123">Remarks</span></span>

<span data-ttu-id="681db-124">Lorsque le compilateur utilise la méthode Branch pour compiler une instruction if, il génère du code qui évalue un seul côté de l’instruction if en fonction de la condition donnée.</span><span class="sxs-lookup"><span data-stu-id="681db-124">When the compiler uses the branch method for compiling an if statement it will generate code that will evaluate only one side of the if statement depending on the given condition.</span></span> <span data-ttu-id="681db-125">Par exemple, dans l’instruction if :</span><span class="sxs-lookup"><span data-stu-id="681db-125">For example, in the if statement:</span></span>


```
[branch] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="681db-126">L’instruction **If** a un bloc Else implicite, qui est équivalent à x = x.</span><span class="sxs-lookup"><span data-stu-id="681db-126">The **if** statement has an implicit else block, which is equivalent to x = x.</span></span> <span data-ttu-id="681db-127">Étant donné que nous avons indiqué au compilateur d’utiliser la méthode Branch avec l’attribut Branch précédent, le code compilé évalue x et n’exécute que le côté qui doit être exécuté. Si x est égal à zéro, il exécute le côté **else** et, s’il n’est pas nul, il exécute le côté **Then** .</span><span class="sxs-lookup"><span data-stu-id="681db-127">Because we have told the compiler to use the branch method with the preceding branch attribute, the compiled code will evaluate x and execute only the side that should be executed; if x is zero, then it will execute the **else** side, and if it is non-zero it will execute the **then** side.</span></span>

<span data-ttu-id="681db-128">À l’inverse, si l’attribut **flattive** est utilisé, le code compilé évalue les deux côtés de l’instruction **If** et choisit entre les deux valeurs résultantes à l’aide de la valeur d’origine x.</span><span class="sxs-lookup"><span data-stu-id="681db-128">Conversely, if the **flatten** attribute is used, then the compiled code will evaluate both sides of the **if** statement and choose between the two resulting values using the original value of x.</span></span> <span data-ttu-id="681db-129">Voici un exemple d’utilisation de l’attribut Flatten :</span><span class="sxs-lookup"><span data-stu-id="681db-129">Here is an example of a usage of the flatten attribute:</span></span>


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="681db-130">Dans certains cas, l’utilisation des attributs Branch ou flattx peut générer une erreur de compilation.</span><span class="sxs-lookup"><span data-stu-id="681db-130">There are certain cases where using the branch or flatten attributes may generate a compile error.</span></span> <span data-ttu-id="681db-131">L’attribut Branch peut échouer si l’une des deux côtés de l’instruction if contient une fonction de dégradé, telle que [**tex2D**](dx-graphics-hlsl-tex2d.md).</span><span class="sxs-lookup"><span data-stu-id="681db-131">The branch attribute may fail if either side of the if statement contains a gradient function, such as [**tex2D**](dx-graphics-hlsl-tex2d.md).</span></span> <span data-ttu-id="681db-132">L’attribut aplati peut échouer si l’une des deux faces de l’instruction if contient une instruction Append de flux ou toute autre instruction qui a des effets secondaires.</span><span class="sxs-lookup"><span data-stu-id="681db-132">The flatten attribute may fail if either side of the if statement contains a stream append statement or any other statement that has side-effects.</span></span>

<span data-ttu-id="681db-133">Une instruction **If** peut également utiliser un bloc Else facultatif.</span><span class="sxs-lookup"><span data-stu-id="681db-133">An **if** statement can also use an optional else block.</span></span> <span data-ttu-id="681db-134">Si l’expression **If** a la valeur true, le code du bloc d’instructions associé à l’instruction if est traité.</span><span class="sxs-lookup"><span data-stu-id="681db-134">If the **if** expression is true, the code in the statement block associated with the if statement is processed.</span></span> <span data-ttu-id="681db-135">Dans le cas contraire, le bloc d’instructions associé au bloc Else facultatif est traité.</span><span class="sxs-lookup"><span data-stu-id="681db-135">Otherwise, the statement block associated with the optional else block is processed.</span></span>

## <a name="see-also"></a><span data-ttu-id="681db-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="681db-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="681db-137">Contrôle de Flow</span><span class="sxs-lookup"><span data-stu-id="681db-137">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





