---
title: MOV (SM4-ASM)
description: Déplacement au niveau du composant. | MOV (SM4-ASM)
ms.assetid: A8865237-59D3-4332-9F09-157E10C4FFC6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f029cd8a31a9348e729681878773c225b87b9fbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211385"
---
# <a name="mov-sm4---asm"></a><span data-ttu-id="e905f-104">MOV (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e905f-104">mov (sm4 - asm)</span></span>

<span data-ttu-id="e905f-105">Déplacement au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="e905f-105">Component-wise move.</span></span>



| <span data-ttu-id="e905f-106">Instruction : MOV \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e905f-106">Instruction: mov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="e905f-107">Élément</span><span class="sxs-lookup"><span data-stu-id="e905f-107">Item</span></span>                                                            | <span data-ttu-id="e905f-108">Description</span><span class="sxs-lookup"><span data-stu-id="e905f-108">Description</span></span>                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e905f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e905f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e905f-110">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e905f-110">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="e905f-111">*dest*  =  . *src0*</span><span class="sxs-lookup"><span data-stu-id="e905f-111">*dest* = *src0*</span></span><br/> |
| <span data-ttu-id="e905f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e905f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e905f-113">\[dans \] les composants à déplacer.</span><span class="sxs-lookup"><span data-stu-id="e905f-113">\[in\] The components to move.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="e905f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e905f-114">Remarks</span></span>

<span data-ttu-id="e905f-115">Les modificateurs, autres que Swizzle, supposent que les données sont à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="e905f-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="e905f-116">L’absence de modificateurs déplace uniquement les données sans modifier les bits.</span><span class="sxs-lookup"><span data-stu-id="e905f-116">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="e905f-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="e905f-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e905f-118">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="e905f-118">Vertex Shader</span></span> | <span data-ttu-id="e905f-119">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="e905f-119">Geometry Shader</span></span> | <span data-ttu-id="e905f-120">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="e905f-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e905f-121">x</span><span class="sxs-lookup"><span data-stu-id="e905f-121">x</span></span>             | <span data-ttu-id="e905f-122">x</span><span class="sxs-lookup"><span data-stu-id="e905f-122">x</span></span>               | <span data-ttu-id="e905f-123">x</span><span class="sxs-lookup"><span data-stu-id="e905f-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e905f-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="e905f-124">Minimum Shader Model</span></span>

<span data-ttu-id="e905f-125">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="e905f-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e905f-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="e905f-126">Shader Model</span></span>                                              | <span data-ttu-id="e905f-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="e905f-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e905f-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e905f-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e905f-129">Oui</span><span class="sxs-lookup"><span data-stu-id="e905f-129">yes</span></span>       |
| [<span data-ttu-id="e905f-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="e905f-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e905f-131">Oui</span><span class="sxs-lookup"><span data-stu-id="e905f-131">yes</span></span>       |
| [<span data-ttu-id="e905f-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="e905f-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e905f-133">Oui</span><span class="sxs-lookup"><span data-stu-id="e905f-133">yes</span></span>       |
| [<span data-ttu-id="e905f-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e905f-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e905f-135">non</span><span class="sxs-lookup"><span data-stu-id="e905f-135">no</span></span>        |
| [<span data-ttu-id="e905f-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e905f-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e905f-137">non</span><span class="sxs-lookup"><span data-stu-id="e905f-137">no</span></span>        |
| [<span data-ttu-id="e905f-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e905f-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e905f-139">non</span><span class="sxs-lookup"><span data-stu-id="e905f-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e905f-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e905f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e905f-141">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e905f-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





