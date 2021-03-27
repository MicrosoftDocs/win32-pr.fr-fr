---
title: InterlockedXor, fonction (référence HLSL)
description: Exécute un XOR atomique garanti.
ms.assetid: 844ca31f-d051-4713-b9e1-dd6712ad36ca
keywords:
- InterlockedXor fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8ecaf0aa78a3bd2c1d79d10bea1e97299605398
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2020
ms.locfileid: "103679581"
---
# <a name="interlockedxor-function-hlsl-reference"></a><span data-ttu-id="578e4-104">InterlockedXor, fonction (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="578e4-104">InterlockedXor function (HLSL reference)</span></span>

<span data-ttu-id="578e4-105">Exécute un XOR atomique garanti.</span><span class="sxs-lookup"><span data-stu-id="578e4-105">Performs a guaranteed atomic xor.</span></span>

## <a name="syntax"></a><span data-ttu-id="578e4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="578e4-106">Syntax</span></span>

``` syntax
void InterlockedXor(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="578e4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="578e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="578e4-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="578e4-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="578e4-109">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="578e4-109">Type: **R**</span></span>

<span data-ttu-id="578e4-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="578e4-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="578e4-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="578e4-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="578e4-112">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="578e4-112">Type: **T**</span></span>

<span data-ttu-id="578e4-113">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="578e4-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="578e4-114">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="578e4-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="578e4-115">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="578e4-115">Type: **T**</span></span>

<span data-ttu-id="578e4-116">facultatif.</span><span class="sxs-lookup"><span data-stu-id="578e4-116">Optional.</span></span> <span data-ttu-id="578e4-117">Valeur d’entrée d’origine.</span><span class="sxs-lookup"><span data-stu-id="578e4-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="578e4-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="578e4-118">Return value</span></span>

<span data-ttu-id="578e4-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="578e4-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="578e4-120">Notes</span><span class="sxs-lookup"><span data-stu-id="578e4-120">Remarks</span></span>

<span data-ttu-id="578e4-121">Cette opération ne peut être effectuée que sur des ressources typées int ou uint et des variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="578e4-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="578e4-122">Il existe deux utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="578e4-122">There are two possible uses for this function.</span></span> <span data-ttu-id="578e4-123">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="578e4-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="578e4-124">Dans ce cas, la fonction effectue un XOR atomique de value sur le registre de mémoire partagée référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="578e4-124">In this case, the function performs an atomic XOR of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="578e4-125">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="578e4-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="578e4-126">Dans ce scénario, la fonction effectue une valeur Atomic XORof à l’emplacement de la ressource référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="578e4-126">In this scenario, the function performs an atomic XORof value to the resource location referenced by dest.</span></span> <span data-ttu-id="578e4-127">La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de dest.</span><span class="sxs-lookup"><span data-stu-id="578e4-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="578e4-128">Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="578e4-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="578e4-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="578e4-129">Minimum Shader Model</span></span>

<span data-ttu-id="578e4-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="578e4-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="578e4-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="578e4-131">Shader Model</span></span>                                                                | <span data-ttu-id="578e4-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="578e4-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="578e4-133">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="578e4-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="578e4-134">Oui</span><span class="sxs-lookup"><span data-stu-id="578e4-134">yes</span></span>       |



 

<span data-ttu-id="578e4-135">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="578e4-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="578e4-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="578e4-136">Vertex</span></span> | <span data-ttu-id="578e4-137">Forme</span><span class="sxs-lookup"><span data-stu-id="578e4-137">Hull</span></span> | <span data-ttu-id="578e4-138">Domain</span><span class="sxs-lookup"><span data-stu-id="578e4-138">Domain</span></span> | <span data-ttu-id="578e4-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="578e4-139">Geometry</span></span> | <span data-ttu-id="578e4-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="578e4-140">Pixel</span></span> | <span data-ttu-id="578e4-141">Compute</span><span class="sxs-lookup"><span data-stu-id="578e4-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|  <span data-ttu-id="578e4-142">x</span><span class="sxs-lookup"><span data-stu-id="578e4-142">x</span></span>     |  <span data-ttu-id="578e4-143">x</span><span class="sxs-lookup"><span data-stu-id="578e4-143">x</span></span>   | <span data-ttu-id="578e4-144">x</span><span class="sxs-lookup"><span data-stu-id="578e4-144">x</span></span>      |  <span data-ttu-id="578e4-145">x</span><span class="sxs-lookup"><span data-stu-id="578e4-145">x</span></span>       | <span data-ttu-id="578e4-146">x</span><span class="sxs-lookup"><span data-stu-id="578e4-146">x</span></span>     | <span data-ttu-id="578e4-147">x</span><span class="sxs-lookup"><span data-stu-id="578e4-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="578e4-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="578e4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578e4-149">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="578e4-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="578e4-150">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="578e4-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




