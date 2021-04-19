---
UID: NS:directml.DML_GATHER_ELEMENTS_OPERATOR_DESC
title: DML_GATHER_ELEMENTS_OPERATOR_DESC
description: Recueille des éléments à partir du tenseur d’entrée le long de l’axe donné en utilisant les index tenseur pour remapper dans l’entrée.
helpviewer_keywords:
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- DML_GATHER_ELEMENTS_OPERATOR_DESC structure
- direct3d12.dml_gather_elements_operator_desc
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.openlocfilehash: 19a3f19a19d0287dfcbff8b312b1d245fcfe6c09
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106537152"
---
# <a name="dml_gather_elements_operator_desc-structure-directmlh"></a><span data-ttu-id="8cf76-103">Structure DML_GATHER_ELEMENTS_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="8cf76-103">DML_GATHER_ELEMENTS_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="8cf76-104">Recueille des éléments à partir du tenseur d’entrée le long de l’axe donné en utilisant les index tenseur pour remapper dans l’entrée.</span><span class="sxs-lookup"><span data-stu-id="8cf76-104">Gathers elements from the input tensor along the given axis using the indices tensor to remap into the input.</span></span> <span data-ttu-id="8cf76-105">Cet opérateur effectue le pseudo-code suivant, avec le comportement exact qui dépend de l’axe, du nombre de dimensions d’entrée et du nombre de dimensions d’index.</span><span class="sxs-lookup"><span data-stu-id="8cf76-105">This operator performs the following pseudocode, with the exact behavior dependent on the axis, input dimension count, and indices dimension count.</span></span>

```
output[i, j, k, ...] = input[index[i, j, k, ...], j, k, ...] // if axis == 0
output[i, j, k, ...] = input[i, index[i, j, k, ...], k, ...] // if axis == 1
output[i, j, k, ...] = input[i, j, index[i, j, k, ...], ...] // if axis == 2
...
```

> [!IMPORTANT]
> <span data-ttu-id="8cf76-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="8cf76-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="8cf76-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="8cf76-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf76-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cf76-108">Syntax</span></span>
```cpp
struct DML_GATHER_ELEMENTS_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="8cf76-109">Membres</span><span class="sxs-lookup"><span data-stu-id="8cf76-109">Members</span></span>

`InputTensor`

<span data-ttu-id="8cf76-110">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8cf76-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8cf76-111">Tenseur à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="8cf76-111">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="8cf76-112">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8cf76-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8cf76-113">Index dans le tenseur d’entrée le long de l’axe actif.</span><span class="sxs-lookup"><span data-stu-id="8cf76-113">The indices into the input tensor along the active axis.</span></span> <span data-ttu-id="8cf76-114">Les *tailles* doivent correspondre à *InputTensor. Sizes* pour chaque dimension, à l’exception de *Axis*.</span><span class="sxs-lookup"><span data-stu-id="8cf76-114">The *Sizes* must match *InputTensor.Sizes* for every dimension except *Axis*.</span></span>

<span data-ttu-id="8cf76-115">À compter de `DML_FEATURE_LEVEL_3_0` , cet opérateur prend en charge les valeurs d’index négatives lors de l’utilisation d’un type intégral signé avec ce tenseur.</span><span class="sxs-lookup"><span data-stu-id="8cf76-115">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="8cf76-116">Les indices négatifs sont interprétés comme étant relatifs à la fin de la dimension de l’axe.</span><span class="sxs-lookup"><span data-stu-id="8cf76-116">Negative indices are interpreted as being relative to the end of the axis dimension.</span></span> <span data-ttu-id="8cf76-117">Par exemple, un index de-1 fait référence au dernier élément de cette dimension.</span><span class="sxs-lookup"><span data-stu-id="8cf76-117">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="8cf76-118">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8cf76-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8cf76-119">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="8cf76-119">The tensor to write the results to.</span></span> <span data-ttu-id="8cf76-120">Les *tailles* doivent correspondre à *IndicesTensor. Sizes*, et *DataType* doit correspondre à *InputTensor. DataType*.</span><span class="sxs-lookup"><span data-stu-id="8cf76-120">The *Sizes* must match *IndicesTensor.Sizes*, and *DataType* must match *InputTensor.DataType*.</span></span>


`Axis`

<span data-ttu-id="8cf76-121">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8cf76-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="8cf76-122">Dimension d’axe des *InputTensor* à rassembler, à savoir `[0, *InputTensor.DimensionCount*)` .</span><span class="sxs-lookup"><span data-stu-id="8cf76-122">The axis dimension of *InputTensor* to gather along, ranging `[0, *InputTensor.DimensionCount*)`.</span></span>

## <a name="examples"></a><span data-ttu-id="8cf76-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="8cf76-123">Examples</span></span>

```
Axis = 0

