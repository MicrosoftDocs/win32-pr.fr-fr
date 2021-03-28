---
title: degrés
description: Convertit la valeur spécifiée de radians en degrés.
ms.assetid: e60a3ec4-9177-457a-8314-a5788f353633
keywords:
- degrés HLSL
topic_type:
- apiref
api_name:
- degrees
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47d8bba0ee43da81a18baaeaffca0e3c917e460d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382146"
---
# <a name="degrees"></a><span data-ttu-id="d9b9d-104">degrés</span><span class="sxs-lookup"><span data-stu-id="d9b9d-104">degrees</span></span>

<span data-ttu-id="d9b9d-105">Convertit la valeur spécifiée de radians en degrés.</span><span class="sxs-lookup"><span data-stu-id="d9b9d-105">Converts the specified value from radians to degrees.</span></span>



| <span data-ttu-id="d9b9d-106">*RET* degrés (*x*)</span><span class="sxs-lookup"><span data-stu-id="d9b9d-106">*ret* degrees(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="d9b9d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9b9d-107">Parameters</span></span>



| <span data-ttu-id="d9b9d-108">Élément</span><span class="sxs-lookup"><span data-stu-id="d9b9d-108">Item</span></span>                                                   | <span data-ttu-id="d9b9d-109">Description</span><span class="sxs-lookup"><span data-stu-id="d9b9d-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="d9b9d-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="d9b9d-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="d9b9d-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d9b9d-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d9b9d-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d9b9d-112">Return Value</span></span>

<span data-ttu-id="d9b9d-113">Résultat de la conversion du paramètre *x* de radians en degrés.</span><span class="sxs-lookup"><span data-stu-id="d9b9d-113">The result of converting the *x* parameter from radians to degrees.</span></span>

## <a name="type-description"></a><span data-ttu-id="d9b9d-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="d9b9d-114">Type Description</span></span>



| <span data-ttu-id="d9b9d-115">Nom</span><span class="sxs-lookup"><span data-stu-id="d9b9d-115">Name</span></span>  | [<span data-ttu-id="d9b9d-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="d9b9d-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="d9b9d-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="d9b9d-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d9b9d-118">Taille</span><span class="sxs-lookup"><span data-stu-id="d9b9d-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="d9b9d-119">*x*</span><span class="sxs-lookup"><span data-stu-id="d9b9d-119">*x*</span></span>   | <span data-ttu-id="d9b9d-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="d9b9d-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="d9b9d-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d9b9d-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d9b9d-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="d9b9d-122">any</span></span>                            |
| <span data-ttu-id="d9b9d-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="d9b9d-123">*ret*</span></span> | <span data-ttu-id="d9b9d-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="d9b9d-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="d9b9d-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="d9b9d-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d9b9d-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="d9b9d-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d9b9d-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="d9b9d-127">Minimum Shader Model</span></span>

<span data-ttu-id="d9b9d-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="d9b9d-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d9b9d-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="d9b9d-129">Shader Model</span></span>                                                                       | <span data-ttu-id="d9b9d-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="d9b9d-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d9b9d-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="d9b9d-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d9b9d-132">Oui</span><span class="sxs-lookup"><span data-stu-id="d9b9d-132">yes</span></span>       |
| [<span data-ttu-id="d9b9d-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9b9d-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d9b9d-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d9b9d-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="d9b9d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9b9d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b9d-136">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d9b9d-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

