---
title: Floor (Corecrt \_ Math. h)
description: Retourne le plus grand entier qui est inférieur ou égal à la valeur spécifiée.
ms.assetid: f7193425-2448-4ae6-99d5-bb5e1aa74111
keywords:
- HLSL Floor
topic_type:
- apiref
api_name:
- floor
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ecb46719d5361ec9f7c36b21d94793bc9a67ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974499"
---
# <a name="floor"></a><span data-ttu-id="a9a51-104">floor</span><span class="sxs-lookup"><span data-stu-id="a9a51-104">floor</span></span>

<span data-ttu-id="a9a51-105">Retourne le plus grand entier qui est inférieur ou égal à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a9a51-105">Returns the largest integer that is less than or equal to the specified value.</span></span>



| <span data-ttu-id="a9a51-106">*RET* Floor (*x*)</span><span class="sxs-lookup"><span data-stu-id="a9a51-106">*ret* floor(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="a9a51-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9a51-107">Parameters</span></span>



| <span data-ttu-id="a9a51-108">Élément</span><span class="sxs-lookup"><span data-stu-id="a9a51-108">Item</span></span>                                                   | <span data-ttu-id="a9a51-109">Description</span><span class="sxs-lookup"><span data-stu-id="a9a51-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="a9a51-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="a9a51-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a9a51-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a9a51-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a9a51-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a9a51-112">Return Value</span></span>

<span data-ttu-id="a9a51-113">Plus grande valeur entière (retournée en tant que type à virgule flottante) inférieure ou égale au paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="a9a51-113">The largest integer value (returned as a floating-point type) that is less than or equal to the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="a9a51-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="a9a51-114">Type Description</span></span>



| <span data-ttu-id="a9a51-115">Nom</span><span class="sxs-lookup"><span data-stu-id="a9a51-115">Name</span></span>  | [<span data-ttu-id="a9a51-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="a9a51-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="a9a51-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="a9a51-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a9a51-118">Taille</span><span class="sxs-lookup"><span data-stu-id="a9a51-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="a9a51-119">*x*</span><span class="sxs-lookup"><span data-stu-id="a9a51-119">*x*</span></span>   | <span data-ttu-id="a9a51-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="a9a51-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="a9a51-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="a9a51-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a9a51-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="a9a51-122">any</span></span>                            |
| <span data-ttu-id="a9a51-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="a9a51-123">*ret*</span></span> | <span data-ttu-id="a9a51-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="a9a51-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="a9a51-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="a9a51-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a9a51-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="a9a51-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a9a51-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="a9a51-127">Minimum Shader Model</span></span>

<span data-ttu-id="a9a51-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="a9a51-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a9a51-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="a9a51-129">Shader Model</span></span>                                                                       | <span data-ttu-id="a9a51-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="a9a51-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a9a51-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="a9a51-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="a9a51-132">Oui</span><span class="sxs-lookup"><span data-stu-id="a9a51-132">yes</span></span>       |
| [<span data-ttu-id="a9a51-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9a51-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="a9a51-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="a9a51-134">vs\_1\_1</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="a9a51-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a9a51-135">Requirements</span></span>



| <span data-ttu-id="a9a51-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9a51-136">Requirement</span></span> | <span data-ttu-id="a9a51-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9a51-137">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a51-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9a51-138">Header</span></span><br/> | <dl> <span data-ttu-id="a9a51-139"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9a51-139"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a51-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9a51-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a51-141">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a9a51-141">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

