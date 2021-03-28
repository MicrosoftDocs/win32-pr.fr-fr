---
title: WaveActiveBitAnd fonction)
description: Retourne l’opération de bits AND de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique vers tous les couloirs actifs.
ms.assetid: 602884CD-E656-4DEB-A30A-8A7D127A2217
keywords:
- WaveActiveBitAnd fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b6a3b0b097ea8737e07a91fcfc6553f22b828f1
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032097"
---
# <a name="waveactivebitand-function"></a><span data-ttu-id="4e075-104">WaveActiveBitAnd fonction)</span><span class="sxs-lookup"><span data-stu-id="4e075-104">WaveActiveBitAnd function</span></span>

<span data-ttu-id="4e075-105">Retourne l’opération de bits AND de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique vers tous les couloirs actifs.</span><span class="sxs-lookup"><span data-stu-id="4e075-105">Returns the bitwise AND of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e075-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e075-106">Syntax</span></span>


``` syntax
<int_type> WaveActiveBitAnd(
   <int_type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="4e075-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e075-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e075-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="4e075-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="4e075-109">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="4e075-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e075-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e075-110">Return value</span></span>

<span data-ttu-id="4e075-111">Valeur and au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="4e075-111">The bitwise AND value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e075-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4e075-112">Remarks</span></span>

<span data-ttu-id="4e075-113">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="4e075-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="4e075-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e075-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e075-115">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="4e075-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="4e075-116">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="4e075-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




