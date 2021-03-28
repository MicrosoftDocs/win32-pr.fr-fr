---
title: max
description: Sélectionne la valeur supérieure de x et y.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- HLSL max.
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a40ccb32bb2c2fcd7ca7342b9d7d4d143688102
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382395"
---
# <a name="max"></a><span data-ttu-id="02aa1-104">max</span><span class="sxs-lookup"><span data-stu-id="02aa1-104">max</span></span>

<span data-ttu-id="02aa1-105">Sélectionne la valeur supérieure de x et y.</span><span class="sxs-lookup"><span data-stu-id="02aa1-105">Selects the greater of x and y.</span></span>



| <span data-ttu-id="02aa1-106">RET Max (x, y)</span><span class="sxs-lookup"><span data-stu-id="02aa1-106">ret max(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="02aa1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02aa1-107">Parameters</span></span>



| <span data-ttu-id="02aa1-108">Élément</span><span class="sxs-lookup"><span data-stu-id="02aa1-108">Item</span></span>                                                   | <span data-ttu-id="02aa1-109">Description</span><span class="sxs-lookup"><span data-stu-id="02aa1-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="02aa1-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="02aa1-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="02aa1-111">\[dans \] la valeur d’entrée x.</span><span class="sxs-lookup"><span data-stu-id="02aa1-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="02aa1-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="02aa1-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="02aa1-113">\[dans \] la valeur d’entrée y.</span><span class="sxs-lookup"><span data-stu-id="02aa1-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="02aa1-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="02aa1-114">Return Value</span></span>

<span data-ttu-id="02aa1-115">Paramètre *x* ou *y* , selon la valeur la plus grande.</span><span class="sxs-lookup"><span data-stu-id="02aa1-115">The *x* or *y* parameter, whichever is the largest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="02aa1-116">Notes</span><span class="sxs-lookup"><span data-stu-id="02aa1-116">Remarks</span></span>

<span data-ttu-id="02aa1-117">Les dénormals sont gérés comme suit :</span><span class="sxs-lookup"><span data-stu-id="02aa1-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="02aa1-118">src0 src1-></span><span class="sxs-lookup"><span data-stu-id="02aa1-118">src0 src1-></span></span> | <span data-ttu-id="02aa1-119">-inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-119">-inf</span></span> | <span data-ttu-id="02aa1-120">F</span><span class="sxs-lookup"><span data-stu-id="02aa1-120">F</span></span>             | <span data-ttu-id="02aa1-121">+inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-121">+inf</span></span> | <span data-ttu-id="02aa1-122">NAN</span><span class="sxs-lookup"><span data-stu-id="02aa1-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="02aa1-123">-inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-123">-inf</span></span>        | <span data-ttu-id="02aa1-124">-inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-124">-inf</span></span> | <span data-ttu-id="02aa1-125">src1</span><span class="sxs-lookup"><span data-stu-id="02aa1-125">src1</span></span>          | <span data-ttu-id="02aa1-126">+inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-126">+inf</span></span> | <span data-ttu-id="02aa1-127">-inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-127">-inf</span></span> |
| <span data-ttu-id="02aa1-128">F</span><span class="sxs-lookup"><span data-stu-id="02aa1-128">F</span></span>           | <span data-ttu-id="02aa1-129">src0</span><span class="sxs-lookup"><span data-stu-id="02aa1-129">src0</span></span> | <span data-ttu-id="02aa1-130">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="02aa1-130">src0 or src1</span></span>  | <span data-ttu-id="02aa1-131">+inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-131">+inf</span></span> | <span data-ttu-id="02aa1-132">src0</span><span class="sxs-lookup"><span data-stu-id="02aa1-132">src0</span></span> |
| <span data-ttu-id="02aa1-133">+inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-133">+inf</span></span>        | <span data-ttu-id="02aa1-134">+inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-134">+inf</span></span> | <span data-ttu-id="02aa1-135">+inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-135">+inf</span></span>          | <span data-ttu-id="02aa1-136">+inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-136">+inf</span></span> | <span data-ttu-id="02aa1-137">+inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-137">+inf</span></span> |
| <span data-ttu-id="02aa1-138">NaN</span><span class="sxs-lookup"><span data-stu-id="02aa1-138">NaN</span></span>         | <span data-ttu-id="02aa1-139">-inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-139">-inf</span></span> | <span data-ttu-id="02aa1-140">src1</span><span class="sxs-lookup"><span data-stu-id="02aa1-140">src1</span></span>          | <span data-ttu-id="02aa1-141">+inf</span><span class="sxs-lookup"><span data-stu-id="02aa1-141">+inf</span></span> | <span data-ttu-id="02aa1-142">NaN</span><span class="sxs-lookup"><span data-stu-id="02aa1-142">NaN</span></span>  |

<span data-ttu-id="02aa1-143">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="02aa1-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="02aa1-144">Description du type</span><span class="sxs-lookup"><span data-stu-id="02aa1-144">Type Description</span></span>

| <span data-ttu-id="02aa1-145">Nom</span><span class="sxs-lookup"><span data-stu-id="02aa1-145">Name</span></span> | <span data-ttu-id="02aa1-146">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="02aa1-146">In/Out</span></span>      | [<span data-ttu-id="02aa1-147">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="02aa1-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="02aa1-148">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="02aa1-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="02aa1-149">Taille</span><span class="sxs-lookup"><span data-stu-id="02aa1-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="02aa1-150">x</span><span class="sxs-lookup"><span data-stu-id="02aa1-150">x</span></span>    | <span data-ttu-id="02aa1-151">in</span><span class="sxs-lookup"><span data-stu-id="02aa1-151">in</span></span>          | <span data-ttu-id="02aa1-152">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="02aa1-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="02aa1-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="02aa1-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="02aa1-154">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="02aa1-154">any</span></span>                          |
| <span data-ttu-id="02aa1-155">y</span><span class="sxs-lookup"><span data-stu-id="02aa1-155">y</span></span>    | <span data-ttu-id="02aa1-156">in</span><span class="sxs-lookup"><span data-stu-id="02aa1-156">in</span></span>          | <span data-ttu-id="02aa1-157">identique à l’entrée x</span><span class="sxs-lookup"><span data-stu-id="02aa1-157">same as input x</span></span>                                                                                                | <span data-ttu-id="02aa1-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="02aa1-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="02aa1-159">la ou les mêmes dimensions comme entrée x</span><span class="sxs-lookup"><span data-stu-id="02aa1-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="02aa1-160">Av</span><span class="sxs-lookup"><span data-stu-id="02aa1-160">ret</span></span>  | <span data-ttu-id="02aa1-161">type de retour</span><span class="sxs-lookup"><span data-stu-id="02aa1-161">return type</span></span> | <span data-ttu-id="02aa1-162">identique à l’entrée x</span><span class="sxs-lookup"><span data-stu-id="02aa1-162">same as input x</span></span>                                                                                                | <span data-ttu-id="02aa1-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="02aa1-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="02aa1-164">la ou les mêmes dimensions comme entrée x</span><span class="sxs-lookup"><span data-stu-id="02aa1-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="02aa1-165">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="02aa1-165">Minimum Shader Model</span></span>

<span data-ttu-id="02aa1-166">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="02aa1-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="02aa1-167">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="02aa1-167">Shader Model</span></span>                                                                       | <span data-ttu-id="02aa1-168">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="02aa1-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="02aa1-169">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="02aa1-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="02aa1-170">Oui</span><span class="sxs-lookup"><span data-stu-id="02aa1-170">yes</span></span>                         |
| [<span data-ttu-id="02aa1-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="02aa1-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="02aa1-172">Oui (vs \_ 1 \_ 1 et PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="02aa1-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="02aa1-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02aa1-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02aa1-174">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="02aa1-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="02aa1-175">**Spécification fonctionnelle DirectX**</span><span class="sxs-lookup"><span data-stu-id="02aa1-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
