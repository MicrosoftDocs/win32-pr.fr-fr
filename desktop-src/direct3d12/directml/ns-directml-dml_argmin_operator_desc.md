---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: Génère les index des éléments de valeur minimale dans une ou plusieurs dimensions du tenseur d’entrée.
helpviewer_keywords:
- DML_ARGMIN_OPERATOR_DESC
- DML_ARGMIN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMIN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMIN_OPERATOR_DESC, DML_ARGMIN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
- directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
ms.openlocfilehash: 2e12a81593504a4eb7a0917e545bfa20c70647ff
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804082"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a><span data-ttu-id="b93b9-103">Structure DML_ARGMIN_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="b93b9-103">DML_ARGMIN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b93b9-104">Génère les index des éléments de valeur minimale dans une ou plusieurs dimensions du tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b93b9-104">Outputs the indices of the minimum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="b93b9-105">Chaque élément de sortie est le résultat de l’application d’une réduction *argmin* sur un sous-ensemble du tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b93b9-105">Each output element is the result of applying an *argmin* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="b93b9-106">La fonction *argmin* génère l’index de l’élément de valeur minimale dans un jeu d’éléments d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b93b9-106">The *argmin* function outputs the index of the minimum-valued element within a set of input elements.</span></span> <span data-ttu-id="b93b9-107">Les éléments d’entrée impliqués dans chaque réduction sont déterminés par les axes d’entrée fournis.</span><span class="sxs-lookup"><span data-stu-id="b93b9-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="b93b9-108">De même, chaque index de sortie est relatif aux axes d’entrée fournis.</span><span class="sxs-lookup"><span data-stu-id="b93b9-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="b93b9-109">Si tous les axes d’entrée sont spécifiés, l’opérateur applique une seule réduction *argmin* et produit un seul élément Output.</span><span class="sxs-lookup"><span data-stu-id="b93b9-109">If all input axes are specified, then the operator applies a single *argmin* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b93b9-110">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b93b9-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b93b9-111">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b93b9-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b93b9-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b93b9-112">Syntax</span></span>
```cpp
struct DML_ARGMIN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="b93b9-113">Membres</span><span class="sxs-lookup"><span data-stu-id="b93b9-113">Members</span></span>

`InputTensor`

<span data-ttu-id="b93b9-114">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b93b9-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b93b9-115">Tenseur à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="b93b9-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="b93b9-116">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b93b9-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b93b9-117">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="b93b9-117">The tensor to write the results to.</span></span> <span data-ttu-id="b93b9-118">Chaque élément de sortie est le résultat d’une réduction *argmin* sur un sous-ensemble d’éléments du *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="b93b9-118">Each output element is the result of an *argmin* reduction on a subset of elements from the *InputTensor*.</span></span>

- <span data-ttu-id="b93b9-119">*DimensionCount* doit correspondre à *InputTensor. DimensionCount* (le rang du tenseur d’entrée est préservé).</span><span class="sxs-lookup"><span data-stu-id="b93b9-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="b93b9-120">Les *tailles* doivent correspondre à *InputTensor.* sizes, à l’exception des dimensions incluses dans les *axes* réduits, qui doivent être de taille 1.</span><span class="sxs-lookup"><span data-stu-id="b93b9-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="b93b9-121">Type : **[uint](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b93b9-121">Type: **[UINT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="b93b9-122">Nombre d’axes à réduire.</span><span class="sxs-lookup"><span data-stu-id="b93b9-122">The number of axes to reduce.</span></span> <span data-ttu-id="b93b9-123">Ce champ détermine la taille du tableau *axes* .</span><span class="sxs-lookup"><span data-stu-id="b93b9-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="b93b9-124">Type : \_ Field_size \_ (AxisCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="b93b9-124">Type: \_Field_size\_(AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="b93b9-125">Axes avec lesquels réduire.</span><span class="sxs-lookup"><span data-stu-id="b93b9-125">The axes along which to reduce.</span></span> <span data-ttu-id="b93b9-126">Les valeurs doivent être comprises dans la plage `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="b93b9-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="b93b9-127">DML_AXIS_DIRECTION AxisDirection ;</span><span class="sxs-lookup"><span data-stu-id="b93b9-127">DML_AXIS_DIRECTION AxisDirection;</span></span>

