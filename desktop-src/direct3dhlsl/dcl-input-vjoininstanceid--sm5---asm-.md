---
title: dcl_input vJoinInstanceID (SM5-ASM)
description: Déclarez l’ID d’instance dans une phase de jointure de nuanceur de coque.
ms.assetid: 2EABB24A-7ED7-460D-A2AD-D2C40DCCB2DC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bae9351fc7183aa37cd660c265aab803f4661e9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940580"
---
# <a name="dcl_input-vjoininstanceid-sm5---asm"></a><span data-ttu-id="e4aaf-103">\_vJoinInstanceID d’entrée DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e4aaf-103">dcl\_input vJoinInstanceID (sm5 - asm)</span></span>

<span data-ttu-id="e4aaf-104">Déclarez l’ID d’instance dans une phase de jointure de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="e4aaf-104">Declare the instance ID in a hull shader join phase.</span></span>



| <span data-ttu-id="e4aaf-105">\_vJoinInstanceID d’entrée DCL</span><span class="sxs-lookup"><span data-stu-id="e4aaf-105">dcl\_input vJoinInstanceID</span></span> |
|----------------------------|



 



| <span data-ttu-id="e4aaf-106">Élément</span><span class="sxs-lookup"><span data-stu-id="e4aaf-106">Item</span></span>                                                                                                                               | <span data-ttu-id="e4aaf-107">Description</span><span class="sxs-lookup"><span data-stu-id="e4aaf-107">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="e4aaf-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*vJoinInstanceID*</span><span class="sxs-lookup"><span data-stu-id="e4aaf-108"><span id="vJoinInstanceID"></span><span id="vjoininstanceid"></span><span id="VJOININSTANCEID"></span>*vJoinInstanceID*</span></span><br/> | <span data-ttu-id="e4aaf-109">\[dans \] l’ID d’instance.</span><span class="sxs-lookup"><span data-stu-id="e4aaf-109">\[in\] The instance ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e4aaf-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e4aaf-110">Remarks</span></span>

<span data-ttu-id="e4aaf-111">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="e4aaf-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e4aaf-112">Sommet</span><span class="sxs-lookup"><span data-stu-id="e4aaf-112">Vertex</span></span> | <span data-ttu-id="e4aaf-113">Forme</span><span class="sxs-lookup"><span data-stu-id="e4aaf-113">Hull</span></span> | <span data-ttu-id="e4aaf-114">Domain</span><span class="sxs-lookup"><span data-stu-id="e4aaf-114">Domain</span></span> | <span data-ttu-id="e4aaf-115">Géométrie</span><span class="sxs-lookup"><span data-stu-id="e4aaf-115">Geometry</span></span> | <span data-ttu-id="e4aaf-116">Pixel</span><span class="sxs-lookup"><span data-stu-id="e4aaf-116">Pixel</span></span> | <span data-ttu-id="e4aaf-117">Compute</span><span class="sxs-lookup"><span data-stu-id="e4aaf-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="e4aaf-118">X</span><span class="sxs-lookup"><span data-stu-id="e4aaf-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e4aaf-119">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="e4aaf-119">Minimum Shader Model</span></span>

<span data-ttu-id="e4aaf-120">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="e4aaf-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e4aaf-121">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="e4aaf-121">Shader Model</span></span>                                              | <span data-ttu-id="e4aaf-122">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="e4aaf-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e4aaf-123">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e4aaf-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e4aaf-124">Oui</span><span class="sxs-lookup"><span data-stu-id="e4aaf-124">yes</span></span>       |
| [<span data-ttu-id="e4aaf-125">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="e4aaf-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e4aaf-126">non</span><span class="sxs-lookup"><span data-stu-id="e4aaf-126">no</span></span>        |
| [<span data-ttu-id="e4aaf-127">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="e4aaf-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e4aaf-128">non</span><span class="sxs-lookup"><span data-stu-id="e4aaf-128">no</span></span>        |
| [<span data-ttu-id="e4aaf-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4aaf-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e4aaf-130">non</span><span class="sxs-lookup"><span data-stu-id="e4aaf-130">no</span></span>        |
| [<span data-ttu-id="e4aaf-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4aaf-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e4aaf-132">non</span><span class="sxs-lookup"><span data-stu-id="e4aaf-132">no</span></span>        |
| [<span data-ttu-id="e4aaf-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4aaf-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e4aaf-134">non</span><span class="sxs-lookup"><span data-stu-id="e4aaf-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e4aaf-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e4aaf-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4aaf-136">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4aaf-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





