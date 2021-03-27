---
title: dcl_indexRange (SM4-ASM)
description: DCL \_ indexRange (SM4-ASM)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b0e2c250afd4ce52729a4c4bffeee0f33e4be6b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971622"
---
# <a name="dcl_indexrange-sm4---asm"></a><span data-ttu-id="62187-103">DCL \_ indexRange (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="62187-103">dcl\_indexRange (sm4 - asm)</span></span>

<span data-ttu-id="62187-104">Déclare une plage de registres accessibles par index (un entier calculé dans le nuanceur).</span><span class="sxs-lookup"><span data-stu-id="62187-104">Declares a range of registers that will be accessed by index (an integer computed in the shader).</span></span>



| <span data-ttu-id="62187-105">DCL \_ IndexRange *minRegisterM*, *maxRegisterN*</span><span class="sxs-lookup"><span data-stu-id="62187-105">dcl\_indexRange *minRegisterM*, *maxRegisterN*</span></span> |
|------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62187-106">Élément</span><span class="sxs-lookup"><span data-stu-id="62187-106">Item</span></span></th>
<th><span data-ttu-id="62187-107">Description</span><span class="sxs-lookup"><span data-stu-id="62187-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="62187-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span><span class="sxs-lookup"><span data-stu-id="62187-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span></span><br/></td>
<td><span data-ttu-id="62187-109">dans Premier registre auquel accéder par index.</span><span class="sxs-lookup"><span data-stu-id="62187-109">[in] The first register to access by index.</span></span> <br/>
<ul>
<li><span data-ttu-id="62187-110"><em>minRegister</em> est soit <strong>v</strong> pour un registre d’entrée de nuanceur de vertex ou de pixels, soit <strong>o</strong> pour un registre de sortie de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="62187-110"><em>minRegister</em> is either <strong>v</strong> for a vertex or pixel shader input register, or <strong>o</strong> for a vertex shader output register.</span></span></li>
<li><span data-ttu-id="62187-111"><em>M</em> est un entier qui indique le numéro du Registre.</span><span class="sxs-lookup"><span data-stu-id="62187-111"><em>M</em> is an integer that denotes the register number.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62187-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span><span class="sxs-lookup"><span data-stu-id="62187-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span></span><br/></td>
<td><span data-ttu-id="62187-113">dans Dernier registre auquel accéder par index.</span><span class="sxs-lookup"><span data-stu-id="62187-113">[in] The last register to access by index.</span></span> <span data-ttu-id="62187-114">Même forme que <em>minRegister</em> , sauf que <em>N</em> est le numéro du Registre.</span><span class="sxs-lookup"><span data-stu-id="62187-114">Same form as <em>minRegister</em> except <em>N</em> is the register number.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="62187-115">Les restrictions suivantes s’appliquent à tous les registres :</span><span class="sxs-lookup"><span data-stu-id="62187-115">The following restrictions apply to all registers:</span></span>

-   <span data-ttu-id="62187-116">Les registres min et Max doivent être du même type et avoir les mêmes masques de composant (si les masques sont déclarés).</span><span class="sxs-lookup"><span data-stu-id="62187-116">The min and max registers must be the same type and have the same component masks (if masks are declared).</span></span>
-   <span data-ttu-id="62187-117">Un registre peut avoir plusieurs plages d’index, à condition qu’elles ne se chevauchent pas.</span><span class="sxs-lookup"><span data-stu-id="62187-117">A register may have multiple index ranges, as long as they do no not overlap.</span></span>
-   <span data-ttu-id="62187-118">Le numéro de Registre minimal doit être inférieur au nombre maximal de registres.</span><span class="sxs-lookup"><span data-stu-id="62187-118">The min register number must be less than the max register number.</span></span>
-   <span data-ttu-id="62187-119">Un registre d’index ne peut pas contenir une [valeur système](dx-graphics-hlsl-semantics.md).</span><span class="sxs-lookup"><span data-stu-id="62187-119">An index register cannot contain a [system-value](dx-graphics-hlsl-semantics.md).</span></span>
-   <span data-ttu-id="62187-120">L’indexation d’un registre en dehors de la déclaration d’index max génère des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="62187-120">Indexing a register outside of the max index declaration produces undefined results.</span></span>

<span data-ttu-id="62187-121">Les registres d’entrée de nuanceur de pixels doivent utiliser le même mode d’interpolation ; les registres de sortie du nuanceur de pixels ne sont pas indexables.</span><span class="sxs-lookup"><span data-stu-id="62187-121">Pixel shader input registers must use the same interpolation mode; pixel shader output registers are not indexable.</span></span>

<span data-ttu-id="62187-122">Un registre d’entrée de nuanceur Geometry a deux dimensions (axe de vertex, axe d’attribut); la plage d’index s’applique uniquement à l’axe des attributs, car l’axe des vertex est toujours entièrement indexé.</span><span class="sxs-lookup"><span data-stu-id="62187-122">A geometry shader input register has two dimensions (vertex axis, attribute axis); the index range applies only to the attribute axis because the vertex axis is always fully indexable.</span></span>

<span data-ttu-id="62187-123">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="62187-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="62187-124">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="62187-124">Vertex Shader</span></span> | <span data-ttu-id="62187-125">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="62187-125">Geometry Shader</span></span> | <span data-ttu-id="62187-126">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="62187-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="62187-127">x</span><span class="sxs-lookup"><span data-stu-id="62187-127">x</span></span>             | <span data-ttu-id="62187-128">x</span><span class="sxs-lookup"><span data-stu-id="62187-128">x</span></span>               | <span data-ttu-id="62187-129">x</span><span class="sxs-lookup"><span data-stu-id="62187-129">x</span></span>            |



 

<span data-ttu-id="62187-130">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="62187-130">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="62187-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="62187-131">Example</span></span>

<span data-ttu-id="62187-132">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="62187-132">Here is an example.</span></span>


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="62187-133">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="62187-133">Minimum Shader Model</span></span>

<span data-ttu-id="62187-134">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="62187-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="62187-135">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="62187-135">Shader Model</span></span>                                              | <span data-ttu-id="62187-136">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="62187-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="62187-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="62187-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="62187-138">Oui</span><span class="sxs-lookup"><span data-stu-id="62187-138">yes</span></span>       |
| [<span data-ttu-id="62187-139">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="62187-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="62187-140">Oui</span><span class="sxs-lookup"><span data-stu-id="62187-140">yes</span></span>       |
| [<span data-ttu-id="62187-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="62187-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="62187-142">Oui</span><span class="sxs-lookup"><span data-stu-id="62187-142">yes</span></span>       |
| [<span data-ttu-id="62187-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62187-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="62187-144">non</span><span class="sxs-lookup"><span data-stu-id="62187-144">no</span></span>        |
| [<span data-ttu-id="62187-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62187-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="62187-146">non</span><span class="sxs-lookup"><span data-stu-id="62187-146">no</span></span>        |
| [<span data-ttu-id="62187-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62187-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="62187-148">non</span><span class="sxs-lookup"><span data-stu-id="62187-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="62187-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62187-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62187-150">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62187-150">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





