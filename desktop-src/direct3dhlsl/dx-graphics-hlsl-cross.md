---
title: cross
description: Retourne le produit croisé de deux vecteurs 3D à virgule flottante.
ms.assetid: 5f1832af-6bc5-49a7-956a-fd762f674f5f
keywords:
- HLSL croisé
topic_type:
- apiref
api_name:
- cross
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91959bf415c3e56edf370942de268523bf998743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991013"
---
# <a name="cross"></a><span data-ttu-id="9ef88-104">cross</span><span class="sxs-lookup"><span data-stu-id="9ef88-104">cross</span></span>

<span data-ttu-id="9ef88-105">Retourne le produit croisé de deux vecteurs 3D à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="9ef88-105">Returns the cross product of two floating-point, 3D vectors.</span></span>



| <span data-ttu-id="9ef88-106">*RET* inter (*x*, *y*)</span><span class="sxs-lookup"><span data-stu-id="9ef88-106">*ret* cross(*x*, *y*)</span></span> |
|-----------------------|



 

## <a name="parameters"></a><span data-ttu-id="9ef88-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ef88-107">Parameters</span></span>



| <span data-ttu-id="9ef88-108">Élément</span><span class="sxs-lookup"><span data-stu-id="9ef88-108">Item</span></span>                                                   | <span data-ttu-id="9ef88-109">Description</span><span class="sxs-lookup"><span data-stu-id="9ef88-109">Description</span></span>                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9ef88-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="9ef88-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="9ef88-111">\[dans \] le premier vecteur 3D à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="9ef88-111">\[in\] The first floating-point, 3D vector.</span></span><br/>  |
| <span data-ttu-id="9ef88-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="9ef88-112"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="9ef88-113">\[dans \] le deuxième vecteur 3D à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="9ef88-113">\[in\] The second floating-point, 3D vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="9ef88-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9ef88-114">Return Value</span></span>

<span data-ttu-id="9ef88-115">Produit croisé du paramètre *x* et du paramètre *y* .</span><span class="sxs-lookup"><span data-stu-id="9ef88-115">The cross product of the *x* parameter and the *y* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="9ef88-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="9ef88-116">Type Description</span></span>



| <span data-ttu-id="9ef88-117">Nom</span><span class="sxs-lookup"><span data-stu-id="9ef88-117">Name</span></span>  | [<span data-ttu-id="9ef88-118">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="9ef88-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="9ef88-119">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="9ef88-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="9ef88-120">Taille</span><span class="sxs-lookup"><span data-stu-id="9ef88-120">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="9ef88-121">*x*</span><span class="sxs-lookup"><span data-stu-id="9ef88-121">*x*</span></span>   | [<span data-ttu-id="9ef88-122">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="9ef88-122">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9ef88-123">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="9ef88-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9ef88-124">3</span><span class="sxs-lookup"><span data-stu-id="9ef88-124">3</span></span>    |
| <span data-ttu-id="9ef88-125">*y*</span><span class="sxs-lookup"><span data-stu-id="9ef88-125">*y*</span></span>   | [<span data-ttu-id="9ef88-126">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="9ef88-126">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9ef88-127">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="9ef88-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9ef88-128">3</span><span class="sxs-lookup"><span data-stu-id="9ef88-128">3</span></span>    |
| <span data-ttu-id="9ef88-129">*Av*</span><span class="sxs-lookup"><span data-stu-id="9ef88-129">*ret*</span></span> | [<span data-ttu-id="9ef88-130">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="9ef88-130">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="9ef88-131">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="9ef88-131">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="9ef88-132">3</span><span class="sxs-lookup"><span data-stu-id="9ef88-132">3</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9ef88-133">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9ef88-133">Minimum Shader Model</span></span>

<span data-ttu-id="9ef88-134">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="9ef88-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9ef88-135">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9ef88-135">Shader Model</span></span>                                                                       | <span data-ttu-id="9ef88-136">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9ef88-136">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="9ef88-137">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="9ef88-137">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="9ef88-138">Oui</span><span class="sxs-lookup"><span data-stu-id="9ef88-138">yes</span></span>                   |
| [<span data-ttu-id="9ef88-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9ef88-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="9ef88-140">vs \_ 1 \_ 1 et PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="9ef88-140">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="9ef88-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ef88-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef88-142">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="9ef88-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

