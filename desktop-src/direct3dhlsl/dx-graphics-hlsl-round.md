---
title: Round (Corecrt \_ Math. h)
description: Arrondit la valeur spécifiée à l’entier le plus proche.
ms.assetid: 258ce717-dca1-4ed2-ad98-1ecfdb58f939
keywords:
- rondes HLSL
topic_type:
- apiref
api_name:
- round
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00bf845dfe16a92729b523fba62f6fd6dcde2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953892"
---
# <a name="round"></a><span data-ttu-id="d410b-104">round</span><span class="sxs-lookup"><span data-stu-id="d410b-104">round</span></span>

<span data-ttu-id="d410b-105">Arrondit la valeur spécifiée à l’entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="d410b-105">Rounds the specified value to the nearest integer.</span></span> <span data-ttu-id="d410b-106">Les cas à mi-chemin sont arrondis au pair le plus proche.</span><span class="sxs-lookup"><span data-stu-id="d410b-106">Halfway cases are rounded to the nearest even.</span></span>



| <span data-ttu-id="d410b-107">*RET* . aller-retour (*x*)</span><span class="sxs-lookup"><span data-stu-id="d410b-107">*ret* round(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="d410b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d410b-108">Parameters</span></span>



| <span data-ttu-id="d410b-109">Élément</span><span class="sxs-lookup"><span data-stu-id="d410b-109">Item</span></span>                                                   | <span data-ttu-id="d410b-110">Description</span><span class="sxs-lookup"><span data-stu-id="d410b-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="d410b-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d410b-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d410b-112">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d410b-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d410b-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d410b-113">Return Value</span></span>

<span data-ttu-id="d410b-114">Paramètre *x* , arrondi à l’entier le plus proche dans un type à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d410b-114">The *x* parameter, rounded to the nearest integer within a floating-point type.</span></span>

## <a name="type-description"></a><span data-ttu-id="d410b-115">Description du type</span><span class="sxs-lookup"><span data-stu-id="d410b-115">Type Description</span></span>



| <span data-ttu-id="d410b-116">Nom</span><span class="sxs-lookup"><span data-stu-id="d410b-116">Name</span></span>  | [<span data-ttu-id="d410b-117">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="d410b-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d410b-118">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="d410b-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d410b-119">Taille</span><span class="sxs-lookup"><span data-stu-id="d410b-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d410b-120">*x*</span><span class="sxs-lookup"><span data-stu-id="d410b-120">*x*</span></span>   | <span data-ttu-id="d410b-121">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="d410b-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d410b-122">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d410b-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d410b-123">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="d410b-123">any</span></span>                            |
| <span data-ttu-id="d410b-124">*Av*</span><span class="sxs-lookup"><span data-stu-id="d410b-124">*ret*</span></span> | <span data-ttu-id="d410b-125">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="d410b-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d410b-126">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d410b-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d410b-127">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="d410b-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d410b-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d410b-128">Minimum Shader Model</span></span>

<span data-ttu-id="d410b-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d410b-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d410b-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d410b-130">Shader Model</span></span>                                                                       | <span data-ttu-id="d410b-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d410b-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="d410b-132">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="d410b-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d410b-133">Oui</span><span class="sxs-lookup"><span data-stu-id="d410b-133">yes</span></span>                 |
| [<span data-ttu-id="d410b-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d410b-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d410b-135">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="d410b-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d410b-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d410b-136">Requirements</span></span>



| <span data-ttu-id="d410b-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d410b-137">Requirement</span></span> | <span data-ttu-id="d410b-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="d410b-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d410b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="d410b-139">Header</span></span><br/> | <dl> <span data-ttu-id="d410b-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d410b-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d410b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d410b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d410b-142">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d410b-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

