---
title: WaveActiveBitXor fonction)
description: Retourne l’opérateur de bits XOR de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et les réplique sur tous les couloirs actifs.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- WaveActiveBitXor fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e55ce8a43311f4f4c428e97bff1e107ab5c7038
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032089"
---
# <a name="waveactivebitxor-function"></a><span data-ttu-id="ceb61-104">WaveActiveBitXor fonction)</span><span class="sxs-lookup"><span data-stu-id="ceb61-104">WaveActiveBitXor function</span></span>

<span data-ttu-id="ceb61-105">Retourne l’opérateur de bits XOR de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et les réplique sur tous les couloirs actifs.</span><span class="sxs-lookup"><span data-stu-id="ceb61-105">Returns the bitwise XOR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceb61-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ceb61-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="ceb61-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ceb61-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceb61-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="ceb61-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="ceb61-109">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="ceb61-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceb61-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ceb61-110">Return value</span></span>

<span data-ttu-id="ceb61-111">Valeur XOR au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="ceb61-111">The bitwise XOR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceb61-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ceb61-112">Remarks</span></span>

<span data-ttu-id="ceb61-113">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ceb61-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="ceb61-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ceb61-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb61-115">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="ceb61-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="ceb61-116">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="ceb61-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




