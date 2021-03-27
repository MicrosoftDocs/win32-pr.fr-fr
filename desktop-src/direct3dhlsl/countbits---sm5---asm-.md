---
title: countbits (SM5-ASM)
description: Compte le nombre de bits définis dans un nombre.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d46fe9c750790d65630a743dd9ddc347fea50e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841661"
---
# <a name="countbits-sm5---asm"></a><span data-ttu-id="b4faa-103">countbits (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b4faa-103">countbits (sm5 - asm)</span></span>

<span data-ttu-id="b4faa-104">Compte le nombre de bits définis dans un nombre.</span><span class="sxs-lookup"><span data-stu-id="b4faa-104">Counts the number of bits set in a number.</span></span>



| <span data-ttu-id="b4faa-105">countbits dest \[ . Mask \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b4faa-105">countbits dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="b4faa-106">Élément</span><span class="sxs-lookup"><span data-stu-id="b4faa-106">Item</span></span>                                                            | <span data-ttu-id="b4faa-107">Description</span><span class="sxs-lookup"><span data-stu-id="b4faa-107">Description</span></span>                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="b4faa-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b4faa-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b4faa-109">\[dans \] l’adresse des résultats.</span><span class="sxs-lookup"><span data-stu-id="b4faa-109">\[in\] The address of the results.</span></span><br/> |
| <span data-ttu-id="b4faa-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b4faa-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b4faa-111">\[dans \] le numéro d’entrée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b4faa-111">\[in\] The input 32-bit number.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="b4faa-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b4faa-112">Remarks</span></span>

<span data-ttu-id="b4faa-113">Cette instruction peut être utilisée pour calculer le pourcentage de couverture d’entrée du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="b4faa-113">This instruction can be used to compute shader input coverage percentage.</span></span>

<span data-ttu-id="b4faa-114">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="b4faa-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b4faa-115">Sommet</span><span class="sxs-lookup"><span data-stu-id="b4faa-115">Vertex</span></span> | <span data-ttu-id="b4faa-116">Forme</span><span class="sxs-lookup"><span data-stu-id="b4faa-116">Hull</span></span> | <span data-ttu-id="b4faa-117">Domain</span><span class="sxs-lookup"><span data-stu-id="b4faa-117">Domain</span></span> | <span data-ttu-id="b4faa-118">Géométrie</span><span class="sxs-lookup"><span data-stu-id="b4faa-118">Geometry</span></span> | <span data-ttu-id="b4faa-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="b4faa-119">Pixel</span></span> | <span data-ttu-id="b4faa-120">Compute</span><span class="sxs-lookup"><span data-stu-id="b4faa-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b4faa-121">X</span><span class="sxs-lookup"><span data-stu-id="b4faa-121">X</span></span>      | <span data-ttu-id="b4faa-122">X</span><span class="sxs-lookup"><span data-stu-id="b4faa-122">X</span></span>    | <span data-ttu-id="b4faa-123">X</span><span class="sxs-lookup"><span data-stu-id="b4faa-123">X</span></span>      | <span data-ttu-id="b4faa-124">X</span><span class="sxs-lookup"><span data-stu-id="b4faa-124">X</span></span>        | <span data-ttu-id="b4faa-125">X</span><span class="sxs-lookup"><span data-stu-id="b4faa-125">X</span></span>     | <span data-ttu-id="b4faa-126">X</span><span class="sxs-lookup"><span data-stu-id="b4faa-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b4faa-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b4faa-127">Minimum Shader Model</span></span>

<span data-ttu-id="b4faa-128">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="b4faa-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b4faa-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b4faa-129">Shader Model</span></span>                                              | <span data-ttu-id="b4faa-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b4faa-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b4faa-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="b4faa-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b4faa-132">Oui</span><span class="sxs-lookup"><span data-stu-id="b4faa-132">yes</span></span>       |
| [<span data-ttu-id="b4faa-133">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="b4faa-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b4faa-134">non</span><span class="sxs-lookup"><span data-stu-id="b4faa-134">no</span></span>        |
| [<span data-ttu-id="b4faa-135">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="b4faa-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b4faa-136">non</span><span class="sxs-lookup"><span data-stu-id="b4faa-136">no</span></span>        |
| [<span data-ttu-id="b4faa-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4faa-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b4faa-138">non</span><span class="sxs-lookup"><span data-stu-id="b4faa-138">no</span></span>        |
| [<span data-ttu-id="b4faa-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4faa-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b4faa-140">non</span><span class="sxs-lookup"><span data-stu-id="b4faa-140">no</span></span>        |
| [<span data-ttu-id="b4faa-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4faa-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b4faa-142">non</span><span class="sxs-lookup"><span data-stu-id="b4faa-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b4faa-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4faa-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4faa-144">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4faa-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