InputTensor: (Sizes:{3,3}, DataType:FLOAT32)
    [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]

IndicesTensor: (Sizes:{2,3}, DataType:UINT32)
    [[1, 2, 0],
     [2, 0, 0]]

// output[y, x] = input[indices[y, x], x]
OutputTensor: (Sizes:{2,3}, DataType:UINT32)
    [[4, 8, 3], // select elements vertically from data
     [7, 2, 3]]
```

## <a name="availability"></a><span data-ttu-id="8cf76-124">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="8cf76-124">Availability</span></span>
<span data-ttu-id="8cf76-125">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="8cf76-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8cf76-126">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="8cf76-126">Tensor constraints</span></span>
* <span data-ttu-id="8cf76-127">`IndicesTensor`, *InputTensor* et *OutputTensor* doivent avoir le même *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="8cf76-127">`IndicesTensor`, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="8cf76-128">*InputTensor* et *OutputTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="8cf76-128">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8cf76-129">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="8cf76-129">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="8cf76-130">DML_FEATURE_LEVEL_3_0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="8cf76-130">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="8cf76-131">Tenseur</span><span class="sxs-lookup"><span data-stu-id="8cf76-131">Tensor</span></span> | <span data-ttu-id="8cf76-132">Type</span><span class="sxs-lookup"><span data-stu-id="8cf76-132">Kind</span></span> | <span data-ttu-id="8cf76-133">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="8cf76-133">Supported dimension counts</span></span> | <span data-ttu-id="8cf76-134">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cf76-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8cf76-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8cf76-135">InputTensor</span></span> | <span data-ttu-id="8cf76-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="8cf76-136">Input</span></span> | <span data-ttu-id="8cf76-137">1 à 8</span><span class="sxs-lookup"><span data-stu-id="8cf76-137">1 to 8</span></span> | <span data-ttu-id="8cf76-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8cf76-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8cf76-139">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="8cf76-139">IndicesTensor</span></span> | <span data-ttu-id="8cf76-140">Entrée</span><span class="sxs-lookup"><span data-stu-id="8cf76-140">Input</span></span> | <span data-ttu-id="8cf76-141">1 à 8</span><span class="sxs-lookup"><span data-stu-id="8cf76-141">1 to 8</span></span> | <span data-ttu-id="8cf76-142">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="8cf76-142">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="8cf76-143">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8cf76-143">OutputTensor</span></span> | <span data-ttu-id="8cf76-144">Output</span><span class="sxs-lookup"><span data-stu-id="8cf76-144">Output</span></span> | <span data-ttu-id="8cf76-145">1 à 8</span><span class="sxs-lookup"><span data-stu-id="8cf76-145">1 to 8</span></span> | <span data-ttu-id="8cf76-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8cf76-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="8cf76-147">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="8cf76-147">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="8cf76-148">Tenseur</span><span class="sxs-lookup"><span data-stu-id="8cf76-148">Tensor</span></span> | <span data-ttu-id="8cf76-149">Type</span><span class="sxs-lookup"><span data-stu-id="8cf76-149">Kind</span></span> | <span data-ttu-id="8cf76-150">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="8cf76-150">Supported dimension counts</span></span> | <span data-ttu-id="8cf76-151">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cf76-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8cf76-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8cf76-152">InputTensor</span></span> | <span data-ttu-id="8cf76-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="8cf76-153">Input</span></span> | <span data-ttu-id="8cf76-154">4</span><span class="sxs-lookup"><span data-stu-id="8cf76-154">4</span></span> | <span data-ttu-id="8cf76-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8cf76-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8cf76-156">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="8cf76-156">IndicesTensor</span></span> | <span data-ttu-id="8cf76-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="8cf76-157">Input</span></span> | <span data-ttu-id="8cf76-158">4</span><span class="sxs-lookup"><span data-stu-id="8cf76-158">4</span></span> | <span data-ttu-id="8cf76-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="8cf76-159">UINT32</span></span> |
| <span data-ttu-id="8cf76-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8cf76-160">OutputTensor</span></span> | <span data-ttu-id="8cf76-161">Output</span><span class="sxs-lookup"><span data-stu-id="8cf76-161">Output</span></span> | <span data-ttu-id="8cf76-162">4</span><span class="sxs-lookup"><span data-stu-id="8cf76-162">4</span></span> | <span data-ttu-id="8cf76-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8cf76-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="8cf76-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cf76-164">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8cf76-165">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="8cf76-165">**Header**</span></span> | <span data-ttu-id="8cf76-166">directml. h</span><span class="sxs-lookup"><span data-stu-id="8cf76-166">directml.h</span></span> |