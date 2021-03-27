---
title: tex1Dproj
description: Échantillonne une texture 1D à l’aide d’une division projective ; la coordonnée de texture est divisée par t. w avant que la recherche ait lieu.
ms.assetid: 7cfe996d-3967-40da-b0e7-e03938478594
keywords:
- HLSL tex1Dproj
topic_type:
- apiref
api_name:
- tex1Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34fc1c019ab5479fe8a23446c94073e19ca68de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971763"
---
# <a name="tex1dproj"></a><span data-ttu-id="d4c3b-104">tex1Dproj</span><span class="sxs-lookup"><span data-stu-id="d4c3b-104">tex1Dproj</span></span>

<span data-ttu-id="d4c3b-105">Échantillonne une texture 1D à l’aide d’une division projective ; la coordonnée de texture est divisée par t. w avant que la recherche ait lieu.</span><span class="sxs-lookup"><span data-stu-id="d4c3b-105">Samples a 1D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="d4c3b-106">RET tex1Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="d4c3b-106">ret tex1Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="d4c3b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4c3b-107">Parameters</span></span>



| <span data-ttu-id="d4c3b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="d4c3b-108">Item</span></span>                                                   | <span data-ttu-id="d4c3b-109">Description</span><span class="sxs-lookup"><span data-stu-id="d4c3b-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="d4c3b-110"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d4c3b-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="d4c3b-111">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="d4c3b-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="d4c3b-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="d4c3b-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="d4c3b-113">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="d4c3b-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d4c3b-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d4c3b-114">Return Value</span></span>

<span data-ttu-id="d4c3b-115">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="d4c3b-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="d4c3b-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="d4c3b-116">Type Description</span></span>



| <span data-ttu-id="d4c3b-117">Nom</span><span class="sxs-lookup"><span data-stu-id="d4c3b-117">Name</span></span> | <span data-ttu-id="d4c3b-118">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="d4c3b-118">In/Out</span></span> | [<span data-ttu-id="d4c3b-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="d4c3b-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d4c3b-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="d4c3b-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d4c3b-121">Taille</span><span class="sxs-lookup"><span data-stu-id="d4c3b-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="d4c3b-122">s</span><span class="sxs-lookup"><span data-stu-id="d4c3b-122">s</span></span>    | <span data-ttu-id="d4c3b-123">in</span><span class="sxs-lookup"><span data-stu-id="d4c3b-123">in</span></span>     | [<span data-ttu-id="d4c3b-124">**object**</span><span class="sxs-lookup"><span data-stu-id="d4c3b-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d4c3b-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="d4c3b-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="d4c3b-126">1</span><span class="sxs-lookup"><span data-stu-id="d4c3b-126">1</span></span>    |
| <span data-ttu-id="d4c3b-127">t</span><span class="sxs-lookup"><span data-stu-id="d4c3b-127">t</span></span>    | <span data-ttu-id="d4c3b-128">in</span><span class="sxs-lookup"><span data-stu-id="d4c3b-128">in</span></span>     | [<span data-ttu-id="d4c3b-129">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="d4c3b-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d4c3b-130">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d4c3b-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d4c3b-131">4</span><span class="sxs-lookup"><span data-stu-id="d4c3b-131">4</span></span>    |
| <span data-ttu-id="d4c3b-132">Av</span><span class="sxs-lookup"><span data-stu-id="d4c3b-132">ret</span></span>  | <span data-ttu-id="d4c3b-133">out</span><span class="sxs-lookup"><span data-stu-id="d4c3b-133">out</span></span>    | [<span data-ttu-id="d4c3b-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="d4c3b-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d4c3b-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d4c3b-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d4c3b-136">4</span><span class="sxs-lookup"><span data-stu-id="d4c3b-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d4c3b-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d4c3b-137">Minimum Shader Model</span></span>

<span data-ttu-id="d4c3b-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d4c3b-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d4c3b-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d4c3b-139">Shader Model</span></span>                                              | <span data-ttu-id="d4c3b-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d4c3b-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="d4c3b-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="d4c3b-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d4c3b-142">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="d4c3b-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="d4c3b-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d4c3b-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d4c3b-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="d4c3b-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="d4c3b-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d4c3b-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d4c3b-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="d4c3b-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="d4c3b-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d4c3b-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d4c3b-148">non</span><span class="sxs-lookup"><span data-stu-id="d4c3b-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="d4c3b-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4c3b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c3b-150">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d4c3b-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

