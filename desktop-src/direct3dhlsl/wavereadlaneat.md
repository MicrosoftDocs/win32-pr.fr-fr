---
title: WaveReadLaneAt fonction)
description: Retourne la valeur de l’expression pour l’index Lane donné dans l’onde spécifiée.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- WaveReadLaneAt fonction HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 573730053a93a110381637ef8e62dc08a4aa1535
ms.sourcegitcommit: 1897c2a39b4ac4ca4b1e4aec394cef2ce2619c03
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/06/2021
ms.locfileid: "113316481"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="15bd1-104">WaveReadLaneAt fonction)</span><span class="sxs-lookup"><span data-stu-id="15bd1-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="15bd1-105">Retourne la valeur de l’expression pour l’index Lane donné dans l’onde spécifiée.</span><span class="sxs-lookup"><span data-stu-id="15bd1-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="15bd1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15bd1-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="15bd1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15bd1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15bd1-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="15bd1-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="15bd1-109">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="15bd1-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="15bd1-110">*laneIndex*</span><span class="sxs-lookup"><span data-stu-id="15bd1-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="15bd1-111">Index de la voie pour laquelle le résultat *expr* sera retourné.</span><span class="sxs-lookup"><span data-stu-id="15bd1-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15bd1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="15bd1-112">Return value</span></span>

<span data-ttu-id="15bd1-113">La valeur résultante est le résultat de *expr*.</span><span class="sxs-lookup"><span data-stu-id="15bd1-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="15bd1-114">Elle est uniforme si *laneIndex* est uniforme.</span><span class="sxs-lookup"><span data-stu-id="15bd1-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="15bd1-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="15bd1-115">Remarks</span></span>

<span data-ttu-id="15bd1-116">Cette fonction est effectivement une diffusion de la valeur de la *laneIndex*« ième allée ».</span><span class="sxs-lookup"><span data-stu-id="15bd1-116">This function is effectively a broadcast of the value in the *laneIndex*'th lane.</span></span>

<span data-ttu-id="15bd1-117">Cette fonction est prise en charge à partir du Shader Model 6,0 dans toutes les étapes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="15bd1-117">This function is supported from shader model 6.0 in all shader stages.</span></span>

## <a name="see-also"></a><span data-ttu-id="15bd1-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15bd1-118">See also</span></span>

* [<span data-ttu-id="15bd1-119">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="15bd1-119">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [<span data-ttu-id="15bd1-120">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="15bd1-120">Shader Model 6</span></span>](shader-model-6-0.md)
