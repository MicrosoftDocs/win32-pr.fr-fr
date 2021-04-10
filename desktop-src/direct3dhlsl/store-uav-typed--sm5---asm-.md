---
title: store_uav_typed (SM5-ASM)
description: Écriture à accès aléatoire d’un élément dans une vue d’accès non triée typée (UAV).
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030570"
---
# <a name="store_uav_typed-sm5---asm"></a><span data-ttu-id="54c78-103">Store \_ UAV \_ typé (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="54c78-103">store\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="54c78-104">Écriture à accès aléatoire d’un élément dans une vue d’accès non triée typée (UAV).</span><span class="sxs-lookup"><span data-stu-id="54c78-104">Random-access write of an element into a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="54c78-105">Store \_ UAV \_ typé dstUAV. XYZW, dstAddress \[ . Swizzle \] , src0 \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="54c78-105">store\_uav\_typed dstUAV.xyzw, dstAddress\[.swizzle\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="54c78-106">Élément</span><span class="sxs-lookup"><span data-stu-id="54c78-106">Item</span></span>                                                                                                           | <span data-ttu-id="54c78-107">Description</span><span class="sxs-lookup"><span data-stu-id="54c78-107">Description</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="54c78-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="54c78-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                 | <span data-ttu-id="54c78-109">\[dans \] contient le résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="54c78-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="54c78-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="54c78-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="54c78-111">\[dans \] l’adresse à laquelle écrire.</span><span class="sxs-lookup"><span data-stu-id="54c78-111">\[in\] The address at which to write.</span></span><br/>        |
| <span data-ttu-id="54c78-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="54c78-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="54c78-113">\[dans \] les composants à écrire.</span><span class="sxs-lookup"><span data-stu-id="54c78-113">\[in\] The components to write.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="54c78-114">Notes</span><span class="sxs-lookup"><span data-stu-id="54c78-114">Remarks</span></span>

