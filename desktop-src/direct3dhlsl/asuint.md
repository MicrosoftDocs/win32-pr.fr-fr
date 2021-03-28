---
title: asuint fonction)
description: Réinterprète le modèle binaire d’une valeur 64 bits comme deux entiers 32 bits non signés.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- asuint fonction HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030388"
---
# <a name="asuint-function"></a><span data-ttu-id="db399-104">asuint fonction)</span><span class="sxs-lookup"><span data-stu-id="db399-104">asuint function</span></span>

<span data-ttu-id="db399-105">Réinterprète le modèle binaire d’une valeur 64 bits comme deux entiers 32 bits non signés.</span><span class="sxs-lookup"><span data-stu-id="db399-105">Reinterprets the bit pattern of a 64-bit value as two unsigned 32-bit integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="db399-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db399-106">Syntax</span></span>

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="db399-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db399-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db399-108">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db399-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db399-109">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="db399-109">Type: **double**</span></span>

<span data-ttu-id="db399-110">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="db399-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="db399-111">*lowbits* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="db399-111">*lowbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db399-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="db399-112">Type: **uint**</span></span>

<span data-ttu-id="db399-113">Modèle de *valeur* faible 32 bits.</span><span class="sxs-lookup"><span data-stu-id="db399-113">The low 32-bit pattern of *value*.</span></span>

</dd> <dt>

<span data-ttu-id="db399-114">*highbits* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="db399-114">*highbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db399-115">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="db399-115">Type: **uint**</span></span>

<span data-ttu-id="db399-116">Modèle de *valeur* élevée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="db399-116">The high 32-bit pattern of *value*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db399-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="db399-117">Return value</span></span>

<span data-ttu-id="db399-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="db399-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db399-119">Notes</span><span class="sxs-lookup"><span data-stu-id="db399-119">Remarks</span></span>

<span data-ttu-id="db399-120">Cette fonction est une autre version de l’intrinsèque [**asuint**](dx-graphics-hlsl-asuint.md) qui est disponible dans les modèles de nuanceur précédents et qui a été introduite pour le Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="db399-120">This function is an alternate version of the [**asuint**](dx-graphics-hlsl-asuint.md) intrinsic that has been available in earlier shader models, and was introduced for Shader Model 5.</span></span> <span data-ttu-id="db399-121">La fonction d’origine (reconnue dans le compilateur HLSL par sa signature différente) reste disponible pour le Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="db399-121">The original function (recognized in the HLSL compiler by its different signature) remains available to Shader Model 5.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="db399-122">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="db399-122">Minimum Shader Model</span></span>

<span data-ttu-id="db399-123">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="db399-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="db399-124">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="db399-124">Shader Model</span></span>                                                                | <span data-ttu-id="db399-125">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="db399-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="db399-126">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="db399-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="db399-127">Oui</span><span class="sxs-lookup"><span data-stu-id="db399-127">yes</span></span>       |



 

<span data-ttu-id="db399-128">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="db399-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="db399-129">Sommet</span><span class="sxs-lookup"><span data-stu-id="db399-129">Vertex</span></span> | <span data-ttu-id="db399-130">Forme</span><span class="sxs-lookup"><span data-stu-id="db399-130">Hull</span></span> | <span data-ttu-id="db399-131">Domain</span><span class="sxs-lookup"><span data-stu-id="db399-131">Domain</span></span> | <span data-ttu-id="db399-132">Géométrie</span><span class="sxs-lookup"><span data-stu-id="db399-132">Geometry</span></span> | <span data-ttu-id="db399-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="db399-133">Pixel</span></span> | <span data-ttu-id="db399-134">Compute</span><span class="sxs-lookup"><span data-stu-id="db399-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="db399-135">x</span><span class="sxs-lookup"><span data-stu-id="db399-135">x</span></span>      | <span data-ttu-id="db399-136">x</span><span class="sxs-lookup"><span data-stu-id="db399-136">x</span></span>    | <span data-ttu-id="db399-137">x</span><span class="sxs-lookup"><span data-stu-id="db399-137">x</span></span>      | <span data-ttu-id="db399-138">x</span><span class="sxs-lookup"><span data-stu-id="db399-138">x</span></span>        | <span data-ttu-id="db399-139">x</span><span class="sxs-lookup"><span data-stu-id="db399-139">x</span></span>     | <span data-ttu-id="db399-140">x</span><span class="sxs-lookup"><span data-stu-id="db399-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="db399-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db399-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db399-142">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="db399-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="db399-143">**asuint (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="db399-143">**asuint (DirectX HLSL)**</span></span>](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[<span data-ttu-id="db399-144">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="db399-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




