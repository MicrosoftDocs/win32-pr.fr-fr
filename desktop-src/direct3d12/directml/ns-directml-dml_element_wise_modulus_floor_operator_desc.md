---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
description: Calcule le modulo, avec les mêmes résultats que le modulo Python, pour chaque paire d’éléments correspondants à partir des dizaines d’entrée, en plaçant le résultat dans l’élément correspondant de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_floor_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.openlocfilehash: 8c70bd4649a57270807ac408802fe07edd36d98e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803066"
---
# <a name="dml_element_wise_modulus_floor_operator_desc-structure-directmlh"></a><span data-ttu-id="104f0-103">Structure DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="104f0-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="104f0-104">Calcule le modulo, avec les mêmes résultats que le modulo Python, pour chaque paire d’éléments correspondants à partir des dizaines d’entrée, en plaçant le résultat dans l’élément correspondant de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="104f0-104">Computes the modulus, with the same results as the Python modulus, for each pair of corresponding elements from the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="104f0-105">Étant donné que le quotient est arrondi vers-inf, le résultat aura le même signe que le diviseur.</span><span class="sxs-lookup"><span data-stu-id="104f0-105">Because the quotient is rounded towards -inf, the result will have the same sign as the divisor.</span></span>

```
f(a, b) = a - (b * floor(a / b))
```

<span data-ttu-id="104f0-106">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que *OutputTensor* est autorisé à aliaser l’un des dizaines d’entrée pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="104f0-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="104f0-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="104f0-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="104f0-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="104f0-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="104f0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="104f0-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="104f0-110">Membres</span><span class="sxs-lookup"><span data-stu-id="104f0-110">Members</span></span>

`ATensor`

<span data-ttu-id="104f0-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="104f0-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="104f0-112">Tenseur contenant les entrées côté gauche.</span><span class="sxs-lookup"><span data-stu-id="104f0-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="104f0-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="104f0-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="104f0-114">Tenseur contenant les entrées côté droit.</span><span class="sxs-lookup"><span data-stu-id="104f0-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="104f0-115">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="104f0-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="104f0-116">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="104f0-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="104f0-117">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="104f0-117">Availability</span></span>
<span data-ttu-id="104f0-118">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="104f0-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="104f0-119">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="104f0-119">Tensor constraints</span></span>
<span data-ttu-id="104f0-120">*ATensor*, *BTensor* et *OutputTensor* doivent avoir le même *type de données*, *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="104f0-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="104f0-121">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="104f0-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="104f0-122">DML_FEATURE_LEVEL_3_0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="104f0-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="104f0-123">Tenseur</span><span class="sxs-lookup"><span data-stu-id="104f0-123">Tensor</span></span> | <span data-ttu-id="104f0-124">Type</span><span class="sxs-lookup"><span data-stu-id="104f0-124">Kind</span></span> | <span data-ttu-id="104f0-125">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="104f0-125">Supported dimension counts</span></span> | <span data-ttu-id="104f0-126">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="104f0-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="104f0-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="104f0-127">ATensor</span></span> | <span data-ttu-id="104f0-128">Entrée</span><span class="sxs-lookup"><span data-stu-id="104f0-128">Input</span></span> | <span data-ttu-id="104f0-129">1 à 8</span><span class="sxs-lookup"><span data-stu-id="104f0-129">1 to 8</span></span> | <span data-ttu-id="104f0-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="104f0-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="104f0-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="104f0-131">BTensor</span></span> | <span data-ttu-id="104f0-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="104f0-132">Input</span></span> | <span data-ttu-id="104f0-133">1 à 8</span><span class="sxs-lookup"><span data-stu-id="104f0-133">1 to 8</span></span> | <span data-ttu-id="104f0-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="104f0-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="104f0-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="104f0-135">OutputTensor</span></span> | <span data-ttu-id="104f0-136">Output</span><span class="sxs-lookup"><span data-stu-id="104f0-136">Output</span></span> | <span data-ttu-id="104f0-137">1 à 8</span><span class="sxs-lookup"><span data-stu-id="104f0-137">1 to 8</span></span> | <span data-ttu-id="104f0-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="104f0-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="104f0-139">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="104f0-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="104f0-140">Tenseur</span><span class="sxs-lookup"><span data-stu-id="104f0-140">Tensor</span></span> | <span data-ttu-id="104f0-141">Type</span><span class="sxs-lookup"><span data-stu-id="104f0-141">Kind</span></span> | <span data-ttu-id="104f0-142">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="104f0-142">Supported dimension counts</span></span> | <span data-ttu-id="104f0-143">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="104f0-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="104f0-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="104f0-144">ATensor</span></span> | <span data-ttu-id="104f0-145">Entrée</span><span class="sxs-lookup"><span data-stu-id="104f0-145">Input</span></span> | <span data-ttu-id="104f0-146">4</span><span class="sxs-lookup"><span data-stu-id="104f0-146">4</span></span> | <span data-ttu-id="104f0-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="104f0-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="104f0-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="104f0-148">BTensor</span></span> | <span data-ttu-id="104f0-149">Entrée</span><span class="sxs-lookup"><span data-stu-id="104f0-149">Input</span></span> | <span data-ttu-id="104f0-150">4</span><span class="sxs-lookup"><span data-stu-id="104f0-150">4</span></span> | <span data-ttu-id="104f0-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="104f0-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="104f0-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="104f0-152">OutputTensor</span></span> | <span data-ttu-id="104f0-153">Output</span><span class="sxs-lookup"><span data-stu-id="104f0-153">Output</span></span> | <span data-ttu-id="104f0-154">4</span><span class="sxs-lookup"><span data-stu-id="104f0-154">4</span></span> | <span data-ttu-id="104f0-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="104f0-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="104f0-156">Spécifications</span><span class="sxs-lookup"><span data-stu-id="104f0-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="104f0-157">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="104f0-157">**Header**</span></span> | <span data-ttu-id="104f0-158">directml. h</span><span class="sxs-lookup"><span data-stu-id="104f0-158">directml.h</span></span> |