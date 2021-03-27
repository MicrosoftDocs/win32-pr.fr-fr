---
title: Log2 (Corecrt \_ Math. h)
description: Retourne le logarithme de base 2 de la valeur spécifiée.
ms.assetid: 0bc75697-92c0-4de5-89bd-2ce824baa03e
keywords:
- HLSL log2
topic_type:
- apiref
api_name:
- log2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81692071b7886fa3e3096d785bccf80c7eff937a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953996"
---
# <a name="log2"></a><span data-ttu-id="c59a3-104">Log2</span><span class="sxs-lookup"><span data-stu-id="c59a3-104">log2</span></span>

<span data-ttu-id="c59a3-105">Retourne le logarithme de base 2 de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c59a3-105">Returns the base-2 logarithm of the specified value.</span></span>



| <span data-ttu-id="c59a3-106">*RET* Log2 (*x*)</span><span class="sxs-lookup"><span data-stu-id="c59a3-106">*ret* log2(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="c59a3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c59a3-107">Parameters</span></span>



| <span data-ttu-id="c59a3-108">Élément</span><span class="sxs-lookup"><span data-stu-id="c59a3-108">Item</span></span>                                                   | <span data-ttu-id="c59a3-109">Description</span><span class="sxs-lookup"><span data-stu-id="c59a3-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="c59a3-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="c59a3-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c59a3-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c59a3-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c59a3-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c59a3-112">Return Value</span></span>

<span data-ttu-id="c59a3-113">Logarithme de base 2 du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="c59a3-113">The base-2 logarithm of the *x* parameter.</span></span> <span data-ttu-id="c59a3-114">Si le paramètre *x* est négatif, cette fonction retourne la valeur indéfinie.</span><span class="sxs-lookup"><span data-stu-id="c59a3-114">If the *x* parameter is negative, this function returns indefinite.</span></span> <span data-ttu-id="c59a3-115">Si le paramètre *x* est égal à 0, cette fonction retourne + INF.</span><span class="sxs-lookup"><span data-stu-id="c59a3-115">If the *x* parameter is 0, this function returns +INF.</span></span>

## <a name="type-description"></a><span data-ttu-id="c59a3-116">Description du type</span><span class="sxs-lookup"><span data-stu-id="c59a3-116">Type Description</span></span>



| <span data-ttu-id="c59a3-117">Nom</span><span class="sxs-lookup"><span data-stu-id="c59a3-117">Name</span></span>  | [<span data-ttu-id="c59a3-118">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="c59a3-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="c59a3-119">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="c59a3-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="c59a3-120">Taille</span><span class="sxs-lookup"><span data-stu-id="c59a3-120">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="c59a3-121">*x*</span><span class="sxs-lookup"><span data-stu-id="c59a3-121">*x*</span></span>   | <span data-ttu-id="c59a3-122">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="c59a3-122">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="c59a3-123">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="c59a3-123">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c59a3-124">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="c59a3-124">any</span></span>                            |
| <span data-ttu-id="c59a3-125">*Av*</span><span class="sxs-lookup"><span data-stu-id="c59a3-125">*ret*</span></span> | <span data-ttu-id="c59a3-126">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="c59a3-126">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="c59a3-127">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="c59a3-127">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="c59a3-128">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="c59a3-128">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c59a3-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="c59a3-129">Minimum Shader Model</span></span>

<span data-ttu-id="c59a3-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="c59a3-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c59a3-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="c59a3-131">Shader Model</span></span>                                                                       | <span data-ttu-id="c59a3-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="c59a3-132">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="c59a3-133">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="c59a3-133">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="c59a3-134">Oui</span><span class="sxs-lookup"><span data-stu-id="c59a3-134">yes</span></span>                 |
| [<span data-ttu-id="c59a3-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c59a3-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="c59a3-136">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="c59a3-136">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c59a3-137">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c59a3-137">Requirements</span></span>



| <span data-ttu-id="c59a3-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c59a3-138">Requirement</span></span> | <span data-ttu-id="c59a3-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="c59a3-139">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c59a3-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="c59a3-140">Header</span></span><br/> | <dl> <span data-ttu-id="c59a3-141"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c59a3-141"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c59a3-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c59a3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59a3-143">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c59a3-143">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

