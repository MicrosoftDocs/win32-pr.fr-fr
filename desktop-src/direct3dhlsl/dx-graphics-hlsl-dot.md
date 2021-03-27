---
title: dot
description: Retourne le produit scalaire de deux vecteurs.
ms.assetid: ad24c06c-0b40-4dc5-a2b9-1d5438635ed8
keywords:
- HLSL point
topic_type:
- apiref
api_name:
- dot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6d05abf0d67628d1d77b362b028107e07b83457
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941247"
---
# <a name="dot"></a><span data-ttu-id="70cd1-104">dot</span><span class="sxs-lookup"><span data-stu-id="70cd1-104">dot</span></span>

<span data-ttu-id="70cd1-105">Retourne le produit scalaire de deux vecteurs.</span><span class="sxs-lookup"><span data-stu-id="70cd1-105">Returns the dot product of two vectors.</span></span>



| <span data-ttu-id="70cd1-106">*RET* point (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="70cd1-106">*ret* dot(*x*, *y*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="70cd1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70cd1-107">Parameters</span></span>



| <span data-ttu-id="70cd1-108">Élément</span><span class="sxs-lookup"><span data-stu-id="70cd1-108">Item</span></span>                                                   | <span data-ttu-id="70cd1-109">Description</span><span class="sxs-lookup"><span data-stu-id="70cd1-109">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="70cd1-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="70cd1-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="70cd1-111">\[dans \] le premier vecteur.</span><span class="sxs-lookup"><span data-stu-id="70cd1-111">\[in\] The first vector.</span></span><br/>  |
| <span data-ttu-id="70cd1-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="70cd1-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="70cd1-113">\[dans \] le second vecteur.</span><span class="sxs-lookup"><span data-stu-id="70cd1-113">\[in\] The second vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="70cd1-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="70cd1-114">Return Value</span></span>

<span data-ttu-id="70cd1-115">Produit scalaire du paramètre *x* et du paramètre *y* .</span><span class="sxs-lookup"><span data-stu-id="70cd1-115">The dot product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="70cd1-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="70cd1-116">Type Description</span></span>



| <span data-ttu-id="70cd1-117">Nom</span><span class="sxs-lookup"><span data-stu-id="70cd1-117">Name</span></span>  | [<span data-ttu-id="70cd1-118">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="70cd1-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="70cd1-119">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="70cd1-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                 | <span data-ttu-id="70cd1-120">Taille</span><span class="sxs-lookup"><span data-stu-id="70cd1-120">Size</span></span>                            |
|-------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="70cd1-121">*x*</span><span class="sxs-lookup"><span data-stu-id="70cd1-121">*x*</span></span>   | [<span data-ttu-id="70cd1-122">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="70cd1-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="70cd1-123">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="70cd1-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="70cd1-124">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="70cd1-124">any</span></span>                             |
| <span data-ttu-id="70cd1-125">*y*</span><span class="sxs-lookup"><span data-stu-id="70cd1-125">*y*</span></span>   | [<span data-ttu-id="70cd1-126">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="70cd1-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="70cd1-127">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="70cd1-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="70cd1-128">mêmes dimensions (s) que l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="70cd1-128">same dimensions(s) as input *x*</span></span> |
| <span data-ttu-id="70cd1-129">*Av*</span><span class="sxs-lookup"><span data-stu-id="70cd1-129">*ret*</span></span> | [<span data-ttu-id="70cd1-130">**scalaire**</span><span class="sxs-lookup"><span data-stu-id="70cd1-130">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="70cd1-131">[**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="70cd1-131">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="70cd1-132">1</span><span class="sxs-lookup"><span data-stu-id="70cd1-132">1</span></span>                               |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="70cd1-133">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="70cd1-133">Minimum Shader Model</span></span>

<span data-ttu-id="70cd1-134">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="70cd1-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="70cd1-135">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="70cd1-135">Shader Model</span></span>                                                                       | <span data-ttu-id="70cd1-136">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="70cd1-136">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="70cd1-137">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="70cd1-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="70cd1-138">Oui</span><span class="sxs-lookup"><span data-stu-id="70cd1-138">yes</span></span>       |
| [<span data-ttu-id="70cd1-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="70cd1-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="70cd1-140">Oui</span><span class="sxs-lookup"><span data-stu-id="70cd1-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="70cd1-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70cd1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70cd1-142">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="70cd1-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

