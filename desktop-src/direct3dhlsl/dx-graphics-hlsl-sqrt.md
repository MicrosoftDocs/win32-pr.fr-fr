---
title: sqrt
description: Retourne la racine carrée de la valeur à virgule flottante spécifiée, par composant.
ms.assetid: e8debc60-1441-4974-9ab3-6d1c2217caaf
keywords:
- langage HLSL racine
topic_type:
- apiref
api_name:
- sqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff3c872dac6da28a1ec92993e387bd23daec7f86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104381987"
---
# <a name="sqrt"></a><span data-ttu-id="cc7ac-104">sqrt</span><span class="sxs-lookup"><span data-stu-id="cc7ac-104">sqrt</span></span>

<span data-ttu-id="cc7ac-105">Retourne la racine carrée de la valeur à virgule flottante spécifiée, par composant.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-105">Returns the square root of the specified floating-point value, per component.</span></span>



| <span data-ttu-id="cc7ac-106">*RET* racine (*x*)</span><span class="sxs-lookup"><span data-stu-id="cc7ac-106">*ret* sqrt(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="cc7ac-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc7ac-107">Parameters</span></span>



| <span data-ttu-id="cc7ac-108">Élément</span><span class="sxs-lookup"><span data-stu-id="cc7ac-108">Item</span></span>                                                   | <span data-ttu-id="cc7ac-109">Description</span><span class="sxs-lookup"><span data-stu-id="cc7ac-109">Description</span></span>                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="cc7ac-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="cc7ac-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="cc7ac-111">\[dans \] la valeur à virgule flottante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-111">\[in\] The specified floating-point value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="cc7ac-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc7ac-112">Return Value</span></span>

<span data-ttu-id="cc7ac-113">Racine carrée du paramètre *x* , par composant.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-113">The square root of the *x* parameter, per component.</span></span>

## <a name="type-description"></a><span data-ttu-id="cc7ac-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="cc7ac-114">Type Description</span></span>



| <span data-ttu-id="cc7ac-115">Nom</span><span class="sxs-lookup"><span data-stu-id="cc7ac-115">Name</span></span>  | [<span data-ttu-id="cc7ac-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="cc7ac-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="cc7ac-118">Taille</span><span class="sxs-lookup"><span data-stu-id="cc7ac-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="cc7ac-119">*x*</span><span class="sxs-lookup"><span data-stu-id="cc7ac-119">*x*</span></span>   | <span data-ttu-id="cc7ac-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="cc7ac-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="cc7ac-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="cc7ac-122">any</span></span>                            |
| <span data-ttu-id="cc7ac-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="cc7ac-123">*ret*</span></span> | <span data-ttu-id="cc7ac-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="cc7ac-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="cc7ac-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="cc7ac-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="cc7ac-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cc7ac-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="cc7ac-127">Minimum Shader Model</span></span>

<span data-ttu-id="cc7ac-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cc7ac-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="cc7ac-129">Shader Model</span></span>                                                                       | <span data-ttu-id="cc7ac-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="cc7ac-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="cc7ac-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="cc7ac-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="cc7ac-132">Oui</span><span class="sxs-lookup"><span data-stu-id="cc7ac-132">yes</span></span>                 |
| [<span data-ttu-id="cc7ac-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc7ac-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="cc7ac-134">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="cc7ac-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="cc7ac-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc7ac-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc7ac-136">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

