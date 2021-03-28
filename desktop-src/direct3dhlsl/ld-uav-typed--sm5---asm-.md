---
title: ld_uav_typed (SM5-ASM)
description: Lecture à accès aléatoire d’un élément à partir d’une vue d’accès non triée typée (UAV).
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b22392c802378c094b443c8ff2f2282909bd1f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313681"
---
# <a name="ld_uav_typed-sm5---asm"></a><span data-ttu-id="7a058-103">LD \_ UAV \_ typé (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7a058-103">ld\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="7a058-104">Lecture à accès aléatoire d’un élément à partir d’une vue d’accès non triée typée (UAV).</span><span class="sxs-lookup"><span data-stu-id="7a058-104">Random-access read of an element from a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="7a058-105">LD \_ UAV \_ typé dst0 \[ . Mask \] , srcAddress \[ . Swizzle \] , srcUAV \[ . Swizzle\]</span><span class="sxs-lookup"><span data-stu-id="7a058-105">ld\_uav\_typed dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="7a058-106">Élément</span><span class="sxs-lookup"><span data-stu-id="7a058-106">Item</span></span>                                                                                                           | <span data-ttu-id="7a058-107">Description</span><span class="sxs-lookup"><span data-stu-id="7a058-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="7a058-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="7a058-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="7a058-109">\[dans \] l’adresse des résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7a058-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="7a058-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="7a058-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/> | <span data-ttu-id="7a058-111">\[dans \] spécifie l’adresse à partir de laquelle effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="7a058-111">\[in\] Specifies the address to read from.</span></span><br/>          |
| <span data-ttu-id="7a058-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span><span class="sxs-lookup"><span data-stu-id="7a058-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span></span><br/>                 | <span data-ttu-id="7a058-113">\[dans \] la source à lire.</span><span class="sxs-lookup"><span data-stu-id="7a058-113">\[in\] The source to read from.</span></span> <br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="7a058-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7a058-114">Remarks</span></span>

<span data-ttu-id="7a058-115">Cette instruction effectue une lecture d’élément à 4 composants à partir de *srcUAV* à l’adresse entière non signée dans *srcAddress*, convertie en 32 bits par composant en fonction du format, puis écrite dans *dst0* dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="7a058-115">This instruction performs a 4-component element read from *srcUAV* at the unsigned integer address in *srcAddress*, converted to 32bit per component based on the format, then written to *dst0* in the shader.</span></span>

<span data-ttu-id="7a058-116">*srcUAV* est un UAV (u \# ) déclaré comme typé.</span><span class="sxs-lookup"><span data-stu-id="7a058-116">*srcUAV* is a UAV (u\#) declared as typed.</span></span> <span data-ttu-id="7a058-117">Toutefois, le type de la ressource liée doit être R32 \_ uint/Saint/.</span><span class="sxs-lookup"><span data-stu-id="7a058-117">However, the type of the bound resource must be R32\_UINT/SINT/FLOAT.</span></span>

<span data-ttu-id="7a058-118">Le nombre de composants entiers non signés 32 bits pris à partir de l’adresse est déterminé par la dimensionnalité de la ressource déclarée dans *srcUAV*.</span><span class="sxs-lookup"><span data-stu-id="7a058-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *srcUAV*.</span></span> <span data-ttu-id="7a058-119">L’adressage est le même que l’instruction [LD](ld--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="7a058-119">Addressing is the same as the [ld](ld--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="7a058-120">L’adressage hors limites est le même que l’instruction **LD** .</span><span class="sxs-lookup"><span data-stu-id="7a058-120">Out of bounds addressing is the same as the **ld** instruction.</span></span>

<span data-ttu-id="7a058-121">Le comportement de cette instruction est identique à l’instruction **LD** si elle est appelée en tant que **LD dst0 \[ . Mask \] , srcAddress \[ . Swizzle \] , srcUAV \[ . Swizzle \]**</span><span class="sxs-lookup"><span data-stu-id="7a058-121">The behavior of this instruction is identical to the **ld** instruction if called as **ld dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]**</span></span>

