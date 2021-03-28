---
title: rcp
description: Calcule une réciproque rapide, approximative et par composant.
ms.assetid: c8d451e4-717e-45b3-a0fe-da55feb8f443
keywords:
- RCP HLSL
topic_type:
- apiref
api_name:
- rcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a857c897def08f31e18ef19466daa2b4584740a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728196"
---
# <a name="rcp"></a><span data-ttu-id="0c087-104">rcp</span><span class="sxs-lookup"><span data-stu-id="0c087-104">rcp</span></span>

<span data-ttu-id="0c087-105">Calcule une réciproque rapide, approximative et par composant.</span><span class="sxs-lookup"><span data-stu-id="0c087-105">Calculates a fast, approximate, per-component reciprocal.</span></span>



| <span data-ttu-id="0c087-106">*RET* RCP (*x*)</span><span class="sxs-lookup"><span data-stu-id="0c087-106">*ret* rcp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="0c087-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c087-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c087-108"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="0c087-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="0c087-109">\[dans \] la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0c087-109">\[in\] The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c087-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0c087-110">Return Value</span></span>

<span data-ttu-id="0c087-111">Réciproque du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="0c087-111">The reciprocal of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="0c087-112">Description du type</span><span class="sxs-lookup"><span data-stu-id="0c087-112">Type Description</span></span>



| <span data-ttu-id="0c087-113">Nom</span><span class="sxs-lookup"><span data-stu-id="0c087-113">Name</span></span>  | [<span data-ttu-id="0c087-114">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="0c087-114">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0c087-115">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="0c087-115">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                      | <span data-ttu-id="0c087-116">Taille</span><span class="sxs-lookup"><span data-stu-id="0c087-116">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0c087-117">*x*</span><span class="sxs-lookup"><span data-stu-id="0c087-117">*x*</span></span>   | <span data-ttu-id="0c087-118">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="0c087-118">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="0c087-119">[**float**](/windows/desktop/WinProg/windows-data-types) ou [ **double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0c087-119">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="0c087-120">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="0c087-120">any</span></span>                            |
| <span data-ttu-id="0c087-121">*Av*</span><span class="sxs-lookup"><span data-stu-id="0c087-121">*ret*</span></span> | <span data-ttu-id="0c087-122">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="0c087-122">same as input *x*</span></span>                                                                                              | <span data-ttu-id="0c087-123">[**float**](/windows/desktop/WinProg/windows-data-types) ou [ **double**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0c087-123">[**float**](/windows/desktop/WinProg/windows-data-types) or [**double**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="0c087-124">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="0c087-124">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0c087-125">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0c087-125">Minimum Shader Model</span></span>

<span data-ttu-id="0c087-126">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0c087-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0c087-127">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0c087-127">Shader Model</span></span>                                                                | <span data-ttu-id="0c087-128">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0c087-128">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0c087-129">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="0c087-129">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="0c087-130">Oui</span><span class="sxs-lookup"><span data-stu-id="0c087-130">yes</span></span>       |



 

<span data-ttu-id="0c087-131">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="0c087-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="0c087-132">Sommet</span><span class="sxs-lookup"><span data-stu-id="0c087-132">Vertex</span></span> | <span data-ttu-id="0c087-133">Forme</span><span class="sxs-lookup"><span data-stu-id="0c087-133">Hull</span></span> | <span data-ttu-id="0c087-134">Domain</span><span class="sxs-lookup"><span data-stu-id="0c087-134">Domain</span></span> | <span data-ttu-id="0c087-135">Géométrie</span><span class="sxs-lookup"><span data-stu-id="0c087-135">Geometry</span></span> | <span data-ttu-id="0c087-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="0c087-136">Pixel</span></span> | <span data-ttu-id="0c087-137">Compute</span><span class="sxs-lookup"><span data-stu-id="0c087-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0c087-138">x</span><span class="sxs-lookup"><span data-stu-id="0c087-138">x</span></span>      | <span data-ttu-id="0c087-139">x</span><span class="sxs-lookup"><span data-stu-id="0c087-139">x</span></span>    | <span data-ttu-id="0c087-140">x</span><span class="sxs-lookup"><span data-stu-id="0c087-140">x</span></span>      | <span data-ttu-id="0c087-141">x</span><span class="sxs-lookup"><span data-stu-id="0c087-141">x</span></span>        | <span data-ttu-id="0c087-142">x</span><span class="sxs-lookup"><span data-stu-id="0c087-142">x</span></span>     | <span data-ttu-id="0c087-143">x</span><span class="sxs-lookup"><span data-stu-id="0c087-143">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0c087-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c087-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c087-145">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="0c087-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="0c087-146">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0c087-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 