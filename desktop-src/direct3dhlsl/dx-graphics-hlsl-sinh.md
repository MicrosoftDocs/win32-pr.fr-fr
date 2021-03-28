---
title: sinh
description: Retourne le sinus hyperbolique de la valeur spécifiée.
ms.assetid: 8a9e11a3-582f-4680-a5bd-ecde90560db3
keywords:
- LANGAGE de l’sinh
topic_type:
- apiref
api_name:
- sinh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbf6c5e04eb248c81782ba236010298ebb9564db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031715"
---
# <a name="sinh"></a><span data-ttu-id="8937a-104">sinh</span><span class="sxs-lookup"><span data-stu-id="8937a-104">sinh</span></span>

<span data-ttu-id="8937a-105">Retourne le sinus hyperbolique de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8937a-105">Returns the hyperbolic sine of the specified value.</span></span>



| <span data-ttu-id="8937a-106">*RET* sinh (*x*)</span><span class="sxs-lookup"><span data-stu-id="8937a-106">*ret* sinh(*x*)</span></span> |
|-----------------|



 

## <a name="parameters"></a><span data-ttu-id="8937a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8937a-107">Parameters</span></span>



| <span data-ttu-id="8937a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="8937a-108">Item</span></span>                                                   | <span data-ttu-id="8937a-109">Description</span><span class="sxs-lookup"><span data-stu-id="8937a-109">Description</span></span>                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="8937a-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="8937a-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8937a-111">\[dans \] la valeur spécifiée, en radians.</span><span class="sxs-lookup"><span data-stu-id="8937a-111">\[in\] The specified value, in radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8937a-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8937a-112">Return Value</span></span>

<span data-ttu-id="8937a-113">Sinus hyperbolique du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="8937a-113">The hyperbolic sine of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="8937a-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="8937a-114">Type Description</span></span>



| <span data-ttu-id="8937a-115">Nom</span><span class="sxs-lookup"><span data-stu-id="8937a-115">Name</span></span>  | [<span data-ttu-id="8937a-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="8937a-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8937a-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="8937a-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8937a-118">Taille</span><span class="sxs-lookup"><span data-stu-id="8937a-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="8937a-119">*x*</span><span class="sxs-lookup"><span data-stu-id="8937a-119">*x*</span></span>   | <span data-ttu-id="8937a-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="8937a-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="8937a-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="8937a-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8937a-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="8937a-122">any</span></span>                            |
| <span data-ttu-id="8937a-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="8937a-123">*ret*</span></span> | <span data-ttu-id="8937a-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="8937a-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="8937a-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="8937a-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8937a-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="8937a-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8937a-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="8937a-127">Minimum Shader Model</span></span>

<span data-ttu-id="8937a-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="8937a-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8937a-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8937a-129">Shader Model</span></span>                                                                       | <span data-ttu-id="8937a-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="8937a-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="8937a-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="8937a-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="8937a-132">Oui</span><span class="sxs-lookup"><span data-stu-id="8937a-132">yes</span></span>                 |
| [<span data-ttu-id="8937a-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8937a-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="8937a-134">Oui (vs \_ 1 \_ 1 uniquement)</span><span class="sxs-lookup"><span data-stu-id="8937a-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="8937a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8937a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8937a-136">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8937a-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

