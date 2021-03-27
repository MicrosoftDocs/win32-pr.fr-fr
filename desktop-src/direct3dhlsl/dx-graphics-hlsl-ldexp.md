---
title: ldexp (Corecrt \_ Math. h)
description: Retourne le résultat de la multiplication de la valeur spécifiée par deux, élevé à la puissance de l’exposant spécifié.
ms.assetid: 6d6fee96-f952-4058-a1ac-3abb98dbd540
keywords:
- HLSL ldexp
topic_type:
- apiref
api_name:
- ldexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731cb5cbf933ea3f8754a7d70b9ef0b7a54e783b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870138"
---
# <a name="ldexp"></a><span data-ttu-id="42927-104">ldexp</span><span class="sxs-lookup"><span data-stu-id="42927-104">ldexp</span></span>

<span data-ttu-id="42927-105">Retourne le résultat de la multiplication de la valeur spécifiée par deux, élevé à la puissance de l’exposant spécifié.</span><span class="sxs-lookup"><span data-stu-id="42927-105">Returns the result of multiplying the specified value by two, raised to the power of the specified exponent.</span></span>



| <span data-ttu-id="42927-106">*RET* ldexp (*x*, *exp*)</span><span class="sxs-lookup"><span data-stu-id="42927-106">*ret* ldexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="42927-107">Cette fonction utilise la formule suivante : *x* \* 2 <sup>exp</sup></span><span class="sxs-lookup"><span data-stu-id="42927-107">This function uses the following formula: *x* \* 2<sup>exp</sup></span></span>

## <a name="parameters"></a><span data-ttu-id="42927-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42927-108">Parameters</span></span>



| <span data-ttu-id="42927-109">Élément</span><span class="sxs-lookup"><span data-stu-id="42927-109">Item</span></span>                                                         | <span data-ttu-id="42927-110">Description</span><span class="sxs-lookup"><span data-stu-id="42927-110">Description</span></span>                               |
|--------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="42927-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="42927-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="42927-112">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="42927-112">\[in\] The specified value.</span></span><br/>    |
| <span data-ttu-id="42927-113"><span id="exp"></span><span id="EXP"></span>*venir*</span><span class="sxs-lookup"><span data-stu-id="42927-113"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="42927-114">\[dans \] l’exposant spécifié.</span><span class="sxs-lookup"><span data-stu-id="42927-114">\[in\] The specified exponent.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="42927-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="42927-115">Return Value</span></span>

<span data-ttu-id="42927-116">Résultat de la multiplication du paramètre *x* par deux, élevé à la puissance du paramètre *exp* .</span><span class="sxs-lookup"><span data-stu-id="42927-116">The result of multiplying the *x* parameter by two, raised to the power of the *exp* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="42927-117">Description du type</span><span class="sxs-lookup"><span data-stu-id="42927-117">Type Description</span></span>



| <span data-ttu-id="42927-118">Nom</span><span class="sxs-lookup"><span data-stu-id="42927-118">Name</span></span>  | [<span data-ttu-id="42927-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="42927-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="42927-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="42927-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="42927-121">Taille</span><span class="sxs-lookup"><span data-stu-id="42927-121">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="42927-122">*x*</span><span class="sxs-lookup"><span data-stu-id="42927-122">*x*</span></span>   | <span data-ttu-id="42927-123">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="42927-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="42927-124">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="42927-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="42927-125">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="42927-125">any</span></span>                            |
| <span data-ttu-id="42927-126">*exp*</span><span class="sxs-lookup"><span data-stu-id="42927-126">*exp*</span></span> | <span data-ttu-id="42927-127">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="42927-127">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="42927-128">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="42927-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="42927-129">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="42927-129">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="42927-130">*Av*</span><span class="sxs-lookup"><span data-stu-id="42927-130">*ret*</span></span> | <span data-ttu-id="42927-131">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="42927-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="42927-132">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="42927-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="42927-133">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="42927-133">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="42927-134">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="42927-134">Minimum Shader Model</span></span>

<span data-ttu-id="42927-135">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="42927-135">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="42927-136">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="42927-136">Shader Model</span></span>                                                                       | <span data-ttu-id="42927-137">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="42927-137">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="42927-138">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="42927-138">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="42927-139">Oui</span><span class="sxs-lookup"><span data-stu-id="42927-139">yes</span></span>                 |
| [<span data-ttu-id="42927-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42927-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="42927-141">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="42927-141">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="42927-142">Spécifications</span><span class="sxs-lookup"><span data-stu-id="42927-142">Requirements</span></span>



| <span data-ttu-id="42927-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42927-143">Requirement</span></span> | <span data-ttu-id="42927-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="42927-144">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="42927-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="42927-145">Header</span></span><br/> | <dl> <span data-ttu-id="42927-146"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="42927-146"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42927-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42927-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42927-148">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="42927-148">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

