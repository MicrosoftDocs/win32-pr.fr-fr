---
title: dcl_hs_max_tessfactor (SM5-ASM)
description: Déclarez le maxTessFactor pour le correctif.
ms.assetid: 7EF0FD81-69FE-49F6-95DF-0C452A90A713
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd20fc8f4a3687988e8b100975f74016a45ae6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990845"
---
# <a name="dcl_hs_max_tessfactor-sm5---asm"></a><span data-ttu-id="1244f-103">DCL \_ HS \_ Max \_ tessfactor (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1244f-103">dcl\_hs\_max\_tessfactor (sm5 - asm)</span></span>

<span data-ttu-id="1244f-104">Déclarez le maxTessFactor pour le correctif.</span><span class="sxs-lookup"><span data-stu-id="1244f-104">Declare the maxTessFactor for the patch.</span></span>



| <span data-ttu-id="1244f-105">DCL \_ HS \_ Max \_ tessfactor n</span><span class="sxs-lookup"><span data-stu-id="1244f-105">dcl\_hs\_max\_tessfactor n</span></span> |
|----------------------------|



 



| <span data-ttu-id="1244f-106">Élément</span><span class="sxs-lookup"><span data-stu-id="1244f-106">Item</span></span>                                                   | <span data-ttu-id="1244f-107">Description</span><span class="sxs-lookup"><span data-stu-id="1244f-107">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="1244f-108"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="1244f-108"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="1244f-109">\[dans \] le maxTessFactor.</span><span class="sxs-lookup"><span data-stu-id="1244f-109">\[in\] The maxTessFactor.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1244f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1244f-110">Remarks</span></span>

<span data-ttu-id="1244f-111">MaxTessFactor est une valeur float32 comprise dans la plage {1,0... 64,0}.</span><span class="sxs-lookup"><span data-stu-id="1244f-111">The maxTessFactor is a float32 value in the range {1.0 ... 64.0}.</span></span>

<span data-ttu-id="1244f-112">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="1244f-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1244f-113">Sommet</span><span class="sxs-lookup"><span data-stu-id="1244f-113">Vertex</span></span> | <span data-ttu-id="1244f-114">Forme</span><span class="sxs-lookup"><span data-stu-id="1244f-114">Hull</span></span> | <span data-ttu-id="1244f-115">Domain</span><span class="sxs-lookup"><span data-stu-id="1244f-115">Domain</span></span> | <span data-ttu-id="1244f-116">Géométrie</span><span class="sxs-lookup"><span data-stu-id="1244f-116">Geometry</span></span> | <span data-ttu-id="1244f-117">Pixel</span><span class="sxs-lookup"><span data-stu-id="1244f-117">Pixel</span></span> | <span data-ttu-id="1244f-118">Compute</span><span class="sxs-lookup"><span data-stu-id="1244f-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="1244f-119">X</span><span class="sxs-lookup"><span data-stu-id="1244f-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1244f-120">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1244f-120">Minimum Shader Model</span></span>

<span data-ttu-id="1244f-121">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="1244f-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1244f-122">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1244f-122">Shader Model</span></span>                                              | <span data-ttu-id="1244f-123">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="1244f-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1244f-124">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1244f-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1244f-125">Oui</span><span class="sxs-lookup"><span data-stu-id="1244f-125">yes</span></span>       |
| [<span data-ttu-id="1244f-126">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="1244f-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1244f-127">non</span><span class="sxs-lookup"><span data-stu-id="1244f-127">no</span></span>        |
| [<span data-ttu-id="1244f-128">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="1244f-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1244f-129">non</span><span class="sxs-lookup"><span data-stu-id="1244f-129">no</span></span>        |
| [<span data-ttu-id="1244f-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1244f-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1244f-131">non</span><span class="sxs-lookup"><span data-stu-id="1244f-131">no</span></span>        |
| [<span data-ttu-id="1244f-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1244f-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1244f-133">non</span><span class="sxs-lookup"><span data-stu-id="1244f-133">no</span></span>        |
| [<span data-ttu-id="1244f-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1244f-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1244f-135">non</span><span class="sxs-lookup"><span data-stu-id="1244f-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1244f-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1244f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1244f-137">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1244f-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





