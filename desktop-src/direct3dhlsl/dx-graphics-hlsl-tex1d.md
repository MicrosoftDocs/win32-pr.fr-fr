---
title: tex1D (référence HLSL)
description: Échantillonne une texture 1D.
ms.assetid: 587be0fd-af12-4bf0-862b-84988435e90e
keywords:
- HLSL tex1D
topic_type:
- apiref
api_name:
- tex1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dec5cc8a35b18c35076f99443ad3c1166fcf410
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728204"
---
# <a name="tex1d-hlsl-reference"></a><span data-ttu-id="feaef-104">tex1D (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="feaef-104">tex1D (HLSL reference)</span></span>

<span data-ttu-id="feaef-105">Échantillonne une texture 1D.</span><span class="sxs-lookup"><span data-stu-id="feaef-105">Samples a 1D texture.</span></span>



| <span data-ttu-id="feaef-106">RET tex1D (s, t)</span><span class="sxs-lookup"><span data-stu-id="feaef-106">ret tex1D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="feaef-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="feaef-107">Parameters</span></span>



| <span data-ttu-id="feaef-108">Élément</span><span class="sxs-lookup"><span data-stu-id="feaef-108">Item</span></span>                                                   | <span data-ttu-id="feaef-109">Description</span><span class="sxs-lookup"><span data-stu-id="feaef-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="feaef-110"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="feaef-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="feaef-111">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="feaef-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="feaef-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="feaef-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="feaef-113">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="feaef-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="feaef-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="feaef-114">Return Value</span></span>

<span data-ttu-id="feaef-115">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="feaef-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="feaef-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="feaef-116">Type Description</span></span>



| <span data-ttu-id="feaef-117">Nom</span><span class="sxs-lookup"><span data-stu-id="feaef-117">Name</span></span> | <span data-ttu-id="feaef-118">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="feaef-118">In/Out</span></span> | [<span data-ttu-id="feaef-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="feaef-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="feaef-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="feaef-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="feaef-121">Taille</span><span class="sxs-lookup"><span data-stu-id="feaef-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="feaef-122">s</span><span class="sxs-lookup"><span data-stu-id="feaef-122">s</span></span>    | <span data-ttu-id="feaef-123">in</span><span class="sxs-lookup"><span data-stu-id="feaef-123">in</span></span>     | [<span data-ttu-id="feaef-124">**object**</span><span class="sxs-lookup"><span data-stu-id="feaef-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="feaef-125">sampler1D</span><span class="sxs-lookup"><span data-stu-id="feaef-125">sampler1D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="feaef-126">1</span><span class="sxs-lookup"><span data-stu-id="feaef-126">1</span></span>    |
| <span data-ttu-id="feaef-127">t</span><span class="sxs-lookup"><span data-stu-id="feaef-127">t</span></span>    | <span data-ttu-id="feaef-128">in</span><span class="sxs-lookup"><span data-stu-id="feaef-128">in</span></span>     | [<span data-ttu-id="feaef-129">**scalaire**</span><span class="sxs-lookup"><span data-stu-id="feaef-129">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="feaef-130">**float**</span><span class="sxs-lookup"><span data-stu-id="feaef-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="feaef-131">1</span><span class="sxs-lookup"><span data-stu-id="feaef-131">1</span></span>    |
| <span data-ttu-id="feaef-132">Av</span><span class="sxs-lookup"><span data-stu-id="feaef-132">ret</span></span>  | <span data-ttu-id="feaef-133">out</span><span class="sxs-lookup"><span data-stu-id="feaef-133">out</span></span>    | [<span data-ttu-id="feaef-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="feaef-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="feaef-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="feaef-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="feaef-136">4</span><span class="sxs-lookup"><span data-stu-id="feaef-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="feaef-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="feaef-137">Minimum Shader Model</span></span>

<span data-ttu-id="feaef-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="feaef-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="feaef-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="feaef-139">Shader Model</span></span>                                              | <span data-ttu-id="feaef-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="feaef-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="feaef-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="feaef-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="feaef-142">Oui (nuanceur de pixels uniquement), mais vous devez utiliser l' [option de compilation héritée](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) lors de la compilation.</span><span class="sxs-lookup"><span data-stu-id="feaef-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="feaef-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="feaef-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="feaef-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="feaef-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="feaef-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="feaef-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="feaef-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="feaef-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="feaef-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="feaef-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="feaef-148">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="feaef-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="feaef-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="feaef-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feaef-150">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="feaef-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

