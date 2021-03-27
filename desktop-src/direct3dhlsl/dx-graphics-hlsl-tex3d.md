---
title: tex3D (référence HLSL)
description: Échantillonne une texture 3D.
ms.assetid: 713eec24-bdf5-456e-98da-30e2c9d7e808
keywords:
- HLSL tex3D
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3a071d00dedabdff02bae302c71aa8ecece4ba2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729517"
---
# <a name="tex3d-hlsl-reference"></a><span data-ttu-id="0ab34-104">tex3D (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ab34-104">tex3D (HLSL reference)</span></span>

<span data-ttu-id="0ab34-105">Échantillonne une texture 3D.</span><span class="sxs-lookup"><span data-stu-id="0ab34-105">Samples a 3D texture.</span></span>



| <span data-ttu-id="0ab34-106">RET tex3D (s, t)</span><span class="sxs-lookup"><span data-stu-id="0ab34-106">ret tex3D(s, t)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="0ab34-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ab34-107">Parameters</span></span>



| <span data-ttu-id="0ab34-108">Élément</span><span class="sxs-lookup"><span data-stu-id="0ab34-108">Item</span></span>                                                   | <span data-ttu-id="0ab34-109">Description</span><span class="sxs-lookup"><span data-stu-id="0ab34-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="0ab34-110"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="0ab34-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="0ab34-111">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="0ab34-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="0ab34-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="0ab34-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="0ab34-113">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="0ab34-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0ab34-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0ab34-114">Return Value</span></span>

<span data-ttu-id="0ab34-115">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="0ab34-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="0ab34-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="0ab34-116">Type Description</span></span>



| <span data-ttu-id="0ab34-117">Nom</span><span class="sxs-lookup"><span data-stu-id="0ab34-117">Name</span></span> | <span data-ttu-id="0ab34-118">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="0ab34-118">In/Out</span></span> | [<span data-ttu-id="0ab34-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="0ab34-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="0ab34-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="0ab34-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0ab34-121">Taille</span><span class="sxs-lookup"><span data-stu-id="0ab34-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="0ab34-122">s</span><span class="sxs-lookup"><span data-stu-id="0ab34-122">s</span></span>    | <span data-ttu-id="0ab34-123">in</span><span class="sxs-lookup"><span data-stu-id="0ab34-123">in</span></span>     | [<span data-ttu-id="0ab34-124">**object**</span><span class="sxs-lookup"><span data-stu-id="0ab34-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0ab34-125">sampler3D</span><span class="sxs-lookup"><span data-stu-id="0ab34-125">sampler3D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="0ab34-126">1</span><span class="sxs-lookup"><span data-stu-id="0ab34-126">1</span></span>    |
| <span data-ttu-id="0ab34-127">t</span><span class="sxs-lookup"><span data-stu-id="0ab34-127">t</span></span>    | <span data-ttu-id="0ab34-128">in</span><span class="sxs-lookup"><span data-stu-id="0ab34-128">in</span></span>     | [<span data-ttu-id="0ab34-129">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="0ab34-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0ab34-130">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="0ab34-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0ab34-131">3</span><span class="sxs-lookup"><span data-stu-id="0ab34-131">3</span></span>    |
| <span data-ttu-id="0ab34-132">Av</span><span class="sxs-lookup"><span data-stu-id="0ab34-132">ret</span></span>  | <span data-ttu-id="0ab34-133">out</span><span class="sxs-lookup"><span data-stu-id="0ab34-133">out</span></span>    | [<span data-ttu-id="0ab34-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="0ab34-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="0ab34-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="0ab34-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0ab34-136">4</span><span class="sxs-lookup"><span data-stu-id="0ab34-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0ab34-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0ab34-137">Minimum Shader Model</span></span>

<span data-ttu-id="0ab34-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0ab34-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0ab34-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0ab34-139">Shader Model</span></span>                                              | <span data-ttu-id="0ab34-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0ab34-140">Supported</span></span>                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ab34-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="0ab34-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0ab34-142">Oui (nuanceur de pixels uniquement), mais vous devez utiliser l' [option de compilation héritée](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) lors de la compilation.</span><span class="sxs-lookup"><span data-stu-id="0ab34-142">yes (pixel shader only), but you must use the [legacy compile option](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) when compiling.</span></span> |
| [<span data-ttu-id="0ab34-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ab34-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0ab34-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="0ab34-144">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="0ab34-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ab34-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0ab34-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="0ab34-146">yes (pixel shader only)</span></span>                                                                                                           |
| [<span data-ttu-id="0ab34-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0ab34-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0ab34-148">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="0ab34-148">yes (pixel shader only)</span></span>                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="0ab34-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ab34-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ab34-150">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0ab34-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

