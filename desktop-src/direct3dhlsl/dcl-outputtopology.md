---
title: dcl_outputTopology (SM4-ASM)
description: DCL \_ outputTopology (SM4-ASM)
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3b305d195ca09a1ef95c99624b47a50058021ca
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679182"
---
# <a name="dcl_outputtopology-sm4---asm"></a><span data-ttu-id="2cda1-103">DCL \_ outputTopology (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2cda1-103">dcl\_outputTopology (sm4 - asm)</span></span>

<span data-ttu-id="2cda1-104">Déclare la géométrie du type primitif-données de sortie du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="2cda1-104">Declares the primitive type geometry-shader output data.</span></span>



| <span data-ttu-id="2cda1-105">\_ *type* de outputTopology DCL</span><span class="sxs-lookup"><span data-stu-id="2cda1-105">dcl\_outputTopology *Type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2cda1-106">Élément</span><span class="sxs-lookup"><span data-stu-id="2cda1-106">Item</span></span></th>
<th><span data-ttu-id="2cda1-107">Description</span><span class="sxs-lookup"><span data-stu-id="2cda1-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2cda1-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Entrer</em></span><span class="sxs-lookup"><span data-stu-id="2cda1-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span><br/></td>
<td><span data-ttu-id="2cda1-109">dans Une topologie de primitive de sortie, qui est l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cda1-109">[in] An output primitive topology, which is one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="2cda1-110"><em>pointlist</em></span><span class="sxs-lookup"><span data-stu-id="2cda1-110"><em>pointlist</em></span></span></li>
<li><span data-ttu-id="2cda1-111"><em>linestrip</em></span><span class="sxs-lookup"><span data-stu-id="2cda1-111"><em>linestrip</em></span></span></li>
<li><span data-ttu-id="2cda1-112"><em>trianglestrip</em></span><span class="sxs-lookup"><span data-stu-id="2cda1-112"><em>trianglestrip</em></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2cda1-113">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="2cda1-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2cda1-114">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="2cda1-114">Vertex Shader</span></span> | <span data-ttu-id="2cda1-115">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="2cda1-115">Geometry Shader</span></span> | <span data-ttu-id="2cda1-116">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="2cda1-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="2cda1-117">x</span><span class="sxs-lookup"><span data-stu-id="2cda1-117">x</span></span>               |              |



 

<span data-ttu-id="2cda1-118">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="2cda1-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="2cda1-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="2cda1-119">Example</span></span>

<span data-ttu-id="2cda1-120">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="2cda1-120">Here is an example.</span></span>


```
dcl_outputTopology trianglestrip
```



## <a name="minimum-shader-model"></a><span data-ttu-id="2cda1-121">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="2cda1-121">Minimum Shader Model</span></span>

<span data-ttu-id="2cda1-122">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="2cda1-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2cda1-123">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="2cda1-123">Shader Model</span></span>                                              | <span data-ttu-id="2cda1-124">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="2cda1-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2cda1-125">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="2cda1-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2cda1-126">Oui</span><span class="sxs-lookup"><span data-stu-id="2cda1-126">yes</span></span>       |
| [<span data-ttu-id="2cda1-127">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="2cda1-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2cda1-128">Oui</span><span class="sxs-lookup"><span data-stu-id="2cda1-128">yes</span></span>       |
| [<span data-ttu-id="2cda1-129">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="2cda1-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2cda1-130">Oui</span><span class="sxs-lookup"><span data-stu-id="2cda1-130">yes</span></span>       |
| [<span data-ttu-id="2cda1-131">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2cda1-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2cda1-132">non</span><span class="sxs-lookup"><span data-stu-id="2cda1-132">no</span></span>        |
| [<span data-ttu-id="2cda1-133">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2cda1-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2cda1-134">non</span><span class="sxs-lookup"><span data-stu-id="2cda1-134">no</span></span>        |
| [<span data-ttu-id="2cda1-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2cda1-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2cda1-136">non</span><span class="sxs-lookup"><span data-stu-id="2cda1-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2cda1-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2cda1-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cda1-138">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2cda1-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





