---
title: tex2Dproj
description: Échantillonne une texture 2D à l’aide d’une division projective ; la coordonnée de texture est divisée par t. w avant que la recherche ait lieu.
ms.assetid: c6b79360-3737-4b74-bdf3-6d46323e8e54
keywords:
- HLSL tex2Dproj
topic_type:
- apiref
api_name:
- tex2Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 365401e4e4eca8703207ffb5c7676748f4a06d30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507966"
---
# <a name="tex2dproj"></a><span data-ttu-id="04728-104">tex2Dproj</span><span class="sxs-lookup"><span data-stu-id="04728-104">tex2Dproj</span></span>

<span data-ttu-id="04728-105">Échantillonne une texture 2D à l’aide d’une division projective ; la coordonnée de texture est divisée par t. w avant que la recherche ait lieu.</span><span class="sxs-lookup"><span data-stu-id="04728-105">Samples a 2D texture using a projective divide; the texture coordinate is divided by t.w before the lookup takes place.</span></span>



| <span data-ttu-id="04728-106">RET tex2Dproj (s, t)</span><span class="sxs-lookup"><span data-stu-id="04728-106">ret tex2Dproj(s, t)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="04728-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04728-107">Parameters</span></span>



| <span data-ttu-id="04728-108">Élément</span><span class="sxs-lookup"><span data-stu-id="04728-108">Item</span></span>                                                   | <span data-ttu-id="04728-109">Description</span><span class="sxs-lookup"><span data-stu-id="04728-109">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="04728-110"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="04728-110"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="04728-111">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="04728-111">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="04728-112"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="04728-112"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="04728-113">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="04728-113">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="04728-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04728-114">Return Value</span></span>

<span data-ttu-id="04728-115">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="04728-115">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="04728-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="04728-116">Type Description</span></span>



| <span data-ttu-id="04728-117">Nom</span><span class="sxs-lookup"><span data-stu-id="04728-117">Name</span></span> | <span data-ttu-id="04728-118">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="04728-118">In/Out</span></span> | [<span data-ttu-id="04728-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="04728-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="04728-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="04728-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="04728-121">Taille</span><span class="sxs-lookup"><span data-stu-id="04728-121">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="04728-122">s</span><span class="sxs-lookup"><span data-stu-id="04728-122">s</span></span>    | <span data-ttu-id="04728-123">in</span><span class="sxs-lookup"><span data-stu-id="04728-123">in</span></span>     | [<span data-ttu-id="04728-124">**object**</span><span class="sxs-lookup"><span data-stu-id="04728-124">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="04728-125">sampler2D</span><span class="sxs-lookup"><span data-stu-id="04728-125">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="04728-126">1</span><span class="sxs-lookup"><span data-stu-id="04728-126">1</span></span>    |
| <span data-ttu-id="04728-127">t</span><span class="sxs-lookup"><span data-stu-id="04728-127">t</span></span>    | <span data-ttu-id="04728-128">in</span><span class="sxs-lookup"><span data-stu-id="04728-128">in</span></span>     | [<span data-ttu-id="04728-129">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="04728-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="04728-130">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="04728-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="04728-131">4</span><span class="sxs-lookup"><span data-stu-id="04728-131">4</span></span>    |
| <span data-ttu-id="04728-132">Av</span><span class="sxs-lookup"><span data-stu-id="04728-132">ret</span></span>  | <span data-ttu-id="04728-133">out</span><span class="sxs-lookup"><span data-stu-id="04728-133">out</span></span>    | [<span data-ttu-id="04728-134">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="04728-134">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="04728-135">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="04728-135">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="04728-136">4</span><span class="sxs-lookup"><span data-stu-id="04728-136">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="04728-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="04728-137">Minimum Shader Model</span></span>

<span data-ttu-id="04728-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="04728-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="04728-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="04728-139">Shader Model</span></span>                                              | <span data-ttu-id="04728-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="04728-140">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="04728-141">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="04728-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="04728-142">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="04728-142">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="04728-143">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04728-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="04728-144">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="04728-144">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="04728-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04728-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="04728-146">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="04728-146">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="04728-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="04728-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="04728-148">non</span><span class="sxs-lookup"><span data-stu-id="04728-148">no</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="04728-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04728-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04728-150">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="04728-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

