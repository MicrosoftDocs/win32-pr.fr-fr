---
title: modf, (Corecrt \_ Math. h)
description: Fractionne la valeur x en parties fractionnaires et entières, chacune ayant le même signe que x.
ms.assetid: 0cac1cf3-f0da-4b0a-ba30-4af5d65b04b2
keywords:
- HLSL modf,
topic_type:
- apiref
api_name:
- modf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5079549e70414f8237fd33a5e263dd8f17dcb9e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953893"
---
# <a name="modf"></a><span data-ttu-id="54bc8-104">modf</span><span class="sxs-lookup"><span data-stu-id="54bc8-104">modf</span></span>

<span data-ttu-id="54bc8-105">Fractionne la valeur x en parties fractionnaires et entières, chacune ayant le même signe que x.</span><span class="sxs-lookup"><span data-stu-id="54bc8-105">Splits the value x into fractional and integer parts, each of which has the same sign as x.</span></span>



| <span data-ttu-id="54bc8-106">RET modf, (x, adresse IP out)</span><span class="sxs-lookup"><span data-stu-id="54bc8-106">ret modf(x, out ip)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="54bc8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54bc8-107">Parameters</span></span>



| <span data-ttu-id="54bc8-108">Élément</span><span class="sxs-lookup"><span data-stu-id="54bc8-108">Item</span></span>                                                      | <span data-ttu-id="54bc8-109">Description</span><span class="sxs-lookup"><span data-stu-id="54bc8-109">Description</span></span>                                    |
|-----------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="54bc8-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="54bc8-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/>    | <span data-ttu-id="54bc8-111">\[dans \] la valeur d’entrée x.</span><span class="sxs-lookup"><span data-stu-id="54bc8-111">\[in\] The x input value.</span></span><br/>           |
| <span data-ttu-id="54bc8-112"><span id="ip"></span><span id="IP"></span>*adressesIP*</span><span class="sxs-lookup"><span data-stu-id="54bc8-112"><span id="ip"></span><span id="IP"></span>*ip*</span></span><br/> | <span data-ttu-id="54bc8-113">\[\]partie entière de *x*.</span><span class="sxs-lookup"><span data-stu-id="54bc8-113">\[out\] The integer portion of *x*.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="54bc8-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="54bc8-114">Return Value</span></span>

<span data-ttu-id="54bc8-115">Partie décimale signée de x.</span><span class="sxs-lookup"><span data-stu-id="54bc8-115">The signed-fractional portion of x.</span></span>

## <a name="type-description"></a><span data-ttu-id="54bc8-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="54bc8-116">Type Description</span></span>



| <span data-ttu-id="54bc8-117">Nom</span><span class="sxs-lookup"><span data-stu-id="54bc8-117">Name</span></span> | <span data-ttu-id="54bc8-118">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="54bc8-118">In/Out</span></span> | [<span data-ttu-id="54bc8-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="54bc8-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="54bc8-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="54bc8-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="54bc8-121">Taille</span><span class="sxs-lookup"><span data-stu-id="54bc8-121">Size</span></span>                         |
|------|--------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="54bc8-122">x</span><span class="sxs-lookup"><span data-stu-id="54bc8-122">x</span></span>    | <span data-ttu-id="54bc8-123">in</span><span class="sxs-lookup"><span data-stu-id="54bc8-123">in</span></span>     | <span data-ttu-id="54bc8-124">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="54bc8-124">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="54bc8-125">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="54bc8-125">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="54bc8-126">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="54bc8-126">any</span></span>                          |
| <span data-ttu-id="54bc8-127">ip</span><span class="sxs-lookup"><span data-stu-id="54bc8-127">ip</span></span>   | <span data-ttu-id="54bc8-128">out</span><span class="sxs-lookup"><span data-stu-id="54bc8-128">out</span></span>    | <span data-ttu-id="54bc8-129">identique à l’entrée x</span><span class="sxs-lookup"><span data-stu-id="54bc8-129">same as input x</span></span>                                                                                                | <span data-ttu-id="54bc8-130">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="54bc8-130">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="54bc8-131">la ou les mêmes dimensions comme entrée x</span><span class="sxs-lookup"><span data-stu-id="54bc8-131">same dimension(s) as input x</span></span> |
| <span data-ttu-id="54bc8-132">Av</span><span class="sxs-lookup"><span data-stu-id="54bc8-132">ret</span></span>  | <span data-ttu-id="54bc8-133">out</span><span class="sxs-lookup"><span data-stu-id="54bc8-133">out</span></span>    | <span data-ttu-id="54bc8-134">identique à l’entrée x</span><span class="sxs-lookup"><span data-stu-id="54bc8-134">same as input x</span></span>                                                                                                | <span data-ttu-id="54bc8-135">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="54bc8-135">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="54bc8-136">la ou les mêmes dimensions comme entrée x</span><span class="sxs-lookup"><span data-stu-id="54bc8-136">same dimension(s) as input x</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="54bc8-137">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="54bc8-137">Minimum Shader Model</span></span>

<span data-ttu-id="54bc8-138">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="54bc8-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="54bc8-139">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="54bc8-139">Shader Model</span></span>                                                                       | <span data-ttu-id="54bc8-140">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="54bc8-140">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="54bc8-141">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="54bc8-141">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="54bc8-142">Oui</span><span class="sxs-lookup"><span data-stu-id="54bc8-142">yes</span></span>                 |
| [<span data-ttu-id="54bc8-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54bc8-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="54bc8-144">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="54bc8-144">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="54bc8-145">Spécifications</span><span class="sxs-lookup"><span data-stu-id="54bc8-145">Requirements</span></span>



| <span data-ttu-id="54bc8-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54bc8-146">Requirement</span></span> | <span data-ttu-id="54bc8-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="54bc8-147">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="54bc8-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="54bc8-148">Header</span></span><br/> | <dl> <span data-ttu-id="54bc8-149"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="54bc8-149"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54bc8-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54bc8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54bc8-151">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="54bc8-151">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

