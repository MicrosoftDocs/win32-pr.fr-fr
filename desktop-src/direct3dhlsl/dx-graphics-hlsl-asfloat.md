---
title: asfloat
description: Interprète le modèle binaire de x comme un nombre à virgule flottante.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- HLSL asfloat
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990989"
---
# <a name="asfloat"></a><span data-ttu-id="f49f0-104">asfloat</span><span class="sxs-lookup"><span data-stu-id="f49f0-104">asfloat</span></span>

<span data-ttu-id="f49f0-105">Interprète le modèle binaire de *x* comme un nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="f49f0-105">Interprets the bit pattern of *x* as a floating-point number.</span></span>



| <span data-ttu-id="f49f0-106">RET asfloat (*x*)</span><span class="sxs-lookup"><span data-stu-id="f49f0-106">ret asfloat(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="f49f0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f49f0-107">Parameters</span></span>



| <span data-ttu-id="f49f0-108">Élément</span><span class="sxs-lookup"><span data-stu-id="f49f0-108">Item</span></span>                                                   | <span data-ttu-id="f49f0-109">Description</span><span class="sxs-lookup"><span data-stu-id="f49f0-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="f49f0-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="f49f0-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="f49f0-111">\[dans \] la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f49f0-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f49f0-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f49f0-112">Return Value</span></span>

<span data-ttu-id="f49f0-113">Entrée interprétée comme un nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="f49f0-113">The input interpreted as a floating-point number.</span></span>

## <a name="type-description"></a><span data-ttu-id="f49f0-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="f49f0-114">Type Description</span></span>



| <span data-ttu-id="f49f0-115">Nom</span><span class="sxs-lookup"><span data-stu-id="f49f0-115">Name</span></span>  | [<span data-ttu-id="f49f0-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="f49f0-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f49f0-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="f49f0-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="f49f0-118">Taille</span><span class="sxs-lookup"><span data-stu-id="f49f0-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="f49f0-119">*x*</span><span class="sxs-lookup"><span data-stu-id="f49f0-119">*x*</span></span>   | <span data-ttu-id="f49f0-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="f49f0-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="f49f0-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f49f0-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="f49f0-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="f49f0-122">any</span></span>                            |
| <span data-ttu-id="f49f0-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="f49f0-123">*ret*</span></span> | <span data-ttu-id="f49f0-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="f49f0-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="f49f0-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="f49f0-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                | <span data-ttu-id="f49f0-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="f49f0-126">same dimension(s) as input *x*</span></span> |



 

## <a name="function-overloads"></a><span data-ttu-id="f49f0-127">Surcharges de fonction</span><span class="sxs-lookup"><span data-stu-id="f49f0-127">Function Overloads</span></span>

<dl> <span data-ttu-id="f49f0-128">'float <x> asfloat (valeur flottante <x> ); `  
` float <x> asfloat ( <x> valeur int); `  
` float <x> asfloat ( <x> valeur uint); '</span><span class="sxs-lookup"><span data-stu-id="f49f0-128">`float<x> asfloat(float<x> value);`  
`float<x> asfloat(int<x> value);`  
`float<x> asfloat(uint<x> value);`</span></span>
</dl>

## <a name="minimum-shader-model"></a><span data-ttu-id="f49f0-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f49f0-129">Minimum Shader Model</span></span>

<span data-ttu-id="f49f0-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f49f0-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f49f0-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f49f0-131">Shader Model</span></span>                                                        | <span data-ttu-id="f49f0-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f49f0-132">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="f49f0-133">[Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="f49f0-133">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="f49f0-134">Oui</span><span class="sxs-lookup"><span data-stu-id="f49f0-134">yes</span></span>       |
| [<span data-ttu-id="f49f0-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f49f0-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="f49f0-136">non</span><span class="sxs-lookup"><span data-stu-id="f49f0-136">no</span></span>        |
| [<span data-ttu-id="f49f0-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f49f0-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="f49f0-138">non</span><span class="sxs-lookup"><span data-stu-id="f49f0-138">no</span></span>        |
| [<span data-ttu-id="f49f0-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f49f0-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="f49f0-140">non</span><span class="sxs-lookup"><span data-stu-id="f49f0-140">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="f49f0-141">Notes</span><span class="sxs-lookup"><span data-stu-id="f49f0-141">Remarks</span></span>

<span data-ttu-id="f49f0-142">Les compilateurs plus anciens ne `asfloat(bool)` sont pas correctement autorisés, mais notez que les entrées bool ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f49f0-142">Older compilers incorrectly allowed `asfloat(bool)`, but note that bool inputs are not supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="f49f0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f49f0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f49f0-144">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f49f0-144">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

