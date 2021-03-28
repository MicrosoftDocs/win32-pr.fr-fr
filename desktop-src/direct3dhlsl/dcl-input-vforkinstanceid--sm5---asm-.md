---
title: dcl_input vForkInstanceID (SM5-ASM)
description: Déclarez l’ID d’instance dans une phase de bifurcation de nuanceur de coque.
ms.assetid: AA73E8B6-C6D7-4483-B46E-C733341F552C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ce5fcf111a59abb0c9a6ccb36de63d94dcb11e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030623"
---
# <a name="dcl_input-vforkinstanceid-sm5---asm"></a><span data-ttu-id="6b062-103">\_vForkInstanceID d’entrée DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6b062-103">dcl\_input vForkInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="6b062-104">Déclarez l’ID d’instance dans une phase de bifurcation de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="6b062-104">Declare the instance ID in a hull shader fork phase.</span></span>



| <span data-ttu-id="6b062-105">\_vForkInstanceID d’entrée DCL</span><span class="sxs-lookup"><span data-stu-id="6b062-105">dcl\_input vForkInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="6b062-106">Élément</span><span class="sxs-lookup"><span data-stu-id="6b062-106">Item</span></span>                                                                                                                               | <span data-ttu-id="6b062-107">Description</span><span class="sxs-lookup"><span data-stu-id="6b062-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="6b062-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span><span class="sxs-lookup"><span data-stu-id="6b062-108"><span id="vForkInstanceID"></span><span id="vforkinstanceid"></span><span id="VFORKINSTANCEID"></span>*vForkInstanceID*</span></span><br/> | <span data-ttu-id="6b062-109">\[dans \] l’ID d’instance.</span><span class="sxs-lookup"><span data-stu-id="6b062-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6b062-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6b062-110">Remarks</span></span>

<span data-ttu-id="6b062-111">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="6b062-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6b062-112">Sommet</span><span class="sxs-lookup"><span data-stu-id="6b062-112">Vertex</span></span> | <span data-ttu-id="6b062-113">Forme</span><span class="sxs-lookup"><span data-stu-id="6b062-113">Hull</span></span> | <span data-ttu-id="6b062-114">Domain</span><span class="sxs-lookup"><span data-stu-id="6b062-114">Domain</span></span> | <span data-ttu-id="6b062-115">Géométrie</span><span class="sxs-lookup"><span data-stu-id="6b062-115">Geometry</span></span> | <span data-ttu-id="6b062-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="6b062-116">Pixel</span></span> | <span data-ttu-id="6b062-117">Compute</span><span class="sxs-lookup"><span data-stu-id="6b062-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="6b062-118">X</span><span class="sxs-lookup"><span data-stu-id="6b062-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6b062-119">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="6b062-119">Minimum Shader Model</span></span>

<span data-ttu-id="6b062-120">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="6b062-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6b062-121">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6b062-121">Shader Model</span></span>                                              | <span data-ttu-id="6b062-122">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="6b062-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6b062-123">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6b062-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6b062-124">Oui</span><span class="sxs-lookup"><span data-stu-id="6b062-124">yes</span></span>       |
| [<span data-ttu-id="6b062-125">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="6b062-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6b062-126">non</span><span class="sxs-lookup"><span data-stu-id="6b062-126">no</span></span>        |
| [<span data-ttu-id="6b062-127">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="6b062-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6b062-128">non</span><span class="sxs-lookup"><span data-stu-id="6b062-128">no</span></span>        |
| [<span data-ttu-id="6b062-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b062-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6b062-130">non</span><span class="sxs-lookup"><span data-stu-id="6b062-130">no</span></span>        |
| [<span data-ttu-id="6b062-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b062-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6b062-132">non</span><span class="sxs-lookup"><span data-stu-id="6b062-132">no</span></span>        |
| [<span data-ttu-id="6b062-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b062-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6b062-134">non</span><span class="sxs-lookup"><span data-stu-id="6b062-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6b062-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b062-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b062-136">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b062-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





