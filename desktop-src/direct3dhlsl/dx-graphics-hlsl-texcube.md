---
title: texCUBE (référence HLSL)
description: Échantillonne une texture de cube.
ms.assetid: 77943eb9-86e8-4ae4-8975-8f925e084ce4
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
ms.openlocfilehash: 524ed44028372eeabf176c30da8b3a31a8ee7988
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031372"
---
# <a name="texcube-hlsl-reference"></a><span data-ttu-id="b0965-104">texCUBE (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0965-104">texCUBE (HLSL reference)</span></span>

<span data-ttu-id="b0965-105">Échantillonne une texture de cube.</span><span class="sxs-lookup"><span data-stu-id="b0965-105">Samples a cube texture.</span></span>



| <span data-ttu-id="b0965-106">RET texCUBE (s, t)</span><span class="sxs-lookup"><span data-stu-id="b0965-106">ret texCUBE(s, t)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="b0965-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0965-107">Parameters</span></span>



| <span data-ttu-id="b0965-108">Élément</span><span class="sxs-lookup"><span data-stu-id="b0965-108">Item</span></span>                                                   | <span data-ttu-id="b0965-109">Description</span><span class="sxs-lookup"><span data-stu-id="b0965-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b0965-110"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b0965-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="b0965-111">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="b0965-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="b0965-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="b0965-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="b0965-113">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="b0965-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b0965-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b0965-114">Return Value</span></span>

<span data-ttu-id="b0965-115">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="b0965-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="b0965-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="b0965-116">Type Description</span></span>



| <span data-ttu-id="b0965-117">Nom</span><span class="sxs-lookup"><span data-stu-id="b0965-117">Name</span></span> | <span data-ttu-id="b0965-118">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="b0965-118">In/Out</span></span> | [<span data-ttu-id="b0965-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="b0965-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="b0965-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="b0965-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b0965-121">Taille</span><span class="sxs-lookup"><span data-stu-id="b0965-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="b0965-122">s</span><span class="sxs-lookup"><span data-stu-id="b0965-122">s</span></span>    | <span data-ttu-id="b0965-123">in</span><span class="sxs-lookup"><span data-stu-id="b0965-123">in</span></span>     | [<span data-ttu-id="b0965-124">**object**</span><span class="sxs-lookup"><span data-stu-id="b0965-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b0965-125">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="b0965-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="b0965-126">1</span><span class="sxs-lookup"><span data-stu-id="b0965-126">1</span></span>    |
| <span data-ttu-id="b0965-127">t</span><span class="sxs-lookup"><span data-stu-id="b0965-127">t</span></span>    | <span data-ttu-id="b0965-128">in</span><span class="sxs-lookup"><span data-stu-id="b0965-128">in</span></span>     | [<span data-ttu-id="b0965-129">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="b0965-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b0965-130">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b0965-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b0965-131">3</span><span class="sxs-lookup"><span data-stu-id="b0965-131">3</span></span>    |
| <span data-ttu-id="b0965-132">Av</span><span class="sxs-lookup"><span data-stu-id="b0965-132">ret</span></span>  | <span data-ttu-id="b0965-133">out</span><span class="sxs-lookup"><span data-stu-id="b0965-133">out</span></span>    | [<span data-ttu-id="b0965-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="b0965-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b0965-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b0965-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b0965-136">4</span><span class="sxs-lookup"><span data-stu-id="b0965-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b0965-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b0965-137">Minimum Shader Model</span></span>

<span data-ttu-id="b0965-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b0965-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b0965-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b0965-139">Shader Model</span></span>                                              | <span data-ttu-id="b0965-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b0965-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="b0965-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="b0965-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b0965-142">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="b0965-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="b0965-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0965-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b0965-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="b0965-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="b0965-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0965-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b0965-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="b0965-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="b0965-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0965-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b0965-148">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="b0965-148">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b0965-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0965-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0965-150">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b0965-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

