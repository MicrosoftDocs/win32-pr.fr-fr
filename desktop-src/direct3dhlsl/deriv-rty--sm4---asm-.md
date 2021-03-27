---
title: deriv_rty (SM4-ASM)
description: Rendu-cible y équivalent de Deriv \_ RTX.
ms.assetid: F78F2DBD-9428-4F34-85AD-276DF54C52D1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e4517782c687473b4789229334b4cafc94b989
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841637"
---
# <a name="deriv_rty-sm4---asm"></a><span data-ttu-id="34579-103">Deriv \_ propriété (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="34579-103">deriv\_rty (sm4 - asm)</span></span>

<span data-ttu-id="34579-104">Rendu-cible y équivalent de [Deriv \_ RTX](deriv-rtx--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="34579-104">Render-target y equivalent of [deriv\_rtx](deriv-rtx--sm4---asm-.md).</span></span>



| <span data-ttu-id="34579-105">Deriv \_ propriété \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="34579-105">deriv\_rty\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="34579-106">Élément</span><span class="sxs-lookup"><span data-stu-id="34579-106">Item</span></span>                                                            | <span data-ttu-id="34579-107">Description</span><span class="sxs-lookup"><span data-stu-id="34579-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="34579-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="34579-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="34579-109">\[dans \] l’adresse du résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="34579-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="34579-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="34579-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="34579-111">\[dans \] le composant de l’opération.</span><span class="sxs-lookup"><span data-stu-id="34579-111">\[in\] The component in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="34579-112">Notes</span><span class="sxs-lookup"><span data-stu-id="34579-112">Remarks</span></span>

<span data-ttu-id="34579-113">Une seule paire dérivée x, y est calculée pour chaque tampon 2x2 de pixels.</span><span class="sxs-lookup"><span data-stu-id="34579-113">Only a single x,y derivative pair is computed for each 2x2 stamp of pixels.</span></span>

<span data-ttu-id="34579-114">Cette opération dépend du matériel.</span><span class="sxs-lookup"><span data-stu-id="34579-114">This operation is hardware dependent.</span></span>

<span data-ttu-id="34579-115">Implémentation du rastériseur de référence pour les triangles :</span><span class="sxs-lookup"><span data-stu-id="34579-115">Reference rasterizer implementation for triangles:</span></span>

-   <span data-ttu-id="34579-116">Le nuanceur de pixels exécute toujours le nuanceur sur des quadruples Quad de pixels dans échelons (même via le contrôle de Flow et le masquage des pixels désactivés).</span><span class="sxs-lookup"><span data-stu-id="34579-116">Pixel Shader always runs Shader over 2x2 quad of pixels in lockstep (even through flow control, masking disabled pixels).</span></span>
-   <span data-ttu-id="34579-117">Les quatre cœurs ont toujours des coordonnées de pixels même numérotées (à la fois x et y) pour le pixel supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="34579-117">Quads always have even numbered pixel coordinates (both x and y) for top-left pixel.</span></span>
-   <span data-ttu-id="34579-118">Les pixels factices s’exécutent en mode primitif si la primitive est trop petite pour remplir un quadruple Quad.</span><span class="sxs-lookup"><span data-stu-id="34579-118">Dummy pixels run off primitive if primitive is too small to fill a 2x2 quad.</span></span>
-   <span data-ttu-id="34579-119">[Deriv \_ RTX](deriv-rtx--sm4---asm-.md) est calculé en sélectionnant d’abord 2 pixels : le pixel actuel et l’autre Pixel avec la même coordonnée y du quadruple.</span><span class="sxs-lookup"><span data-stu-id="34579-119">[deriv\_rtx](deriv-rtx--sm4---asm-.md) is computed by first choosing 2 pixels: the current pixel and the other pixel with the same y coordinate from the quad.</span></span> <span data-ttu-id="34579-120">Ensuite, le résultat est calculé comme suit : *src0*(impair x pixel)- *src0*(même x pixel) \[ par composant\]</span><span class="sxs-lookup"><span data-stu-id="34579-120">Then, the result is calculated as: *src0*(odd x pixel) - *src0*(even x pixel) \[per-component\]</span></span>
-   <span data-ttu-id="34579-121">**Deriv \_ propriété** est calculé en sélectionnant d’abord 2 pixels : le pixel actuel et l’autre Pixel avec la même coordonnée x du quadruple.</span><span class="sxs-lookup"><span data-stu-id="34579-121">**deriv\_rty** is computed by first choosing 2 pixels: the current pixel and the other pixel with the same x coordinate from the quad.</span></span> <span data-ttu-id="34579-122">Ensuite, le résultat est calculé comme suit : *src0*(pixel y impair)- *src0*(y compris y pixel) \[ par composant\]</span><span class="sxs-lookup"><span data-stu-id="34579-122">Then, the result is calculated as: *src0*(odd y pixel) - *src0*(even y pixel) \[per-component\]</span></span>

<span data-ttu-id="34579-123">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="34579-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="34579-124">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="34579-124">Vertex Shader</span></span> | <span data-ttu-id="34579-125">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="34579-125">Geometry Shader</span></span> | <span data-ttu-id="34579-126">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="34579-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="34579-127">x</span><span class="sxs-lookup"><span data-stu-id="34579-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="34579-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="34579-128">Minimum Shader Model</span></span>

<span data-ttu-id="34579-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="34579-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="34579-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="34579-130">Shader Model</span></span>                                              | <span data-ttu-id="34579-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="34579-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="34579-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="34579-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="34579-133">Oui</span><span class="sxs-lookup"><span data-stu-id="34579-133">yes</span></span>       |
| [<span data-ttu-id="34579-134">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="34579-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="34579-135">Oui</span><span class="sxs-lookup"><span data-stu-id="34579-135">yes</span></span>       |
| [<span data-ttu-id="34579-136">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="34579-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="34579-137">Oui</span><span class="sxs-lookup"><span data-stu-id="34579-137">yes</span></span>       |
| [<span data-ttu-id="34579-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34579-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="34579-139">non</span><span class="sxs-lookup"><span data-stu-id="34579-139">no</span></span>        |
| [<span data-ttu-id="34579-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34579-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="34579-141">non</span><span class="sxs-lookup"><span data-stu-id="34579-141">no</span></span>        |
| [<span data-ttu-id="34579-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34579-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="34579-143">non</span><span class="sxs-lookup"><span data-stu-id="34579-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="34579-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34579-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34579-145">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34579-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





