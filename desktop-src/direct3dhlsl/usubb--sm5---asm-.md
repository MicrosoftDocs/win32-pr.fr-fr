---
title: usubb (SM5-ASM)
description: Entier non signé soustrait avec emprunt.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111ffd134a75b8cfe19f63597cd80655201359c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381133"
---
# <a name="usubb-sm5---asm"></a><span data-ttu-id="ae1df-103">usubb (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ae1df-103">usubb (sm5 - asm)</span></span>

<span data-ttu-id="ae1df-104">Entier non signé soustrait avec emprunt.</span><span class="sxs-lookup"><span data-stu-id="ae1df-104">Unsigned integer subtract with borrow.</span></span>



| <span data-ttu-id="ae1df-105">usubb dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ae1df-105">usubb dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="ae1df-106">Élément</span><span class="sxs-lookup"><span data-stu-id="ae1df-106">Item</span></span>                                                               | <span data-ttu-id="ae1df-107">Description</span><span class="sxs-lookup"><span data-stu-id="ae1df-107">Description</span></span>                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae1df-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="ae1df-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="ae1df-109">\[dans \] contient les résultats LSAB de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="ae1df-109">\[in\] Contains the LSAB results of the instruction.</span></span><br/>                                   |
| <span data-ttu-id="ae1df-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="ae1df-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="ae1df-111">\[dans \] le composant correspondant de *dest0* qui spécifie si un emprunt a été produit.</span><span class="sxs-lookup"><span data-stu-id="ae1df-111">\[in\] The corresponding component of *dest0* that specifies if a borrow was produced.</span></span><br/> |
| <span data-ttu-id="ae1df-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ae1df-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="ae1df-113">\[dans \] la valeur à partir de laquelle soustraire.</span><span class="sxs-lookup"><span data-stu-id="ae1df-113">\[in\] The value from which to subtract.</span></span><br/>                                               |
| <span data-ttu-id="ae1df-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ae1df-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="ae1df-115">\[dans \] le montant à soustraire de *src0*.</span><span class="sxs-lookup"><span data-stu-id="ae1df-115">\[in\] The amount to subtract from *src0*.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="ae1df-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ae1df-116">Remarks</span></span>

<span data-ttu-id="ae1df-117">Cette instruction effectue une soustraction non signée au niveau du composant des opérandes 32 bits *src1* à partir de *src0*, en plaçant la partie LSB du résultat 32 bits dans *dest0*.</span><span class="sxs-lookup"><span data-stu-id="ae1df-117">This instruction performs a component-wise unsigned subtract of 32-bit operands *src1* from *src0*, placing the LSB part of the 32-bit result in *dest0*.</span></span>

<span data-ttu-id="ae1df-118">Le composant correspondant dans *dest1* est écrit avec 1 si un emprunt est produit, 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ae1df-118">The corresponding component in *dest1* is written with 1 if a borrow is produced, 0 otherwise.</span></span>

<span data-ttu-id="ae1df-119">*dest1* peut avoir la valeur null si le emprunt n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ae1df-119">*dest1* can be NULL if the borrow is not needed.</span></span>

<span data-ttu-id="ae1df-120">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="ae1df-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ae1df-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="ae1df-121">Vertex</span></span> | <span data-ttu-id="ae1df-122">Forme</span><span class="sxs-lookup"><span data-stu-id="ae1df-122">Hull</span></span> | <span data-ttu-id="ae1df-123">Domain</span><span class="sxs-lookup"><span data-stu-id="ae1df-123">Domain</span></span> | <span data-ttu-id="ae1df-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="ae1df-124">Geometry</span></span> | <span data-ttu-id="ae1df-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="ae1df-125">Pixel</span></span> | <span data-ttu-id="ae1df-126">Compute</span><span class="sxs-lookup"><span data-stu-id="ae1df-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ae1df-127">X</span><span class="sxs-lookup"><span data-stu-id="ae1df-127">X</span></span>      | <span data-ttu-id="ae1df-128">X</span><span class="sxs-lookup"><span data-stu-id="ae1df-128">X</span></span>    | <span data-ttu-id="ae1df-129">X</span><span class="sxs-lookup"><span data-stu-id="ae1df-129">X</span></span>      | <span data-ttu-id="ae1df-130">X</span><span class="sxs-lookup"><span data-stu-id="ae1df-130">X</span></span>        | <span data-ttu-id="ae1df-131">X</span><span class="sxs-lookup"><span data-stu-id="ae1df-131">X</span></span>     | <span data-ttu-id="ae1df-132">X</span><span class="sxs-lookup"><span data-stu-id="ae1df-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ae1df-133">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="ae1df-133">Minimum Shader Model</span></span>

<span data-ttu-id="ae1df-134">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="ae1df-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ae1df-135">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="ae1df-135">Shader Model</span></span>                                              | <span data-ttu-id="ae1df-136">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="ae1df-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ae1df-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="ae1df-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ae1df-138">Oui</span><span class="sxs-lookup"><span data-stu-id="ae1df-138">yes</span></span>       |
| [<span data-ttu-id="ae1df-139">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="ae1df-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ae1df-140">non</span><span class="sxs-lookup"><span data-stu-id="ae1df-140">no</span></span>        |
| [<span data-ttu-id="ae1df-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="ae1df-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ae1df-142">non</span><span class="sxs-lookup"><span data-stu-id="ae1df-142">no</span></span>        |
| [<span data-ttu-id="ae1df-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae1df-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ae1df-144">non</span><span class="sxs-lookup"><span data-stu-id="ae1df-144">no</span></span>        |
| [<span data-ttu-id="ae1df-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae1df-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ae1df-146">non</span><span class="sxs-lookup"><span data-stu-id="ae1df-146">no</span></span>        |
| [<span data-ttu-id="ae1df-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae1df-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ae1df-148">non</span><span class="sxs-lookup"><span data-stu-id="ae1df-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ae1df-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae1df-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae1df-150">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ae1df-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





