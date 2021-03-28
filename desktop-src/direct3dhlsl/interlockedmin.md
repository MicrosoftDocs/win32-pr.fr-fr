---
title: InterlockedMin, fonction (référence HLSL)
description: Exécute un minimum atomique garanti.
ms.assetid: a6d3d81c-45d7-4e15-b8ec-fa2e30f854ce
keywords:
- InterlockedMin fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c85be82f87ce62d03c824e8cd895166c18c262c
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104381398"
---
# <a name="interlockedmin-function-hlsl-reference"></a><span data-ttu-id="3c9cd-104">InterlockedMin, fonction (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="3c9cd-104">InterlockedMin function (HLSL reference)</span></span>

<span data-ttu-id="3c9cd-105">Exécute un minimum atomique garanti.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-105">Performs a guaranteed atomic min.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c9cd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c9cd-106">Syntax</span></span>

``` syntax
void InterlockedMin(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="3c9cd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c9cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c9cd-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="3c9cd-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c9cd-109">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="3c9cd-109">Type: **R**</span></span>

<span data-ttu-id="3c9cd-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="3c9cd-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c9cd-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c9cd-112">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="3c9cd-112">Type: **T**</span></span>

<span data-ttu-id="3c9cd-113">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="3c9cd-114">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="3c9cd-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c9cd-115">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="3c9cd-115">Type: **T**</span></span>

<span data-ttu-id="3c9cd-116">facultatif.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-116">Optional.</span></span> <span data-ttu-id="3c9cd-117">Valeur d’entrée d’origine.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c9cd-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3c9cd-118">Return value</span></span>

<span data-ttu-id="3c9cd-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c9cd-120">Notes</span><span class="sxs-lookup"><span data-stu-id="3c9cd-120">Remarks</span></span>

<span data-ttu-id="3c9cd-121">Cette opération ne peut être effectuée que sur les ressources typées int et uint et les variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-121">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="3c9cd-122">Il existe deux utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-122">There are two possible uses for this function.</span></span> <span data-ttu-id="3c9cd-123">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="3c9cd-124">Dans ce cas, la fonction effectue un minimum de valeur atomique sur le registre de mémoire partagée référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-124">In this case, the function performs an atomic min of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="3c9cd-125">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="3c9cd-126">Dans ce scénario, la fonction effectue un minimum de valeur atomique sur l’emplacement de la ressource référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-126">In this scenario, the function performs an atomic min of value to the resource location referenced by dest.</span></span> <span data-ttu-id="3c9cd-127">La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de dest.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="3c9cd-128">Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="3c9cd-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3c9cd-129">Minimum Shader Model</span></span>

<span data-ttu-id="3c9cd-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3c9cd-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3c9cd-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3c9cd-131">Shader Model</span></span>                                                                | <span data-ttu-id="3c9cd-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3c9cd-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3c9cd-133">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="3c9cd-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="3c9cd-134">Oui</span><span class="sxs-lookup"><span data-stu-id="3c9cd-134">yes</span></span>       |



 

<span data-ttu-id="3c9cd-135">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="3c9cd-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3c9cd-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="3c9cd-136">Vertex</span></span> | <span data-ttu-id="3c9cd-137">Forme</span><span class="sxs-lookup"><span data-stu-id="3c9cd-137">Hull</span></span> | <span data-ttu-id="3c9cd-138">Domain</span><span class="sxs-lookup"><span data-stu-id="3c9cd-138">Domain</span></span> | <span data-ttu-id="3c9cd-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="3c9cd-139">Geometry</span></span> | <span data-ttu-id="3c9cd-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="3c9cd-140">Pixel</span></span> | <span data-ttu-id="3c9cd-141">Compute</span><span class="sxs-lookup"><span data-stu-id="3c9cd-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3c9cd-142">x</span><span class="sxs-lookup"><span data-stu-id="3c9cd-142">x</span></span>      |  <span data-ttu-id="3c9cd-143">x</span><span class="sxs-lookup"><span data-stu-id="3c9cd-143">x</span></span>   |  <span data-ttu-id="3c9cd-144">x</span><span class="sxs-lookup"><span data-stu-id="3c9cd-144">x</span></span>     |  <span data-ttu-id="3c9cd-145">x</span><span class="sxs-lookup"><span data-stu-id="3c9cd-145">x</span></span>       | <span data-ttu-id="3c9cd-146">x</span><span class="sxs-lookup"><span data-stu-id="3c9cd-146">x</span></span>     | <span data-ttu-id="3c9cd-147">x</span><span class="sxs-lookup"><span data-stu-id="3c9cd-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3c9cd-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c9cd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c9cd-149">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="3c9cd-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="3c9cd-150">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3c9cd-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




