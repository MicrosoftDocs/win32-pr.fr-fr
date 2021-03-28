---
title: sin
description: Retourne le sinus de la valeur spécifiée.
ms.assetid: e1c3ead8-73dd-4798-8553-1a42dbaefe8e
keywords:
- Sin (HLSL)
topic_type:
- apiref
api_name:
- sin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d48332d35052a893dcb348a70e4d464a6bbfe0c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382552"
---
# <a name="sin"></a><span data-ttu-id="7251b-104">sin</span><span class="sxs-lookup"><span data-stu-id="7251b-104">sin</span></span>

<span data-ttu-id="7251b-105">Retourne le sinus de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7251b-105">Returns the sine of the specified value.</span></span>



| <span data-ttu-id="7251b-106">*RENV* Sin (*x*)</span><span class="sxs-lookup"><span data-stu-id="7251b-106">*ret* sin(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="7251b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7251b-107">Parameters</span></span>



| <span data-ttu-id="7251b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7251b-108">Item</span></span>                                                   | <span data-ttu-id="7251b-109">Description</span><span class="sxs-lookup"><span data-stu-id="7251b-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="7251b-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="7251b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="7251b-111">\[dans \] la valeur spécifiée, en radians.</span><span class="sxs-lookup"><span data-stu-id="7251b-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="7251b-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7251b-112">Return Value</span></span>

<span data-ttu-id="7251b-113">Sinus du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="7251b-113">The sine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="7251b-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="7251b-114">Type Description</span></span>



| <span data-ttu-id="7251b-115">Nom</span><span class="sxs-lookup"><span data-stu-id="7251b-115">Name</span></span>  | [<span data-ttu-id="7251b-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="7251b-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="7251b-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="7251b-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="7251b-118">Taille</span><span class="sxs-lookup"><span data-stu-id="7251b-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="7251b-119">*x*</span><span class="sxs-lookup"><span data-stu-id="7251b-119">*x*</span></span>   | <span data-ttu-id="7251b-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="7251b-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="7251b-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="7251b-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7251b-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="7251b-122">any</span></span>                            |
| <span data-ttu-id="7251b-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="7251b-123">*ret*</span></span> | <span data-ttu-id="7251b-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="7251b-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="7251b-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="7251b-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="7251b-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="7251b-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7251b-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="7251b-127">Minimum Shader Model</span></span>

<span data-ttu-id="7251b-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="7251b-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7251b-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="7251b-129">Shader Model</span></span>                                                                       | <span data-ttu-id="7251b-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="7251b-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="7251b-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="7251b-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="7251b-132">Oui</span><span class="sxs-lookup"><span data-stu-id="7251b-132">yes</span></span>                 |
| [<span data-ttu-id="7251b-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7251b-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="7251b-134">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="7251b-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="7251b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7251b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7251b-136">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="7251b-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

