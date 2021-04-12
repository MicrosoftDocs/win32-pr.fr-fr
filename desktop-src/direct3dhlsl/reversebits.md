---
title: reversebits (fonction)
description: Inverse l’ordre des bits, par composant.
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- reversebits fonction HLSL
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d98b824883ddc4f06e6c11d30c2759bb0fc2be26
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104462566"
---
# <a name="reversebits-function"></a><span data-ttu-id="8b06c-104">reversebits (fonction)</span><span class="sxs-lookup"><span data-stu-id="8b06c-104">reversebits function</span></span>

<span data-ttu-id="8b06c-105">Inverse l’ordre des bits, par composant.</span><span class="sxs-lookup"><span data-stu-id="8b06c-105">Reverses the order of the bits, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b06c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b06c-106">Syntax</span></span>

``` syntax
uint reversebits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="8b06c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b06c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b06c-108">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b06c-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b06c-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="8b06c-109">Type: **uint**</span></span>

<span data-ttu-id="8b06c-110">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="8b06c-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b06c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b06c-111">Return value</span></span>

<span data-ttu-id="8b06c-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="8b06c-112">Type: **uint**</span></span>

<span data-ttu-id="8b06c-113">Valeur d’entrée, avec l’ordre de bits inversé.</span><span class="sxs-lookup"><span data-stu-id="8b06c-113">The input value, with the bit order reversed.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b06c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8b06c-114">Remarks</span></span>

<span data-ttu-id="8b06c-115">Les versions surchargées suivantes sont également disponibles :</span><span class="sxs-lookup"><span data-stu-id="8b06c-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="8b06c-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="8b06c-116">Minimum Shader Model</span></span>

<span data-ttu-id="8b06c-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="8b06c-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8b06c-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8b06c-118">Shader Model</span></span>                                                                | <span data-ttu-id="8b06c-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="8b06c-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8b06c-120">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="8b06c-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="8b06c-121">Oui</span><span class="sxs-lookup"><span data-stu-id="8b06c-121">yes</span></span>       |



 

<span data-ttu-id="8b06c-122">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="8b06c-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="8b06c-123">Sommet</span><span class="sxs-lookup"><span data-stu-id="8b06c-123">Vertex</span></span> | <span data-ttu-id="8b06c-124">Forme</span><span class="sxs-lookup"><span data-stu-id="8b06c-124">Hull</span></span> | <span data-ttu-id="8b06c-125">Domain</span><span class="sxs-lookup"><span data-stu-id="8b06c-125">Domain</span></span> | <span data-ttu-id="8b06c-126">Géométrie</span><span class="sxs-lookup"><span data-stu-id="8b06c-126">Geometry</span></span> | <span data-ttu-id="8b06c-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="8b06c-127">Pixel</span></span> | <span data-ttu-id="8b06c-128">Compute</span><span class="sxs-lookup"><span data-stu-id="8b06c-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8b06c-129">x</span><span class="sxs-lookup"><span data-stu-id="8b06c-129">x</span></span>      | <span data-ttu-id="8b06c-130">x</span><span class="sxs-lookup"><span data-stu-id="8b06c-130">x</span></span>    | <span data-ttu-id="8b06c-131">x</span><span class="sxs-lookup"><span data-stu-id="8b06c-131">x</span></span>      | <span data-ttu-id="8b06c-132">x</span><span class="sxs-lookup"><span data-stu-id="8b06c-132">x</span></span>        | <span data-ttu-id="8b06c-133">x</span><span class="sxs-lookup"><span data-stu-id="8b06c-133">x</span></span>     | <span data-ttu-id="8b06c-134">x</span><span class="sxs-lookup"><span data-stu-id="8b06c-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8b06c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b06c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b06c-136">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="8b06c-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="8b06c-137">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="8b06c-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




