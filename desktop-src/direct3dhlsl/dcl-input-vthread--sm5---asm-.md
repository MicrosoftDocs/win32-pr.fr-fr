---
title: dcl_input vThread (SM5-ASM)
description: Déclarer des ID d’entrée de nuanceur de calcul.
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf6a7bb19feef95eae9cc153911407b206fde16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679189"
---
# <a name="dcl_input-vthread-sm5---asm"></a><span data-ttu-id="63ae0-103">\_vThread d’entrée DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="63ae0-103">dcl\_input vThread (sm5 - asm)</span></span>

<span data-ttu-id="63ae0-104">Déclarer des ID d’entrée de nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="63ae0-104">Declare compute shader input IDs.</span></span>



| <span data-ttu-id="63ae0-105">\_entrée DCL {vThreadID.xyz </span><span class="sxs-lookup"><span data-stu-id="63ae0-105">dcl\_input {vThreadID.xyz</span></span>\|<span data-ttu-id="63ae0-106">vThreadGroupID.xyz </span><span class="sxs-lookup"><span data-stu-id="63ae0-106">vThreadGroupID.xyz</span></span>\| <span data-ttu-id="63ae0-107">vThreadIDInGroup.xyz </span><span class="sxs-lookup"><span data-stu-id="63ae0-107">vThreadIDInGroup.xyz</span></span>\|<span data-ttu-id="63ae0-108">vThreadIDInGroupFlattened}</span><span class="sxs-lookup"><span data-stu-id="63ae0-108">vThreadIDInGroupFlattened}</span></span> |
|--------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="63ae0-109">Élément</span><span class="sxs-lookup"><span data-stu-id="63ae0-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="63ae0-110">Description</span><span class="sxs-lookup"><span data-stu-id="63ae0-110">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="63ae0-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span><span class="sxs-lookup"><span data-stu-id="63ae0-111"><span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*</span></span><br/> | <span data-ttu-id="63ae0-112">\[dans \] la valeur d’ID d’entier 32 bits non signé 3 composants.</span><span class="sxs-lookup"><span data-stu-id="63ae0-112">\[in\] The 3-component unsigned 32-bit integer ID value.</span></span><br/> |



 

<span data-ttu-id="63ae0-113">**l' \_ entrée DCL** est une déclaration existante dans d’autres étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="63ae0-113">**dcl\_input** is an existing declaration in other shader stages.</span></span> <span data-ttu-id="63ae0-114">Il est utilisé dans le nuanceur de calcul pour déclarer les différentes valeurs d’ID d’entier 32 non signées à 3 composants propres au nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="63ae0-114">It is used in the compute shader to declare the various 3-component unsigned 32-bit integer ID values unique to the compute shader.</span></span> <span data-ttu-id="63ae0-115">Il s'agit de :</span><span class="sxs-lookup"><span data-stu-id="63ae0-115">They are:</span></span>

-   <span data-ttu-id="63ae0-116">vThreadID.xyz</span><span class="sxs-lookup"><span data-stu-id="63ae0-116">vThreadID.xyz</span></span>
-   <span data-ttu-id="63ae0-117">vGroupID.xyz</span><span class="sxs-lookup"><span data-stu-id="63ae0-117">vGroupID.xyz</span></span>
-   <span data-ttu-id="63ae0-118">vThreadIDInGroup.xyz</span><span class="sxs-lookup"><span data-stu-id="63ae0-118">vThreadIDInGroup.xyz</span></span>
-   <span data-ttu-id="63ae0-119">vThreadIDInGroupFlattened (composant unique)</span><span class="sxs-lookup"><span data-stu-id="63ae0-119">vThreadIDInGroupFlattened (single component)</span></span>

<span data-ttu-id="63ae0-120">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="63ae0-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="63ae0-121">Sommet</span><span class="sxs-lookup"><span data-stu-id="63ae0-121">Vertex</span></span> | <span data-ttu-id="63ae0-122">Forme</span><span class="sxs-lookup"><span data-stu-id="63ae0-122">Hull</span></span> | <span data-ttu-id="63ae0-123">Domain</span><span class="sxs-lookup"><span data-stu-id="63ae0-123">Domain</span></span> | <span data-ttu-id="63ae0-124">Géométrie</span><span class="sxs-lookup"><span data-stu-id="63ae0-124">Geometry</span></span> | <span data-ttu-id="63ae0-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="63ae0-125">Pixel</span></span> | <span data-ttu-id="63ae0-126">Compute</span><span class="sxs-lookup"><span data-stu-id="63ae0-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="63ae0-127">X</span><span class="sxs-lookup"><span data-stu-id="63ae0-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="63ae0-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="63ae0-128">Minimum Shader Model</span></span>

<span data-ttu-id="63ae0-129">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="63ae0-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="63ae0-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="63ae0-130">Shader Model</span></span>                                              | <span data-ttu-id="63ae0-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="63ae0-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="63ae0-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="63ae0-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="63ae0-133">Oui</span><span class="sxs-lookup"><span data-stu-id="63ae0-133">yes</span></span>       |
| [<span data-ttu-id="63ae0-134">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="63ae0-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="63ae0-135">non</span><span class="sxs-lookup"><span data-stu-id="63ae0-135">no</span></span>        |
| [<span data-ttu-id="63ae0-136">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="63ae0-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="63ae0-137">non</span><span class="sxs-lookup"><span data-stu-id="63ae0-137">no</span></span>        |
| [<span data-ttu-id="63ae0-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63ae0-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="63ae0-139">non</span><span class="sxs-lookup"><span data-stu-id="63ae0-139">no</span></span>        |
| [<span data-ttu-id="63ae0-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63ae0-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="63ae0-141">non</span><span class="sxs-lookup"><span data-stu-id="63ae0-141">no</span></span>        |
| [<span data-ttu-id="63ae0-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63ae0-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="63ae0-143">non</span><span class="sxs-lookup"><span data-stu-id="63ae0-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="63ae0-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63ae0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63ae0-145">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63ae0-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





