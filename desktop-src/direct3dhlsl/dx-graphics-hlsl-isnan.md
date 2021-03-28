---
title: isNaN (Corecrt \_ Math. h)
description: Détermine si la valeur spécifiée est NAN ou QNAN.
ms.assetid: 09085634-e610-4793-848e-abda8241f1cc
keywords:
- langage HLSL IsNaN
topic_type:
- apiref
api_name:
- isnan
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9f4549b6a142f5bf6011cdfb144de92efde64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043176"
---
# <a name="isnan"></a><span data-ttu-id="ffe23-104">isNaN</span><span class="sxs-lookup"><span data-stu-id="ffe23-104">isnan</span></span>

<span data-ttu-id="ffe23-105">Détermine si la valeur spécifiée est NAN ou QNAN.</span><span class="sxs-lookup"><span data-stu-id="ffe23-105">Determines if the specified value is NAN or QNAN.</span></span>



| <span data-ttu-id="ffe23-106">*RET* IsNaN (*x*)</span><span class="sxs-lookup"><span data-stu-id="ffe23-106">*ret* isnan(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="ffe23-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffe23-107">Parameters</span></span>



| <span data-ttu-id="ffe23-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ffe23-108">Item</span></span>                                                   | <span data-ttu-id="ffe23-109">Description</span><span class="sxs-lookup"><span data-stu-id="ffe23-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="ffe23-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="ffe23-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ffe23-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ffe23-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ffe23-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ffe23-112">Return Value</span></span>

<span data-ttu-id="ffe23-113">Retourne une valeur de la même taille que l’entrée, avec une valeur égale à **true** si le paramètre *x* est NaN ou QNAN.</span><span class="sxs-lookup"><span data-stu-id="ffe23-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is NAN or QNAN.</span></span> <span data-ttu-id="ffe23-114">Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="ffe23-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="ffe23-115">Description du type</span><span class="sxs-lookup"><span data-stu-id="ffe23-115">Type Description</span></span>



| <span data-ttu-id="ffe23-116">Nom</span><span class="sxs-lookup"><span data-stu-id="ffe23-116">Name</span></span>  | [<span data-ttu-id="ffe23-117">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="ffe23-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ffe23-118">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="ffe23-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ffe23-119">Taille</span><span class="sxs-lookup"><span data-stu-id="ffe23-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="ffe23-120">*x*</span><span class="sxs-lookup"><span data-stu-id="ffe23-120">*x*</span></span>   | <span data-ttu-id="ffe23-121">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="ffe23-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ffe23-122">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="ffe23-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ffe23-123">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="ffe23-123">any</span></span>      |
| <span data-ttu-id="ffe23-124">*Av*</span><span class="sxs-lookup"><span data-stu-id="ffe23-124">*ret*</span></span> | <span data-ttu-id="ffe23-125">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="ffe23-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ffe23-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ffe23-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="ffe23-127">comme entrée</span><span class="sxs-lookup"><span data-stu-id="ffe23-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ffe23-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="ffe23-128">Minimum Shader Model</span></span>

<span data-ttu-id="ffe23-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="ffe23-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ffe23-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="ffe23-130">Shader Model</span></span>                                                                       | <span data-ttu-id="ffe23-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="ffe23-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="ffe23-132">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="ffe23-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ffe23-133">Oui</span><span class="sxs-lookup"><span data-stu-id="ffe23-133">yes</span></span>                 |
| [<span data-ttu-id="ffe23-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ffe23-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ffe23-135">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="ffe23-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ffe23-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ffe23-136">Requirements</span></span>



| <span data-ttu-id="ffe23-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffe23-137">Requirement</span></span> | <span data-ttu-id="ffe23-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffe23-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe23-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffe23-139">Header</span></span><br/> | <dl> <span data-ttu-id="ffe23-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffe23-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffe23-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffe23-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe23-142">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ffe23-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

