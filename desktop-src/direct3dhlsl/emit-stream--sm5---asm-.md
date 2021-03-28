---
title: emit_stream (SM5-ASM)
description: Émet un vertex vers un flux donné.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381160"
---
# <a name="emit_stream-sm5---asm"></a><span data-ttu-id="bfab2-103">émettre \_ un flux (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="bfab2-103">emit\_stream (sm5 - asm)</span></span>

<span data-ttu-id="bfab2-104">Émet un vertex vers un flux donné.</span><span class="sxs-lookup"><span data-stu-id="bfab2-104">Emit a vertex to a given stream.</span></span>



| <span data-ttu-id="bfab2-105">émettre un \_ flux streamIndex</span><span class="sxs-lookup"><span data-stu-id="bfab2-105">emit\_stream streamIndex</span></span> |
|--------------------------|



 



| <span data-ttu-id="bfab2-106">Élément</span><span class="sxs-lookup"><span data-stu-id="bfab2-106">Item</span></span>                                                                                                               | <span data-ttu-id="bfab2-107">Description</span><span class="sxs-lookup"><span data-stu-id="bfab2-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="bfab2-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span><span class="sxs-lookup"><span data-stu-id="bfab2-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="bfab2-109">\[dans \] l’index de flux.</span><span class="sxs-lookup"><span data-stu-id="bfab2-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bfab2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bfab2-110">Remarks</span></span>

<span data-ttu-id="bfab2-111">Cette instruction entraîne la lecture de tous les registres o déclarés \# pour le flux donné à partir du nuanceur Geometry pour générer un vertex.</span><span class="sxs-lookup"><span data-stu-id="bfab2-111">This instruction causes all declared o\# registers for the given stream to be read out of the geometry shader to generate a vertex.</span></span> <span data-ttu-id="bfab2-112">Après l’émission, toutes les données de tous les registres de sortie pour tous les flux de données deviennent non initialisés, pas seulement le flux émis vers.</span><span class="sxs-lookup"><span data-stu-id="bfab2-112">Afer the emit, all data in all output registers for all streams become uninitialized, not just the stream emitted to.</span></span>

<span data-ttu-id="bfab2-113">*streamIndex* doit être une valeur immédiate \[ comprise entre 0 et 3 \] pour un flux déclaré.</span><span class="sxs-lookup"><span data-stu-id="bfab2-113">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="bfab2-114">À mesure que plusieurs appels de **\_ flux d’émission** sont émis, des primitives sont générées.</span><span class="sxs-lookup"><span data-stu-id="bfab2-114">As multiple **emit\_stream** calls are issued, primitives are generated.</span></span>

### <a name="restrictions"></a><span data-ttu-id="bfab2-115">Restrictions</span><span class="sxs-lookup"><span data-stu-id="bfab2-115">Restrictions</span></span>

-   <span data-ttu-id="bfab2-116">**un \_ flux d’émission** peut apparaître un nombre quelconque de fois dans un nuanceur Geometry, y compris dans le contrôle de flux.</span><span class="sxs-lookup"><span data-stu-id="bfab2-116">**emit\_stream** can appear any number of times in a geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="bfab2-117">Si les flux n’ont pas été déclarés, vous devez utiliser [Emit](emit--sm4---asm-.md) au lieu d' **émettre le \_ flux**.</span><span class="sxs-lookup"><span data-stu-id="bfab2-117">If streams have not been declared, then you must use [emit](emit--sm4---asm-.md) instead of **emit\_stream**.</span></span>

<span data-ttu-id="bfab2-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="bfab2-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bfab2-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="bfab2-119">Vertex</span></span> | <span data-ttu-id="bfab2-120">Forme</span><span class="sxs-lookup"><span data-stu-id="bfab2-120">Hull</span></span> | <span data-ttu-id="bfab2-121">Domain</span><span class="sxs-lookup"><span data-stu-id="bfab2-121">Domain</span></span> | <span data-ttu-id="bfab2-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="bfab2-122">Geometry</span></span> | <span data-ttu-id="bfab2-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="bfab2-123">Pixel</span></span> | <span data-ttu-id="bfab2-124">Compute</span><span class="sxs-lookup"><span data-stu-id="bfab2-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="bfab2-125">X</span><span class="sxs-lookup"><span data-stu-id="bfab2-125">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bfab2-126">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="bfab2-126">Minimum Shader Model</span></span>

<span data-ttu-id="bfab2-127">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="bfab2-127">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="bfab2-128">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="bfab2-128">Shader Model</span></span>                                              | <span data-ttu-id="bfab2-129">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="bfab2-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bfab2-130">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="bfab2-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bfab2-131">Oui</span><span class="sxs-lookup"><span data-stu-id="bfab2-131">yes</span></span>       |
| [<span data-ttu-id="bfab2-132">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="bfab2-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bfab2-133">non</span><span class="sxs-lookup"><span data-stu-id="bfab2-133">no</span></span>        |
| [<span data-ttu-id="bfab2-134">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="bfab2-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bfab2-135">non</span><span class="sxs-lookup"><span data-stu-id="bfab2-135">no</span></span>        |
| [<span data-ttu-id="bfab2-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfab2-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bfab2-137">non</span><span class="sxs-lookup"><span data-stu-id="bfab2-137">no</span></span>        |
| [<span data-ttu-id="bfab2-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfab2-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bfab2-139">non</span><span class="sxs-lookup"><span data-stu-id="bfab2-139">no</span></span>        |
| [<span data-ttu-id="bfab2-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfab2-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bfab2-141">non</span><span class="sxs-lookup"><span data-stu-id="bfab2-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bfab2-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bfab2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfab2-143">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfab2-143">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





