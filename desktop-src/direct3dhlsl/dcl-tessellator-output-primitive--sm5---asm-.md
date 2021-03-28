---
title: dcl_tessellator_output_primitive (SM5-ASM)
description: Déclarez le type primitif de sortie du paveur dans une section de déclaration de nuanceur de coque.
ms.assetid: 95F074C5-6012-4160-B78E-440C33C1ECC3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 390f22cdafe3b0d078bf8a502623a1c741e34e34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030616"
---
# <a name="dcl_tessellator_output_primitive-sm5---asm"></a><span data-ttu-id="62c89-103">\_ \_ primitive de sortie DCL du paveur \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="62c89-103">dcl\_tessellator\_output\_primitive (sm5 - asm)</span></span>

<span data-ttu-id="62c89-104">Déclarez le type primitif de sortie du paveur dans une section de déclaration de nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="62c89-104">Declare the tessellator output primitive type in a hull shader declaration section.</span></span>



| <span data-ttu-id="62c89-105">\_primitive de sortie DCL du paveur \_ \_ {Output \_ point </span><span class="sxs-lookup"><span data-stu-id="62c89-105">dcl\_tessellator\_output\_primitive {output\_point </span></span>\| <span data-ttu-id="62c89-106">ligne de sortie \_ </span><span class="sxs-lookup"><span data-stu-id="62c89-106">output\_line </span></span>\| <span data-ttu-id="62c89-107">triangloutput \_ e \_ PV </span><span class="sxs-lookup"><span data-stu-id="62c89-107">triangloutput\_e\_cw </span></span>\| <span data-ttu-id="62c89-108">triangle de sortie, \_ \_ CCW}</span><span class="sxs-lookup"><span data-stu-id="62c89-108">output\_triangle\_ccw}</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="62c89-109">Élément</span><span class="sxs-lookup"><span data-stu-id="62c89-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="62c89-110">Description</span><span class="sxs-lookup"><span data-stu-id="62c89-110">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="62c89-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*ligne de sortie du point de sortie \_ \| \_ \| triangloutput \_ e \_ PV de sortie en \| \_ triangle \_*</span><span class="sxs-lookup"><span data-stu-id="62c89-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*output\_point \| output\_line \| triangloutput\_e\_cw \| output\_triangle\_ccw*</span></span><br/> | <span data-ttu-id="62c89-112">\[dans \] le type primitif de sortie.</span><span class="sxs-lookup"><span data-stu-id="62c89-112">\[in\] The output primitive type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62c89-113">Notes</span><span class="sxs-lookup"><span data-stu-id="62c89-113">Remarks</span></span>

<span data-ttu-id="62c89-114">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="62c89-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="62c89-115">Sommet</span><span class="sxs-lookup"><span data-stu-id="62c89-115">Vertex</span></span> | <span data-ttu-id="62c89-116">Forme</span><span class="sxs-lookup"><span data-stu-id="62c89-116">Hull</span></span>                 | <span data-ttu-id="62c89-117">Domain</span><span class="sxs-lookup"><span data-stu-id="62c89-117">Domain</span></span> | <span data-ttu-id="62c89-118">Géométrie</span><span class="sxs-lookup"><span data-stu-id="62c89-118">Geometry</span></span> | <span data-ttu-id="62c89-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="62c89-119">Pixel</span></span> | <span data-ttu-id="62c89-120">Compute</span><span class="sxs-lookup"><span data-stu-id="62c89-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="62c89-121">Section déclarations</span><span class="sxs-lookup"><span data-stu-id="62c89-121">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="62c89-122">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="62c89-122">Minimum Shader Model</span></span>

<span data-ttu-id="62c89-123">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="62c89-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="62c89-124">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="62c89-124">Shader Model</span></span>                                              | <span data-ttu-id="62c89-125">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="62c89-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="62c89-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="62c89-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="62c89-127">Oui</span><span class="sxs-lookup"><span data-stu-id="62c89-127">yes</span></span>       |
| [<span data-ttu-id="62c89-128">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="62c89-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="62c89-129">non</span><span class="sxs-lookup"><span data-stu-id="62c89-129">no</span></span>        |
| [<span data-ttu-id="62c89-130">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="62c89-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="62c89-131">non</span><span class="sxs-lookup"><span data-stu-id="62c89-131">no</span></span>        |
| [<span data-ttu-id="62c89-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62c89-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="62c89-133">non</span><span class="sxs-lookup"><span data-stu-id="62c89-133">no</span></span>        |
| [<span data-ttu-id="62c89-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62c89-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="62c89-135">non</span><span class="sxs-lookup"><span data-stu-id="62c89-135">no</span></span>        |
| [<span data-ttu-id="62c89-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62c89-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="62c89-137">non</span><span class="sxs-lookup"><span data-stu-id="62c89-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="62c89-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62c89-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62c89-139">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62c89-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





