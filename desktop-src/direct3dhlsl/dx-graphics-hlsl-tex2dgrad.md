---
title: tex2Dgrad
description: Échantillonne une texture 2D à l’aide d’un dégradé pour sélectionner le niveau MIP. | tex2Dgrad
ms.assetid: a9ab7972-3480-4b37-aa10-c5cf811bdd0e
keywords:
- HLSL tex2Dgrad
topic_type:
- apiref
api_name:
- tex2Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74b20f1cf1f6f5d3b2873f4546dd57ef73b23dbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973931"
---
# <a name="tex2dgrad"></a><span data-ttu-id="d897b-105">tex2Dgrad</span><span class="sxs-lookup"><span data-stu-id="d897b-105">tex2Dgrad</span></span>

<span data-ttu-id="d897b-106">Échantillonne une texture 2D à l’aide d’un dégradé pour sélectionner le niveau MIP.</span><span class="sxs-lookup"><span data-stu-id="d897b-106">Samples a 2D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="d897b-107">RET tex2Dgrad (s, t, DDX, ddy)</span><span class="sxs-lookup"><span data-stu-id="d897b-107">ret tex2Dgrad(s, t, ddx, ddy)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d897b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d897b-108">Parameters</span></span>



| <span data-ttu-id="d897b-109">Élément</span><span class="sxs-lookup"><span data-stu-id="d897b-109">Item</span></span>                                                         | <span data-ttu-id="d897b-110">Description</span><span class="sxs-lookup"><span data-stu-id="d897b-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d897b-111"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d897b-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="d897b-112">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="d897b-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="d897b-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="d897b-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="d897b-114">\[dans \] les coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="d897b-114">\[in\] The texture coordinates.</span></span><br/>                                   |
| <span data-ttu-id="d897b-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="d897b-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="d897b-116">\[en \] taux de changement de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="d897b-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="d897b-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="d897b-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="d897b-118">\[en \] taux de changement de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="d897b-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d897b-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d897b-119">Return Value</span></span>

<span data-ttu-id="d897b-120">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="d897b-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="d897b-121">Description du type</span><span class="sxs-lookup"><span data-stu-id="d897b-121">Type Description</span></span>



| <span data-ttu-id="d897b-122">Nom</span><span class="sxs-lookup"><span data-stu-id="d897b-122">Name</span></span> | <span data-ttu-id="d897b-123">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="d897b-123">In/Out</span></span> | [<span data-ttu-id="d897b-124">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="d897b-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d897b-125">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="d897b-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d897b-126">Taille</span><span class="sxs-lookup"><span data-stu-id="d897b-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="d897b-127">s</span><span class="sxs-lookup"><span data-stu-id="d897b-127">s</span></span>    | <span data-ttu-id="d897b-128">in</span><span class="sxs-lookup"><span data-stu-id="d897b-128">in</span></span>     | [<span data-ttu-id="d897b-129">**object**</span><span class="sxs-lookup"><span data-stu-id="d897b-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d897b-130">sampler2D</span><span class="sxs-lookup"><span data-stu-id="d897b-130">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="d897b-131">1</span><span class="sxs-lookup"><span data-stu-id="d897b-131">1</span></span>    |
| <span data-ttu-id="d897b-132">t</span><span class="sxs-lookup"><span data-stu-id="d897b-132">t</span></span>    | <span data-ttu-id="d897b-133">in</span><span class="sxs-lookup"><span data-stu-id="d897b-133">in</span></span>     | [<span data-ttu-id="d897b-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="d897b-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d897b-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d897b-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d897b-136">2</span><span class="sxs-lookup"><span data-stu-id="d897b-136">2</span></span>    |
| <span data-ttu-id="d897b-137">DDX</span><span class="sxs-lookup"><span data-stu-id="d897b-137">ddx</span></span>  | <span data-ttu-id="d897b-138">in</span><span class="sxs-lookup"><span data-stu-id="d897b-138">in</span></span>     | [<span data-ttu-id="d897b-139">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="d897b-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d897b-140">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d897b-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d897b-141">2</span><span class="sxs-lookup"><span data-stu-id="d897b-141">2</span></span>    |
| <span data-ttu-id="d897b-142">ddy</span><span class="sxs-lookup"><span data-stu-id="d897b-142">ddy</span></span>  | <span data-ttu-id="d897b-143">in</span><span class="sxs-lookup"><span data-stu-id="d897b-143">in</span></span>     | [<span data-ttu-id="d897b-144">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="d897b-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d897b-145">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d897b-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d897b-146">2</span><span class="sxs-lookup"><span data-stu-id="d897b-146">2</span></span>    |
| <span data-ttu-id="d897b-147">Av</span><span class="sxs-lookup"><span data-stu-id="d897b-147">ret</span></span>  | <span data-ttu-id="d897b-148">out</span><span class="sxs-lookup"><span data-stu-id="d897b-148">out</span></span>    | [<span data-ttu-id="d897b-149">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="d897b-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d897b-150">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d897b-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d897b-151">4</span><span class="sxs-lookup"><span data-stu-id="d897b-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d897b-152">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d897b-152">Minimum Shader Model</span></span>

<span data-ttu-id="d897b-153">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d897b-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d897b-154">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d897b-154">Shader Model</span></span>                                              | <span data-ttu-id="d897b-155">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d897b-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="d897b-156">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d897b-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d897b-157">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="d897b-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="d897b-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d897b-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d897b-159">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="d897b-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="d897b-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d897b-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d897b-161">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="d897b-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="d897b-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d897b-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d897b-163">non</span><span class="sxs-lookup"><span data-stu-id="d897b-163">no</span></span>                       |



 

1.  <span data-ttu-id="d897b-164">La réorganisation de code importante est effectuée pour déplacer des calculs de dégradé en dehors du contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="d897b-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="d897b-165">Si le \_ Cap D3DPSHADERCAPS2 0 est défini avec D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, le compilateur mappe cette fonction à texldd.</span><span class="sxs-lookup"><span data-stu-id="d897b-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="d897b-166">Notes</span><span class="sxs-lookup"><span data-stu-id="d897b-166">Remarks</span></span>

<span data-ttu-id="d897b-167">Lorsque le contrôle de Flow est présent dans un nuanceur, le résultat d’un calcul de dégradé demandé dans un chemin de branche donné est ambigu lorsque les pixels adjacents peuvent descendre dans des chemins de contrôle de Flow distincts.</span><span class="sxs-lookup"><span data-stu-id="d897b-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="d897b-168">Par conséquent, il est jugé illégal d’utiliser toute opération de nuanceur de pixels qui demande un calcul de dégradé à un emplacement qui se trouve à l’intérieur d’une construction de contrôle de Flow qui peut varier d’un pixel à l’autre, pour une primitive donnée en cours de pixellisation.</span><span class="sxs-lookup"><span data-stu-id="d897b-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="d897b-169">Si l’un des côtés d’une instruction **If** avec l’attribut Branch utilise une fonction de dégradé, une erreur de compilateur peut être générée.</span><span class="sxs-lookup"><span data-stu-id="d897b-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="d897b-170">Consultez l' [instruction if (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="d897b-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d897b-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d897b-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d897b-172">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d897b-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

