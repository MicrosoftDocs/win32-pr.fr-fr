---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Génère les index des éléments de valeur maximale dans une ou plusieurs dimensions du tenseur d’entrée.
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 4c2852c3d301a12d318c5e3006b26830c6eaa6e1
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550494"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a><span data-ttu-id="e3099-103">Structure DML_ARGMAX_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="e3099-103">DML_ARGMAX_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e3099-104">Génère les index des éléments de valeur maximale dans une ou plusieurs dimensions du tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e3099-104">Outputs the indices of the maximum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="e3099-105">Chaque élément de sortie est le résultat de l’application d’une réduction *argmax* sur un sous-ensemble du tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e3099-105">Each output element is the result of applying an *argmax* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="e3099-106">La fonction *argmax* génère l’index de l’élément de valeur maximale dans un jeu d’éléments d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e3099-106">The *argmax* function outputs the index of the maximum-valued element within a set of input elements.</span></span> <span data-ttu-id="e3099-107">Les éléments d’entrée impliqués dans chaque réduction sont déterminés par les axes d’entrée fournis.</span><span class="sxs-lookup"><span data-stu-id="e3099-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="e3099-108">De même, chaque index de sortie est relatif aux axes d’entrée fournis.</span><span class="sxs-lookup"><span data-stu-id="e3099-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="e3099-109">Si tous les axes d’entrée sont spécifiés, l’opérateur applique une seule réduction *argmax* et produit un seul élément Output.</span><span class="sxs-lookup"><span data-stu-id="e3099-109">If all input axes are specified, then the operator applies a single *argmax* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3099-110">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e3099-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e3099-111">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e3099-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3099-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3099-112">Syntax</span></span>
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="e3099-113">Membres</span><span class="sxs-lookup"><span data-stu-id="e3099-113">Members</span></span>

`InputTensor`

<span data-ttu-id="e3099-114">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e3099-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e3099-115">Tenseur à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="e3099-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="e3099-116">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e3099-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e3099-117">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="e3099-117">The tensor to write the results to.</span></span> <span data-ttu-id="e3099-118">Chaque élément de sortie est le résultat d’une réduction *argmax* sur un sous-ensemble d’éléments du *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="e3099-118">Each output element is the result of an *argmax* reduction on a subset of elements from the *InputTensor*.</span></span> 

