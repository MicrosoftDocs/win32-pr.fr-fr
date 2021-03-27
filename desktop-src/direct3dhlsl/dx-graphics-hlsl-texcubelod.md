---
title: texCUBElod
description: Échantillonne une texture de cube avec des mipmaps. Le LOD mipmap est spécifié dans t.w.
ms.assetid: fa7b236d-2c52-42bd-9123-919541f9e675
keywords:
- HLSL texCUBElod
topic_type:
- apiref
api_name:
- texCUBElod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72635211263085f03b87c2e013ea57d1b6a21464
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971791"
---
# <a name="texcubelod"></a><span data-ttu-id="3ebc4-105">texCUBElod</span><span class="sxs-lookup"><span data-stu-id="3ebc4-105">texCUBElod</span></span>

<span data-ttu-id="3ebc4-106">Échantillonne une texture de cube avec des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="3ebc4-106">Samples a cube texture with mipmaps.</span></span> <span data-ttu-id="3ebc4-107">Le LOD mipmap est spécifié dans t.w.</span><span class="sxs-lookup"><span data-stu-id="3ebc4-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="3ebc4-108">RET texCUBElod (s, t)</span><span class="sxs-lookup"><span data-stu-id="3ebc4-108">ret texCUBElod(s, t)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="3ebc4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ebc4-109">Parameters</span></span>



| <span data-ttu-id="3ebc4-110">Élément</span><span class="sxs-lookup"><span data-stu-id="3ebc4-110">Item</span></span>                                                   | <span data-ttu-id="3ebc4-111">Description</span><span class="sxs-lookup"><span data-stu-id="3ebc4-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="3ebc4-112"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="3ebc4-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="3ebc4-113">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="3ebc4-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="3ebc4-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="3ebc4-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="3ebc4-115">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="3ebc4-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3ebc4-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3ebc4-116">Return Value</span></span>

<span data-ttu-id="3ebc4-117">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="3ebc4-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="3ebc4-118">Description du type</span><span class="sxs-lookup"><span data-stu-id="3ebc4-118">Type Description</span></span>



| <span data-ttu-id="3ebc4-119">Nom</span><span class="sxs-lookup"><span data-stu-id="3ebc4-119">Name</span></span> | <span data-ttu-id="3ebc4-120">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="3ebc4-120">In/Out</span></span> | [<span data-ttu-id="3ebc4-121">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="3ebc4-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="3ebc4-122">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="3ebc4-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="3ebc4-123">Taille</span><span class="sxs-lookup"><span data-stu-id="3ebc4-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="3ebc4-124">s</span><span class="sxs-lookup"><span data-stu-id="3ebc4-124">s</span></span>    | <span data-ttu-id="3ebc4-125">in</span><span class="sxs-lookup"><span data-stu-id="3ebc4-125">in</span></span>     | [<span data-ttu-id="3ebc4-126">**object**</span><span class="sxs-lookup"><span data-stu-id="3ebc4-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3ebc4-127">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="3ebc4-127">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="3ebc4-128">1</span><span class="sxs-lookup"><span data-stu-id="3ebc4-128">1</span></span>    |
| <span data-ttu-id="3ebc4-129">t</span><span class="sxs-lookup"><span data-stu-id="3ebc4-129">t</span></span>    | <span data-ttu-id="3ebc4-130">in</span><span class="sxs-lookup"><span data-stu-id="3ebc4-130">in</span></span>     | [<span data-ttu-id="3ebc4-131">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="3ebc4-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3ebc4-132">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="3ebc4-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3ebc4-133">4</span><span class="sxs-lookup"><span data-stu-id="3ebc4-133">4</span></span>    |
| <span data-ttu-id="3ebc4-134">Av</span><span class="sxs-lookup"><span data-stu-id="3ebc4-134">ret</span></span>  | <span data-ttu-id="3ebc4-135">out</span><span class="sxs-lookup"><span data-stu-id="3ebc4-135">out</span></span>    | [<span data-ttu-id="3ebc4-136">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="3ebc4-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="3ebc4-137">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="3ebc4-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="3ebc4-138">4</span><span class="sxs-lookup"><span data-stu-id="3ebc4-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3ebc4-139">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3ebc4-139">Minimum Shader Model</span></span>

<span data-ttu-id="3ebc4-140">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3ebc4-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3ebc4-141">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3ebc4-141">Shader Model</span></span>                                              | <span data-ttu-id="3ebc4-142">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3ebc4-142">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="3ebc4-143">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="3ebc4-143">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3ebc4-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="3ebc4-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="3ebc4-145">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3ebc4-145">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3ebc4-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="3ebc4-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="3ebc4-147">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3ebc4-147">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3ebc4-148">non</span><span class="sxs-lookup"><span data-stu-id="3ebc4-148">no</span></span>                      |
| [<span data-ttu-id="3ebc4-149">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3ebc4-149">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3ebc4-150">non</span><span class="sxs-lookup"><span data-stu-id="3ebc4-150">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="3ebc4-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ebc4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ebc4-152">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="3ebc4-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

