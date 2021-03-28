---
title: faceforward
description: Retourne la surface normale (si nécessaire) à la face dans une direction opposée à i ; retourne le résultat dans n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- HLSL faceforward
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101824"
---
# <a name="faceforward"></a><span data-ttu-id="53d38-104">faceforward</span><span class="sxs-lookup"><span data-stu-id="53d38-104">faceforward</span></span>

<span data-ttu-id="53d38-105">Retourne la surface normale (si nécessaire) à la face dans une direction opposée à i ; retourne le résultat dans n.</span><span class="sxs-lookup"><span data-stu-id="53d38-105">Flips the surface-normal (if needed) to face in a direction opposite to i; returns the result in n.</span></span>



| <span data-ttu-id="53d38-106">*RET* faceforward (*n*, *i*, *ng*)</span><span class="sxs-lookup"><span data-stu-id="53d38-106">*ret* faceforward(*n*, *i*, *ng*)</span></span> |
|-----------------------------------|



 

<span data-ttu-id="53d38-107">Cette fonction utilise la formule suivante :-*n*  signe (point (*i*, *ng*)).</span><span class="sxs-lookup"><span data-stu-id="53d38-107">This function uses the following formula: -*n*  sign(dot(*i*, *ng*)).</span></span>

## <a name="parameters"></a><span data-ttu-id="53d38-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53d38-108">Parameters</span></span>



| <span data-ttu-id="53d38-109">Élément</span><span class="sxs-lookup"><span data-stu-id="53d38-109">Item</span></span>                                                      | <span data-ttu-id="53d38-110">Description</span><span class="sxs-lookup"><span data-stu-id="53d38-110">Description</span></span>                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53d38-111"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="53d38-111"><span id="n"></span><span id="N"></span>*n*</span></span><br/>    | <span data-ttu-id="53d38-112">\[dans \] le vecteur de surface à virgule flottante résultant-normal.</span><span class="sxs-lookup"><span data-stu-id="53d38-112">\[in\] The resulting floating-point surface-normal vector.</span></span><br/>                                           |
| <span data-ttu-id="53d38-113"><span id="i"></span><span id="I"></span>*cliqu*</span><span class="sxs-lookup"><span data-stu-id="53d38-113"><span id="i"></span><span id="I"></span>*i*</span></span><br/>    | <span data-ttu-id="53d38-114">\[dans \] un vecteur à virgule flottante, vecteur d’incident qui pointe de la position de la vue à la position d’ombrage.</span><span class="sxs-lookup"><span data-stu-id="53d38-114">\[in\] A floating-point, incident vector that points from the view position to the shading position.</span></span><br/> |
| <span data-ttu-id="53d38-115"><span id="ng"></span><span id="NG"></span>*ng*</span><span class="sxs-lookup"><span data-stu-id="53d38-115"><span id="ng"></span><span id="NG"></span>*ng*</span></span><br/> | <span data-ttu-id="53d38-116">\[dans \] un vecteur de surface à virgule flottante-normal.</span><span class="sxs-lookup"><span data-stu-id="53d38-116">\[in\] A floating-point surface-normal vector.</span></span><br/>                                                       |



 

## <a name="return-value"></a><span data-ttu-id="53d38-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="53d38-117">Return Value</span></span>

<span data-ttu-id="53d38-118">Vecteur normal à virgule flottante qui est orienté vers le sens de la vue.</span><span class="sxs-lookup"><span data-stu-id="53d38-118">A floating-point, surface normal vector that is facing the view direction.</span></span>

## <a name="type-description"></a><span data-ttu-id="53d38-119">Description du type</span><span class="sxs-lookup"><span data-stu-id="53d38-119">Type Description</span></span>



| <span data-ttu-id="53d38-120">Nom</span><span class="sxs-lookup"><span data-stu-id="53d38-120">Name</span></span>  | [<span data-ttu-id="53d38-121">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="53d38-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="53d38-122">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="53d38-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="53d38-123">Taille</span><span class="sxs-lookup"><span data-stu-id="53d38-123">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="53d38-124">*n*</span><span class="sxs-lookup"><span data-stu-id="53d38-124">*n*</span></span>   | [<span data-ttu-id="53d38-125">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="53d38-125">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="53d38-126">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="53d38-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="53d38-127">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="53d38-127">any</span></span>                            |
| <span data-ttu-id="53d38-128">*i*</span><span class="sxs-lookup"><span data-stu-id="53d38-128">*i*</span></span>   | [<span data-ttu-id="53d38-129">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="53d38-129">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="53d38-130">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="53d38-130">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="53d38-131">la ou les mêmes dimensions comme entrée *n*</span><span class="sxs-lookup"><span data-stu-id="53d38-131">same dimension(s) as input *n*</span></span> |
| <span data-ttu-id="53d38-132">*ng*</span><span class="sxs-lookup"><span data-stu-id="53d38-132">*ng*</span></span>  | [<span data-ttu-id="53d38-133">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="53d38-133">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="53d38-134">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="53d38-134">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="53d38-135">mêmes dimensions que l’entrée *n*</span><span class="sxs-lookup"><span data-stu-id="53d38-135">same dimensions as input *n*</span></span>   |
| <span data-ttu-id="53d38-136">*Av*</span><span class="sxs-lookup"><span data-stu-id="53d38-136">*ret*</span></span> | [<span data-ttu-id="53d38-137">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="53d38-137">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="53d38-138">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="53d38-138">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="53d38-139">mêmes dimensions que l’entrée *n*</span><span class="sxs-lookup"><span data-stu-id="53d38-139">same dimensions as input *n*</span></span>   |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="53d38-140">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="53d38-140">Minimum Shader Model</span></span>

<span data-ttu-id="53d38-141">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="53d38-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="53d38-142">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="53d38-142">Shader Model</span></span>                                                                       | <span data-ttu-id="53d38-143">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="53d38-143">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="53d38-144">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="53d38-144">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="53d38-145">Oui</span><span class="sxs-lookup"><span data-stu-id="53d38-145">yes</span></span>                   |
| [<span data-ttu-id="53d38-146">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="53d38-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="53d38-147">vs \_ 1 \_ 1 et PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="53d38-147">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="53d38-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53d38-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d38-149">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="53d38-149">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

