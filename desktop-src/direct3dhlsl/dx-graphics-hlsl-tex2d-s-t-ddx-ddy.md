---
title: tex2D (référence HLSL)-sélectionner le niveau MIP
description: Échantillonne une texture 2D à l’aide d’un dégradé pour sélectionner le niveau MIP. | tex2D (référence HLSL)
ms.assetid: 0e8c32ed-d174-4045-9cbf-6c04586ea5bb
keywords:
- HLSL tex2D
topic_type:
- apiref
api_name:
- tex2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5a642a92756f3f0774e5719aa1fcf9ec302eecb5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982695"
---
# <a name="tex2d-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="13bf1-105">tex2D (référence HLSL)-sélectionner le niveau MIP</span><span class="sxs-lookup"><span data-stu-id="13bf1-105">tex2D (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="13bf1-106">Échantillonne une texture 2D à l’aide d’un dégradé pour sélectionner le niveau MIP.</span><span class="sxs-lookup"><span data-stu-id="13bf1-106">Samples a 2D texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="13bf1-107">RET tex2D (s, t, DDX, ddy)</span><span class="sxs-lookup"><span data-stu-id="13bf1-107">ret tex2D(s, t, ddx, ddy)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="13bf1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13bf1-108">Parameters</span></span>



| <span data-ttu-id="13bf1-109">Élément</span><span class="sxs-lookup"><span data-stu-id="13bf1-109">Item</span></span>                                                         | <span data-ttu-id="13bf1-110">Description</span><span class="sxs-lookup"><span data-stu-id="13bf1-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="13bf1-111"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="13bf1-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="13bf1-112">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="13bf1-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="13bf1-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="13bf1-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="13bf1-114">\[dans \] les coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="13bf1-114">\[in\] The texture coordinates.</span></span><br/>                                   |
| <span data-ttu-id="13bf1-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="13bf1-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="13bf1-116">\[en \] taux de changement de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="13bf1-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="13bf1-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="13bf1-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="13bf1-118">\[en \] taux de changement de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="13bf1-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="13bf1-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="13bf1-119">Return Value</span></span>

<span data-ttu-id="13bf1-120">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="13bf1-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="13bf1-121">Description du type</span><span class="sxs-lookup"><span data-stu-id="13bf1-121">Type Description</span></span>



