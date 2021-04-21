---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Sélectionne les éléments *K* les plus grands ou les plus petits de chaque séquence le long d’un axe du *InputTensor*, puis retourne les valeurs et les index de ces éléments dans *OutputValueTensor* et *OutputIndexTensor*, respectivement.
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 599541032e0f1711c0e747a4ca5906391849a932
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803815"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a><span data-ttu-id="c3bf2-103">Structure DML_TOP_K1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="c3bf2-103">DML_TOP_K1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="c3bf2-104">Sélectionne les éléments *K* les plus grands ou les plus petits de chaque séquence le long d’un axe du *InputTensor*, puis retourne les valeurs et les index de ces éléments dans *OutputValueTensor* et *OutputIndexTensor*, respectivement.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-104">Selects the largest or smallest *K* elements from each sequence along an axis of the *InputTensor*, and returns the values and indices of those elements in the *OutputValueTensor* and *OutputIndexTensor*, respectively.</span></span> <span data-ttu-id="c3bf2-105">Une *séquence* fait référence à l’un des ensembles d’éléments qui existent le long de la dimension d' *axe* du *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-105">A *sequence* refers to one of the sets of elements that exist along the *Axis* dimension of the *InputTensor*.</span></span>

<span data-ttu-id="c3bf2-106">Le choix de sélectionner les éléments les plus importants ou les plus petits éléments K peut être contrôlé à l’aide de *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-106">The choice of whether to select the largest K elements or the smallest K elements can be controlled using *AxisDirection*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3bf2-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="c3bf2-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c3bf2-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c3bf2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3bf2-109">Syntax</span></span>
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="c3bf2-110">Membres</span><span class="sxs-lookup"><span data-stu-id="c3bf2-110">Members</span></span>

`InputTensor`

<span data-ttu-id="c3bf2-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c3bf2-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c3bf2-112">Tenseur d’entrée contenant les éléments à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-112">The input tensor containing elements to select.</span></span>

`OutputValueTensor`

