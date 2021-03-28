---
title: 'RWByteAddressBuffer :: InterlockedAnd, fonction'
description: Ands la valeur, atomiquement.
ms.assetid: c4024be0-3884-4af9-8075-76774c7c6178
keywords:
- InterlockedAnd fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a389da886b193815c7d4b2c1fe0a86db1f068fc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382137"
---
# <a name="interlockedand-function"></a><span data-ttu-id="2fa8b-104">InterlockedAnd fonction)</span><span class="sxs-lookup"><span data-stu-id="2fa8b-104">InterlockedAnd function</span></span>

<span data-ttu-id="2fa8b-105">Ands la valeur, atomiquement.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-105">Ands the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa8b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fa8b-106">Syntax</span></span>

``` syntax
void InterlockedAnd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="2fa8b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fa8b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fa8b-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="2fa8b-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa8b-109">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2fa8b-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2fa8b-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="2fa8b-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fa8b-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa8b-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2fa8b-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2fa8b-113">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="2fa8b-114">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="2fa8b-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa8b-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2fa8b-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2fa8b-116">Valeur d'origine.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fa8b-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2fa8b-117">Return value</span></span>

<span data-ttu-id="2fa8b-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fa8b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="2fa8b-119">Remarks</span></span>

<span data-ttu-id="2fa8b-120">Cette opération ne peut être effectuée que sur des ressources typées int ou uint et des variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="2fa8b-121">Il existe trois utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-121">There are three possible uses for this function.</span></span> <span data-ttu-id="2fa8b-122">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="2fa8b-123">Dans ce cas, la fonction effectue une valeur atomique et une valeur vers le registre de mémoire partagée référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-123">In this case, the function performs an atomic and of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="2fa8b-124">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="2fa8b-125">Dans ce scénario, la fonction effectue un atomique et une valeur à l’emplacement de la ressource référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-125">In this scenario, the function performs an atomic and of value to the resource location referenced by dest.</span></span> <span data-ttu-id="2fa8b-126">Enfin, le troisième scénario est lorsque R est un type de variable locale.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="2fa8b-127">Dans ce scénario, la fonction est réduite à un et de la valeur de dest et value, stockée dans dest.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-127">In this scenario, the function reduces to an and of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="2fa8b-128">La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de dest.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="2fa8b-129">Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="2fa8b-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="2fa8b-130">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="2fa8b-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2fa8b-131">VS</span><span class="sxs-lookup"><span data-stu-id="2fa8b-131">VS</span></span>  | <span data-ttu-id="2fa8b-132">SH</span><span class="sxs-lookup"><span data-stu-id="2fa8b-132">HS</span></span>  | <span data-ttu-id="2fa8b-133">Source de données</span><span class="sxs-lookup"><span data-stu-id="2fa8b-133">DS</span></span>  | <span data-ttu-id="2fa8b-134">GS</span><span class="sxs-lookup"><span data-stu-id="2fa8b-134">GS</span></span>  | <span data-ttu-id="2fa8b-135">PS</span><span class="sxs-lookup"><span data-stu-id="2fa8b-135">PS</span></span>  | <span data-ttu-id="2fa8b-136">CS</span><span class="sxs-lookup"><span data-stu-id="2fa8b-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="2fa8b-137">x</span><span class="sxs-lookup"><span data-stu-id="2fa8b-137">x</span></span>   | <span data-ttu-id="2fa8b-138">x</span><span class="sxs-lookup"><span data-stu-id="2fa8b-138">x</span></span>   |  <span data-ttu-id="2fa8b-139">x</span><span class="sxs-lookup"><span data-stu-id="2fa8b-139">x</span></span>  | <span data-ttu-id="2fa8b-140">x</span><span class="sxs-lookup"><span data-stu-id="2fa8b-140">x</span></span>   | <span data-ttu-id="2fa8b-141">x</span><span class="sxs-lookup"><span data-stu-id="2fa8b-141">x</span></span>   | <span data-ttu-id="2fa8b-142">x</span><span class="sxs-lookup"><span data-stu-id="2fa8b-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="2fa8b-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fa8b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa8b-144">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="2fa8b-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="2fa8b-145">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="2fa8b-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 