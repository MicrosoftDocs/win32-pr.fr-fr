---
title: SinCos,
description: Retourne le sinus et le cosinus de x.
ms.assetid: 2ef9e84e-4539-47f5-9966-d8e02ca15d36
keywords:
- HLSL SinCos,
topic_type:
- apiref
api_name:
- sincos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8391c2fcecc939db1d7044fe56fbd281fe3e79fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990993"
---
# <a name="sincos"></a><span data-ttu-id="da5c0-104">SinCos,</span><span class="sxs-lookup"><span data-stu-id="da5c0-104">sincos</span></span>

<span data-ttu-id="da5c0-105">Retourne le sinus et le cosinus de x.</span><span class="sxs-lookup"><span data-stu-id="da5c0-105">Returns the sine and cosine of x.</span></span>



| <span data-ttu-id="da5c0-106">SinCos, (*x*, sortie *s*, sortie *c*)</span><span class="sxs-lookup"><span data-stu-id="da5c0-106">sincos(*x*, out *s*, out *c*)</span></span> |
|-------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="da5c0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da5c0-107">Parameters</span></span>



| <span data-ttu-id="da5c0-108">Élément</span><span class="sxs-lookup"><span data-stu-id="da5c0-108">Item</span></span>                                                   | <span data-ttu-id="da5c0-109">Description</span><span class="sxs-lookup"><span data-stu-id="da5c0-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="da5c0-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="da5c0-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="da5c0-111">\[dans \] la valeur spécifiée, en radians.</span><span class="sxs-lookup"><span data-stu-id="da5c0-111">\[in\] The specified value, in radians.</span></span><br/> |
| <span data-ttu-id="da5c0-112"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="da5c0-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="da5c0-113">\[out \] retourne le sinus de x.</span><span class="sxs-lookup"><span data-stu-id="da5c0-113">\[out\] Returns the sine of x.</span></span><br/>          |
| <span data-ttu-id="da5c0-114"><span id="c"></span><span id="C"></span>*secteur*</span><span class="sxs-lookup"><span data-stu-id="da5c0-114"><span id="c"></span><span id="C"></span>*c*</span></span><br/> | <span data-ttu-id="da5c0-115">\[out \] retourne le cosinus de x.</span><span class="sxs-lookup"><span data-stu-id="da5c0-115">\[out\] Returns the cosine of x.</span></span><br/>        |



 

## <a name="return-value"></a><span data-ttu-id="da5c0-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="da5c0-116">Return Value</span></span>

<span data-ttu-id="da5c0-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="da5c0-117">None.</span></span>

## <a name="type-description"></a><span data-ttu-id="da5c0-118">Description du type</span><span class="sxs-lookup"><span data-stu-id="da5c0-118">Type Description</span></span>



| <span data-ttu-id="da5c0-119">Nom</span><span class="sxs-lookup"><span data-stu-id="da5c0-119">Name</span></span> | [<span data-ttu-id="da5c0-120">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="da5c0-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="da5c0-121">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="da5c0-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="da5c0-122">Taille</span><span class="sxs-lookup"><span data-stu-id="da5c0-122">Size</span></span>                           |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="da5c0-123">*x*</span><span class="sxs-lookup"><span data-stu-id="da5c0-123">*x*</span></span>  | <span data-ttu-id="da5c0-124">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="da5c0-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="da5c0-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="da5c0-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="da5c0-126">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="da5c0-126">any</span></span>                            |
| <span data-ttu-id="da5c0-127">*s*</span><span class="sxs-lookup"><span data-stu-id="da5c0-127">*s*</span></span>  | <span data-ttu-id="da5c0-128">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="da5c0-128">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="da5c0-129">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="da5c0-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="da5c0-130">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="da5c0-130">same dimension(s) as input *x*</span></span> |
| <span data-ttu-id="da5c0-131">c</span><span class="sxs-lookup"><span data-stu-id="da5c0-131">c</span></span>    | <span data-ttu-id="da5c0-132">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="da5c0-132">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="da5c0-133">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="da5c0-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="da5c0-134">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="da5c0-134">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="da5c0-135">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="da5c0-135">Minimum Shader Model</span></span>

<span data-ttu-id="da5c0-136">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="da5c0-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="da5c0-137">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="da5c0-137">Shader Model</span></span>                                                                       | <span data-ttu-id="da5c0-138">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="da5c0-138">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="da5c0-139">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="da5c0-139">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="da5c0-140">Oui</span><span class="sxs-lookup"><span data-stu-id="da5c0-140">yes</span></span>                 |
| [<span data-ttu-id="da5c0-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="da5c0-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="da5c0-142">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="da5c0-142">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="da5c0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da5c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da5c0-144">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="da5c0-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

