---
title: tex3Dproj
description: Échantillonne une texture 3D à l’aide d’une division projective ; la coordonnée de texture est divisée par t. w avant que la recherche ait lieu.
ms.assetid: c7062ef0-3169-4cbe-b47b-4efc80944963
keywords:
- HLSL tex3Dproj
topic_type:
- apiref
api_name:
- tex3Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 519477b7dba4f746dc1720a08c2ce581ab7b7205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508077"
---
# <a name="tex3dproj"></a><span data-ttu-id="99ee6-104">tex3Dproj</span><span class="sxs-lookup"><span data-stu-id="99ee6-104">tex3Dproj</span></span>

<span data-ttu-id="99ee6-105">Échantillonne une texture 3D à l’aide d’une division projective ; la coordonnée de texture est divisée par t. w avant que la recherche ait lieu.</span><span class="sxs-lookup"><span data-stu-id="99ee6-105">Samples a 3D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="99ee6-106">RET tex3Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="99ee6-106">ret tex3Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="99ee6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99ee6-107">Parameters</span></span>



| <span data-ttu-id="99ee6-108">Élément</span><span class="sxs-lookup"><span data-stu-id="99ee6-108">Item</span></span>                                                   | <span data-ttu-id="99ee6-109">Description</span><span class="sxs-lookup"><span data-stu-id="99ee6-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="99ee6-110"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="99ee6-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="99ee6-111">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="99ee6-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="99ee6-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="99ee6-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="99ee6-113">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="99ee6-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="99ee6-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="99ee6-114">Return Value</span></span>

<span data-ttu-id="99ee6-115">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="99ee6-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="99ee6-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="99ee6-116">Type Description</span></span>



| <span data-ttu-id="99ee6-117">Nom</span><span class="sxs-lookup"><span data-stu-id="99ee6-117">Name</span></span> | <span data-ttu-id="99ee6-118">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="99ee6-118">In/Out</span></span> | [<span data-ttu-id="99ee6-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="99ee6-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="99ee6-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="99ee6-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="99ee6-121">Taille</span><span class="sxs-lookup"><span data-stu-id="99ee6-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="99ee6-122">s</span><span class="sxs-lookup"><span data-stu-id="99ee6-122">s</span></span>    | <span data-ttu-id="99ee6-123">in</span><span class="sxs-lookup"><span data-stu-id="99ee6-123">in</span></span>     | [<span data-ttu-id="99ee6-124">**object**</span><span class="sxs-lookup"><span data-stu-id="99ee6-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="99ee6-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="99ee6-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="99ee6-126">1</span><span class="sxs-lookup"><span data-stu-id="99ee6-126">1</span></span>    |
| <span data-ttu-id="99ee6-127">t</span><span class="sxs-lookup"><span data-stu-id="99ee6-127">t</span></span>    | <span data-ttu-id="99ee6-128">in</span><span class="sxs-lookup"><span data-stu-id="99ee6-128">in</span></span>     | [<span data-ttu-id="99ee6-129">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="99ee6-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="99ee6-130">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="99ee6-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="99ee6-131">4</span><span class="sxs-lookup"><span data-stu-id="99ee6-131">4</span></span>    |
| <span data-ttu-id="99ee6-132">Av</span><span class="sxs-lookup"><span data-stu-id="99ee6-132">ret</span></span>  | <span data-ttu-id="99ee6-133">out</span><span class="sxs-lookup"><span data-stu-id="99ee6-133">out</span></span>    | [<span data-ttu-id="99ee6-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="99ee6-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="99ee6-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="99ee6-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="99ee6-136">4</span><span class="sxs-lookup"><span data-stu-id="99ee6-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="99ee6-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="99ee6-137">Minimum Shader Model</span></span>

<span data-ttu-id="99ee6-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="99ee6-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="99ee6-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="99ee6-139">Shader Model</span></span>                                              | <span data-ttu-id="99ee6-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="99ee6-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="99ee6-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="99ee6-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="99ee6-142">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="99ee6-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="99ee6-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="99ee6-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="99ee6-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="99ee6-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="99ee6-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="99ee6-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="99ee6-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="99ee6-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="99ee6-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="99ee6-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="99ee6-148">non</span><span class="sxs-lookup"><span data-stu-id="99ee6-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="99ee6-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99ee6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ee6-150">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="99ee6-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