<span data-ttu-id="b93b9-128">Type : **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="b93b9-128">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="b93b9-129">Détermine l’index à sélectionner lorsque plusieurs éléments d’entrée ont la même valeur.</span><span class="sxs-lookup"><span data-stu-id="b93b9-129">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="b93b9-130">**DML_AXIS_DIRECTION_INCREASING** retourne l’index du premier élément à valeur minimale (par exemple, `argmin({1,2,3,2,1}) = 0` )</span><span class="sxs-lookup"><span data-stu-id="b93b9-130">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first minimum-valued element (for example, `argmin({1,2,3,2,1}) = 0`)</span></span>
- <span data-ttu-id="b93b9-131">**DML_AXIS_DIRECTION_DECREASING** retourne l’index du dernier élément à valeur minimale (par exemple, `argmin({1,2,3,2,1}) = 4` )</span><span class="sxs-lookup"><span data-stu-id="b93b9-131">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last minimum-valued element (for example, `argmin({1,2,3,2,1}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="b93b9-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="b93b9-132">Examples</span></span>

<span data-ttu-id="b93b9-133">Les exemples de cette section utilisent tous ce même tenseur d’entrée à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="b93b9-133">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a><span data-ttu-id="b93b9-134">Exemple 1.</span><span class="sxs-lookup"><span data-stu-id="b93b9-134">Example 1.</span></span> <span data-ttu-id="b93b9-135">Application de *argmin* à des colonnes</span><span class="sxs-lookup"><span data-stu-id="b93b9-135">Applying *argmin* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a><span data-ttu-id="b93b9-136">Exemple 2.</span><span class="sxs-lookup"><span data-stu-id="b93b9-136">Example 2.</span></span> <span data-ttu-id="b93b9-137">Application de *argmin* à des lignes</span><span class="sxs-lookup"><span data-stu-id="b93b9-137">Applying *argmin* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a><span data-ttu-id="b93b9-138">Exemple 3.</span><span class="sxs-lookup"><span data-stu-id="b93b9-138">Example 3.</span></span> <span data-ttu-id="b93b9-139">Application de *argmin* à tous les axes (le tenseur entier)</span><span class="sxs-lookup"><span data-stu-id="b93b9-139">Applying *argmin* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="b93b9-140">Notes </span><span class="sxs-lookup"><span data-stu-id="b93b9-140">Remarks</span></span>
<span data-ttu-id="b93b9-141">Les tailles de tenseur de sortie doivent être les mêmes que les tailles de tenseur d’entrée, à l’exception des axes réduits, qui doivent être 1.</span><span class="sxs-lookup"><span data-stu-id="b93b9-141">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="b93b9-142">Quand *AxisDirection* est [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), cette API est équivalente à [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) avec [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="b93b9-142">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="b93b9-143">Un sous-ensemble de cette fonctionnalité est exposé via l’opérateur [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) et est pris en charge sur les niveaux de fonctionnalité DirectML antérieurs.</span><span class="sxs-lookup"><span data-stu-id="b93b9-143">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="b93b9-144">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="b93b9-144">Availability</span></span>
<span data-ttu-id="b93b9-145">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="b93b9-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b93b9-146">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="b93b9-146">Tensor constraints</span></span>
<span data-ttu-id="b93b9-147">*InputTensor* et *OutputTensor* doivent avoir le même *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="b93b9-147">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b93b9-148">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="b93b9-148">Tensor support</span></span>
| <span data-ttu-id="b93b9-149">Tenseur</span><span class="sxs-lookup"><span data-stu-id="b93b9-149">Tensor</span></span> | <span data-ttu-id="b93b9-150">Type</span><span class="sxs-lookup"><span data-stu-id="b93b9-150">Kind</span></span> | <span data-ttu-id="b93b9-151">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="b93b9-151">Supported dimension counts</span></span> | <span data-ttu-id="b93b9-152">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="b93b9-152">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b93b9-153">InputTensor</span><span class="sxs-lookup"><span data-stu-id="b93b9-153">InputTensor</span></span> | <span data-ttu-id="b93b9-154">Entrée</span><span class="sxs-lookup"><span data-stu-id="b93b9-154">Input</span></span> | <span data-ttu-id="b93b9-155">1 à 8</span><span class="sxs-lookup"><span data-stu-id="b93b9-155">1 to 8</span></span> | <span data-ttu-id="b93b9-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b93b9-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b93b9-157">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b93b9-157">OutputTensor</span></span> | <span data-ttu-id="b93b9-158">Output</span><span class="sxs-lookup"><span data-stu-id="b93b9-158">Output</span></span> | <span data-ttu-id="b93b9-159">1 à 8</span><span class="sxs-lookup"><span data-stu-id="b93b9-159">1 to 8</span></span> | <span data-ttu-id="b93b9-160">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="b93b9-160">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="b93b9-161">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b93b9-161">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b93b9-162">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="b93b9-162">**Header**</span></span> | <span data-ttu-id="b93b9-163">directml. h</span><span class="sxs-lookup"><span data-stu-id="b93b9-163">directml.h</span></span> |