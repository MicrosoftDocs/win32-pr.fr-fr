---
title: packoffset
description: Mot clé de compression de constante de nuanceur facultatif, qui utilise la syntaxe suivante
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- HLSL packoffset
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6feeaa586abe30fa8a36c28d0298dc408cdfb099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312460"
---
# <a name="packoffset"></a><span data-ttu-id="876ab-104">packoffset</span><span class="sxs-lookup"><span data-stu-id="876ab-104">packoffset</span></span>

<span data-ttu-id="876ab-105">Mot clé de compression de constante de nuanceur facultatif, qui utilise la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="876ab-105">Optional shader constant packing keyword, which uses the following syntax:</span></span>



|                                                 |
|-------------------------------------------------|
| <span data-ttu-id="876ab-106">: packoffset (sous- \[ composant c \] \[ . composant \] )</span><span class="sxs-lookup"><span data-stu-id="876ab-106">: packoffset( c\[Subcomponent\]\[.component\] )</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="876ab-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="876ab-107">Parameters</span></span>



| <span data-ttu-id="876ab-108">Élément</span><span class="sxs-lookup"><span data-stu-id="876ab-108">Item</span></span>                                                                                                                                                                                 | <span data-ttu-id="876ab-109">Description</span><span class="sxs-lookup"><span data-stu-id="876ab-109">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="876ab-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span><span class="sxs-lookup"><span data-stu-id="876ab-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span></span><br/>                                                                                                  | <span data-ttu-id="876ab-111">Mot clé requis.</span><span class="sxs-lookup"><span data-stu-id="876ab-111">Required keyword.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="876ab-112"><span id="c"></span><span id="C"></span>**secteur**</span><span class="sxs-lookup"><span data-stu-id="876ab-112"><span id="c"></span><span id="C"></span>**c**</span></span><br/>                                                                                                                             | <span data-ttu-id="876ab-113">L’empaquetage s’applique uniquement aux registres constants (c).</span><span class="sxs-lookup"><span data-stu-id="876ab-113">Packing applies to constant registers (c) only.</span></span> <br/>                                                                                          |
| <span data-ttu-id="876ab-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Sous-composant \] \[ . composant\]**</span><span class="sxs-lookup"><span data-stu-id="876ab-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent\]\[.component\]**</span></span><br/> | <span data-ttu-id="876ab-115">Sous-composants et composants facultatifs.</span><span class="sxs-lookup"><span data-stu-id="876ab-115">Optional subcomponents and components.</span></span> <span data-ttu-id="876ab-116">Un sous-composant est un numéro de Registre, qui est un entier.</span><span class="sxs-lookup"><span data-stu-id="876ab-116">A subcomponent is a register number, which is an integer.</span></span> <span data-ttu-id="876ab-117">Un composant se présente sous la forme \[ . XYZW \] .</span><span class="sxs-lookup"><span data-stu-id="876ab-117">A component is in the form of \[.xyzw\].</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="876ab-118">Notes</span><span class="sxs-lookup"><span data-stu-id="876ab-118">Remarks</span></span>

<span data-ttu-id="876ab-119">Utilisez ce mot clé pour empaqueter manuellement une constante de nuanceur lors [de la déclaration d’un type de variable](dx-graphics-hlsl-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="876ab-119">Use this keyword to manually pack a shader constant when [declaring a variable type](dx-graphics-hlsl-variable-syntax.md).</span></span>

<span data-ttu-id="876ab-120">Lorsque vous compressez une constante, vous ne pouvez pas mélanger des types de constantes.</span><span class="sxs-lookup"><span data-stu-id="876ab-120">When packing a constant, you cannot mix constant types.</span></span>

<span data-ttu-id="876ab-121">Le compilateur se comporte de façon légèrement différente pour les constantes globales et les constantes uniformes :</span><span class="sxs-lookup"><span data-stu-id="876ab-121">The compiler behaves slightly differently for global constants and uniform constants:</span></span>

-   <span data-ttu-id="876ab-122">Constante globale.</span><span class="sxs-lookup"><span data-stu-id="876ab-122">A global constant.</span></span> <span data-ttu-id="876ab-123">Une variable globale est ajoutée en tant que constante globale à un *$Global* CBuffer par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="876ab-123">A global variable is added as a global constant to a *$Global* cbuffer by the compiler.</span></span> <span data-ttu-id="876ab-124">Les éléments empaquetés automatiquement (ceux déclarés sans packoffset) s’affichent après la dernière variable compressée manuellement.</span><span class="sxs-lookup"><span data-stu-id="876ab-124">Automatically packed elements (those declared without packoffset) will appear after the last manually packed variable.</span></span> <span data-ttu-id="876ab-125">Vous pouvez combiner des types lors de l’empaquetage de constantes globales.</span><span class="sxs-lookup"><span data-stu-id="876ab-125">You may mix types when packing global constants.</span></span>
-   <span data-ttu-id="876ab-126">Constante uniforme.</span><span class="sxs-lookup"><span data-stu-id="876ab-126">A uniform constant.</span></span> <span data-ttu-id="876ab-127">Un paramètre uniforme dans la liste de paramètres d’une fonction sera ajouté à une *$param* mémoire tampon constante par le compilateur lorsque le nuanceur est compilé en dehors de l’infrastructure des effets.</span><span class="sxs-lookup"><span data-stu-id="876ab-127">A uniform parameter in the parameter list of a function will be added to a *$Param* constant buffer by the compiler when the shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="876ab-128">En cas de compilation dans l’infrastructure Effect, une constante uniforme doit être résolue en une variable uniforme définie dans la portée globale.</span><span class="sxs-lookup"><span data-stu-id="876ab-128">When compiled inside the effect framework, a uniform constant must resolve to a uniform variable defined in global scope.</span></span> <span data-ttu-id="876ab-129">Une constante uniforme ne peut pas être décalée manuellement ; leur utilisation recommandée est uniquement destinée à la spécialisation des nuanceurs dans lesquels elles sont réaffectées aux données globales, et non à la transmission de données d’application dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="876ab-129">A uniform constant cannot be manually offset; their recommend use is only for specialization of shaders where they alias back to globals, not as a means of passing application data into the shader.</span></span>

<span data-ttu-id="876ab-130">Voici quelques exemples supplémentaires : les [constantes de compression à l’aide du Shader Model 4](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="876ab-130">Here are some additional examples: [packing constants using shader model 4](dx-graphics-hlsl-packing-rules.md).</span></span>

## <a name="examples"></a><span data-ttu-id="876ab-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="876ab-131">Examples</span></span>

<span data-ttu-id="876ab-132">Voici plusieurs exemples de décompression manuelle des constantes de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="876ab-132">Here are several examples of manually packing shader constants.</span></span>

<span data-ttu-id="876ab-133">Compresser les sous-composants des vecteurs et des scalaires dont la taille est suffisamment grande pour empêcher le franchissement des limites du Registre.</span><span class="sxs-lookup"><span data-stu-id="876ab-133">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundaries.</span></span> <span data-ttu-id="876ab-134">Par exemple, ils sont tous valides :</span><span class="sxs-lookup"><span data-stu-id="876ab-134">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a><span data-ttu-id="876ab-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="876ab-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876ab-136">Syntaxe des variables</span><span class="sxs-lookup"><span data-stu-id="876ab-136">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="876ab-137">Variables (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="876ab-137">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





