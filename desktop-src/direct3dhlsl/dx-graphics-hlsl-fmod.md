---
title: fmod (Corecrt \_ Math. h)
description: Retourne le reste à virgule flottante de x/y.
ms.assetid: bb940548-c4c5-4109-a488-4ea7295c7213
keywords:
- HLSL fmod
topic_type:
- apiref
api_name:
- fmod
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dc4367e3aa80484098e88926567953fc8e9a90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322873"
---
# <a name="fmod"></a><span data-ttu-id="d205f-104">fmod</span><span class="sxs-lookup"><span data-stu-id="d205f-104">fmod</span></span>

<span data-ttu-id="d205f-105">Retourne le reste à virgule flottante de x/y.</span><span class="sxs-lookup"><span data-stu-id="d205f-105">Returns the floating-point remainder of x/y.</span></span>



| <span data-ttu-id="d205f-106">*RET* fmod (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="d205f-106">*ret* fmod(*x*, *y*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="d205f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d205f-107">Parameters</span></span>



| <span data-ttu-id="d205f-108">Élément</span><span class="sxs-lookup"><span data-stu-id="d205f-108">Item</span></span>                                                   | <span data-ttu-id="d205f-109">Description</span><span class="sxs-lookup"><span data-stu-id="d205f-109">Description</span></span>                                    |
|--------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="d205f-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d205f-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d205f-111">\[dans \] le dividende à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d205f-111">\[in\] The floating-point dividend.</span></span><br/> |
| <span data-ttu-id="d205f-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="d205f-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="d205f-113">\[dans \] le diviseur à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d205f-113">\[in\] The floating-point divisor.</span></span><br/>  |



 

## <a name="return-value"></a><span data-ttu-id="d205f-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d205f-114">Return Value</span></span>

<span data-ttu-id="d205f-115">Reste à virgule flottante du paramètre *x* divisé par le paramètre *y* .</span><span class="sxs-lookup"><span data-stu-id="d205f-115">The floating-point remainder of the *x* parameter divided by the *y* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="d205f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d205f-116">Remarks</span></span>

<span data-ttu-id="d205f-117">Le reste à virgule flottante est calculé de telle sorte que x = i \* y + f, où i est un entier, f a le même signe que x, et la valeur absolue de f est inférieure à la valeur absolue de y.</span><span class="sxs-lookup"><span data-stu-id="d205f-117">The floating-point remainder is calculated such that x = i \* y + f, where i is an integer, f has the same sign as x, and the absolute value of f is less than the absolute value of y.</span></span>

## <a name="type-description"></a><span data-ttu-id="d205f-118">Description du type</span><span class="sxs-lookup"><span data-stu-id="d205f-118">Type Description</span></span>



| <span data-ttu-id="d205f-119">Nom</span><span class="sxs-lookup"><span data-stu-id="d205f-119">Name</span></span>  | [<span data-ttu-id="d205f-120">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="d205f-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d205f-121">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="d205f-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d205f-122">Taille</span><span class="sxs-lookup"><span data-stu-id="d205f-122">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d205f-123">*x*</span><span class="sxs-lookup"><span data-stu-id="d205f-123">*x*</span></span>   | <span data-ttu-id="d205f-124">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="d205f-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d205f-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d205f-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d205f-126">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="d205f-126">any</span></span>                            |
| <span data-ttu-id="d205f-127">*y*</span><span class="sxs-lookup"><span data-stu-id="d205f-127">*y*</span></span>   | <span data-ttu-id="d205f-128">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="d205f-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d205f-129">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d205f-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d205f-130">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="d205f-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="d205f-131">*Av*</span><span class="sxs-lookup"><span data-stu-id="d205f-131">*ret*</span></span> | <span data-ttu-id="d205f-132">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="d205f-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d205f-133">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d205f-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d205f-134">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="d205f-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d205f-135">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d205f-135">Minimum Shader Model</span></span>

<span data-ttu-id="d205f-136">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d205f-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d205f-137">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d205f-137">Shader Model</span></span>                                                                       | <span data-ttu-id="d205f-138">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d205f-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d205f-139">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="d205f-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d205f-140">Oui</span><span class="sxs-lookup"><span data-stu-id="d205f-140">yes</span></span>       |
| [<span data-ttu-id="d205f-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d205f-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d205f-142">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d205f-142">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="d205f-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d205f-143">Requirements</span></span>



| <span data-ttu-id="d205f-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d205f-144">Requirement</span></span> | <span data-ttu-id="d205f-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="d205f-145">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d205f-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="d205f-146">Header</span></span><br/> | <dl> <span data-ttu-id="d205f-147"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d205f-147"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d205f-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d205f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d205f-149">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d205f-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

