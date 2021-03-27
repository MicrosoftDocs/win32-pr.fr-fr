---
title: log
description: Retourne le logarithme de base e de la valeur spécifiée.
ms.assetid: 443e7aa7-7219-40ad-aafc-4bce09c8f596
keywords:
- Journal HLSL
topic_type:
- apiref
api_name:
- log
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdd08fe178925406145476b3250e8d256b263c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729164"
---
# <a name="log"></a><span data-ttu-id="f34d4-104">journal</span><span class="sxs-lookup"><span data-stu-id="f34d4-104">log</span></span>

<span data-ttu-id="f34d4-105">Retourne le logarithme de base e de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f34d4-105">Returns the base-e logarithm of the specified value.</span></span>



| <span data-ttu-id="f34d4-106">journal *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="f34d4-106">*ret* log(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="f34d4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f34d4-107">Parameters</span></span>



| <span data-ttu-id="f34d4-108">Élément</span><span class="sxs-lookup"><span data-stu-id="f34d4-108">Item</span></span>                                                   | <span data-ttu-id="f34d4-109">Description</span><span class="sxs-lookup"><span data-stu-id="f34d4-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="f34d4-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="f34d4-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="f34d4-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f34d4-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="f34d4-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f34d4-112">Return Value</span></span>

<span data-ttu-id="f34d4-113">Logarithme de base e du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="f34d4-113">The base-e logarithm of the *x* parameter.</span></span> <span data-ttu-id="f34d4-114">Si le paramètre *x* est négatif, cette fonction retourne la valeur indéfinie.</span><span class="sxs-lookup"><span data-stu-id="f34d4-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="f34d4-115">Si le paramètre *x* est égal à 0, cette fonction retourne-INF.</span><span class="sxs-lookup"><span data-stu-id="f34d4-115">If the *x* parameter is 0, this function returns -INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="f34d4-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="f34d4-116">Type Description</span></span>



| <span data-ttu-id="f34d4-117">Nom</span><span class="sxs-lookup"><span data-stu-id="f34d4-117">Name</span></span>  | [<span data-ttu-id="f34d4-118">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="f34d4-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f34d4-119">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="f34d4-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f34d4-120">Taille</span><span class="sxs-lookup"><span data-stu-id="f34d4-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="f34d4-121">*x*</span><span class="sxs-lookup"><span data-stu-id="f34d4-121">*x*</span></span>   | <span data-ttu-id="f34d4-122">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="f34d4-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f34d4-123">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="f34d4-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f34d4-124">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="f34d4-124">any</span></span>                            |
| <span data-ttu-id="f34d4-125">*Av*</span><span class="sxs-lookup"><span data-stu-id="f34d4-125">*ret*</span></span> | <span data-ttu-id="f34d4-126">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="f34d4-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="f34d4-127">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="f34d4-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="f34d4-128">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="f34d4-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f34d4-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f34d4-129">Minimum Shader Model</span></span>

<span data-ttu-id="f34d4-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f34d4-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f34d4-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f34d4-131">Shader Model</span></span>                                                                       | <span data-ttu-id="f34d4-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f34d4-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="f34d4-133">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="f34d4-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="f34d4-134">Oui</span><span class="sxs-lookup"><span data-stu-id="f34d4-134">yes</span></span>                 |
| [<span data-ttu-id="f34d4-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f34d4-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="f34d4-136">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="f34d4-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="f34d4-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f34d4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f34d4-138">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="f34d4-138">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

