---
title: dcl_tgsm_structured (SM5-ASM)
description: Déclarez une référence à une région d’espace mémoire partagée disponible pour le groupe de threads du nuanceur de calcul. La mémoire est affichée sous la forme d’un tableau de structures.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990744"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a><span data-ttu-id="42fd2-104">DCL \_ TGSM \_ structurée (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="42fd2-104">dcl\_tgsm\_structured (sm5 - asm)</span></span>

<span data-ttu-id="42fd2-105">Déclarez une référence à une région d’espace mémoire partagée disponible pour le groupe de threads du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="42fd2-105">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span> <span data-ttu-id="42fd2-106">La mémoire est affichée sous la forme d’un tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="42fd2-106">The memory is viewed as an array of structures.</span></span>



| <span data-ttu-id="42fd2-107">DCL \_ TGSM \_ structuré g \# , structByteStride, structCount</span><span class="sxs-lookup"><span data-stu-id="42fd2-107">dcl\_tgsm\_structured g\#, structByteStride, structCount</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="42fd2-108">Élément</span><span class="sxs-lookup"><span data-stu-id="42fd2-108">Item</span></span>                                                                                                                                   | <span data-ttu-id="42fd2-109">Description</span><span class="sxs-lookup"><span data-stu-id="42fd2-109">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42fd2-110"><span id="g_"></span><span id="G_"></span>*activée\#*</span><span class="sxs-lookup"><span data-stu-id="42fd2-110"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                                             | <span data-ttu-id="42fd2-111">\[dans \] une référence à un bloc de mémoire partagée de taille *structByteStride* \* *structCount* octets.</span><span class="sxs-lookup"><span data-stu-id="42fd2-111">\[in\] A reference to a block of shared memory of size *structByteStride* \* *structCount* bytes.</span></span> <br/> |
| <span data-ttu-id="42fd2-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="42fd2-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="42fd2-113">\[dans \] la structure Stride.</span><span class="sxs-lookup"><span data-stu-id="42fd2-113">\[in\] The structure stride.</span></span> <span data-ttu-id="42fd2-114">Cette valeur est un uint en octets et doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="42fd2-114">This value is a uint in bytes and must be a multiple of 4.</span></span> <br/>           |
| <span data-ttu-id="42fd2-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span><span class="sxs-lookup"><span data-stu-id="42fd2-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span></span><br/>                     | <span data-ttu-id="42fd2-116">\[dans \] le nombre de structures.</span><span class="sxs-lookup"><span data-stu-id="42fd2-116">\[in\] The number of structures.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="42fd2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="42fd2-117">Remarks</span></span>

<span data-ttu-id="42fd2-118">Le stockage total pour tous les g \# doit être <= la quantité de mémoire partagée disponible par groupe de threads, soit 32 Ko, soit les valeurs scalaires de 8192 32 bits.</span><span class="sxs-lookup"><span data-stu-id="42fd2-118">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB, or 8192 32-bit scalars.</span></span>

<span data-ttu-id="42fd2-119">Dans un cas extrême, vous pouvez déclarer 8192 g s au total \# , si chacun a un *structByteStride* de 4 et un *structCount* de 1.</span><span class="sxs-lookup"><span data-stu-id="42fd2-119">In an extreme case, you can declare 8192 total g\# s, if each has a *structByteStride* of 4 and a *structCount* of 1.</span></span>

<span data-ttu-id="42fd2-120">À l’opposé, vous pouvez déclarer un g unique \# avec une structure Stride de 32KO et un nombre de structures de 1.</span><span class="sxs-lookup"><span data-stu-id="42fd2-120">In the opposite extreme, you can declare a single g\# with a structure stride of 32kB and a structure count of 1.</span></span>

<span data-ttu-id="42fd2-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="42fd2-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="42fd2-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="42fd2-122">Vertex</span></span> | <span data-ttu-id="42fd2-123">Forme</span><span class="sxs-lookup"><span data-stu-id="42fd2-123">Hull</span></span> | <span data-ttu-id="42fd2-124">Domain</span><span class="sxs-lookup"><span data-stu-id="42fd2-124">Domain</span></span> | <span data-ttu-id="42fd2-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="42fd2-125">Geometry</span></span> | <span data-ttu-id="42fd2-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="42fd2-126">Pixel</span></span> | <span data-ttu-id="42fd2-127">Compute</span><span class="sxs-lookup"><span data-stu-id="42fd2-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="42fd2-128">X</span><span class="sxs-lookup"><span data-stu-id="42fd2-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="42fd2-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="42fd2-129">Minimum Shader Model</span></span>

<span data-ttu-id="42fd2-130">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="42fd2-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="42fd2-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="42fd2-131">Shader Model</span></span>                                              | <span data-ttu-id="42fd2-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="42fd2-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="42fd2-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="42fd2-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="42fd2-134">Oui</span><span class="sxs-lookup"><span data-stu-id="42fd2-134">yes</span></span>       |
| [<span data-ttu-id="42fd2-135">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="42fd2-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="42fd2-136">non</span><span class="sxs-lookup"><span data-stu-id="42fd2-136">no</span></span>        |
| [<span data-ttu-id="42fd2-137">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="42fd2-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="42fd2-138">non</span><span class="sxs-lookup"><span data-stu-id="42fd2-138">no</span></span>        |
| [<span data-ttu-id="42fd2-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42fd2-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="42fd2-140">non</span><span class="sxs-lookup"><span data-stu-id="42fd2-140">no</span></span>        |
| [<span data-ttu-id="42fd2-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42fd2-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="42fd2-142">non</span><span class="sxs-lookup"><span data-stu-id="42fd2-142">no</span></span>        |
| [<span data-ttu-id="42fd2-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42fd2-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="42fd2-144">non</span><span class="sxs-lookup"><span data-stu-id="42fd2-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="42fd2-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="42fd2-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42fd2-146">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42fd2-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





