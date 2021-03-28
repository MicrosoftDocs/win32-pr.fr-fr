---
title: dcl_inputPrimitive (SM4-ASM)
description: DCL \_ inputPrimitive (SM4-ASM)
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 76c131b7c4225c0b30ad1183e4da1fe6c0561754
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940579"
---
# <a name="dcl_inputprimitive-sm4---asm"></a><span data-ttu-id="d5259-103">DCL \_ inputPrimitive (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d5259-103">dcl\_inputPrimitive (sm4 - asm)</span></span>

<span data-ttu-id="d5259-104">Déclare le type primitif pour les entrées Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="d5259-104">Declares the primitive type for geometry-shader inputs.</span></span>



| <span data-ttu-id="d5259-105">\_ *type* de inputPrimitive DCL</span><span class="sxs-lookup"><span data-stu-id="d5259-105">dcl\_inputPrimitive *type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5259-106">Élément</span><span class="sxs-lookup"><span data-stu-id="d5259-106">Item</span></span></th>
<th><span data-ttu-id="d5259-107">Description</span><span class="sxs-lookup"><span data-stu-id="d5259-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5259-108"><span id="type"></span><span id="TYPE"></span><em>entrer</em></span><span class="sxs-lookup"><span data-stu-id="d5259-108"><span id="type"></span><span id="TYPE"></span><em>type</em></span></span><br/></td>
<td><span data-ttu-id="d5259-109">dans Type primitif de données d’entrée, qui est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d5259-109">[in] Input-data primitive type, which is one of the following:</span></span> <br/>
<ul>
<li><span data-ttu-id="d5259-110"><em>point</em> - Liste des points</span><span class="sxs-lookup"><span data-stu-id="d5259-110"><em>point</em> - point list</span></span></li>
<li><span data-ttu-id="d5259-111"><em>ligne</em> - Liste des lignes</span><span class="sxs-lookup"><span data-stu-id="d5259-111"><em>line</em> - line list</span></span></li>
<li><span data-ttu-id="d5259-112"><em>triangle</em> - liste de triangles</span><span class="sxs-lookup"><span data-stu-id="d5259-112"><em>triangle</em> - triangle list</span></span></li>
<li><span data-ttu-id="d5259-113"><em>line_adj</em> - Liste des lignes avec données d’contiguïté</span><span class="sxs-lookup"><span data-stu-id="d5259-113"><em>line_adj</em> - line list with adjacency data</span></span></li>
<li><span data-ttu-id="d5259-114"><em>triangle_adj</em> - liste de triangles avec données d’contiguïté</span><span class="sxs-lookup"><span data-stu-id="d5259-114"><em>triangle_adj</em> - triangle list with adjacency data</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d5259-115">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="d5259-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d5259-116">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="d5259-116">Vertex Shader</span></span> | <span data-ttu-id="d5259-117">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="d5259-117">Geometry Shader</span></span> | <span data-ttu-id="d5259-118">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d5259-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="d5259-119">x</span><span class="sxs-lookup"><span data-stu-id="d5259-119">x</span></span>               |              |



 

<span data-ttu-id="d5259-120">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="d5259-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="d5259-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="d5259-121">Example</span></span>

<span data-ttu-id="d5259-122">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="d5259-122">Here is an example.</span></span>


```
dcl_inputPrimitive triangle
```



## <a name="minimum-shader-model"></a><span data-ttu-id="d5259-123">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d5259-123">Minimum Shader Model</span></span>

<span data-ttu-id="d5259-124">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d5259-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d5259-125">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d5259-125">Shader Model</span></span>                                              | <span data-ttu-id="d5259-126">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d5259-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d5259-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="d5259-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d5259-128">Oui</span><span class="sxs-lookup"><span data-stu-id="d5259-128">yes</span></span>       |
| [<span data-ttu-id="d5259-129">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="d5259-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d5259-130">Oui</span><span class="sxs-lookup"><span data-stu-id="d5259-130">yes</span></span>       |
| [<span data-ttu-id="d5259-131">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d5259-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d5259-132">Oui</span><span class="sxs-lookup"><span data-stu-id="d5259-132">yes</span></span>       |
| [<span data-ttu-id="d5259-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5259-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d5259-134">non</span><span class="sxs-lookup"><span data-stu-id="d5259-134">no</span></span>        |
| [<span data-ttu-id="d5259-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5259-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d5259-136">non</span><span class="sxs-lookup"><span data-stu-id="d5259-136">no</span></span>        |
| [<span data-ttu-id="d5259-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5259-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d5259-138">non</span><span class="sxs-lookup"><span data-stu-id="d5259-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d5259-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5259-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5259-140">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d5259-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





