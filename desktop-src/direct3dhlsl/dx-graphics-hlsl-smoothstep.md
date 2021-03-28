---
title: smoothstep
description: Retourne une interpolation Smooth Hermite entre 0 et 1, si x est dans la plage \ min, Max \.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- HLSL SmoothStep
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971707"
---
# <a name="smoothstep"></a><span data-ttu-id="88dcd-104">smoothstep</span><span class="sxs-lookup"><span data-stu-id="88dcd-104">smoothstep</span></span>

<span data-ttu-id="88dcd-105">Retourne une interpolation Smooth Hermite entre 0 et 1, si *x* est dans la plage \[ *min*, *Max* \] .</span><span class="sxs-lookup"><span data-stu-id="88dcd-105">Returns a smooth Hermite interpolation between 0 and 1, if *x* is in the range \[*min*, *max*\].</span></span>



| <span data-ttu-id="88dcd-106">*RET* SmoothStep (*min*, *Max*, *x*)</span><span class="sxs-lookup"><span data-stu-id="88dcd-106">*ret* smoothstep(*min*, *max*, *x*)</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="88dcd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88dcd-107">Parameters</span></span>



| <span data-ttu-id="88dcd-108">Élément</span><span class="sxs-lookup"><span data-stu-id="88dcd-108">Item</span></span>                                                         | <span data-ttu-id="88dcd-109">Description</span><span class="sxs-lookup"><span data-stu-id="88dcd-109">Description</span></span>                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="88dcd-110"><span id="min"></span><span id="MIN"></span>*min*</span><span class="sxs-lookup"><span data-stu-id="88dcd-110"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="88dcd-111">\[dans \] la plage minimale du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="88dcd-111">\[in\] The minimum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="88dcd-112"><span id="max"></span><span id="MAX"></span>*Max*</span><span class="sxs-lookup"><span data-stu-id="88dcd-112"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="88dcd-113">\[dans \] la plage maximale du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="88dcd-113">\[in\] The maximum range of the *x* parameter.</span></span><br/> |
| <span data-ttu-id="88dcd-114"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="88dcd-114"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="88dcd-115">\[dans \] la valeur spécifiée à interpoler.</span><span class="sxs-lookup"><span data-stu-id="88dcd-115">\[in\] The specified value to be interpolated.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="88dcd-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="88dcd-116">Return Value</span></span>

<span data-ttu-id="88dcd-117">Retourne 0 si *x* est inférieur à *min*; 1 si *x* est supérieur à *Max*; Sinon, une valeur comprise entre 0 et 1 si *x* est comprise dans la plage \[ *min*, *Max* \] .</span><span class="sxs-lookup"><span data-stu-id="88dcd-117">Returns 0 if *x* is less than *min*; 1 if *x* is greater than *max*; otherwise, a value between 0 and 1 if *x* is in the range \[*min*, *max*\].</span></span>

## <a name="remarks"></a><span data-ttu-id="88dcd-118">Notes</span><span class="sxs-lookup"><span data-stu-id="88dcd-118">Remarks</span></span>

<span data-ttu-id="88dcd-119">Utilisez la fonction intrinsèque **SmoothStep** HLSL pour créer une transition lisse entre deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="88dcd-119">Use the **smoothstep** HLSL intrinsic function to create a smooth transition between two values.</span></span> <span data-ttu-id="88dcd-120">Par exemple, vous pouvez utiliser cette fonction pour fusionner deux couleurs en douceur.</span><span class="sxs-lookup"><span data-stu-id="88dcd-120">For example, you can use this function to blend two colors smoothly.</span></span>

## <a name="type-description"></a><span data-ttu-id="88dcd-121">Description du type</span><span class="sxs-lookup"><span data-stu-id="88dcd-121">Type Description</span></span>



| <span data-ttu-id="88dcd-122">Nom</span><span class="sxs-lookup"><span data-stu-id="88dcd-122">Name</span></span>  | [<span data-ttu-id="88dcd-123">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="88dcd-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="88dcd-124">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="88dcd-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="88dcd-125">Taille</span><span class="sxs-lookup"><span data-stu-id="88dcd-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="88dcd-126">*x*</span><span class="sxs-lookup"><span data-stu-id="88dcd-126">*x*</span></span>   | <span data-ttu-id="88dcd-127">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="88dcd-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="88dcd-128">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="88dcd-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="88dcd-129">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="88dcd-129">any</span></span>                            |
| <span data-ttu-id="88dcd-130">*min*</span><span class="sxs-lookup"><span data-stu-id="88dcd-130">*min*</span></span> | <span data-ttu-id="88dcd-131">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="88dcd-131">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="88dcd-132">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="88dcd-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="88dcd-133">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="88dcd-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="88dcd-134">*max*</span><span class="sxs-lookup"><span data-stu-id="88dcd-134">*max*</span></span> | <span data-ttu-id="88dcd-135">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="88dcd-135">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="88dcd-136">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="88dcd-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="88dcd-137">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="88dcd-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="88dcd-138">*Av*</span><span class="sxs-lookup"><span data-stu-id="88dcd-138">*ret*</span></span> | <span data-ttu-id="88dcd-139">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="88dcd-139">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="88dcd-140">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="88dcd-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="88dcd-141">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="88dcd-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="88dcd-142">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="88dcd-142">Minimum Shader Model</span></span>

<span data-ttu-id="88dcd-143">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="88dcd-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="88dcd-144">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="88dcd-144">Shader Model</span></span>                                                                       | <span data-ttu-id="88dcd-145">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="88dcd-145">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="88dcd-146">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="88dcd-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="88dcd-147">Oui</span><span class="sxs-lookup"><span data-stu-id="88dcd-147">yes</span></span>                 |
| [<span data-ttu-id="88dcd-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="88dcd-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="88dcd-149">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="88dcd-149">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="88dcd-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88dcd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88dcd-151">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="88dcd-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

