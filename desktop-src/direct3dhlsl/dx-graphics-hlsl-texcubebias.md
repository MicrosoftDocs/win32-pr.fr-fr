---
title: texCUBEbias
description: Échantillonne une texture de cube après avoir biaisé le niveau MIP par t.w.
ms.assetid: dad27cff-6b10-45db-b70f-c4ad78c64e76
keywords:
- HLSL texCUBEbias
topic_type:
- apiref
api_name:
- texCUBEbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0129c20db1da320e9cb85aacfc4490124be28f8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101724"
---
# <a name="texcubebias"></a><span data-ttu-id="6a292-104">texCUBEbias</span><span class="sxs-lookup"><span data-stu-id="6a292-104">texCUBEbias</span></span>

<span data-ttu-id="6a292-105">Échantillonne une texture de cube après avoir biaisé le niveau MIP par t.w.</span><span class="sxs-lookup"><span data-stu-id="6a292-105">Samples a cube texture after biasing the mip level by t.w.</span></span>



| <span data-ttu-id="6a292-106">RET texCUBEbias (s, t)</span><span class="sxs-lookup"><span data-stu-id="6a292-106">ret texCUBEbias(s, t)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="6a292-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a292-107">Parameters</span></span>



| <span data-ttu-id="6a292-108">Élément</span><span class="sxs-lookup"><span data-stu-id="6a292-108">Item</span></span>                                                   | <span data-ttu-id="6a292-109">Description</span><span class="sxs-lookup"><span data-stu-id="6a292-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="6a292-110"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="6a292-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="6a292-111">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="6a292-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="6a292-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="6a292-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="6a292-113">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="6a292-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="6a292-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a292-114">Return Value</span></span>

<span data-ttu-id="6a292-115">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="6a292-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="6a292-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="6a292-116">Type Description</span></span>



| <span data-ttu-id="6a292-117">Nom</span><span class="sxs-lookup"><span data-stu-id="6a292-117">Name</span></span> | <span data-ttu-id="6a292-118">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="6a292-118">In/Out</span></span> | [<span data-ttu-id="6a292-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="6a292-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="6a292-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="6a292-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="6a292-121">Taille</span><span class="sxs-lookup"><span data-stu-id="6a292-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="6a292-122">s</span><span class="sxs-lookup"><span data-stu-id="6a292-122">s</span></span>    | <span data-ttu-id="6a292-123">in</span><span class="sxs-lookup"><span data-stu-id="6a292-123">in</span></span>     | [<span data-ttu-id="6a292-124">**object**</span><span class="sxs-lookup"><span data-stu-id="6a292-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6a292-125">samplerCUBE</span><span class="sxs-lookup"><span data-stu-id="6a292-125">samplerCUBE</span></span>](dx-graphics-hlsl-sampler.md)                    | <span data-ttu-id="6a292-126">1</span><span class="sxs-lookup"><span data-stu-id="6a292-126">1</span></span>    |
| <span data-ttu-id="6a292-127">t</span><span class="sxs-lookup"><span data-stu-id="6a292-127">t</span></span>    | <span data-ttu-id="6a292-128">in</span><span class="sxs-lookup"><span data-stu-id="6a292-128">in</span></span>     | [<span data-ttu-id="6a292-129">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="6a292-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6a292-130">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="6a292-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6a292-131">4</span><span class="sxs-lookup"><span data-stu-id="6a292-131">4</span></span>    |
| <span data-ttu-id="6a292-132">Av</span><span class="sxs-lookup"><span data-stu-id="6a292-132">ret</span></span>  | <span data-ttu-id="6a292-133">out</span><span class="sxs-lookup"><span data-stu-id="6a292-133">out</span></span>    | [<span data-ttu-id="6a292-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="6a292-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="6a292-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="6a292-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="6a292-136">4</span><span class="sxs-lookup"><span data-stu-id="6a292-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6a292-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="6a292-137">Minimum Shader Model</span></span>

<span data-ttu-id="6a292-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="6a292-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6a292-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6a292-139">Shader Model</span></span>                                              | <span data-ttu-id="6a292-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="6a292-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="6a292-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="6a292-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6a292-142">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="6a292-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="6a292-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a292-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6a292-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="6a292-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="6a292-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a292-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6a292-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="6a292-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="6a292-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a292-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6a292-148">non</span><span class="sxs-lookup"><span data-stu-id="6a292-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="6a292-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a292-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a292-150">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="6a292-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

