---
title: radians
description: Convertit la valeur spécifiée de degrés en radians.
ms.assetid: 6fc6b1f8-b686-49ba-93ea-2b2470b3fc72
keywords:
- radians HLSL
topic_type:
- apiref
api_name:
- radians
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 029c0ffe2838cdcc997e47cae4e0adafede4411d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382748"
---
# <a name="radians"></a><span data-ttu-id="160a9-104">radians</span><span class="sxs-lookup"><span data-stu-id="160a9-104">radians</span></span>

<span data-ttu-id="160a9-105">Convertit la valeur spécifiée de degrés en radians.</span><span class="sxs-lookup"><span data-stu-id="160a9-105">Converts the specified value from degrees to radians.</span></span>



| <span data-ttu-id="160a9-106">*RET* en radians (*x*)</span><span class="sxs-lookup"><span data-stu-id="160a9-106">*ret* radians(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="160a9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="160a9-107">Parameters</span></span>



| <span data-ttu-id="160a9-108">Élément</span><span class="sxs-lookup"><span data-stu-id="160a9-108">Item</span></span>                                                   | <span data-ttu-id="160a9-109">Description</span><span class="sxs-lookup"><span data-stu-id="160a9-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="160a9-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="160a9-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="160a9-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="160a9-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="160a9-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="160a9-112">Return Value</span></span>

<span data-ttu-id="160a9-113">Paramètre *x* converti de degrés en radians.</span><span class="sxs-lookup"><span data-stu-id="160a9-113">The *x* parameter converted from degrees to radians.</span></span>

## <a name="type-description"></a><span data-ttu-id="160a9-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="160a9-114">Type Description</span></span>



| <span data-ttu-id="160a9-115">Nom</span><span class="sxs-lookup"><span data-stu-id="160a9-115">Name</span></span>  | [<span data-ttu-id="160a9-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="160a9-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="160a9-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="160a9-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="160a9-118">Taille</span><span class="sxs-lookup"><span data-stu-id="160a9-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="160a9-119">*x*</span><span class="sxs-lookup"><span data-stu-id="160a9-119">*x*</span></span>   | <span data-ttu-id="160a9-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="160a9-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="160a9-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="160a9-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="160a9-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="160a9-122">any</span></span>                            |
| <span data-ttu-id="160a9-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="160a9-123">*ret*</span></span> | <span data-ttu-id="160a9-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="160a9-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="160a9-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="160a9-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="160a9-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="160a9-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="160a9-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="160a9-127">Minimum Shader Model</span></span>

<span data-ttu-id="160a9-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="160a9-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="160a9-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="160a9-129">Shader Model</span></span>                                                                       | <span data-ttu-id="160a9-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="160a9-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="160a9-131">[Nuancier Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="160a9-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="160a9-132">Oui</span><span class="sxs-lookup"><span data-stu-id="160a9-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="160a9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="160a9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="160a9-134">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="160a9-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