<span data-ttu-id="7a058-122">Il n’est pas valide et n’est pas défini pour utiliser cette instruction sur un UAV qui n’est pas déclaré comme typé.</span><span class="sxs-lookup"><span data-stu-id="7a058-122">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="7a058-123">Le fait de procéder sur un UAV structuré ou non n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7a058-123">Doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="7a058-124">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="7a058-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7a058-125">Sommet</span><span class="sxs-lookup"><span data-stu-id="7a058-125">Vertex</span></span> | <span data-ttu-id="7a058-126">Forme</span><span class="sxs-lookup"><span data-stu-id="7a058-126">Hull</span></span> | <span data-ttu-id="7a058-127">Domain</span><span class="sxs-lookup"><span data-stu-id="7a058-127">Domain</span></span> | <span data-ttu-id="7a058-128">Géométrie</span><span class="sxs-lookup"><span data-stu-id="7a058-128">Geometry</span></span> | <span data-ttu-id="7a058-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="7a058-129">Pixel</span></span> | <span data-ttu-id="7a058-130">Compute</span><span class="sxs-lookup"><span data-stu-id="7a058-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7a058-131">X</span><span class="sxs-lookup"><span data-stu-id="7a058-131">X</span></span>     | <span data-ttu-id="7a058-132">X</span><span class="sxs-lookup"><span data-stu-id="7a058-132">X</span></span>       |



 

<span data-ttu-id="7a058-133">Étant donné que les UAVs sont disponibles à toutes les étapes de nuanceur pour Direct3D 11,1, cette instruction s’applique à toutes les étapes de nuanceur pour le runtime Direct3D 11,1, disponible à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a058-133">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="7a058-134">Sommet</span><span class="sxs-lookup"><span data-stu-id="7a058-134">Vertex</span></span> | <span data-ttu-id="7a058-135">Forme</span><span class="sxs-lookup"><span data-stu-id="7a058-135">Hull</span></span> | <span data-ttu-id="7a058-136">Domain</span><span class="sxs-lookup"><span data-stu-id="7a058-136">Domain</span></span> | <span data-ttu-id="7a058-137">Géométrie</span><span class="sxs-lookup"><span data-stu-id="7a058-137">Geometry</span></span> | <span data-ttu-id="7a058-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="7a058-138">Pixel</span></span> | <span data-ttu-id="7a058-139">Compute</span><span class="sxs-lookup"><span data-stu-id="7a058-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7a058-140">X</span><span class="sxs-lookup"><span data-stu-id="7a058-140">X</span></span>      | <span data-ttu-id="7a058-141">X</span><span class="sxs-lookup"><span data-stu-id="7a058-141">X</span></span>    | <span data-ttu-id="7a058-142">X</span><span class="sxs-lookup"><span data-stu-id="7a058-142">X</span></span>      | <span data-ttu-id="7a058-143">X</span><span class="sxs-lookup"><span data-stu-id="7a058-143">X</span></span>        | <span data-ttu-id="7a058-144">X</span><span class="sxs-lookup"><span data-stu-id="7a058-144">X</span></span>     | <span data-ttu-id="7a058-145">X</span><span class="sxs-lookup"><span data-stu-id="7a058-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7a058-146">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="7a058-146">Minimum Shader Model</span></span>

<span data-ttu-id="7a058-147">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="7a058-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7a058-148">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="7a058-148">Shader Model</span></span>                                              | <span data-ttu-id="7a058-149">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="7a058-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7a058-150">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="7a058-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7a058-151">Oui</span><span class="sxs-lookup"><span data-stu-id="7a058-151">yes</span></span>       |
| [<span data-ttu-id="7a058-152">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="7a058-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7a058-153">non</span><span class="sxs-lookup"><span data-stu-id="7a058-153">no</span></span>        |
| [<span data-ttu-id="7a058-154">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="7a058-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7a058-155">non</span><span class="sxs-lookup"><span data-stu-id="7a058-155">no</span></span>        |
| [<span data-ttu-id="7a058-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a058-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7a058-157">non</span><span class="sxs-lookup"><span data-stu-id="7a058-157">no</span></span>        |
| [<span data-ttu-id="7a058-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a058-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7a058-159">non</span><span class="sxs-lookup"><span data-stu-id="7a058-159">no</span></span>        |
| [<span data-ttu-id="7a058-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a058-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7a058-161">non</span><span class="sxs-lookup"><span data-stu-id="7a058-161">no</span></span>        |



 

<span data-ttu-id="7a058-162">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction pour UAV, SRV et TGSM.</span><span class="sxs-lookup"><span data-stu-id="7a058-162">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a058-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a058-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a058-164">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7a058-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





