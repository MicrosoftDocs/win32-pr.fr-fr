---
title: dcl_immediateConstantBuffer (SM4-ASM)
description: DCL \_ immediateConstantBuffer (SM4-ASM)
ms.assetid: 55e21ab1-0749-4200-8e68-bb098e935dac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f4b4868f3b07285465abb9080688adf6129e1bf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313768"
---
# <a name="dcl_immediateconstantbuffer-sm4---asm"></a><span data-ttu-id="8f0e0-103">DCL \_ immediateConstantBuffer (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8f0e0-103">dcl\_immediateConstantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="8f0e0-104">Déclare un tampon constant immédiat du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="8f0e0-104">Declares a shader immediate-constant buffer.</span></span>



| <span data-ttu-id="8f0e0-105">\_ *valeur (s) de* immediateConstantBuffer DCL</span><span class="sxs-lookup"><span data-stu-id="8f0e0-105">dcl\_immediateConstantBuffer *value(s)*</span></span> |
|-----------------------------------------|



 

<dl> <dt>

<span data-ttu-id="8f0e0-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*valeur (s)*</span><span class="sxs-lookup"><span data-stu-id="8f0e0-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*value(s)*</span></span>
</dt> <dd>

<span data-ttu-id="8f0e0-107">\[dans \] , la mémoire tampon doit contenir au moins une valeur, mais pas plus de 4096 valeurs.</span><span class="sxs-lookup"><span data-stu-id="8f0e0-107">\[in\] The buffer must contain at least one value, but not more than 4096 values.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="8f0e0-108">Notes</span><span class="sxs-lookup"><span data-stu-id="8f0e0-108">Remarks</span></span>

<span data-ttu-id="8f0e0-109">Un nuanceur est autorisé à disposer d’une mémoire tampon constante immédiate.</span><span class="sxs-lookup"><span data-stu-id="8f0e0-109">A shader is allowed one immediate-constant buffer.</span></span> <span data-ttu-id="8f0e0-110">Une mémoire tampon constante immédiate est accessible comme une mémoire tampon constante avec l’indexation dynamique.</span><span class="sxs-lookup"><span data-stu-id="8f0e0-110">An immediate-constant buffer is accessed just like a constant buffer with dynamic indexing.</span></span>

<span data-ttu-id="8f0e0-111">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="8f0e0-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8f0e0-112">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="8f0e0-112">Vertex Shader</span></span> | <span data-ttu-id="8f0e0-113">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="8f0e0-113">Geometry Shader</span></span> | <span data-ttu-id="8f0e0-114">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="8f0e0-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8f0e0-115">x</span><span class="sxs-lookup"><span data-stu-id="8f0e0-115">x</span></span>             | <span data-ttu-id="8f0e0-116">x</span><span class="sxs-lookup"><span data-stu-id="8f0e0-116">x</span></span>               | <span data-ttu-id="8f0e0-117">x</span><span class="sxs-lookup"><span data-stu-id="8f0e0-117">x</span></span>            |



 

<span data-ttu-id="8f0e0-118">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="8f0e0-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="8f0e0-119">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="8f0e0-119">Minimum Shader Model</span></span>

<span data-ttu-id="8f0e0-120">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="8f0e0-120">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8f0e0-121">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8f0e0-121">Shader Model</span></span>                                              | <span data-ttu-id="8f0e0-122">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="8f0e0-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8f0e0-123">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="8f0e0-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8f0e0-124">Oui</span><span class="sxs-lookup"><span data-stu-id="8f0e0-124">yes</span></span>       |
| [<span data-ttu-id="8f0e0-125">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="8f0e0-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8f0e0-126">Oui</span><span class="sxs-lookup"><span data-stu-id="8f0e0-126">yes</span></span>       |
| [<span data-ttu-id="8f0e0-127">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="8f0e0-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8f0e0-128">Oui</span><span class="sxs-lookup"><span data-stu-id="8f0e0-128">yes</span></span>       |
| [<span data-ttu-id="8f0e0-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f0e0-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8f0e0-130">non</span><span class="sxs-lookup"><span data-stu-id="8f0e0-130">no</span></span>        |
| [<span data-ttu-id="8f0e0-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f0e0-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8f0e0-132">non</span><span class="sxs-lookup"><span data-stu-id="8f0e0-132">no</span></span>        |
| [<span data-ttu-id="8f0e0-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f0e0-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8f0e0-134">non</span><span class="sxs-lookup"><span data-stu-id="8f0e0-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8f0e0-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8f0e0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f0e0-136">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f0e0-136">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




