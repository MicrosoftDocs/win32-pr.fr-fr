---
title: lerp
description: Effectue une interpolation linéaire.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- HLSL Lerp
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7a5251aaf410d7224b87b9ee9a8f0e8a0c947e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990940"
---
# <a name="lerp"></a><span data-ttu-id="24c03-104">lerp</span><span class="sxs-lookup"><span data-stu-id="24c03-104">lerp</span></span>

<span data-ttu-id="24c03-105">Effectue une interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="24c03-105">Performs a linear interpolation.</span></span>



| <span data-ttu-id="24c03-106">*RET* Lerp (*x*, *y*, *s*)</span><span class="sxs-lookup"><span data-stu-id="24c03-106">*ret* lerp(*x*, *y*, *s*)</span></span> |
|---------------------------|



 

## <a name="parameters"></a><span data-ttu-id="24c03-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24c03-107">Parameters</span></span>



| <span data-ttu-id="24c03-108">Élément</span><span class="sxs-lookup"><span data-stu-id="24c03-108">Item</span></span>                                                   | <span data-ttu-id="24c03-109">Description</span><span class="sxs-lookup"><span data-stu-id="24c03-109">Description</span></span>                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c03-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="24c03-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="24c03-111">\[dans \] la première valeur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="24c03-111">\[in\] The first-floating point value.</span></span><br/>                                                     |
| <span data-ttu-id="24c03-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="24c03-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="24c03-113">\[dans \] la deuxième valeur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="24c03-113">\[in\] The second-floating point value.</span></span><br/>                                                    |
| <span data-ttu-id="24c03-114"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="24c03-114"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="24c03-115">\[dans \] une valeur qui interpole de manière linéaire entre le paramètre *x* et le paramètre *y* .</span><span class="sxs-lookup"><span data-stu-id="24c03-115">\[in\] A value that linearly interpolates between the *x* parameter and the *y* parameter.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="24c03-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="24c03-116">Return Value</span></span>

<span data-ttu-id="24c03-117">Résultat de l’interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="24c03-117">The result of the linear interpolation.</span></span>

## <a name="type-description"></a><span data-ttu-id="24c03-118">Description du type</span><span class="sxs-lookup"><span data-stu-id="24c03-118">Type Description</span></span>



| <span data-ttu-id="24c03-119">Nom</span><span class="sxs-lookup"><span data-stu-id="24c03-119">Name</span></span>  | [<span data-ttu-id="24c03-120">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="24c03-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="24c03-121">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="24c03-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="24c03-122">Taille</span><span class="sxs-lookup"><span data-stu-id="24c03-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="24c03-123">*x*</span><span class="sxs-lookup"><span data-stu-id="24c03-123">*x*</span></span>   | <span data-ttu-id="24c03-124">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="24c03-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="24c03-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="24c03-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="24c03-126">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="24c03-126">any</span></span>                            |
| <span data-ttu-id="24c03-127">*y*</span><span class="sxs-lookup"><span data-stu-id="24c03-127">*y*</span></span>   | <span data-ttu-id="24c03-128">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="24c03-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="24c03-129">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="24c03-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="24c03-130">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="24c03-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="24c03-131">*s*</span><span class="sxs-lookup"><span data-stu-id="24c03-131">*s*</span></span>   | <span data-ttu-id="24c03-132">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="24c03-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="24c03-133">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="24c03-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="24c03-134">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="24c03-134">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="24c03-135">*Av*</span><span class="sxs-lookup"><span data-stu-id="24c03-135">*ret*</span></span> | <span data-ttu-id="24c03-136">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="24c03-136">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="24c03-137">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="24c03-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="24c03-138">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="24c03-138">same dimension(s) as input *x*</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="24c03-139">Notes</span><span class="sxs-lookup"><span data-stu-id="24c03-139">Remarks</span></span>

<span data-ttu-id="24c03-140">L’interpolation linéaire est basée sur la formule suivante : x \* (1-s) + y \* s qui peut être écrit de façon équivalente sous la forme x + s (y-x).</span><span class="sxs-lookup"><span data-stu-id="24c03-140">Linear interpolation is based on the following formula: x\*(1-s) + y\*s which can equivalently be written as x + s(y-x).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="24c03-141">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="24c03-141">Minimum Shader Model</span></span>

<span data-ttu-id="24c03-142">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="24c03-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="24c03-143">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="24c03-143">Shader Model</span></span>                                                                       | <span data-ttu-id="24c03-144">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="24c03-144">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="24c03-145">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="24c03-145">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="24c03-146">Oui</span><span class="sxs-lookup"><span data-stu-id="24c03-146">yes</span></span>                         |
| [<span data-ttu-id="24c03-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="24c03-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="24c03-148">Oui (vs \_ 1 1 \_ et PS \_ 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="24c03-148">yes (vs\_1\_1 and ps\_1\_1)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="24c03-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24c03-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c03-150">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="24c03-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

