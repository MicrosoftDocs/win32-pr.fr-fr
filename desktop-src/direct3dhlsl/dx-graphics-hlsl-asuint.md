---
title: asuint
description: Interprète le modèle binaire de x comme un entier non signé.
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- HLSL asuint
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a2d351eb36c6910790e2dceb94e3a97951ad850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971771"
---
# <a name="asuint"></a><span data-ttu-id="8bd3f-104">asuint</span><span class="sxs-lookup"><span data-stu-id="8bd3f-104">asuint</span></span>

<span data-ttu-id="8bd3f-105">Interprète le modèle binaire de *x* comme un entier non signé.</span><span class="sxs-lookup"><span data-stu-id="8bd3f-105">Interprets the bit pattern of *x* as an unsigned integer.</span></span>



| <span data-ttu-id="8bd3f-106">RET asuint (*x*)</span><span class="sxs-lookup"><span data-stu-id="8bd3f-106">ret asuint(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="8bd3f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bd3f-107">Parameters</span></span>



| <span data-ttu-id="8bd3f-108">Élément</span><span class="sxs-lookup"><span data-stu-id="8bd3f-108">Item</span></span>                                                   | <span data-ttu-id="8bd3f-109">Description</span><span class="sxs-lookup"><span data-stu-id="8bd3f-109">Description</span></span>                        |
|--------------------------------------------------------|------------------------------------|
| <span data-ttu-id="8bd3f-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="8bd3f-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8bd3f-111">\[dans \] la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8bd3f-111">\[in\] The input value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8bd3f-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8bd3f-112">Return Value</span></span>

<span data-ttu-id="8bd3f-113">Entrée interprétée comme un entier non signé.</span><span class="sxs-lookup"><span data-stu-id="8bd3f-113">The input interpreted as an unsigned integer.</span></span>

## <a name="type-description"></a><span data-ttu-id="8bd3f-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="8bd3f-114">Type Description</span></span>



| <span data-ttu-id="8bd3f-115">Nom</span><span class="sxs-lookup"><span data-stu-id="8bd3f-115">Name</span></span>  | [<span data-ttu-id="8bd3f-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="8bd3f-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8bd3f-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="8bd3f-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="8bd3f-118">Taille</span><span class="sxs-lookup"><span data-stu-id="8bd3f-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8bd3f-119">*x*</span><span class="sxs-lookup"><span data-stu-id="8bd3f-119">*x*</span></span>   | <span data-ttu-id="8bd3f-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="8bd3f-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="8bd3f-121">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8bd3f-121">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="8bd3f-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="8bd3f-122">any</span></span>                            |
| <span data-ttu-id="8bd3f-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="8bd3f-123">*ret*</span></span> | <span data-ttu-id="8bd3f-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="8bd3f-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="8bd3f-125">**uint**</span><span class="sxs-lookup"><span data-stu-id="8bd3f-125">**uint**</span></span>](/windows/desktop/WinProg/windows-data-types)                                         | <span data-ttu-id="8bd3f-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="8bd3f-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8bd3f-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="8bd3f-127">Minimum Shader Model</span></span>

<span data-ttu-id="8bd3f-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="8bd3f-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8bd3f-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8bd3f-129">Shader Model</span></span>                                                        | <span data-ttu-id="8bd3f-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="8bd3f-130">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="8bd3f-131">[Nuancier modèle 4](dx-graphics-hlsl-sm4.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="8bd3f-131">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="8bd3f-132">Oui</span><span class="sxs-lookup"><span data-stu-id="8bd3f-132">yes</span></span>       |
| [<span data-ttu-id="8bd3f-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8bd3f-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="8bd3f-134">non</span><span class="sxs-lookup"><span data-stu-id="8bd3f-134">no</span></span>        |
| [<span data-ttu-id="8bd3f-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8bd3f-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="8bd3f-136">non</span><span class="sxs-lookup"><span data-stu-id="8bd3f-136">no</span></span>        |
| [<span data-ttu-id="8bd3f-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8bd3f-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="8bd3f-138">non</span><span class="sxs-lookup"><span data-stu-id="8bd3f-138">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="8bd3f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bd3f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bd3f-140">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8bd3f-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

