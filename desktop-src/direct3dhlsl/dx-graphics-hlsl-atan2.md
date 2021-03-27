---
title: atan2 (Corecrt \_ Math. h)
description: Retourne l’arc tangente de deux valeurs (x, y).
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- langage HLSL atan2
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fbc6574d0fc0d53a165ae7da87c2627a295be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211752"
---
# <a name="atan2"></a><span data-ttu-id="68f8a-104">atan2</span><span class="sxs-lookup"><span data-stu-id="68f8a-104">atan2</span></span>

<span data-ttu-id="68f8a-105">Retourne l’arc tangente de deux valeurs (x, y).</span><span class="sxs-lookup"><span data-stu-id="68f8a-105">Returns the arctangent of two values (x,y).</span></span>



| <span data-ttu-id="68f8a-106">*RET* atan2 (*y*, *x*)</span><span class="sxs-lookup"><span data-stu-id="68f8a-106">*ret* atan2(*y*, *x*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="68f8a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68f8a-107">Parameters</span></span>



| <span data-ttu-id="68f8a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="68f8a-108">Item</span></span>                                                   | <span data-ttu-id="68f8a-109">Description</span><span class="sxs-lookup"><span data-stu-id="68f8a-109">Description</span></span>                    |
|--------------------------------------------------------|--------------------------------|
| <span data-ttu-id="68f8a-110"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="68f8a-110"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="68f8a-111">\[dans \] la valeur y.</span><span class="sxs-lookup"><span data-stu-id="68f8a-111">\[in\] The y value.</span></span><br/> |
| <span data-ttu-id="68f8a-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="68f8a-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="68f8a-113">\[dans \] la valeur x.</span><span class="sxs-lookup"><span data-stu-id="68f8a-113">\[in\] The x value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="68f8a-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="68f8a-114">Return Value</span></span>

<span data-ttu-id="68f8a-115">Arctangente de (y, x).</span><span class="sxs-lookup"><span data-stu-id="68f8a-115">The arctangent of (y,x).</span></span>

## <a name="remarks"></a><span data-ttu-id="68f8a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="68f8a-116">Remarks</span></span>

<span data-ttu-id="68f8a-117">Les signes des paramètres *x* et *y* sont utilisés pour déterminer le quadrant des valeurs de retour dans la plage de-π à π.</span><span class="sxs-lookup"><span data-stu-id="68f8a-117">The signs of the *x* and *y* parameters are used to determine the quadrant of the return values within the range of -π to π.</span></span> <span data-ttu-id="68f8a-118">La fonction intrinsèque HLSL **atan2** est bien définie pour chaque point autre que l’origine, même si *y* est égal à 0 et que *x* n’est pas égal à 0.</span><span class="sxs-lookup"><span data-stu-id="68f8a-118">The **atan2** HLSL intrinsic function is well-defined for every point other than the origin, even if *y* equals 0 and *x* does not equal 0.</span></span>

## <a name="type-description"></a><span data-ttu-id="68f8a-119">Description du type</span><span class="sxs-lookup"><span data-stu-id="68f8a-119">Type Description</span></span>



| <span data-ttu-id="68f8a-120">Nom</span><span class="sxs-lookup"><span data-stu-id="68f8a-120">Name</span></span>  | [<span data-ttu-id="68f8a-121">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="68f8a-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="68f8a-122">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="68f8a-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="68f8a-123">Taille</span><span class="sxs-lookup"><span data-stu-id="68f8a-123">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="68f8a-124">*y*</span><span class="sxs-lookup"><span data-stu-id="68f8a-124">*y*</span></span>   | <span data-ttu-id="68f8a-125">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="68f8a-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="68f8a-126">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="68f8a-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="68f8a-127">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="68f8a-127">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="68f8a-128">*x*</span><span class="sxs-lookup"><span data-stu-id="68f8a-128">*x*</span></span>   | <span data-ttu-id="68f8a-129">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="68f8a-129">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="68f8a-130">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="68f8a-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="68f8a-131">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="68f8a-131">any</span></span>                            |
| <span data-ttu-id="68f8a-132">*Av*</span><span class="sxs-lookup"><span data-stu-id="68f8a-132">*ret*</span></span> | <span data-ttu-id="68f8a-133">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="68f8a-133">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="68f8a-134">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="68f8a-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="68f8a-135">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="68f8a-135">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="68f8a-136">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="68f8a-136">Minimum Shader Model</span></span>

<span data-ttu-id="68f8a-137">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="68f8a-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="68f8a-138">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="68f8a-138">Shader Model</span></span>                                                                       | <span data-ttu-id="68f8a-139">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="68f8a-139">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="68f8a-140">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="68f8a-140">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="68f8a-141">Oui</span><span class="sxs-lookup"><span data-stu-id="68f8a-141">yes</span></span>       |
| [<span data-ttu-id="68f8a-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68f8a-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="68f8a-143">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="68f8a-143">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="68f8a-144">Spécifications</span><span class="sxs-lookup"><span data-stu-id="68f8a-144">Requirements</span></span>



| <span data-ttu-id="68f8a-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68f8a-145">Requirement</span></span> | <span data-ttu-id="68f8a-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="68f8a-146">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="68f8a-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="68f8a-147">Header</span></span><br/> | <dl> <span data-ttu-id="68f8a-148"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="68f8a-148"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68f8a-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68f8a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f8a-150">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="68f8a-150">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

