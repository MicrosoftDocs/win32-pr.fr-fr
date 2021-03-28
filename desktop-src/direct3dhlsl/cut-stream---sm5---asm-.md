---
title: cut_stream (SM5-ASM)
description: Instruction de nuanceur Geometry qui termine la topologie primitive actuelle au niveau du flux spécifié, si des vertex y ont été émis, et démarre une nouvelle topologie du type déclaré par le nuanceur Geometry au niveau de ce flux.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381143"
---
# <a name="cut_stream-sm5---asm"></a><span data-ttu-id="6d99f-103">couper \_ le flux (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6d99f-103">cut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="6d99f-104">Instruction de nuanceur Geometry qui termine la topologie primitive actuelle au niveau du flux spécifié, si des vertex y ont été émis, et démarre une nouvelle topologie du type déclaré par le nuanceur Geometry au niveau de ce flux.</span><span class="sxs-lookup"><span data-stu-id="6d99f-104">The geometry shader instruction that completes the current primitive topology at the specified stream, if any vertices have been emitted to it, and starts a new topology of the type declared by the geometry shader at that stream.</span></span>



| <span data-ttu-id="6d99f-105">couper le \_ streamIndex de flux</span><span class="sxs-lookup"><span data-stu-id="6d99f-105">cut\_stream streamIndex</span></span> |
|-------------------------|



 



| <span data-ttu-id="6d99f-106">Élément</span><span class="sxs-lookup"><span data-stu-id="6d99f-106">Item</span></span>                                                                                                               | <span data-ttu-id="6d99f-107">Description</span><span class="sxs-lookup"><span data-stu-id="6d99f-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="6d99f-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="6d99f-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="6d99f-109">\[dans \] l’index de flux.</span><span class="sxs-lookup"><span data-stu-id="6d99f-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d99f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6d99f-110">Remarks</span></span>

<span data-ttu-id="6d99f-111">Lorsque cette instruction est exécutée, toute topologie précédemment émise par l’appel de nuanceur Geometry est terminée.</span><span class="sxs-lookup"><span data-stu-id="6d99f-111">When this instruction is executed, any previously emitted topology by the geometry shader invocation is completed.</span></span> <span data-ttu-id="6d99f-112">Si le nombre de vertex émis pour la topologie primitive précédente est insuffisant, ils sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="6d99f-112">If there are not enough vertices emitted for the previous primitive topology, then they are discarded.</span></span> <span data-ttu-id="6d99f-113">Étant donné que les seules topologies de sortie disponibles pour le nuanceur Geometry sont PointList, linestrip et TriangleStrip, il n’y a jamais de vertex restants.</span><span class="sxs-lookup"><span data-stu-id="6d99f-113">Because the only available output topologies for the geometry shader are pointlist, linestrip and trianglestrip, there are never any leftover vertices.</span></span>

<span data-ttu-id="6d99f-114">*streamIndex* doit être une valeur immédiate \[ comprise entre 0 et 3 \] pour un flux déclaré.</span><span class="sxs-lookup"><span data-stu-id="6d99f-114">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="6d99f-115">Après la topologie précédente, le cas échéant, cette instruction provoque le début d’une nouvelle topologie, à l’aide de la topologie déclarée comme sortie du nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="6d99f-115">After the previous topology, if any, is completed, this instruction causes a new topology to begin, using the topology declared as the output for the geometry shader.</span></span>

### <a name="restrictions"></a><span data-ttu-id="6d99f-116">Restrictions</span><span class="sxs-lookup"><span data-stu-id="6d99f-116">Restrictions</span></span>

-   <span data-ttu-id="6d99f-117">Cette instruction s’applique uniquement au nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="6d99f-117">This instruction applies to the geometry shader only.</span></span>
-   <span data-ttu-id="6d99f-118">**le \_ flux réduit** peut apparaître un nombre quelconque de fois dans le nuanceur Geometry, y compris dans le contrôle de flux.</span><span class="sxs-lookup"><span data-stu-id="6d99f-118">**cut\_stream** can appear any number of times in the geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="6d99f-119">Si le nuanceur Geometry se termine et que les vertex ont été émis, la topologie qu’ils génèrent est terminée, comme si une instruction de **\_ flux réduit** avait été exécutée en tant que dernière instruction.</span><span class="sxs-lookup"><span data-stu-id="6d99f-119">If the geometry shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut\_stream** instruction was executed as the last instruction.</span></span>
-   <span data-ttu-id="6d99f-120">Si les flux n’ont pas été déclarés, vous devez utiliser **le \_ flux** [Cut](cut--sm4---asm-.md) au lieu de Cut.</span><span class="sxs-lookup"><span data-stu-id="6d99f-120">If streams have not been declared, you must use [cut](cut--sm4---asm-.md) instead of **cut\_stream**.</span></span>

<span data-ttu-id="6d99f-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="6d99f-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6d99f-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="6d99f-122">Vertex</span></span> | <span data-ttu-id="6d99f-123">Forme</span><span class="sxs-lookup"><span data-stu-id="6d99f-123">Hull</span></span> | <span data-ttu-id="6d99f-124">Domain</span><span class="sxs-lookup"><span data-stu-id="6d99f-124">Domain</span></span> | <span data-ttu-id="6d99f-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="6d99f-125">Geometry</span></span> | <span data-ttu-id="6d99f-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="6d99f-126">Pixel</span></span> | <span data-ttu-id="6d99f-127">Compute</span><span class="sxs-lookup"><span data-stu-id="6d99f-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="6d99f-128">X</span><span class="sxs-lookup"><span data-stu-id="6d99f-128">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6d99f-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="6d99f-129">Minimum Shader Model</span></span>

<span data-ttu-id="6d99f-130">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="6d99f-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6d99f-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6d99f-131">Shader Model</span></span>                                              | <span data-ttu-id="6d99f-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="6d99f-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6d99f-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6d99f-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6d99f-134">Oui</span><span class="sxs-lookup"><span data-stu-id="6d99f-134">yes</span></span>       |
| [<span data-ttu-id="6d99f-135">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="6d99f-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6d99f-136">non</span><span class="sxs-lookup"><span data-stu-id="6d99f-136">no</span></span>        |
| [<span data-ttu-id="6d99f-137">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="6d99f-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6d99f-138">non</span><span class="sxs-lookup"><span data-stu-id="6d99f-138">no</span></span>        |
| [<span data-ttu-id="6d99f-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d99f-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6d99f-140">non</span><span class="sxs-lookup"><span data-stu-id="6d99f-140">no</span></span>        |
| [<span data-ttu-id="6d99f-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d99f-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6d99f-142">non</span><span class="sxs-lookup"><span data-stu-id="6d99f-142">no</span></span>        |
| [<span data-ttu-id="6d99f-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d99f-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6d99f-144">non</span><span class="sxs-lookup"><span data-stu-id="6d99f-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6d99f-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6d99f-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d99f-146">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d99f-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