<span data-ttu-id="54c78-115">Cette instruction effectue un élément de 4 composants \* 32 bits écrit à partir de *Src0* vers *dstUAV* à l’adresse dans *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="54c78-115">This instruction performs a 4 component \*32-bit element written from *src0* to *dstUAV* at the address in *dstAddress*.</span></span> <span data-ttu-id="54c78-116">*dstUAV* est un UAV typé (u \# ).</span><span class="sxs-lookup"><span data-stu-id="54c78-116">*dstUAV* is a typed UAV (u\#).</span></span>

<span data-ttu-id="54c78-117">Le format de UAV détermine la conversion de format.</span><span class="sxs-lookup"><span data-stu-id="54c78-117">The format of the UAV determines format conversion.</span></span>

<span data-ttu-id="54c78-118">Le nombre de composants entiers non signés 32 bits pris à partir de l’adresse est déterminé par la dimensionnalité de la ressource déclarée dans *dstUAV*.</span><span class="sxs-lookup"><span data-stu-id="54c78-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *dstUAV*.</span></span> <span data-ttu-id="54c78-119">Cette adresse se trouve dans les éléments.</span><span class="sxs-lookup"><span data-stu-id="54c78-119">This address is in elements.</span></span>

<span data-ttu-id="54c78-120">L’adressage hors limites signifie que rien n’est écrit dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="54c78-120">Out of bounds addressing means nothing gets written to memory.</span></span>

<span data-ttu-id="54c78-121">*dstUAV* a toujours un masque d’écriture. XYZW.</span><span class="sxs-lookup"><span data-stu-id="54c78-121">*dstUAV* always has a .xyzw write mask.</span></span> <span data-ttu-id="54c78-122">Tous les composants doivent être écrits.</span><span class="sxs-lookup"><span data-stu-id="54c78-122">All components must be written.</span></span>

<span data-ttu-id="54c78-123">Il n’est pas valide et n’est pas défini pour utiliser cette instruction sur un UAV qui n’est pas déclaré comme typé.</span><span class="sxs-lookup"><span data-stu-id="54c78-123">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="54c78-124">Autrement dit, cette action sur un UAV structuré ou non n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="54c78-124">That is, doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="54c78-125">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="54c78-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="54c78-126">Sommet</span><span class="sxs-lookup"><span data-stu-id="54c78-126">Vertex</span></span> | <span data-ttu-id="54c78-127">Forme</span><span class="sxs-lookup"><span data-stu-id="54c78-127">Hull</span></span> | <span data-ttu-id="54c78-128">Domain</span><span class="sxs-lookup"><span data-stu-id="54c78-128">Domain</span></span> | <span data-ttu-id="54c78-129">Géométrie</span><span class="sxs-lookup"><span data-stu-id="54c78-129">Geometry</span></span> | <span data-ttu-id="54c78-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="54c78-130">Pixel</span></span> | <span data-ttu-id="54c78-131">Compute</span><span class="sxs-lookup"><span data-stu-id="54c78-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="54c78-132">X</span><span class="sxs-lookup"><span data-stu-id="54c78-132">X</span></span>     | <span data-ttu-id="54c78-133">X</span><span class="sxs-lookup"><span data-stu-id="54c78-133">X</span></span>       |



 

<span data-ttu-id="54c78-134">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="54c78-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="54c78-135">Sommet</span><span class="sxs-lookup"><span data-stu-id="54c78-135">Vertex</span></span> | <span data-ttu-id="54c78-136">Forme</span><span class="sxs-lookup"><span data-stu-id="54c78-136">Hull</span></span> | <span data-ttu-id="54c78-137">Domain</span><span class="sxs-lookup"><span data-stu-id="54c78-137">Domain</span></span> | <span data-ttu-id="54c78-138">Géométrie</span><span class="sxs-lookup"><span data-stu-id="54c78-138">Geometry</span></span> | <span data-ttu-id="54c78-139">Pixel</span><span class="sxs-lookup"><span data-stu-id="54c78-139">Pixel</span></span> | <span data-ttu-id="54c78-140">Compute</span><span class="sxs-lookup"><span data-stu-id="54c78-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="54c78-141">X</span><span class="sxs-lookup"><span data-stu-id="54c78-141">X</span></span>      | <span data-ttu-id="54c78-142">X</span><span class="sxs-lookup"><span data-stu-id="54c78-142">X</span></span>    | <span data-ttu-id="54c78-143">X</span><span class="sxs-lookup"><span data-stu-id="54c78-143">X</span></span>      | <span data-ttu-id="54c78-144">X</span><span class="sxs-lookup"><span data-stu-id="54c78-144">X</span></span>        | <span data-ttu-id="54c78-145">X</span><span class="sxs-lookup"><span data-stu-id="54c78-145">X</span></span>     | <span data-ttu-id="54c78-146">X</span><span class="sxs-lookup"><span data-stu-id="54c78-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="54c78-147">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="54c78-147">Minimum Shader Model</span></span>

<span data-ttu-id="54c78-148">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="54c78-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="54c78-149">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="54c78-149">Shader Model</span></span>                                              | <span data-ttu-id="54c78-150">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="54c78-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="54c78-151">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="54c78-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="54c78-152">Oui</span><span class="sxs-lookup"><span data-stu-id="54c78-152">yes</span></span>       |
| [<span data-ttu-id="54c78-153">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="54c78-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="54c78-154">non</span><span class="sxs-lookup"><span data-stu-id="54c78-154">no</span></span>        |
| [<span data-ttu-id="54c78-155">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="54c78-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="54c78-156">non</span><span class="sxs-lookup"><span data-stu-id="54c78-156">no</span></span>        |
| [<span data-ttu-id="54c78-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54c78-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="54c78-158">non</span><span class="sxs-lookup"><span data-stu-id="54c78-158">no</span></span>        |
| [<span data-ttu-id="54c78-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54c78-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="54c78-160">non</span><span class="sxs-lookup"><span data-stu-id="54c78-160">no</span></span>        |
| [<span data-ttu-id="54c78-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54c78-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="54c78-162">non</span><span class="sxs-lookup"><span data-stu-id="54c78-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="54c78-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54c78-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54c78-164">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54c78-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





