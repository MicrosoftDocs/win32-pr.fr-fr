---
title: clip
description: Ignore le pixel actuel si la valeur spécifiée est inférieure à zéro.
ms.assetid: c9f84a27-5572-45aa-a12f-4446614b7be5
keywords:
- découpage HLSL
topic_type:
- apiref
api_name:
- clip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92a75f2839dbbb605d976e07fffa5c2f9b27fd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971731"
---
# <a name="clip"></a><span data-ttu-id="fa98a-104">clip</span><span class="sxs-lookup"><span data-stu-id="fa98a-104">clip</span></span>

<span data-ttu-id="fa98a-105">Ignore le pixel actuel si la valeur spécifiée est inférieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="fa98a-105">Discards the current pixel if the specified value is less than zero.</span></span>



| <span data-ttu-id="fa98a-106">clip (*x*)</span><span class="sxs-lookup"><span data-stu-id="fa98a-106">clip(*x*)</span></span> |
|-----------|



 

## <a name="parameters"></a><span data-ttu-id="fa98a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa98a-107">Parameters</span></span>



| <span data-ttu-id="fa98a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="fa98a-108">Item</span></span>                                                   | <span data-ttu-id="fa98a-109">Description</span><span class="sxs-lookup"><span data-stu-id="fa98a-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="fa98a-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="fa98a-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="fa98a-111">\[dans \] la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fa98a-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="fa98a-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fa98a-112">Return Value</span></span>

<span data-ttu-id="fa98a-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fa98a-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa98a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="fa98a-114">Remarks</span></span>

<span data-ttu-id="fa98a-115">Utilisez la fonction intrinsèque **clip** HLSL pour simuler des plans de découpage si chaque composant du paramètre *x* représente la distance à partir d’un plan.</span><span class="sxs-lookup"><span data-stu-id="fa98a-115">Use the **clip** HLSL intrinsic function to simulate clipping planes if each component of the *x* parameter represents the distance from a plane.</span></span>

<span data-ttu-id="fa98a-116">Utilisez également la fonction **clip** pour tester le comportement alpha, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="fa98a-116">Also, use the **clip** function to test for alpha behavior, as shown in the following example:</span></span>


```
clip( Input.Color.A < 0.1f ? -1:1 );
```



## <a name="type-description"></a><span data-ttu-id="fa98a-117">Description du type</span><span class="sxs-lookup"><span data-stu-id="fa98a-117">Type Description</span></span>



| <span data-ttu-id="fa98a-118">Nom</span><span class="sxs-lookup"><span data-stu-id="fa98a-118">Name</span></span> | [<span data-ttu-id="fa98a-119">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="fa98a-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="fa98a-120">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="fa98a-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="fa98a-121">Taille</span><span class="sxs-lookup"><span data-stu-id="fa98a-121">Size</span></span> |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="fa98a-122">*x*</span><span class="sxs-lookup"><span data-stu-id="fa98a-122">*x*</span></span>  | <span data-ttu-id="fa98a-123">[**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice**</span><span class="sxs-lookup"><span data-stu-id="fa98a-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="fa98a-124">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="fa98a-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="fa98a-125">n'importe laquelle</span><span class="sxs-lookup"><span data-stu-id="fa98a-125">any</span></span>  |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fa98a-126">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="fa98a-126">Minimum Shader Model</span></span>

<span data-ttu-id="fa98a-127">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="fa98a-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fa98a-128">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="fa98a-128">Shader Model</span></span>                                              | <span data-ttu-id="fa98a-129">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="fa98a-129">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="fa98a-130">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="fa98a-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fa98a-131">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="fa98a-131">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="fa98a-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa98a-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fa98a-133">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="fa98a-133">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="fa98a-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa98a-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fa98a-135">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="fa98a-135">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="fa98a-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa98a-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fa98a-137">Oui (nuanceur de pixels uniquement)</span><span class="sxs-lookup"><span data-stu-id="fa98a-137">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="fa98a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa98a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa98a-139">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="fa98a-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

