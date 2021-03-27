---
title: bride
description: Fixe la valeur spécifiée à la plage minimale et maximale spécifiée.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- verrouillage HLSL
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d6b0a3e83c0b1a5e511aba96df03b828b90c11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729541"
---
# <a name="clamp"></a><span data-ttu-id="b00f5-104">bride</span><span class="sxs-lookup"><span data-stu-id="b00f5-104">clamp</span></span>

<span data-ttu-id="b00f5-105">Fixe la valeur spécifiée à la plage minimale et maximale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b00f5-105">Clamps the specified value to the specified minimum and maximum range.</span></span>



| <span data-ttu-id="b00f5-106">*RET* clamp (*x*, *min*, *Max*)</span><span class="sxs-lookup"><span data-stu-id="b00f5-106">*ret* clamp(*x*, *min*, *max*)</span></span> |
|--------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="b00f5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b00f5-107">Parameters</span></span>



| <span data-ttu-id="b00f5-108">Élément</span><span class="sxs-lookup"><span data-stu-id="b00f5-108">Item</span></span>                                                         | <span data-ttu-id="b00f5-109">Description</span><span class="sxs-lookup"><span data-stu-id="b00f5-109">Description</span></span>                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="b00f5-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="b00f5-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>       | <span data-ttu-id="b00f5-111">\[dans \] une valeur à brider.</span><span class="sxs-lookup"><span data-stu-id="b00f5-111">\[in\] A value to clamp.</span></span><br/>            |
| <span data-ttu-id="b00f5-112"><span id="min"></span><span id="MIN"></span>*min*</span><span class="sxs-lookup"><span data-stu-id="b00f5-112"><span id="min"></span><span id="MIN"></span>*min*</span></span><br/> | <span data-ttu-id="b00f5-113">\[dans \] la plage minimale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b00f5-113">\[in\] The specified minimum range.</span></span><br/> |
| <span data-ttu-id="b00f5-114"><span id="max"></span><span id="MAX"></span>*Max*</span><span class="sxs-lookup"><span data-stu-id="b00f5-114"><span id="max"></span><span id="MAX"></span>*max*</span></span><br/> | <span data-ttu-id="b00f5-115">\[dans \] la plage maximale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b00f5-115">\[in\] The specified maximum range.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b00f5-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b00f5-116">Return Value</span></span>

<span data-ttu-id="b00f5-117">Valeur de fixation du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="b00f5-117">The clamped value for the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="b00f5-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b00f5-118">Remarks</span></span>

<span data-ttu-id="b00f5-119">Pour les valeurs de-INF ou INF, la bride se comportera comme prévu.</span><span class="sxs-lookup"><span data-stu-id="b00f5-119">For values of -INF or INF, clamp will behave as expected.</span></span> <span data-ttu-id="b00f5-120">Toutefois, pour les valeurs NaN, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="b00f5-120">However for values of NaN, the results are undefined.</span></span>

## <a name="type-description"></a><span data-ttu-id="b00f5-121">Description du type</span><span class="sxs-lookup"><span data-stu-id="b00f5-121">Type Description</span></span>



| <span data-ttu-id="b00f5-122">Nom</span><span class="sxs-lookup"><span data-stu-id="b00f5-122">Name</span></span>  | [<span data-ttu-id="b00f5-123">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="b00f5-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="b00f5-124">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="b00f5-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="b00f5-125">Taille</span><span class="sxs-lookup"><span data-stu-id="b00f5-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="b00f5-126">*x*</span><span class="sxs-lookup"><span data-stu-id="b00f5-126">*x*</span></span>   | <span data-ttu-id="b00f5-127">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="b00f5-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="b00f5-128">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b00f5-128">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="b00f5-129">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="b00f5-129">any</span></span>                            |
| <span data-ttu-id="b00f5-130">*min*</span><span class="sxs-lookup"><span data-stu-id="b00f5-130">*min*</span></span> | <span data-ttu-id="b00f5-131">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b00f5-131">same as input *x*</span></span>                                                                                              | <span data-ttu-id="b00f5-132">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b00f5-132">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="b00f5-133">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b00f5-133">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="b00f5-134">*max*</span><span class="sxs-lookup"><span data-stu-id="b00f5-134">*max*</span></span> | <span data-ttu-id="b00f5-135">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b00f5-135">same as input *x*</span></span>                                                                                              | <span data-ttu-id="b00f5-136">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b00f5-136">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="b00f5-137">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b00f5-137">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="b00f5-138">*Av*</span><span class="sxs-lookup"><span data-stu-id="b00f5-138">*ret*</span></span> | <span data-ttu-id="b00f5-139">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b00f5-139">same as input *x*</span></span>                                                                                              | <span data-ttu-id="b00f5-140">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b00f5-140">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="b00f5-141">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="b00f5-141">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b00f5-142">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b00f5-142">Minimum Shader Model</span></span>

<span data-ttu-id="b00f5-143">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b00f5-143">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b00f5-144">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b00f5-144">Shader Model</span></span>                                                                       | <span data-ttu-id="b00f5-145">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b00f5-145">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="b00f5-146">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="b00f5-146">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b00f5-147">Oui</span><span class="sxs-lookup"><span data-stu-id="b00f5-147">yes</span></span>                   |
| [<span data-ttu-id="b00f5-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b00f5-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b00f5-149">vs \_ 1 \_ 1 et PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="b00f5-149">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b00f5-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b00f5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b00f5-151">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b00f5-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

