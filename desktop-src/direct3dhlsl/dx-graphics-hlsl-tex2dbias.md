---
title: tex2Dbias
description: Échantillonne une texture 2D après avoir biaisé le niveau MIP par t.w.
ms.assetid: adf2891a-732a-4953-875b-df315c19748b
keywords:
- HLSL tex2Dbias
topic_type:
- apiref
api_name:
- tex2Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cfaec24e1d188460d36a24d68b0fde8ddcb45c29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316163"
---
# <a name="tex2dbias"></a><span data-ttu-id="0541e-104">tex2Dbias</span><span class="sxs-lookup"><span data-stu-id="0541e-104">tex2Dbias</span></span>

<span data-ttu-id="0541e-105">Échantillonne une texture 2D après avoir biaisé le niveau MIP par t.w.</span><span class="sxs-lookup"><span data-stu-id="0541e-105">Samples a 2D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="0541e-106">RET tex2Dbias (s, t)</span><span class="sxs-lookup"><span data-stu-id="0541e-106">ret tex2Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="0541e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0541e-107">Parameters</span></span>



| <span data-ttu-id="0541e-108">Élément</span><span class="sxs-lookup"><span data-stu-id="0541e-108">Item</span></span>                                                   | <span data-ttu-id="0541e-109">Description</span><span class="sxs-lookup"><span data-stu-id="0541e-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="0541e-110"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="0541e-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="0541e-111">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="0541e-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="0541e-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="0541e-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="0541e-113">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="0541e-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0541e-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0541e-114">Return Value</span></span>

<span data-ttu-id="0541e-115">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="0541e-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="0541e-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="0541e-116">Type Description</span></span>



| <span data-ttu-id="0541e-117">Nom</span><span class="sxs-lookup"><span data-stu-id="0541e-117">Name</span></span> | <span data-ttu-id="0541e-118">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="0541e-118">In/Out</span></span> | [<span data-ttu-id="0541e-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="0541e-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="0541e-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="0541e-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0541e-121">Taille</span><span class="sxs-lookup"><span data-stu-id="0541e-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="0541e-122">s</span><span class="sxs-lookup"><span data-stu-id="0541e-122">s</span></span>    | <span data-ttu-id="0541e-123">in</span><span class="sxs-lookup"><span data-stu-id="0541e-123">in</span></span>     | [<span data-ttu-id="0541e-124">**object**</span><span class="sxs-lookup"><span data-stu-id="0541e-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0541e-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="0541e-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="0541e-126">1</span><span class="sxs-lookup"><span data-stu-id="0541e-126">1</span></span>    |
| <span data-ttu-id="0541e-127">t</span><span class="sxs-lookup"><span data-stu-id="0541e-127">t</span></span>    | <span data-ttu-id="0541e-128">in</span><span class="sxs-lookup"><span data-stu-id="0541e-128">in</span></span>     | [<span data-ttu-id="0541e-129">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="0541e-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0541e-130">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="0541e-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0541e-131">4</span><span class="sxs-lookup"><span data-stu-id="0541e-131">4</span></span>    |
| <span data-ttu-id="0541e-132">Av</span><span class="sxs-lookup"><span data-stu-id="0541e-132">ret</span></span>  | <span data-ttu-id="0541e-133">out</span><span class="sxs-lookup"><span data-stu-id="0541e-133">out</span></span>    | [<span data-ttu-id="0541e-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="0541e-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0541e-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="0541e-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0541e-136">4</span><span class="sxs-lookup"><span data-stu-id="0541e-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0541e-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0541e-137">Minimum Shader Model</span></span>

<span data-ttu-id="0541e-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0541e-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0541e-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0541e-139">Shader Model</span></span>                                              | <span data-ttu-id="0541e-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0541e-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="0541e-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0541e-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0541e-142">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="0541e-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="0541e-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0541e-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0541e-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="0541e-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="0541e-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0541e-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0541e-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="0541e-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="0541e-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0541e-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0541e-148">non</span><span class="sxs-lookup"><span data-stu-id="0541e-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="0541e-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0541e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0541e-150">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0541e-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

