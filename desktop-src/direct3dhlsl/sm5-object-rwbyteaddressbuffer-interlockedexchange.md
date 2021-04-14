---
title: 'RWByteAddressBuffer :: Interlockedexchang, fonction'
description: Échange une valeur, de manière atomique.
ms.assetid: a50f4cba-a7a2-44b0-9de7-003b4c7a947f
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
ms.openlocfilehash: 47c51374b7dcd62ac208e0aa8811a8d693ce0ac6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990900"
---
# <a name="interlockedexchange-function"></a><span data-ttu-id="3791a-104">Interlockedexchang fonction)</span><span class="sxs-lookup"><span data-stu-id="3791a-104">InterlockedExchange function</span></span>

<span data-ttu-id="3791a-105">Échange une valeur, de manière atomique.</span><span class="sxs-lookup"><span data-stu-id="3791a-105">Exchanges a value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="3791a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3791a-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="3791a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3791a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3791a-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="3791a-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3791a-109">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3791a-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3791a-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="3791a-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="3791a-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3791a-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3791a-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3791a-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3791a-113">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="3791a-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="3791a-114">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="3791a-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3791a-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3791a-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3791a-116">Valeur d'origine.</span><span class="sxs-lookup"><span data-stu-id="3791a-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3791a-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3791a-117">Return value</span></span>

<span data-ttu-id="3791a-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3791a-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3791a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="3791a-119">Remarks</span></span>

<span data-ttu-id="3791a-120">Cette opération ne peut être effectuée que sur des ressources de type scalaire et des variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="3791a-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="3791a-121">Il existe trois utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="3791a-121">There are three possible uses for this function.</span></span> <span data-ttu-id="3791a-122">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="3791a-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="3791a-123">Dans ce cas, la fonction effectue l’opération sur le registre de mémoire partagée référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="3791a-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="3791a-124">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="3791a-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="3791a-125">Dans ce scénario, la fonction effectue l’opération sur l’emplacement de la ressource référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="3791a-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="3791a-126">Enfin, le troisième scénario est lorsque R est un type de variable locale.</span><span class="sxs-lookup"><span data-stu-id="3791a-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="3791a-127">Dans ce scénario, la fonction réduit à l’opération effectuée à l’aide d’opérations locales.</span><span class="sxs-lookup"><span data-stu-id="3791a-127">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="3791a-128">Cette opération est uniquement disponible lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="3791a-128">This operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="3791a-129">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="3791a-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3791a-130">VS</span><span class="sxs-lookup"><span data-stu-id="3791a-130">VS</span></span>  | <span data-ttu-id="3791a-131">SH</span><span class="sxs-lookup"><span data-stu-id="3791a-131">HS</span></span>  | <span data-ttu-id="3791a-132">Source de données</span><span class="sxs-lookup"><span data-stu-id="3791a-132">DS</span></span>  | <span data-ttu-id="3791a-133">GS</span><span class="sxs-lookup"><span data-stu-id="3791a-133">GS</span></span>  | <span data-ttu-id="3791a-134">PS</span><span class="sxs-lookup"><span data-stu-id="3791a-134">PS</span></span>  | <span data-ttu-id="3791a-135">CS</span><span class="sxs-lookup"><span data-stu-id="3791a-135">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
|  <span data-ttu-id="3791a-136">x</span><span class="sxs-lookup"><span data-stu-id="3791a-136">x</span></span>  |  <span data-ttu-id="3791a-137">x</span><span class="sxs-lookup"><span data-stu-id="3791a-137">x</span></span>  |  <span data-ttu-id="3791a-138">x</span><span class="sxs-lookup"><span data-stu-id="3791a-138">x</span></span>  |  <span data-ttu-id="3791a-139">x</span><span class="sxs-lookup"><span data-stu-id="3791a-139">x</span></span>  | <span data-ttu-id="3791a-140">x</span><span class="sxs-lookup"><span data-stu-id="3791a-140">x</span></span>   | <span data-ttu-id="3791a-141">x</span><span class="sxs-lookup"><span data-stu-id="3791a-141">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="3791a-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3791a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3791a-143">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="3791a-143">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="3791a-144">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3791a-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 