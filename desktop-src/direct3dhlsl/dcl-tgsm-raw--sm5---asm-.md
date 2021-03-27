---
title: dcl_tgsm_raw (SM5-ASM)
description: Déclarez une référence à une région d’espace mémoire partagée disponible pour le groupe de threads du nuanceur de calcul.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679177"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a><span data-ttu-id="f36cc-103">DCL \_ TGSM \_ brute (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f36cc-103">dcl\_tgsm\_raw (sm5 - asm)</span></span>

<span data-ttu-id="f36cc-104">Déclarez une référence à une région d’espace mémoire partagée disponible pour le groupe de threads du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="f36cc-104">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span>



| <span data-ttu-id="f36cc-105">DCL \_ TGSM \_ brute g \# , byteCount</span><span class="sxs-lookup"><span data-stu-id="f36cc-105">dcl\_tgsm\_raw g\#, byteCount</span></span> |
|-------------------------------|



 



| <span data-ttu-id="f36cc-106">Élément</span><span class="sxs-lookup"><span data-stu-id="f36cc-106">Item</span></span>                                                                                                       | <span data-ttu-id="f36cc-107">Description</span><span class="sxs-lookup"><span data-stu-id="f36cc-107">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f36cc-108"><span id="g_"></span><span id="G_"></span>*activée\#*</span><span class="sxs-lookup"><span data-stu-id="f36cc-108"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                 | <span data-ttu-id="f36cc-109">\[dans \] une référence à un bloc de taille *byteCount* de mémoire partagée non typée.</span><span class="sxs-lookup"><span data-stu-id="f36cc-109">\[in\] A reference to a block of size *byteCount* of untyped shared memory.</span></span> <br/> |
| <span data-ttu-id="f36cc-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span><span class="sxs-lookup"><span data-stu-id="f36cc-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span></span><br/> | <span data-ttu-id="f36cc-111">\[dans \] doit être un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="f36cc-111">\[in\] Must be a multiple of 4.</span></span> <br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="f36cc-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f36cc-112">Remarks</span></span>

<span data-ttu-id="f36cc-113">Le stockage total pour tous les g \# doit être <= la quantité de mémoire partagée disponible par groupe de threads, soit 32KO.</span><span class="sxs-lookup"><span data-stu-id="f36cc-113">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB.</span></span>

<span data-ttu-id="f36cc-114">Dans un cas extrême, vous pouvez déclarer 8192 g s au total \# , chacun avec un *byteCount* de 4.</span><span class="sxs-lookup"><span data-stu-id="f36cc-114">In an extreme case, you can declare 8192 total g\# s, each with a *byteCount* of 4.</span></span>

<span data-ttu-id="f36cc-115">Dans l’autre extrême, vous pouvez déclarer un g unique \# avec un *byteCount* de 32768.</span><span class="sxs-lookup"><span data-stu-id="f36cc-115">In the opposite extreme, you can declare a single g\# with a *byteCount* of 32768.</span></span>

> [!Note]  
> <span data-ttu-id="f36cc-116">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge la [ \_ TGSM \_ structurée DCL](dcl-tgsm-structured--sm5---asm-.md), mais pas la **\_ TGSM \_ brute du DCL**.</span><span class="sxs-lookup"><span data-stu-id="f36cc-116">cs\_4\_0 and cs\_4\_1 supports [dcl\_tgsm\_structured](dcl-tgsm-structured--sm5---asm-.md), but not **dcl\_tgsm\_raw**.</span></span>

 

<span data-ttu-id="f36cc-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="f36cc-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f36cc-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="f36cc-118">Vertex</span></span> | <span data-ttu-id="f36cc-119">Forme</span><span class="sxs-lookup"><span data-stu-id="f36cc-119">Hull</span></span> | <span data-ttu-id="f36cc-120">Domain</span><span class="sxs-lookup"><span data-stu-id="f36cc-120">Domain</span></span> | <span data-ttu-id="f36cc-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f36cc-121">Geometry</span></span> | <span data-ttu-id="f36cc-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="f36cc-122">Pixel</span></span> | <span data-ttu-id="f36cc-123">Compute</span><span class="sxs-lookup"><span data-stu-id="f36cc-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="f36cc-124">X</span><span class="sxs-lookup"><span data-stu-id="f36cc-124">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f36cc-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f36cc-125">Minimum Shader Model</span></span>

<span data-ttu-id="f36cc-126">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="f36cc-126">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f36cc-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f36cc-127">Shader Model</span></span>                                              | <span data-ttu-id="f36cc-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f36cc-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f36cc-129">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f36cc-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f36cc-130">Oui</span><span class="sxs-lookup"><span data-stu-id="f36cc-130">yes</span></span>       |
| [<span data-ttu-id="f36cc-131">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="f36cc-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f36cc-132">non</span><span class="sxs-lookup"><span data-stu-id="f36cc-132">no</span></span>        |
| [<span data-ttu-id="f36cc-133">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f36cc-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f36cc-134">non</span><span class="sxs-lookup"><span data-stu-id="f36cc-134">no</span></span>        |
| [<span data-ttu-id="f36cc-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f36cc-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f36cc-136">non</span><span class="sxs-lookup"><span data-stu-id="f36cc-136">no</span></span>        |
| [<span data-ttu-id="f36cc-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f36cc-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f36cc-138">non</span><span class="sxs-lookup"><span data-stu-id="f36cc-138">no</span></span>        |
| [<span data-ttu-id="f36cc-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f36cc-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f36cc-140">non</span><span class="sxs-lookup"><span data-stu-id="f36cc-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f36cc-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f36cc-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f36cc-142">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f36cc-142">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





