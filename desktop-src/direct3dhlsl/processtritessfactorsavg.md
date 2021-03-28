---
title: ProcessTriTessFactorsAvg fonction)
description: Génère les facteurs de pavage corrigés pour un correctif triple. | ProcessTriTessFactorsAvg fonction)
ms.assetid: 005a63b6-f35d-42d6-bb29-f4ebb374080e
keywords:
- ProcessTriTessFactorsAvg fonction HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90cfa86a09e0e76c90f0013cfa6121917ca25378
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991937"
---
# <a name="processtritessfactorsavg-function"></a><span data-ttu-id="9bfd9-105">ProcessTriTessFactorsAvg fonction)</span><span class="sxs-lookup"><span data-stu-id="9bfd9-105">ProcessTriTessFactorsAvg function</span></span>

<span data-ttu-id="9bfd9-106">Génère les facteurs de pavage corrigés pour un correctif triple.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bfd9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9bfd9-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsAvg(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a><span data-ttu-id="9bfd9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9bfd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bfd9-109">*RawEdgeFactors* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bfd9-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bfd9-110">Type : **float3**</span><span class="sxs-lookup"><span data-stu-id="9bfd9-110">Type: **float3**</span></span>

<span data-ttu-id="9bfd9-111">Facteurs de pavage Edge, passés à l’étape du paveur.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="9bfd9-112">*InsideScale* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bfd9-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bfd9-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="9bfd9-113">Type: **float**</span></span>

<span data-ttu-id="9bfd9-114">Facteur d’échelle appliqué aux facteurs de pavage UV calculés par l’étape de pavage.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="9bfd9-115">La plage autorisée pour InsideScale est 0,0 à 1,0.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="9bfd9-116">*RoundedEdgeTessFactors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9bfd9-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bfd9-117">Type : **float3**</span><span class="sxs-lookup"><span data-stu-id="9bfd9-117">Type: **float3**</span></span>

<span data-ttu-id="9bfd9-118">Facteurs de pavage de bords arrondis calculés par l’étape du paveur.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="9bfd9-119">*RoundedInsideTessFactor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9bfd9-119">*RoundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bfd9-120">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="9bfd9-120">Type: **float**</span></span>

<span data-ttu-id="9bfd9-121">Facteurs de pavage calculés par l’étape du paveur et arrondis.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-121">The tessellation factors calculated by the tessellator stage, and rounded.</span></span>

</dd> <dt>

<span data-ttu-id="9bfd9-122">*UnroundedInsideTessFactor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9bfd9-122">*UnroundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bfd9-123">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="9bfd9-123">Type: **float**</span></span>

<span data-ttu-id="9bfd9-124">Facteurs de pavage UV originaux et inarrondis calculés par l’étape de pavage.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-124">The original, unrounded, UV tessellation factors computed by the tessellation stage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bfd9-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9bfd9-125">Return value</span></span>

<span data-ttu-id="9bfd9-126">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bfd9-127">Notes</span><span class="sxs-lookup"><span data-stu-id="9bfd9-127">Remarks</span></span>

<span data-ttu-id="9bfd9-128">Génère les facteurs de pavage corrigés pour un correctif triple, en calculant le facteur de pavage intérieur comme la moyenne des facteurs de pavage Edge, qui est ensuite mis à l’échelle par InsideScale.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the average of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="9bfd9-129">Le résultat est ensuite arrondi selon le mode de partitionnement, mais les résultats non arrondis sont disponibles à l’aide du paramètre UnroundedInsideTessFactor.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="9bfd9-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="9bfd9-130">Minimum Shader Model</span></span>

<span data-ttu-id="9bfd9-131">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9bfd9-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="9bfd9-132">Shader Model</span></span>                                                                | <span data-ttu-id="9bfd9-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="9bfd9-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9bfd9-134">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="9bfd9-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9bfd9-135">Oui</span><span class="sxs-lookup"><span data-stu-id="9bfd9-135">yes</span></span>       |



 

<span data-ttu-id="9bfd9-136">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="9bfd9-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="9bfd9-137">Sommet</span><span class="sxs-lookup"><span data-stu-id="9bfd9-137">Vertex</span></span> | <span data-ttu-id="9bfd9-138">Forme</span><span class="sxs-lookup"><span data-stu-id="9bfd9-138">Hull</span></span> | <span data-ttu-id="9bfd9-139">Domain</span><span class="sxs-lookup"><span data-stu-id="9bfd9-139">Domain</span></span> | <span data-ttu-id="9bfd9-140">Géométrie</span><span class="sxs-lookup"><span data-stu-id="9bfd9-140">Geometry</span></span> | <span data-ttu-id="9bfd9-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="9bfd9-141">Pixel</span></span> | <span data-ttu-id="9bfd9-142">Compute</span><span class="sxs-lookup"><span data-stu-id="9bfd9-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="9bfd9-143">x</span><span class="sxs-lookup"><span data-stu-id="9bfd9-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="9bfd9-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bfd9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bfd9-145">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="9bfd9-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="9bfd9-146">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="9bfd9-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




