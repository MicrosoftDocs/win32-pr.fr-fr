---
title: dcl_output (SM4-ASM)
description: '\_sortie DCL (SM4-ASM)'
ms.assetid: 47e707ad-3ca4-477e-9eb8-3ec462abe864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4391a30e172ef28133b8fe09a99bae7f77c971af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971618"
---
# <a name="dcl_output-sm4---asm"></a><span data-ttu-id="3cafb-103">\_sortie DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3cafb-103">dcl\_output (sm4 - asm)</span></span>

<span data-ttu-id="3cafb-104">Déclare un registre Shader-output.</span><span class="sxs-lookup"><span data-stu-id="3cafb-104">Declares a shader-output register.</span></span>



| <span data-ttu-id="3cafb-105">\_sortie DCL o *N \[ . masque \]*</span><span class="sxs-lookup"><span data-stu-id="3cafb-105">dcl\_output o *N\[.mask\]*</span></span> |
|---------------------------|



 



| <span data-ttu-id="3cafb-106">Élément</span><span class="sxs-lookup"><span data-stu-id="3cafb-106">Item</span></span>                                                                           | <span data-ttu-id="3cafb-107">Description</span><span class="sxs-lookup"><span data-stu-id="3cafb-107">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cafb-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="3cafb-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/> | <span data-ttu-id="3cafb-109">\[dans \] un registre de données de sortie ; *N* est un entier qui indique le numéro du Registre.</span><span class="sxs-lookup"><span data-stu-id="3cafb-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>               |
| <span data-ttu-id="3cafb-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="3cafb-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>     | <span data-ttu-id="3cafb-111">\[\]facultatif.</span><span class="sxs-lookup"><span data-stu-id="3cafb-111">\[in\] Optional.</span></span> <span data-ttu-id="3cafb-112">Masque de composant (. XYZW) qui spécifie les composants Register à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3cafb-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/> |



 

<span data-ttu-id="3cafb-113">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="3cafb-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3cafb-114">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="3cafb-114">Vertex Shader</span></span> | <span data-ttu-id="3cafb-115">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="3cafb-115">Geometry Shader</span></span> | <span data-ttu-id="3cafb-116">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="3cafb-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3cafb-117">x</span><span class="sxs-lookup"><span data-stu-id="3cafb-117">x</span></span>             | <span data-ttu-id="3cafb-118">x</span><span class="sxs-lookup"><span data-stu-id="3cafb-118">x</span></span>               | <span data-ttu-id="3cafb-119">x</span><span class="sxs-lookup"><span data-stu-id="3cafb-119">x</span></span>            |



 

<span data-ttu-id="3cafb-120">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="3cafb-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="3cafb-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="3cafb-121">Example</span></span>

<span data-ttu-id="3cafb-122">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="3cafb-122">Here are some examples.</span></span>


```
dcl_output o0.xyz
dcl_output o1
dcl_output o2.xw
```



## <a name="minimum-shader-model"></a><span data-ttu-id="3cafb-123">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3cafb-123">Minimum Shader Model</span></span>

<span data-ttu-id="3cafb-124">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3cafb-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3cafb-125">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3cafb-125">Shader Model</span></span>                                              | <span data-ttu-id="3cafb-126">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3cafb-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3cafb-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3cafb-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3cafb-128">Oui</span><span class="sxs-lookup"><span data-stu-id="3cafb-128">yes</span></span>       |
| [<span data-ttu-id="3cafb-129">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="3cafb-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3cafb-130">Oui</span><span class="sxs-lookup"><span data-stu-id="3cafb-130">yes</span></span>       |
| [<span data-ttu-id="3cafb-131">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="3cafb-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3cafb-132">Oui</span><span class="sxs-lookup"><span data-stu-id="3cafb-132">yes</span></span>       |
| [<span data-ttu-id="3cafb-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cafb-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3cafb-134">non</span><span class="sxs-lookup"><span data-stu-id="3cafb-134">no</span></span>        |
| [<span data-ttu-id="3cafb-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cafb-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3cafb-136">non</span><span class="sxs-lookup"><span data-stu-id="3cafb-136">no</span></span>        |
| [<span data-ttu-id="3cafb-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cafb-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3cafb-138">non</span><span class="sxs-lookup"><span data-stu-id="3cafb-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3cafb-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3cafb-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cafb-140">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cafb-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





