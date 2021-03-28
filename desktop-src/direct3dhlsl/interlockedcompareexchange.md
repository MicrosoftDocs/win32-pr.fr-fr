---
title: InterlockedCompareExchange, fonction (référence HLSL)
description: Compare atomiquement la destination à la valeur de comparaison. S’ils sont identiques, la destination est remplacée par la valeur d’entrée. La valeur d’origine est définie sur la valeur d’origine de la destination.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- InterlockedCompareExchange fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104990881"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a><span data-ttu-id="09130-106">InterlockedCompareExchange, fonction (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="09130-106">InterlockedCompareExchange function (HLSL reference)</span></span>

<span data-ttu-id="09130-107">Compare atomiquement la destination à la valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="09130-107">Atomically compares the destination with the comparison value.</span></span> <span data-ttu-id="09130-108">S’ils sont identiques, la destination est remplacée par la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="09130-108">If they are identical, the destination is overwritten with the input value.</span></span> <span data-ttu-id="09130-109">La valeur d’origine est définie sur la valeur d’origine de la destination.</span><span class="sxs-lookup"><span data-stu-id="09130-109">The original value is set to the destination's original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="09130-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09130-110">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="09130-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09130-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09130-112">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="09130-112">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09130-113">Type : **R**</span><span class="sxs-lookup"><span data-stu-id="09130-113">Type: **R**</span></span>

<span data-ttu-id="09130-114">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="09130-114">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="09130-115">*comparer la \_ valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09130-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09130-116">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="09130-116">Type: **T**</span></span>

<span data-ttu-id="09130-117">Valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="09130-117">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="09130-118">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09130-118">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09130-119">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="09130-119">Type: **T**</span></span>

<span data-ttu-id="09130-120">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="09130-120">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="09130-121">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="09130-121">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09130-122">Type : **T**</span><span class="sxs-lookup"><span data-stu-id="09130-122">Type: **T**</span></span>

<span data-ttu-id="09130-123">Valeur d'origine.</span><span class="sxs-lookup"><span data-stu-id="09130-123">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09130-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="09130-124">Return value</span></span>

<span data-ttu-id="09130-125">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="09130-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09130-126">Notes</span><span class="sxs-lookup"><span data-stu-id="09130-126">Remarks</span></span>

<span data-ttu-id="09130-127">Compare atomiquement la valeur référencée par *dest* avec *la \_ valeur de comparaison*, stocke la *valeur* dans l’emplacement référencé par *dest* si les valeurs correspondent, retourne la valeur d’origine de *dest* dans la *\_ valeur d’origine*.</span><span class="sxs-lookup"><span data-stu-id="09130-127">Atomically compares the value referenced by *dest* with *compare\_value*, stores *value* in the location referenced by *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="09130-128">Cette opération ne peut être effectuée que sur des ressources typées **int** ou **uint** et des variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="09130-128">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="09130-129">Il existe deux utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="09130-129">There are two possible uses for this function.</span></span> <span data-ttu-id="09130-130">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="09130-130">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="09130-131">Dans ce cas, la fonction effectue l’opération sur le registre de mémoire partagée référencé par *dest*.</span><span class="sxs-lookup"><span data-stu-id="09130-131">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="09130-132">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="09130-132">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="09130-133">Dans ce scénario, la fonction effectue l’opération sur l’emplacement de la ressource référencé par *dest*.</span><span class="sxs-lookup"><span data-stu-id="09130-133">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="09130-134">Cette opération est uniquement disponible lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="09130-134">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="09130-135">Si vous appelez **InterlockedCompareExchange** dans une boucle de nuanceur [**de calcul for**](dx-graphics-hlsl-for.md) ou [**while**](dx-graphics-hlsl-while.md) , pour compiler correctement, vous devez utiliser l’attribut de **\[ \_ \_ \] condition allow UAV** sur cette boucle.</span><span class="sxs-lookup"><span data-stu-id="09130-135">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

### <a name="minimum-shader-model"></a><span data-ttu-id="09130-136">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="09130-136">Minimum Shader Model</span></span>

<span data-ttu-id="09130-137">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="09130-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="09130-138">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="09130-138">Shader Model</span></span>                                                                | <span data-ttu-id="09130-139">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="09130-139">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="09130-140">[Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs</span><span class="sxs-lookup"><span data-stu-id="09130-140">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="09130-141">Oui</span><span class="sxs-lookup"><span data-stu-id="09130-141">yes</span></span>       |



 

<span data-ttu-id="09130-142">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="09130-142">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="09130-143">Sommet</span><span class="sxs-lookup"><span data-stu-id="09130-143">Vertex</span></span> | <span data-ttu-id="09130-144">Forme</span><span class="sxs-lookup"><span data-stu-id="09130-144">Hull</span></span> | <span data-ttu-id="09130-145">Domain</span><span class="sxs-lookup"><span data-stu-id="09130-145">Domain</span></span> | <span data-ttu-id="09130-146">Géométrie</span><span class="sxs-lookup"><span data-stu-id="09130-146">Geometry</span></span> | <span data-ttu-id="09130-147">Pixel</span><span class="sxs-lookup"><span data-stu-id="09130-147">Pixel</span></span> | <span data-ttu-id="09130-148">Compute</span><span class="sxs-lookup"><span data-stu-id="09130-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="09130-149">x</span><span class="sxs-lookup"><span data-stu-id="09130-149">x</span></span>      |  <span data-ttu-id="09130-150">x</span><span class="sxs-lookup"><span data-stu-id="09130-150">x</span></span>   |  <span data-ttu-id="09130-151">x</span><span class="sxs-lookup"><span data-stu-id="09130-151">x</span></span>     |  <span data-ttu-id="09130-152">x</span><span class="sxs-lookup"><span data-stu-id="09130-152">x</span></span>       | <span data-ttu-id="09130-153">x</span><span class="sxs-lookup"><span data-stu-id="09130-153">x</span></span>     | <span data-ttu-id="09130-154">x</span><span class="sxs-lookup"><span data-stu-id="09130-154">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="09130-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09130-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09130-156">Fonctions intrinsèques</span><span class="sxs-lookup"><span data-stu-id="09130-156">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="09130-157">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="09130-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




