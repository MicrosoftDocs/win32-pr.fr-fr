---
title: ceil (Corecrt \_ Math. h)
description: Retourne la plus petite valeur entière qui est supérieure ou égale à la valeur spécifiée.
ms.assetid: 9823f321-14c3-4b27-9a4b-7a885cece39b
keywords:
- HLSL ceil
topic_type:
- apiref
api_name:
- ceil
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec86db320119b7f162ed48a748c1d1ff4335b6f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992169"
---
# <a name="ceil"></a><span data-ttu-id="8517c-104">ceil</span><span class="sxs-lookup"><span data-stu-id="8517c-104">ceil</span></span>

<span data-ttu-id="8517c-105">Retourne la plus petite valeur entière qui est supérieure ou égale à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8517c-105">Returns the smallest integer value that is greater than or equal to the specified value.</span></span>



| <span data-ttu-id="8517c-106">*RET* ceil (*x*)</span><span class="sxs-lookup"><span data-stu-id="8517c-106">*ret* ceil(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="8517c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8517c-107">Parameters</span></span>



| <span data-ttu-id="8517c-108">Élément</span><span class="sxs-lookup"><span data-stu-id="8517c-108">Item</span></span>                                                   | <span data-ttu-id="8517c-109">Description</span><span class="sxs-lookup"><span data-stu-id="8517c-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="8517c-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="8517c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8517c-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8517c-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8517c-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8517c-112">Return Value</span></span>

<span data-ttu-id="8517c-113">Plus petite valeur entière (retournée en tant que type à virgule flottante) supérieure ou égale au paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="8517c-113">The smallest integer value (returned as a floating-point type) that is greater than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="8517c-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="8517c-114">Type Description</span></span>



| <span data-ttu-id="8517c-115">Nom</span><span class="sxs-lookup"><span data-stu-id="8517c-115">Name</span></span>  | [<span data-ttu-id="8517c-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="8517c-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8517c-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="8517c-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8517c-118">Taille</span><span class="sxs-lookup"><span data-stu-id="8517c-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8517c-119">*x*</span><span class="sxs-lookup"><span data-stu-id="8517c-119">*x*</span></span>   | <span data-ttu-id="8517c-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="8517c-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="8517c-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="8517c-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8517c-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="8517c-122">any</span></span>                            |
| <span data-ttu-id="8517c-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="8517c-123">*ret*</span></span> | <span data-ttu-id="8517c-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="8517c-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="8517c-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="8517c-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8517c-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="8517c-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8517c-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="8517c-127">Minimum Shader Model</span></span>

<span data-ttu-id="8517c-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="8517c-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8517c-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8517c-129">Shader Model</span></span>                                                                       | <span data-ttu-id="8517c-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="8517c-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8517c-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="8517c-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="8517c-132">Oui</span><span class="sxs-lookup"><span data-stu-id="8517c-132">yes</span></span>       |
| [<span data-ttu-id="8517c-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8517c-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8517c-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8517c-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="8517c-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8517c-135">Requirements</span></span>



| <span data-ttu-id="8517c-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8517c-136">Requirement</span></span> | <span data-ttu-id="8517c-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="8517c-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8517c-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="8517c-138">Header</span></span><br/> | <dl> <span data-ttu-id="8517c-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8517c-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8517c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8517c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8517c-141">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8517c-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

