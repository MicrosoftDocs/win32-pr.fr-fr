---
title: saturation (référence HLSL)
description: Fixe la valeur spécifiée dans la plage comprise entre 0 et 1.
ms.assetid: efe4dedd-732a-4643-8a57-61814434f6ff
keywords:
- saturer le HLSL
topic_type:
- apiref
api_name:
- saturate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 609443bdc1d0cff6a4c81c8eb26d86a30ea1e721
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315186"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="8673e-104">saturation (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="8673e-104">saturate (HLSL reference)</span></span>

<span data-ttu-id="8673e-105">Fixe la valeur spécifiée dans la plage comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="8673e-105">Clamps the specified value within the range of 0 to 1.</span></span>



| <span data-ttu-id="8673e-106">*RET* saturé (*x*)</span><span class="sxs-lookup"><span data-stu-id="8673e-106">*ret* saturate(*x*)</span></span> |
|---------------------|



 

## <a name="parameters"></a><span data-ttu-id="8673e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8673e-107">Parameters</span></span>



| <span data-ttu-id="8673e-108">Élément</span><span class="sxs-lookup"><span data-stu-id="8673e-108">Item</span></span>                                                   | <span data-ttu-id="8673e-109">Description</span><span class="sxs-lookup"><span data-stu-id="8673e-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="8673e-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="8673e-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8673e-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8673e-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8673e-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8673e-112">Return Value</span></span>

<span data-ttu-id="8673e-113">Paramètre *x* , ancré dans la plage comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="8673e-113">The *x* parameter, clamped within the range of 0 to 1.</span></span>

## <a name="type-description"></a><span data-ttu-id="8673e-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="8673e-114">Type Description</span></span>



| <span data-ttu-id="8673e-115">Nom</span><span class="sxs-lookup"><span data-stu-id="8673e-115">Name</span></span>  | [<span data-ttu-id="8673e-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="8673e-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8673e-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="8673e-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8673e-118">Taille</span><span class="sxs-lookup"><span data-stu-id="8673e-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8673e-119">*x*</span><span class="sxs-lookup"><span data-stu-id="8673e-119">*x*</span></span>   | <span data-ttu-id="8673e-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="8673e-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="8673e-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="8673e-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8673e-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="8673e-122">any</span></span>                            |
| <span data-ttu-id="8673e-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="8673e-123">*ret*</span></span> | <span data-ttu-id="8673e-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="8673e-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="8673e-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="8673e-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8673e-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="8673e-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8673e-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="8673e-127">Minimum Shader Model</span></span>

<span data-ttu-id="8673e-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="8673e-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8673e-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8673e-129">Shader Model</span></span>                                                                       | <span data-ttu-id="8673e-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="8673e-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8673e-131">[Nuancier Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="8673e-131">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="8673e-132">Oui</span><span class="sxs-lookup"><span data-stu-id="8673e-132">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8673e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8673e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8673e-134">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8673e-134">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

