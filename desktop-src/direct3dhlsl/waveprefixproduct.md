---
title: Fonction WavePrefixProduct
description: Retourne le produit de toutes les valeurs des couloirs actifs dans cette vague avec des index inférieurs à ce couloir.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- WavePrefixProduct fonction HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383283"
---
# <a name="waveprefixproduct-function"></a><span data-ttu-id="ad82e-104">Fonction WavePrefixProduct</span><span class="sxs-lookup"><span data-stu-id="ad82e-104">WavePrefixProduct function</span></span>

<span data-ttu-id="ad82e-105">Retourne le produit de toutes les valeurs des couloirs actifs dans cette vague avec des index inférieurs à ce couloir.</span><span class="sxs-lookup"><span data-stu-id="ad82e-105">Returns the product of all of the values in the active lanes in this wave with indices less than this lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad82e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad82e-106">Syntax</span></span>

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="ad82e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad82e-107">Parameters</span></span>

<span data-ttu-id="ad82e-108">*value*</span><span class="sxs-lookup"><span data-stu-id="ad82e-108">*value*</span></span> 

<span data-ttu-id="ad82e-109">Valeur à multiplier.</span><span class="sxs-lookup"><span data-stu-id="ad82e-109">The value to multiply.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad82e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad82e-110">Return value</span></span>

<span data-ttu-id="ad82e-111">Produit de toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="ad82e-111">The product of all the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad82e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ad82e-112">Remarks</span></span>

<span data-ttu-id="ad82e-113">L’ordre des opérations sur cette routine ne peut pas être garanti.</span><span class="sxs-lookup"><span data-stu-id="ad82e-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="ad82e-114">Ainsi, en fait, \[ l' \] indicateur précis est ignoré dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="ad82e-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="ad82e-115">Un produit postfix peut être calculé en multipliant le préfixe produit par la valeur de la voie actuelle.</span><span class="sxs-lookup"><span data-stu-id="ad82e-115">A postfix product can be computed by multiplying the prefix product by the current lane's value.</span></span>

<span data-ttu-id="ad82e-116">Notez que la voie active avec l’index le plus bas reçoit toujours 1 pour son préfixe Product.</span><span class="sxs-lookup"><span data-stu-id="ad82e-116">Note that the active lane with the lowest index will always receive a 1 for its prefix product.</span></span>

<span data-ttu-id="ad82e-117">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ad82e-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="ad82e-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="ad82e-118">Examples</span></span>

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

<span data-ttu-id="ad82e-119">Sur un ordinateur doté d’une taille d’onde de 8, et de tous les couloirs actifs, à l’exception des couloirs 0 et 4, les valeurs suivantes sont retournées à partir de WavePrefixProduct.</span><span class="sxs-lookup"><span data-stu-id="ad82e-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixProduct.</span></span>

| <span data-ttu-id="ad82e-120">index Lane</span><span class="sxs-lookup"><span data-stu-id="ad82e-120">lane index</span></span> | <span data-ttu-id="ad82e-121">status</span><span class="sxs-lookup"><span data-stu-id="ad82e-121">status</span></span>   | <span data-ttu-id="ad82e-122">prefixProduct</span><span class="sxs-lookup"><span data-stu-id="ad82e-122">prefixProduct</span></span> | 
|------------|----------|---------------|
| <span data-ttu-id="ad82e-123">0</span><span class="sxs-lookup"><span data-stu-id="ad82e-123">0</span></span>          | <span data-ttu-id="ad82e-124">inactive</span><span class="sxs-lookup"><span data-stu-id="ad82e-124">inactive</span></span> | <span data-ttu-id="ad82e-125">n/a</span><span class="sxs-lookup"><span data-stu-id="ad82e-125">n/a</span></span>           |
| <span data-ttu-id="ad82e-126">1</span><span class="sxs-lookup"><span data-stu-id="ad82e-126">1</span></span>          | <span data-ttu-id="ad82e-127">active</span><span class="sxs-lookup"><span data-stu-id="ad82e-127">active</span></span>   | <span data-ttu-id="ad82e-128">= 1</span><span class="sxs-lookup"><span data-stu-id="ad82e-128">= 1</span></span>           |
| <span data-ttu-id="ad82e-129">2</span><span class="sxs-lookup"><span data-stu-id="ad82e-129">2</span></span>          | <span data-ttu-id="ad82e-130">active</span><span class="sxs-lookup"><span data-stu-id="ad82e-130">active</span></span>   | <span data-ttu-id="ad82e-131">= 1 \* 2</span><span class="sxs-lookup"><span data-stu-id="ad82e-131">= 1\*2</span></span>        |
| <span data-ttu-id="ad82e-132">3</span><span class="sxs-lookup"><span data-stu-id="ad82e-132">3</span></span>          | <span data-ttu-id="ad82e-133">active</span><span class="sxs-lookup"><span data-stu-id="ad82e-133">active</span></span>   | <span data-ttu-id="ad82e-134">= 1 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="ad82e-134">= 1\*2\*2</span></span>     |
| <span data-ttu-id="ad82e-135">4</span><span class="sxs-lookup"><span data-stu-id="ad82e-135">4</span></span>          | <span data-ttu-id="ad82e-136">inactive</span><span class="sxs-lookup"><span data-stu-id="ad82e-136">inactive</span></span> | <span data-ttu-id="ad82e-137">n/a</span><span class="sxs-lookup"><span data-stu-id="ad82e-137">n/a</span></span>           |
| <span data-ttu-id="ad82e-138">5</span><span class="sxs-lookup"><span data-stu-id="ad82e-138">5</span></span>          | <span data-ttu-id="ad82e-139">active</span><span class="sxs-lookup"><span data-stu-id="ad82e-139">active</span></span>   | <span data-ttu-id="ad82e-140">= 1 \* 2 \* 2 2 \*</span><span class="sxs-lookup"><span data-stu-id="ad82e-140">= 1\*2\*2\*2</span></span>       |
| <span data-ttu-id="ad82e-141">6</span><span class="sxs-lookup"><span data-stu-id="ad82e-141">6</span></span>          | <span data-ttu-id="ad82e-142">active</span><span class="sxs-lookup"><span data-stu-id="ad82e-142">active</span></span>   | <span data-ttu-id="ad82e-143">= 1 \* 2 \* 2 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="ad82e-143">= 1\*2\*2\*2\*2</span></span>    |
| <span data-ttu-id="ad82e-144">7</span><span class="sxs-lookup"><span data-stu-id="ad82e-144">7</span></span>          | <span data-ttu-id="ad82e-145">active</span><span class="sxs-lookup"><span data-stu-id="ad82e-145">active</span></span>   | <span data-ttu-id="ad82e-146">= 1 \* 2 \* 2 \* 2 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="ad82e-146">= 1\*2\*2\*2\*2\*2</span></span> |

## <a name="see-also"></a><span data-ttu-id="ad82e-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad82e-147">See also</span></span>

[<span data-ttu-id="ad82e-148">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="ad82e-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="ad82e-149">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="ad82e-149">Shader Model 6</span></span>](shader-model-6-0.md)
