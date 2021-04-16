---
title: minute(s)
description: Sélectionne le plus petit de x et y.
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- HLSL min
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 129c5cb641c2d69b6c1365d8221663e264060532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463635"
---
# <a name="min"></a><span data-ttu-id="a82dc-104">minute(s)</span><span class="sxs-lookup"><span data-stu-id="a82dc-104">min</span></span>

<span data-ttu-id="a82dc-105">Sélectionne le plus petit de x et y.</span><span class="sxs-lookup"><span data-stu-id="a82dc-105">Selects the lesser of x and y.</span></span>



| <span data-ttu-id="a82dc-106">RET min (x, y)</span><span class="sxs-lookup"><span data-stu-id="a82dc-106">ret min(x, y)</span></span> |
|---------------|



 

## <a name="parameters"></a><span data-ttu-id="a82dc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a82dc-107">Parameters</span></span>



| <span data-ttu-id="a82dc-108">Élément</span><span class="sxs-lookup"><span data-stu-id="a82dc-108">Item</span></span>                                                   | <span data-ttu-id="a82dc-109">Description</span><span class="sxs-lookup"><span data-stu-id="a82dc-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="a82dc-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="a82dc-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a82dc-111">\[dans \] la valeur d’entrée x.</span><span class="sxs-lookup"><span data-stu-id="a82dc-111">\[in\] The x input value.</span></span><br/> |
| <span data-ttu-id="a82dc-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="a82dc-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="a82dc-113">\[dans \] la valeur d’entrée y.</span><span class="sxs-lookup"><span data-stu-id="a82dc-113">\[in\] The y input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a82dc-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a82dc-114">Return Value</span></span>

<span data-ttu-id="a82dc-115">Paramètre *x* ou *y* , selon la valeur la plus petite.</span><span class="sxs-lookup"><span data-stu-id="a82dc-115">The *x* or *y* parameter, whichever is the smallest value.</span></span>


## <a name="remarks"></a><span data-ttu-id="a82dc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a82dc-116">Remarks</span></span>

<span data-ttu-id="a82dc-117">Les dénormals sont gérés comme suit :</span><span class="sxs-lookup"><span data-stu-id="a82dc-117">Denormals are handled as follows:</span></span>

| <span data-ttu-id="a82dc-118">src0 src1-></span><span class="sxs-lookup"><span data-stu-id="a82dc-118">src0 src1-></span></span> | <span data-ttu-id="a82dc-119">-inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-119">-inf</span></span> | <span data-ttu-id="a82dc-120">F</span><span class="sxs-lookup"><span data-stu-id="a82dc-120">F</span></span>             | <span data-ttu-id="a82dc-121">+inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-121">+inf</span></span> | <span data-ttu-id="a82dc-122">NAN</span><span class="sxs-lookup"><span data-stu-id="a82dc-122">NAN</span></span>  |
|-------------|------|---------------|------|------|
| <span data-ttu-id="a82dc-123">-inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-123">-inf</span></span>        | <span data-ttu-id="a82dc-124">-inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-124">-inf</span></span> | <span data-ttu-id="a82dc-125">-inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-125">-inf</span></span>          | <span data-ttu-id="a82dc-126">-inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-126">-inf</span></span> | <span data-ttu-id="a82dc-127">-inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-127">-inf</span></span> |
| <span data-ttu-id="a82dc-128">F</span><span class="sxs-lookup"><span data-stu-id="a82dc-128">F</span></span>           | <span data-ttu-id="a82dc-129">-inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-129">-inf</span></span> | <span data-ttu-id="a82dc-130">src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="a82dc-130">src0 or src1</span></span>  | <span data-ttu-id="a82dc-131">src0</span><span class="sxs-lookup"><span data-stu-id="a82dc-131">src0</span></span> | <span data-ttu-id="a82dc-132">src0</span><span class="sxs-lookup"><span data-stu-id="a82dc-132">src0</span></span> |
| <span data-ttu-id="a82dc-133">+inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-133">+inf</span></span>        | <span data-ttu-id="a82dc-134">-inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-134">-inf</span></span> | <span data-ttu-id="a82dc-135">src1</span><span class="sxs-lookup"><span data-stu-id="a82dc-135">src1</span></span>          | <span data-ttu-id="a82dc-136">+inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-136">+inf</span></span> | <span data-ttu-id="a82dc-137">+inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-137">+inf</span></span> |
| <span data-ttu-id="a82dc-138">NaN</span><span class="sxs-lookup"><span data-stu-id="a82dc-138">NaN</span></span>         | <span data-ttu-id="a82dc-139">-inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-139">-inf</span></span> | <span data-ttu-id="a82dc-140">src1</span><span class="sxs-lookup"><span data-stu-id="a82dc-140">src1</span></span>          | <span data-ttu-id="a82dc-141">+inf</span><span class="sxs-lookup"><span data-stu-id="a82dc-141">+inf</span></span> | <span data-ttu-id="a82dc-142">NaN</span><span class="sxs-lookup"><span data-stu-id="a82dc-142">NaN</span></span>  |

