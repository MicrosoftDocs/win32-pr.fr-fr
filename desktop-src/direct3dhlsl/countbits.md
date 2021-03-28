---
title: countbits (fonction)
description: Compte le nombre de bits (par composant) dans l’entier d’entrée.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- countbits fonction HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d3cd63502c6217e6fb0b0ff17685b2d2b5bf25
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030372"
---
# <a name="countbits-function"></a><span data-ttu-id="6d0d1-104">countbits (fonction)</span><span class="sxs-lookup"><span data-stu-id="6d0d1-104">countbits function</span></span>

<span data-ttu-id="6d0d1-105">Compte le nombre de bits (par composant) dans l’entier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6d0d1-105">Counts the number of bits (per component) in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d0d1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d0d1-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="6d0d1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d0d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d0d1-108">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d0d1-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d0d1-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="6d0d1-109">Type: **uint**</span></span>

<span data-ttu-id="6d0d1-110">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="6d0d1-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d0d1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d0d1-111">Return value</span></span>

<span data-ttu-id="6d0d1-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="6d0d1-112">Type: **uint**</span></span>

<span data-ttu-id="6d0d1-113">Nombre de bits.</span><span class="sxs-lookup"><span data-stu-id="6d0d1-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d0d1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6d0d1-114">Remarks</span></span>

<span data-ttu-id="6d0d1-115">Les versions surchargées suivantes sont également disponibles :</span><span class="sxs-lookup"><span data-stu-id="6d0d1-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="6d0d1-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="6d0d1-116">Minimum Shader Model</span></span>

<span data-ttu-id="6d0d1-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="6d0d1-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6d0d1-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6d0d1-118">Shader Model</span></span>                                                                | <span data-ttu-id="6d0d1-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="6d0d1-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="6d0d1-120">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="6d0d1-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="6d0d1-121">Oui</span><span class="sxs-lookup"><span data-stu-id="6d0d1-121">yes</span></span>       |



 

<span data-ttu-id="6d0d1-122">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="6d0d1-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="6d0d1-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="6d0d1-123">Vertex</span></span> | <span data-ttu-id="6d0d1-124">Forme</span><span class="sxs-lookup"><span data-stu-id="6d0d1-124">Hull</span></span> | <span data-ttu-id="6d0d1-125">Domain</span><span class="sxs-lookup"><span data-stu-id="6d0d1-125">Domain</span></span> | <span data-ttu-id="6d0d1-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="6d0d1-126">Geometry</span></span> | <span data-ttu-id="6d0d1-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="6d0d1-127">Pixel</span></span> | <span data-ttu-id="6d0d1-128">Compute</span><span class="sxs-lookup"><span data-stu-id="6d0d1-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6d0d1-129">x</span><span class="sxs-lookup"><span data-stu-id="6d0d1-129">x</span></span>      | <span data-ttu-id="6d0d1-130">x</span><span class="sxs-lookup"><span data-stu-id="6d0d1-130">x</span></span>    | <span data-ttu-id="6d0d1-131">x</span><span class="sxs-lookup"><span data-stu-id="6d0d1-131">x</span></span>      | <span data-ttu-id="6d0d1-132">x</span><span class="sxs-lookup"><span data-stu-id="6d0d1-132">x</span></span>        | <span data-ttu-id="6d0d1-133">x</span><span class="sxs-lookup"><span data-stu-id="6d0d1-133">x</span></span>     | <span data-ttu-id="6d0d1-134">x</span><span class="sxs-lookup"><span data-stu-id="6d0d1-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6d0d1-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d0d1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d0d1-136">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="6d0d1-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="6d0d1-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6d0d1-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




