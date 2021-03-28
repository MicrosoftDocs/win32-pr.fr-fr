---
title: dcl_output_sgv (SM4-ASM)
description: DCL \_ Output \_ SGV (SM4-ASM)
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cfc5da7724a7e661f84ae5e7b293e5e84b61f15
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381231"
---
# <a name="dcl_output_sgv-sm4---asm"></a><span data-ttu-id="10713-103">DCL \_ Output \_ SGV (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="10713-103">dcl\_output\_sgv (sm4 - asm)</span></span>

<span data-ttu-id="10713-104">Déclare un registre de sortie qui contient un paramètre [de valeur système](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="10713-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="10713-105">la \_ sortie DCL \_ SGV sur *\[ . \] Mask*, *systemValue*</span><span class="sxs-lookup"><span data-stu-id="10713-105">dcl\_output\_sgv oN *\[.mask\]*, *systemValue*</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="10713-106">Élément</span><span class="sxs-lookup"><span data-stu-id="10713-106">Item</span></span>                                                                                                                               | <span data-ttu-id="10713-107">Description</span><span class="sxs-lookup"><span data-stu-id="10713-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10713-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="10713-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="10713-109">\[dans \] un registre de données de sortie ; *N* est un entier qui indique le numéro du Registre.</span><span class="sxs-lookup"><span data-stu-id="10713-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="10713-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="10713-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="10713-111">\[\]facultatif.</span><span class="sxs-lookup"><span data-stu-id="10713-111">\[in\] Optional.</span></span> <span data-ttu-id="10713-112">Masque de composant (. XYZW) qui spécifie les composants Register à utiliser.</span><span class="sxs-lookup"><span data-stu-id="10713-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="10713-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span><span class="sxs-lookup"><span data-stu-id="10713-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="10713-114">\[dans \] le nom de la valeur système qui est une chaîne (voir [sémantique de valeur système](dx-graphics-hlsl-semantics.md)) sans le \_ préfixe « SV ».</span><span class="sxs-lookup"><span data-stu-id="10713-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="10713-115">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="10713-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="10713-116">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="10713-116">Vertex Shader</span></span> | <span data-ttu-id="10713-117">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="10713-117">Geometry Shader</span></span> | <span data-ttu-id="10713-118">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="10713-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="10713-119">x</span><span class="sxs-lookup"><span data-stu-id="10713-119">x</span></span>               |              |



 

<span data-ttu-id="10713-120">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="10713-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="10713-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="10713-121">Example</span></span>

<span data-ttu-id="10713-122">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="10713-122">Here is an example.</span></span>


```
dcl_output_sgv o4.x, primitiveID
```



## <a name="minimum-shader-model"></a><span data-ttu-id="10713-123">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="10713-123">Minimum Shader Model</span></span>

<span data-ttu-id="10713-124">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="10713-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="10713-125">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="10713-125">Shader Model</span></span>                                              | <span data-ttu-id="10713-126">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="10713-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="10713-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="10713-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="10713-128">Oui</span><span class="sxs-lookup"><span data-stu-id="10713-128">yes</span></span>       |
| [<span data-ttu-id="10713-129">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="10713-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="10713-130">Oui</span><span class="sxs-lookup"><span data-stu-id="10713-130">yes</span></span>       |
| [<span data-ttu-id="10713-131">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="10713-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="10713-132">Oui</span><span class="sxs-lookup"><span data-stu-id="10713-132">yes</span></span>       |
| [<span data-ttu-id="10713-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="10713-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="10713-134">non</span><span class="sxs-lookup"><span data-stu-id="10713-134">no</span></span>        |
| [<span data-ttu-id="10713-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="10713-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="10713-136">non</span><span class="sxs-lookup"><span data-stu-id="10713-136">no</span></span>        |
| [<span data-ttu-id="10713-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="10713-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="10713-138">non</span><span class="sxs-lookup"><span data-stu-id="10713-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="10713-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10713-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10713-140">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="10713-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





