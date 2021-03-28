---
title: dcl_globalFlags (SM4-ASM)
description: DCL \_ globalFlags (SM4-ASM)
ms.assetid: 7289db9e-f0cd-4849-854f-34aa38ec2c2d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e15fce958056f91a41954b987850ad4c5a43e521
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381239"
---
# <a name="dcl_globalflags-sm4---asm"></a><span data-ttu-id="4edad-103">DCL \_ globalFlags (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4edad-103">dcl\_globalFlags (sm4 - asm)</span></span>

<span data-ttu-id="4edad-104">Déclare des indicateurs globaux de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4edad-104">Declares shader global flags.</span></span>



| <span data-ttu-id="4edad-105">\_ *indicateurs* du globalFlags DCL</span><span class="sxs-lookup"><span data-stu-id="4edad-105">dcl\_globalFlags *flags*</span></span> |
|--------------------------|



 

<dl> <dt>

<span data-ttu-id="4edad-106"><span id="flags"></span><span id="FLAGS"></span>*père*</span><span class="sxs-lookup"><span data-stu-id="4edad-106"><span id="flags"></span><span id="FLAGS"></span>*flags*</span></span>
</dt> <dd>

<span data-ttu-id="4edad-107">\[dans \] un indicateur de nuanceur global.</span><span class="sxs-lookup"><span data-stu-id="4edad-107">\[in\] A global shader flag.</span></span> <span data-ttu-id="4edad-108">Un indicateur est actuellement défini.</span><span class="sxs-lookup"><span data-stu-id="4edad-108">There is currently one flag defined.</span></span>

-   <span data-ttu-id="4edad-109">Refactorisation \_ autorisée : permet au pilote de réorganiser les opérations arithmétiques à des fins d’optimisation, comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="4edad-109">REFACTORING\_ALLOWED - Permits the driver to reorder arithmetic operations for optimization, as shown here.</span></span>

    ```
    // Original code
    a = b*c + b*d + b*e + b*f

    // Reordered code
    a = b*(c + d + e + f)
    // or 
    a = dot4((b,b,b,b), (c,d,e,f))
    ```

    

> [!Note]
>
> <span data-ttu-id="4edad-110">La réorganisation des opérations arithmétiques peut générer des résultats différents.</span><span class="sxs-lookup"><span data-stu-id="4edad-110">Reordering arithmetic operations may generate different results.</span></span>

 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="4edad-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4edad-111">Remarks</span></span>

<span data-ttu-id="4edad-112">Cette instruction facultative s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4edad-112">This optional instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4edad-113">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="4edad-113">Vertex Shader</span></span> | <span data-ttu-id="4edad-114">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="4edad-114">Geometry Shader</span></span> | <span data-ttu-id="4edad-115">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="4edad-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4edad-116">x</span><span class="sxs-lookup"><span data-stu-id="4edad-116">x</span></span>             | <span data-ttu-id="4edad-117">x</span><span class="sxs-lookup"><span data-stu-id="4edad-117">x</span></span>               | <span data-ttu-id="4edad-118">x</span><span class="sxs-lookup"><span data-stu-id="4edad-118">x</span></span>            |



 

<span data-ttu-id="4edad-119">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="4edad-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="4edad-120">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4edad-120">Minimum Shader Model</span></span>

<span data-ttu-id="4edad-121">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="4edad-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4edad-122">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4edad-122">Shader Model</span></span>                                              | <span data-ttu-id="4edad-123">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="4edad-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4edad-124">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4edad-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4edad-125">Oui</span><span class="sxs-lookup"><span data-stu-id="4edad-125">yes</span></span>       |
| [<span data-ttu-id="4edad-126">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4edad-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4edad-127">Oui</span><span class="sxs-lookup"><span data-stu-id="4edad-127">yes</span></span>       |
| [<span data-ttu-id="4edad-128">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4edad-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4edad-129">Oui</span><span class="sxs-lookup"><span data-stu-id="4edad-129">yes</span></span>       |
| [<span data-ttu-id="4edad-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4edad-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4edad-131">non</span><span class="sxs-lookup"><span data-stu-id="4edad-131">no</span></span>        |
| [<span data-ttu-id="4edad-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4edad-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4edad-133">non</span><span class="sxs-lookup"><span data-stu-id="4edad-133">no</span></span>        |
| [<span data-ttu-id="4edad-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4edad-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4edad-135">non</span><span class="sxs-lookup"><span data-stu-id="4edad-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4edad-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4edad-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4edad-137">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4edad-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




