---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copie l’ensemble de l’entrée tenseur dans la sortie, puis remplace les index sélectionnés par les valeurs correspondantes de la tenseur mises à jour.
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: 6c987e01862d849c6215a2d25fe957ef0a22e7af
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803975"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="346ba-103">Structure DML_SCATTER_ND_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="346ba-103">DML_SCATTER_ND_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="346ba-104">Copie l’ensemble de l’entrée tenseur dans la sortie, puis remplace les index sélectionnés par les valeurs correspondantes de la tenseur mises à jour.</span><span class="sxs-lookup"><span data-stu-id="346ba-104">Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.</span></span> <span data-ttu-id="346ba-105">Cet opérateur effectue le pseudocode suivant, où « ... » représente une série de coordonnées, avec le comportement exact déterminé par l’axe et la taille des index.</span><span class="sxs-lookup"><span data-stu-id="346ba-105">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices size.</span></span>

```
output = input
output[indices[...]] = updates[...]
```

<span data-ttu-id="346ba-106">Si deux index d’élément de sortie se chevauchent (ce qui n’est pas valide), il n’y a aucune garantie de la dernière écriture qui gagne.</span><span class="sxs-lookup"><span data-stu-id="346ba-106">If two output element indices overlap (which is invalid), there is no guarantee of which last write wins.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="346ba-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="346ba-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="346ba-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="346ba-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="346ba-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="346ba-109">Syntax</span></span>
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="346ba-110">Membres</span><span class="sxs-lookup"><span data-stu-id="346ba-110">Members</span></span>

`InputTensor`

<span data-ttu-id="346ba-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="346ba-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="346ba-112">Tenseur à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="346ba-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="346ba-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="346ba-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="346ba-114">Tenseur contenant les index.</span><span class="sxs-lookup"><span data-stu-id="346ba-114">A tensor containing the indices.</span></span> <span data-ttu-id="346ba-115">Le *DimensionCount* de ce tenseur doit correspondre à *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="346ba-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="346ba-116">La dernière dimension du *IndicesTensor* est en fait le nombre de coordonnées par tuple d’index et ne doit pas dépasse *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="346ba-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it mustn't exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="346ba-117">Par exemple, un tenseur index de taille `{1,4,5,2}` avec *IndicesDimensionCount* = 3 signifie un tableau à de tuples de coordonnée à 2 valeurs qui sont indexés dans *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="346ba-117">For example, an indices tensor of size `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-value coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="346ba-118">À compter de `DML_FEATURE_LEVEL_3_0` , cet opérateur prend en charge les valeurs d’index négatives lors de l’utilisation d’un type intégral signé avec ce tenseur.</span><span class="sxs-lookup"><span data-stu-id="346ba-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="346ba-119">Les indices négatifs sont interprétés comme étant relatifs à la fin de la dimension respective.</span><span class="sxs-lookup"><span data-stu-id="346ba-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="346ba-120">Par exemple, un index de-1 fait référence au dernier élément de cette dimension.</span><span class="sxs-lookup"><span data-stu-id="346ba-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`UpdatesTensor`

<span data-ttu-id="346ba-121">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="346ba-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="346ba-122">Tenseur contenant les nouvelles valeurs pour remplacer les valeurs d’entrée existantes aux index correspondants.</span><span class="sxs-lookup"><span data-stu-id="346ba-122">A tensor containing the new values to replace the existing input values at the corresponding indices.</span></span> <span data-ttu-id="346ba-123">Le *DimensionCount* de ce tenseur doit correspondre à *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="346ba-123">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="346ba-124">Les *UpdatesTensor. Sizes* attendues sont la concaténation des segments de début *IndicesTensor. Sizes* et *InputTensor. Sizes* pour produire les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="346ba-124">The expected *UpdatesTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

<span data-ttu-id="346ba-125">Les dimensions sont alignées à droite, avec 1 valeur ajoutée au début si nécessaire pour satisfaire *UpdatesTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="346ba-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *UpdatesTensor.DimensionCount*.</span></span>

<span data-ttu-id="346ba-126">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="346ba-126">Here's an example.</span></span>

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

<span data-ttu-id="346ba-127">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="346ba-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="346ba-128">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="346ba-128">The tensor to write the results to.</span></span> <span data-ttu-id="346ba-129">Les *tailles* et le *type de données* de ce tenseur doivent correspondre à *InputTensor. Sizes*.</span><span class="sxs-lookup"><span data-stu-id="346ba-129">The *Sizes* and *DataType* of this tensor must match *InputTensor.Sizes*.</span></span>


`InputDimensionCount`

