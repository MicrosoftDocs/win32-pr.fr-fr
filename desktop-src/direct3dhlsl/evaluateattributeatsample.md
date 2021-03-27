---
title: EvaluateAttributeAtSample fonction)
description: Évalue à l’emplacement de l’exemple indexé.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- EvaluateAttributeAtSample fonction HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678294"
---
# <a name="evaluateattributeatsample-function"></a><span data-ttu-id="3263a-104">EvaluateAttributeAtSample fonction)</span><span class="sxs-lookup"><span data-stu-id="3263a-104">EvaluateAttributeAtSample function</span></span>

<span data-ttu-id="3263a-105">Évalue à l’emplacement de l’exemple indexé.</span><span class="sxs-lookup"><span data-stu-id="3263a-105">Evaluates at the indexed sample location.</span></span>

## <a name="syntax"></a><span data-ttu-id="3263a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3263a-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="3263a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3263a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3263a-108">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3263a-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3263a-109">Type : **Attrib Numeric**</span><span class="sxs-lookup"><span data-stu-id="3263a-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="3263a-110">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="3263a-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="3263a-111">*sampleindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3263a-111">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3263a-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="3263a-112">Type: **uint**</span></span>

<span data-ttu-id="3263a-113">Emplacement de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="3263a-113">The sample location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3263a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3263a-114">Remarks</span></span>

<span data-ttu-id="3263a-115">Le mode d’interpolation peut être **linéaire** ou **linéaire, \_ sans \_ perspective** sur la variable.</span><span class="sxs-lookup"><span data-stu-id="3263a-115">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="3263a-116">L’utilisation de l’argument de centre de **gravité** ou d' **échantillon** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3263a-116">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="3263a-117">Les attributs avec interpolation constante sont également autorisés. dans ce cas, l’exemple d’index est ignoré.</span><span class="sxs-lookup"><span data-stu-id="3263a-117">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="3263a-118">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3263a-118">Minimum Shader Model</span></span>

<span data-ttu-id="3263a-119">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3263a-119">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3263a-120">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3263a-120">Shader Model</span></span>                                                                | <span data-ttu-id="3263a-121">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3263a-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3263a-122">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="3263a-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="3263a-123">Oui</span><span class="sxs-lookup"><span data-stu-id="3263a-123">yes</span></span>       |



 

<span data-ttu-id="3263a-124">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="3263a-124">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3263a-125">Sommet</span><span class="sxs-lookup"><span data-stu-id="3263a-125">Vertex</span></span> | <span data-ttu-id="3263a-126">Forme</span><span class="sxs-lookup"><span data-stu-id="3263a-126">Hull</span></span> | <span data-ttu-id="3263a-127">Domain</span><span class="sxs-lookup"><span data-stu-id="3263a-127">Domain</span></span> | <span data-ttu-id="3263a-128">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3263a-128">Geometry</span></span> | <span data-ttu-id="3263a-129">Pixel</span><span class="sxs-lookup"><span data-stu-id="3263a-129">Pixel</span></span> | <span data-ttu-id="3263a-130">Compute</span><span class="sxs-lookup"><span data-stu-id="3263a-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3263a-131">x</span><span class="sxs-lookup"><span data-stu-id="3263a-131">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="3263a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3263a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3263a-133">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="3263a-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="3263a-134">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3263a-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




