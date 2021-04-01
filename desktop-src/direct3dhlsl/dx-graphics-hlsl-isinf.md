---
title: isinf, (Corecrt \_ Math. h)
description: Détermine si la valeur spécifiée est infinie.
ms.assetid: 2028dc5a-e48b-4081-a0ec-35901113aab6
keywords:
- HLSL isinf,
topic_type:
- apiref
api_name:
- isinf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4df738438d62d5a66dd3b08ad769d475df562d5f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211830"
---
# <a name="isinf"></a><span data-ttu-id="acb24-104">isinf</span><span class="sxs-lookup"><span data-stu-id="acb24-104">isinf</span></span>

<span data-ttu-id="acb24-105">Détermine si la valeur spécifiée est infinie.</span><span class="sxs-lookup"><span data-stu-id="acb24-105">Determines if the specified value is infinite.</span></span>



| <span data-ttu-id="acb24-106">*RET* isinf, (*x*)</span><span class="sxs-lookup"><span data-stu-id="acb24-106">*ret* isinf(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="acb24-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acb24-107">Parameters</span></span>



| <span data-ttu-id="acb24-108">Élément</span><span class="sxs-lookup"><span data-stu-id="acb24-108">Item</span></span>                                                   | <span data-ttu-id="acb24-109">Description</span><span class="sxs-lookup"><span data-stu-id="acb24-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="acb24-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="acb24-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="acb24-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="acb24-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="acb24-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="acb24-112">Return Value</span></span>

<span data-ttu-id="acb24-113">Retourne une valeur de la même taille que l’entrée, avec une valeur égale à **true** si le paramètre *x* est + inf ou-INF.</span><span class="sxs-lookup"><span data-stu-id="acb24-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is +INF or -INF.</span></span> <span data-ttu-id="acb24-114">Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="acb24-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="acb24-115">Description du type</span><span class="sxs-lookup"><span data-stu-id="acb24-115">Type Description</span></span>



| <span data-ttu-id="acb24-116">Nom</span><span class="sxs-lookup"><span data-stu-id="acb24-116">Name</span></span>  | [<span data-ttu-id="acb24-117">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="acb24-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="acb24-118">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="acb24-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="acb24-119">Taille</span><span class="sxs-lookup"><span data-stu-id="acb24-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="acb24-120">*x*</span><span class="sxs-lookup"><span data-stu-id="acb24-120">*x*</span></span>   | <span data-ttu-id="acb24-121">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="acb24-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="acb24-122">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="acb24-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="acb24-123">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="acb24-123">any</span></span>      |
| <span data-ttu-id="acb24-124">*Av*</span><span class="sxs-lookup"><span data-stu-id="acb24-124">*ret*</span></span> | <span data-ttu-id="acb24-125">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="acb24-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="acb24-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="acb24-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="acb24-127">comme entrée</span><span class="sxs-lookup"><span data-stu-id="acb24-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="acb24-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="acb24-128">Minimum Shader Model</span></span>

<span data-ttu-id="acb24-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="acb24-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="acb24-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="acb24-130">Shader Model</span></span>                                                                       | <span data-ttu-id="acb24-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="acb24-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="acb24-132">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="acb24-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="acb24-133">Oui</span><span class="sxs-lookup"><span data-stu-id="acb24-133">yes</span></span>                 |
| [<span data-ttu-id="acb24-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="acb24-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="acb24-135">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="acb24-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="acb24-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="acb24-136">Requirements</span></span>



| <span data-ttu-id="acb24-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acb24-137">Requirement</span></span> | <span data-ttu-id="acb24-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="acb24-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="acb24-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="acb24-139">Header</span></span><br/> | <dl> <span data-ttu-id="acb24-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="acb24-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acb24-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acb24-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acb24-142">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="acb24-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

