---
title: ddy_fine fonction)
description: Calcule un dérivée partiel de haute précision par rapport à la coordonnée x de l’espace d’écran. | ddy_fine fonction)
ms.assetid: 29fcdbc9-470b-4b5b-b18c-f75dd2c87920
keywords:
- ddy_fine fonction HLSL
topic_type:
- apiref
api_name:
- ddy_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a4cb297180a4988cb049ccebfa4f82571c4655c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992121"
---
# <a name="ddy_fine-function"></a><span data-ttu-id="40e67-105">\_fonction de fin ddy</span><span class="sxs-lookup"><span data-stu-id="40e67-105">ddy\_fine function</span></span>

<span data-ttu-id="40e67-106">Calcule un dérivée partiel de haute précision par rapport à la coordonnée x de l’espace d’écran.</span><span class="sxs-lookup"><span data-stu-id="40e67-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="40e67-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40e67-107">Syntax</span></span>

``` syntax
float ddy_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="40e67-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40e67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40e67-109">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40e67-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40e67-110">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="40e67-110">Type: **float**</span></span>

<span data-ttu-id="40e67-111">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="40e67-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40e67-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40e67-112">Return value</span></span>

<span data-ttu-id="40e67-113">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="40e67-113">Type: **float**</span></span>

<span data-ttu-id="40e67-114">Dérivée partiel de haute précision de la *valeur*.</span><span class="sxs-lookup"><span data-stu-id="40e67-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="40e67-115">Notes</span><span class="sxs-lookup"><span data-stu-id="40e67-115">Remarks</span></span>

<span data-ttu-id="40e67-116">Les versions surchargées suivantes sont également disponibles :</span><span class="sxs-lookup"><span data-stu-id="40e67-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_fine(float2 value);
float3 ddy_fine(float3 value);
float4 ddy_fine(float4 value);  
```

### <a name="minimum-shader-model"></a><span data-ttu-id="40e67-117">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="40e67-117">Minimum Shader Model</span></span>

<span data-ttu-id="40e67-118">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="40e67-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="40e67-119">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="40e67-119">Shader Model</span></span>                                                                | <span data-ttu-id="40e67-120">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="40e67-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="40e67-121">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="40e67-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="40e67-122">Oui</span><span class="sxs-lookup"><span data-stu-id="40e67-122">yes</span></span>       |



 

<span data-ttu-id="40e67-123">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="40e67-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="40e67-124">Sommet</span><span class="sxs-lookup"><span data-stu-id="40e67-124">Vertex</span></span> | <span data-ttu-id="40e67-125">Forme</span><span class="sxs-lookup"><span data-stu-id="40e67-125">Hull</span></span> | <span data-ttu-id="40e67-126">Domain</span><span class="sxs-lookup"><span data-stu-id="40e67-126">Domain</span></span> | <span data-ttu-id="40e67-127">Géométrie</span><span class="sxs-lookup"><span data-stu-id="40e67-127">Geometry</span></span> | <span data-ttu-id="40e67-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="40e67-128">Pixel</span></span> | <span data-ttu-id="40e67-129">Compute</span><span class="sxs-lookup"><span data-stu-id="40e67-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="40e67-130">x</span><span class="sxs-lookup"><span data-stu-id="40e67-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="40e67-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40e67-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40e67-132">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="40e67-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="40e67-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="40e67-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




