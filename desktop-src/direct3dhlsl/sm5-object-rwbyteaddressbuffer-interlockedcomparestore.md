---
title: 'RWByteAddressBuffer :: InterlockedCompareStore, fonction'
description: Ccompares l’entrée à la valeur de comparaison, atomiquement.
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
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
ms.openlocfilehash: abaa390ba74657e42b54a5147a7bc4006564a5fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842558"
---
# <a name="interlockedcomparestore-function"></a><span data-ttu-id="77e69-104">InterlockedCompareStore fonction)</span><span class="sxs-lookup"><span data-stu-id="77e69-104">InterlockedCompareStore function</span></span>

<span data-ttu-id="77e69-105">Ccompares l’entrée à la valeur de comparaison, atomiquement.</span><span class="sxs-lookup"><span data-stu-id="77e69-105">Ccompares the input to the comparison value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="77e69-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77e69-106">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a><span data-ttu-id="77e69-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77e69-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77e69-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="77e69-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e69-109">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77e69-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="77e69-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="77e69-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="77e69-111">*comparer la \_ valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77e69-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e69-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77e69-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="77e69-113">Valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="77e69-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="77e69-114">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77e69-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e69-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77e69-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="77e69-116">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="77e69-116">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77e69-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="77e69-117">Return value</span></span>

<span data-ttu-id="77e69-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="77e69-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77e69-119">Notes</span><span class="sxs-lookup"><span data-stu-id="77e69-119">Remarks</span></span>

<span data-ttu-id="77e69-120">Cette opération ne peut être effectuée que sur des ressources typées int ou uint et des variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="77e69-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="77e69-121">Il existe trois utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="77e69-121">There are three possible uses for this function.</span></span> <span data-ttu-id="77e69-122">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="77e69-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="77e69-123">Dans ce cas, la fonction effectue l’opération sur le registre de mémoire partagée référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="77e69-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="77e69-124">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="77e69-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="77e69-125">Dans ce scénario, la fonction effectue l’opération sur l’emplacement de la ressource référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="77e69-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="77e69-126">Enfin, le troisième scénario est lorsque R est un type de variable locale.</span><span class="sxs-lookup"><span data-stu-id="77e69-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="77e69-127">Dans ce scénario, la fonction réduit à l’opération effectuée à l’aide d’opérations locales.</span><span class="sxs-lookup"><span data-stu-id="77e69-127">In this scenario, the function reduces to the operation performed using local operations.</span></span>

<span data-ttu-id="77e69-128">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="77e69-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="77e69-129">VS</span><span class="sxs-lookup"><span data-stu-id="77e69-129">VS</span></span>  | <span data-ttu-id="77e69-130">SH</span><span class="sxs-lookup"><span data-stu-id="77e69-130">HS</span></span>  | <span data-ttu-id="77e69-131">Source de données</span><span class="sxs-lookup"><span data-stu-id="77e69-131">DS</span></span>  | <span data-ttu-id="77e69-132">GS</span><span class="sxs-lookup"><span data-stu-id="77e69-132">GS</span></span>  | <span data-ttu-id="77e69-133">PS</span><span class="sxs-lookup"><span data-stu-id="77e69-133">PS</span></span>  | <span data-ttu-id="77e69-134">CS</span><span class="sxs-lookup"><span data-stu-id="77e69-134">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="77e69-135">x</span><span class="sxs-lookup"><span data-stu-id="77e69-135">x</span></span>   | <span data-ttu-id="77e69-136">x</span><span class="sxs-lookup"><span data-stu-id="77e69-136">x</span></span>   | <span data-ttu-id="77e69-137">x</span><span class="sxs-lookup"><span data-stu-id="77e69-137">x</span></span>   | <span data-ttu-id="77e69-138">x</span><span class="sxs-lookup"><span data-stu-id="77e69-138">x</span></span>   | <span data-ttu-id="77e69-139">x</span><span class="sxs-lookup"><span data-stu-id="77e69-139">x</span></span>   | <span data-ttu-id="77e69-140">x</span><span class="sxs-lookup"><span data-stu-id="77e69-140">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="77e69-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77e69-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e69-142">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="77e69-142">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="77e69-143">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="77e69-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 