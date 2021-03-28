---
title: fwidth
description: Retourne la valeur absolue des dérivées partielles de la valeur spécifiée.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- HLSL FWidth
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf2d5a34e1f387aadb3b044ddd1264616a61109b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102045"
---
# <a name="fwidth"></a><span data-ttu-id="4c279-104">fwidth</span><span class="sxs-lookup"><span data-stu-id="4c279-104">fwidth</span></span>

<span data-ttu-id="4c279-105">Retourne la valeur absolue des dérivées partielles de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4c279-105">Returns the absolute value of the partial derivatives of the specified value.</span></span>



| <span data-ttu-id="4c279-106">*RET* FWidth (*x*)</span><span class="sxs-lookup"><span data-stu-id="4c279-106">*ret* fwidth(*x*)</span></span> |
|-------------------|



 

<span data-ttu-id="4c279-107">Cette fonction calcule les éléments suivants : [**ABS**](dx-graphics-hlsl-abs.md)([**ddx**](dx-graphics-hlsl-ddx.md)(*x*)) + [**ABS**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).</span><span class="sxs-lookup"><span data-stu-id="4c279-107">This function computes the following: [**abs**](dx-graphics-hlsl-abs.md)([**ddx**](dx-graphics-hlsl-ddx.md)(*x*)) + [**abs**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).</span></span>

<span data-ttu-id="4c279-108">Cette fonction est prise en charge uniquement dans les nuanceurs de pixels.</span><span class="sxs-lookup"><span data-stu-id="4c279-108">This function is only supported in pixel shaders.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c279-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c279-109">Parameters</span></span>



| <span data-ttu-id="4c279-110">Élément</span><span class="sxs-lookup"><span data-stu-id="4c279-110">Item</span></span>                                                   | <span data-ttu-id="4c279-111">Description</span><span class="sxs-lookup"><span data-stu-id="4c279-111">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="4c279-112"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="4c279-112"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="4c279-113">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4c279-113">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4c279-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4c279-114">Return Value</span></span>

<span data-ttu-id="4c279-115">Valeur absolue des dérivées partielles du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="4c279-115">The absolute value of the partial derivatives of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="4c279-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="4c279-116">Type Description</span></span>



| <span data-ttu-id="4c279-117">Nom</span><span class="sxs-lookup"><span data-stu-id="4c279-117">Name</span></span>  | [<span data-ttu-id="4c279-118">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="4c279-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="4c279-119">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="4c279-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="4c279-120">Taille</span><span class="sxs-lookup"><span data-stu-id="4c279-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="4c279-121">*x*</span><span class="sxs-lookup"><span data-stu-id="4c279-121">*x*</span></span>   | <span data-ttu-id="4c279-122">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="4c279-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="4c279-123">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="4c279-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4c279-124">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="4c279-124">any</span></span>                            |
| <span data-ttu-id="4c279-125">*Av*</span><span class="sxs-lookup"><span data-stu-id="4c279-125">*ret*</span></span> | <span data-ttu-id="4c279-126">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="4c279-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="4c279-127">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="4c279-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="4c279-128">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="4c279-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4c279-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4c279-129">Minimum Shader Model</span></span>

<span data-ttu-id="4c279-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="4c279-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4c279-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4c279-131">Shader Model</span></span>                                                                       | <span data-ttu-id="4c279-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="4c279-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="4c279-133">[Nuancier modèle 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="4c279-133">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="4c279-134">Oui</span><span class="sxs-lookup"><span data-stu-id="4c279-134">yes</span></span>                 |
| [<span data-ttu-id="4c279-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c279-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="4c279-136">Oui (PS \_ 2 \_ x uniquement)</span><span class="sxs-lookup"><span data-stu-id="4c279-136">yes (ps\_2\_x only)</span></span> |
| [<span data-ttu-id="4c279-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4c279-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="4c279-138">non</span><span class="sxs-lookup"><span data-stu-id="4c279-138">no</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="4c279-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c279-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c279-140">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4c279-140">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

