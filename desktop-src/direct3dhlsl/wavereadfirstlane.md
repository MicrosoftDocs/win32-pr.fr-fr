---
title: WaveReadLaneFirst fonction)
description: Retourne la valeur de l’expression pour la voie active de l’onde actuelle avec l’index le plus petit.
ms.assetid: 89CA4FD5-4573-42ED-88D3-01C79C69FF6F
keywords:
- WaveReadLaneFirst fonction HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneFirst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 04d10e5439b8cd653f7c0a37d3a951167561f964
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104971815"
---
# <a name="wavereadlanefirst-function"></a><span data-ttu-id="2608e-104">WaveReadLaneFirst fonction)</span><span class="sxs-lookup"><span data-stu-id="2608e-104">WaveReadLaneFirst function</span></span>

<span data-ttu-id="2608e-105">Retourne la valeur de l’expression pour la voie active de l’onde actuelle avec l’index le plus petit.</span><span class="sxs-lookup"><span data-stu-id="2608e-105">Returns the value of the expression for the active lane of the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2608e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2608e-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneFirst(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="2608e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2608e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2608e-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="2608e-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="2608e-109">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="2608e-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2608e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2608e-110">Return value</span></span>

<span data-ttu-id="2608e-111">La valeur obtenue est uniforme sur l’onde.</span><span class="sxs-lookup"><span data-stu-id="2608e-111">The resulting value is uniform across the wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="2608e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2608e-112">Remarks</span></span>

<span data-ttu-id="2608e-113">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="2608e-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="2608e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2608e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2608e-115">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="2608e-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="2608e-116">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="2608e-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




