---
title: dcl_thread_group (SM5-ASM)
description: Déclarez la taille du groupe de threads.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030608"
---
# <a name="dcl_thread_group-sm5---asm"></a><span data-ttu-id="54ec8-103">\_groupe de threads DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="54ec8-103">dcl\_thread\_group (sm5 - asm)</span></span>

<span data-ttu-id="54ec8-104">Déclarez la taille du groupe de threads.</span><span class="sxs-lookup"><span data-stu-id="54ec8-104">Declare thread group size.</span></span>



| <span data-ttu-id="54ec8-105">\_groupe de threads DCL \_ x, y, z</span><span class="sxs-lookup"><span data-stu-id="54ec8-105">dcl\_thread\_group x, y, z</span></span> |
|----------------------------|



 



| <span data-ttu-id="54ec8-106">Élément</span><span class="sxs-lookup"><span data-stu-id="54ec8-106">Item</span></span>                                                   | <span data-ttu-id="54ec8-107">Description</span><span class="sxs-lookup"><span data-stu-id="54ec8-107">Description</span></span>                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="54ec8-108"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="54ec8-108"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="54ec8-109">\[dans \] un entier usigned 32 bits.</span><span class="sxs-lookup"><span data-stu-id="54ec8-109">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="54ec8-110">1 <= x <= 1024</span><span class="sxs-lookup"><span data-stu-id="54ec8-110">1 <= x <= 1024</span></span> <br/> |
| <span data-ttu-id="54ec8-111"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="54ec8-111"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="54ec8-112">\[dans \] un entier usigned 32 bits.</span><span class="sxs-lookup"><span data-stu-id="54ec8-112">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="54ec8-113">1 <= y <= 1024</span><span class="sxs-lookup"><span data-stu-id="54ec8-113">1 <= y <= 1024</span></span><br/>  |
| <span data-ttu-id="54ec8-114"><span id="z"></span><span id="Z"></span>*Lettre*</span><span class="sxs-lookup"><span data-stu-id="54ec8-114"><span id="z"></span><span id="Z"></span>*z*</span></span><br/> | <span data-ttu-id="54ec8-115">\[dans \] un entier usigned 32 bits.</span><span class="sxs-lookup"><span data-stu-id="54ec8-115">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="54ec8-116">1 <= z <= 64</span><span class="sxs-lookup"><span data-stu-id="54ec8-116">1 <= z <= 64</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="54ec8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="54ec8-117">Remarks</span></span>

<span data-ttu-id="54ec8-118">x \* y \* z <= 1024</span><span class="sxs-lookup"><span data-stu-id="54ec8-118">x\*y\*z <= 1024</span></span>

<span data-ttu-id="54ec8-119">Cette déclaration de groupe de threads doit apparaître une fois dans un nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="54ec8-119">This thread group declaration must appear once in a compute shader.</span></span>

<span data-ttu-id="54ec8-120">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="54ec8-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="54ec8-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="54ec8-121">Vertex</span></span> | <span data-ttu-id="54ec8-122">Forme</span><span class="sxs-lookup"><span data-stu-id="54ec8-122">Hull</span></span> | <span data-ttu-id="54ec8-123">Domain</span><span class="sxs-lookup"><span data-stu-id="54ec8-123">Domain</span></span> | <span data-ttu-id="54ec8-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="54ec8-124">Geometry</span></span> | <span data-ttu-id="54ec8-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="54ec8-125">Pixel</span></span> | <span data-ttu-id="54ec8-126">Compute</span><span class="sxs-lookup"><span data-stu-id="54ec8-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="54ec8-127">X</span><span class="sxs-lookup"><span data-stu-id="54ec8-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="54ec8-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="54ec8-128">Minimum Shader Model</span></span>

<span data-ttu-id="54ec8-129">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="54ec8-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="54ec8-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="54ec8-130">Shader Model</span></span>                                              | <span data-ttu-id="54ec8-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="54ec8-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="54ec8-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="54ec8-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="54ec8-133">Oui</span><span class="sxs-lookup"><span data-stu-id="54ec8-133">yes</span></span>       |
| [<span data-ttu-id="54ec8-134">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="54ec8-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="54ec8-135">non</span><span class="sxs-lookup"><span data-stu-id="54ec8-135">no</span></span>        |
| [<span data-ttu-id="54ec8-136">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="54ec8-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="54ec8-137">non</span><span class="sxs-lookup"><span data-stu-id="54ec8-137">no</span></span>        |
| [<span data-ttu-id="54ec8-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54ec8-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="54ec8-139">non</span><span class="sxs-lookup"><span data-stu-id="54ec8-139">no</span></span>        |
| [<span data-ttu-id="54ec8-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54ec8-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="54ec8-141">non</span><span class="sxs-lookup"><span data-stu-id="54ec8-141">no</span></span>        |
| [<span data-ttu-id="54ec8-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54ec8-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="54ec8-143">non</span><span class="sxs-lookup"><span data-stu-id="54ec8-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="54ec8-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54ec8-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54ec8-145">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54ec8-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





