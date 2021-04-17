---
title: dcl_output_siv (SM4-ASM)
description: '\_ \_ SIV de sortie DCL (SM4-ASM)'
ms.assetid: 5a87a113-7413-48ef-9a6a-13eb185650be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df57ea991b9177dc081443301e426560834df894
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990832"
---
# <a name="dcl_output_siv-sm4---asm"></a><span data-ttu-id="fe998-103">\_ \_ SIV de sortie DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fe998-103">dcl\_output\_siv (sm4 - asm)</span></span>

<span data-ttu-id="fe998-104">Déclare un registre de sortie qui contient un paramètre [de valeur système](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="fe998-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="fe998-105">\_ \_ SIV de sortie DCL sur \[ *. Masks* \] , *systemValue*</span><span class="sxs-lookup"><span data-stu-id="fe998-105">dcl\_output\_siv oN\[*.masks*\], *systemValue*</span></span> |
|------------------------------------------------|



 



| <span data-ttu-id="fe998-106">Élément</span><span class="sxs-lookup"><span data-stu-id="fe998-106">Item</span></span>                                                                                                                               | <span data-ttu-id="fe998-107">Description</span><span class="sxs-lookup"><span data-stu-id="fe998-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe998-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="fe998-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="fe998-109">\[dans \] un registre de données de sortie ; *N* est un entier qui indique le numéro du Registre.</span><span class="sxs-lookup"><span data-stu-id="fe998-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="fe998-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="fe998-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="fe998-111">\[\]facultatif.</span><span class="sxs-lookup"><span data-stu-id="fe998-111">\[in\] Optional.</span></span> <span data-ttu-id="fe998-112">Masque de composant (. XYZW) qui spécifie les composants Register à utiliser.</span><span class="sxs-lookup"><span data-stu-id="fe998-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="fe998-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span><span class="sxs-lookup"><span data-stu-id="fe998-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="fe998-114">\[dans \] le nom de la valeur système qui est une chaîne (voir [sémantique de valeur système](dx-graphics-hlsl-semantics.md)) sans le \_ préfixe « SV ».</span><span class="sxs-lookup"><span data-stu-id="fe998-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="fe998-115">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="fe998-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fe998-116">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="fe998-116">Vertex Shader</span></span> | <span data-ttu-id="fe998-117">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="fe998-117">Geometry Shader</span></span> | <span data-ttu-id="fe998-118">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="fe998-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fe998-119">x</span><span class="sxs-lookup"><span data-stu-id="fe998-119">x</span></span>             | <span data-ttu-id="fe998-120">x</span><span class="sxs-lookup"><span data-stu-id="fe998-120">x</span></span>               |              |



 

<span data-ttu-id="fe998-121">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="fe998-121">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="fe998-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="fe998-122">Example</span></span>

<span data-ttu-id="fe998-123">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="fe998-123">Here are some examples.</span></span>


```
dcl_output o[0].y
dcl_output_siv o[0].w, clipDistance
dcl_output_siv o[0].z, cullDistance
```



## <a name="minimum-shader-model"></a><span data-ttu-id="fe998-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="fe998-124">Minimum Shader Model</span></span>

<span data-ttu-id="fe998-125">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="fe998-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fe998-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="fe998-126">Shader Model</span></span>                                              | <span data-ttu-id="fe998-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="fe998-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fe998-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="fe998-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fe998-129">Oui</span><span class="sxs-lookup"><span data-stu-id="fe998-129">yes</span></span>       |
| [<span data-ttu-id="fe998-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="fe998-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fe998-131">Oui</span><span class="sxs-lookup"><span data-stu-id="fe998-131">yes</span></span>       |
| [<span data-ttu-id="fe998-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="fe998-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fe998-133">Oui</span><span class="sxs-lookup"><span data-stu-id="fe998-133">yes</span></span>       |
| [<span data-ttu-id="fe998-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe998-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fe998-135">non</span><span class="sxs-lookup"><span data-stu-id="fe998-135">no</span></span>        |
| [<span data-ttu-id="fe998-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe998-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fe998-137">non</span><span class="sxs-lookup"><span data-stu-id="fe998-137">no</span></span>        |
| [<span data-ttu-id="fe998-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe998-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fe998-139">non</span><span class="sxs-lookup"><span data-stu-id="fe998-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fe998-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe998-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe998-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fe998-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