<span data-ttu-id="346ba-130">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="346ba-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="346ba-131">Nombre de dimensions d’entrée réelles dans le *InputTensor* après avoir ignoré les éléments de début non significatifs, à partir de [1, *InputTensor. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="346ba-131">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging [1, *InputTensor.DimensionCount*).</span></span> <span data-ttu-id="346ba-132">Par exemple, si vous fournissez *InputTensor. Sizes* = {1,1,4,6} et *InputDimensionCount* = 3, les index significatifs réels sont {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="346ba-132">For example, given *InputTensor.Sizes* = {1,1,4,6} and *InputDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="346ba-133">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="346ba-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="346ba-134">Nombre de dimensions d’index réelles dans le *IndicesTensor* après avoir ignoré les éléments de début non significatifs, à partir de [1, *IndicesTensor. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="346ba-134">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="346ba-135">Par exemple, si vous fournissez *IndicesTensor. Sizes* = {1,1,4,6} et *IndicesDimensionCount* = 3, les index significatifs réels sont {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="346ba-135">For example, given *IndicesTensor.Sizes* = {1,1,4,6} and *IndicesDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>

## <a name="examples"></a><span data-ttu-id="346ba-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="346ba-136">Examples</span></span>

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a><span data-ttu-id="346ba-137">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="346ba-137">Availability</span></span>
<span data-ttu-id="346ba-138">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="346ba-138">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="346ba-139">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="346ba-139">Tensor constraints</span></span>
* <span data-ttu-id="346ba-140">*IndicesTensor*, *InputTensor*, *OutputTensor* et `UpdatesTensor` doivent avoir le même *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="346ba-140">*IndicesTensor*, *InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="346ba-141">*InputTensor*, *OutputTensor* et `UpdatesTensor` doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="346ba-141">*InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="346ba-142">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="346ba-142">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="346ba-143">DML_FEATURE_LEVEL_3_0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="346ba-143">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="346ba-144">Tenseur</span><span class="sxs-lookup"><span data-stu-id="346ba-144">Tensor</span></span> | <span data-ttu-id="346ba-145">Type</span><span class="sxs-lookup"><span data-stu-id="346ba-145">Kind</span></span> | <span data-ttu-id="346ba-146">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="346ba-146">Supported dimension counts</span></span> | <span data-ttu-id="346ba-147">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="346ba-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="346ba-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="346ba-148">InputTensor</span></span> | <span data-ttu-id="346ba-149">Entrée</span><span class="sxs-lookup"><span data-stu-id="346ba-149">Input</span></span> | <span data-ttu-id="346ba-150">1 à 8</span><span class="sxs-lookup"><span data-stu-id="346ba-150">1 to 8</span></span> | <span data-ttu-id="346ba-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="346ba-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="346ba-152">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="346ba-152">IndicesTensor</span></span> | <span data-ttu-id="346ba-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="346ba-153">Input</span></span> | <span data-ttu-id="346ba-154">1 à 8</span><span class="sxs-lookup"><span data-stu-id="346ba-154">1 to 8</span></span> | <span data-ttu-id="346ba-155">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="346ba-155">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="346ba-156">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="346ba-156">UpdatesTensor</span></span> | <span data-ttu-id="346ba-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="346ba-157">Input</span></span> | <span data-ttu-id="346ba-158">1 à 8</span><span class="sxs-lookup"><span data-stu-id="346ba-158">1 to 8</span></span> | <span data-ttu-id="346ba-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="346ba-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="346ba-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="346ba-160">OutputTensor</span></span> | <span data-ttu-id="346ba-161">Output</span><span class="sxs-lookup"><span data-stu-id="346ba-161">Output</span></span> | <span data-ttu-id="346ba-162">1 à 8</span><span class="sxs-lookup"><span data-stu-id="346ba-162">1 to 8</span></span> | <span data-ttu-id="346ba-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="346ba-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="346ba-164">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="346ba-164">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="346ba-165">Tenseur</span><span class="sxs-lookup"><span data-stu-id="346ba-165">Tensor</span></span> | <span data-ttu-id="346ba-166">Type</span><span class="sxs-lookup"><span data-stu-id="346ba-166">Kind</span></span> | <span data-ttu-id="346ba-167">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="346ba-167">Supported dimension counts</span></span> | <span data-ttu-id="346ba-168">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="346ba-168">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="346ba-169">InputTensor</span><span class="sxs-lookup"><span data-stu-id="346ba-169">InputTensor</span></span> | <span data-ttu-id="346ba-170">Entrée</span><span class="sxs-lookup"><span data-stu-id="346ba-170">Input</span></span> | <span data-ttu-id="346ba-171">4</span><span class="sxs-lookup"><span data-stu-id="346ba-171">4</span></span> | <span data-ttu-id="346ba-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="346ba-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="346ba-173">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="346ba-173">IndicesTensor</span></span> | <span data-ttu-id="346ba-174">Entrée</span><span class="sxs-lookup"><span data-stu-id="346ba-174">Input</span></span> | <span data-ttu-id="346ba-175">4</span><span class="sxs-lookup"><span data-stu-id="346ba-175">4</span></span> | <span data-ttu-id="346ba-176">UINT32</span><span class="sxs-lookup"><span data-stu-id="346ba-176">UINT32</span></span> |
| <span data-ttu-id="346ba-177">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="346ba-177">UpdatesTensor</span></span> | <span data-ttu-id="346ba-178">Entrée</span><span class="sxs-lookup"><span data-stu-id="346ba-178">Input</span></span> | <span data-ttu-id="346ba-179">4</span><span class="sxs-lookup"><span data-stu-id="346ba-179">4</span></span> | <span data-ttu-id="346ba-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="346ba-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="346ba-181">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="346ba-181">OutputTensor</span></span> | <span data-ttu-id="346ba-182">Output</span><span class="sxs-lookup"><span data-stu-id="346ba-182">Output</span></span> | <span data-ttu-id="346ba-183">4</span><span class="sxs-lookup"><span data-stu-id="346ba-183">4</span></span> | <span data-ttu-id="346ba-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="346ba-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="346ba-185">Spécifications</span><span class="sxs-lookup"><span data-stu-id="346ba-185">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="346ba-186">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="346ba-186">**Header**</span></span> | <span data-ttu-id="346ba-187">directml. h</span><span class="sxs-lookup"><span data-stu-id="346ba-187">directml.h</span></span> |