---
title: frexp (Corecrt \_ Math. h)
description: Retourne la mantisse et l’exposant de la valeur à virgule flottante spécifiée.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- HLSL frexp
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953844"
---
# <a name="frexp"></a><span data-ttu-id="b0905-104">frexp</span><span class="sxs-lookup"><span data-stu-id="b0905-104">frexp</span></span>

<span data-ttu-id="b0905-105">Retourne la mantisse et l’exposant de la valeur à virgule flottante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b0905-105">Returns the mantissa and exponent of the specified floating-point value.</span></span>



| <span data-ttu-id="b0905-106">*RET* frexp (*x*, *exp*)</span><span class="sxs-lookup"><span data-stu-id="b0905-106">*ret* frexp(*x*, *exp*)</span></span> |
|-------------------------|



 

<span data-ttu-id="b0905-107">La valeur de retour est la mantisse et la valeur retournée par le paramètre *exp* est l’exposant.</span><span class="sxs-lookup"><span data-stu-id="b0905-107">The return value is the mantissa, and the value returned by *exp* parameter is the exponent.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0905-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0905-108">Parameters</span></span>



| <span data-ttu-id="b0905-109">Élément</span><span class="sxs-lookup"><span data-stu-id="b0905-109">Item</span></span>                                                         | <span data-ttu-id="b0905-110">Description</span><span class="sxs-lookup"><span data-stu-id="b0905-110">Description</span></span>                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0905-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b0905-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="b0905-112">\[dans \] la valeur à virgule flottante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b0905-112">\[in\] The specified floating-point value.</span></span> <span data-ttu-id="b0905-113">Si le paramètre *x* est égal à 0, cette fonction retourne 0 pour la mantisse et l’exposant.</span><span class="sxs-lookup"><span data-stu-id="b0905-113">If the *x* parameter is 0, this function returns 0 for both the mantissa and the exponent.</span></span><br/> |
| <span data-ttu-id="b0905-114"><span id="exp"></span><span id="EXP"></span>*venir*</span><span class="sxs-lookup"><span data-stu-id="b0905-114"><span id="exp"></span><span id="EXP"></span>*exp*</span></span><br/> | <span data-ttu-id="b0905-115">\[sortie \] de l’exposant retourné du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="b0905-115">\[out\] The returned exponent of the *x* parameter.</span></span><br/>                                                                                   |



 

## <a name="return-value"></a><span data-ttu-id="b0905-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b0905-116">Return Value</span></span>

<span data-ttu-id="b0905-117">Mantisse du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="b0905-117">The mantissa of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="b0905-118">Description du type</span><span class="sxs-lookup"><span data-stu-id="b0905-118">Type Description</span></span>



| <span data-ttu-id="b0905-119">Nom</span><span class="sxs-lookup"><span data-stu-id="b0905-119">Name</span></span>  | [<span data-ttu-id="b0905-120">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="b0905-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b0905-121">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="b0905-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b0905-122">Taille</span><span class="sxs-lookup"><span data-stu-id="b0905-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b0905-123">*x*</span><span class="sxs-lookup"><span data-stu-id="b0905-123">*x*</span></span>   | <span data-ttu-id="b0905-124">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="b0905-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b0905-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b0905-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b0905-126">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="b0905-126">any</span></span>                            |
| <span data-ttu-id="b0905-127">*exp*</span><span class="sxs-lookup"><span data-stu-id="b0905-127">*exp*</span></span> | <span data-ttu-id="b0905-128">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b0905-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b0905-129">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b0905-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b0905-130">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b0905-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="b0905-131">*Av*</span><span class="sxs-lookup"><span data-stu-id="b0905-131">*ret*</span></span> | <span data-ttu-id="b0905-132">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b0905-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b0905-133">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b0905-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b0905-134">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b0905-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b0905-135">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b0905-135">Minimum Shader Model</span></span>

<span data-ttu-id="b0905-136">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b0905-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b0905-137">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b0905-137">Shader Model</span></span>                                                                       | <span data-ttu-id="b0905-138">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b0905-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="b0905-139">[Nuancier modèle 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="b0905-139">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="b0905-140">Oui</span><span class="sxs-lookup"><span data-stu-id="b0905-140">yes</span></span>                 |
| [<span data-ttu-id="b0905-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0905-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="b0905-142">Oui (PS \_ 2 \_ x uniquement)</span><span class="sxs-lookup"><span data-stu-id="b0905-142">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="b0905-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b0905-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b0905-144">non</span><span class="sxs-lookup"><span data-stu-id="b0905-144">no</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="b0905-145">Notes</span><span class="sxs-lookup"><span data-stu-id="b0905-145">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b0905-146">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b0905-146">Requirements</span></span>



| <span data-ttu-id="b0905-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0905-147">Requirement</span></span> | <span data-ttu-id="b0905-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0905-148">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0905-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0905-149">Header</span></span><br/> | <dl> <span data-ttu-id="b0905-150"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0905-150"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0905-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0905-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0905-152">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b0905-152">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

