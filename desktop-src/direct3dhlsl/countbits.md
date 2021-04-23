---
title: countbits (fonction)
description: Compte le nombre de bits (par composant) défini dans l’entier d’entrée.
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
ms.openlocfilehash: 357aceca6e2aea261a9e94212b58ff6308c99560
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925622"
---
# <a name="countbits-function"></a><span data-ttu-id="cbf14-104">countbits (fonction)</span><span class="sxs-lookup"><span data-stu-id="cbf14-104">countbits function</span></span>

<span data-ttu-id="cbf14-105">Compte le nombre de bits (par composant) défini dans l’entier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cbf14-105">Counts the number of bits (per component) set in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbf14-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbf14-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="cbf14-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbf14-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbf14-108">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbf14-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf14-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="cbf14-109">Type: **uint**</span></span>

<span data-ttu-id="cbf14-110">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="cbf14-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbf14-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cbf14-111">Return value</span></span>

<span data-ttu-id="cbf14-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="cbf14-112">Type: **uint**</span></span>

<span data-ttu-id="cbf14-113">Nombre de bits.</span><span class="sxs-lookup"><span data-stu-id="cbf14-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbf14-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cbf14-114">Remarks</span></span>

<span data-ttu-id="cbf14-115">Les versions surchargées suivantes sont également disponibles :</span><span class="sxs-lookup"><span data-stu-id="cbf14-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="cbf14-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="cbf14-116">Minimum Shader Model</span></span>

<span data-ttu-id="cbf14-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="cbf14-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cbf14-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="cbf14-118">Shader Model</span></span>                                                                | <span data-ttu-id="cbf14-119">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbf14-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="cbf14-120">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="cbf14-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="cbf14-121">Oui</span><span class="sxs-lookup"><span data-stu-id="cbf14-121">yes</span></span>       |



 

<span data-ttu-id="cbf14-122">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="cbf14-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="cbf14-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="cbf14-123">Vertex</span></span> | <span data-ttu-id="cbf14-124">Forme</span><span class="sxs-lookup"><span data-stu-id="cbf14-124">Hull</span></span> | <span data-ttu-id="cbf14-125">Domain</span><span class="sxs-lookup"><span data-stu-id="cbf14-125">Domain</span></span> | <span data-ttu-id="cbf14-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="cbf14-126">Geometry</span></span> | <span data-ttu-id="cbf14-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="cbf14-127">Pixel</span></span> | <span data-ttu-id="cbf14-128">Compute</span><span class="sxs-lookup"><span data-stu-id="cbf14-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cbf14-129">x</span><span class="sxs-lookup"><span data-stu-id="cbf14-129">x</span></span>      | <span data-ttu-id="cbf14-130">x</span><span class="sxs-lookup"><span data-stu-id="cbf14-130">x</span></span>    | <span data-ttu-id="cbf14-131">x</span><span class="sxs-lookup"><span data-stu-id="cbf14-131">x</span></span>      | <span data-ttu-id="cbf14-132">x</span><span class="sxs-lookup"><span data-stu-id="cbf14-132">x</span></span>        | <span data-ttu-id="cbf14-133">x</span><span class="sxs-lookup"><span data-stu-id="cbf14-133">x</span></span>     | <span data-ttu-id="cbf14-134">x</span><span class="sxs-lookup"><span data-stu-id="cbf14-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cbf14-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbf14-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf14-136">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="cbf14-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="cbf14-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="cbf14-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




