---
title: dcl_constantBuffer (SM4-ASM)
description: DCL \_ constantBuffer (SM4-ASM)
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2eeb9368af0121ee61fde5d106eb0f3b08e5acb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101093"
---
# <a name="dcl_constantbuffer-sm4---asm"></a><span data-ttu-id="e916c-103">DCL \_ constantBuffer (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e916c-103">dcl\_constantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="e916c-104">Déclare une mémoire tampon de constante de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="e916c-104">Declares a shader constant buffer.</span></span>



| <span data-ttu-id="e916c-105">\_constantBuffer *cbN \[ \]*, *AccessPattern*</span><span class="sxs-lookup"><span data-stu-id="e916c-105">dcl\_constantBuffer *cbN\[size\]*, *AccessPattern*</span></span> |
|----------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e916c-106">Élément</span><span class="sxs-lookup"><span data-stu-id="e916c-106">Item</span></span></th>
<th><span data-ttu-id="e916c-107">Description</span><span class="sxs-lookup"><span data-stu-id="e916c-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e916c-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>CB<em>N [Taille]</em></span><span class="sxs-lookup"><span data-stu-id="e916c-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>cb<em>N[size]</em></span></span><br/></td>
<td><span data-ttu-id="e916c-109">dans Une mémoire tampon de constante de nuanceur, où N est un entier qui indique le nombre de buffer-buffer-Register et Size est un entier qui indique le nombre d’éléments dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e916c-109">[in] A shader constant buffer where N is an integer that denotes the constant-buffer-register number and size is an integer that denotes the number of elements in the buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e916c-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span><span class="sxs-lookup"><span data-stu-id="e916c-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span></span><br/></td>
<td><span data-ttu-id="e916c-111">dans La façon dont la mémoire tampon est accessible par le code du nuanceur, qui est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e916c-111">[in] The way that the buffer will be accessed by shader code, which is one of the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e916c-112">Nom</span><span class="sxs-lookup"><span data-stu-id="e916c-112">Name</span></span></th>
<th><span data-ttu-id="e916c-113">Description</span><span class="sxs-lookup"><span data-stu-id="e916c-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e916c-114">immediateIndexed</span><span class="sxs-lookup"><span data-stu-id="e916c-114">immediateIndexed</span></span></td>
<td><span data-ttu-id="e916c-115">Indexez la mémoire tampon avec une valeur littérale.</span><span class="sxs-lookup"><span data-stu-id="e916c-115">Index the buffer with a literal value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e916c-116">dynamic_indexed</span><span class="sxs-lookup"><span data-stu-id="e916c-116">dynamic_indexed</span></span></td>
<td><span data-ttu-id="e916c-117">Indexez la mémoire tampon avec le résultat d’une expression évaluée.</span><span class="sxs-lookup"><span data-stu-id="e916c-117">Index the buffer with the result of an evaluated expression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e916c-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="e916c-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e916c-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="e916c-119">Vertex Shader</span></span> | <span data-ttu-id="e916c-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="e916c-120">Geometry Shader</span></span> | <span data-ttu-id="e916c-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="e916c-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e916c-122">x</span><span class="sxs-lookup"><span data-stu-id="e916c-122">x</span></span>             | <span data-ttu-id="e916c-123">x</span><span class="sxs-lookup"><span data-stu-id="e916c-123">x</span></span>               | <span data-ttu-id="e916c-124">x</span><span class="sxs-lookup"><span data-stu-id="e916c-124">x</span></span>            |



 

<span data-ttu-id="e916c-125">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="e916c-125">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="e916c-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="e916c-126">Example</span></span>

<span data-ttu-id="e916c-127">Cet exemple déclare une mémoire tampon constante pour Register CB0, qui contient 19 éléments.</span><span class="sxs-lookup"><span data-stu-id="e916c-127">This example declares a constant buffer for register cb0, which has 19 elements.</span></span> <span data-ttu-id="e916c-128">Ces éléments sont accessibles à l’aide d’un index littéral.</span><span class="sxs-lookup"><span data-stu-id="e916c-128">These elements are accessed with a literal index.</span></span>


```
dcl_constantbuffer  cb0[19], immediateIndexed
```



## <a name="minimum-shader-model"></a><span data-ttu-id="e916c-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="e916c-129">Minimum Shader Model</span></span>

<span data-ttu-id="e916c-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="e916c-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e916c-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="e916c-131">Shader Model</span></span>                                              | <span data-ttu-id="e916c-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="e916c-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e916c-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e916c-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e916c-134">Oui</span><span class="sxs-lookup"><span data-stu-id="e916c-134">yes</span></span>       |
| [<span data-ttu-id="e916c-135">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="e916c-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e916c-136">Oui</span><span class="sxs-lookup"><span data-stu-id="e916c-136">yes</span></span>       |
| [<span data-ttu-id="e916c-137">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="e916c-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e916c-138">Oui</span><span class="sxs-lookup"><span data-stu-id="e916c-138">yes</span></span>       |
| [<span data-ttu-id="e916c-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e916c-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e916c-140">non</span><span class="sxs-lookup"><span data-stu-id="e916c-140">no</span></span>        |
| [<span data-ttu-id="e916c-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e916c-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e916c-142">non</span><span class="sxs-lookup"><span data-stu-id="e916c-142">no</span></span>        |
| [<span data-ttu-id="e916c-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e916c-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e916c-144">non</span><span class="sxs-lookup"><span data-stu-id="e916c-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e916c-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e916c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e916c-146">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e916c-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