<span data-ttu-id="c3bf2-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c3bf2-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c3bf2-114">Tenseur de sortie dans lequel écrire les valeurs des premiers éléments *K* .</span><span class="sxs-lookup"><span data-stu-id="c3bf2-114">The output tensor to write the values of the top *K* elements to.</span></span> <span data-ttu-id="c3bf2-115">Les *K* premiers éléments sont sélectionnés selon qu’ils sont le plus grand ou le plus petit, en fonction de la valeur de *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-115">The top *K* elements are selected based on whether they are the largest or the smallest, depending on the value of *AxisDirection*.</span></span> <span data-ttu-id="c3bf2-116">Ce tenseur doit avoir des tailles égales à *InputTensor*, *à l’exception* de la dimension spécifiée par le paramètre *Axis* , qui doit avoir une taille égale à *K*.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-116">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="c3bf2-117">Les valeurs *K* sélectionnées à partir de chaque séquence d’entrée sont systématiquement triées par ordre décroissant (du plus grand au plus petit) si *AxisDirection* est [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span><span class="sxs-lookup"><span data-stu-id="c3bf2-117">The *K* values selected from each input sequence are guaranteed to be sorted descending (largest to smallest) if *AxisDirection* is [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span></span> <span data-ttu-id="c3bf2-118">Dans le cas contraire, l’inverse est vrai et les valeurs sélectionnées sont systématiquement triées par ordre croissant (du plus petit au plus grand).</span><span class="sxs-lookup"><span data-stu-id="c3bf2-118">Otherwise, the opposite is true and the values selected are guaranteed to be sorted ascending (smallest to largest).</span></span>

`OutputIndexTensor`

<span data-ttu-id="c3bf2-119">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c3bf2-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c3bf2-120">Tenseur de sortie dans lequel écrire les index des premiers éléments *K* .</span><span class="sxs-lookup"><span data-stu-id="c3bf2-120">The output tensor to write the indices of the top *K* elements to.</span></span> <span data-ttu-id="c3bf2-121">Ce tenseur doit avoir des tailles égales à *InputTensor*, *à l’exception* de la dimension spécifiée par le paramètre *Axis* , qui doit avoir une taille égale à *K*.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-121">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="c3bf2-122">Les index retournés dans ce tenseur sont mesurés par rapport au début de leur séquence (par opposition au début du tenseur).</span><span class="sxs-lookup"><span data-stu-id="c3bf2-122">The indices returned in this tensor are measured relative to the beginning of their sequence (as opposed to the beginning of the tensor).</span></span> <span data-ttu-id="c3bf2-123">Par exemple, un index de 0 fait toujours référence au premier élément pour toutes les séquences d’un axe.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-123">For example, an index of 0 always refers to the first element for all sequences in an axis.</span></span>

<span data-ttu-id="c3bf2-124">Dans les cas où deux ou plusieurs éléments de la clause TOP-K ont la même valeur (autrement dit, en cas d’égalité), les index des deux éléments sont inclus et sont assurés d’être classés par ordre croissant des index des éléments.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-124">In cases where two or more elements in the top-K have the same value (that is, when there is a tie), the indices of both elements are included, and are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="c3bf2-125">Notez que cela est vrai, quelle que soit la valeur de *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-125">Note that this is true irrespective of the value of *AxisDirection*.</span></span>

`Axis`

<span data-ttu-id="c3bf2-126">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c3bf2-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c3bf2-127">Index de la dimension dans laquelle sélectionner les éléments.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-127">The index of the dimension to select elements across.</span></span> <span data-ttu-id="c3bf2-128">Cette valeur doit être inférieure à la *DimensionCount* du *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-128">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`K`

<span data-ttu-id="c3bf2-129">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="c3bf2-129">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="c3bf2-130">Nombre d’éléments à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-130">The number of elements to select.</span></span> <span data-ttu-id="c3bf2-131">*K* doit être supérieur à 0, mais inférieur au nombre d’éléments dans *InputTensor* le long de la dimension spécifiée par *Axis*.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-131">*K* must be greater than 0, but less than the number of elements in the *InputTensor* along the dimension specified by *Axis*.</span></span>

`AxisDirection`

<span data-ttu-id="c3bf2-132">Type : **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="c3bf2-132">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="c3bf2-133">Valeur de l’énumération [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="c3bf2-133">A value from the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="c3bf2-134">Si la valeur est **DML_AXIS_DIRECTION_INCREASING**, cet opérateur retourne les *plus petits* éléments *K* par ordre de valeur d’incrément.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-134">If set to **DML_AXIS_DIRECTION_INCREASING**, then this operator returns the *smallest* *K* elements in order of increasing value.</span></span> <span data-ttu-id="c3bf2-135">Dans le cas contraire, elle retourne les éléments *K* les *plus importants* dans l’ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-135">Otherwise, it returns the *largest* *K* elements in decreasing order.</span></span>

## <a name="examples"></a><span data-ttu-id="c3bf2-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="c3bf2-136">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="c3bf2-137">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="c3bf2-137">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a><span data-ttu-id="c3bf2-138">Exemple 2.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-138">Example 2.</span></span> <span data-ttu-id="c3bf2-139">Utilisation d’un autre axe</span><span class="sxs-lookup"><span data-stu-id="c3bf2-139">Using a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a><span data-ttu-id="c3bf2-140">Exemple 3.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-140">Example 3.</span></span> <span data-ttu-id="c3bf2-141">Valeurs liées</span><span class="sxs-lookup"><span data-stu-id="c3bf2-141">Tied values</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a><span data-ttu-id="c3bf2-142">Exemple 4 :</span><span class="sxs-lookup"><span data-stu-id="c3bf2-142">Example 4.</span></span> <span data-ttu-id="c3bf2-143">Incrémentation de la direction de l’axe</span><span class="sxs-lookup"><span data-stu-id="c3bf2-143">Increasing axis direction</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a><span data-ttu-id="c3bf2-144">Notes </span><span class="sxs-lookup"><span data-stu-id="c3bf2-144">Remarks</span></span>
<span data-ttu-id="c3bf2-145">Quand *AxisDirection* a la valeur [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), cet opérateur équivaut à [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="c3bf2-145">When *AxisDirection* is set to [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), this operator is equivalent to [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="c3bf2-146">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="c3bf2-146">Availability</span></span>
<span data-ttu-id="c3bf2-147">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="c3bf2-147">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c3bf2-148">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="c3bf2-148">Tensor constraints</span></span>

* <span data-ttu-id="c3bf2-149">*InputTensor*, *OutputIndexTensor* et *OutputValueTensor* doivent avoir le même *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-149">*InputTensor*, *OutputIndexTensor*, and *OutputValueTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="c3bf2-150">*InputTensor* et *OutputValueTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="c3bf2-150">*InputTensor* and *OutputValueTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c3bf2-151">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="c3bf2-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="c3bf2-152">DML_FEATURE_LEVEL_3_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="c3bf2-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="c3bf2-153">Tenseur</span><span class="sxs-lookup"><span data-stu-id="c3bf2-153">Tensor</span></span> | <span data-ttu-id="c3bf2-154">Type</span><span class="sxs-lookup"><span data-stu-id="c3bf2-154">Kind</span></span> | <span data-ttu-id="c3bf2-155">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="c3bf2-155">Supported dimension counts</span></span> | <span data-ttu-id="c3bf2-156">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3bf2-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c3bf2-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c3bf2-157">InputTensor</span></span> | <span data-ttu-id="c3bf2-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="c3bf2-158">Input</span></span> | <span data-ttu-id="c3bf2-159">1 à 8</span><span class="sxs-lookup"><span data-stu-id="c3bf2-159">1 to 8</span></span> | <span data-ttu-id="c3bf2-160">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c3bf2-160">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c3bf2-161">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="c3bf2-161">OutputValueTensor</span></span> | <span data-ttu-id="c3bf2-162">Output</span><span class="sxs-lookup"><span data-stu-id="c3bf2-162">Output</span></span> | <span data-ttu-id="c3bf2-163">1 à 8</span><span class="sxs-lookup"><span data-stu-id="c3bf2-163">1 to 8</span></span> | <span data-ttu-id="c3bf2-164">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c3bf2-164">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c3bf2-165">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="c3bf2-165">OutputIndexTensor</span></span> | <span data-ttu-id="c3bf2-166">Output</span><span class="sxs-lookup"><span data-stu-id="c3bf2-166">Output</span></span> | <span data-ttu-id="c3bf2-167">1 à 8</span><span class="sxs-lookup"><span data-stu-id="c3bf2-167">1 to 8</span></span> | <span data-ttu-id="c3bf2-168">UINT32</span><span class="sxs-lookup"><span data-stu-id="c3bf2-168">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="c3bf2-169">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="c3bf2-169">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="c3bf2-170">Tenseur</span><span class="sxs-lookup"><span data-stu-id="c3bf2-170">Tensor</span></span> | <span data-ttu-id="c3bf2-171">Type</span><span class="sxs-lookup"><span data-stu-id="c3bf2-171">Kind</span></span> | <span data-ttu-id="c3bf2-172">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="c3bf2-172">Supported dimension counts</span></span> | <span data-ttu-id="c3bf2-173">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3bf2-173">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c3bf2-174">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c3bf2-174">InputTensor</span></span> | <span data-ttu-id="c3bf2-175">Entrée</span><span class="sxs-lookup"><span data-stu-id="c3bf2-175">Input</span></span> | <span data-ttu-id="c3bf2-176">4</span><span class="sxs-lookup"><span data-stu-id="c3bf2-176">4</span></span> | <span data-ttu-id="c3bf2-177">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c3bf2-177">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c3bf2-178">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="c3bf2-178">OutputValueTensor</span></span> | <span data-ttu-id="c3bf2-179">Output</span><span class="sxs-lookup"><span data-stu-id="c3bf2-179">Output</span></span> | <span data-ttu-id="c3bf2-180">4</span><span class="sxs-lookup"><span data-stu-id="c3bf2-180">4</span></span> | <span data-ttu-id="c3bf2-181">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c3bf2-181">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c3bf2-182">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="c3bf2-182">OutputIndexTensor</span></span> | <span data-ttu-id="c3bf2-183">Output</span><span class="sxs-lookup"><span data-stu-id="c3bf2-183">Output</span></span> | <span data-ttu-id="c3bf2-184">4</span><span class="sxs-lookup"><span data-stu-id="c3bf2-184">4</span></span> | <span data-ttu-id="c3bf2-185">UINT32</span><span class="sxs-lookup"><span data-stu-id="c3bf2-185">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="c3bf2-186">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c3bf2-186">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c3bf2-187">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="c3bf2-187">**Header**</span></span> | <span data-ttu-id="c3bf2-188">directml. h</span><span class="sxs-lookup"><span data-stu-id="c3bf2-188">directml.h</span></span> |
