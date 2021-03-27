---
title: correspond
description: Retourne un vecteur de réflexion à l’aide d’un rayon d’incident et d’une surface normale.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- réfléchir au HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729925"
---
# <a name="reflect"></a><span data-ttu-id="5c664-104">correspond</span><span class="sxs-lookup"><span data-stu-id="5c664-104">reflect</span></span>

<span data-ttu-id="5c664-105">Retourne un vecteur de réflexion à l’aide d’un rayon d’incident et d’une surface normale.</span><span class="sxs-lookup"><span data-stu-id="5c664-105">Returns a reflection vector using an incident ray and a surface normal.</span></span>



| <span data-ttu-id="5c664-106">*RET* réfléchi (*i*, *n*)</span><span class="sxs-lookup"><span data-stu-id="5c664-106">*ret* reflect(*i*, *n*)</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="5c664-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c664-107">Parameters</span></span>



| <span data-ttu-id="5c664-108">Élément</span><span class="sxs-lookup"><span data-stu-id="5c664-108">Item</span></span>                                                   | <span data-ttu-id="5c664-109">Description</span><span class="sxs-lookup"><span data-stu-id="5c664-109">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c664-110"><span id="i"></span><span id="I"></span>*cliqu*</span><span class="sxs-lookup"><span data-stu-id="5c664-110"><span id="i"></span><span id="I"></span>*i*</span></span><br/> | <span data-ttu-id="5c664-111">\[dans \] un vecteur d’incident à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5c664-111">\[in\] A floating-point, incident vector.</span></span><br/> |
| <span data-ttu-id="5c664-112"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="5c664-112"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="5c664-113">\[dans \] un vecteur normal à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5c664-113">\[in\] A floating-point, normal vector.</span></span><br/>   |



 

## <a name="return-value"></a><span data-ttu-id="5c664-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5c664-114">Return Value</span></span>

<span data-ttu-id="5c664-115">Vecteur de réflexion à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5c664-115">A floating-point, reflection vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c664-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5c664-116">Remarks</span></span>

<span data-ttu-id="5c664-117">Cette fonction calcule le vecteur de réflexion à l’aide de la formule suivante : v = i-2 \* n \* point (i n).</span><span class="sxs-lookup"><span data-stu-id="5c664-117">This function calculates the reflection vector using the following formula: v = i - 2 \* n \* dot(i n) .</span></span>

## <a name="type-description"></a><span data-ttu-id="5c664-118">Description du type</span><span class="sxs-lookup"><span data-stu-id="5c664-118">Type Description</span></span>



| <span data-ttu-id="5c664-119">Nom</span><span class="sxs-lookup"><span data-stu-id="5c664-119">Name</span></span>  | [<span data-ttu-id="5c664-120">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="5c664-120">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="5c664-121">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="5c664-121">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="5c664-122">Taille</span><span class="sxs-lookup"><span data-stu-id="5c664-122">Size</span></span>                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="5c664-123">*i*</span><span class="sxs-lookup"><span data-stu-id="5c664-123">*i*</span></span>   | [<span data-ttu-id="5c664-124">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="5c664-124">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5c664-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="5c664-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5c664-126">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="5c664-126">any</span></span>                            |
| <span data-ttu-id="5c664-127">*n*</span><span class="sxs-lookup"><span data-stu-id="5c664-127">*n*</span></span>   | [<span data-ttu-id="5c664-128">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="5c664-128">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5c664-129">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="5c664-129">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5c664-130">la ou les mêmes dimensions que l’entrée *i*</span><span class="sxs-lookup"><span data-stu-id="5c664-130">same dimension(s) as input *i*</span></span> |
| <span data-ttu-id="5c664-131">*Av*</span><span class="sxs-lookup"><span data-stu-id="5c664-131">*ret*</span></span> | [<span data-ttu-id="5c664-132">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="5c664-132">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="5c664-133">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="5c664-133">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="5c664-134">la ou les mêmes dimensions que l’entrée *i*</span><span class="sxs-lookup"><span data-stu-id="5c664-134">same dimension(s) as input *i*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5c664-135">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5c664-135">Minimum Shader Model</span></span>

<span data-ttu-id="5c664-136">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5c664-136">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5c664-137">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5c664-137">Shader Model</span></span>                                                                       | <span data-ttu-id="5c664-138">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5c664-138">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="5c664-139">[Nuancier Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="5c664-139">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="5c664-140">Oui</span><span class="sxs-lookup"><span data-stu-id="5c664-140">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5c664-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c664-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c664-142">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="5c664-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

