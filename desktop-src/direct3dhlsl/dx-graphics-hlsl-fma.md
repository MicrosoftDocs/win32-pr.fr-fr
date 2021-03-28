---
title: FMA (Corecrt \_ Math. h)
description: Retourne l’addition fusionnée double précision de a \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- HLSL FMA
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287f07881a00ca53a3f1fe702cf4d95b64bf14c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384608"
---
# <a name="fma"></a><span data-ttu-id="81cff-104">fma</span><span class="sxs-lookup"><span data-stu-id="81cff-104">fma</span></span>

<span data-ttu-id="81cff-105">Retourne l’addition fusionnée double précision d’un \* b + c.</span><span class="sxs-lookup"><span data-stu-id="81cff-105">Returns the double-precision fused multiply-addition of a \* b + c.</span></span>



| <span data-ttu-id="81cff-106">*RET* FMA (double *a*, *b*, *c*);</span><span class="sxs-lookup"><span data-stu-id="81cff-106">*ret* fma(double *a*, *b*, *c*);</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="81cff-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81cff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81cff-108"><span id="a"></span><span id="A"></span>*un*</span><span class="sxs-lookup"><span data-stu-id="81cff-108"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="81cff-109">\[dans \] la première valeur de l’addition fusionnée.</span><span class="sxs-lookup"><span data-stu-id="81cff-109">\[in\] The first value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="81cff-110"><span id="b"></span><span id="B"></span>*p*</span><span class="sxs-lookup"><span data-stu-id="81cff-110"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="81cff-111">\[dans \] la deuxième valeur de l’addition fusionnée.</span><span class="sxs-lookup"><span data-stu-id="81cff-111">\[in\] The second value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="81cff-112"><span id="c"></span><span id="C"></span>*secteur*</span><span class="sxs-lookup"><span data-stu-id="81cff-112"><span id="c"></span><span id="C"></span>*c*</span></span>
</dt> <dd>

<span data-ttu-id="81cff-113">\[dans \] la troisième valeur de l’addition fusionnée.</span><span class="sxs-lookup"><span data-stu-id="81cff-113">\[in\] The third value in the fused multiply-addition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81cff-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="81cff-114">Return Value</span></span>

<span data-ttu-id="81cff-115">Addition fusionnée double précision des paramètres *a* \* *b*  +  *c*.</span><span class="sxs-lookup"><span data-stu-id="81cff-115">The double-precision fused multiply-addition of parameters *a* \* *b* + *c*.</span></span> <span data-ttu-id="81cff-116">La valeur retournée doit être précise à 0,5 unités de précision minimale (ULP).</span><span class="sxs-lookup"><span data-stu-id="81cff-116">The returned value must be accurate to 0.5 units of least precision (ULP).</span></span>

## <a name="remarks"></a><span data-ttu-id="81cff-117">Notes</span><span class="sxs-lookup"><span data-stu-id="81cff-117">Remarks</span></span>

<span data-ttu-id="81cff-118">L’intrinsèque **FMA** doit prendre en charge les valeurs NaN, les fichiers INF et les dénormes.</span><span class="sxs-lookup"><span data-stu-id="81cff-118">The **fma** intrinsic must support NaNs, INFs, and Denorms.</span></span>

