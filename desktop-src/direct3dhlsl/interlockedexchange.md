---
title: Interlockedexchang, fonction (référence HLSL)
description: Affecte la valeur à dest et retourne la valeur d’origine.
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- Interlockedexchang fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c39dc4f68429fa3f070d446f998fd528a99af01
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104971663"
---
# <a name="interlockedexchange-function-hlsl-reference"></a><span data-ttu-id="44f2c-104">Interlockedexchang, fonction (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="44f2c-104">InterlockedExchange function (HLSL reference)</span></span>

<span data-ttu-id="44f2c-105">Affecte la valeur à dest et retourne la valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="44f2c-105">Assigns value to dest and returns the original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="44f2c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44f2c-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="44f2c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44f2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44f2c-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="44f2c-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44f2c-109">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="44f2c-109">Type: **R**</span></span>

<span data-ttu-id="44f2c-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="44f2c-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="44f2c-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44f2c-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44f2c-112">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="44f2c-112">Type: **T**</span></span>

<span data-ttu-id="44f2c-113">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="44f2c-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="44f2c-114">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="44f2c-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44f2c-115">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="44f2c-115">Type: **T**</span></span>

<span data-ttu-id="44f2c-116">Valeur d'origine.</span><span class="sxs-lookup"><span data-stu-id="44f2c-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44f2c-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="44f2c-117">Return value</span></span>

<span data-ttu-id="44f2c-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="44f2c-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f2c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="44f2c-119">Remarks</span></span>

<span data-ttu-id="44f2c-120">Cette opération ne peut être effectuée que sur des ressources de type scalaire et des variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="44f2c-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="44f2c-121">Il existe deux utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="44f2c-121">There are two possible uses for this function.</span></span> <span data-ttu-id="44f2c-122">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="44f2c-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="44f2c-123">Dans ce cas, la fonction effectue l’opération sur le registre de mémoire partagée référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="44f2c-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="44f2c-124">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="44f2c-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="44f2c-125">Dans ce scénario, la fonction effectue l’opération sur l’emplacement de la ressource référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="44f2c-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="44f2c-126">Cette opération est uniquement disponible lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="44f2c-126">This operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="44f2c-127">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="44f2c-127">Minimum Shader Model</span></span>

<span data-ttu-id="44f2c-128">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="44f2c-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="44f2c-129">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="44f2c-129">Shader Model</span></span>                                                                | <span data-ttu-id="44f2c-130">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="44f2c-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="44f2c-131">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="44f2c-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="44f2c-132">Oui</span><span class="sxs-lookup"><span data-stu-id="44f2c-132">yes</span></span>       |



 

<span data-ttu-id="44f2c-133">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="44f2c-133">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="44f2c-134">Sommet</span><span class="sxs-lookup"><span data-stu-id="44f2c-134">Vertex</span></span> | <span data-ttu-id="44f2c-135">Forme</span><span class="sxs-lookup"><span data-stu-id="44f2c-135">Hull</span></span> | <span data-ttu-id="44f2c-136">Domain</span><span class="sxs-lookup"><span data-stu-id="44f2c-136">Domain</span></span> | <span data-ttu-id="44f2c-137">Géométrie</span><span class="sxs-lookup"><span data-stu-id="44f2c-137">Geometry</span></span> | <span data-ttu-id="44f2c-138">Pixel</span><span class="sxs-lookup"><span data-stu-id="44f2c-138">Pixel</span></span> | <span data-ttu-id="44f2c-139">Compute</span><span class="sxs-lookup"><span data-stu-id="44f2c-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="44f2c-140">x</span><span class="sxs-lookup"><span data-stu-id="44f2c-140">x</span></span>      |  <span data-ttu-id="44f2c-141">x</span><span class="sxs-lookup"><span data-stu-id="44f2c-141">x</span></span>   | <span data-ttu-id="44f2c-142">x</span><span class="sxs-lookup"><span data-stu-id="44f2c-142">x</span></span>      |  <span data-ttu-id="44f2c-143">x</span><span class="sxs-lookup"><span data-stu-id="44f2c-143">x</span></span>       | <span data-ttu-id="44f2c-144">x</span><span class="sxs-lookup"><span data-stu-id="44f2c-144">x</span></span>     | <span data-ttu-id="44f2c-145">x</span><span class="sxs-lookup"><span data-stu-id="44f2c-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="44f2c-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44f2c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f2c-147">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="44f2c-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="44f2c-148">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="44f2c-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




