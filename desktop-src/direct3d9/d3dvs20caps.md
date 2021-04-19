---
description: Constantes de sommets de nuanceur de sommets. Ces constantes sont utilisées par le membre VS20Caps de D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caccdebe3dc67b6299c038935e26c0dbac2be6d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544587"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="1995d-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="1995d-104">D3DVS20CAPS</span></span>

<span data-ttu-id="1995d-105">Constantes de sommets de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="1995d-105">Vertex shader caps constants.</span></span> <span data-ttu-id="1995d-106">Ces constantes sont utilisées par le membre VS20Caps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="1995d-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="1995d-107">\#définition</span><span class="sxs-lookup"><span data-stu-id="1995d-107">\#define</span></span>                              | <span data-ttu-id="1995d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="1995d-108">Value</span></span>          | <span data-ttu-id="1995d-109">Description</span><span class="sxs-lookup"><span data-stu-id="1995d-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1995d-110">\_PRÉDICAT D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="1995d-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="1995d-111">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="1995d-111">(1 << 0)</span></span> | <span data-ttu-id="1995d-112">Le prédicat d’instruction est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1995d-112">Instruction predication is supported.</span></span> <span data-ttu-id="1995d-113">Voir [ \_ COMP setp-vs](../direct3dhlsl/setp-comp---vs.md).</span><span class="sxs-lookup"><span data-stu-id="1995d-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="1995d-114">D3DVS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="1995d-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="1995d-115">24</span><span class="sxs-lookup"><span data-stu-id="1995d-115">24</span></span>             | <span data-ttu-id="1995d-116">Le niveau maximal d’imbrication des instructions de contrôle de workflow dynamique ([interruption-vs](../direct3dhlsl/break---vs.md), [rupture \_ COMP-vs](../direct3dhlsl/break-comp---vs.md), [breakp-vs](../direct3dhlsl/breakp---vs.md), si [COMP- \_ vs](../direct3dhlsl/if-comp---vs.md), si COMP-vs, \_ [si prédit-vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="1995d-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="1995d-117">D3DVS20 \_ Min \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="1995d-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="1995d-118">0</span><span class="sxs-lookup"><span data-stu-id="1995d-118">0</span></span>              | <span data-ttu-id="1995d-119">Le niveau minimal d’imbrication des instructions de contrôle de workflow dynamique ([break-vs](../direct3dhlsl/break---vs.md), [pause \_ COMP-vs](../direct3dhlsl/break-comp---vs.md), [breakp-vs](../direct3dhlsl/breakp---vs.md), [si \_ COMP-vs](../direct3dhlsl/if-comp---vs.md), si COMP-vs, \_ [si préditd-vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="1995d-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="1995d-120">D3DVS20 \_ Max \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="1995d-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="1995d-121">32</span><span class="sxs-lookup"><span data-stu-id="1995d-121">32</span></span>             | <span data-ttu-id="1995d-122">Nombre maximal de registres temporaires pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1995d-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1995d-123">D3DVS20 \_ Min \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="1995d-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="1995d-124">12</span><span class="sxs-lookup"><span data-stu-id="1995d-124">12</span></span>             | <span data-ttu-id="1995d-125">Nombre minimal de registres temporaires pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1995d-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1995d-126">D3DVS20 \_ Max \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="1995d-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="1995d-127">4</span><span class="sxs-lookup"><span data-stu-id="1995d-127">4</span></span>              | <span data-ttu-id="1995d-128">Profondeur maximale d’imbrication des instructions [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) et [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="1995d-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="1995d-129">D3DVS20 \_ Min \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="1995d-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="1995d-130">1</span><span class="sxs-lookup"><span data-stu-id="1995d-130">1</span></span>              | <span data-ttu-id="1995d-131">Profondeur minimale de l’imbrication des instructions [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) et [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="1995d-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="1995d-132">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="1995d-132">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="1995d-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="1995d-133">Header</span></span>                   | <span data-ttu-id="1995d-134">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="1995d-134">d3d9caps.h</span></span> |
| <span data-ttu-id="1995d-135">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="1995d-135">Minimum operating system</span></span> | <span data-ttu-id="1995d-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="1995d-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1995d-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1995d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1995d-138">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="1995d-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="1995d-139">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="1995d-139">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
