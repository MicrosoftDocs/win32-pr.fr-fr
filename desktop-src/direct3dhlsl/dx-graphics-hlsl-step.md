---
title: étape
description: Compare deux valeurs, en retournant 0 ou 1 en fonction de la valeur la plus élevée.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- étape HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c800e8d8c6f78386139f822f118163f3b431f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729525"
---
# <a name="step"></a><span data-ttu-id="59be2-104">étape</span><span class="sxs-lookup"><span data-stu-id="59be2-104">step</span></span>

<span data-ttu-id="59be2-105">Compare deux valeurs, en retournant 0 ou 1 en fonction de la valeur la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="59be2-105">Compares two values, returning 0 or 1 based on which value is greater.</span></span>



| <span data-ttu-id="59be2-106">*RET* , étape (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="59be2-106">*ret* step(*y*, *x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="59be2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59be2-107">Parameters</span></span>



| <span data-ttu-id="59be2-108">Élément</span><span class="sxs-lookup"><span data-stu-id="59be2-108">Item</span></span>                                                   | <span data-ttu-id="59be2-109">Description</span><span class="sxs-lookup"><span data-stu-id="59be2-109">Description</span></span>                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="59be2-110"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="59be2-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="59be2-111">\[dans \] la première valeur à virgule flottante à comparer.</span><span class="sxs-lookup"><span data-stu-id="59be2-111">\[in\] The first floating-point value to compare.</span></span><br/>  |
| <span data-ttu-id="59be2-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="59be2-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="59be2-113">\[dans \] la deuxième valeur à virgule flottante à comparer.</span><span class="sxs-lookup"><span data-stu-id="59be2-113">\[in\] The second floating-point value to compare.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="59be2-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="59be2-114">Return Value</span></span>

<span data-ttu-id="59be2-115">1 si le paramètre *x* est supérieur ou égal au paramètre *y* ; Sinon, 0.</span><span class="sxs-lookup"><span data-stu-id="59be2-115">1 if the *x* parameter is greater than or equal to the *y* parameter; otherwise, 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="59be2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="59be2-116">Remarks</span></span>

<span data-ttu-id="59be2-117">Cette fonction utilise la formule suivante : (*x*  >=  *y*) ?</span><span class="sxs-lookup"><span data-stu-id="59be2-117">This function uses the following formula: (*x* >= *y*) ?</span></span> <span data-ttu-id="59be2-118">1:0.</span><span class="sxs-lookup"><span data-stu-id="59be2-118">1 : 0.</span></span> <span data-ttu-id="59be2-119">La fonction retourne la valeur 0 ou 1, selon que le paramètre *x* est supérieur au paramètre *y* .</span><span class="sxs-lookup"><span data-stu-id="59be2-119">The function returns either 0 or 1 depending on whether the *x* parameter is greater than the *y* parameter.</span></span> <span data-ttu-id="59be2-120">Pour calculer une interpolation lisse entre 0 et 1, utilisez la fonction intrinsèque [**SmoothStep**](dx-graphics-hlsl-smoothstep.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="59be2-120">To compute a smooth interpolation between 0 and 1, use the [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL intrinsic function.</span></span>

## <a name="type-description"></a><span data-ttu-id="59be2-121">Description du type</span><span class="sxs-lookup"><span data-stu-id="59be2-121">Type Description</span></span>



| <span data-ttu-id="59be2-122">Nom</span><span class="sxs-lookup"><span data-stu-id="59be2-122">Name</span></span>  | [<span data-ttu-id="59be2-123">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="59be2-123">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="59be2-124">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="59be2-124">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="59be2-125">Taille</span><span class="sxs-lookup"><span data-stu-id="59be2-125">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="59be2-126">*y*</span><span class="sxs-lookup"><span data-stu-id="59be2-126">*y*</span></span>   | <span data-ttu-id="59be2-127">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="59be2-127">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="59be2-128">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="59be2-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="59be2-129">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="59be2-129">any</span></span>                            |
| <span data-ttu-id="59be2-130">*x*</span><span class="sxs-lookup"><span data-stu-id="59be2-130">*x*</span></span>   | <span data-ttu-id="59be2-131">identique à l’entrée *y*</span><span class="sxs-lookup"><span data-stu-id="59be2-131">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="59be2-132">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="59be2-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="59be2-133">la ou les mêmes dimensions comme entrée *y*</span><span class="sxs-lookup"><span data-stu-id="59be2-133">same dimension(s) as input *y*</span></span> |
| <span data-ttu-id="59be2-134">*Av*</span><span class="sxs-lookup"><span data-stu-id="59be2-134">*ret*</span></span> | <span data-ttu-id="59be2-135">identique à l’entrée *y*</span><span class="sxs-lookup"><span data-stu-id="59be2-135">same as input *y*</span></span>                                                                                              | [<span data-ttu-id="59be2-136">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="59be2-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="59be2-137">la ou les mêmes dimensions comme entrée *y*</span><span class="sxs-lookup"><span data-stu-id="59be2-137">same dimension(s) as input *y*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="59be2-138">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="59be2-138">Minimum Shader Model</span></span>

<span data-ttu-id="59be2-139">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="59be2-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="59be2-140">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="59be2-140">Shader Model</span></span>                                                                       | <span data-ttu-id="59be2-141">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="59be2-141">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="59be2-142">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="59be2-142">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="59be2-143">Oui</span><span class="sxs-lookup"><span data-stu-id="59be2-143">yes</span></span>                         |
| [<span data-ttu-id="59be2-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="59be2-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="59be2-145">Oui (vs \_ 1 \_ 1 et PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="59be2-145">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="59be2-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59be2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59be2-147">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="59be2-147">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

