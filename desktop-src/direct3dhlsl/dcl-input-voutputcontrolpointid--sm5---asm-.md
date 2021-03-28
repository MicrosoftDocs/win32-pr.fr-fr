---
title: dcl_input vOutputControlPointID (SM5-ASM)
description: Déclarez l’ID du point de contrôle de sortie dans une phase du point de contrôle de nuanceur de coque.
ms.assetid: 376ECA4F-DD71-4466-8A9D-E92A536832BC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cee49a8a825f25b0fbbccff027d5ad1b9ade514
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030622"
---
# <a name="dcl_input-voutputcontrolpointid-sm5---asm"></a><span data-ttu-id="ce6d0-103">\_vOutputControlPointID d’entrée DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ce6d0-103">dcl\_input vOutputControlPointID (sm5 - asm)</span></span>

<span data-ttu-id="ce6d0-104">Déclarez l’ID du point de contrôle de sortie dans une phase du point de contrôle de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="ce6d0-104">Declare the output control point ID in a hull shader control point phase.</span></span>



| <span data-ttu-id="ce6d0-105">\_vOutputControlPointID d’entrée DCL</span><span class="sxs-lookup"><span data-stu-id="ce6d0-105">dcl\_input vOutputControlPointID</span></span> |
|----------------------------------|



 



| <span data-ttu-id="ce6d0-106">Élément</span><span class="sxs-lookup"><span data-stu-id="ce6d0-106">Item</span></span>                                                                                                                                                       | <span data-ttu-id="ce6d0-107">Description</span><span class="sxs-lookup"><span data-stu-id="ce6d0-107">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="ce6d0-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span><span class="sxs-lookup"><span data-stu-id="ce6d0-108"><span id="vOutputControlPointID"></span><span id="voutputcontrolpointid"></span><span id="VOUTPUTCONTROLPOINTID"></span>*vOutputControlPointID*</span></span><br/> | <span data-ttu-id="ce6d0-109">\[dans \] l’ID du point de contrôle de sortie.</span><span class="sxs-lookup"><span data-stu-id="ce6d0-109">\[in\] The output control point ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce6d0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ce6d0-110">Remarks</span></span>

<span data-ttu-id="ce6d0-111">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="ce6d0-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ce6d0-112">Sommet</span><span class="sxs-lookup"><span data-stu-id="ce6d0-112">Vertex</span></span> | <span data-ttu-id="ce6d0-113">Forme</span><span class="sxs-lookup"><span data-stu-id="ce6d0-113">Hull</span></span> | <span data-ttu-id="ce6d0-114">Domain</span><span class="sxs-lookup"><span data-stu-id="ce6d0-114">Domain</span></span> | <span data-ttu-id="ce6d0-115">Géométrie</span><span class="sxs-lookup"><span data-stu-id="ce6d0-115">Geometry</span></span> | <span data-ttu-id="ce6d0-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="ce6d0-116">Pixel</span></span> | <span data-ttu-id="ce6d0-117">Compute</span><span class="sxs-lookup"><span data-stu-id="ce6d0-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="ce6d0-118">X</span><span class="sxs-lookup"><span data-stu-id="ce6d0-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ce6d0-119">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="ce6d0-119">Minimum Shader Model</span></span>

<span data-ttu-id="ce6d0-120">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="ce6d0-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ce6d0-121">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="ce6d0-121">Shader Model</span></span>                                              | <span data-ttu-id="ce6d0-122">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="ce6d0-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ce6d0-123">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="ce6d0-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ce6d0-124">Oui</span><span class="sxs-lookup"><span data-stu-id="ce6d0-124">yes</span></span>       |
| [<span data-ttu-id="ce6d0-125">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="ce6d0-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ce6d0-126">non</span><span class="sxs-lookup"><span data-stu-id="ce6d0-126">no</span></span>        |
| [<span data-ttu-id="ce6d0-127">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="ce6d0-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ce6d0-128">non</span><span class="sxs-lookup"><span data-stu-id="ce6d0-128">no</span></span>        |
| [<span data-ttu-id="ce6d0-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce6d0-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ce6d0-130">non</span><span class="sxs-lookup"><span data-stu-id="ce6d0-130">no</span></span>        |
| [<span data-ttu-id="ce6d0-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce6d0-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ce6d0-132">non</span><span class="sxs-lookup"><span data-stu-id="ce6d0-132">no</span></span>        |
| [<span data-ttu-id="ce6d0-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce6d0-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ce6d0-134">non</span><span class="sxs-lookup"><span data-stu-id="ce6d0-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ce6d0-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce6d0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce6d0-136">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce6d0-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





