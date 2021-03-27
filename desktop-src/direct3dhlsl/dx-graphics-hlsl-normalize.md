---
title: normalize
description: Normalise le vecteur à virgule flottante spécifié en fonction de x/longueur (x).
ms.assetid: 7fd6f8ff-f3ff-4d14-b3fc-b44fdddf6c75
keywords:
- normaliser le HLSL
topic_type:
- apiref
api_name:
- normalize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f48c78f80f5f92f950795018f05a46c7883d9736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941333"
---
# <a name="normalize"></a><span data-ttu-id="29ece-104">normalize</span><span class="sxs-lookup"><span data-stu-id="29ece-104">normalize</span></span>

<span data-ttu-id="29ece-105">Normalise le vecteur à virgule flottante spécifié en fonction de x/longueur (x).</span><span class="sxs-lookup"><span data-stu-id="29ece-105">Normalizes the specified floating-point vector according to x / length(x).</span></span>



| <span data-ttu-id="29ece-106">*RET* Normalize (*x*)</span><span class="sxs-lookup"><span data-stu-id="29ece-106">*ret* normalize(*x*)</span></span> |
|----------------------|



 

## <a name="parameters"></a><span data-ttu-id="29ece-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29ece-107">Parameters</span></span>



| <span data-ttu-id="29ece-108">Élément</span><span class="sxs-lookup"><span data-stu-id="29ece-108">Item</span></span>                                                   | <span data-ttu-id="29ece-109">Description</span><span class="sxs-lookup"><span data-stu-id="29ece-109">Description</span></span>                                            |
|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="29ece-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="29ece-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="29ece-111">\[dans \] le vecteur à virgule flottante spécifié.</span><span class="sxs-lookup"><span data-stu-id="29ece-111">\[in\] The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="29ece-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="29ece-112">Return Value</span></span>

<span data-ttu-id="29ece-113">Paramètre *x* normalisé.</span><span class="sxs-lookup"><span data-stu-id="29ece-113">The normalized *x* parameter.</span></span> <span data-ttu-id="29ece-114">Si la longueur du paramètre *x* est égale à 0, le résultat est indéfini.</span><span class="sxs-lookup"><span data-stu-id="29ece-114">If the length of the *x* parameter is 0, the result is indefinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="29ece-115">Notes</span><span class="sxs-lookup"><span data-stu-id="29ece-115">Remarks</span></span>

<span data-ttu-id="29ece-116">La fonction intrinsèque **Normalize** HLSL utilise la formule suivante : *x*  /  [**Length**](dx-graphics-hlsl-length.md)(*x*).</span><span class="sxs-lookup"><span data-stu-id="29ece-116">The **normalize** HLSL intrinsic function uses the following formula: *x* / [**length**](dx-graphics-hlsl-length.md)(*x*).</span></span>

## <a name="type-description"></a><span data-ttu-id="29ece-117">Description du type</span><span class="sxs-lookup"><span data-stu-id="29ece-117">Type Description</span></span>



| <span data-ttu-id="29ece-118">Nom</span><span class="sxs-lookup"><span data-stu-id="29ece-118">Name</span></span>  | [<span data-ttu-id="29ece-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="29ece-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="29ece-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="29ece-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="29ece-121">Taille</span><span class="sxs-lookup"><span data-stu-id="29ece-121">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="29ece-122">*x*</span><span class="sxs-lookup"><span data-stu-id="29ece-122">*x*</span></span>   | [<span data-ttu-id="29ece-123">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="29ece-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="29ece-124">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="29ece-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="29ece-125">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="29ece-125">any</span></span>                            |
| <span data-ttu-id="29ece-126">*Av*</span><span class="sxs-lookup"><span data-stu-id="29ece-126">*ret*</span></span> | <span data-ttu-id="29ece-127">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="29ece-127">same as input *x*</span></span>                                                                   | [<span data-ttu-id="29ece-128">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="29ece-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="29ece-129">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="29ece-129">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="29ece-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="29ece-130">Minimum Shader Model</span></span>

<span data-ttu-id="29ece-131">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="29ece-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="29ece-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="29ece-132">Shader Model</span></span>                                                                       | <span data-ttu-id="29ece-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="29ece-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="29ece-134">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="29ece-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="29ece-135">Oui</span><span class="sxs-lookup"><span data-stu-id="29ece-135">yes</span></span>                 |
| [<span data-ttu-id="29ece-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="29ece-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="29ece-137">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="29ece-137">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="29ece-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29ece-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ece-139">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="29ece-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

