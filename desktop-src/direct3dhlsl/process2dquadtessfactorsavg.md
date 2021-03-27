---
title: Process2DQuadTessFactorsAvg fonction)
description: Génère les facteurs de pavage corrigés pour un correctif Quad. | Process2DQuadTessFactorsAvg fonction)
ms.assetid: 7f96f634-0ad5-4037-a08e-b0b99b89cd91
keywords:
- Process2DQuadTessFactorsAvg fonction HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4012d99a1f7714fae68f4679991aedcf810d1b4e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761654"
---
# <a name="process2dquadtessfactorsavg-function"></a><span data-ttu-id="3cdd4-105">Process2DQuadTessFactorsAvg fonction)</span><span class="sxs-lookup"><span data-stu-id="3cdd4-105">Process2DQuadTessFactorsAvg function</span></span>

<span data-ttu-id="3cdd4-106">Génère les facteurs de pavage corrigés pour un correctif Quad.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-106">Generates the corrected tessellation factors for a quad patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cdd4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cdd4-107">Syntax</span></span>

``` syntax
void Process2DQuadTessFactorsAvg(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="3cdd4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cdd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cdd4-109">*RawEdgeFactors* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3cdd4-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdd4-110">Type : **float4**</span><span class="sxs-lookup"><span data-stu-id="3cdd4-110">Type: **float4**</span></span>

<span data-ttu-id="3cdd4-111">Facteurs de pavage Edge, passés à l’étape du paveur.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="3cdd4-112">*InsideScale* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3cdd4-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdd4-113">Type : **float2**</span><span class="sxs-lookup"><span data-stu-id="3cdd4-113">Type: **float2**</span></span>

<span data-ttu-id="3cdd4-114">Facteur d’échelle appliqué aux facteurs de pavage UV calculés par l’étape de pavage.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="3cdd4-115">La plage autorisée pour InsideScale est 0,0 à 1,0.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="3cdd4-116">*RoundedEdgeTessFactors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3cdd4-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdd4-117">Type : **float4**</span><span class="sxs-lookup"><span data-stu-id="3cdd4-117">Type: **float4**</span></span>

<span data-ttu-id="3cdd4-118">Facteurs de pavage de bords arrondis calculés par l’étape du paveur.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="3cdd4-119">*RoundedInsideTessFactors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3cdd4-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdd4-120">Type : **float2**</span><span class="sxs-lookup"><span data-stu-id="3cdd4-120">Type: **float2**</span></span>

<span data-ttu-id="3cdd4-121">Facteurs de pavage arrondis calculés par l’étape du paveur pour les bords intérieurs.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="3cdd4-122">*UnroundedInsideTessFactors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3cdd4-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdd4-123">Type : **float2**</span><span class="sxs-lookup"><span data-stu-id="3cdd4-123">Type: **float2**</span></span>

<span data-ttu-id="3cdd4-124">Facteurs de pavage calculés par l’étape du paveur pour les bords intérieurs.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cdd4-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3cdd4-125">Return value</span></span>

<span data-ttu-id="3cdd4-126">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cdd4-127">Notes</span><span class="sxs-lookup"><span data-stu-id="3cdd4-127">Remarks</span></span>

<span data-ttu-id="3cdd4-128">Génère les facteurs de pavage corrigés pour un correctif Quad, en calculant les facteurs de pavage intérieurs comme la moyenne des facteurs de pavage Edge.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-128">Generates the corrected tessellation factors for a quad patch, computing the inside tessellation factors as the average of the edge tessellation factors.</span></span> <span data-ttu-id="3cdd4-129">Les facteurs de pavage à l’intérieur de votre et de V sont calculés indépendamment à l’aide de la moyenne des côtés opposés du domaine, puis sont mis à l’échelle par InsideScale.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-129">The U and V inside tessellation factors are computed independently using the average of opposing sides of the domain, then are scaled by InsideScale.</span></span> <span data-ttu-id="3cdd4-130">Le résultat est ensuite arrondi selon le mode de partitionnement, mais les résultats non arrondis sont disponibles à l’aide du paramètre UnroundedInsideTessFactors.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-130">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactors parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="3cdd4-131">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3cdd4-131">Minimum Shader Model</span></span>

<span data-ttu-id="3cdd4-132">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3cdd4-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3cdd4-133">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3cdd4-133">Shader Model</span></span>                                                                | <span data-ttu-id="3cdd4-134">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3cdd4-134">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3cdd4-135">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="3cdd4-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="3cdd4-136">Oui</span><span class="sxs-lookup"><span data-stu-id="3cdd4-136">yes</span></span>       |



 

<span data-ttu-id="3cdd4-137">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="3cdd4-137">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3cdd4-138">Sommet</span><span class="sxs-lookup"><span data-stu-id="3cdd4-138">Vertex</span></span> | <span data-ttu-id="3cdd4-139">Forme</span><span class="sxs-lookup"><span data-stu-id="3cdd4-139">Hull</span></span> | <span data-ttu-id="3cdd4-140">Domain</span><span class="sxs-lookup"><span data-stu-id="3cdd4-140">Domain</span></span> | <span data-ttu-id="3cdd4-141">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3cdd4-141">Geometry</span></span> | <span data-ttu-id="3cdd4-142">Pixel</span><span class="sxs-lookup"><span data-stu-id="3cdd4-142">Pixel</span></span> | <span data-ttu-id="3cdd4-143">Compute</span><span class="sxs-lookup"><span data-stu-id="3cdd4-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="3cdd4-144">x</span><span class="sxs-lookup"><span data-stu-id="3cdd4-144">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="3cdd4-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cdd4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cdd4-146">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="3cdd4-146">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="3cdd4-147">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3cdd4-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