- <span data-ttu-id="e3099-119">*DimensionCount* doit correspondre à *InputTensor. DimensionCount* (le rang du tenseur d’entrée est préservé).</span><span class="sxs-lookup"><span data-stu-id="e3099-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="e3099-120">Les *tailles* doivent correspondre à *InputTensor.* sizes, à l’exception des dimensions incluses dans les *axes* réduits, qui doivent être de taille 1.</span><span class="sxs-lookup"><span data-stu-id="e3099-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="e3099-121">Type : **[uint](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3099-121">Type: **[UINT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3099-122">Nombre d’axes à réduire.</span><span class="sxs-lookup"><span data-stu-id="e3099-122">The number of axes to reduce.</span></span> <span data-ttu-id="e3099-123">Ce champ détermine la taille du tableau *axes* .</span><span class="sxs-lookup"><span data-stu-id="e3099-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="e3099-124">Type : \_ Field_size \_ (AxisCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3099-124">Type: \_Field_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e3099-125">Axes avec lesquels réduire.</span><span class="sxs-lookup"><span data-stu-id="e3099-125">The axes along which to reduce.</span></span> <span data-ttu-id="e3099-126">Les valeurs doivent être comprises dans la plage `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="e3099-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="e3099-127">Type : **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="e3099-127">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="e3099-128">Détermine l’index à sélectionner lorsque plusieurs éléments d’entrée ont la même valeur.</span><span class="sxs-lookup"><span data-stu-id="e3099-128">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="e3099-129">**DML_AXIS_DIRECTION_INCREASING** retourne l’index du premier élément à valeur maximale (par exemple, `argmax({3,2,1,2,3}) = 0` )</span><span class="sxs-lookup"><span data-stu-id="e3099-129">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first maximum-valued element (for example, `argmax({3,2,1,2,3}) = 0`)</span></span>
- <span data-ttu-id="e3099-130">**DML_AXIS_DIRECTION_DECREASING** retourne l’index du dernier élément à valeur maximale (par exemple, `argmax({3,2,1,2,3}) = 4` )</span><span class="sxs-lookup"><span data-stu-id="e3099-130">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last maximum-valued element (for example, `argmax({3,2,1,2,3}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="e3099-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="e3099-131">Examples</span></span>

<span data-ttu-id="e3099-132">Les exemples de cette section utilisent tous ce même tenseur d’entrée à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="e3099-132">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a><span data-ttu-id="e3099-133">Exemple 1.</span><span class="sxs-lookup"><span data-stu-id="e3099-133">Example 1.</span></span> <span data-ttu-id="e3099-134">Application de *argmax* à des colonnes</span><span class="sxs-lookup"><span data-stu-id="e3099-134">Applying *argmax* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a><span data-ttu-id="e3099-135">Exemple 2.</span><span class="sxs-lookup"><span data-stu-id="e3099-135">Example 2.</span></span> <span data-ttu-id="e3099-136">Application de *argmax* à des lignes</span><span class="sxs-lookup"><span data-stu-id="e3099-136">Applying *argmax* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a><span data-ttu-id="e3099-137">Exemple 3.</span><span class="sxs-lookup"><span data-stu-id="e3099-137">Example 3.</span></span> <span data-ttu-id="e3099-138">Application de *argmax* à tous les axes (le tenseur entier)</span><span class="sxs-lookup"><span data-stu-id="e3099-138">Applying *argmax* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="e3099-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3099-139">Remarks</span></span>
<span data-ttu-id="e3099-140">Les tailles de tenseur de sortie doivent être les mêmes que les tailles de tenseur d’entrée, à l’exception des axes réduits, qui doivent être 1.</span><span class="sxs-lookup"><span data-stu-id="e3099-140">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="e3099-141">Quand *AxisDirection* est [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), cette API est équivalente à [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) avec [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="e3099-141">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="e3099-142">Un sous-ensemble de cette fonctionnalité est exposé via l’opérateur [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) et est pris en charge sur les niveaux de fonctionnalité DirectML antérieurs.</span><span class="sxs-lookup"><span data-stu-id="e3099-142">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="e3099-143">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="e3099-143">Availability</span></span>
<span data-ttu-id="e3099-144">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="e3099-144">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e3099-145">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="e3099-145">Tensor constraints</span></span>
<span data-ttu-id="e3099-146">*InputTensor* et *OutputTensor* doivent avoir le même *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="e3099-146">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e3099-147">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="e3099-147">Tensor support</span></span>
| <span data-ttu-id="e3099-148">Tenseur</span><span class="sxs-lookup"><span data-stu-id="e3099-148">Tensor</span></span> | <span data-ttu-id="e3099-149">Type</span><span class="sxs-lookup"><span data-stu-id="e3099-149">Kind</span></span> | <span data-ttu-id="e3099-150">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="e3099-150">Supported dimension counts</span></span> | <span data-ttu-id="e3099-151">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3099-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e3099-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="e3099-152">InputTensor</span></span> | <span data-ttu-id="e3099-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="e3099-153">Input</span></span> | <span data-ttu-id="e3099-154">1 à 8</span><span class="sxs-lookup"><span data-stu-id="e3099-154">1 to 8</span></span> | <span data-ttu-id="e3099-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="e3099-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="e3099-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e3099-156">OutputTensor</span></span> | <span data-ttu-id="e3099-157">Output</span><span class="sxs-lookup"><span data-stu-id="e3099-157">Output</span></span> | <span data-ttu-id="e3099-158">1 à 8</span><span class="sxs-lookup"><span data-stu-id="e3099-158">1 to 8</span></span> | <span data-ttu-id="e3099-159">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="e3099-159">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="e3099-160">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e3099-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e3099-161">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="e3099-161">**Header**</span></span> | <span data-ttu-id="e3099-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="e3099-162">directml.h</span></span> |