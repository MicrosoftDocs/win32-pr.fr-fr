---
title: cosh
description: Retourne le cosinus hyperbolique de la valeur spécifiée.
ms.assetid: ed68c461-de91-4ce4-a424-8ab28ee43f23
keywords:
- en HLSL.
topic_type:
- apiref
api_name:
- cosh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3bd6cad2b79e849d8f20bbaf5baa6cfc7db0b702
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991016"
---
# <a name="cosh"></a><span data-ttu-id="dbb9c-104">cosh</span><span class="sxs-lookup"><span data-stu-id="dbb9c-104">cosh</span></span>

<span data-ttu-id="dbb9c-105">Retourne le cosinus hyperbolique de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dbb9c-105">Returns the hyperbolic cosine of the specified value.</span></span>



| <span data-ttu-id="dbb9c-106">*RET* Cosh (*x*)</span><span class="sxs-lookup"><span data-stu-id="dbb9c-106">*ret* cosh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="dbb9c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbb9c-107">Parameters</span></span>



| <span data-ttu-id="dbb9c-108">Élément</span><span class="sxs-lookup"><span data-stu-id="dbb9c-108">Item</span></span>                                                   | <span data-ttu-id="dbb9c-109">Description</span><span class="sxs-lookup"><span data-stu-id="dbb9c-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="dbb9c-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="dbb9c-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="dbb9c-111">\[dans \] la valeur spécifiée, en radians.</span><span class="sxs-lookup"><span data-stu-id="dbb9c-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="dbb9c-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dbb9c-112">Return Value</span></span>

<span data-ttu-id="dbb9c-113">Cosinus hyperbolique du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="dbb9c-113">The hyperbolic cosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="dbb9c-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="dbb9c-114">Type Description</span></span>



| <span data-ttu-id="dbb9c-115">Nom</span><span class="sxs-lookup"><span data-stu-id="dbb9c-115">Name</span></span>  | [<span data-ttu-id="dbb9c-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="dbb9c-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="dbb9c-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="dbb9c-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="dbb9c-118">Taille</span><span class="sxs-lookup"><span data-stu-id="dbb9c-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="dbb9c-119">*x*</span><span class="sxs-lookup"><span data-stu-id="dbb9c-119">*x*</span></span>   | <span data-ttu-id="dbb9c-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="dbb9c-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="dbb9c-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="dbb9c-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="dbb9c-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="dbb9c-122">any</span></span>                            |
| <span data-ttu-id="dbb9c-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="dbb9c-123">*ret*</span></span> | <span data-ttu-id="dbb9c-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="dbb9c-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="dbb9c-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="dbb9c-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="dbb9c-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="dbb9c-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dbb9c-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="dbb9c-127">Minimum Shader Model</span></span>

<span data-ttu-id="dbb9c-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="dbb9c-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dbb9c-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="dbb9c-129">Shader Model</span></span>                                                                       | <span data-ttu-id="dbb9c-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="dbb9c-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="dbb9c-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="dbb9c-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="dbb9c-132">Oui</span><span class="sxs-lookup"><span data-stu-id="dbb9c-132">yes</span></span>       |
| [<span data-ttu-id="dbb9c-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dbb9c-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="dbb9c-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="dbb9c-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="dbb9c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbb9c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb9c-136">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="dbb9c-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

