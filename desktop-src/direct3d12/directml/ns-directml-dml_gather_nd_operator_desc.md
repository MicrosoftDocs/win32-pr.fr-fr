---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Recueille des éléments à partir du tenseur d’entrée, en utilisant les index tenseur pour remapper les index à des sous-blocs complets de l’entrée. | DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 6a48fd19621bed100a13412dbb1992974d125323
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538303"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="8c4e4-104">Structure DML_GATHER_ND_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="8c4e4-104">DML_GATHER_ND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="8c4e4-105">Recueille des éléments à partir du tenseur d’entrée, en utilisant les index tenseur pour remapper les index à des sous-blocs complets de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="8c4e4-106">Cet opérateur effectue le pseudocode suivant, où « ... » représente une série de coordonnées, avec le comportement exact qui dépend du nombre de dimensions d’entrée et d’index.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the input and indices dimension count.</span></span>

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> <span data-ttu-id="8c4e4-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="8c4e4-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="8c4e4-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="8c4e4-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4e4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c4e4-109">Syntax</span></span>
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="8c4e4-110">Membres</span><span class="sxs-lookup"><span data-stu-id="8c4e4-110">Members</span></span>

`InputTensor`

<span data-ttu-id="8c4e4-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8c4e4-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8c4e4-112">Tenseur à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="8c4e4-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8c4e4-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8c4e4-114">Tenseur contenant les index.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-114">The tensor containing the indices.</span></span> <span data-ttu-id="8c4e4-115">Le *DimensionCount* de ce tenseur doit correspondre à *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="8c4e4-116">La dernière dimension du *IndicesTensor* est en fait le nombre de coordonnées par tuple d’index et ne peut pas dépasser *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="8c4e4-117">Par exemple, un tenseur d’index de *tailles* `{1,4,5,2}` avec *IndicesDimensionCount* = 3 représente un tableau à de tuples à 2 coordonnées qui sont indexés dans *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="8c4e4-118">À compter de `DML_FEATURE_LEVEL_3_0` , cet opérateur prend en charge les valeurs d’index négatives lors de l’utilisation d’un type intégral signé avec ce tenseur.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="8c4e4-119">Les indices négatifs sont interprétés comme étant relatifs à la fin de la dimension respective.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="8c4e4-120">Par exemple, un index de-1 fait référence au dernier élément de cette dimension.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="8c4e4-121">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8c4e4-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8c4e4-122">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-122">The tensor to write the results to.</span></span> <span data-ttu-id="8c4e4-123">Le *DimensionCount* et le *type de données* de ce tenseur doivent correspondre à *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="8c4e4-124">Les *OutputTensor. Sizes* attendues sont la concaténation des segments de début *IndicesTensor. Sizes* et *InputTensor. Sizes* segment de fin à yield :</span><span class="sxs-lookup"><span data-stu-id="8c4e4-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield:</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="8c4e4-125">Les dimensions de sortie sont alignées à droite, avec les valeurs les plus grandes ajoutées si nécessaire pour répondre à *OutputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-125">The output dimensions are right-aligned, with leading 1 values prepended if needed to satisfy up to *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="8c4e4-126">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-126">Here's an example.</span></span>

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```


`InputDimensionCount`

<span data-ttu-id="8c4e4-127">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8c4e4-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="8c4e4-128">Nombre de dimensions d’entrée réelles dans le *InputTensor* après avoir ignoré les éléments de début non significatifs, à partir de `[1, *InputTensor.DimensionCount*]` .</span><span class="sxs-lookup"><span data-stu-id="8c4e4-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="8c4e4-129">Par exemple, étant donné *InputTensor. Sizes*  =  `{1,1,4,6}` et `InputDimensionCount` = 3, les index significatifs réels sont `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="8c4e4-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="8c4e4-130">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8c4e4-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="8c4e4-131">Nombre de dimensions d’index réelles dans le *IndicesTensor* après avoir ignoré les éléments de début non significatifs, à partir de [1, *IndicesTensor. DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="8c4e4-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="8c4e4-132">Par exemple, étant donné *IndicesTensor. Sizes*  =  `{1,1,4,6}` et *IndicesDimensionCount* = 3, les index significatifs réels sont `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="8c4e4-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

## <a name="examples"></a><span data-ttu-id="8c4e4-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="8c4e4-133">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="8c4e4-134">Exemple 1.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-134">Example 1.</span></span> <span data-ttu-id="8c4e4-135">remappage 1D</span><span class="sxs-lookup"><span data-stu-id="8c4e4-135">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a><span data-ttu-id="8c4e4-136">Exemple 2.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-136">Example 2.</span></span> <span data-ttu-id="8c4e4-137">remappage 2D</span><span class="sxs-lookup"><span data-stu-id="8c4e4-137">2D remapping</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a><span data-ttu-id="8c4e4-138">Notes</span><span class="sxs-lookup"><span data-stu-id="8c4e4-138">Remarks</span></span>
<span data-ttu-id="8c4e4-139">Une version plus récente de cet opérateur, `DML_OPERATOR_GATHER_ND1` , a été introduite dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="8c4e4-139">A newer version of this operator, `DML_OPERATOR_GATHER_ND1`, was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="availability"></a><span data-ttu-id="8c4e4-140">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="8c4e4-140">Availability</span></span>
<span data-ttu-id="8c4e4-141">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="8c4e4-141">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8c4e4-142">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="8c4e4-142">Tensor constraints</span></span>
* <span data-ttu-id="8c4e4-143">*IndicesTensor*, *InputTensor* et *OutputTensor* doivent avoir le même *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-143">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="8c4e4-144">*InputTensor* et *OutputTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="8c4e4-144">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8c4e4-145">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="8c4e4-145">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="8c4e4-146">DML_FEATURE_LEVEL_3_0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="8c4e4-146">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="8c4e4-147">Tenseur</span><span class="sxs-lookup"><span data-stu-id="8c4e4-147">Tensor</span></span> | <span data-ttu-id="8c4e4-148">Type</span><span class="sxs-lookup"><span data-stu-id="8c4e4-148">Kind</span></span> | <span data-ttu-id="8c4e4-149">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="8c4e4-149">Supported dimension counts</span></span> | <span data-ttu-id="8c4e4-150">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c4e4-150">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8c4e4-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8c4e4-151">InputTensor</span></span> | <span data-ttu-id="8c4e4-152">Entrée</span><span class="sxs-lookup"><span data-stu-id="8c4e4-152">Input</span></span> | <span data-ttu-id="8c4e4-153">1 à 8</span><span class="sxs-lookup"><span data-stu-id="8c4e4-153">1 to 8</span></span> | <span data-ttu-id="8c4e4-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8c4e4-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8c4e4-155">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="8c4e4-155">IndicesTensor</span></span> | <span data-ttu-id="8c4e4-156">Entrée</span><span class="sxs-lookup"><span data-stu-id="8c4e4-156">Input</span></span> | <span data-ttu-id="8c4e4-157">1 à 8</span><span class="sxs-lookup"><span data-stu-id="8c4e4-157">1 to 8</span></span> | <span data-ttu-id="8c4e4-158">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="8c4e4-158">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="8c4e4-159">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8c4e4-159">OutputTensor</span></span> | <span data-ttu-id="8c4e4-160">Output</span><span class="sxs-lookup"><span data-stu-id="8c4e4-160">Output</span></span> | <span data-ttu-id="8c4e4-161">1 à 8</span><span class="sxs-lookup"><span data-stu-id="8c4e4-161">1 to 8</span></span> | <span data-ttu-id="8c4e4-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8c4e4-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="8c4e4-163">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="8c4e4-163">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="8c4e4-164">Tenseur</span><span class="sxs-lookup"><span data-stu-id="8c4e4-164">Tensor</span></span> | <span data-ttu-id="8c4e4-165">Type</span><span class="sxs-lookup"><span data-stu-id="8c4e4-165">Kind</span></span> | <span data-ttu-id="8c4e4-166">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="8c4e4-166">Supported dimension counts</span></span> | <span data-ttu-id="8c4e4-167">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c4e4-167">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8c4e4-168">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8c4e4-168">InputTensor</span></span> | <span data-ttu-id="8c4e4-169">Entrée</span><span class="sxs-lookup"><span data-stu-id="8c4e4-169">Input</span></span> | <span data-ttu-id="8c4e4-170">4</span><span class="sxs-lookup"><span data-stu-id="8c4e4-170">4</span></span> | <span data-ttu-id="8c4e4-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8c4e4-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8c4e4-172">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="8c4e4-172">IndicesTensor</span></span> | <span data-ttu-id="8c4e4-173">Entrée</span><span class="sxs-lookup"><span data-stu-id="8c4e4-173">Input</span></span> | <span data-ttu-id="8c4e4-174">4</span><span class="sxs-lookup"><span data-stu-id="8c4e4-174">4</span></span> | <span data-ttu-id="8c4e4-175">UINT32</span><span class="sxs-lookup"><span data-stu-id="8c4e4-175">UINT32</span></span> |
| <span data-ttu-id="8c4e4-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8c4e4-176">OutputTensor</span></span> | <span data-ttu-id="8c4e4-177">Output</span><span class="sxs-lookup"><span data-stu-id="8c4e4-177">Output</span></span> | <span data-ttu-id="8c4e4-178">4</span><span class="sxs-lookup"><span data-stu-id="8c4e4-178">4</span></span> | <span data-ttu-id="8c4e4-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8c4e4-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="8c4e4-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c4e4-180">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8c4e4-181">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="8c4e4-181">**Header**</span></span> | <span data-ttu-id="8c4e4-182">directml. h</span><span class="sxs-lookup"><span data-stu-id="8c4e4-182">directml.h</span></span> |
