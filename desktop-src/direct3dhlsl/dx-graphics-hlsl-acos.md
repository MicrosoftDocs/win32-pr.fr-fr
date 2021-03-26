---
title: acos
description: Retourne l’arc cosinus de la valeur spécifiée.
ms.assetid: c9bc33b8-d586-4c64-9453-5ab97396f2cf
keywords:
- ACOS (HLSL)
topic_type:
- apiref
api_name:
- acos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2cd909c4a4c1300374bba723f1edabb48d51b2e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102249"
---
# <a name="acos"></a><span data-ttu-id="25fe2-104">acos</span><span class="sxs-lookup"><span data-stu-id="25fe2-104">acos</span></span>

<span data-ttu-id="25fe2-105">Retourne l’arc cosinus de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="25fe2-105">Returns the arccosine of the specified value.</span></span>



| <span data-ttu-id="25fe2-106">*RET* ACOS (*x*)</span><span class="sxs-lookup"><span data-stu-id="25fe2-106">*ret* acos(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="25fe2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25fe2-107">Parameters</span></span>



| <span data-ttu-id="25fe2-108">Élément</span><span class="sxs-lookup"><span data-stu-id="25fe2-108">Item</span></span>                                                   | <span data-ttu-id="25fe2-109">Description</span><span class="sxs-lookup"><span data-stu-id="25fe2-109">Description</span></span>                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25fe2-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="25fe2-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="25fe2-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="25fe2-111">\[in\] The specified value.</span></span> <span data-ttu-id="25fe2-112">Chaque composant doit être une valeur à virgule flottante comprise entre-1 et 1.</span><span class="sxs-lookup"><span data-stu-id="25fe2-112">Each component should be a floating-point value within the range of -1 to 1.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="25fe2-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="25fe2-113">Return Value</span></span>

<span data-ttu-id="25fe2-114">Arccosinus du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="25fe2-114">The arccosine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="25fe2-115">Description du type</span><span class="sxs-lookup"><span data-stu-id="25fe2-115">Type Description</span></span>



| <span data-ttu-id="25fe2-116">Nom</span><span class="sxs-lookup"><span data-stu-id="25fe2-116">Name</span></span>  | [<span data-ttu-id="25fe2-117">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="25fe2-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="25fe2-118">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="25fe2-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="25fe2-119">Taille</span><span class="sxs-lookup"><span data-stu-id="25fe2-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="25fe2-120">*x*</span><span class="sxs-lookup"><span data-stu-id="25fe2-120">*x*</span></span>   | <span data-ttu-id="25fe2-121">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="25fe2-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="25fe2-122">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="25fe2-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="25fe2-123">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="25fe2-123">any</span></span>                            |
| <span data-ttu-id="25fe2-124">*Av*</span><span class="sxs-lookup"><span data-stu-id="25fe2-124">*ret*</span></span> | <span data-ttu-id="25fe2-125">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="25fe2-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="25fe2-126">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="25fe2-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="25fe2-127">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="25fe2-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="25fe2-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="25fe2-128">Minimum Shader Model</span></span>

<span data-ttu-id="25fe2-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="25fe2-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="25fe2-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="25fe2-130">Shader Model</span></span>                                                                       | <span data-ttu-id="25fe2-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="25fe2-131">Supported</span></span>     |
|------------------------------------------------------------------------------------|---------------|
| <span data-ttu-id="25fe2-132">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="25fe2-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="25fe2-133">Oui</span><span class="sxs-lookup"><span data-stu-id="25fe2-133">yes</span></span>           |
| [<span data-ttu-id="25fe2-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="25fe2-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="25fe2-135">vs \_ 1 \_ 1 uniquement</span><span class="sxs-lookup"><span data-stu-id="25fe2-135">vs\_1\_1 only</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="25fe2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25fe2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fe2-137">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="25fe2-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

