---
description: Indicateurs de capacité de nuanceur de pixels.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2326b8f5066d34087fb543c7771a0cd547b98f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995266"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="9dfcb-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9dfcb-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="9dfcb-104">Indicateurs de capacité de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-104">Pixel shader capability flags.</span></span>



| <span data-ttu-id="9dfcb-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="9dfcb-105">\#define</span></span>                                     | <span data-ttu-id="9dfcb-106">Value</span><span class="sxs-lookup"><span data-stu-id="9dfcb-106">Value</span></span>          | <span data-ttu-id="9dfcb-107">Description</span><span class="sxs-lookup"><span data-stu-id="9dfcb-107">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfcb-108">D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="9dfcb-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="9dfcb-109">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="9dfcb-109">(1 << 0)</span></span> | <span data-ttu-id="9dfcb-110">Swizzling arbitraire est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="9dfcb-111">D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="9dfcb-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="9dfcb-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="9dfcb-112">(1 << 1)</span></span> | <span data-ttu-id="9dfcb-113">Les instructions de dégradé sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="9dfcb-114">\_PRÉDICAT D3DD3DPSHADERCAPS2 0 \_</span><span class="sxs-lookup"><span data-stu-id="9dfcb-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="9dfcb-115">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="9dfcb-115">(1 << 2)</span></span> | <span data-ttu-id="9dfcb-116">Le prédicat d’instruction est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-116">Instruction predication is supported.</span></span> <span data-ttu-id="9dfcb-117">Consultez [setp \_ COMP-PS](../direct3dhlsl/setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="9dfcb-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="9dfcb-118">D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="9dfcb-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="9dfcb-119">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="9dfcb-119">(1 << 3)</span></span> | <span data-ttu-id="9dfcb-120">Il n’existe aucune limite quant au nombre de lectures dépendantes par instruction.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="9dfcb-121">D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="9dfcb-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="9dfcb-122">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="9dfcb-122">(1 << 4)</span></span> | <span data-ttu-id="9dfcb-123">Il n’existe aucune limite quant au nombre d’instructions de Tex.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="9dfcb-124">D3DPS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="9dfcb-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="9dfcb-125">24</span><span class="sxs-lookup"><span data-stu-id="9dfcb-125">24</span></span>             | <span data-ttu-id="9dfcb-126">Niveau maximal d’imbrication des instructions de contrôle de workflow dynamique (break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="9dfcb-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="9dfcb-127">D3DPS20 \_ Min \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="9dfcb-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="9dfcb-128">0</span><span class="sxs-lookup"><span data-stu-id="9dfcb-128">0</span></span>              | <span data-ttu-id="9dfcb-129">Niveau minimal d’imbrication des instructions de contrôle de workflow dynamique (break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="9dfcb-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="9dfcb-130">D3DPS20 \_ Max \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="9dfcb-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="9dfcb-131">32</span><span class="sxs-lookup"><span data-stu-id="9dfcb-131">32</span></span>             | <span data-ttu-id="9dfcb-132">Le pilote prendra en charge au maximum ce nombre temporaire de registres.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="9dfcb-133">D3DPS20 \_ Min \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="9dfcb-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="9dfcb-134">12</span><span class="sxs-lookup"><span data-stu-id="9dfcb-134">12</span></span>             | <span data-ttu-id="9dfcb-135">Le pilote prendra en charge au moins ce nombre temporaire de registres.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="9dfcb-136">D3DPS20 \_ Max \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="9dfcb-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="9dfcb-137">4</span><span class="sxs-lookup"><span data-stu-id="9dfcb-137">4</span></span>              | <span data-ttu-id="9dfcb-138">Profondeur maximale d’imbrication des instructions [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) et [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="9dfcb-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="9dfcb-139">D3DPS20 \_ Min \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="9dfcb-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="9dfcb-140">1</span><span class="sxs-lookup"><span data-stu-id="9dfcb-140">1</span></span>              | <span data-ttu-id="9dfcb-141">Profondeur minimale de l’imbrication des instructions [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) et [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="9dfcb-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="9dfcb-142">D3DPS20 \_ Max \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="9dfcb-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="9dfcb-143">512</span><span class="sxs-lookup"><span data-stu-id="9dfcb-143">512</span></span>            | <span data-ttu-id="9dfcb-144">Le pilote prendra en charge le plus grand nombre d’instructions.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="9dfcb-145">D3DPS20 \_ Min \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="9dfcb-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="9dfcb-146">96</span><span class="sxs-lookup"><span data-stu-id="9dfcb-146">96</span></span>             | <span data-ttu-id="9dfcb-147">Le pilote prendra en charge au moins ce nombre d’instructions.</span><span class="sxs-lookup"><span data-stu-id="9dfcb-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="9dfcb-148">Ces constantes sont utilisées par le \_ membre D3DPSHADERCAPS2 0 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="9dfcb-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="9dfcb-149">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="9dfcb-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="9dfcb-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="9dfcb-150">Header</span></span>                   | <span data-ttu-id="9dfcb-151">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="9dfcb-151">d3d9caps.h</span></span> |
| <span data-ttu-id="9dfcb-152">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="9dfcb-152">Minimum operating system</span></span> | <span data-ttu-id="9dfcb-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9dfcb-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9dfcb-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9dfcb-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dfcb-155">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="9dfcb-155">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="9dfcb-156">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="9dfcb-156">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
