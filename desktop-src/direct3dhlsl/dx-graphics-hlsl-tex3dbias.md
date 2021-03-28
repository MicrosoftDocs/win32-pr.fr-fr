---
title: tex3Dbias
description: Échantillonne une texture 3D après avoir biaisé le niveau MIP par t.w.
ms.assetid: 6a506036-90d1-420c-a712-a373068c8c16
keywords:
- HLSL tex3Dbias
topic_type:
- apiref
api_name:
- tex3Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53fb0a196831a9dd9d7f7cbe7c34c56259f9a0e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382747"
---
# <a name="tex3dbias"></a><span data-ttu-id="9bf26-104">tex3Dbias</span><span class="sxs-lookup"><span data-stu-id="9bf26-104">tex3Dbias</span></span>

<span data-ttu-id="9bf26-105">Échantillonne une texture 3D après avoir biaisé le niveau MIP par t.w.</span><span class="sxs-lookup"><span data-stu-id="9bf26-105">Samples a 3D texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="9bf26-106">RET tex3Dbias (s, t)</span><span class="sxs-lookup"><span data-stu-id="9bf26-106">ret tex3Dbias(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="9bf26-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9bf26-107">Parameters</span></span>



| <span data-ttu-id="9bf26-108">Élément</span><span class="sxs-lookup"><span data-stu-id="9bf26-108">Item</span></span>                                                   | <span data-ttu-id="9bf26-109">Description</span><span class="sxs-lookup"><span data-stu-id="9bf26-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="9bf26-110"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="9bf26-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="9bf26-111">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="9bf26-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="9bf26-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="9bf26-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="9bf26-113">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="9bf26-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="9bf26-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9bf26-114">Return Value</span></span>

<span data-ttu-id="9bf26-115">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="9bf26-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="9bf26-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="9bf26-116">Type Description</span></span>



| <span data-ttu-id="9bf26-117">Nom</span><span class="sxs-lookup"><span data-stu-id="9bf26-117">Name</span></span> | <span data-ttu-id="9bf26-118">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="9bf26-118">In/Out</span></span> | [<span data-ttu-id="9bf26-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="9bf26-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="9bf26-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="9bf26-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="9bf26-121">Taille</span><span class="sxs-lookup"><span data-stu-id="9bf26-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="9bf26-122">s</span><span class="sxs-lookup"><span data-stu-id="9bf26-122">s</span></span>    | <span data-ttu-id="9bf26-123">in</span><span class="sxs-lookup"><span data-stu-id="9bf26-123">in</span></span>     | [<span data-ttu-id="9bf26-124">**object**</span><span class="sxs-lookup"><span data-stu-id="9bf26-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9bf26-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="9bf26-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="9bf26-126">1</span><span class="sxs-lookup"><span data-stu-id="9bf26-126">1</span></span>    |
| <span data-ttu-id="9bf26-127">t</span><span class="sxs-lookup"><span data-stu-id="9bf26-127">t</span></span>    | <span data-ttu-id="9bf26-128">in</span><span class="sxs-lookup"><span data-stu-id="9bf26-128">in</span></span>     | [<span data-ttu-id="9bf26-129">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="9bf26-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9bf26-130">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="9bf26-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9bf26-131">4</span><span class="sxs-lookup"><span data-stu-id="9bf26-131">4</span></span>    |
| <span data-ttu-id="9bf26-132">Av</span><span class="sxs-lookup"><span data-stu-id="9bf26-132">ret</span></span>  | <span data-ttu-id="9bf26-133">out</span><span class="sxs-lookup"><span data-stu-id="9bf26-133">out</span></span>    | [<span data-ttu-id="9bf26-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="9bf26-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9bf26-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="9bf26-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9bf26-136">4</span><span class="sxs-lookup"><span data-stu-id="9bf26-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9bf26-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9bf26-137">Minimum Shader Model</span></span>

<span data-ttu-id="9bf26-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="9bf26-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9bf26-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9bf26-139">Shader Model</span></span>                                              | <span data-ttu-id="9bf26-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9bf26-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="9bf26-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="9bf26-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9bf26-142">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="9bf26-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="9bf26-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bf26-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9bf26-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="9bf26-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="9bf26-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bf26-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9bf26-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="9bf26-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="9bf26-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9bf26-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9bf26-148">non</span><span class="sxs-lookup"><span data-stu-id="9bf26-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="9bf26-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bf26-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bf26-150">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="9bf26-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

