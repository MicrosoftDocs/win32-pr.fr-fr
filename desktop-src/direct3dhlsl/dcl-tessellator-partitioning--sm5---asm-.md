---
title: dcl_tessellator_partitioning (SM5-ASM)
description: Déclarez le partitionnement du paveur dans une section de déclaration de nuanceur de coque.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381225"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a><span data-ttu-id="b7596-103">\_ \_ partitionnement de du paveur DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b7596-103">dcl\_tessellator\_partitioning (sm5 - asm)</span></span>

<span data-ttu-id="b7596-104">Déclarez le partitionnement du paveur dans une section de déclaration de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="b7596-104">Declare the tessellator partitioning in a hull shader declaration section.</span></span>



| <span data-ttu-id="b7596-105">\_partitionnement de du paveur DCL \_ {entier de partitionnement \_ </span><span class="sxs-lookup"><span data-stu-id="b7596-105">dcl\_tessellator\_partitioning {partitioning\_integer</span></span>\| <span data-ttu-id="b7596-106">partitionnement \_ pow2 </span><span class="sxs-lookup"><span data-stu-id="b7596-106">partitioning\_pow2</span></span>\|<span data-ttu-id="b7596-107">partitionnement de \_ fractions \_ impair </span><span class="sxs-lookup"><span data-stu-id="b7596-107">partitioning\_fractional\_odd</span></span>\| <span data-ttu-id="b7596-108">partitionnement \_ fractionnaire \_ pair}</span><span class="sxs-lookup"><span data-stu-id="b7596-108">partitioning\_fractional\_even}</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b7596-109">Élément</span><span class="sxs-lookup"><span data-stu-id="b7596-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="b7596-110">Description</span><span class="sxs-lookup"><span data-stu-id="b7596-110">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="b7596-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partitionnement des nombres entiers partitionnement pow2 partitionnement du partitionnement impair fractionnement \_ \| \_ \| \_ \_ \| \_ fractionnaire \_ même*</span><span class="sxs-lookup"><span data-stu-id="b7596-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partitioning\_integer\| partitioning\_pow2\|partitioning\_fractional\_odd\| partitioning\_fractional\_even*</span></span><br/> | <span data-ttu-id="b7596-112">\[dans \] le partitionnement du paveur.</span><span class="sxs-lookup"><span data-stu-id="b7596-112">\[in\] The tessellator partitioning.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b7596-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b7596-113">Remarks</span></span>

<span data-ttu-id="b7596-114">Du point de vue matériel, \_ pow2 se comporte comme un \_ entier.</span><span class="sxs-lookup"><span data-stu-id="b7596-114">From the hardware point of view, \_pow2 behaves just like \_integer.</span></span> <span data-ttu-id="b7596-115">C’est à l’auteur du nuanceur HLSL et/ou compilercode d’arrondir les TessFactors aux puissances de 2.</span><span class="sxs-lookup"><span data-stu-id="b7596-115">It is up to the HLSL shader author and/or compilercode to round TessFactors to powers of 2.</span></span>

<span data-ttu-id="b7596-116">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="b7596-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b7596-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="b7596-117">Vertex</span></span> | <span data-ttu-id="b7596-118">Forme</span><span class="sxs-lookup"><span data-stu-id="b7596-118">Hull</span></span>                 | <span data-ttu-id="b7596-119">Domain</span><span class="sxs-lookup"><span data-stu-id="b7596-119">Domain</span></span> | <span data-ttu-id="b7596-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="b7596-120">Geometry</span></span> | <span data-ttu-id="b7596-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="b7596-121">Pixel</span></span> | <span data-ttu-id="b7596-122">Compute</span><span class="sxs-lookup"><span data-stu-id="b7596-122">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="b7596-123">Section déclarations</span><span class="sxs-lookup"><span data-stu-id="b7596-123">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b7596-124">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b7596-124">Minimum Shader Model</span></span>

<span data-ttu-id="b7596-125">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="b7596-125">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b7596-126">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b7596-126">Shader Model</span></span>                                              | <span data-ttu-id="b7596-127">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b7596-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b7596-128">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="b7596-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b7596-129">Oui</span><span class="sxs-lookup"><span data-stu-id="b7596-129">yes</span></span>       |
| [<span data-ttu-id="b7596-130">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="b7596-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b7596-131">non</span><span class="sxs-lookup"><span data-stu-id="b7596-131">no</span></span>        |
| [<span data-ttu-id="b7596-132">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="b7596-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b7596-133">non</span><span class="sxs-lookup"><span data-stu-id="b7596-133">no</span></span>        |
| [<span data-ttu-id="b7596-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7596-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b7596-135">non</span><span class="sxs-lookup"><span data-stu-id="b7596-135">no</span></span>        |
| [<span data-ttu-id="b7596-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7596-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b7596-137">non</span><span class="sxs-lookup"><span data-stu-id="b7596-137">no</span></span>        |
| [<span data-ttu-id="b7596-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7596-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b7596-139">non</span><span class="sxs-lookup"><span data-stu-id="b7596-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b7596-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7596-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7596-141">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7596-141">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





