---
title: AsDouble fonction)
description: Réinterprète une valeur de cast (valeurs 2 32 bits) dans un double.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- AsDouble fonction HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa2c83ee01739a2e2ee9595d0a26e1bdb80fef1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030389"
---
# <a name="asdouble-function"></a><span data-ttu-id="45081-104">AsDouble fonction)</span><span class="sxs-lookup"><span data-stu-id="45081-104">asdouble function</span></span>

<span data-ttu-id="45081-105">Réinterprète une valeur de cast (valeurs 2 32 bits) dans un double.</span><span class="sxs-lookup"><span data-stu-id="45081-105">Reinterprets a cast value (two 32-bit values) into a double.</span></span>

## <a name="syntax"></a><span data-ttu-id="45081-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45081-106">Syntax</span></span>

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="45081-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45081-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45081-108">*lowbits* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45081-108">*lowbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45081-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="45081-109">Type: **uint**</span></span>

<span data-ttu-id="45081-110">Modèle de faible bit 32 de la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="45081-110">The low 32-bit pattern of the input value.</span></span>

</dd> <dt>

<span data-ttu-id="45081-111">*highbits* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45081-111">*highbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45081-112">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="45081-112">Type: **uint**</span></span>

<span data-ttu-id="45081-113">Modèle 32 bits élevé de la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="45081-113">The high 32-bit pattern of the input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45081-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45081-114">Return value</span></span>

<span data-ttu-id="45081-115">Type : **double**</span><span class="sxs-lookup"><span data-stu-id="45081-115">Type: **double**</span></span>

<span data-ttu-id="45081-116">Entrée (valeurs 2 32 bits) recastées en deux.</span><span class="sxs-lookup"><span data-stu-id="45081-116">The input (two 32-bit values) recast as a double.</span></span>

## <a name="remarks"></a><span data-ttu-id="45081-117">Notes</span><span class="sxs-lookup"><span data-stu-id="45081-117">Remarks</span></span>

<span data-ttu-id="45081-118">La version surchargée suivante est également disponible :</span><span class="sxs-lookup"><span data-stu-id="45081-118">The following overloaded version is also available:</span></span>

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

<span data-ttu-id="45081-119">Si la valeur d’entrée est de composants 2 32 bits, le type de retour contient un double.</span><span class="sxs-lookup"><span data-stu-id="45081-119">If the input value is two 32-bit components, the return type will contain one double.</span></span> <span data-ttu-id="45081-120">Si la valeur d’entrée est de composants 4 32 bits, le type de retour contient deux doubles.</span><span class="sxs-lookup"><span data-stu-id="45081-120">If the input value is four 32-bit components, the return type will contain two doubles.</span></span> <span data-ttu-id="45081-121">Si la valeur d’entrée est un type 64 bits, la valeur retournée aura le même nombre de composants que la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="45081-121">If the input value is a 64-bit type, the returned value will have the same number of components as the input value.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="45081-122">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="45081-122">Minimum Shader Model</span></span>

<span data-ttu-id="45081-123">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="45081-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="45081-124">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="45081-124">Shader Model</span></span>                                                                | <span data-ttu-id="45081-125">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="45081-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="45081-126">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="45081-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="45081-127">Oui</span><span class="sxs-lookup"><span data-stu-id="45081-127">yes</span></span>       |



 

<span data-ttu-id="45081-128">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="45081-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="45081-129">Sommet</span><span class="sxs-lookup"><span data-stu-id="45081-129">Vertex</span></span> | <span data-ttu-id="45081-130">Forme</span><span class="sxs-lookup"><span data-stu-id="45081-130">Hull</span></span> | <span data-ttu-id="45081-131">Domain</span><span class="sxs-lookup"><span data-stu-id="45081-131">Domain</span></span> | <span data-ttu-id="45081-132">Géométrie</span><span class="sxs-lookup"><span data-stu-id="45081-132">Geometry</span></span> | <span data-ttu-id="45081-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="45081-133">Pixel</span></span> | <span data-ttu-id="45081-134">Compute</span><span class="sxs-lookup"><span data-stu-id="45081-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="45081-135">x</span><span class="sxs-lookup"><span data-stu-id="45081-135">x</span></span>      | <span data-ttu-id="45081-136">x</span><span class="sxs-lookup"><span data-stu-id="45081-136">x</span></span>    | <span data-ttu-id="45081-137">x</span><span class="sxs-lookup"><span data-stu-id="45081-137">x</span></span>      | <span data-ttu-id="45081-138">x</span><span class="sxs-lookup"><span data-stu-id="45081-138">x</span></span>        | <span data-ttu-id="45081-139">x</span><span class="sxs-lookup"><span data-stu-id="45081-139">x</span></span>     | <span data-ttu-id="45081-140">x</span><span class="sxs-lookup"><span data-stu-id="45081-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="45081-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45081-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45081-142">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="45081-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="45081-143">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="45081-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




