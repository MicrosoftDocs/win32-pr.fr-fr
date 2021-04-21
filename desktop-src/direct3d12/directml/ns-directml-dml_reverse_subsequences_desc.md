---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Inverse les éléments d’une ou plusieurs sous- *séquences* d’un tenseur. L’ensemble de sous-séquences à inverser est choisi en fonction des longueurs d’axe et de séquence fournies.
helpviewer_keywords:
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure
- direct3d12.dml_reverse_subsequences_operator_desc
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.openlocfilehash: 3deddea3d60db1a8689ceabfac92ff17393b7606
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804002"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a><span data-ttu-id="0d5b8-104">Structure DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="0d5b8-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="0d5b8-105">Inverse les éléments d’une ou plusieurs sous- *séquences* d’un tenseur.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-105">Reverses the elements of one or more *subsequences* of a tensor.</span></span> <span data-ttu-id="0d5b8-106">L’ensemble de sous-séquences à inverser est choisi en fonction des longueurs d’axe et de séquence fournies.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-106">The set of subsequences to be reversed is chosen based on the provided axis and sequence lengths.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d5b8-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="0d5b8-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="0d5b8-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d5b8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d5b8-109">Syntax</span></span>
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="0d5b8-110">Membres</span><span class="sxs-lookup"><span data-stu-id="0d5b8-110">Members</span></span>

`InputTensor`

<span data-ttu-id="0d5b8-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0d5b8-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0d5b8-112">Tenseur d’entrée contenant les éléments à inverser.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-112">The input tensor containing elements to be reversed.</span></span>


`SequenceLengthsTensor`

<span data-ttu-id="0d5b8-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0d5b8-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0d5b8-114">Tenseur contenant une valeur pour chaque sous-séquence à inverser, indiquant la longueur des éléments de cette sous-séquence.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-114">A tensor containing a value for each subsequence to be reversed, denoting the length in elements of that subsequence.</span></span> <span data-ttu-id="0d5b8-115">Seuls les éléments de la longueur de la sous-séquence sont inversés. les éléments restants le long de cet axe sont copiés dans la sortie sans modification.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-115">Only the elements within the length of the subsequence are reversed; the remaining elements along that axis are copied to the output unchanged.</span></span>

<span data-ttu-id="0d5b8-116">Ce tenseur doit avoir un nombre de dimensions et des tailles égales à *InputTensor*, *à l’exception* de la dimension spécifiée par le paramètre *Axis* .</span><span class="sxs-lookup"><span data-stu-id="0d5b8-116">This tensor must have dimension count and sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter.</span></span> <span data-ttu-id="0d5b8-117">La taille de la dimension de l' *axe* doit être 1.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-117">The size of the *Axis* dimension must be 1.</span></span> <span data-ttu-id="0d5b8-118">Par exemple, si *InputTensor* a une taille de `{2,3,4,5}` , et *Axis* est 1, les tailles de *SequenceLengthsTensor* doivent être `{2,1,4,5}` .</span><span class="sxs-lookup"><span data-stu-id="0d5b8-118">For example if the *InputTensor* has sizes of `{2,3,4,5}`, and *Axis* is 1, then the sizes of the *SequenceLengthsTensor* must be `{2,1,4,5}`.</span></span>

<span data-ttu-id="0d5b8-119">Si la longueur d’une sous-séquence dépasse le nombre maximal d’éléments sur cet axe, cet opérateur se comporte comme si la valeur était ancrée au maximum.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-119">If the length of a subsequence exceeds the maximum number of elements along that axis, then this operator behaves as if the value were clamped to the maximum.</span></span>


`OutputTensor`

<span data-ttu-id="0d5b8-120">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0d5b8-120">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0d5b8-121">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-121">The output tensor to write the results to.</span></span> <span data-ttu-id="0d5b8-122">Ce tenseur doit avoir les mêmes tailles et le même type de données que le *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-122">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="0d5b8-123">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0d5b8-123">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="0d5b8-124">Index de la dimension sur laquelle les éléments sont retournés.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-124">The index of the dimension to reverse elements over.</span></span> <span data-ttu-id="0d5b8-125">Cette valeur doit être inférieure à la DimensionCount du *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-125">This value must be less than the DimensionCount of the *InputTensor*.</span></span>

## <a name="examples"></a><span data-ttu-id="0d5b8-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="0d5b8-126">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="0d5b8-127">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="0d5b8-127">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,3,1}, DataType:UINT32)
[[[[2],
   [4],
   [3]]]]

Axis: 3

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  4],
   [ 8,  7,  6,  5],
   [11, 10,  9, 12]]]]
```

### <a name="example-2-reversing-along-a-different-axis"></a><span data-ttu-id="0d5b8-128">Exemple 2.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-128">Example 2.</span></span> <span data-ttu-id="0d5b8-129">Inverser le long d’un axe différent</span><span class="sxs-lookup"><span data-stu-id="0d5b8-129">Reversing along a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,1,4}, DataType:UINT32)
[[[[2, 3, 1, 0]]]]

Axis: 2

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[5, 10,  3,  4], // Notice that sequence lengths of 1 and 0 are effective nops
   [1,  6,  7,  8],
   [9,  2, 11, 12]]]]
```

