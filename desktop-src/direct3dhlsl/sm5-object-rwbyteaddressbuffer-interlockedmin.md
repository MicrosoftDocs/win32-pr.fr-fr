---
title: 'RWByteAddressBuffer :: InterlockedMin, fonction'
description: Recherche la valeur minimale, atomiquement.
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- InterlockedMin fonction HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b818a1fa0897d103e7d609a676212c6db428935f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031262"
---
# <a name="interlockedmin-function"></a><span data-ttu-id="de80c-104">InterlockedMin fonction)</span><span class="sxs-lookup"><span data-stu-id="de80c-104">InterlockedMin function</span></span>

<span data-ttu-id="de80c-105">Recherche la valeur minimale, atomiquement.</span><span class="sxs-lookup"><span data-stu-id="de80c-105">Finds the minimum value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="de80c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de80c-106">Syntax</span></span>

``` syntax
void InterlockedMin(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="de80c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de80c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de80c-108">*dest* \[ . dans\]</span><span class="sxs-lookup"><span data-stu-id="de80c-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de80c-109">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="de80c-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="de80c-110">Adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="de80c-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="de80c-111">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de80c-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de80c-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="de80c-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="de80c-113">Valeur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="de80c-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="de80c-114">*\_ valeur d’origine* \[\]</span><span class="sxs-lookup"><span data-stu-id="de80c-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de80c-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="de80c-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="de80c-116">Valeur d'origine.</span><span class="sxs-lookup"><span data-stu-id="de80c-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de80c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de80c-117">Return value</span></span>

<span data-ttu-id="de80c-118">Rien</span><span class="sxs-lookup"><span data-stu-id="de80c-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="de80c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="de80c-119">Remarks</span></span>

<span data-ttu-id="de80c-120">Cette opération ne peut être effectuée que sur les ressources typées int et uint et les variables de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="de80c-120">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="de80c-121">Il existe trois utilisations possibles de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="de80c-121">There are three possible uses for this function.</span></span> <span data-ttu-id="de80c-122">La première est lorsque R est un type de variable de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="de80c-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="de80c-123">Dans ce cas, la fonction effectue un minimum atomique de la valeur dans le registre de mémoire partagée référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="de80c-123">In this case, the function performs an atomic minimum of the value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="de80c-124">Le deuxième scénario est lorsque R est un type de variable de ressource.</span><span class="sxs-lookup"><span data-stu-id="de80c-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="de80c-125">Dans ce scénario, la fonction effectue un minimum atomique de la valeur à l’emplacement de la ressource référencé par dest.</span><span class="sxs-lookup"><span data-stu-id="de80c-125">In this scenario, the function performs an atomic minimum of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="de80c-126">Enfin, le troisième scénario est lorsque R est un type de variable locale.</span><span class="sxs-lookup"><span data-stu-id="de80c-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="de80c-127">Dans ce scénario, la fonction réduit à un minimum de la valeur de dest et value, stockée dans dest.</span><span class="sxs-lookup"><span data-stu-id="de80c-127">In this scenario, the function reduces to a minimum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="de80c-128">La fonction surchargée a une variable de sortie supplémentaire qui sera définie sur la valeur d’origine de dest.</span><span class="sxs-lookup"><span data-stu-id="de80c-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="de80c-129">Cette opération surchargée est disponible uniquement lorsque R est accessible en lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="de80c-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="de80c-130">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="de80c-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="de80c-131">VS</span><span class="sxs-lookup"><span data-stu-id="de80c-131">VS</span></span>  | <span data-ttu-id="de80c-132">SH</span><span class="sxs-lookup"><span data-stu-id="de80c-132">HS</span></span>  | <span data-ttu-id="de80c-133">Source de données</span><span class="sxs-lookup"><span data-stu-id="de80c-133">DS</span></span>  | <span data-ttu-id="de80c-134">GS</span><span class="sxs-lookup"><span data-stu-id="de80c-134">GS</span></span>  | <span data-ttu-id="de80c-135">PS</span><span class="sxs-lookup"><span data-stu-id="de80c-135">PS</span></span>  | <span data-ttu-id="de80c-136">CS</span><span class="sxs-lookup"><span data-stu-id="de80c-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="de80c-137">x</span><span class="sxs-lookup"><span data-stu-id="de80c-137">x</span></span>   |  <span data-ttu-id="de80c-138">x</span><span class="sxs-lookup"><span data-stu-id="de80c-138">x</span></span>  | <span data-ttu-id="de80c-139">x</span><span class="sxs-lookup"><span data-stu-id="de80c-139">x</span></span>   | <span data-ttu-id="de80c-140">x</span><span class="sxs-lookup"><span data-stu-id="de80c-140">x</span></span>   | <span data-ttu-id="de80c-141">x</span><span class="sxs-lookup"><span data-stu-id="de80c-141">x</span></span>   | <span data-ttu-id="de80c-142">x</span><span class="sxs-lookup"><span data-stu-id="de80c-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="de80c-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de80c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de80c-144">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="de80c-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="de80c-145">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="de80c-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 