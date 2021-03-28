---
title: EXP2 (Corecrt \_ Math. h)
description: Retourne la valeur exponentielle de base 2, ou 2x, de la valeur spécifiée.
ms.assetid: 68b0057c-864d-440b-84f6-781d5fa3b019
keywords:
- HLSL EXP2
topic_type:
- apiref
api_name:
- exp2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63aaf5ee7c29da49ca2e7b21d80af6967721058d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974502"
---
# <a name="exp2"></a><span data-ttu-id="7b759-104">EXP2</span><span class="sxs-lookup"><span data-stu-id="7b759-104">exp2</span></span>

<span data-ttu-id="7b759-105">Retourne la valeur exponentielle de base 2, ou 2<sup>x</sup>, de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7b759-105">Returns the base 2 exponential, or 2<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="7b759-106">*RET* EXP2 (*x*)</span><span class="sxs-lookup"><span data-stu-id="7b759-106">*ret* exp2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="7b759-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b759-107">Parameters</span></span>



| <span data-ttu-id="7b759-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7b759-108">Item</span></span>                                                   | <span data-ttu-id="7b759-109">Description</span><span class="sxs-lookup"><span data-stu-id="7b759-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="7b759-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="7b759-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="7b759-111">\[dans \] la valeur à virgule flottante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7b759-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7b759-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7b759-112">Return Value</span></span>

<span data-ttu-id="7b759-113">Valeur exponentielle de base 2 du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="7b759-113">The base 2 exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="7b759-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="7b759-114">Type Description</span></span>



| <span data-ttu-id="7b759-115">Nom</span><span class="sxs-lookup"><span data-stu-id="7b759-115">Name</span></span>  | [<span data-ttu-id="7b759-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="7b759-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7b759-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="7b759-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7b759-118">Taille</span><span class="sxs-lookup"><span data-stu-id="7b759-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7b759-119">*x*</span><span class="sxs-lookup"><span data-stu-id="7b759-119">*x*</span></span>   | <span data-ttu-id="7b759-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="7b759-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="7b759-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="7b759-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7b759-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="7b759-122">any</span></span>                            |
| <span data-ttu-id="7b759-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="7b759-123">*ret*</span></span> | <span data-ttu-id="7b759-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="7b759-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="7b759-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="7b759-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7b759-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="7b759-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7b759-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="7b759-127">Minimum Shader Model</span></span>

<span data-ttu-id="7b759-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="7b759-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7b759-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="7b759-129">Shader Model</span></span>                                                                       | <span data-ttu-id="7b759-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="7b759-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7b759-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="7b759-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="7b759-132">Oui</span><span class="sxs-lookup"><span data-stu-id="7b759-132">yes</span></span>       |
| [<span data-ttu-id="7b759-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7b759-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="7b759-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="7b759-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="7b759-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7b759-135">Requirements</span></span>



| <span data-ttu-id="7b759-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b759-136">Requirement</span></span> | <span data-ttu-id="7b759-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b759-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b759-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b759-138">Header</span></span><br/> | <dl> <span data-ttu-id="7b759-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b759-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b759-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b759-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b759-141">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7b759-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

