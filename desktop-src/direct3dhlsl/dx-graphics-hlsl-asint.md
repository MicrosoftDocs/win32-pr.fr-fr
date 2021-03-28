---
title: asint
description: Interprète le modèle binaire de x comme un entier.
ms.assetid: e17e0a11-ef52-4b23-94b8-5db0b18aff4d
keywords:
- HLSL asint
topic_type:
- apiref
api_name:
- asint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1b0ca7e1c7b3716be1a3029c5478f96e261ce5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031630"
---
# <a name="asint"></a><span data-ttu-id="7d4a6-104">asint</span><span class="sxs-lookup"><span data-stu-id="7d4a6-104">asint</span></span>

<span data-ttu-id="7d4a6-105">Interprète le modèle binaire de *x* comme un entier.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-105">Interprets the bit pattern of *x* as an integer.</span></span>



| <span data-ttu-id="7d4a6-106">RET asint (*x*)</span><span class="sxs-lookup"><span data-stu-id="7d4a6-106">ret asint(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="7d4a6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d4a6-107">Parameters</span></span>



| <span data-ttu-id="7d4a6-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7d4a6-108">Item</span></span>                                                   | <span data-ttu-id="7d4a6-109">Description</span><span class="sxs-lookup"><span data-stu-id="7d4a6-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="7d4a6-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="7d4a6-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="7d4a6-111">\[dans \] la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7d4a6-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7d4a6-112">Return Value</span></span>

<span data-ttu-id="7d4a6-113">Entrée interprétée comme un entier.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-113">The input interpreted as an integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="7d4a6-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="7d4a6-114">Type Description</span></span>



| <span data-ttu-id="7d4a6-115">Nom</span><span class="sxs-lookup"><span data-stu-id="7d4a6-115">Name</span></span>  | [<span data-ttu-id="7d4a6-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="7d4a6-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7d4a6-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="7d4a6-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                  | <span data-ttu-id="7d4a6-118">Taille</span><span class="sxs-lookup"><span data-stu-id="7d4a6-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7d4a6-119">*x*</span><span class="sxs-lookup"><span data-stu-id="7d4a6-119">*x*</span></span>   | <span data-ttu-id="7d4a6-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="7d4a6-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="7d4a6-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **uint**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7d4a6-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="7d4a6-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="7d4a6-122">any</span></span>                            |
| <span data-ttu-id="7d4a6-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="7d4a6-123">*ret*</span></span> | <span data-ttu-id="7d4a6-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="7d4a6-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="7d4a6-125">**int**</span><span class="sxs-lookup"><span data-stu-id="7d4a6-125">**int**</span></span>](/windows/desktop/WinProg/windows-data-types)                                           | <span data-ttu-id="7d4a6-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="7d4a6-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7d4a6-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="7d4a6-127">Minimum Shader Model</span></span>

<span data-ttu-id="7d4a6-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="7d4a6-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7d4a6-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="7d4a6-129">Shader Model</span></span>                                                        | <span data-ttu-id="7d4a6-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="7d4a6-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="7d4a6-131">[Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="7d4a6-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="7d4a6-132">Oui</span><span class="sxs-lookup"><span data-stu-id="7d4a6-132">yes</span></span>       |
| [<span data-ttu-id="7d4a6-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d4a6-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="7d4a6-134">non</span><span class="sxs-lookup"><span data-stu-id="7d4a6-134">no</span></span>        |
| [<span data-ttu-id="7d4a6-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d4a6-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="7d4a6-136">non</span><span class="sxs-lookup"><span data-stu-id="7d4a6-136">no</span></span>        |
| [<span data-ttu-id="7d4a6-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d4a6-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="7d4a6-138">non</span><span class="sxs-lookup"><span data-stu-id="7d4a6-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="7d4a6-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d4a6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d4a6-140">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7d4a6-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

