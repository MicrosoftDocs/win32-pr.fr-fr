---
title: InterlockedMax, fonction (référence HLSL)
description: Effectue un nombre maximal atomique garanti.
ms.assetid: ea2c67ef-3133-424d-9cc3-81da79aee87e
keywords:
- InterlockedMax fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 997641b086625532b99e3ae8d17be49cd71ae21f
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104381399"
---
# <a name="interlockedmax-function-hlsl-reference"></a><span data-ttu-id="f913a-104">InterlockedMax, fonction (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="f913a-104">InterlockedMax function (HLSL reference)</span></span>

<span data-ttu-id="f913a-105">Effectue un nombre maximal atomique garanti.</span><span class="sxs-lookup"><span data-stu-id="f913a-105">Performs a guaranteed atomic max.</span></span>

## <a name="syntax"></a><span data-ttu-id="f913a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f913a-106">Syntax</span></span>

``` syntax
void InterlockedMax(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="f913a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f913a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f913a-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="f913a-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f913a-109">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="f913a-109">Type: **R**</span></span>

<span data-ttu-id="f913a-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="f913a-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="f913a-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f913a-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f913a-112">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="f913a-112">Type: **T**</span></span>

<span data-ttu-id="f913a-113">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="f913a-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="f913a-114">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="f913a-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f913a-115">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="f913a-115">Type: **T**</span></span>

<span data-ttu-id="f913a-116">facultatif.</span><span class="sxs-lookup"><span data-stu-id="f913a-116">Optional.</span></span> <span data-ttu-id="f913a-117">Valeur d’entrée d’origine.</span><span class="sxs-lookup"><span data-stu-id="f913a-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f913a-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f913a-118">Return value</span></span>

<span data-ttu-id="f913a-119">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f913a-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f913a-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f913a-120">Remarks</span></span>

<span data-ttu-id="f913a-121">Cette opération ne peut être effectuée que sur les ressources typées int et uint et les variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="f913a-121">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="f913a-122">Il existe deux utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f913a-122">There are two possible uses for this function.</span></span> <span data-ttu-id="f913a-123">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="f913a-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="f913a-124">Dans ce cas, la fonction effectue un maximum atomique de valeur dans le registre de mémoire partagée référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="f913a-124">In this case, the function performs an atomic max of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="f913a-125">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="f913a-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="f913a-126">Dans ce scénario, la fonction effectue un maximum atomique de valeur à l’emplacement de la ressource référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="f913a-126">In this scenario, the function performs an atomic max of value to the resource location referenced by dest.</span></span> <span data-ttu-id="f913a-127">La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de dest.</span><span class="sxs-lookup"><span data-stu-id="f913a-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="f913a-128">Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="f913a-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="f913a-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f913a-129">Minimum Shader Model</span></span>

<span data-ttu-id="f913a-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f913a-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f913a-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f913a-131">Shader Model</span></span>                                                                | <span data-ttu-id="f913a-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f913a-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f913a-133">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="f913a-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f913a-134">Oui</span><span class="sxs-lookup"><span data-stu-id="f913a-134">yes</span></span>       |



 

<span data-ttu-id="f913a-135">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="f913a-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f913a-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="f913a-136">Vertex</span></span> | <span data-ttu-id="f913a-137">Forme</span><span class="sxs-lookup"><span data-stu-id="f913a-137">Hull</span></span> | <span data-ttu-id="f913a-138">Domain</span><span class="sxs-lookup"><span data-stu-id="f913a-138">Domain</span></span> | <span data-ttu-id="f913a-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="f913a-139">Geometry</span></span> | <span data-ttu-id="f913a-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="f913a-140">Pixel</span></span> | <span data-ttu-id="f913a-141">Compute</span><span class="sxs-lookup"><span data-stu-id="f913a-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f913a-142">x</span><span class="sxs-lookup"><span data-stu-id="f913a-142">x</span></span>      |  <span data-ttu-id="f913a-143">x</span><span class="sxs-lookup"><span data-stu-id="f913a-143">x</span></span>   |  <span data-ttu-id="f913a-144">x</span><span class="sxs-lookup"><span data-stu-id="f913a-144">x</span></span>     |  <span data-ttu-id="f913a-145">x</span><span class="sxs-lookup"><span data-stu-id="f913a-145">x</span></span>       | <span data-ttu-id="f913a-146">x</span><span class="sxs-lookup"><span data-stu-id="f913a-146">x</span></span>     | <span data-ttu-id="f913a-147">x</span><span class="sxs-lookup"><span data-stu-id="f913a-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f913a-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f913a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f913a-149">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="f913a-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="f913a-150">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f913a-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




