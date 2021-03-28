---
title: 'RWByteAddressBuffer :: interverrouiller, fonction'
description: Exécute un Atomic ou sur la valeur.
ms.assetid: 3a05619b-db97-4cf1-af3c-12c376e605a6
keywords:
- Fonction d’interverrouillage HLSL
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14b902f70919c79ed3e313671ede709f284a1490
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941013"
---
# <a name="interlockedor-function"></a><span data-ttu-id="00c10-104">Fonction d’interverrouillage</span><span class="sxs-lookup"><span data-stu-id="00c10-104">InterlockedOr function</span></span>

<span data-ttu-id="00c10-105">Exécute un Atomic **ou** sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="00c10-105">Performs an atomic **OR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="00c10-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00c10-106">Syntax</span></span>

``` syntax
void InterlockedOr(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="00c10-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00c10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00c10-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="00c10-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00c10-109">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="00c10-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="00c10-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="00c10-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="00c10-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00c10-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00c10-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="00c10-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="00c10-113">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="00c10-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="00c10-114">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="00c10-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00c10-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="00c10-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="00c10-116">Valeur d'origine.</span><span class="sxs-lookup"><span data-stu-id="00c10-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00c10-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00c10-117">Return value</span></span>

<span data-ttu-id="00c10-118">Rien</span><span class="sxs-lookup"><span data-stu-id="00c10-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="00c10-119">Notes</span><span class="sxs-lookup"><span data-stu-id="00c10-119">Remarks</span></span>

<span data-ttu-id="00c10-120">Cette opération ne peut être effectuée que sur des ressources typées **int** ou **uint** et des variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="00c10-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="00c10-121">Il existe trois utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="00c10-121">There are three possible uses for this function.</span></span> <span data-ttu-id="00c10-122">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="00c10-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="00c10-123">Dans ce cas, la fonction exécute un Atomic **ou** avec la valeur du registre de mémoire partagée référencé par *dest*.</span><span class="sxs-lookup"><span data-stu-id="00c10-123">In this case, the function performs an atomic **OR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="00c10-124">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="00c10-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="00c10-125">Dans ce scénario, la fonction effectue un atomicité **ou** avec la valeur de l’emplacement de la ressource référencée par *dest*.</span><span class="sxs-lookup"><span data-stu-id="00c10-125">In this scenario, the function performs an atomic **OR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="00c10-126">Enfin, le troisième scénario est lorsque R est un type de variable locale.</span><span class="sxs-lookup"><span data-stu-id="00c10-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="00c10-127">Dans ce scénario, la fonction est réduite à un **ou** avec les valeurs de *dest* et *value*.</span><span class="sxs-lookup"><span data-stu-id="00c10-127">In this scenario, the function reduces to an **OR** with the values of *dest* and *value*.</span></span> <span data-ttu-id="00c10-128">Le résultat de l’opération remplace la valeur de *dest*.</span><span class="sxs-lookup"><span data-stu-id="00c10-128">The result of the operation replaces the value of *dest*.</span></span> <span data-ttu-id="00c10-129">La fonction surchargée a une variable de sortie supplémentaire, qui sera définie sur la valeur d’origine de *dest*.</span><span class="sxs-lookup"><span data-stu-id="00c10-129">The overloaded function has an additional output variable, which will be set to the original value of *dest*.</span></span> <span data-ttu-id="00c10-130">Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="00c10-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="00c10-131">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="00c10-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="00c10-132">VS</span><span class="sxs-lookup"><span data-stu-id="00c10-132">VS</span></span>  | <span data-ttu-id="00c10-133">SH</span><span class="sxs-lookup"><span data-stu-id="00c10-133">HS</span></span>  | <span data-ttu-id="00c10-134">Source de données</span><span class="sxs-lookup"><span data-stu-id="00c10-134">DS</span></span>  | <span data-ttu-id="00c10-135">GS</span><span class="sxs-lookup"><span data-stu-id="00c10-135">GS</span></span>  | <span data-ttu-id="00c10-136">PS</span><span class="sxs-lookup"><span data-stu-id="00c10-136">PS</span></span>  | <span data-ttu-id="00c10-137">CS</span><span class="sxs-lookup"><span data-stu-id="00c10-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="00c10-138">x</span><span class="sxs-lookup"><span data-stu-id="00c10-138">x</span></span>   |  <span data-ttu-id="00c10-139">x</span><span class="sxs-lookup"><span data-stu-id="00c10-139">x</span></span>  | <span data-ttu-id="00c10-140">x</span><span class="sxs-lookup"><span data-stu-id="00c10-140">x</span></span>   | <span data-ttu-id="00c10-141">x</span><span class="sxs-lookup"><span data-stu-id="00c10-141">x</span></span>   | <span data-ttu-id="00c10-142">x</span><span class="sxs-lookup"><span data-stu-id="00c10-142">x</span></span>   | <span data-ttu-id="00c10-143">x</span><span class="sxs-lookup"><span data-stu-id="00c10-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="00c10-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00c10-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00c10-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="00c10-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="00c10-146">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="00c10-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 