## <a name="availability"></a><span data-ttu-id="0d5b8-130">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="0d5b8-130">Availability</span></span>
<span data-ttu-id="0d5b8-131">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="0d5b8-131">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="0d5b8-132">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="0d5b8-132">Tensor constraints</span></span>
* <span data-ttu-id="0d5b8-133">*InputTensor*, *OutputTensor* et *SequenceLengthsTensor* doivent avoir le même *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-133">*InputTensor*, *OutputTensor*, and *SequenceLengthsTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="0d5b8-134">*InputTensor* et *OutputTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="0d5b8-134">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="0d5b8-135">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="0d5b8-135">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="0d5b8-136">DML_FEATURE_LEVEL_3_0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0d5b8-136">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="0d5b8-137">Tenseur</span><span class="sxs-lookup"><span data-stu-id="0d5b8-137">Tensor</span></span> | <span data-ttu-id="0d5b8-138">Type</span><span class="sxs-lookup"><span data-stu-id="0d5b8-138">Kind</span></span> | <span data-ttu-id="0d5b8-139">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="0d5b8-139">Supported dimension counts</span></span> | <span data-ttu-id="0d5b8-140">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d5b8-140">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0d5b8-141">InputTensor</span><span class="sxs-lookup"><span data-stu-id="0d5b8-141">InputTensor</span></span> | <span data-ttu-id="0d5b8-142">Entrée</span><span class="sxs-lookup"><span data-stu-id="0d5b8-142">Input</span></span> | <span data-ttu-id="0d5b8-143">4 à 5</span><span class="sxs-lookup"><span data-stu-id="0d5b8-143">4 to 5</span></span> | <span data-ttu-id="0d5b8-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="0d5b8-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="0d5b8-145">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="0d5b8-145">SequenceLengthsTensor</span></span> | <span data-ttu-id="0d5b8-146">Entrée</span><span class="sxs-lookup"><span data-stu-id="0d5b8-146">Input</span></span> | <span data-ttu-id="0d5b8-147">4 à 5</span><span class="sxs-lookup"><span data-stu-id="0d5b8-147">4 to 5</span></span> | <span data-ttu-id="0d5b8-148">UINT32</span><span class="sxs-lookup"><span data-stu-id="0d5b8-148">UINT32</span></span> |
| <span data-ttu-id="0d5b8-149">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="0d5b8-149">OutputTensor</span></span> | <span data-ttu-id="0d5b8-150">Output</span><span class="sxs-lookup"><span data-stu-id="0d5b8-150">Output</span></span> | <span data-ttu-id="0d5b8-151">4 à 5</span><span class="sxs-lookup"><span data-stu-id="0d5b8-151">4 to 5</span></span> | <span data-ttu-id="0d5b8-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="0d5b8-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="0d5b8-153">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0d5b8-153">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="0d5b8-154">Tenseur</span><span class="sxs-lookup"><span data-stu-id="0d5b8-154">Tensor</span></span> | <span data-ttu-id="0d5b8-155">Type</span><span class="sxs-lookup"><span data-stu-id="0d5b8-155">Kind</span></span> | <span data-ttu-id="0d5b8-156">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="0d5b8-156">Supported dimension counts</span></span> | <span data-ttu-id="0d5b8-157">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d5b8-157">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0d5b8-158">InputTensor</span><span class="sxs-lookup"><span data-stu-id="0d5b8-158">InputTensor</span></span> | <span data-ttu-id="0d5b8-159">Entrée</span><span class="sxs-lookup"><span data-stu-id="0d5b8-159">Input</span></span> | <span data-ttu-id="0d5b8-160">4</span><span class="sxs-lookup"><span data-stu-id="0d5b8-160">4</span></span> | <span data-ttu-id="0d5b8-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="0d5b8-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="0d5b8-162">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="0d5b8-162">SequenceLengthsTensor</span></span> | <span data-ttu-id="0d5b8-163">Entrée</span><span class="sxs-lookup"><span data-stu-id="0d5b8-163">Input</span></span> | <span data-ttu-id="0d5b8-164">4</span><span class="sxs-lookup"><span data-stu-id="0d5b8-164">4</span></span> | <span data-ttu-id="0d5b8-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="0d5b8-165">UINT32</span></span> |
| <span data-ttu-id="0d5b8-166">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="0d5b8-166">OutputTensor</span></span> | <span data-ttu-id="0d5b8-167">Output</span><span class="sxs-lookup"><span data-stu-id="0d5b8-167">Output</span></span> | <span data-ttu-id="0d5b8-168">4</span><span class="sxs-lookup"><span data-stu-id="0d5b8-168">4</span></span> | <span data-ttu-id="0d5b8-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="0d5b8-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="0d5b8-170">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0d5b8-170">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0d5b8-171">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="0d5b8-171">**Header**</span></span> | <span data-ttu-id="0d5b8-172">directml. h</span><span class="sxs-lookup"><span data-stu-id="0d5b8-172">directml.h</span></span> |