---
title: ProcessTriTessFactorsMin fonction)
description: Génère les facteurs de pavage corrigés pour un correctif triple. | ProcessTriTessFactorsMin fonction)
ms.assetid: fa1e19c2-fadf-42d4-9574-834eaf871393
keywords:
- ProcessTriTessFactorsMin fonction HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f82c7935d47813d833ccc21a7ec0134adee1cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530651"
---
# <a name="processtritessfactorsmin-function"></a><span data-ttu-id="34bcd-105">ProcessTriTessFactorsMin fonction)</span><span class="sxs-lookup"><span data-stu-id="34bcd-105">ProcessTriTessFactorsMin function</span></span>

<span data-ttu-id="34bcd-106">Génère les facteurs de pavage corrigés pour un correctif triple.</span><span class="sxs-lookup"><span data-stu-id="34bcd-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="34bcd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34bcd-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsMin(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactors,
  out float UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="34bcd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34bcd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34bcd-109">*RawEdgeFactors* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34bcd-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34bcd-110">Type : **float3**</span><span class="sxs-lookup"><span data-stu-id="34bcd-110">Type: **float3**</span></span>

<span data-ttu-id="34bcd-111">Facteurs de pavage Edge, passés à l’étape du paveur.</span><span class="sxs-lookup"><span data-stu-id="34bcd-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="34bcd-112">*InsideScale* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34bcd-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34bcd-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="34bcd-113">Type: **float**</span></span>

<span data-ttu-id="34bcd-114">Facteur d’échelle appliqué aux facteurs de pavage UV calculés par l’étape de pavage.</span><span class="sxs-lookup"><span data-stu-id="34bcd-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="34bcd-115">La plage autorisée pour InsideScale est 0,0 à 1,0.</span><span class="sxs-lookup"><span data-stu-id="34bcd-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="34bcd-116">*RoundedEdgeTessFactors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="34bcd-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34bcd-117">Type : **float3**</span><span class="sxs-lookup"><span data-stu-id="34bcd-117">Type: **float3**</span></span>

<span data-ttu-id="34bcd-118">Facteurs de pavage de bords arrondis calculés par l’étape du paveur.</span><span class="sxs-lookup"><span data-stu-id="34bcd-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="34bcd-119">*RoundedInsideTessFactors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="34bcd-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34bcd-120">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="34bcd-120">Type: **float**</span></span>

<span data-ttu-id="34bcd-121">Facteurs de pavage arrondis calculés par l’étape du paveur pour les bords intérieurs.</span><span class="sxs-lookup"><span data-stu-id="34bcd-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="34bcd-122">*UnroundedInsideTessFactors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="34bcd-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34bcd-123">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="34bcd-123">Type: **float**</span></span>

<span data-ttu-id="34bcd-124">Facteurs de pavage calculés par l’étape du paveur pour les bords intérieurs.</span><span class="sxs-lookup"><span data-stu-id="34bcd-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34bcd-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="34bcd-125">Return value</span></span>

<span data-ttu-id="34bcd-126">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="34bcd-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="34bcd-127">Notes</span><span class="sxs-lookup"><span data-stu-id="34bcd-127">Remarks</span></span>

<span data-ttu-id="34bcd-128">Génère les facteurs de pavage corrigés pour un correctif triple, en calculant le facteur de pavage intérieur comme au minimum des facteurs de pavage Edge, qui est ensuite mis à l’échelle par InsideScale.</span><span class="sxs-lookup"><span data-stu-id="34bcd-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the minimum of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="34bcd-129">Le résultat est ensuite arrondi selon le mode de partitionnement, mais les résultats non arrondis sont disponibles à l’aide du paramètre UnroundedInsideTessFactor.</span><span class="sxs-lookup"><span data-stu-id="34bcd-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="34bcd-130">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="34bcd-130">Minimum Shader Model</span></span>

<span data-ttu-id="34bcd-131">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="34bcd-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="34bcd-132">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="34bcd-132">Shader Model</span></span>                                                                | <span data-ttu-id="34bcd-133">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="34bcd-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="34bcd-134">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="34bcd-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="34bcd-135">Oui</span><span class="sxs-lookup"><span data-stu-id="34bcd-135">yes</span></span>       |



 

<span data-ttu-id="34bcd-136">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="34bcd-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="34bcd-137">Sommet</span><span class="sxs-lookup"><span data-stu-id="34bcd-137">Vertex</span></span> | <span data-ttu-id="34bcd-138">Forme</span><span class="sxs-lookup"><span data-stu-id="34bcd-138">Hull</span></span> | <span data-ttu-id="34bcd-139">Domain</span><span class="sxs-lookup"><span data-stu-id="34bcd-139">Domain</span></span> | <span data-ttu-id="34bcd-140">Géométrie</span><span class="sxs-lookup"><span data-stu-id="34bcd-140">Geometry</span></span> | <span data-ttu-id="34bcd-141">Pixel</span><span class="sxs-lookup"><span data-stu-id="34bcd-141">Pixel</span></span> | <span data-ttu-id="34bcd-142">Compute</span><span class="sxs-lookup"><span data-stu-id="34bcd-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="34bcd-143">x</span><span class="sxs-lookup"><span data-stu-id="34bcd-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="34bcd-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34bcd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34bcd-145">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="34bcd-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="34bcd-146">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="34bcd-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




