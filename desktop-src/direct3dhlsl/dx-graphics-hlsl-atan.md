---
title: atan
description: Retourne l’arc tangente de la valeur spécifiée.
ms.assetid: e3ce3ac3-1012-414f-a193-102208083e39
keywords:
- ATAN (HLSL)
topic_type:
- apiref
api_name:
- atan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 290ced1e5100e3bbc780fab6ab984deaca38528f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727868"
---
# <a name="atan"></a><span data-ttu-id="8d32b-104">atan</span><span class="sxs-lookup"><span data-stu-id="8d32b-104">atan</span></span>

<span data-ttu-id="8d32b-105">Retourne l’arc tangente de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8d32b-105">Returns the arctangent of the specified value.</span></span>



| <span data-ttu-id="8d32b-106">*RET* ATAN (*x*)</span><span class="sxs-lookup"><span data-stu-id="8d32b-106">*ret* atan(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="8d32b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d32b-107">Parameters</span></span>



| <span data-ttu-id="8d32b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="8d32b-108">Item</span></span>                                                   | <span data-ttu-id="8d32b-109">Description</span><span class="sxs-lookup"><span data-stu-id="8d32b-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="8d32b-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="8d32b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8d32b-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8d32b-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8d32b-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8d32b-112">Return Value</span></span>

<span data-ttu-id="8d32b-113">Arctangente du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="8d32b-113">The arctangent of the *x* parameter.</span></span> <span data-ttu-id="8d32b-114">Cette valeur est comprise entre-π/2 et π/2.</span><span class="sxs-lookup"><span data-stu-id="8d32b-114">This value is within the range of -π/2 to π/2.</span></span>

## <a name="type-description"></a><span data-ttu-id="8d32b-115">Description du type</span><span class="sxs-lookup"><span data-stu-id="8d32b-115">Type Description</span></span>



| <span data-ttu-id="8d32b-116">Nom</span><span class="sxs-lookup"><span data-stu-id="8d32b-116">Name</span></span>  | [<span data-ttu-id="8d32b-117">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="8d32b-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8d32b-118">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="8d32b-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8d32b-119">Taille</span><span class="sxs-lookup"><span data-stu-id="8d32b-119">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8d32b-120">*x*</span><span class="sxs-lookup"><span data-stu-id="8d32b-120">*x*</span></span>   | <span data-ttu-id="8d32b-121">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="8d32b-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="8d32b-122">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="8d32b-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8d32b-123">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="8d32b-123">any</span></span>                            |
| <span data-ttu-id="8d32b-124">*Av*</span><span class="sxs-lookup"><span data-stu-id="8d32b-124">*ret*</span></span> | <span data-ttu-id="8d32b-125">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="8d32b-125">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="8d32b-126">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="8d32b-126">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8d32b-127">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="8d32b-127">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8d32b-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="8d32b-128">Minimum Shader Model</span></span>

<span data-ttu-id="8d32b-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="8d32b-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8d32b-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8d32b-130">Shader Model</span></span>                                                                       | <span data-ttu-id="8d32b-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="8d32b-131">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8d32b-132">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="8d32b-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="8d32b-133">Oui</span><span class="sxs-lookup"><span data-stu-id="8d32b-133">yes</span></span>       |
| [<span data-ttu-id="8d32b-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d32b-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8d32b-135">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="8d32b-135">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="8d32b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d32b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d32b-137">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8d32b-137">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

