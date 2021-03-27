---
title: exp
description: Retourne la valeur exponentielle de base e (ou ex) de la valeur spécifiée.
ms.assetid: 7a713251-af47-4f8d-b708-40309b80ba18
keywords:
- ATT (HLSL)
topic_type:
- apiref
api_name:
- exp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 699eb97ae0fd6bbdeba0da47693178d1e4c48e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727860"
---
# <a name="exp"></a><span data-ttu-id="ece36-104">exp</span><span class="sxs-lookup"><span data-stu-id="ece36-104">exp</span></span>

<span data-ttu-id="ece36-105">Retourne l’exponentiel de base e (ou e<sup>x</sup>) de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ece36-105">Returns the base-e exponential, or e<sup>x</sup>, of the specified value.</span></span>



| <span data-ttu-id="ece36-106">*RET* exp (*x*)</span><span class="sxs-lookup"><span data-stu-id="ece36-106">*ret* exp(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="ece36-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ece36-107">Parameters</span></span>



| <span data-ttu-id="ece36-108">Élément</span><span class="sxs-lookup"><span data-stu-id="ece36-108">Item</span></span>                                                   | <span data-ttu-id="ece36-109">Description</span><span class="sxs-lookup"><span data-stu-id="ece36-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="ece36-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="ece36-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ece36-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ece36-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ece36-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ece36-112">Return Value</span></span>

<span data-ttu-id="ece36-113">Exponentiel de base e du paramètre *x* .</span><span class="sxs-lookup"><span data-stu-id="ece36-113">The base-e exponential of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="ece36-114">Description du type</span><span class="sxs-lookup"><span data-stu-id="ece36-114">Type Description</span></span>



| <span data-ttu-id="ece36-115">Nom</span><span class="sxs-lookup"><span data-stu-id="ece36-115">Name</span></span>  | [<span data-ttu-id="ece36-116">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="ece36-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="ece36-117">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="ece36-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ece36-118">Taille</span><span class="sxs-lookup"><span data-stu-id="ece36-118">Size</span></span>                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="ece36-119">*x*</span><span class="sxs-lookup"><span data-stu-id="ece36-119">*x*</span></span>   | <span data-ttu-id="ece36-120">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="ece36-120">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="ece36-121">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="ece36-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ece36-122">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="ece36-122">any</span></span>                            |
| <span data-ttu-id="ece36-123">*Av*</span><span class="sxs-lookup"><span data-stu-id="ece36-123">*ret*</span></span> | <span data-ttu-id="ece36-124">identique à l’entrée *x*</span><span class="sxs-lookup"><span data-stu-id="ece36-124">same as input *x*</span></span>                                                                                              | [<span data-ttu-id="ece36-125">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="ece36-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ece36-126">la ou les mêmes dimensions comme entrée *x*</span><span class="sxs-lookup"><span data-stu-id="ece36-126">same dimension(s) as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ece36-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="ece36-127">Minimum Shader Model</span></span>

<span data-ttu-id="ece36-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="ece36-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ece36-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="ece36-129">Shader Model</span></span>                                                                       | <span data-ttu-id="ece36-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="ece36-130">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ece36-131">[Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="ece36-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ece36-132">Oui</span><span class="sxs-lookup"><span data-stu-id="ece36-132">yes</span></span>       |
| [<span data-ttu-id="ece36-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ece36-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ece36-134">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ece36-134">vs\_1\_1</span></span>  |



 

## <a name="see-also"></a><span data-ttu-id="ece36-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ece36-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece36-136">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ece36-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

