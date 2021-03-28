---
title: pow
description: Retourne la valeur spécifiée élevée à la puissance spécifiée.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- en HLSL pow
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f190c374b6c0ac42d41862eb918f0c0482b6d785
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463634"
---
# <a name="pow"></a><span data-ttu-id="b9d82-104">pow</span><span class="sxs-lookup"><span data-stu-id="b9d82-104">pow</span></span>

<span data-ttu-id="b9d82-105">Retourne la valeur spécifiée élevée à la puissance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b9d82-105">Returns the specified value raised to the specified power.</span></span>



| <span data-ttu-id="b9d82-106">*RET* Pow (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="b9d82-106">*ret* pow(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="b9d82-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9d82-107">Parameters</span></span>



| <span data-ttu-id="b9d82-108">Élément</span><span class="sxs-lookup"><span data-stu-id="b9d82-108">Item</span></span>                                                   | <span data-ttu-id="b9d82-109">Description</span><span class="sxs-lookup"><span data-stu-id="b9d82-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="b9d82-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b9d82-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="b9d82-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b9d82-111">\[in\] The specified value.</span></span><br/> |
| <span data-ttu-id="b9d82-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="b9d82-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="b9d82-113">\[dans \] la puissance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b9d82-113">\[in\] The specified power.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b9d82-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b9d82-114">Return Value</span></span>

<span data-ttu-id="b9d82-115">Le paramètre *x* élevé à la puissance du paramètre *y* .</span><span class="sxs-lookup"><span data-stu-id="b9d82-115">The *x* parameter raised to the power of the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9d82-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b9d82-116">Remarks</span></span>

<span data-ttu-id="b9d82-117">La fonction intrinsèque Pow du langage **Pow** calcule *x*<sup>y</sup>.</span><span class="sxs-lookup"><span data-stu-id="b9d82-117">The **pow** HLSL intrinsic function calculates *x*<sup>y</sup>.</span></span>



| <span data-ttu-id="b9d82-118">X</span><span class="sxs-lookup"><span data-stu-id="b9d82-118">X</span></span>      | <span data-ttu-id="b9d82-119">Y</span><span class="sxs-lookup"><span data-stu-id="b9d82-119">Y</span></span>      | <span data-ttu-id="b9d82-120">Résultat</span><span class="sxs-lookup"><span data-stu-id="b9d82-120">Result</span></span>                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b9d82-121">< 0</span><span class="sxs-lookup"><span data-stu-id="b9d82-121">< 0</span></span> | <span data-ttu-id="b9d82-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="b9d82-122">any</span></span>    | <span data-ttu-id="b9d82-123">NAN</span><span class="sxs-lookup"><span data-stu-id="b9d82-123">NAN</span></span>                                                                         |
| <span data-ttu-id="b9d82-124">> 0</span><span class="sxs-lookup"><span data-stu-id="b9d82-124">> 0</span></span> | <span data-ttu-id="b9d82-125">= = 0</span><span class="sxs-lookup"><span data-stu-id="b9d82-125">== 0</span></span>   | <span data-ttu-id="b9d82-126">1</span><span class="sxs-lookup"><span data-stu-id="b9d82-126">1</span></span>                                                                           |
| <span data-ttu-id="b9d82-127">= = 0</span><span class="sxs-lookup"><span data-stu-id="b9d82-127">== 0</span></span>   | <span data-ttu-id="b9d82-128">> 0</span><span class="sxs-lookup"><span data-stu-id="b9d82-128">> 0</span></span> | <span data-ttu-id="b9d82-129">0</span><span class="sxs-lookup"><span data-stu-id="b9d82-129">0</span></span>                                                                           |
| <span data-ttu-id="b9d82-130">= = 0</span><span class="sxs-lookup"><span data-stu-id="b9d82-130">== 0</span></span>   | <span data-ttu-id="b9d82-131">< 0</span><span class="sxs-lookup"><span data-stu-id="b9d82-131">< 0</span></span> | <span data-ttu-id="b9d82-132">fichier</span><span class="sxs-lookup"><span data-stu-id="b9d82-132">inf</span></span>                                                                         |
| <span data-ttu-id="b9d82-133">> 0</span><span class="sxs-lookup"><span data-stu-id="b9d82-133">> 0</span></span> | <span data-ttu-id="b9d82-134">< 0</span><span class="sxs-lookup"><span data-stu-id="b9d82-134">< 0</span></span> | <span data-ttu-id="b9d82-135">1/X<sup>-Y</sup></span><span class="sxs-lookup"><span data-stu-id="b9d82-135">1/X<sup>-Y</sup></span></span>                                                            |
| <span data-ttu-id="b9d82-136">= = 0</span><span class="sxs-lookup"><span data-stu-id="b9d82-136">== 0</span></span>   | <span data-ttu-id="b9d82-137">= = 0</span><span class="sxs-lookup"><span data-stu-id="b9d82-137">== 0</span></span>   | <span data-ttu-id="b9d82-138">Dépend du processeur graphique</span><span class="sxs-lookup"><span data-stu-id="b9d82-138">Depends on the particular graphics processor</span></span><br/> <span data-ttu-id="b9d82-139">0, ou 1 ou NAN</span><span class="sxs-lookup"><span data-stu-id="b9d82-139">0, or 1, or NAN</span></span><br/> |



 

## <a name="type-description"></a><span data-ttu-id="b9d82-140">Description du type</span><span class="sxs-lookup"><span data-stu-id="b9d82-140">Type Description</span></span>



| <span data-ttu-id="b9d82-141">Nom</span><span class="sxs-lookup"><span data-stu-id="b9d82-141">Name</span></span>  | [<span data-ttu-id="b9d82-142">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="b9d82-142">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b9d82-143">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="b9d82-143">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b9d82-144">Taille</span><span class="sxs-lookup"><span data-stu-id="b9d82-144">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b9d82-145">*x*</span><span class="sxs-lookup"><span data-stu-id="b9d82-145">*x*</span></span>   | <span data-ttu-id="b9d82-146">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="b9d82-146">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="b9d82-147">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b9d82-147">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b9d82-148">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="b9d82-148">any</span></span>                            |
| <span data-ttu-id="b9d82-149">*y*</span><span class="sxs-lookup"><span data-stu-id="b9d82-149">*y*</span></span>   | <span data-ttu-id="b9d82-150">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b9d82-150">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b9d82-151">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b9d82-151">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b9d82-152">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b9d82-152">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="b9d82-153">*Av*</span><span class="sxs-lookup"><span data-stu-id="b9d82-153">*ret*</span></span> | <span data-ttu-id="b9d82-154">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b9d82-154">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="b9d82-155">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b9d82-155">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b9d82-156">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b9d82-156">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b9d82-157">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b9d82-157">Minimum Shader Model</span></span>

<span data-ttu-id="b9d82-158">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b9d82-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b9d82-159">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b9d82-159">Shader Model</span></span>                                                                       | <span data-ttu-id="b9d82-160">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b9d82-160">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="b9d82-161">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="b9d82-161">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b9d82-162">Oui</span><span class="sxs-lookup"><span data-stu-id="b9d82-162">yes</span></span>                 |
| [<span data-ttu-id="b9d82-163">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b9d82-163">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b9d82-164">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="b9d82-164">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b9d82-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9d82-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d82-166">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b9d82-166">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

