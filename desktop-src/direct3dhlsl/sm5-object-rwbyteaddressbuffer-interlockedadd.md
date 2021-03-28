---
title: 'RWByteAddressBuffer :: InterlockedAdd, fonction'
description: Ajoute la valeur, atomiquement.
ms.assetid: 27274aae-1e75-4626-9997-57c4e9393000
keywords:
- InterlockedAdd fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_location:
- winnt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d352ed97df15ce076c10950c6da94aaeaff0f2d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990929"
---
# <a name="interlockedadd-function"></a><span data-ttu-id="e3151-104">InterlockedAdd fonction)</span><span class="sxs-lookup"><span data-stu-id="e3151-104">InterlockedAdd function</span></span>

<span data-ttu-id="e3151-105">Ajoute la valeur, atomiquement.</span><span class="sxs-lookup"><span data-stu-id="e3151-105">Adds the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3151-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3151-106">Syntax</span></span>

``` syntax
void InterlockedAdd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="e3151-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3151-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3151-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="e3151-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3151-109">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e3151-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e3151-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="e3151-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="e3151-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3151-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3151-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e3151-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e3151-113">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="e3151-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="e3151-114">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="e3151-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3151-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e3151-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e3151-116">Valeur d'origine.</span><span class="sxs-lookup"><span data-stu-id="e3151-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3151-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e3151-117">Return value</span></span>

<span data-ttu-id="e3151-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e3151-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3151-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e3151-119">Remarks</span></span>

<span data-ttu-id="e3151-120">Cette opération ne peut être effectuée que sur des ressources typées int ou uint et des variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="e3151-120">This operation can be performed only on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="e3151-121">Il existe trois utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e3151-121">There are three possible uses for this function.</span></span> <span data-ttu-id="e3151-122">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="e3151-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="e3151-123">Dans ce cas, la fonction effectue un ajout atomique de valeur au registre de mémoire partagée référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="e3151-123">In this case, the function performs an atomic add of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="e3151-124">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="e3151-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="e3151-125">Dans ce scénario, la fonction effectue un ajout atomique de la valeur à l’emplacement de la ressource référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="e3151-125">In this scenario, the function performs an atomic add of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="e3151-126">Enfin, le troisième scénario est lorsque R est un type de variable locale.</span><span class="sxs-lookup"><span data-stu-id="e3151-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="e3151-127">Dans ce scénario, la fonction réduit à une somme de la valeur de dest et de value, stockée dans dest.</span><span class="sxs-lookup"><span data-stu-id="e3151-127">In this scenario, the function reduces to a sum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="e3151-128">La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de dest.</span><span class="sxs-lookup"><span data-stu-id="e3151-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="e3151-129">Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="e3151-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="e3151-130">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="e3151-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e3151-131">VS</span><span class="sxs-lookup"><span data-stu-id="e3151-131">VS</span></span>  | <span data-ttu-id="e3151-132">SH</span><span class="sxs-lookup"><span data-stu-id="e3151-132">HS</span></span>  | <span data-ttu-id="e3151-133">Source de données</span><span class="sxs-lookup"><span data-stu-id="e3151-133">DS</span></span>  | <span data-ttu-id="e3151-134">GS</span><span class="sxs-lookup"><span data-stu-id="e3151-134">GS</span></span>  | <span data-ttu-id="e3151-135">PS</span><span class="sxs-lookup"><span data-stu-id="e3151-135">PS</span></span>  | <span data-ttu-id="e3151-136">CS</span><span class="sxs-lookup"><span data-stu-id="e3151-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="e3151-137">x</span><span class="sxs-lookup"><span data-stu-id="e3151-137">x</span></span>   | <span data-ttu-id="e3151-138">x</span><span class="sxs-lookup"><span data-stu-id="e3151-138">x</span></span>   | <span data-ttu-id="e3151-139">x</span><span class="sxs-lookup"><span data-stu-id="e3151-139">x</span></span>   | <span data-ttu-id="e3151-140">x</span><span class="sxs-lookup"><span data-stu-id="e3151-140">x</span></span>   | <span data-ttu-id="e3151-141">x</span><span class="sxs-lookup"><span data-stu-id="e3151-141">x</span></span>   | <span data-ttu-id="e3151-142">x</span><span class="sxs-lookup"><span data-stu-id="e3151-142">x</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="e3151-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e3151-143">Requirements</span></span>




## <a name="see-also"></a><span data-ttu-id="e3151-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3151-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3151-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="e3151-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="e3151-146">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="e3151-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

