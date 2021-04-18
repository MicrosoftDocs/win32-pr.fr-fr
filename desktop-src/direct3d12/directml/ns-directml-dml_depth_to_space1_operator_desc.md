---
UID: NS:directml.DML_DEPTH_TO_SPACE1_OPERATOR_DESC
title: DML_DEPTH_TO_SPACE1_OPERATOR_DESC
description: Réorganise (permute) les données de profondeur en blocs de données spatiales. L’opérateur génère une copie du tenseur d’entrée où les valeurs de la dimension de profondeur sont déplacées dans les blocs spatiaux vers les dimensions de hauteur et de largeur.
helpviewer_keywords:
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure
- direct3d12.dml_depth_to_space1_operator_desc
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.openlocfilehash: 639bda0b8d398d24b01649635d3cfcbd2301a211
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106527029"
---
# <a name="dml_depth_to_space1_operator_desc-structure-directmlh"></a><span data-ttu-id="30ac9-104">Structure DML_DEPTH_TO_SPACE1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="30ac9-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="30ac9-105">Réorganise (permute) les données de profondeur en blocs de données spatiales.</span><span class="sxs-lookup"><span data-stu-id="30ac9-105">Rearranges (permutes) data from depth into blocks of spatial data.</span></span> <span data-ttu-id="30ac9-106">L’opérateur génère une copie du tenseur d’entrée où les valeurs de la dimension de profondeur sont déplacées dans les blocs spatiaux vers les dimensions de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="30ac9-106">The operator outputs a copy of the input tensor where values from the depth dimension are moved in spatial blocks to the height and width dimensions.</span></span>

<span data-ttu-id="30ac9-107">Il s’agit de la transformation inverse de [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="30ac9-107">This is the inverse transformation of [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30ac9-108">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="30ac9-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="30ac9-109">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="30ac9-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30ac9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30ac9-110">Syntax</span></span>
```cpp
struct DML_DEPTH_TO_SPACE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="30ac9-111">Membres</span><span class="sxs-lookup"><span data-stu-id="30ac9-111">Members</span></span>

`InputTensor`

<span data-ttu-id="30ac9-112">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="30ac9-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="30ac9-113">Tenseur à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="30ac9-113">The tensor to read from.</span></span> <span data-ttu-id="30ac9-114">Les dimensions de l’tenseur d’entrée sont `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="30ac9-114">The input tensor's dimensions are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`OutputTensor`

<span data-ttu-id="30ac9-115">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="30ac9-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="30ac9-116">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="30ac9-116">The tensor to write the results to.</span></span> <span data-ttu-id="30ac9-117">Les dimensions de tenseur de sortie sont `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` , où :</span><span class="sxs-lookup"><span data-stu-id="30ac9-117">The output tensor's dimensions are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`, where:</span></span>

* <span data-ttu-id="30ac9-118">OutputChannelCount est calculé en tant que InputChannelCount/( `BlockSize`  \*  `BlockSize` )</span><span class="sxs-lookup"><span data-stu-id="30ac9-118">OutputChannelCount is computed as InputChannelCount / (`BlockSize` \* `BlockSize`)</span></span>
* <span data-ttu-id="30ac9-119">OutputHeight est calculé en tant que InputHeight \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="30ac9-119">OutputHeight is computed as InputHeight \* `BlockSize`</span></span>
* <span data-ttu-id="30ac9-120">OutputWidth est calculé en tant que InputWidth \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="30ac9-120">OutputWidth is computed as InputWidth \* `BlockSize`</span></span>


`BlockSize`

<span data-ttu-id="30ac9-121">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="30ac9-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="30ac9-122">La largeur et la hauteur des blocs qui sont déplacés.</span><span class="sxs-lookup"><span data-stu-id="30ac9-122">The width and height of the blocks that are moved.</span></span>


`Order`

<span data-ttu-id="30ac9-123">Type : **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="30ac9-123">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="30ac9-124">Consultez [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span><span class="sxs-lookup"><span data-stu-id="30ac9-124">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="30ac9-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="30ac9-125">Examples</span></span>

<span data-ttu-id="30ac9-126">Les exemples de cette section utilisent tous l’entrée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="30ac9-126">The examples in this section all use the input below.</span></span>

```
InputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="30ac9-127">Exemple 1.</span><span class="sxs-lookup"><span data-stu-id="30ac9-127">Example 1.</span></span> <span data-ttu-id="30ac9-128">Profondeur-colonne-ordre des lignes</span><span class="sxs-lookup"><span data-stu-id="30ac9-128">Depth-column-row order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="30ac9-129">Exemple 2.</span><span class="sxs-lookup"><span data-stu-id="30ac9-129">Example 2.</span></span> <span data-ttu-id="30ac9-130">Ordre colonne-ligne-profondeur</span><span class="sxs-lookup"><span data-stu-id="30ac9-130">Column-row-depth order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
```


## <a name="remarks"></a><span data-ttu-id="30ac9-131">Notes</span><span class="sxs-lookup"><span data-stu-id="30ac9-131">Remarks</span></span>
<span data-ttu-id="30ac9-132">Lorsque *Order* a la valeur [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** équivaut à [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span><span class="sxs-lookup"><span data-stu-id="30ac9-132">When *Order* is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** is equivalent to [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span></span>

## <a name="availability"></a><span data-ttu-id="30ac9-133">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="30ac9-133">Availability</span></span>
<span data-ttu-id="30ac9-134">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="30ac9-134">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="30ac9-135">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="30ac9-135">Tensor constraints</span></span>
<span data-ttu-id="30ac9-136">*InputTensor* et *OutputTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="30ac9-136">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="30ac9-137">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="30ac9-137">Tensor support</span></span>
| <span data-ttu-id="30ac9-138">Tenseur</span><span class="sxs-lookup"><span data-stu-id="30ac9-138">Tensor</span></span> | <span data-ttu-id="30ac9-139">Type</span><span class="sxs-lookup"><span data-stu-id="30ac9-139">Kind</span></span> | <span data-ttu-id="30ac9-140">Dimensions</span><span class="sxs-lookup"><span data-stu-id="30ac9-140">Dimensions</span></span> | <span data-ttu-id="30ac9-141">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="30ac9-141">Supported dimension counts</span></span> | <span data-ttu-id="30ac9-142">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="30ac9-142">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="30ac9-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="30ac9-143">InputTensor</span></span> | <span data-ttu-id="30ac9-144">Entrée</span><span class="sxs-lookup"><span data-stu-id="30ac9-144">Input</span></span> | <span data-ttu-id="30ac9-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="30ac9-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="30ac9-146">4</span><span class="sxs-lookup"><span data-stu-id="30ac9-146">4</span></span> | <span data-ttu-id="30ac9-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="30ac9-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="30ac9-148">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="30ac9-148">OutputTensor</span></span> | <span data-ttu-id="30ac9-149">Output</span><span class="sxs-lookup"><span data-stu-id="30ac9-149">Output</span></span> | <span data-ttu-id="30ac9-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="30ac9-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="30ac9-151">4</span><span class="sxs-lookup"><span data-stu-id="30ac9-151">4</span></span> | <span data-ttu-id="30ac9-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="30ac9-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="30ac9-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30ac9-153">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="30ac9-154">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="30ac9-154">**Header**</span></span> | <span data-ttu-id="30ac9-155">directml. h</span><span class="sxs-lookup"><span data-stu-id="30ac9-155">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="30ac9-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30ac9-156">See also</span></span>

* [<span data-ttu-id="30ac9-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="30ac9-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_depth_to_space_operator_desc)
* [<span data-ttu-id="30ac9-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="30ac9-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)