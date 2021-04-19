---
title: fraction
description: Retourne un vecteur de réfraction à l’aide d’une entrée Ray, d’une surface normale et d’un index de réfraction.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- réfractx HLSL
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991008"
---
# <a name="refract"></a><span data-ttu-id="bc2f1-104">fraction</span><span class="sxs-lookup"><span data-stu-id="bc2f1-104">refract</span></span>

<span data-ttu-id="bc2f1-105">Retourne un vecteur de réfraction à l’aide d’une entrée Ray, d’une surface normale et d’un index de réfraction.</span><span class="sxs-lookup"><span data-stu-id="bc2f1-105">Returns a refraction vector using an entering ray, a surface normal, and a refraction index.</span></span>



| <span data-ttu-id="bc2f1-106">*RET* réfract (*i*, *n*, ?)</span><span class="sxs-lookup"><span data-stu-id="bc2f1-106">*ret* refract(*i*, *n*, ?)</span></span> |
|----------------------------|



 

## <a name="parameters"></a><span data-ttu-id="bc2f1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc2f1-107">Parameters</span></span>



| <span data-ttu-id="bc2f1-108">Élément</span><span class="sxs-lookup"><span data-stu-id="bc2f1-108">Item</span></span>                                                   | <span data-ttu-id="bc2f1-109">Description</span><span class="sxs-lookup"><span data-stu-id="bc2f1-109">Description</span></span>                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bc2f1-110"><span id="i"></span><span id="I"></span>*cliqu*</span><span class="sxs-lookup"><span data-stu-id="bc2f1-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="bc2f1-111">\[dans \] un vecteur de direction de rayon à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="bc2f1-111">\[in\] A floating-point, ray direction vector.</span></span><br/>    |
| <span data-ttu-id="bc2f1-112"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="bc2f1-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="bc2f1-113">\[dans \] un vecteur de surface à virgule flottante, vecteur normal.</span><span class="sxs-lookup"><span data-stu-id="bc2f1-113">\[in\] A floating-point, surface normal vector.</span></span><br/>   |
| <span data-ttu-id="bc2f1-114">*?*</span><span class="sxs-lookup"><span data-stu-id="bc2f1-114">*?*</span></span><br/>                                         | <span data-ttu-id="bc2f1-115">\[dans \] un index scalaire à virgule flottante, réfraction.</span><span class="sxs-lookup"><span data-stu-id="bc2f1-115">\[in\] A floating-point, refraction index scalar.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="bc2f1-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bc2f1-116">Return Value</span></span>

<span data-ttu-id="bc2f1-117">Vecteur à virgule flottante, réfraction.</span><span class="sxs-lookup"><span data-stu-id="bc2f1-117">A floating-point, refraction vector.</span></span> <span data-ttu-id="bc2f1-118">Si l’angle entre l’entrée de Ray i et la surface normale n est trop grand pour un index de réfraction donné ?, la valeur de retour est (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="bc2f1-118">If the angle between the entering ray i and the surface normal n is too great for a given refraction index ?, the return value is (0,0,0).</span></span>

## <a name="type-description"></a><span data-ttu-id="bc2f1-119">Description du type</span><span class="sxs-lookup"><span data-stu-id="bc2f1-119">Type Description</span></span>



| <span data-ttu-id="bc2f1-120">Nom</span><span class="sxs-lookup"><span data-stu-id="bc2f1-120">Name</span></span>              | [<span data-ttu-id="bc2f1-121">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="bc2f1-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="bc2f1-122">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="bc2f1-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="bc2f1-123">Taille</span><span class="sxs-lookup"><span data-stu-id="bc2f1-123">Size</span></span>                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="bc2f1-124">*i*</span><span class="sxs-lookup"><span data-stu-id="bc2f1-124">*i*</span></span>               | [<span data-ttu-id="bc2f1-125">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="bc2f1-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bc2f1-126">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="bc2f1-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bc2f1-127">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="bc2f1-127">any</span></span>                            |
| <span data-ttu-id="bc2f1-128">*n*</span><span class="sxs-lookup"><span data-stu-id="bc2f1-128">*n*</span></span>               | [<span data-ttu-id="bc2f1-129">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="bc2f1-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bc2f1-130">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="bc2f1-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bc2f1-131">la ou les mêmes dimensions que l’entrée *i*</span><span class="sxs-lookup"><span data-stu-id="bc2f1-131">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="bc2f1-132">?</span><span class="sxs-lookup"><span data-stu-id="bc2f1-132">?</span></span>                 | [<span data-ttu-id="bc2f1-133">**scalaire**</span><span class="sxs-lookup"><span data-stu-id="bc2f1-133">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bc2f1-134">**float**</span><span class="sxs-lookup"><span data-stu-id="bc2f1-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bc2f1-135">1</span><span class="sxs-lookup"><span data-stu-id="bc2f1-135">1</span></span>                              |
| <span data-ttu-id="bc2f1-136">vecteur de réfraction</span><span class="sxs-lookup"><span data-stu-id="bc2f1-136">refraction vector</span></span> | [<span data-ttu-id="bc2f1-137">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="bc2f1-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="bc2f1-138">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="bc2f1-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="bc2f1-139">la ou les mêmes dimensions que l’entrée *i*</span><span class="sxs-lookup"><span data-stu-id="bc2f1-139">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bc2f1-140">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="bc2f1-140">Minimum Shader Model</span></span>

<span data-ttu-id="bc2f1-141">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="bc2f1-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bc2f1-142">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="bc2f1-142">Shader Model</span></span>                                                                       | <span data-ttu-id="bc2f1-143">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="bc2f1-143">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="bc2f1-144">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="bc2f1-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="bc2f1-145">Oui</span><span class="sxs-lookup"><span data-stu-id="bc2f1-145">yes</span></span>                 |
| [<span data-ttu-id="bc2f1-146">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bc2f1-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="bc2f1-147">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="bc2f1-147">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="bc2f1-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc2f1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc2f1-149">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="bc2f1-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

