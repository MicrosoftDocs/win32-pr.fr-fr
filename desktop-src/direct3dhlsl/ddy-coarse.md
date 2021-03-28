---
title: ddy_coarse fonction)
description: Calcule une dérivée partielle de faible précision par rapport à la coordonnée y de l’espace d’écran.
ms.assetid: f6103cd3-f7ee-41c2-b3cf-9e72ca84b25e
keywords:
- ddy_coarse fonction HLSL
topic_type:
- apiref
api_name:
- ddy_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6fef330e919a31e39306742bb03280454d47626
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030370"
---
# <a name="ddy_coarse-function"></a><span data-ttu-id="de117-104">\_fonction grossiste ddy</span><span class="sxs-lookup"><span data-stu-id="de117-104">ddy\_coarse function</span></span>

<span data-ttu-id="de117-105">Calcule une dérivée partielle de faible précision par rapport à la coordonnée y de l’espace d’écran.</span><span class="sxs-lookup"><span data-stu-id="de117-105">Computes a low precision partial derivative with respect to the screen-space y-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="de117-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de117-106">Syntax</span></span>

``` syntax
float ddy_coarse(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="de117-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de117-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de117-108">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de117-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de117-109">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="de117-109">Type: **float**</span></span>

<span data-ttu-id="de117-110">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="de117-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de117-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de117-111">Return value</span></span>

<span data-ttu-id="de117-112">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="de117-112">Type: **float**</span></span>

<span data-ttu-id="de117-113">Dérivée partiel de faible précision de la *valeur*.</span><span class="sxs-lookup"><span data-stu-id="de117-113">The low precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="de117-114">Notes</span><span class="sxs-lookup"><span data-stu-id="de117-114">Remarks</span></span>

<span data-ttu-id="de117-115">Les versions surchargées suivantes sont également disponibles :</span><span class="sxs-lookup"><span data-stu-id="de117-115">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_coarse(float2 value);
float3 ddy_coarse(float3 value);
float4 ddy_coarse(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="de117-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="de117-116">Minimum Shader Model</span></span>

<span data-ttu-id="de117-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="de117-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="de117-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="de117-118">Shader Model</span></span>                                                                | <span data-ttu-id="de117-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="de117-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="de117-120">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="de117-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="de117-121">Oui</span><span class="sxs-lookup"><span data-stu-id="de117-121">yes</span></span>       |



 

<span data-ttu-id="de117-122">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="de117-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="de117-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="de117-123">Vertex</span></span> | <span data-ttu-id="de117-124">Forme</span><span class="sxs-lookup"><span data-stu-id="de117-124">Hull</span></span> | <span data-ttu-id="de117-125">Domain</span><span class="sxs-lookup"><span data-stu-id="de117-125">Domain</span></span> | <span data-ttu-id="de117-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="de117-126">Geometry</span></span> | <span data-ttu-id="de117-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="de117-127">Pixel</span></span> | <span data-ttu-id="de117-128">Compute</span><span class="sxs-lookup"><span data-stu-id="de117-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="de117-129">x</span><span class="sxs-lookup"><span data-stu-id="de117-129">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="de117-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de117-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de117-131">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="de117-131">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="de117-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="de117-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