| <span data-ttu-id="13bf1-122">Nom</span><span class="sxs-lookup"><span data-stu-id="13bf1-122">Name</span></span> | <span data-ttu-id="13bf1-123">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="13bf1-123">In/Out</span></span> | [<span data-ttu-id="13bf1-124">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="13bf1-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="13bf1-125">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="13bf1-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="13bf1-126">Taille</span><span class="sxs-lookup"><span data-stu-id="13bf1-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="13bf1-127">s</span><span class="sxs-lookup"><span data-stu-id="13bf1-127">s</span></span>    | <span data-ttu-id="13bf1-128">in</span><span class="sxs-lookup"><span data-stu-id="13bf1-128">in</span></span>     | [<span data-ttu-id="13bf1-129">**object**</span><span class="sxs-lookup"><span data-stu-id="13bf1-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="13bf1-130">sampler2D</span><span class="sxs-lookup"><span data-stu-id="13bf1-130">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="13bf1-131">1</span><span class="sxs-lookup"><span data-stu-id="13bf1-131">1</span></span>    |
| <span data-ttu-id="13bf1-132">t</span><span class="sxs-lookup"><span data-stu-id="13bf1-132">t</span></span>    | <span data-ttu-id="13bf1-133">in</span><span class="sxs-lookup"><span data-stu-id="13bf1-133">in</span></span>     | [<span data-ttu-id="13bf1-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="13bf1-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="13bf1-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="13bf1-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="13bf1-136">2</span><span class="sxs-lookup"><span data-stu-id="13bf1-136">2</span></span>    |
| <span data-ttu-id="13bf1-137">DDX</span><span class="sxs-lookup"><span data-stu-id="13bf1-137">ddx</span></span>  | <span data-ttu-id="13bf1-138">in</span><span class="sxs-lookup"><span data-stu-id="13bf1-138">in</span></span>     | [<span data-ttu-id="13bf1-139">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="13bf1-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="13bf1-140">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="13bf1-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="13bf1-141">2</span><span class="sxs-lookup"><span data-stu-id="13bf1-141">2</span></span>    |
| <span data-ttu-id="13bf1-142">ddy</span><span class="sxs-lookup"><span data-stu-id="13bf1-142">ddy</span></span>  | <span data-ttu-id="13bf1-143">in</span><span class="sxs-lookup"><span data-stu-id="13bf1-143">in</span></span>     | [<span data-ttu-id="13bf1-144">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="13bf1-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="13bf1-145">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="13bf1-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="13bf1-146">2</span><span class="sxs-lookup"><span data-stu-id="13bf1-146">2</span></span>    |
| <span data-ttu-id="13bf1-147">Av</span><span class="sxs-lookup"><span data-stu-id="13bf1-147">ret</span></span>  | <span data-ttu-id="13bf1-148">out</span><span class="sxs-lookup"><span data-stu-id="13bf1-148">out</span></span>    | [<span data-ttu-id="13bf1-149">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="13bf1-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="13bf1-150">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="13bf1-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="13bf1-151">4</span><span class="sxs-lookup"><span data-stu-id="13bf1-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="13bf1-152">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="13bf1-152">Minimum Shader Model</span></span>

<span data-ttu-id="13bf1-153">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="13bf1-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="13bf1-154">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="13bf1-154">Shader Model</span></span>                                              | <span data-ttu-id="13bf1-155">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="13bf1-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="13bf1-156">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="13bf1-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="13bf1-157">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="13bf1-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="13bf1-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13bf1-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="13bf1-159">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="13bf1-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="13bf1-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13bf1-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="13bf1-161">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="13bf1-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="13bf1-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13bf1-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="13bf1-163">non</span><span class="sxs-lookup"><span data-stu-id="13bf1-163">no</span></span>                       |



 

1.  <span data-ttu-id="13bf1-164">La réorganisation de code importante est effectuée pour déplacer des calculs de dégradé en dehors du contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="13bf1-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="13bf1-165">Si le \_ Cap D3DPSHADERCAPS2 0 est défini avec D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, le compilateur mappe cette fonction à texldd.</span><span class="sxs-lookup"><span data-stu-id="13bf1-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="remarks"></a><span data-ttu-id="13bf1-166">Notes</span><span class="sxs-lookup"><span data-stu-id="13bf1-166">Remarks</span></span>

<span data-ttu-id="13bf1-167">Lorsque le contrôle de Flow est présent dans un nuanceur, le résultat d’un calcul de dégradé demandé dans un chemin de branche donné est ambigu lorsque les pixels adjacents peuvent descendre dans des chemins de contrôle de Flow distincts.</span><span class="sxs-lookup"><span data-stu-id="13bf1-167">When flow control is present in a shader, the result of a gradient calculation requested inside a given branch path is ambiguous when adjacent pixels may go down separate flow control paths.</span></span> <span data-ttu-id="13bf1-168">Par conséquent, il est jugé illégal d’utiliser toute opération de nuanceur de pixels qui demande un calcul de dégradé à un emplacement qui se trouve à l’intérieur d’une construction de contrôle de Flow qui peut varier d’un pixel à l’autre, pour une primitive donnée en cours de pixellisation.</span><span class="sxs-lookup"><span data-stu-id="13bf1-168">Therefore, it is deemed illegal to use any pixel shader operation that requests a gradient calculation to occur at a location that is inside a flow control construct which could vary across pixels for a given primitive being rasterized.</span></span> <span data-ttu-id="13bf1-169">Si l’un des côtés d’une instruction **If** avec l’attribut Branch utilise une fonction de dégradé, une erreur de compilateur peut être générée.</span><span class="sxs-lookup"><span data-stu-id="13bf1-169">If either side of an **if** statement with the branch attribute uses a gradient function a compiler error may be generated.</span></span> <span data-ttu-id="13bf1-170">Consultez l' [instruction if (DirectX HLSL)](dx-graphics-hlsl-if.md).</span><span class="sxs-lookup"><span data-stu-id="13bf1-170">See [if Statement (DirectX HLSL)](dx-graphics-hlsl-if.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="13bf1-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13bf1-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13bf1-172">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="13bf1-172">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

