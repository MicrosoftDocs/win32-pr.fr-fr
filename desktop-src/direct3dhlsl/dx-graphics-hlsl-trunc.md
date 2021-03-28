---
title: trunc (Corecrt \_ Math. h)
description: Tronque une valeur à virgule flottante en composant entier.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- trunc HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992236"
---
# <a name="trunc"></a><span data-ttu-id="01455-104">trunc</span><span class="sxs-lookup"><span data-stu-id="01455-104">trunc</span></span>

<span data-ttu-id="01455-105">Tronque une valeur à virgule flottante en composant entier.</span><span class="sxs-lookup"><span data-stu-id="01455-105">Truncates a floating-point value to the integer component.</span></span>



| <span data-ttu-id="01455-106">RET trunc (*x*)</span><span class="sxs-lookup"><span data-stu-id="01455-106">ret trunc(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="01455-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01455-107">Parameters</span></span>



| <span data-ttu-id="01455-108">Élément</span><span class="sxs-lookup"><span data-stu-id="01455-108">Item</span></span>                                                   | <span data-ttu-id="01455-109">Description</span><span class="sxs-lookup"><span data-stu-id="01455-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="01455-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="01455-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="01455-111">\[dans \] l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="01455-111">\[in\] The specified input.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="01455-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="01455-112">Return Value</span></span>

<span data-ttu-id="01455-113">La valeur d’entrée est tronquée à un composant entier.</span><span class="sxs-lookup"><span data-stu-id="01455-113">The input value truncated to an integer component.</span></span>

## <a name="remarks"></a><span data-ttu-id="01455-114">Notes</span><span class="sxs-lookup"><span data-stu-id="01455-114">Remarks</span></span>

<span data-ttu-id="01455-115">Cette fonction tronque une valeur à virgule flottante au composant entier.</span><span class="sxs-lookup"><span data-stu-id="01455-115">This function truncates a floating-point value to the integer component.</span></span> <span data-ttu-id="01455-116">Étant donné une valeur à virgule flottante de 1,6, la fonction trunc retourne 1,0, où la fonction [**Round (DirectX HLSL)**](dx-graphics-hlsl-round.md) retourne 2,0.</span><span class="sxs-lookup"><span data-stu-id="01455-116">Given a floating-point value of 1.6, the trunc function would return 1.0, where as the [**round (DirectX HLSL)**](dx-graphics-hlsl-round.md) function would return 2.0.</span></span>

## <a name="type-description"></a><span data-ttu-id="01455-117">Description du type</span><span class="sxs-lookup"><span data-stu-id="01455-117">Type Description</span></span>



| <span data-ttu-id="01455-118">Nom</span><span class="sxs-lookup"><span data-stu-id="01455-118">Name</span></span> | [<span data-ttu-id="01455-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="01455-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="01455-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="01455-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="01455-121">Taille</span><span class="sxs-lookup"><span data-stu-id="01455-121">Size</span></span>                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="01455-122">*x*</span><span class="sxs-lookup"><span data-stu-id="01455-122">*x*</span></span>  | <span data-ttu-id="01455-123">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="01455-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="01455-124">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="01455-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="01455-125">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="01455-125">any</span></span>                          |
| <span data-ttu-id="01455-126">Av</span><span class="sxs-lookup"><span data-stu-id="01455-126">ret</span></span>  | <span data-ttu-id="01455-127">Même type que l’entrée x</span><span class="sxs-lookup"><span data-stu-id="01455-127">Same type as input x</span></span>                                                                                           | [<span data-ttu-id="01455-128">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="01455-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="01455-129">La ou les mêmes dimensions comme entrée x</span><span class="sxs-lookup"><span data-stu-id="01455-129">Same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="01455-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="01455-130">Minimum Shader Model</span></span>

<span data-ttu-id="01455-131">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="01455-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="01455-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="01455-132">Shader Model</span></span>                                                                       | <span data-ttu-id="01455-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="01455-133">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="01455-134">[Nuancier Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="01455-134">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="01455-135">Oui</span><span class="sxs-lookup"><span data-stu-id="01455-135">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="01455-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="01455-136">Requirements</span></span>



| <span data-ttu-id="01455-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01455-137">Requirement</span></span> | <span data-ttu-id="01455-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="01455-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="01455-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="01455-139">Header</span></span><br/> | <dl> <span data-ttu-id="01455-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="01455-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01455-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01455-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01455-142">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="01455-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

