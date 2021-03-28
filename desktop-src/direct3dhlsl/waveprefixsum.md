---
title: Fonction WavePrefixSum
description: Retourne la somme de toutes les valeurs des couloirs actifs avec des index plus petits que celui-ci.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- WavePrefixSum fonction HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/31/2021
ms.locfileid: "104973863"
---
# <a name="waveprefixsum-function"></a><span data-ttu-id="3d7cd-104">Fonction WavePrefixSum</span><span class="sxs-lookup"><span data-stu-id="3d7cd-104">WavePrefixSum function</span></span>

<span data-ttu-id="3d7cd-105">Retourne la somme de toutes les valeurs des couloirs actifs avec des index plus petits que celui-ci.</span><span class="sxs-lookup"><span data-stu-id="3d7cd-105">Returns the sum of all of the values in the active lanes with smaller indices than this one.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d7cd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d7cd-106">Syntax</span></span>

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="3d7cd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d7cd-107">Parameters</span></span>

<span data-ttu-id="3d7cd-108">*value*</span><span class="sxs-lookup"><span data-stu-id="3d7cd-108">*value*</span></span> 

<span data-ttu-id="3d7cd-109">Valeur à additionner.</span><span class="sxs-lookup"><span data-stu-id="3d7cd-109">The value to sum up.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d7cd-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3d7cd-110">Return value</span></span>

<span data-ttu-id="3d7cd-111">Somme des valeurs.</span><span class="sxs-lookup"><span data-stu-id="3d7cd-111">The sum of the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d7cd-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3d7cd-112">Remarks</span></span>

<span data-ttu-id="3d7cd-113">L’ordre des opérations sur cette routine ne peut pas être garanti.</span><span class="sxs-lookup"><span data-stu-id="3d7cd-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="3d7cd-114">Ainsi, en fait, \[ l' \] indicateur précis est ignoré dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="3d7cd-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="3d7cd-115">Une somme suffixée peut être calculée en ajoutant la somme du préfixe à la valeur de la voie actuelle.</span><span class="sxs-lookup"><span data-stu-id="3d7cd-115">A postfix sum can be computed by adding the prefix sum to the current lane's value.</span></span>

<span data-ttu-id="3d7cd-116">Notez que la voie active avec l’index le plus bas reçoit toujours 0 pour sa somme de préfixe.</span><span class="sxs-lookup"><span data-stu-id="3d7cd-116">Note that the active lane with the lowest index will always receive a 0 for its prefix sum.</span></span>

<span data-ttu-id="3d7cd-117">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3d7cd-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="3d7cd-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="3d7cd-118">Examples</span></span>

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

<span data-ttu-id="3d7cd-119">Sur un ordinateur doté d’une taille d’onde de 8, et de tous les couloirs actifs, à l’exception des couloirs 0 et 4, les valeurs suivantes sont retournées à partir de WavePrefixSum.</span><span class="sxs-lookup"><span data-stu-id="3d7cd-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixSum.</span></span>

| <span data-ttu-id="3d7cd-120">index Lane</span><span class="sxs-lookup"><span data-stu-id="3d7cd-120">lane index</span></span> | <span data-ttu-id="3d7cd-121">status</span><span class="sxs-lookup"><span data-stu-id="3d7cd-121">status</span></span>   | <span data-ttu-id="3d7cd-122">prefixSum</span><span class="sxs-lookup"><span data-stu-id="3d7cd-122">prefixSum</span></span>     | 
|------------|----------|---------------|
| <span data-ttu-id="3d7cd-123">0</span><span class="sxs-lookup"><span data-stu-id="3d7cd-123">0</span></span>          | <span data-ttu-id="3d7cd-124">inactive</span><span class="sxs-lookup"><span data-stu-id="3d7cd-124">inactive</span></span> | <span data-ttu-id="3d7cd-125">n/a</span><span class="sxs-lookup"><span data-stu-id="3d7cd-125">n/a</span></span>           |
| <span data-ttu-id="3d7cd-126">1</span><span class="sxs-lookup"><span data-stu-id="3d7cd-126">1</span></span>          | <span data-ttu-id="3d7cd-127">active</span><span class="sxs-lookup"><span data-stu-id="3d7cd-127">active</span></span>   | <span data-ttu-id="3d7cd-128">= 0</span><span class="sxs-lookup"><span data-stu-id="3d7cd-128">= 0</span></span>           |
| <span data-ttu-id="3d7cd-129">2</span><span class="sxs-lookup"><span data-stu-id="3d7cd-129">2</span></span>          | <span data-ttu-id="3d7cd-130">active</span><span class="sxs-lookup"><span data-stu-id="3d7cd-130">active</span></span>   | <span data-ttu-id="3d7cd-131">= 0 + 2</span><span class="sxs-lookup"><span data-stu-id="3d7cd-131">= 0+2</span></span>         |
| <span data-ttu-id="3d7cd-132">3</span><span class="sxs-lookup"><span data-stu-id="3d7cd-132">3</span></span>          | <span data-ttu-id="3d7cd-133">active</span><span class="sxs-lookup"><span data-stu-id="3d7cd-133">active</span></span>   | <span data-ttu-id="3d7cd-134">= 0 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="3d7cd-134">= 0+2+2</span></span>       |
| <span data-ttu-id="3d7cd-135">4</span><span class="sxs-lookup"><span data-stu-id="3d7cd-135">4</span></span>          | <span data-ttu-id="3d7cd-136">inactive</span><span class="sxs-lookup"><span data-stu-id="3d7cd-136">inactive</span></span> | <span data-ttu-id="3d7cd-137">n/a</span><span class="sxs-lookup"><span data-stu-id="3d7cd-137">n/a</span></span>           |
| <span data-ttu-id="3d7cd-138">5</span><span class="sxs-lookup"><span data-stu-id="3d7cd-138">5</span></span>          | <span data-ttu-id="3d7cd-139">active</span><span class="sxs-lookup"><span data-stu-id="3d7cd-139">active</span></span>   | <span data-ttu-id="3d7cd-140">= 0 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="3d7cd-140">= 0+2+2+2</span></span>     |
| <span data-ttu-id="3d7cd-141">6</span><span class="sxs-lookup"><span data-stu-id="3d7cd-141">6</span></span>          | <span data-ttu-id="3d7cd-142">active</span><span class="sxs-lookup"><span data-stu-id="3d7cd-142">active</span></span>   | <span data-ttu-id="3d7cd-143">= 0 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="3d7cd-143">= 0+2+2+2+2</span></span>   |
| <span data-ttu-id="3d7cd-144">7</span><span class="sxs-lookup"><span data-stu-id="3d7cd-144">7</span></span>          | <span data-ttu-id="3d7cd-145">active</span><span class="sxs-lookup"><span data-stu-id="3d7cd-145">active</span></span>   | <span data-ttu-id="3d7cd-146">= 0 + 2 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="3d7cd-146">= 0+2+2+2+2+2</span></span> |

## <a name="see-also"></a><span data-ttu-id="3d7cd-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d7cd-147">See also</span></span>

[<span data-ttu-id="3d7cd-148">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="3d7cd-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="3d7cd-149">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="3d7cd-149">Shader Model 6</span></span>](shader-model-6-0.md)
