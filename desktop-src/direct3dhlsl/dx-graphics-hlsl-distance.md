---
title: distance
description: Retourne une distance scalaire entre deux vecteurs.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- HLSL à distance
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315587"
---
# <a name="distance"></a><span data-ttu-id="b2ece-104">distance</span><span class="sxs-lookup"><span data-stu-id="b2ece-104">distance</span></span>

<span data-ttu-id="b2ece-105">Retourne une distance scalaire entre deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="b2ece-105">Returns a distance scalar between two vectors.</span></span>



| <span data-ttu-id="b2ece-106">distance *RET* (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="b2ece-106">*ret* distance(*x*, *y*)</span></span> |
|--------------------------|



 

## <a name="parameters"></a><span data-ttu-id="b2ece-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2ece-107">Parameters</span></span>



| <span data-ttu-id="b2ece-108">Élément</span><span class="sxs-lookup"><span data-stu-id="b2ece-108">Item</span></span>                                                   | <span data-ttu-id="b2ece-109">Description</span><span class="sxs-lookup"><span data-stu-id="b2ece-109">Description</span></span>                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b2ece-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b2ece-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b2ece-111">\[dans \] le premier vecteur à virgule flottante à comparer.</span><span class="sxs-lookup"><span data-stu-id="b2ece-111">\[in\] The first floating-point vector to compare.</span></span><br/>  |
| <span data-ttu-id="b2ece-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="b2ece-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="b2ece-113">\[dans \] le deuxième vecteur à virgule flottante à comparer.</span><span class="sxs-lookup"><span data-stu-id="b2ece-113">\[in\] The second floating-point vector to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b2ece-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b2ece-114">Return Value</span></span>

<span data-ttu-id="b2ece-115">Valeur scalaire à virgule flottante qui représente la distance entre le paramètre *x* et le paramètre *y* .</span><span class="sxs-lookup"><span data-stu-id="b2ece-115">A floating-point, scalar value that represents the distance between the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="b2ece-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="b2ece-116">Type Description</span></span>



| <span data-ttu-id="b2ece-117">Nom</span><span class="sxs-lookup"><span data-stu-id="b2ece-117">Name</span></span>  | [<span data-ttu-id="b2ece-118">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="b2ece-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="b2ece-119">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="b2ece-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b2ece-120">Taille</span><span class="sxs-lookup"><span data-stu-id="b2ece-120">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b2ece-121">*x*</span><span class="sxs-lookup"><span data-stu-id="b2ece-121">*x*</span></span>   | [<span data-ttu-id="b2ece-122">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="b2ece-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b2ece-123">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b2ece-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b2ece-124">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="b2ece-124">any</span></span>                            |
| <span data-ttu-id="b2ece-125">*y*</span><span class="sxs-lookup"><span data-stu-id="b2ece-125">*y*</span></span>   | [<span data-ttu-id="b2ece-126">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="b2ece-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b2ece-127">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b2ece-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b2ece-128">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b2ece-128">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="b2ece-129">*Av*</span><span class="sxs-lookup"><span data-stu-id="b2ece-129">*ret*</span></span> | [<span data-ttu-id="b2ece-130">**scalaire**</span><span class="sxs-lookup"><span data-stu-id="b2ece-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b2ece-131">**float**</span><span class="sxs-lookup"><span data-stu-id="b2ece-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b2ece-132">1</span><span class="sxs-lookup"><span data-stu-id="b2ece-132">1</span></span>                              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b2ece-133">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b2ece-133">Minimum Shader Model</span></span>

<span data-ttu-id="b2ece-134">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b2ece-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b2ece-135">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b2ece-135">Shader Model</span></span>                                                                       | <span data-ttu-id="b2ece-136">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b2ece-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b2ece-137">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="b2ece-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b2ece-138">Oui</span><span class="sxs-lookup"><span data-stu-id="b2ece-138">yes</span></span>       |
| [<span data-ttu-id="b2ece-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b2ece-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b2ece-140">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b2ece-140">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="b2ece-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2ece-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2ece-142">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b2ece-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