<span data-ttu-id="81cff-119">Pour utiliser l’intrinsèque **FMA** dans votre code de nuanceur, appelez la méthode [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) avec les [**\_ options d3d11 Feature \_ d3d11 \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) pour vérifier que l’appareil Direct3D prend en charge l’option de fonctionnalité [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .</span><span class="sxs-lookup"><span data-stu-id="81cff-119">To use the **fma** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="81cff-120">L’intrinsèque **FMA** requiert un pilote d’affichage WDDM 1,2, et tous les pilotes d’affichage WDDM 1,2 doivent prendre en charge **FMA**.</span><span class="sxs-lookup"><span data-stu-id="81cff-120">The **fma** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **fma**.</span></span> <span data-ttu-id="81cff-121">Si votre application crée un appareil de rendu avec le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 ou 11,1 et que la cible de compilation est Shader Model 5 ou version ultérieure, le code source HLSL peut utiliser l’intrinsèque **FMA** .</span><span class="sxs-lookup"><span data-stu-id="81cff-121">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **fma** intrinsic.</span></span>

### <a name="type-description"></a><span data-ttu-id="81cff-122">Description du type</span><span class="sxs-lookup"><span data-stu-id="81cff-122">Type Description</span></span>



| <span data-ttu-id="81cff-123">Nom</span><span class="sxs-lookup"><span data-stu-id="81cff-123">Name</span></span>  | [<span data-ttu-id="81cff-124">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="81cff-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="81cff-125">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="81cff-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="81cff-126">Taille</span><span class="sxs-lookup"><span data-stu-id="81cff-126">Size</span></span>                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="81cff-127">*un*</span><span class="sxs-lookup"><span data-stu-id="81cff-127">*a*</span></span>   | <span data-ttu-id="81cff-128">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="81cff-128">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="81cff-129">**Cliquer**</span><span class="sxs-lookup"><span data-stu-id="81cff-129">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="81cff-130">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="81cff-130">any</span></span>                          |
| <span data-ttu-id="81cff-131">*b*</span><span class="sxs-lookup"><span data-stu-id="81cff-131">*b*</span></span>   | <span data-ttu-id="81cff-132">identique à l’entrée *a*</span><span class="sxs-lookup"><span data-stu-id="81cff-132">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="81cff-133">**Cliquer**</span><span class="sxs-lookup"><span data-stu-id="81cff-133">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="81cff-134">mêmes dimensions que l’entrée *a*</span><span class="sxs-lookup"><span data-stu-id="81cff-134">same dimensions as input *a*</span></span> |
| <span data-ttu-id="81cff-135">*c*</span><span class="sxs-lookup"><span data-stu-id="81cff-135">*c*</span></span>   | <span data-ttu-id="81cff-136">identique à l’entrée *a*</span><span class="sxs-lookup"><span data-stu-id="81cff-136">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="81cff-137">**Cliquer**</span><span class="sxs-lookup"><span data-stu-id="81cff-137">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="81cff-138">mêmes dimensions que l’entrée *a*</span><span class="sxs-lookup"><span data-stu-id="81cff-138">same dimensions as input *a*</span></span> |
| <span data-ttu-id="81cff-139">*Av*</span><span class="sxs-lookup"><span data-stu-id="81cff-139">*ret*</span></span> | <span data-ttu-id="81cff-140">identique à l’entrée *a*</span><span class="sxs-lookup"><span data-stu-id="81cff-140">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="81cff-141">**Cliquer**</span><span class="sxs-lookup"><span data-stu-id="81cff-141">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="81cff-142">mêmes dimensions que l’entrée *a*</span><span class="sxs-lookup"><span data-stu-id="81cff-142">same dimensions as input *a*</span></span> |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="81cff-143">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="81cff-143">Minimum Shader Model</span></span>

<span data-ttu-id="81cff-144">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="81cff-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="81cff-145">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="81cff-145">Shader Model</span></span>                                                | <span data-ttu-id="81cff-146">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="81cff-146">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="81cff-147">Shader Model 5 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="81cff-147">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="81cff-148">Oui</span><span class="sxs-lookup"><span data-stu-id="81cff-148">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="81cff-149">Spécifications</span><span class="sxs-lookup"><span data-stu-id="81cff-149">Requirements</span></span>



| <span data-ttu-id="81cff-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81cff-150">Requirement</span></span> | <span data-ttu-id="81cff-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="81cff-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="81cff-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81cff-152">Minimum supported client</span></span><br/> | <span data-ttu-id="81cff-153">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="81cff-153">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="81cff-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81cff-154">Minimum supported server</span></span><br/> | <span data-ttu-id="81cff-155">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="81cff-155">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="81cff-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="81cff-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="81cff-157"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="81cff-157"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81cff-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81cff-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81cff-159">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="81cff-159">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

