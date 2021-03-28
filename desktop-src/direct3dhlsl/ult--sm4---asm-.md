---
title: ULT (SM4-ASM)
description: Comparaison des entiers non signés Vector au niveau du composant, inférieur à.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624c09d182e9ecfd4d1b603f6fd2c34b83d768ed
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990740"
---
# <a name="ult-sm4---asm"></a><span data-ttu-id="76b07-103">ULT (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="76b07-103">ult (sm4 - asm)</span></span>

<span data-ttu-id="76b07-104">Comparaison des entiers non signés Vector au niveau du composant, inférieur à.</span><span class="sxs-lookup"><span data-stu-id="76b07-104">Component-wise vector unsigned integer less-than comparison.</span></span>



| <span data-ttu-id="76b07-105">ULT dest \[ . Mask \] , src0 \[ . Swizzle \] , src1 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="76b07-105">ult dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="76b07-106">Élément</span><span class="sxs-lookup"><span data-stu-id="76b07-106">Item</span></span>                                                            | <span data-ttu-id="76b07-107">Description</span><span class="sxs-lookup"><span data-stu-id="76b07-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="76b07-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="76b07-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="76b07-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="76b07-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="76b07-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="76b07-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="76b07-111">\[dans \] la valeur à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="76b07-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="76b07-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="76b07-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="76b07-113">\[dans \] la valeur à comparer à *src1*.</span><span class="sxs-lookup"><span data-stu-id="76b07-113">\[in\] The value to compare to *src1*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="76b07-114">Notes</span><span class="sxs-lookup"><span data-stu-id="76b07-114">Remarks</span></span>

<span data-ttu-id="76b07-115">Effectue une comparaison d’entiers non signés (*src0*  <  *src1*) pour chaque composant et écrit le résultat dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="76b07-115">Performs the unsigned integer comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="76b07-116">Si la comparaison est true, cette instruction retourne 0xFFFFFFFF pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="76b07-116">If the comparison is true, this instruction returns 0xFFFFFFFF for that component.</span></span> <span data-ttu-id="76b07-117">Sinon, elle retourne 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="76b07-117">Otherwise it returns 0x0000000.</span></span>

<span data-ttu-id="76b07-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="76b07-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="76b07-119">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="76b07-119">Vertex Shader</span></span> | <span data-ttu-id="76b07-120">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="76b07-120">Geometry Shader</span></span> | <span data-ttu-id="76b07-121">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="76b07-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="76b07-122">x</span><span class="sxs-lookup"><span data-stu-id="76b07-122">x</span></span>             | <span data-ttu-id="76b07-123">x</span><span class="sxs-lookup"><span data-stu-id="76b07-123">x</span></span>               | <span data-ttu-id="76b07-124">x</span><span class="sxs-lookup"><span data-stu-id="76b07-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="76b07-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="76b07-125">Minimum Shader Model</span></span>

<span data-ttu-id="76b07-126">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="76b07-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="76b07-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="76b07-127">Shader Model</span></span>                                              | <span data-ttu-id="76b07-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="76b07-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="76b07-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="76b07-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="76b07-130">Oui</span><span class="sxs-lookup"><span data-stu-id="76b07-130">yes</span></span>       |
| [<span data-ttu-id="76b07-131">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="76b07-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="76b07-132">Oui</span><span class="sxs-lookup"><span data-stu-id="76b07-132">yes</span></span>       |
| [<span data-ttu-id="76b07-133">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="76b07-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="76b07-134">Oui</span><span class="sxs-lookup"><span data-stu-id="76b07-134">yes</span></span>       |
| [<span data-ttu-id="76b07-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76b07-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="76b07-136">non</span><span class="sxs-lookup"><span data-stu-id="76b07-136">no</span></span>        |
| [<span data-ttu-id="76b07-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76b07-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="76b07-138">non</span><span class="sxs-lookup"><span data-stu-id="76b07-138">no</span></span>        |
| [<span data-ttu-id="76b07-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76b07-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="76b07-140">non</span><span class="sxs-lookup"><span data-stu-id="76b07-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="76b07-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76b07-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b07-142">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="76b07-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





