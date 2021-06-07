---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Multiplie les éléments d’un tenseur le long d’un axe, en écrivant le Tally en cours d’exécution du produit dans le tenseur de sortie.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: 68b001467496ab9affc559e76ecac5461902399c
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521195"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a><span data-ttu-id="34e07-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="34e07-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="34e07-104">Multiplie les éléments d’un tenseur le long d’un axe, en écrivant le Tally en cours d’exécution du produit dans le tenseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="34e07-104">Multiplies the elements of a tensor along an axis, writing the running tally of the product into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34e07-105">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="34e07-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="34e07-106">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="34e07-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="34e07-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34e07-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a><span data-ttu-id="34e07-108">Membres</span><span class="sxs-lookup"><span data-stu-id="34e07-108">Members</span></span>

`InputTensor`

<span data-ttu-id="34e07-109">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="34e07-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="34e07-110">Tenseur contenant les données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="34e07-110">A tensor containing the input data.</span></span> <span data-ttu-id="34e07-111">Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *InputTensor* pour [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="34e07-111">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="34e07-112">Tenseur d’entrée contenant les éléments à multiplier.</span><span class="sxs-lookup"><span data-stu-id="34e07-112">The input tensor containing elements to be multiplied.</span></span>

`OutputTensor`

<span data-ttu-id="34e07-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="34e07-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="34e07-114">Tenseur de sortie dans lequel écrire les produits cumulatifs résultants.</span><span class="sxs-lookup"><span data-stu-id="34e07-114">The output tensor to write the resulting cumulative products to.</span></span> <span data-ttu-id="34e07-115">Ce tenseur doit avoir la même taille et le même type de données que *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="34e07-115">This tensor must have the same sizes and data type as *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="34e07-116">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="34e07-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="34e07-117">Index de la dimension sur laquelle multiplier les éléments.</span><span class="sxs-lookup"><span data-stu-id="34e07-117">The index of the dimension to multiply elements over.</span></span> <span data-ttu-id="34e07-118">Cette valeur doit être inférieure à la *DimensionCount* du *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="34e07-118">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="34e07-119">Type : **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="34e07-119">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="34e07-120">L’une des valeurs de l’énumération [DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction) .</span><span class="sxs-lookup"><span data-stu-id="34e07-120">One of the values of the [DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction) enumeration.</span></span> <span data-ttu-id="34e07-121">Si la valeur est **DML_AXIS_DIRECTION_INCREASING**, le produit se produit en parcourant le tenseur le long de l’axe spécifié par l’index d’élément croissant.</span><span class="sxs-lookup"><span data-stu-id="34e07-121">If set to **DML_AXIS_DIRECTION_INCREASING**, then the product occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="34e07-122">Si la valeur est **DML_AXIS_DIRECTION_DECREASING**, l’inverse est vrai et le produit se produit en parcourant les éléments par ordre décroissant d’index.</span><span class="sxs-lookup"><span data-stu-id="34e07-122">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true and the product occurs by traversing elements by descending index.</span></span>

`HasExclusiveProduct`

<span data-ttu-id="34e07-123">Type : <b> <a href="/windows/win32/winprog/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="34e07-123">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="34e07-124">Si la valeur est **true**, la valeur de l’élément actuel est exclue lors de l’écriture du Tally en cours d’exécution dans le tenseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="34e07-124">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="34e07-125">Si la valeur est **false**, la valeur de l’élément actuel est incluse dans le Tally en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="34e07-125">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="34e07-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="34e07-126">Examples</span></span>

<span data-ttu-id="34e07-127">Les exemples de cette section utilisent tous ce même tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="34e07-127">The examples in this section all use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a><span data-ttu-id="34e07-128">Exemple 1.</span><span class="sxs-lookup"><span data-stu-id="34e07-128">Example 1.</span></span> <span data-ttu-id="34e07-129">Produit cumulatif sur des éclats horizontaux</span><span class="sxs-lookup"><span data-stu-id="34e07-129">Cumulative product across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a><span data-ttu-id="34e07-130">Exemple 2.</span><span class="sxs-lookup"><span data-stu-id="34e07-130">Example 2.</span></span> <span data-ttu-id="34e07-131">Produits exclusifs</span><span class="sxs-lookup"><span data-stu-id="34e07-131">Exclusive products</span></span>

