---
title: tex1Dlod
description: Échantillonne une texture 1D avec des mipmaps. Le LOD mipmap est spécifié dans t.w.
ms.assetid: f1700ee6-2f79-4b8b-ad34-30561f319356
keywords:
- HLSL tex1Dlod
topic_type:
- apiref
api_name:
- tex1Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca6379448290d027bba8a8b62f80cac39c84f25
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729157"
---
# <a name="tex1dlod"></a><span data-ttu-id="f2cd6-105">tex1Dlod</span><span class="sxs-lookup"><span data-stu-id="f2cd6-105">tex1Dlod</span></span>

<span data-ttu-id="f2cd6-106">Échantillonne une texture 1D avec des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="f2cd6-106">Samples a 1D texture with mipmaps.</span></span> <span data-ttu-id="f2cd6-107">Le LOD mipmap est spécifié dans t.w.</span><span class="sxs-lookup"><span data-stu-id="f2cd6-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="f2cd6-108">RET tex1Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="f2cd6-108">ret tex1Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="f2cd6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2cd6-109">Parameters</span></span>



| <span data-ttu-id="f2cd6-110">Élément</span><span class="sxs-lookup"><span data-stu-id="f2cd6-110">Item</span></span>                                                   | <span data-ttu-id="f2cd6-111">Description</span><span class="sxs-lookup"><span data-stu-id="f2cd6-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="f2cd6-112"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="f2cd6-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="f2cd6-113">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="f2cd6-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="f2cd6-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="f2cd6-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="f2cd6-115">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="f2cd6-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f2cd6-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f2cd6-116">Return Value</span></span>

<span data-ttu-id="f2cd6-117">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="f2cd6-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="f2cd6-118">Description du type</span><span class="sxs-lookup"><span data-stu-id="f2cd6-118">Type Description</span></span>



| <span data-ttu-id="f2cd6-119">Nom</span><span class="sxs-lookup"><span data-stu-id="f2cd6-119">Name</span></span> | <span data-ttu-id="f2cd6-120">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="f2cd6-120">In/Out</span></span> | [<span data-ttu-id="f2cd6-121">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="f2cd6-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="f2cd6-122">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="f2cd6-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f2cd6-123">Taille</span><span class="sxs-lookup"><span data-stu-id="f2cd6-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="f2cd6-124">s</span><span class="sxs-lookup"><span data-stu-id="f2cd6-124">s</span></span>    | <span data-ttu-id="f2cd6-125">in</span><span class="sxs-lookup"><span data-stu-id="f2cd6-125">in</span></span>     | [<span data-ttu-id="f2cd6-126">**object**</span><span class="sxs-lookup"><span data-stu-id="f2cd6-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f2cd6-127">sampler1D</span><span class="sxs-lookup"><span data-stu-id="f2cd6-127">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="f2cd6-128">1</span><span class="sxs-lookup"><span data-stu-id="f2cd6-128">1</span></span>    |
| <span data-ttu-id="f2cd6-129">t</span><span class="sxs-lookup"><span data-stu-id="f2cd6-129">t</span></span>    | <span data-ttu-id="f2cd6-130">in</span><span class="sxs-lookup"><span data-stu-id="f2cd6-130">in</span></span>     | [<span data-ttu-id="f2cd6-131">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="f2cd6-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f2cd6-132">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="f2cd6-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f2cd6-133">4</span><span class="sxs-lookup"><span data-stu-id="f2cd6-133">4</span></span>    |
| <span data-ttu-id="f2cd6-134">Av</span><span class="sxs-lookup"><span data-stu-id="f2cd6-134">ret</span></span>  | <span data-ttu-id="f2cd6-135">out</span><span class="sxs-lookup"><span data-stu-id="f2cd6-135">out</span></span>    | [<span data-ttu-id="f2cd6-136">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="f2cd6-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="f2cd6-137">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="f2cd6-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f2cd6-138">4</span><span class="sxs-lookup"><span data-stu-id="f2cd6-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f2cd6-139">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f2cd6-139">Minimum Shader Model</span></span>

<span data-ttu-id="f2cd6-140">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f2cd6-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f2cd6-141">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f2cd6-141">Shader Model</span></span>                                              | <span data-ttu-id="f2cd6-142">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f2cd6-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="f2cd6-143">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f2cd6-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f2cd6-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="f2cd6-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="f2cd6-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f2cd6-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f2cd6-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="f2cd6-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="f2cd6-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f2cd6-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f2cd6-148">non</span><span class="sxs-lookup"><span data-stu-id="f2cd6-148">no</span></span>                      |
| [<span data-ttu-id="f2cd6-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f2cd6-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f2cd6-150">non</span><span class="sxs-lookup"><span data-stu-id="f2cd6-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="f2cd6-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2cd6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2cd6-152">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f2cd6-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

