---
title: dcl_input_control_point_count (SM5-ASM)
description: Déclarez le nombre de points de contrôle d’entrée du nuanceur de coque dans la section Déclaration du nuanceur de coque.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381237"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a><span data-ttu-id="de55e-103">\_nombre de \_ points de contrôle d’entrée DCL \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="de55e-103">dcl\_input\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="de55e-104">Déclarez le nombre de points de contrôle d’entrée du nuanceur de coque dans la section Déclaration du nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="de55e-104">Declare the hull shader input control point count in the hull shader declaration section.</span></span>



| <span data-ttu-id="de55e-105">\_nombre de points de contrôle d’entrée DCL \_ \_ \_ {1.. 32}</span><span class="sxs-lookup"><span data-stu-id="de55e-105">dcl\_input\_control\_point\_count {1..32}</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="de55e-106">Élément</span><span class="sxs-lookup"><span data-stu-id="de55e-106">Item</span></span>                                                   | <span data-ttu-id="de55e-107">Description</span><span class="sxs-lookup"><span data-stu-id="de55e-107">Description</span></span>                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="de55e-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="de55e-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="de55e-109">\[dans \] le nombre de points de contrôle d’entrée.</span><span class="sxs-lookup"><span data-stu-id="de55e-109">\[in\] The input control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de55e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="de55e-110">Remarks</span></span>

<span data-ttu-id="de55e-111">Au moins 1 point de contrôle d’entrée est requis ; Il peut être vide s’il n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="de55e-111">At least 1 input control point is required; it can be empty if it is not needed.</span></span>

<span data-ttu-id="de55e-112">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="de55e-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="de55e-113">Sommet</span><span class="sxs-lookup"><span data-stu-id="de55e-113">Vertex</span></span> | <span data-ttu-id="de55e-114">Forme</span><span class="sxs-lookup"><span data-stu-id="de55e-114">Hull</span></span> | <span data-ttu-id="de55e-115">Domain</span><span class="sxs-lookup"><span data-stu-id="de55e-115">Domain</span></span> | <span data-ttu-id="de55e-116">Géométrie</span><span class="sxs-lookup"><span data-stu-id="de55e-116">Geometry</span></span> | <span data-ttu-id="de55e-117">Pixel</span><span class="sxs-lookup"><span data-stu-id="de55e-117">Pixel</span></span> | <span data-ttu-id="de55e-118">Compute</span><span class="sxs-lookup"><span data-stu-id="de55e-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="de55e-119">X</span><span class="sxs-lookup"><span data-stu-id="de55e-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="de55e-120">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="de55e-120">Minimum Shader Model</span></span>

<span data-ttu-id="de55e-121">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="de55e-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="de55e-122">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="de55e-122">Shader Model</span></span>                                              | <span data-ttu-id="de55e-123">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="de55e-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="de55e-124">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="de55e-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="de55e-125">Oui</span><span class="sxs-lookup"><span data-stu-id="de55e-125">yes</span></span>       |
| [<span data-ttu-id="de55e-126">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="de55e-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="de55e-127">non</span><span class="sxs-lookup"><span data-stu-id="de55e-127">no</span></span>        |
| [<span data-ttu-id="de55e-128">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="de55e-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="de55e-129">non</span><span class="sxs-lookup"><span data-stu-id="de55e-129">no</span></span>        |
| [<span data-ttu-id="de55e-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de55e-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="de55e-131">non</span><span class="sxs-lookup"><span data-stu-id="de55e-131">no</span></span>        |
| [<span data-ttu-id="de55e-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de55e-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="de55e-133">non</span><span class="sxs-lookup"><span data-stu-id="de55e-133">no</span></span>        |
| [<span data-ttu-id="de55e-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de55e-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="de55e-135">non</span><span class="sxs-lookup"><span data-stu-id="de55e-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="de55e-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de55e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de55e-137">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de55e-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





