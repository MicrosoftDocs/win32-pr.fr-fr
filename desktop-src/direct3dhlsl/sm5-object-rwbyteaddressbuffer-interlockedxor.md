---
title: 'RWByteAddressBuffer :: InterlockedXor, fonction'
description: Effectue un XOR atomique sur la valeur.
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
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
ms.openlocfilehash: 920ae912c599b66a03a25d7bc8ecc9b199036b26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941012"
---
# <a name="interlockedxor-function"></a><span data-ttu-id="91ac5-104">InterlockedXor fonction)</span><span class="sxs-lookup"><span data-stu-id="91ac5-104">InterlockedXor function</span></span>

<span data-ttu-id="91ac5-105">Effectue un **Xor** atomique sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="91ac5-105">Performs an atomic **XOR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ac5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91ac5-106">Syntax</span></span>

``` syntax
void InterlockedXor(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="91ac5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91ac5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ac5-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="91ac5-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91ac5-109">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="91ac5-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="91ac5-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="91ac5-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="91ac5-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91ac5-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91ac5-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="91ac5-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="91ac5-113">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="91ac5-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="91ac5-114">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="91ac5-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91ac5-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="91ac5-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="91ac5-116">Valeur d'origine.</span><span class="sxs-lookup"><span data-stu-id="91ac5-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91ac5-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="91ac5-117">Return value</span></span>

<span data-ttu-id="91ac5-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="91ac5-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91ac5-119">Notes</span><span class="sxs-lookup"><span data-stu-id="91ac5-119">Remarks</span></span>

<span data-ttu-id="91ac5-120">Cette opération ne peut être effectuée que sur des ressources typées **int** ou **uint** et des variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="91ac5-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="91ac5-121">Il existe trois utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="91ac5-121">There are three possible uses for this function.</span></span> <span data-ttu-id="91ac5-122">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="91ac5-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="91ac5-123">Dans ce cas, la fonction effectue un **Xor** atomique avec la valeur du registre de mémoire partagée référencé par *dest*.</span><span class="sxs-lookup"><span data-stu-id="91ac5-123">In this case, the function performs an atomic **XOR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="91ac5-124">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="91ac5-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="91ac5-125">Dans ce scénario, la fonction effectue une **Xor** atomique avec la valeur de l’emplacement de la ressource référencée par *dest*.</span><span class="sxs-lookup"><span data-stu-id="91ac5-125">In this scenario, the function performs an atomic **XOR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="91ac5-126">Enfin, le troisième scénario est lorsque R est un type de variable locale.</span><span class="sxs-lookup"><span data-stu-id="91ac5-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="91ac5-127">Dans ce scénario, la fonction réduit à un **Xor** des valeurs de *dest* et *value*.</span><span class="sxs-lookup"><span data-stu-id="91ac5-127">In this scenario, the function reduces to an **XOR** of the values of *dest* and *value*.</span></span> <span data-ttu-id="91ac5-128">Le résultat de l’opération remplace la valeur dans *dest*.</span><span class="sxs-lookup"><span data-stu-id="91ac5-128">The result of the operation replaces the value in *dest*.</span></span> <span data-ttu-id="91ac5-129">La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de *dest*.</span><span class="sxs-lookup"><span data-stu-id="91ac5-129">The overloaded function has an additional output variable which will be set to the original value of *dest*.</span></span> <span data-ttu-id="91ac5-130">Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="91ac5-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="91ac5-131">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="91ac5-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="91ac5-132">VS</span><span class="sxs-lookup"><span data-stu-id="91ac5-132">VS</span></span>  | <span data-ttu-id="91ac5-133">SH</span><span class="sxs-lookup"><span data-stu-id="91ac5-133">HS</span></span>  | <span data-ttu-id="91ac5-134">Source de données</span><span class="sxs-lookup"><span data-stu-id="91ac5-134">DS</span></span>  | <span data-ttu-id="91ac5-135">GS</span><span class="sxs-lookup"><span data-stu-id="91ac5-135">GS</span></span>  | <span data-ttu-id="91ac5-136">PS</span><span class="sxs-lookup"><span data-stu-id="91ac5-136">PS</span></span>  | <span data-ttu-id="91ac5-137">CS</span><span class="sxs-lookup"><span data-stu-id="91ac5-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="91ac5-138">x</span><span class="sxs-lookup"><span data-stu-id="91ac5-138">x</span></span>   |  <span data-ttu-id="91ac5-139">x</span><span class="sxs-lookup"><span data-stu-id="91ac5-139">x</span></span>  | <span data-ttu-id="91ac5-140">x</span><span class="sxs-lookup"><span data-stu-id="91ac5-140">x</span></span>   | <span data-ttu-id="91ac5-141">x</span><span class="sxs-lookup"><span data-stu-id="91ac5-141">x</span></span>   | <span data-ttu-id="91ac5-142">x</span><span class="sxs-lookup"><span data-stu-id="91ac5-142">x</span></span>   | <span data-ttu-id="91ac5-143">x</span><span class="sxs-lookup"><span data-stu-id="91ac5-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="91ac5-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91ac5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ac5-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="91ac5-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="91ac5-146">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="91ac5-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 