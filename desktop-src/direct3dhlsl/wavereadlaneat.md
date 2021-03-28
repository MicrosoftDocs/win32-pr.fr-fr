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
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2020
ms.locfileid: "104381742"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="dbe15-104">WaveReadLaneAt fonction)</span><span class="sxs-lookup"><span data-stu-id="dbe15-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="dbe15-105">Retourne la valeur de l’expression pour l’index Lane donné dans l’onde spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dbe15-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe15-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbe15-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="dbe15-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbe15-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbe15-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="dbe15-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe15-109">Expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="dbe15-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="dbe15-110">*laneIndex*</span><span class="sxs-lookup"><span data-stu-id="dbe15-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe15-111">Index de la voie pour laquelle le résultat *expr* sera retourné.</span><span class="sxs-lookup"><span data-stu-id="dbe15-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbe15-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbe15-112">Return value</span></span>

<span data-ttu-id="dbe15-113">La valeur résultante est le résultat de *expr*.</span><span class="sxs-lookup"><span data-stu-id="dbe15-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="dbe15-114">Elle est uniforme si *laneIndex* est uniforme.</span><span class="sxs-lookup"><span data-stu-id="dbe15-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbe15-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dbe15-115">Remarks</span></span>

<span data-ttu-id="dbe15-116">Cette fonction est effectivement une diffusion de la valeur dans la voie laneIndex’th.</span><span class="sxs-lookup"><span data-stu-id="dbe15-116">This function is effectively a broadcast of the value in the laneIndex’th lane.</span></span>

<span data-ttu-id="dbe15-117">Cette fonction est prise en charge à partir du Shader Model 6,0, dans les types suivants de nuanceurs :</span><span class="sxs-lookup"><span data-stu-id="dbe15-117">This function is supported from shader model 6.0, in the following types of shaders:</span></span>



| <span data-ttu-id="dbe15-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="dbe15-118">Vertex</span></span> | <span data-ttu-id="dbe15-119">Forme</span><span class="sxs-lookup"><span data-stu-id="dbe15-119">Hull</span></span> | <span data-ttu-id="dbe15-120">Domain</span><span class="sxs-lookup"><span data-stu-id="dbe15-120">Domain</span></span> | <span data-ttu-id="dbe15-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="dbe15-121">Geometry</span></span> | <span data-ttu-id="dbe15-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="dbe15-122">Pixel</span></span> | <span data-ttu-id="dbe15-123">Compute</span><span class="sxs-lookup"><span data-stu-id="dbe15-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="dbe15-124">x</span><span class="sxs-lookup"><span data-stu-id="dbe15-124">x</span></span>     | <span data-ttu-id="dbe15-125">x</span><span class="sxs-lookup"><span data-stu-id="dbe15-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="dbe15-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbe15-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe15-127">Vue d’ensemble du modèle de nuanceur 6</span><span class="sxs-lookup"><span data-stu-id="dbe15-127">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="dbe15-128">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="dbe15-128">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




