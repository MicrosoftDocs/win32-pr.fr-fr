---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Additionne les éléments d’un tenseur le long d’un axe, en écrivant le haut de la somme en cours dans le tenseur de sortie.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 2862a2add207b0bb6c41f5c1aabbc390797cba23
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417400"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="eb8d8-103">Structure DML_CUMULATIVE_SUMMATION_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="eb8d8-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="eb8d8-104">Additionne les éléments d’un tenseur le long d’un axe, en écrivant le haut de la somme en cours dans le tenseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb8d8-105">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="eb8d8-106">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="eb8d8-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb8d8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb8d8-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```

## <a name="members"></a><span data-ttu-id="eb8d8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="eb8d8-108">Members</span></span>

`InputTensor`

<span data-ttu-id="eb8d8-109">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb8d8-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb8d8-110">Tenseur d’entrée contenant les éléments à additionner.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-110">The input tensor containing elements to be summed.</span></span>

`OutputTensor`

<span data-ttu-id="eb8d8-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb8d8-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb8d8-112">Tenseur de sortie dans lequel écrire les sommes cumulées qui en résultent.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="eb8d8-113">Ce tenseur doit avoir les mêmes tailles et le même type de données que le *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="eb8d8-114">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="eb8d8-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="eb8d8-115">Index de la dimension sur laquelle somme les éléments.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="eb8d8-116">Cette valeur doit être inférieure à la *DimensionCount* du *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="eb8d8-117">Type : **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="eb8d8-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="eb8d8-118">L’une des valeurs de l’énumération [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="eb8d8-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="eb8d8-119">Si la valeur est **DML_AXIS_DIRECTION_INCREASING**, la somme se produit en parcourant le tenseur le long de l’axe spécifié par l’index d’élément croissant.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="eb8d8-120">Si la valeur est **DML_AXIS_DIRECTION_DECREASING**, l’inverse est vrai et la somme se produit en parcourant les éléments par ordre décroissant d’index.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>

`HasExclusiveSum`

<span data-ttu-id="eb8d8-121">Type : <b> <a href="/windows/win32/winprog/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="eb8d8-121">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="eb8d8-122">Si la valeur est **true**, la valeur de l’élément actuel est exclue lors de l’écriture du Tally en cours d’exécution dans le tenseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-122">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="eb8d8-123">Si la valeur est **false**, la valeur de l’élément actuel est incluse dans le Tally en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-123">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="eb8d8-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="eb8d8-124">Examples</span></span>

<span data-ttu-id="eb8d8-125">Les exemples de cette section utilisent tous un tenseur d’entrée avec les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-125">The examples in this section all use an input tensor with the following properties.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-summation-across-horizontal-slivers"></a><span data-ttu-id="eb8d8-126">Exemple 1.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-126">Example 1.</span></span> <span data-ttu-id="eb8d8-127">Somme cumulée sur des éclats horizontaux</span><span class="sxs-lookup"><span data-stu-id="eb8d8-127">Cumulative summation across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  3,  6, 11],     // i.e. [2, 2+1, 2+1+3, 2+1+3+5]
   [3, 11, 18, 21],     //      [...                   ]
   [9, 15, 17, 21]]]]   //      [...                   ]
```

### <a name="example-2-exclusive-sums"></a><span data-ttu-id="eb8d8-128">Exemple 2.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-128">Example 2.</span></span> <span data-ttu-id="eb8d8-129">Sommes exclusives</span><span class="sxs-lookup"><span data-stu-id="eb8d8-129">Exclusive sums</span></span>

<span data-ttu-id="eb8d8-130">La définition de *HasExclusiveSum* sur **true** a pour effet d’exclure la valeur de l’élément actuel de la Tally en cours d’exécution lors de l’écriture dans le tenseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-130">Setting *HasExclusiveSum* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[0, 2,  3,  6],      // Notice the sum is written before adding the input,
   [0, 3, 11, 18],      // and the final total is not written to any output.
   [0, 9, 15, 17]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="eb8d8-131">Exemple 3.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-131">Example 3.</span></span> <span data-ttu-id="eb8d8-132">Direction de l’axe</span><span class="sxs-lookup"><span data-stu-id="eb8d8-132">Axis direction</span></span>