<span data-ttu-id="a82dc-143">F signifie nombre fini-réel.</span><span class="sxs-lookup"><span data-stu-id="a82dc-143">F means finite-real number.</span></span>


## <a name="type-description"></a><span data-ttu-id="a82dc-144">Description du type</span><span class="sxs-lookup"><span data-stu-id="a82dc-144">Type Description</span></span>

| <span data-ttu-id="a82dc-145">Nom</span><span class="sxs-lookup"><span data-stu-id="a82dc-145">Name</span></span> | <span data-ttu-id="a82dc-146">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="a82dc-146">In/Out</span></span>      | [<span data-ttu-id="a82dc-147">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="a82dc-147">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a82dc-148">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="a82dc-148">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="a82dc-149">Taille</span><span class="sxs-lookup"><span data-stu-id="a82dc-149">Size</span></span>                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="a82dc-150">x</span><span class="sxs-lookup"><span data-stu-id="a82dc-150">x</span></span>    | <span data-ttu-id="a82dc-151">in</span><span class="sxs-lookup"><span data-stu-id="a82dc-151">in</span></span>          | <span data-ttu-id="a82dc-152">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="a82dc-152">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="a82dc-153">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a82dc-153">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="a82dc-154">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="a82dc-154">any</span></span>                          |
| <span data-ttu-id="a82dc-155">y</span><span class="sxs-lookup"><span data-stu-id="a82dc-155">y</span></span>    | <span data-ttu-id="a82dc-156">in</span><span class="sxs-lookup"><span data-stu-id="a82dc-156">in</span></span>          | <span data-ttu-id="a82dc-157">identique à l’entrée x</span><span class="sxs-lookup"><span data-stu-id="a82dc-157">same as input x</span></span>                                                                                                | <span data-ttu-id="a82dc-158">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a82dc-158">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="a82dc-159">la ou les mêmes dimensions comme entrée x</span><span class="sxs-lookup"><span data-stu-id="a82dc-159">same dimension(s) as input x</span></span> |
| <span data-ttu-id="a82dc-160">Av</span><span class="sxs-lookup"><span data-stu-id="a82dc-160">ret</span></span>  | <span data-ttu-id="a82dc-161">type de retour</span><span class="sxs-lookup"><span data-stu-id="a82dc-161">return type</span></span> | <span data-ttu-id="a82dc-162">identique à l’entrée x</span><span class="sxs-lookup"><span data-stu-id="a82dc-162">same as input x</span></span>                                                                                                | <span data-ttu-id="a82dc-163">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a82dc-163">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="a82dc-164">la ou les mêmes dimensions comme entrée x</span><span class="sxs-lookup"><span data-stu-id="a82dc-164">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a82dc-165">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="a82dc-165">Minimum Shader Model</span></span>

<span data-ttu-id="a82dc-166">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="a82dc-166">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a82dc-167">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a82dc-167">Shader Model</span></span>                                                                       | <span data-ttu-id="a82dc-168">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="a82dc-168">Supported</span></span>                   |
|------------------------------------------------------------------------------------|-----------------------------|
| <span data-ttu-id="a82dc-169">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="a82dc-169">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="a82dc-170">Oui</span><span class="sxs-lookup"><span data-stu-id="a82dc-170">yes</span></span>                         |
| [<span data-ttu-id="a82dc-171">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a82dc-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="a82dc-172">Oui (vs \_ 1 \_ 1 et PS \_ 1 \_ 4)</span><span class="sxs-lookup"><span data-stu-id="a82dc-172">yes (vs\_1\_1 and ps\_1\_4)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="a82dc-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a82dc-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a82dc-174">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a82dc-174">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[<span data-ttu-id="a82dc-175">**Spécification fonctionnelle DirectX**</span><span class="sxs-lookup"><span data-stu-id="a82dc-175">**DirectX Functional Specification**</span></span>](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)