---
title: isFinite, (Corecrt \_ Math. h)
description: Détermine si la valeur à virgule flottante spécifiée est finie.
ms.assetid: 8be10499-2d06-4520-9697-dab2f461bd0d
keywords:
- HLSL isFinite,
topic_type:
- apiref
api_name:
- isfinite
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c943dadccad9f485668948f366698f3bce5e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992189"
---
# <a name="isfinite"></a><span data-ttu-id="95185-104">isFinite,</span><span class="sxs-lookup"><span data-stu-id="95185-104">isfinite</span></span>

<span data-ttu-id="95185-105">Détermine si la valeur à virgule flottante spécifiée est finie.</span><span class="sxs-lookup"><span data-stu-id="95185-105">Determines if the specified floating-point value is finite.</span></span>



| <span data-ttu-id="95185-106">*RET* isFinite, (*x*)</span><span class="sxs-lookup"><span data-stu-id="95185-106">*ret* isfinite(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="95185-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95185-107">Parameters</span></span>



| <span data-ttu-id="95185-108">Élément</span><span class="sxs-lookup"><span data-stu-id="95185-108">Item</span></span>                                                   | <span data-ttu-id="95185-109">Description</span><span class="sxs-lookup"><span data-stu-id="95185-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="95185-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="95185-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="95185-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="95185-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="95185-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="95185-112">Return Value</span></span>

<span data-ttu-id="95185-113">Retourne une valeur de la même taille que l’entrée, avec une valeur égale à **true** si le paramètre *x* est fini ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="95185-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is finite; otherwise **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="95185-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="95185-114">Type Description</span></span>



| <span data-ttu-id="95185-115">Nom</span><span class="sxs-lookup"><span data-stu-id="95185-115">Name</span></span>  | [<span data-ttu-id="95185-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="95185-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="95185-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="95185-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="95185-118">Taille</span><span class="sxs-lookup"><span data-stu-id="95185-118">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="95185-119">*x*</span><span class="sxs-lookup"><span data-stu-id="95185-119">*x*</span></span>   | <span data-ttu-id="95185-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="95185-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="95185-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="95185-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="95185-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="95185-122">any</span></span>      |
| <span data-ttu-id="95185-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="95185-123">*ret*</span></span> | <span data-ttu-id="95185-124">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="95185-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="95185-125">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="95185-125">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="95185-126">comme entrée</span><span class="sxs-lookup"><span data-stu-id="95185-126">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="95185-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="95185-127">Minimum Shader Model</span></span>

<span data-ttu-id="95185-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="95185-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="95185-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="95185-129">Shader Model</span></span>                                                                       | <span data-ttu-id="95185-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="95185-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="95185-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="95185-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="95185-132">Oui</span><span class="sxs-lookup"><span data-stu-id="95185-132">yes</span></span>                 |
| [<span data-ttu-id="95185-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95185-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="95185-134">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="95185-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="95185-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="95185-135">Requirements</span></span>



| <span data-ttu-id="95185-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95185-136">Requirement</span></span> | <span data-ttu-id="95185-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="95185-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="95185-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="95185-138">Header</span></span><br/> | <dl> <span data-ttu-id="95185-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="95185-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95185-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95185-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95185-141">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="95185-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

