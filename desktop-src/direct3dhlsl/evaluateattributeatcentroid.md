---
title: EvaluateAttributeAtCentroid fonction)
description: Évalue au centre de gravité du pixel.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- EvaluateAttributeAtCentroid fonction HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee95c7f2f202dfd0065e5e9c30003cc46fd29281
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380814"
---
# <a name="evaluateattributeatcentroid-function"></a><span data-ttu-id="41e44-104">EvaluateAttributeAtCentroid fonction)</span><span class="sxs-lookup"><span data-stu-id="41e44-104">EvaluateAttributeAtCentroid function</span></span>

<span data-ttu-id="41e44-105">Évalue au centre de gravité du pixel.</span><span class="sxs-lookup"><span data-stu-id="41e44-105">Evaluates at the pixel centroid.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e44-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41e44-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a><span data-ttu-id="41e44-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41e44-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e44-108">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41e44-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e44-109">Type : **Attrib Numeric**</span><span class="sxs-lookup"><span data-stu-id="41e44-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="41e44-110">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="41e44-110">The input value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41e44-111">Notes</span><span class="sxs-lookup"><span data-stu-id="41e44-111">Remarks</span></span>

<span data-ttu-id="41e44-112">Le mode d’interpolation peut être **linéaire** ou **linéaire, \_ sans \_ perspective** sur la variable.</span><span class="sxs-lookup"><span data-stu-id="41e44-112">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="41e44-113">L’utilisation de l’argument de centre de **gravité** ou d' **échantillon** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="41e44-113">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="41e44-114">Les attributs avec interpolation constante sont également autorisés. dans ce cas, l’exemple d’index est ignoré.</span><span class="sxs-lookup"><span data-stu-id="41e44-114">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="41e44-115">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="41e44-115">Minimum Shader Model</span></span>

<span data-ttu-id="41e44-116">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="41e44-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="41e44-117">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="41e44-117">Shader Model</span></span>                                                                | <span data-ttu-id="41e44-118">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="41e44-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="41e44-119">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="41e44-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="41e44-120">Oui</span><span class="sxs-lookup"><span data-stu-id="41e44-120">yes</span></span>       |



 

<span data-ttu-id="41e44-121">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="41e44-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="41e44-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="41e44-122">Vertex</span></span> | <span data-ttu-id="41e44-123">Forme</span><span class="sxs-lookup"><span data-stu-id="41e44-123">Hull</span></span> | <span data-ttu-id="41e44-124">Domain</span><span class="sxs-lookup"><span data-stu-id="41e44-124">Domain</span></span> | <span data-ttu-id="41e44-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="41e44-125">Geometry</span></span> | <span data-ttu-id="41e44-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="41e44-126">Pixel</span></span> | <span data-ttu-id="41e44-127">Compute</span><span class="sxs-lookup"><span data-stu-id="41e44-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="41e44-128">x</span><span class="sxs-lookup"><span data-stu-id="41e44-128">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="41e44-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41e44-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e44-130">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="41e44-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="41e44-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="41e44-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




