---
title: orange
description: Retourne un vecteur de coefficient d’éclairage.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- en HLSL allumé
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842313"
---
# <a name="lit"></a><span data-ttu-id="b7da4-104">orange</span><span class="sxs-lookup"><span data-stu-id="b7da4-104">lit</span></span>

<span data-ttu-id="b7da4-105">Retourne un vecteur de coefficient d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="b7da4-105">Returns a lighting coefficient vector.</span></span>



| <span data-ttu-id="b7da4-106">*RET* allumé (*n \_ point \_ l*, *n \_ point \_ h*, *m*)</span><span class="sxs-lookup"><span data-stu-id="b7da4-106">*ret* lit(*n\_dot\_l*, *n\_dot\_h*, *m*)</span></span> |
|------------------------------------------|



 

<span data-ttu-id="b7da4-107">Cette fonction retourne un vecteur de coefficient d’éclairage (ambiant, diffuse, spéculaire, 1) où :</span><span class="sxs-lookup"><span data-stu-id="b7da4-107">This function returns a lighting coefficient vector (ambient, diffuse, specular, 1) where:</span></span>

-   <span data-ttu-id="b7da4-108">ambiant = 1</span><span class="sxs-lookup"><span data-stu-id="b7da4-108">ambient = 1</span></span>
-   <span data-ttu-id="b7da4-109">diffuse = n · l < 0 ?</span><span class="sxs-lookup"><span data-stu-id="b7da4-109">diffuse = n · l < 0 ?</span></span> <span data-ttu-id="b7da4-110">0 : n · budget</span><span class="sxs-lookup"><span data-stu-id="b7da4-110">0 : n · l</span></span>
-   <span data-ttu-id="b7da4-111">spéculaire = n · l < 0 \| \| n · h < 0 ?</span><span class="sxs-lookup"><span data-stu-id="b7da4-111">specular = n · l < 0 \|\| n · h < 0 ?</span></span> <span data-ttu-id="b7da4-112">0 : (n · h) ^ m</span><span class="sxs-lookup"><span data-stu-id="b7da4-112">0 : (n · h) ^ m</span></span>

<span data-ttu-id="b7da4-113">Où le vecteur n est le vecteur normal, l est la direction de la lumière et h est le demi-vecteur.</span><span class="sxs-lookup"><span data-stu-id="b7da4-113">Where the vector n is the normal vector, l is the direction to light and h is the half vector.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7da4-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7da4-114">Parameters</span></span>



| <span data-ttu-id="b7da4-115">Élément</span><span class="sxs-lookup"><span data-stu-id="b7da4-115">Item</span></span>                                                                       | <span data-ttu-id="b7da4-116">Description</span><span class="sxs-lookup"><span data-stu-id="b7da4-116">Description</span></span>                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7da4-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ point \_ l*</span><span class="sxs-lookup"><span data-stu-id="b7da4-117"><span id="n_dot_l"></span><span id="N_DOT_L"></span>*n\_dot\_l*</span></span><br/> | <span data-ttu-id="b7da4-118">\[dans \] le produit scalaire de la surface normalisée normale et le vecteur clair.</span><span class="sxs-lookup"><span data-stu-id="b7da4-118">\[in\] The dot product of the normalized surface normal and the light vector.</span></span><br/> |
| <span data-ttu-id="b7da4-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ points \_ h*</span><span class="sxs-lookup"><span data-stu-id="b7da4-119"><span id="n_dot_h"></span><span id="N_DOT_H"></span>*n\_dot\_h*</span></span><br/> | <span data-ttu-id="b7da4-120">\[dans \] le produit scalaire du vecteur demi-angle et de la surface normal.</span><span class="sxs-lookup"><span data-stu-id="b7da4-120">\[in\] The dot product of the half-angle vector and the surface normal.</span></span><br/>       |
| <span data-ttu-id="b7da4-121"><span id="m"></span><span id="M"></span>*lecteur*</span><span class="sxs-lookup"><span data-stu-id="b7da4-121"><span id="m"></span><span id="M"></span>*m*</span></span><br/>                     | <span data-ttu-id="b7da4-122">\[dans \] un exposant spéculaire.</span><span class="sxs-lookup"><span data-stu-id="b7da4-122">\[in\] A specular exponent.</span></span><br/>                                                   |



 

## <a name="return-value"></a><span data-ttu-id="b7da4-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b7da4-123">Return Value</span></span>

<span data-ttu-id="b7da4-124">Vecteur du coefficient d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="b7da4-124">The lighting coefficient vector.</span></span>

## <a name="type-description"></a><span data-ttu-id="b7da4-125">Description du type</span><span class="sxs-lookup"><span data-stu-id="b7da4-125">Type Description</span></span>



| <span data-ttu-id="b7da4-126">Nom</span><span class="sxs-lookup"><span data-stu-id="b7da4-126">Name</span></span>        | [<span data-ttu-id="b7da4-127">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="b7da4-127">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="b7da4-128">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="b7da4-128">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="b7da4-129">Taille</span><span class="sxs-lookup"><span data-stu-id="b7da4-129">Size</span></span> |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="b7da4-130">*n \_ point \_ l*</span><span class="sxs-lookup"><span data-stu-id="b7da4-130">*n\_dot\_l*</span></span> | [<span data-ttu-id="b7da4-131">**scalaire**</span><span class="sxs-lookup"><span data-stu-id="b7da4-131">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b7da4-132">**float**</span><span class="sxs-lookup"><span data-stu-id="b7da4-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7da4-133">1</span><span class="sxs-lookup"><span data-stu-id="b7da4-133">1</span></span>    |
| <span data-ttu-id="b7da4-134">*n \_ points \_ h*</span><span class="sxs-lookup"><span data-stu-id="b7da4-134">*n\_dot\_h*</span></span> | [<span data-ttu-id="b7da4-135">**scalaire**</span><span class="sxs-lookup"><span data-stu-id="b7da4-135">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b7da4-136">**float**</span><span class="sxs-lookup"><span data-stu-id="b7da4-136">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7da4-137">1</span><span class="sxs-lookup"><span data-stu-id="b7da4-137">1</span></span>    |
| <span data-ttu-id="b7da4-138">*m*</span><span class="sxs-lookup"><span data-stu-id="b7da4-138">*m*</span></span>         | [<span data-ttu-id="b7da4-139">**scalaire**</span><span class="sxs-lookup"><span data-stu-id="b7da4-139">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b7da4-140">**float**</span><span class="sxs-lookup"><span data-stu-id="b7da4-140">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7da4-141">1</span><span class="sxs-lookup"><span data-stu-id="b7da4-141">1</span></span>    |
| <span data-ttu-id="b7da4-142">*Av*</span><span class="sxs-lookup"><span data-stu-id="b7da4-142">*ret*</span></span>       | [<span data-ttu-id="b7da4-143">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="b7da4-143">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="b7da4-144">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="b7da4-144">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="b7da4-145">4</span><span class="sxs-lookup"><span data-stu-id="b7da4-145">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b7da4-146">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b7da4-146">Minimum Shader Model</span></span>

<span data-ttu-id="b7da4-147">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b7da4-147">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b7da4-148">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b7da4-148">Shader Model</span></span>                                                                       | <span data-ttu-id="b7da4-149">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b7da4-149">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="b7da4-150">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="b7da4-150">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="b7da4-151">Oui</span><span class="sxs-lookup"><span data-stu-id="b7da4-151">yes</span></span>                 |
| [<span data-ttu-id="b7da4-152">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7da4-152">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="b7da4-153">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="b7da4-153">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="b7da4-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7da4-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7da4-155">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="b7da4-155">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

