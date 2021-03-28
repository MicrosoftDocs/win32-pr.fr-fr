---
title: asin
description: Retourne l’arc sinus de la valeur spécifiée.
ms.assetid: 49559cb2-3305-4c97-8071-1589bcca3a75
keywords:
- sinus HLSL
topic_type:
- apiref
api_name:
- asin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2f64865cb3172037f6630dc422a69aa4d135b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031796"
---
# <a name="asin"></a><span data-ttu-id="5e41e-104">asin</span><span class="sxs-lookup"><span data-stu-id="5e41e-104">asin</span></span>

<span data-ttu-id="5e41e-105">Retourne l’arc sinus de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5e41e-105">Returns the arcsine of the specified value.</span></span>



| <span data-ttu-id="5e41e-106">*RET* ASIN (*x*)</span><span class="sxs-lookup"><span data-stu-id="5e41e-106">*ret* asin(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="5e41e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e41e-107">Parameters</span></span>



| <span data-ttu-id="5e41e-108">Élément</span><span class="sxs-lookup"><span data-stu-id="5e41e-108">Item</span></span>                                                   | <span data-ttu-id="5e41e-109">Description</span><span class="sxs-lookup"><span data-stu-id="5e41e-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="5e41e-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="5e41e-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="5e41e-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5e41e-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5e41e-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5e41e-112">Return Value</span></span>

<span data-ttu-id="5e41e-113">Arcsinus du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="5e41e-113">The arcsine of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e41e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5e41e-114">Remarks</span></span>

<span data-ttu-id="5e41e-115">Chaque composant du paramètre *x* doit être compris entre-π/2 et π/2.</span><span class="sxs-lookup"><span data-stu-id="5e41e-115">Each component of the *x* parameter should be within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="5e41e-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="5e41e-116">Type Description</span></span>



| <span data-ttu-id="5e41e-117">Nom</span><span class="sxs-lookup"><span data-stu-id="5e41e-117">Name</span></span>  | [<span data-ttu-id="5e41e-118">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="5e41e-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="5e41e-119">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="5e41e-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="5e41e-120">Taille</span><span class="sxs-lookup"><span data-stu-id="5e41e-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="5e41e-121">*x*</span><span class="sxs-lookup"><span data-stu-id="5e41e-121">*x*</span></span>   | <span data-ttu-id="5e41e-122">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="5e41e-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="5e41e-123">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="5e41e-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5e41e-124">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="5e41e-124">any</span></span>                            |
| <span data-ttu-id="5e41e-125">*Av*</span><span class="sxs-lookup"><span data-stu-id="5e41e-125">*ret*</span></span> | <span data-ttu-id="5e41e-126">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="5e41e-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="5e41e-127">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="5e41e-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5e41e-128">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="5e41e-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5e41e-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5e41e-129">Minimum Shader Model</span></span>

<span data-ttu-id="5e41e-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5e41e-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5e41e-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5e41e-131">Shader Model</span></span>                                                                       | <span data-ttu-id="5e41e-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5e41e-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5e41e-133">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="5e41e-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="5e41e-134">Oui</span><span class="sxs-lookup"><span data-stu-id="5e41e-134">yes</span></span>       |
| [<span data-ttu-id="5e41e-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5e41e-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="5e41e-136">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5e41e-136">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="5e41e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e41e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e41e-138">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="5e41e-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

