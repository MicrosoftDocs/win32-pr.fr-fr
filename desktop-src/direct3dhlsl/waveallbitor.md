---
title: WaveActiveBitOr fonction)
description: Retourne l’opération or au niveau du bit de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique vers tous les couloirs actifs.
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- WaveActiveBitOr fonction HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6870ac8406a581e358b00ef728562dc59118a933
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032091"
---
# <a name="waveactivebitor-function"></a><span data-ttu-id="aa6fc-104">WaveActiveBitOr fonction)</span><span class="sxs-lookup"><span data-stu-id="aa6fc-104">WaveActiveBitOr function</span></span>

<span data-ttu-id="aa6fc-105">Retourne l’opération or au niveau du bit de toutes les valeurs de l’expression sur tous les couloirs actifs de l’onde actuelle et la réplique vers tous les couloirs actifs.</span><span class="sxs-lookup"><span data-stu-id="aa6fc-105">Returns the bitwise OR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6fc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa6fc-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitOr(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="aa6fc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa6fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa6fc-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="aa6fc-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="aa6fc-109">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="aa6fc-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa6fc-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aa6fc-110">Return value</span></span>

<span data-ttu-id="aa6fc-111">Valeur or au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="aa6fc-111">The bitwise OR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa6fc-112">Notes</span><span class="sxs-lookup"><span data-stu-id="aa6fc-112">Remarks</span></span>

<span data-ttu-id="aa6fc-113">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="aa6fc-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="aa6fc-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa6fc-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa6fc-115">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="aa6fc-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="aa6fc-116">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="aa6fc-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




