---
title: texCUBE (référence HLSL)-sélectionner le niveau MIP
description: Échantillonne une texture de cube à l’aide d’un dégradé pour sélectionner le niveau MIP. | texCUBE (référence HLSL)
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
keywords:
- HLSL texCUBE
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6286b4fedb94b9fd5c84c76171e9478f06e16ce4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982674"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a><span data-ttu-id="b28cd-105">texCUBE (référence HLSL)-sélectionner le niveau MIP</span><span class="sxs-lookup"><span data-stu-id="b28cd-105">texCUBE (HLSL reference) - Select the mip level</span></span>

<span data-ttu-id="b28cd-106">Échantillonne une texture de cube à l’aide d’un dégradé pour sélectionner le niveau MIP.</span><span class="sxs-lookup"><span data-stu-id="b28cd-106">Samples a cube texture using a gradient to select the mip level.</span></span>



| <span data-ttu-id="b28cd-107">RET texCUBE (s, t, DDX, ddy)</span><span class="sxs-lookup"><span data-stu-id="b28cd-107">ret texCUBE(s, t, ddx, ddy)</span></span> |
|-----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="b28cd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b28cd-108">Parameters</span></span>



| <span data-ttu-id="b28cd-109">Élément</span><span class="sxs-lookup"><span data-stu-id="b28cd-109">Item</span></span>                                                         | <span data-ttu-id="b28cd-110">Description</span><span class="sxs-lookup"><span data-stu-id="b28cd-110">Description</span></span>                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b28cd-111"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b28cd-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>       | <span data-ttu-id="b28cd-112">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="b28cd-112">\[in\] The sampler state.</span></span><br/>                                         |
| <span data-ttu-id="b28cd-113"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="b28cd-113"><span id="t"></span><span id="T"></span>*t*</span></span><br/>       | <span data-ttu-id="b28cd-114">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="b28cd-114">\[in\] The texture coordinate.</span></span><br/>                                    |
| <span data-ttu-id="b28cd-115"><span id="ddx"></span><span id="DDX"></span>*DDX*</span><span class="sxs-lookup"><span data-stu-id="b28cd-115"><span id="ddx"></span><span id="DDX"></span>*ddx*</span></span><br/> | <span data-ttu-id="b28cd-116">\[en \] taux de changement de la géométrie de la surface dans l’axe x.</span><span class="sxs-lookup"><span data-stu-id="b28cd-116">\[in\] Rate of change of the surface geometry in the x direction.</span></span><br/> |
| <span data-ttu-id="b28cd-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span><span class="sxs-lookup"><span data-stu-id="b28cd-117"><span id="ddy"></span><span id="DDY"></span>*ddy*</span></span><br/> | <span data-ttu-id="b28cd-118">\[en \] taux de changement de la géométrie de la surface dans l’axe y.</span><span class="sxs-lookup"><span data-stu-id="b28cd-118">\[in\] Rate of change of the surface geometry in the y direction.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b28cd-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b28cd-119">Return Value</span></span>

<span data-ttu-id="b28cd-120">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="b28cd-120">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="b28cd-121">Description du type</span><span class="sxs-lookup"><span data-stu-id="b28cd-121">Type Description</span></span>



