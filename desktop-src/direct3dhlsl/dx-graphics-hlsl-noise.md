---
title: bruit
description: Génère une valeur aléatoire à l’aide de l’algorithme perl-Noise.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- bruit HLSL
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383327"
---
# <a name="noise"></a><span data-ttu-id="816f2-104">bruit</span><span class="sxs-lookup"><span data-stu-id="816f2-104">noise</span></span>

<span data-ttu-id="816f2-105">Génère une valeur aléatoire à l’aide de l’algorithme perl-Noise.</span><span class="sxs-lookup"><span data-stu-id="816f2-105">Generates a random value using the Perlin-noise algorithm.</span></span>




| <span data-ttu-id="816f2-106">bruit *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="816f2-106">*ret* noise(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="816f2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="816f2-107">Parameters</span></span>



| <span data-ttu-id="816f2-108">Élément</span><span class="sxs-lookup"><span data-stu-id="816f2-108">Item</span></span>                                                   | <span data-ttu-id="816f2-109">Description</span><span class="sxs-lookup"><span data-stu-id="816f2-109">Description</span></span>                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="816f2-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="816f2-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="816f2-111">\[dans \] un vecteur à virgule flottante à partir duquel générer le bruit perl.</span><span class="sxs-lookup"><span data-stu-id="816f2-111">\[in\] A floating-point vector from which to generate Perlin noise.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="816f2-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="816f2-112">Return Value</span></span>

<span data-ttu-id="816f2-113">Valeur de bruit perl dans une plage comprise entre-1 et 1.</span><span class="sxs-lookup"><span data-stu-id="816f2-113">The Perlin noise value within a range between -1 and 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="816f2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="816f2-114">Remarks</span></span>

<span data-ttu-id="816f2-115">Les valeurs de bruit perl évoluent correctement d’un point à un autre sur un espace, ce qui crée des valeurs générées de façon aléatoire et à l’aspect naturel.</span><span class="sxs-lookup"><span data-stu-id="816f2-115">Perlin noise values change smoothly from one point to another over a space, creating natural looking, randomly generated values.</span></span> <span data-ttu-id="816f2-116">Vous pouvez utiliser le bruit Perl pour générer des textures procédurales pour des effets tels que la fumée et le feu.</span><span class="sxs-lookup"><span data-stu-id="816f2-116">You can use Perlin noise to generate procedural textures for effects like smoke and fire.</span></span>

## <a name="type-description"></a><span data-ttu-id="816f2-117">Description du type</span><span class="sxs-lookup"><span data-stu-id="816f2-117">Type Description</span></span>



| <span data-ttu-id="816f2-118">Nom</span><span class="sxs-lookup"><span data-stu-id="816f2-118">Name</span></span>  | [<span data-ttu-id="816f2-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="816f2-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="816f2-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="816f2-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="816f2-121">Taille</span><span class="sxs-lookup"><span data-stu-id="816f2-121">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="816f2-122">*x*</span><span class="sxs-lookup"><span data-stu-id="816f2-122">*x*</span></span>   | [<span data-ttu-id="816f2-123">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="816f2-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="816f2-124">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="816f2-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="816f2-125">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="816f2-125">any</span></span>  |
| <span data-ttu-id="816f2-126">*Av*</span><span class="sxs-lookup"><span data-stu-id="816f2-126">*ret*</span></span> | [<span data-ttu-id="816f2-127">**scalaire**</span><span class="sxs-lookup"><span data-stu-id="816f2-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="816f2-128">**float**</span><span class="sxs-lookup"><span data-stu-id="816f2-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="816f2-129">1</span><span class="sxs-lookup"><span data-stu-id="816f2-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="816f2-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="816f2-130">Minimum Shader Model</span></span>

<span data-ttu-id="816f2-131">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="816f2-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="816f2-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="816f2-132">Shader Model</span></span>                                                                       | <span data-ttu-id="816f2-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="816f2-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="816f2-134">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="816f2-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="816f2-135">non</span><span class="sxs-lookup"><span data-stu-id="816f2-135">no</span></span>                  |
| [<span data-ttu-id="816f2-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="816f2-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="816f2-137">Oui (TX \_ 1 \_ 0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="816f2-137">yes (tx\_1\_0 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="816f2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="816f2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="816f2-139">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="816f2-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

