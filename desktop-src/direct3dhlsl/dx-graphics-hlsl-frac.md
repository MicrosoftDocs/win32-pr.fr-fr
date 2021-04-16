---
title: frac
description: Retourne la partie fractionnaire (ou décimale) de x ; qui est supérieur ou égal à 0 et inférieur à 1.
ms.assetid: 4e85390f-2b1a-402b-b932-09b80097f7e6
keywords:
- HLSL FRAC
topic_type:
- apiref
api_name:
- frac
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 468bddc34f22f9bb5f34871102678e1765148b11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463642"
---
# <a name="frac"></a><span data-ttu-id="0b4c3-104">frac</span><span class="sxs-lookup"><span data-stu-id="0b4c3-104">frac</span></span>

<span data-ttu-id="0b4c3-105">Retourne la partie fractionnaire (ou décimale) de x ; qui est supérieur ou égal à 0 et inférieur à 1.</span><span class="sxs-lookup"><span data-stu-id="0b4c3-105">Returns the fractional (or decimal) part of x; which is greater than or equal to 0 and less than 1.</span></span>

<span data-ttu-id="0b4c3-106">Voir aussi [trunc](./dx-graphics-hlsl-trunc.md).</span><span class="sxs-lookup"><span data-stu-id="0b4c3-106">Also see [trunc](./dx-graphics-hlsl-trunc.md).</span></span>

| <span data-ttu-id="0b4c3-107">*RET* FRAC (*x*)</span><span class="sxs-lookup"><span data-stu-id="0b4c3-107">*ret* frac(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="0b4c3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b4c3-108">Parameters</span></span>



| <span data-ttu-id="0b4c3-109">Élément</span><span class="sxs-lookup"><span data-stu-id="0b4c3-109">Item</span></span>                                                   | <span data-ttu-id="0b4c3-110">Description</span><span class="sxs-lookup"><span data-stu-id="0b4c3-110">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="0b4c3-111"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="0b4c3-111"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="0b4c3-112">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0b4c3-112">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="0b4c3-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0b4c3-113">Return Value</span></span>

<span data-ttu-id="0b4c3-114">Partie fractionnaire du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="0b4c3-114">The fractional part of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="0b4c3-115">Description du type</span><span class="sxs-lookup"><span data-stu-id="0b4c3-115">Type Description</span></span>



| <span data-ttu-id="0b4c3-116">Nom</span><span class="sxs-lookup"><span data-stu-id="0b4c3-116">Name</span></span>  | [<span data-ttu-id="0b4c3-117">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="0b4c3-118">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="0b4c3-119">Taille</span><span class="sxs-lookup"><span data-stu-id="0b4c3-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="0b4c3-120">*x*</span><span class="sxs-lookup"><span data-stu-id="0b4c3-120">*x*</span></span>   | <span data-ttu-id="0b4c3-121">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="0b4c3-122">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0b4c3-123">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="0b4c3-123">any</span></span>                            |
| <span data-ttu-id="0b4c3-124">*Av*</span><span class="sxs-lookup"><span data-stu-id="0b4c3-124">*ret*</span></span> | <span data-ttu-id="0b4c3-125">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="0b4c3-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="0b4c3-126">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="0b4c3-127">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="0b4c3-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0b4c3-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="0b4c3-128">Minimum Shader Model</span></span>

<span data-ttu-id="0b4c3-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="0b4c3-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0b4c3-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="0b4c3-130">Shader Model</span></span>                                                                       | <span data-ttu-id="0b4c3-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="0b4c3-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="0b4c3-132">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="0b4c3-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="0b4c3-133">Oui</span><span class="sxs-lookup"><span data-stu-id="0b4c3-133">yes</span></span>       |
| [<span data-ttu-id="0b4c3-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b4c3-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="0b4c3-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0b4c3-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="0b4c3-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b4c3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b4c3-137">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="0b4c3-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

