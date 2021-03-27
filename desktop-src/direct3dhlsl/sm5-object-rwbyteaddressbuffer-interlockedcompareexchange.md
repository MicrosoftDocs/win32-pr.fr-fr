---
title: 'RWByteAddressBuffer :: InterlockedCompareExchange, fonction'
description: Compare l’entrée à la valeur de comparaison et échange le résultat, de manière atomique.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
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
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729141"
---
# <a name="interlockedcompareexchange-function"></a><span data-ttu-id="8a664-104">InterlockedCompareExchange fonction)</span><span class="sxs-lookup"><span data-stu-id="8a664-104">InterlockedCompareExchange function</span></span>

<span data-ttu-id="8a664-105">Compare l’entrée à la valeur de comparaison et échange le résultat, de manière atomique.</span><span class="sxs-lookup"><span data-stu-id="8a664-105">Compares the input to the comparison value and exchanges the result, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a664-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a664-106">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="8a664-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a664-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a664-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="8a664-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a664-109">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a664-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a664-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="8a664-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="8a664-111">*comparer la \_ valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a664-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a664-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a664-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a664-113">Valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="8a664-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="8a664-114">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a664-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a664-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a664-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a664-116">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="8a664-116">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="8a664-117">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="8a664-117">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a664-118">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8a664-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8a664-119">Valeur d'origine.</span><span class="sxs-lookup"><span data-stu-id="8a664-119">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a664-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8a664-120">Return value</span></span>

<span data-ttu-id="8a664-121">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8a664-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a664-122">Notes</span><span class="sxs-lookup"><span data-stu-id="8a664-122">Remarks</span></span>

<span data-ttu-id="8a664-123">Compare atomiquement la valeur de *dest* à *la \_ valeur de comparaison*, stocke la valeur dans *dest* si les valeurs correspondent, retourne la valeur d’origine de *dest* dans la *\_ valeur d’origine*.</span><span class="sxs-lookup"><span data-stu-id="8a664-123">Atomically compares the value in *dest* to *compare\_value*, stores value in *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="8a664-124">Cette opération ne peut être effectuée que sur des ressources typées **int** ou *uint* et des variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="8a664-124">This operation can only be performed on **int** or *uint* typed resources and shared memory variables.</span></span> <span data-ttu-id="8a664-125">Il existe trois utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="8a664-125">There are three possible uses for this function.</span></span> <span data-ttu-id="8a664-126">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="8a664-126">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="8a664-127">Dans ce cas, la fonction effectue l’opération sur le registre de mémoire partagée référencé par *dest*.</span><span class="sxs-lookup"><span data-stu-id="8a664-127">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="8a664-128">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="8a664-128">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="8a664-129">Dans ce scénario, la fonction effectue l’opération sur l’emplacement de la ressource référencé par *dest*.</span><span class="sxs-lookup"><span data-stu-id="8a664-129">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="8a664-130">Enfin, le troisième scénario est lorsque R est un type de variable locale.</span><span class="sxs-lookup"><span data-stu-id="8a664-130">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="8a664-131">Dans ce scénario, la fonction réduit à l’opération effectuée à l’aide d’opérations locales.</span><span class="sxs-lookup"><span data-stu-id="8a664-131">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="8a664-132">Cette opération est uniquement disponible lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="8a664-132">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="8a664-133">Si vous appelez **InterlockedCompareExchange** dans une boucle de nuanceur [**de calcul for**](dx-graphics-hlsl-for.md) ou [**while**](dx-graphics-hlsl-while.md) , pour compiler correctement, vous devez utiliser l’attribut de **\[ \_ \_ \] condition allow UAV** sur cette boucle.</span><span class="sxs-lookup"><span data-stu-id="8a664-133">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

<span data-ttu-id="8a664-134">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="8a664-134">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="8a664-135">VS</span><span class="sxs-lookup"><span data-stu-id="8a664-135">VS</span></span>  | <span data-ttu-id="8a664-136">SH</span><span class="sxs-lookup"><span data-stu-id="8a664-136">HS</span></span>  | <span data-ttu-id="8a664-137">Source de données</span><span class="sxs-lookup"><span data-stu-id="8a664-137">DS</span></span>  | <span data-ttu-id="8a664-138">GS</span><span class="sxs-lookup"><span data-stu-id="8a664-138">GS</span></span>  | <span data-ttu-id="8a664-139">PS</span><span class="sxs-lookup"><span data-stu-id="8a664-139">PS</span></span>  | <span data-ttu-id="8a664-140">CS</span><span class="sxs-lookup"><span data-stu-id="8a664-140">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="8a664-141">x</span><span class="sxs-lookup"><span data-stu-id="8a664-141">x</span></span>   | <span data-ttu-id="8a664-142">x</span><span class="sxs-lookup"><span data-stu-id="8a664-142">x</span></span>   | <span data-ttu-id="8a664-143">x</span><span class="sxs-lookup"><span data-stu-id="8a664-143">x</span></span>   | <span data-ttu-id="8a664-144">x</span><span class="sxs-lookup"><span data-stu-id="8a664-144">x</span></span>   | <span data-ttu-id="8a664-145">x</span><span class="sxs-lookup"><span data-stu-id="8a664-145">x</span></span>   | <span data-ttu-id="8a664-146">x</span><span class="sxs-lookup"><span data-stu-id="8a664-146">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="8a664-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a664-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a664-148">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="8a664-148">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="8a664-149">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="8a664-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 