---
title: WaveActiveMin fonction)
description: Retourne la valeur minimale de l’expression sur tous les couloirs actifs de l’onde actuelle pour la répliquer à tous les couloirs actifs.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- WaveActiveMin fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032090"
---
# <a name="waveactivemin-function"></a><span data-ttu-id="62a7b-104">WaveActiveMin fonction)</span><span class="sxs-lookup"><span data-stu-id="62a7b-104">WaveActiveMin function</span></span>

<span data-ttu-id="62a7b-105">Retourne la valeur minimale de l’expression sur tous les couloirs actifs de l’onde actuelle pour la répliquer à tous les couloirs actifs.</span><span class="sxs-lookup"><span data-stu-id="62a7b-105">Returns the minimum value of the expression across all active lanes in the current wave replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a7b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62a7b-106">Syntax</span></span>

``` syntax
<type> WaveActiveMin(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="62a7b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62a7b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a7b-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="62a7b-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="62a7b-109">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="62a7b-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a7b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62a7b-110">Return value</span></span>

<span data-ttu-id="62a7b-111">Valeur minimale.</span><span class="sxs-lookup"><span data-stu-id="62a7b-111">The minimum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62a7b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="62a7b-112">Remarks</span></span>

<span data-ttu-id="62a7b-113">L’ordre des opérations n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="62a7b-113">The order of operations is undefined.</span></span>

<span data-ttu-id="62a7b-114">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="62a7b-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="62a7b-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="62a7b-115">Examples</span></span>

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a><span data-ttu-id="62a7b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62a7b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a7b-117">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="62a7b-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="62a7b-118">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="62a7b-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