| <span data-ttu-id="b28cd-122">Nom</span><span class="sxs-lookup"><span data-stu-id="b28cd-122">Name</span></span> | <span data-ttu-id="b28cd-123">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="b28cd-123">In/Out</span></span> | [<span data-ttu-id="b28cd-124">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="b28cd-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="b28cd-125">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="b28cd-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b28cd-126">Taille</span><span class="sxs-lookup"><span data-stu-id="b28cd-126">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="b28cd-127">s</span><span class="sxs-lookup"><span data-stu-id="b28cd-127">s</span></span>    | <span data-ttu-id="b28cd-128">in</span><span class="sxs-lookup"><span data-stu-id="b28cd-128">in</span></span>     | [<span data-ttu-id="b28cd-129">**object**</span><span class="sxs-lookup"><span data-stu-id="b28cd-129">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b28cd-130">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="b28cd-130">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="b28cd-131">1</span><span class="sxs-lookup"><span data-stu-id="b28cd-131">1</span></span>    |
| <span data-ttu-id="b28cd-132">t</span><span class="sxs-lookup"><span data-stu-id="b28cd-132">t</span></span>    | <span data-ttu-id="b28cd-133">in</span><span class="sxs-lookup"><span data-stu-id="b28cd-133">in</span></span>     | [<span data-ttu-id="b28cd-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="b28cd-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b28cd-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b28cd-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b28cd-136">3</span><span class="sxs-lookup"><span data-stu-id="b28cd-136">3</span></span>    |
| <span data-ttu-id="b28cd-137">DDX</span><span class="sxs-lookup"><span data-stu-id="b28cd-137">ddx</span></span>  | <span data-ttu-id="b28cd-138">in</span><span class="sxs-lookup"><span data-stu-id="b28cd-138">in</span></span>     | [<span data-ttu-id="b28cd-139">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="b28cd-139">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b28cd-140">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b28cd-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b28cd-141">3</span><span class="sxs-lookup"><span data-stu-id="b28cd-141">3</span></span>    |
| <span data-ttu-id="b28cd-142">ddy</span><span class="sxs-lookup"><span data-stu-id="b28cd-142">ddy</span></span>  | <span data-ttu-id="b28cd-143">in</span><span class="sxs-lookup"><span data-stu-id="b28cd-143">in</span></span>     | [<span data-ttu-id="b28cd-144">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="b28cd-144">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b28cd-145">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b28cd-145">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b28cd-146">3</span><span class="sxs-lookup"><span data-stu-id="b28cd-146">3</span></span>    |
| <span data-ttu-id="b28cd-147">Av</span><span class="sxs-lookup"><span data-stu-id="b28cd-147">ret</span></span>  | <span data-ttu-id="b28cd-148">out</span><span class="sxs-lookup"><span data-stu-id="b28cd-148">out</span></span>    | [<span data-ttu-id="b28cd-149">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="b28cd-149">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b28cd-150">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b28cd-150">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b28cd-151">4</span><span class="sxs-lookup"><span data-stu-id="b28cd-151">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b28cd-152">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b28cd-152">Minimum Shader Model</span></span>

<span data-ttu-id="b28cd-153">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b28cd-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b28cd-154">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b28cd-154">Shader Model</span></span>                                              | <span data-ttu-id="b28cd-155">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b28cd-155">Supported</span></span>                |
|-----------------------------------------------------------|--------------------------|
| [<span data-ttu-id="b28cd-156">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="b28cd-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b28cd-157">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="b28cd-157">yes (pixel shader only)</span></span>  |
| [<span data-ttu-id="b28cd-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b28cd-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b28cd-159">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="b28cd-159">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="b28cd-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b28cd-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b28cd-161">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="b28cd-161">yes  (pixel shader only)</span></span> |
| [<span data-ttu-id="b28cd-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b28cd-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b28cd-163">non</span><span class="sxs-lookup"><span data-stu-id="b28cd-163">no</span></span>                       |



 

1.  <span data-ttu-id="b28cd-164">La réorganisation de code importante est effectuée pour déplacer des calculs de dégradé en dehors du contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="b28cd-164">Significant code reordering is done to move gradient computations outside of flow control.</span></span>
2.  <span data-ttu-id="b28cd-165">Si le \_ Cap D3DPSHADERCAPS2 0 est défini avec D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, le compilateur mappe cette fonction à texldd.</span><span class="sxs-lookup"><span data-stu-id="b28cd-165">If the D3DPSHADERCAPS2\_0 cap is set with D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS, the compiler maps this function to texldd.</span></span>

## <a name="see-also"></a><span data-ttu-id="b28cd-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b28cd-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b28cd-167">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b28cd-167">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

