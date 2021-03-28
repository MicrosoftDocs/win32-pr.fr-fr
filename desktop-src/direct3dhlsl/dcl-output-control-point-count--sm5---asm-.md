---
title: dcl_output_control_point_count (SM5-ASM)
description: Déclare le nombre de points de contrôle de sortie du nuanceur de coque.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030620"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a><span data-ttu-id="5eca3-103">\_nombre de \_ \_ points de contrôle de sortie DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5eca3-103">dcl\_output\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="5eca3-104">Déclare le nombre de points de contrôle de sortie du nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="5eca3-104">Declares the hull shader output control point count.</span></span>



| <span data-ttu-id="5eca3-105">\_nombre de points de contrôle de sortie DCL \_ \_ \_ N</span><span class="sxs-lookup"><span data-stu-id="5eca3-105">dcl\_output\_control\_point\_count N</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="5eca3-106">Élément</span><span class="sxs-lookup"><span data-stu-id="5eca3-106">Item</span></span>                                                   | <span data-ttu-id="5eca3-107">Description</span><span class="sxs-lookup"><span data-stu-id="5eca3-107">Description</span></span>                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eca3-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="5eca3-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="5eca3-109">\[\]valeur entière comprise entre 0 et 32 qui spécifie le nombre de points de contrôle de sortie.</span><span class="sxs-lookup"><span data-stu-id="5eca3-109">\[in\] An integer value from 0 to 32 that specifies the output control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5eca3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5eca3-110">Remarks</span></span>

<span data-ttu-id="5eca3-111">Le nuanceur de coque peut générer des points de contrôle 0 s’ils ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="5eca3-111">The hull shader can output 0 control points if they are not needed.</span></span>

<span data-ttu-id="5eca3-112">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="5eca3-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5eca3-113">Sommet</span><span class="sxs-lookup"><span data-stu-id="5eca3-113">Vertex</span></span> | <span data-ttu-id="5eca3-114">Forme</span><span class="sxs-lookup"><span data-stu-id="5eca3-114">Hull</span></span>                 | <span data-ttu-id="5eca3-115">Domain</span><span class="sxs-lookup"><span data-stu-id="5eca3-115">Domain</span></span> | <span data-ttu-id="5eca3-116">Géométrie</span><span class="sxs-lookup"><span data-stu-id="5eca3-116">Geometry</span></span> | <span data-ttu-id="5eca3-117">Pixel</span><span class="sxs-lookup"><span data-stu-id="5eca3-117">Pixel</span></span> | <span data-ttu-id="5eca3-118">Compute</span><span class="sxs-lookup"><span data-stu-id="5eca3-118">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="5eca3-119">Section déclarations</span><span class="sxs-lookup"><span data-stu-id="5eca3-119">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5eca3-120">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5eca3-120">Minimum Shader Model</span></span>

<span data-ttu-id="5eca3-121">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="5eca3-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5eca3-122">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5eca3-122">Shader Model</span></span>                                              | <span data-ttu-id="5eca3-123">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5eca3-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5eca3-124">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="5eca3-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5eca3-125">Oui</span><span class="sxs-lookup"><span data-stu-id="5eca3-125">yes</span></span>       |
| [<span data-ttu-id="5eca3-126">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="5eca3-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5eca3-127">non</span><span class="sxs-lookup"><span data-stu-id="5eca3-127">no</span></span>        |
| [<span data-ttu-id="5eca3-128">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="5eca3-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5eca3-129">non</span><span class="sxs-lookup"><span data-stu-id="5eca3-129">no</span></span>        |
| [<span data-ttu-id="5eca3-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5eca3-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5eca3-131">non</span><span class="sxs-lookup"><span data-stu-id="5eca3-131">no</span></span>        |
| [<span data-ttu-id="5eca3-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5eca3-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5eca3-133">non</span><span class="sxs-lookup"><span data-stu-id="5eca3-133">no</span></span>        |
| [<span data-ttu-id="5eca3-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5eca3-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5eca3-135">non</span><span class="sxs-lookup"><span data-stu-id="5eca3-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5eca3-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5eca3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eca3-137">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5eca3-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





