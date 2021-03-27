---
title: tex3Dlod
description: Échantillonne une texture 3D avec des mipmaps. Le LOD mipmap est spécifié dans t.w.
ms.assetid: 9bdd8fa1-8c02-4765-8f4d-61ceb532354e
keywords:
- HLSL tex3Dlod
topic_type:
- apiref
api_name:
- tex3Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bc25af449f7f32e94d4ca344bf5ef3a4d09b376c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971706"
---
# <a name="tex3dlod"></a><span data-ttu-id="92177-105">tex3Dlod</span><span class="sxs-lookup"><span data-stu-id="92177-105">tex3Dlod</span></span>

<span data-ttu-id="92177-106">Échantillonne une texture 3D avec des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="92177-106">Samples a 3D texture with mipmaps.</span></span> <span data-ttu-id="92177-107">Le LOD mipmap est spécifié dans t.w.</span><span class="sxs-lookup"><span data-stu-id="92177-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="92177-108">RET tex3Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="92177-108">ret tex3Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="92177-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92177-109">Parameters</span></span>



| <span data-ttu-id="92177-110">Élément</span><span class="sxs-lookup"><span data-stu-id="92177-110">Item</span></span>                                                   | <span data-ttu-id="92177-111">Description</span><span class="sxs-lookup"><span data-stu-id="92177-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="92177-112"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="92177-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="92177-113">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="92177-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="92177-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="92177-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="92177-115">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="92177-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="92177-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="92177-116">Return Value</span></span>

<span data-ttu-id="92177-117">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="92177-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="92177-118">Description du type</span><span class="sxs-lookup"><span data-stu-id="92177-118">Type Description</span></span>



| <span data-ttu-id="92177-119">Nom</span><span class="sxs-lookup"><span data-stu-id="92177-119">Name</span></span> | <span data-ttu-id="92177-120">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="92177-120">In/Out</span></span> | [<span data-ttu-id="92177-121">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="92177-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="92177-122">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="92177-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="92177-123">Taille</span><span class="sxs-lookup"><span data-stu-id="92177-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="92177-124">s</span><span class="sxs-lookup"><span data-stu-id="92177-124">s</span></span>    | <span data-ttu-id="92177-125">in</span><span class="sxs-lookup"><span data-stu-id="92177-125">in</span></span>     | [<span data-ttu-id="92177-126">**object**</span><span class="sxs-lookup"><span data-stu-id="92177-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="92177-127">sampler3D</span><span class="sxs-lookup"><span data-stu-id="92177-127">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="92177-128">1</span><span class="sxs-lookup"><span data-stu-id="92177-128">1</span></span>    |
| <span data-ttu-id="92177-129">t</span><span class="sxs-lookup"><span data-stu-id="92177-129">t</span></span>    | <span data-ttu-id="92177-130">in</span><span class="sxs-lookup"><span data-stu-id="92177-130">in</span></span>     | [<span data-ttu-id="92177-131">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="92177-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="92177-132">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="92177-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="92177-133">4</span><span class="sxs-lookup"><span data-stu-id="92177-133">4</span></span>    |
| <span data-ttu-id="92177-134">Av</span><span class="sxs-lookup"><span data-stu-id="92177-134">ret</span></span>  | <span data-ttu-id="92177-135">out</span><span class="sxs-lookup"><span data-stu-id="92177-135">out</span></span>    | [<span data-ttu-id="92177-136">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="92177-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="92177-137">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="92177-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="92177-138">4</span><span class="sxs-lookup"><span data-stu-id="92177-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="92177-139">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="92177-139">Minimum Shader Model</span></span>

<span data-ttu-id="92177-140">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="92177-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="92177-141">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="92177-141">Shader Model</span></span>                                              | <span data-ttu-id="92177-142">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="92177-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="92177-143">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="92177-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="92177-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="92177-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="92177-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92177-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="92177-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="92177-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="92177-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92177-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="92177-148">non</span><span class="sxs-lookup"><span data-stu-id="92177-148">no</span></span>                      |
| [<span data-ttu-id="92177-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="92177-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="92177-150">non</span><span class="sxs-lookup"><span data-stu-id="92177-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="92177-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92177-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92177-152">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="92177-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