<span data-ttu-id="34e07-132">La définition de *HasExclusiveProduct* sur **true** a pour effet d’exclure la valeur de l’élément actuel de la Tally en cours d’exécution lors de l’écriture dans le tenseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="34e07-132">Setting *HasExclusiveProduct* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="34e07-133">Exemple 3.</span><span class="sxs-lookup"><span data-stu-id="34e07-133">Example 3.</span></span> <span data-ttu-id="34e07-134">Direction de l’axe</span><span class="sxs-lookup"><span data-stu-id="34e07-134">Axis direction</span></span>

<span data-ttu-id="34e07-135">La définition de *AxisDirection* sur [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/api/directml/ne-directml-dml_axis_direction) a pour effet d’inverser l’ordre de traversée des éléments lors du calcul de la Tally en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="34e07-135">Setting the *AxisDirection* to [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/api/directml/ne-directml-dml_axis_direction) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a><span data-ttu-id="34e07-136">Exemple 4 :</span><span class="sxs-lookup"><span data-stu-id="34e07-136">Example 4.</span></span> <span data-ttu-id="34e07-137">Multiplication sur un axe différent</span><span class="sxs-lookup"><span data-stu-id="34e07-137">Multiplying along a different axis</span></span>

<span data-ttu-id="34e07-138">Dans cet exemple, le produit se produit verticalement, le long de l’axe de la hauteur (deuxième dimension).</span><span class="sxs-lookup"><span data-stu-id="34e07-138">In this example, the product occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a><span data-ttu-id="34e07-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="34e07-139">Remarks</span></span>
<span data-ttu-id="34e07-140">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que le tenseur de sortie est autorisé à aliaser les *InputTensor* pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="34e07-140">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="34e07-141">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="34e07-141">Availability</span></span>
<span data-ttu-id="34e07-142">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="34e07-142">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="34e07-143">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="34e07-143">Tensor constraints</span></span>
<span data-ttu-id="34e07-144">*InputTensor* et *OutputTensor* doivent avoir le même *type de données* et les mêmes *tailles*.</span><span class="sxs-lookup"><span data-stu-id="34e07-144">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="34e07-145">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="34e07-145">Tensor support</span></span>
| <span data-ttu-id="34e07-146">Tenseur</span><span class="sxs-lookup"><span data-stu-id="34e07-146">Tensor</span></span> | <span data-ttu-id="34e07-147">Type</span><span class="sxs-lookup"><span data-stu-id="34e07-147">Kind</span></span> | <span data-ttu-id="34e07-148">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="34e07-148">Supported dimension counts</span></span> | <span data-ttu-id="34e07-149">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="34e07-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="34e07-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="34e07-150">InputTensor</span></span> | <span data-ttu-id="34e07-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="34e07-151">Input</span></span> | <span data-ttu-id="34e07-152">4</span><span class="sxs-lookup"><span data-stu-id="34e07-152">4</span></span> | <span data-ttu-id="34e07-153">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="34e07-153">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="34e07-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="34e07-154">OutputTensor</span></span> | <span data-ttu-id="34e07-155">Sortie</span><span class="sxs-lookup"><span data-stu-id="34e07-155">Output</span></span> | <span data-ttu-id="34e07-156">4</span><span class="sxs-lookup"><span data-stu-id="34e07-156">4</span></span> | <span data-ttu-id="34e07-157">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="34e07-157">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="34e07-158">Spécifications</span><span class="sxs-lookup"><span data-stu-id="34e07-158">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="34e07-159">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="34e07-159">**Header**</span></span> | <span data-ttu-id="34e07-160">directml. h</span><span class="sxs-lookup"><span data-stu-id="34e07-160">directml.h</span></span> |