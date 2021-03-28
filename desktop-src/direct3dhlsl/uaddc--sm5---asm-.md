---
title: uaddc (SM5-ASM)
description: Entier non signé ajouter avec Carry.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f57f75be617e32c15212207110851520a7a281e2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507711"
---
# <a name="uaddc-sm5---asm"></a><span data-ttu-id="f5c0a-103">uaddc (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f5c0a-103">uaddc (sm5 - asm)</span></span>

<span data-ttu-id="f5c0a-104">Entier non signé ajouter avec Carry.</span><span class="sxs-lookup"><span data-stu-id="f5c0a-104">Unsigned integer add with carry.</span></span>



| <span data-ttu-id="f5c0a-105">uaddc dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f5c0a-105">uaddc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="f5c0a-106">Élément</span><span class="sxs-lookup"><span data-stu-id="f5c0a-106">Item</span></span>                                                               | <span data-ttu-id="f5c0a-107">Description</span><span class="sxs-lookup"><span data-stu-id="f5c0a-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="f5c0a-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="f5c0a-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="f5c0a-109">\[dans \] adresse du résultat.</span><span class="sxs-lookup"><span data-stu-id="f5c0a-109">\[in\] Address of the result.</span></span><br/>               |
| <span data-ttu-id="f5c0a-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="f5c0a-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="f5c0a-111">\[en \] 1 si le transport est produit.</span><span class="sxs-lookup"><span data-stu-id="f5c0a-111">\[in\] 1 if carry is produced.</span></span> <span data-ttu-id="f5c0a-112">Sinon, 0.</span><span class="sxs-lookup"><span data-stu-id="f5c0a-112">Otherwise 0.</span></span><br/> |
| <span data-ttu-id="f5c0a-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f5c0a-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="f5c0a-114">\[dans l' \] opérande 32 bits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="f5c0a-114">\[in\] 32-bit operand to be added.</span></span><br/>          |
| <span data-ttu-id="f5c0a-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="f5c0a-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="f5c0a-116">\[dans l' \] opérande 32 bits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="f5c0a-116">\[in\] 32-bit operand to be added.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="f5c0a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f5c0a-117">Remarks</span></span>

<span data-ttu-id="f5c0a-118">*dest1* peut avoir la valeur null si le transport n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f5c0a-118">*dest1* can be NULL if the carry is not needed.</span></span>

<span data-ttu-id="f5c0a-119">Utilisez cette instruction pour les opérations arithmétiques de haute précision.</span><span class="sxs-lookup"><span data-stu-id="f5c0a-119">Use this instruction for high precision arithmetic.</span></span>

<span data-ttu-id="f5c0a-120">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="f5c0a-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f5c0a-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="f5c0a-121">Vertex</span></span> | <span data-ttu-id="f5c0a-122">Forme</span><span class="sxs-lookup"><span data-stu-id="f5c0a-122">Hull</span></span> | <span data-ttu-id="f5c0a-123">Domain</span><span class="sxs-lookup"><span data-stu-id="f5c0a-123">Domain</span></span> | <span data-ttu-id="f5c0a-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f5c0a-124">Geometry</span></span> | <span data-ttu-id="f5c0a-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="f5c0a-125">Pixel</span></span> | <span data-ttu-id="f5c0a-126">Compute</span><span class="sxs-lookup"><span data-stu-id="f5c0a-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f5c0a-127">X</span><span class="sxs-lookup"><span data-stu-id="f5c0a-127">X</span></span>      | <span data-ttu-id="f5c0a-128">X</span><span class="sxs-lookup"><span data-stu-id="f5c0a-128">X</span></span>    | <span data-ttu-id="f5c0a-129">X</span><span class="sxs-lookup"><span data-stu-id="f5c0a-129">X</span></span>      | <span data-ttu-id="f5c0a-130">X</span><span class="sxs-lookup"><span data-stu-id="f5c0a-130">X</span></span>        | <span data-ttu-id="f5c0a-131">X</span><span class="sxs-lookup"><span data-stu-id="f5c0a-131">X</span></span>     | <span data-ttu-id="f5c0a-132">X</span><span class="sxs-lookup"><span data-stu-id="f5c0a-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f5c0a-133">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f5c0a-133">Minimum Shader Model</span></span>

<span data-ttu-id="f5c0a-134">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="f5c0a-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f5c0a-135">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f5c0a-135">Shader Model</span></span>                                              | <span data-ttu-id="f5c0a-136">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f5c0a-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f5c0a-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f5c0a-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f5c0a-138">Oui</span><span class="sxs-lookup"><span data-stu-id="f5c0a-138">yes</span></span>       |
| [<span data-ttu-id="f5c0a-139">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="f5c0a-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f5c0a-140">non</span><span class="sxs-lookup"><span data-stu-id="f5c0a-140">no</span></span>        |
| [<span data-ttu-id="f5c0a-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f5c0a-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f5c0a-142">non</span><span class="sxs-lookup"><span data-stu-id="f5c0a-142">no</span></span>        |
| [<span data-ttu-id="f5c0a-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5c0a-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f5c0a-144">non</span><span class="sxs-lookup"><span data-stu-id="f5c0a-144">no</span></span>        |
| [<span data-ttu-id="f5c0a-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5c0a-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f5c0a-146">non</span><span class="sxs-lookup"><span data-stu-id="f5c0a-146">no</span></span>        |
| [<span data-ttu-id="f5c0a-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5c0a-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f5c0a-148">non</span><span class="sxs-lookup"><span data-stu-id="f5c0a-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f5c0a-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f5c0a-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5c0a-150">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f5c0a-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





