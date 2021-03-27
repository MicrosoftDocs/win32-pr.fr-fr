---
title: WaveActiveSum fonction)
description: Additionne la valeur de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs de l’onde actuelle.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- WaveActiveSum fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b98ecf2521841b9da73e1b917d44f1d91b7876d2
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941470"
---
# <a name="waveactivesum-function"></a><span data-ttu-id="259e0-104">WaveActiveSum fonction)</span><span class="sxs-lookup"><span data-stu-id="259e0-104">WaveActiveSum function</span></span>

<span data-ttu-id="259e0-105">Additionne la valeur de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique sur tous les couloirs de l’onde actuelle.</span><span class="sxs-lookup"><span data-stu-id="259e0-105">Sums up the value of the expression across all active lanes in the current wave and replicates it to all lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="259e0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="259e0-106">Syntax</span></span>

``` syntax
<type> WaveActiveSum(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="259e0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="259e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="259e0-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="259e0-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="259e0-109">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="259e0-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="259e0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="259e0-110">Return value</span></span>

<span data-ttu-id="259e0-111">Valeur de la somme.</span><span class="sxs-lookup"><span data-stu-id="259e0-111">The sum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="259e0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="259e0-112">Remarks</span></span>

<span data-ttu-id="259e0-113">L’ordre des opérations n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="259e0-113">The order of operations is undefined.</span></span>

<span data-ttu-id="259e0-114">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="259e0-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="259e0-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="259e0-115">Examples</span></span>

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a><span data-ttu-id="259e0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="259e0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="259e0-117">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="259e0-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="259e0-118">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="259e0-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




