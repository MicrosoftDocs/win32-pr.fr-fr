---
title: dcl_indexableTemp (SM4-ASM)
description: DCL \_ indexableTemp (SM4-ASM)
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ec3ef1222cd3bf73b4ea3f9ac6e2c3e706aa18e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990844"
---
# <a name="dcl_indexabletemp-sm4---asm"></a><span data-ttu-id="0871b-103">DCL \_ indexableTemp (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0871b-103">dcl\_indexableTemp (sm4 - asm)</span></span>

<span data-ttu-id="0871b-104">Déclare un registre temporaire indexé.</span><span class="sxs-lookup"><span data-stu-id="0871b-104">Declares an indexable, temporary register.</span></span>



| <span data-ttu-id="0871b-105">DCL \_ indexableTemp x *N \[ taille \] , ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="0871b-105">dcl\_indexableTemp x *N\[size\], ComponentCount*</span></span> |
|-------------------------------------------------|



 



| <span data-ttu-id="0871b-106">Élément</span><span class="sxs-lookup"><span data-stu-id="0871b-106">Item</span></span>                                                                                                                           | <span data-ttu-id="0871b-107">Description</span><span class="sxs-lookup"><span data-stu-id="0871b-107">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0871b-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="0871b-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/>                                                                         | <span data-ttu-id="0871b-109">\[dans \] un entier qui indique le numéro du Registre.</span><span class="sxs-lookup"><span data-stu-id="0871b-109">\[in\] An integer that denotes the register number.</span></span><br/>                              |
| <span data-ttu-id="0871b-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[corps\]*</span><span class="sxs-lookup"><span data-stu-id="0871b-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[size\]*</span></span><br/>                                                        | <span data-ttu-id="0871b-111">\[dans \] une valeur entière facultative.</span><span class="sxs-lookup"><span data-stu-id="0871b-111">\[in\] An optional integer value.</span></span> <span data-ttu-id="0871b-112">Nombre d’éléments dans le tableau de registres.</span><span class="sxs-lookup"><span data-stu-id="0871b-112">The number of elements in the register array.</span></span><br/>  |
| <span data-ttu-id="0871b-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="0871b-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span></span><br/> | <span data-ttu-id="0871b-114">\[dans \] une valeur entière facultative. Nombre de composants dans le tableau de registres.</span><span class="sxs-lookup"><span data-stu-id="0871b-114">\[in\] An optional integer value.The number of components in the register array.</span></span><br/> |



 

<span data-ttu-id="0871b-115">Un registre contient suffisamment d’espace pour une valeur de quatre composants 32 bits ; le nombre d’éléments dans le tableau de registres temporaires (indexable et [non indexable](dcl-temps.md)) ne peut pas dépasser 4096.</span><span class="sxs-lookup"><span data-stu-id="0871b-115">A register contains enough space for a 32-bit four-component value; the number of elements in the array of temporary registers (indexable and [non-indexable](dcl-temps.md)) cannot exceed 4096.</span></span>

<span data-ttu-id="0871b-116">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="0871b-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0871b-117">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="0871b-117">Vertex Shader</span></span> | <span data-ttu-id="0871b-118">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="0871b-118">Geometry Shader</span></span> | <span data-ttu-id="0871b-119">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0871b-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0871b-120">x</span><span class="sxs-lookup"><span data-stu-id="0871b-120">x</span></span>             | <span data-ttu-id="0871b-121">x</span><span class="sxs-lookup"><span data-stu-id="0871b-121">x</span></span>               | <span data-ttu-id="0871b-122">x</span><span class="sxs-lookup"><span data-stu-id="0871b-122">x</span></span>            |



 

<span data-ttu-id="0871b-123">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="0871b-123">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="0871b-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="0871b-124">Example</span></span>

<span data-ttu-id="0871b-125">Voici quelques exemples du code généré pour les registres indexables.</span><span class="sxs-lookup"><span data-stu-id="0871b-125">Here are some examples of the code generated for indexable registers.</span></span>


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



## <a name="minimum-shader-model"></a><span data-ttu-id="0871b-126">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0871b-126">Minimum Shader Model</span></span>

<span data-ttu-id="0871b-127">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0871b-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0871b-128">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0871b-128">Shader Model</span></span>                                              | <span data-ttu-id="0871b-129">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0871b-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0871b-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0871b-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0871b-131">Oui</span><span class="sxs-lookup"><span data-stu-id="0871b-131">yes</span></span>       |
| [<span data-ttu-id="0871b-132">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="0871b-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0871b-133">Oui</span><span class="sxs-lookup"><span data-stu-id="0871b-133">yes</span></span>       |
| [<span data-ttu-id="0871b-134">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0871b-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0871b-135">Oui</span><span class="sxs-lookup"><span data-stu-id="0871b-135">yes</span></span>       |
| [<span data-ttu-id="0871b-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0871b-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0871b-137">non</span><span class="sxs-lookup"><span data-stu-id="0871b-137">no</span></span>        |
| [<span data-ttu-id="0871b-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0871b-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0871b-139">non</span><span class="sxs-lookup"><span data-stu-id="0871b-139">no</span></span>        |
| [<span data-ttu-id="0871b-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0871b-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0871b-141">non</span><span class="sxs-lookup"><span data-stu-id="0871b-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0871b-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0871b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0871b-143">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0871b-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





