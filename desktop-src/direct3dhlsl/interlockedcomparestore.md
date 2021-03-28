---
title: InterlockedCompareStore, fonction (référence HLSL)
description: Compare atomiquement la destination à la valeur de comparaison. S’ils sont identiques, la destination est remplacée par la valeur d’entrée.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- InterlockedCompareStore fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104381400"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a><span data-ttu-id="b8afd-105">InterlockedCompareStore, fonction (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8afd-105">InterlockedCompareStore function (HLSL reference)</span></span>

<span data-ttu-id="b8afd-106">Compare atomiquement la destination à la valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="b8afd-106">Atomically compares the destination to the comparison value.</span></span> <span data-ttu-id="b8afd-107">S’ils sont identiques, la destination est remplacée par la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b8afd-107">If they are identical, the destination is overwritten with the input value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8afd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8afd-108">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="b8afd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8afd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8afd-110">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="b8afd-110">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8afd-111">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="b8afd-111">Type: **R**</span></span>

<span data-ttu-id="b8afd-112">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="b8afd-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="b8afd-113">*comparer la \_ valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8afd-113">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8afd-114">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="b8afd-114">Type: **T**</span></span>

<span data-ttu-id="b8afd-115">Valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="b8afd-115">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="b8afd-116">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8afd-116">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8afd-117">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="b8afd-117">Type: **T**</span></span>

<span data-ttu-id="b8afd-118">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="b8afd-118">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8afd-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b8afd-119">Return value</span></span>

<span data-ttu-id="b8afd-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b8afd-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8afd-121">Notes</span><span class="sxs-lookup"><span data-stu-id="b8afd-121">Remarks</span></span>

<span data-ttu-id="b8afd-122">Compare atomiquement la valeur référencée par *dest* avec *la \_ valeur de comparaison* et stocke la *valeur* dans l’emplacement référencé par *dest* si les valeurs correspondent.</span><span class="sxs-lookup"><span data-stu-id="b8afd-122">Atomically compares the value referenced by *dest* with *compare\_value* and stores *value* in the location referenced by *dest* if the values match.</span></span> <span data-ttu-id="b8afd-123">Cette opération ne peut être effectuée que sur des ressources typées **int** ou **uint** et des variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="b8afd-123">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="b8afd-124">Il existe deux utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="b8afd-124">There are two possible uses for this function.</span></span> <span data-ttu-id="b8afd-125">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="b8afd-125">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="b8afd-126">Dans ce cas, la fonction effectue l’opération sur le registre de mémoire partagée référencé par *dest*.</span><span class="sxs-lookup"><span data-stu-id="b8afd-126">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="b8afd-127">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="b8afd-127">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="b8afd-128">Dans ce scénario, la fonction effectue l’opération sur l’emplacement de la ressource référencé par *dest*.</span><span class="sxs-lookup"><span data-stu-id="b8afd-128">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="b8afd-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b8afd-129">Minimum Shader Model</span></span>

<span data-ttu-id="b8afd-130">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="b8afd-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b8afd-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b8afd-131">Shader Model</span></span>                                                                | <span data-ttu-id="b8afd-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b8afd-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="b8afd-133">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="b8afd-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="b8afd-134">Oui</span><span class="sxs-lookup"><span data-stu-id="b8afd-134">yes</span></span>       |



 

<span data-ttu-id="b8afd-135">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="b8afd-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="b8afd-136">Sommet</span><span class="sxs-lookup"><span data-stu-id="b8afd-136">Vertex</span></span> | <span data-ttu-id="b8afd-137">Forme</span><span class="sxs-lookup"><span data-stu-id="b8afd-137">Hull</span></span> | <span data-ttu-id="b8afd-138">Domain</span><span class="sxs-lookup"><span data-stu-id="b8afd-138">Domain</span></span> | <span data-ttu-id="b8afd-139">Géométrie</span><span class="sxs-lookup"><span data-stu-id="b8afd-139">Geometry</span></span> | <span data-ttu-id="b8afd-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="b8afd-140">Pixel</span></span> | <span data-ttu-id="b8afd-141">Compute</span><span class="sxs-lookup"><span data-stu-id="b8afd-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|  <span data-ttu-id="b8afd-142">x</span><span class="sxs-lookup"><span data-stu-id="b8afd-142">x</span></span>     | <span data-ttu-id="b8afd-143">x</span><span class="sxs-lookup"><span data-stu-id="b8afd-143">x</span></span>    |  <span data-ttu-id="b8afd-144">x</span><span class="sxs-lookup"><span data-stu-id="b8afd-144">x</span></span>     |  <span data-ttu-id="b8afd-145">x</span><span class="sxs-lookup"><span data-stu-id="b8afd-145">x</span></span>       | <span data-ttu-id="b8afd-146">x</span><span class="sxs-lookup"><span data-stu-id="b8afd-146">x</span></span>     | <span data-ttu-id="b8afd-147">x</span><span class="sxs-lookup"><span data-stu-id="b8afd-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b8afd-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8afd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8afd-149">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="b8afd-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="b8afd-150">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="b8afd-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




