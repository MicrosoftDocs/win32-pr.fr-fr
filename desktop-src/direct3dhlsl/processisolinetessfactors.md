---
title: ProcessIsolineTessFactors fonction)
description: Génère les facteurs de pavage arrondis pour une isoligne.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- ProcessIsolineTessFactors fonction HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678746"
---
# <a name="processisolinetessfactors-function"></a><span data-ttu-id="335d9-104">ProcessIsolineTessFactors fonction)</span><span class="sxs-lookup"><span data-stu-id="335d9-104">ProcessIsolineTessFactors function</span></span>

<span data-ttu-id="335d9-105">Génère les facteurs de pavage arrondis pour une isoligne.</span><span class="sxs-lookup"><span data-stu-id="335d9-105">Generates the rounded tessellation factors for an isoline.</span></span>

## <a name="syntax"></a><span data-ttu-id="335d9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="335d9-106">Syntax</span></span>

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a><span data-ttu-id="335d9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="335d9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="335d9-108">*RawDetailFactor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="335d9-108">*RawDetailFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="335d9-109">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="335d9-109">Type: **float**</span></span>

<span data-ttu-id="335d9-110">Facteur de détail souhaité.</span><span class="sxs-lookup"><span data-stu-id="335d9-110">The desired detail factor.</span></span>

</dd> <dt>

<span data-ttu-id="335d9-111">*RawDensityFactor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="335d9-111">*RawDensityFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="335d9-112">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="335d9-112">Type: **float**</span></span>

<span data-ttu-id="335d9-113">Facteur de densité souhaité.</span><span class="sxs-lookup"><span data-stu-id="335d9-113">The desired density factor.</span></span>

</dd> <dt>

<span data-ttu-id="335d9-114">*RoundedDetailFactor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="335d9-114">*RoundedDetailFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="335d9-115">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="335d9-115">Type: **float**</span></span>

<span data-ttu-id="335d9-116">Facteur de détail arrondi à une plage qui peut être utilisée par le du paveur.</span><span class="sxs-lookup"><span data-stu-id="335d9-116">The rounded detail factor clamped to a range that can be used by the tessellator.</span></span>

</dd> <dt>

<span data-ttu-id="335d9-117">*RoundedDensityFactor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="335d9-117">*RoundedDensityFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="335d9-118">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="335d9-118">Type: **float**</span></span>

<span data-ttu-id="335d9-119">Le facteur de densité arrondie avec un rangethat peut être utilisé par le du paveur.</span><span class="sxs-lookup"><span data-stu-id="335d9-119">The rounded density factor clamped to a rangethat can be used by the tessellator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="335d9-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="335d9-120">Return value</span></span>

<span data-ttu-id="335d9-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="335d9-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="335d9-122">Notes</span><span class="sxs-lookup"><span data-stu-id="335d9-122">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="335d9-123">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="335d9-123">Minimum Shader Model</span></span>

<span data-ttu-id="335d9-124">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="335d9-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="335d9-125">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="335d9-125">Shader Model</span></span>                                                                | <span data-ttu-id="335d9-126">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="335d9-126">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="335d9-127">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="335d9-127">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="335d9-128">Oui</span><span class="sxs-lookup"><span data-stu-id="335d9-128">yes</span></span>       |



 

<span data-ttu-id="335d9-129">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="335d9-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="335d9-130">Sommet</span><span class="sxs-lookup"><span data-stu-id="335d9-130">Vertex</span></span> | <span data-ttu-id="335d9-131">Forme</span><span class="sxs-lookup"><span data-stu-id="335d9-131">Hull</span></span> | <span data-ttu-id="335d9-132">Domain</span><span class="sxs-lookup"><span data-stu-id="335d9-132">Domain</span></span> | <span data-ttu-id="335d9-133">Géométrie</span><span class="sxs-lookup"><span data-stu-id="335d9-133">Geometry</span></span> | <span data-ttu-id="335d9-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="335d9-134">Pixel</span></span> | <span data-ttu-id="335d9-135">Compute</span><span class="sxs-lookup"><span data-stu-id="335d9-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="335d9-136">x</span><span class="sxs-lookup"><span data-stu-id="335d9-136">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="335d9-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="335d9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="335d9-138">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="335d9-138">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="335d9-139">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="335d9-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