<span data-ttu-id="eb8d8-133">La définition de *AxisDirection* sur [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) a pour effet d’inverser l’ordre de traversée des éléments lors du calcul de la Tally en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-133">Setting the *AxisDirection* to [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[11,  9,  8,  5],    // i.e. [2+1+3+5, 1+3+5, 3+5, 5]
   [21, 18, 10,  3],    //      [...                   ]
   [21, 12,  6,  4]]]]  //      [...                   ]
```

### <a name="example-4-summing-along-a-different-axis"></a><span data-ttu-id="eb8d8-134">Exemple 4 :</span><span class="sxs-lookup"><span data-stu-id="eb8d8-134">Example 4.</span></span> <span data-ttu-id="eb8d8-135">Somme sur un axe différent</span><span class="sxs-lookup"><span data-stu-id="eb8d8-135">Summing along a different axis</span></span>

<span data-ttu-id="eb8d8-136">Dans cet exemple, la somme se produit verticalement, le long de l’axe de la hauteur (deuxième dimension).</span><span class="sxs-lookup"><span data-stu-id="eb8d8-136">In this example, the summation occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 5,  9, 10,  8],   //      [2+3,  ...]
   [14, 15, 12, 12]]]] //      [2+3+9 ...]
```

## <a name="remarks"></a><span data-ttu-id="eb8d8-137">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb8d8-137">Remarks</span></span>
<span data-ttu-id="eb8d8-138">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que le *OutputTensor* est autorisé à aliaser le *InputTensor* au cours de la liaison.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-138">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="eb8d8-139">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="eb8d8-139">Availability</span></span>
<span data-ttu-id="eb8d8-140">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="eb8d8-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="eb8d8-141">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="eb8d8-141">Tensor constraints</span></span>
<span data-ttu-id="eb8d8-142">*InputTensor* et *OutputTensor* doivent avoir le même *type de données* et les mêmes *tailles*.</span><span class="sxs-lookup"><span data-stu-id="eb8d8-142">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="eb8d8-143">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="eb8d8-143">Tensor support</span></span>
| <span data-ttu-id="eb8d8-144">Tenseur</span><span class="sxs-lookup"><span data-stu-id="eb8d8-144">Tensor</span></span> | <span data-ttu-id="eb8d8-145">Type</span><span class="sxs-lookup"><span data-stu-id="eb8d8-145">Kind</span></span> | <span data-ttu-id="eb8d8-146">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="eb8d8-146">Supported dimension counts</span></span> | <span data-ttu-id="eb8d8-147">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb8d8-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="eb8d8-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="eb8d8-148">InputTensor</span></span> | <span data-ttu-id="eb8d8-149">Entrée</span><span class="sxs-lookup"><span data-stu-id="eb8d8-149">Input</span></span> | <span data-ttu-id="eb8d8-150">4</span><span class="sxs-lookup"><span data-stu-id="eb8d8-150">4</span></span> | <span data-ttu-id="eb8d8-151">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="eb8d8-151">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="eb8d8-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="eb8d8-152">OutputTensor</span></span> | <span data-ttu-id="eb8d8-153">Sortie</span><span class="sxs-lookup"><span data-stu-id="eb8d8-153">Output</span></span> | <span data-ttu-id="eb8d8-154">4</span><span class="sxs-lookup"><span data-stu-id="eb8d8-154">4</span></span> | <span data-ttu-id="eb8d8-155">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="eb8d8-155">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="eb8d8-156">Spécifications</span><span class="sxs-lookup"><span data-stu-id="eb8d8-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="eb8d8-157">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="eb8d8-157">**Header**</span></span> | <span data-ttu-id="eb8d8-158">directml. h</span><span class="sxs-lookup"><span data-stu-id="eb8d8-158">directml.h</span></span> |
