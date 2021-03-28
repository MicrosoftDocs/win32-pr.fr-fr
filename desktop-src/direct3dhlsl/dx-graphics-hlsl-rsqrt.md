---
title: rsqrt,
description: Retourne la réciproque de la racine carrée de la valeur spécifiée.
ms.assetid: 4e266e41-cde9-4a59-8937-98bfc63f3b5d
keywords:
- HLSL rsqrt,
topic_type:
- apiref
api_name:
- rsqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56eb5f1cba8510e57a2c4b5622e10dc91666b6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990937"
---
# <a name="rsqrt"></a><span data-ttu-id="7e392-104">rsqrt,</span><span class="sxs-lookup"><span data-stu-id="7e392-104">rsqrt</span></span>

<span data-ttu-id="7e392-105">Retourne la réciproque de la racine carrée de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7e392-105">Returns the reciprocal of the square root of the specified value.</span></span>



| <span data-ttu-id="7e392-106">*RET* rsqrt, (*x*)</span><span class="sxs-lookup"><span data-stu-id="7e392-106">*ret* rsqrt(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="7e392-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e392-107">Parameters</span></span>



| <span data-ttu-id="7e392-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7e392-108">Item</span></span>                                                   | <span data-ttu-id="7e392-109">Description</span><span class="sxs-lookup"><span data-stu-id="7e392-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="7e392-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="7e392-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="7e392-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7e392-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7e392-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7e392-112">Return Value</span></span>

<span data-ttu-id="7e392-113">Réciproque de la racine carrée du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="7e392-113">The reciprocal of the square root of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e392-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7e392-114">Remarks</span></span>

<span data-ttu-id="7e392-115">Cette fonction utilise la formule suivante : 1/ **sqrt**(*x*).</span><span class="sxs-lookup"><span data-stu-id="7e392-115">This function uses the following formula: 1 / **sqrt**(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="7e392-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="7e392-116">Type Description</span></span>



| <span data-ttu-id="7e392-117">Nom</span><span class="sxs-lookup"><span data-stu-id="7e392-117">Name</span></span>  | [<span data-ttu-id="7e392-118">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="7e392-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7e392-119">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="7e392-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7e392-120">Taille</span><span class="sxs-lookup"><span data-stu-id="7e392-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7e392-121">*x*</span><span class="sxs-lookup"><span data-stu-id="7e392-121">*x*</span></span>   | <span data-ttu-id="7e392-122">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="7e392-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="7e392-123">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="7e392-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7e392-124">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="7e392-124">any</span></span>                            |
| <span data-ttu-id="7e392-125">*Av*</span><span class="sxs-lookup"><span data-stu-id="7e392-125">*ret*</span></span> | <span data-ttu-id="7e392-126">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="7e392-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="7e392-127">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="7e392-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7e392-128">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="7e392-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7e392-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="7e392-129">Minimum Shader Model</span></span>

<span data-ttu-id="7e392-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="7e392-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7e392-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="7e392-131">Shader Model</span></span>                                                                       | <span data-ttu-id="7e392-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="7e392-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="7e392-133">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="7e392-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="7e392-134">Oui</span><span class="sxs-lookup"><span data-stu-id="7e392-134">yes</span></span>                 |
| [<span data-ttu-id="7e392-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e392-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="7e392-136">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="7e392-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="7e392-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e392-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e392-138">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7e392-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

