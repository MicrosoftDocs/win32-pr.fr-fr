---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Extrait une sous-région unique (« Slice ») d’un tenseur d’entrée.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: 06721a7484426eb293494156a2ec23db6fbf0a6b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106535730"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a><span data-ttu-id="1f515-103">Structure DML_SLICE1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="1f515-103">DML_SLICE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="1f515-104">Extrait une sous-région unique (« Slice ») d’un tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1f515-104">Extracts a single subregion (a "slice") of an input tensor.</span></span>

<span data-ttu-id="1f515-105">La *fenêtre d’entrée* décrit les limites de l’entrée tenseur à prendre en compte dans la tranche.</span><span class="sxs-lookup"><span data-stu-id="1f515-105">The *input window* describes the bounds of the input tensor to consider in the slice.</span></span> <span data-ttu-id="1f515-106">La fenêtre est définie à l’aide de trois valeurs pour chaque dimension.</span><span class="sxs-lookup"><span data-stu-id="1f515-106">The window is defined using three values for each dimension.</span></span>

- <span data-ttu-id="1f515-107">Le *décalage* marque le *début de la fenêtre* dans une dimension.</span><span class="sxs-lookup"><span data-stu-id="1f515-107">The *offset* marks the *beginning of the window* in a dimension.</span></span>
- <span data-ttu-id="1f515-108">La *taille* marque l’étendue de la fenêtre dans une dimension.</span><span class="sxs-lookup"><span data-stu-id="1f515-108">The *size* marks the extent of the window in a dimension.</span></span> <span data-ttu-id="1f515-109">La *fin de la fenêtre* dans une dimension est `offset + size - 1` .</span><span class="sxs-lookup"><span data-stu-id="1f515-109">The *end of the window* in a dimension is `offset + size - 1`.</span></span>
- <span data-ttu-id="1f515-110">Le *Stride* indique comment parcourir les éléments d’une dimension.</span><span class="sxs-lookup"><span data-stu-id="1f515-110">The *stride* indicates how to traverse the elements in a dimension.</span></span>
  - <span data-ttu-id="1f515-111">L’amplitude du Stride indique le nombre d’éléments à avancer lors de la copie dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1f515-111">The magnitude of the stride indicates how many elements to advance when copying within the window.</span></span>
  - <span data-ttu-id="1f515-112">Si une Stride est positive, les éléments sont copiés à partir du *début* de la fenêtre dans la dimension.</span><span class="sxs-lookup"><span data-stu-id="1f515-112">If a stride is positive, elements are copied starting at the *beginning* of the window in the dimension.</span></span>
  - <span data-ttu-id="1f515-113">Si une valeur Stride est négative, les éléments sont copiés à partir de la *fin* de la fenêtre de la dimension.</span><span class="sxs-lookup"><span data-stu-id="1f515-113">If a stride is negative, elements are copied starting at the *end* of the window in the dimension.</span></span>

<span data-ttu-id="1f515-114">Le pseudo-code suivant illustre la façon dont les éléments sont copiés à l’aide de la fenêtre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1f515-114">The following pseudo-code illustrates how elements are copied using the input window.</span></span> <span data-ttu-id="1f515-115">Notez comment les éléments d’une dimension sont copiés du début à la fin avec un Stride positif et copiés de fin à début avec un Stride négatif.</span><span class="sxs-lookup"><span data-stu-id="1f515-115">Note how elements in a dimension are copied from start to end with a positive stride, and copied from end to start with a negative stride.</span></span>

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

<span data-ttu-id="1f515-116">La fenêtre d’entrée ne doit pas être vide dans toutes les dimensions et les ne doit pas de fenêtre s’étendent au-delà des dimensions du tenseur d’entrée (les lectures hors limites ne sont pas autorisées).</span><span class="sxs-lookup"><span data-stu-id="1f515-116">The input window mustn't be empty in any dimension, and the window mustn't extend beyond the dimensions of the input tensor (out-of-bounds reads aren't permitted).</span></span> <span data-ttu-id="1f515-117">La taille et les Strides de la fenêtre limitent efficacement le nombre d’éléments qui peuvent être copiés à partir de chaque dimension `i` du tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1f515-117">The window's size and strides effectively limit the number of elements that may be copied from each dimension `i` of the input tensor.</span></span>

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

<span data-ttu-id="1f515-118">Le tenseur de sortie n’est pas requis pour copier tous les éléments accessibles dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1f515-118">The output tensor isn't required to copy all reachable elements within the window.</span></span> <span data-ttu-id="1f515-119">La tranche est valide aussi longtemps que `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .</span><span class="sxs-lookup"><span data-stu-id="1f515-119">The slice is valid so long as `1 <= OutputSizes[i] <= MaxCopiedElements[i]`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f515-120">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="1f515-120">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="1f515-121">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="1f515-121">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f515-122">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f515-122">Syntax</span></span>
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a><span data-ttu-id="1f515-123">Membres</span><span class="sxs-lookup"><span data-stu-id="1f515-123">Members</span></span>

`InputTensor`

<span data-ttu-id="1f515-124">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1f515-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1f515-125">Tenseur à partir duquel extraire les tranches.</span><span class="sxs-lookup"><span data-stu-id="1f515-125">The tensor to extract slices from.</span></span>


`OutputTensor`

<span data-ttu-id="1f515-126">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1f515-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1f515-127">Tenseur dans lequel écrire les résultats de données découpées.</span><span class="sxs-lookup"><span data-stu-id="1f515-127">The tensor to write the sliced data results to.</span></span>


`DimensionCount`

<span data-ttu-id="1f515-128">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="1f515-128">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="1f515-129">Nombre de dimensions.</span><span class="sxs-lookup"><span data-stu-id="1f515-129">The number of dimensions.</span></span> <span data-ttu-id="1f515-130">Ce champ détermine la taille des tableaux *InputWindowOffsets*, *InputWindowSizes* et *InputWindowStrides* .</span><span class="sxs-lookup"><span data-stu-id="1f515-130">This field determines the size of the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="1f515-131">Cette valeur doit correspondre à la *DimensionCount* des dizaines d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="1f515-131">This value must match the *DimensionCount* of the input and output tensors.</span></span> <span data-ttu-id="1f515-132">Cette valeur doit être comprise entre 1 et 8 inclus, à partir de `DML_FEATURE_LEVEL_3_0` ; les niveaux de fonctionnalités antérieurs nécessitent une valeur de 4 ou 5.</span><span class="sxs-lookup"><span data-stu-id="1f515-132">This value must be between 1 and 8, inclusively, starting from `DML_FEATURE_LEVEL_3_0`; earlier feature levels require a value of either 4 or 5.</span></span>


`InputWindowOffsets`

<span data-ttu-id="1f515-133">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="1f515-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="1f515-134">Tableau contenant le début (éléments) de la fenêtre d’entrée dans chaque dimension.</span><span class="sxs-lookup"><span data-stu-id="1f515-134">An array containing the beginning (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="1f515-135">Les valeurs du tableau doivent satisfaire la contrainte `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="1f515-135">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowSizes`

<span data-ttu-id="1f515-136">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="1f515-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="1f515-137">Tableau contenant l’étendue (en éléments) de la fenêtre d’entrée dans chaque dimension.</span><span class="sxs-lookup"><span data-stu-id="1f515-137">An array containing the extent (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="1f515-138">Les valeurs du tableau doivent satisfaire la contrainte `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="1f515-138">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowStrides`

<span data-ttu-id="1f515-139">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="1f515-139">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="1f515-140">Tableau contenant le Stride de la tranche le long de chaque dimension du tenseur d’entrée, en éléments.</span><span class="sxs-lookup"><span data-stu-id="1f515-140">An array containing the slice's stride along each dimension of the input tensor, in elements.</span></span> <span data-ttu-id="1f515-141">L’amplitude du Stride indique le nombre d’éléments à avancer lors de la copie dans la fenêtre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1f515-141">The magnitude of the stride indicates how many elements to advance when copying within the input window.</span></span> <span data-ttu-id="1f515-142">Le signe du Stride détermine si les éléments sont copiés à partir du début de la fenêtre (Stride positif) ou jusqu’à la fin de la fenêtre (Stride négative).</span><span class="sxs-lookup"><span data-stu-id="1f515-142">The sign of the stride determines if elements are copied starting at the beginning of the window (positive stride) or end of the window (negative stride).</span></span> <span data-ttu-id="1f515-143">Les Strides ne peuvent pas être 0.</span><span class="sxs-lookup"><span data-stu-id="1f515-143">Strides may not be 0.</span></span>

## <a name="examples"></a><span data-ttu-id="1f515-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="1f515-144">Examples</span></span>

<span data-ttu-id="1f515-145">Les exemples suivants utilisent ce même tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1f515-145">The following examples use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a><span data-ttu-id="1f515-146">Exemple 1.</span><span class="sxs-lookup"><span data-stu-id="1f515-146">Example 1.</span></span> <span data-ttu-id="1f515-147">Tranche strided avec des Strides positifs</span><span class="sxs-lookup"><span data-stu-id="1f515-147">Strided slice with positive strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

<span data-ttu-id="1f515-148">Les éléments copiés sont calculés comme suit.</span><span class="sxs-lookup"><span data-stu-id="1f515-148">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a><span data-ttu-id="1f515-149">Exemple 2.</span><span class="sxs-lookup"><span data-stu-id="1f515-149">Example 2.</span></span> <span data-ttu-id="1f515-150">Tranche strided avec des Strides négatifs</span><span class="sxs-lookup"><span data-stu-id="1f515-150">Strided slice with negative strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

<span data-ttu-id="1f515-151">Rappelez-vous que les dimensions avec des Strides de fenêtre négatifs commencent à copier à la fin de la fenêtre d’entrée pour cette dimension ; pour ce faire, ajoutez `InputWindowSize[i] - 1` au décalage de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1f515-151">Recall that dimensions with negative window strides start copying at the end of the input window for that dimension; this is done by adding `InputWindowSize[i] - 1` to the window offset.</span></span> <span data-ttu-id="1f515-152">Les dimensions avec un Stride positif commencent simplement à `InputWindowOffset[i]` .</span><span class="sxs-lookup"><span data-stu-id="1f515-152">Dimensions with a positive stride simply start at `InputWindowOffset[i]`.</span></span>
- <span data-ttu-id="1f515-153">L’axe 0 (Stride de la `+1` fenêtre) commence la copie à `InputWindowOffsets[0] = 0` .</span><span class="sxs-lookup"><span data-stu-id="1f515-153">Axis 0 (`+1` window stride) starts copying at `InputWindowOffsets[0] = 0`.</span></span> 
- <span data-ttu-id="1f515-154">L’axe 1 ( `+1` fenêtre Stride) commence la copie à `InputWindowOffsets[1] = 0` .</span><span class="sxs-lookup"><span data-stu-id="1f515-154">Axis 1 (`+1` window stride) starts copying at `InputWindowOffsets[1] = 0`.</span></span> 
- <span data-ttu-id="1f515-155">L’axe 2 (Stride de la `-2` fenêtre) commence la copie à `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` .</span><span class="sxs-lookup"><span data-stu-id="1f515-155">Axis 2 (`-2` window stride) starts copying at `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3`.</span></span> 
- <span data-ttu-id="1f515-156">L’axe 3 (Stride de la `+2` fenêtre) commence la copie à `InputWindowOffsets[3] = 1` .</span><span class="sxs-lookup"><span data-stu-id="1f515-156">Axis 3 (`+2` window stride) starts copying at `InputWindowOffsets[3] = 1`.</span></span> 

<span data-ttu-id="1f515-157">Les éléments copiés sont calculés comme suit.</span><span class="sxs-lookup"><span data-stu-id="1f515-157">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a><span data-ttu-id="1f515-158">Notes</span><span class="sxs-lookup"><span data-stu-id="1f515-158">Remarks</span></span>
<span data-ttu-id="1f515-159">Cet opérateur est semblable à [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), mais il diffère de deux façons importantes.</span><span class="sxs-lookup"><span data-stu-id="1f515-159">This operator is similar to [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), but it differs in two important ways.</span></span>

- <span data-ttu-id="1f515-160">Les Strides de secteur peuvent être négatifs, ce qui permet d’inverser les valeurs le long des dimensions.</span><span class="sxs-lookup"><span data-stu-id="1f515-160">Slice strides may be negative, which allows reversing values along dimensions.</span></span>
- <span data-ttu-id="1f515-161">Les tailles des fenêtres d’entrée ne sont pas nécessairement les mêmes que celles de la sortie tenseur.</span><span class="sxs-lookup"><span data-stu-id="1f515-161">The input window sizes are not necessarily the same as the output tensor sizes.</span></span>

## <a name="availability"></a><span data-ttu-id="1f515-162">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="1f515-162">Availability</span></span>
<span data-ttu-id="1f515-163">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="1f515-163">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="1f515-164">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="1f515-164">Tensor constraints</span></span>
<span data-ttu-id="1f515-165">*InputTensor* et *OutputTensor* doivent avoir le même *type de données* et *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="1f515-165">*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="1f515-166">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="1f515-166">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="1f515-167">DML_FEATURE_LEVEL_3_0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1f515-167">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="1f515-168">Tenseur</span><span class="sxs-lookup"><span data-stu-id="1f515-168">Tensor</span></span> | <span data-ttu-id="1f515-169">Type</span><span class="sxs-lookup"><span data-stu-id="1f515-169">Kind</span></span> | <span data-ttu-id="1f515-170">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="1f515-170">Supported dimension counts</span></span> | <span data-ttu-id="1f515-171">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f515-171">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1f515-172">InputTensor</span><span class="sxs-lookup"><span data-stu-id="1f515-172">InputTensor</span></span> | <span data-ttu-id="1f515-173">Entrée</span><span class="sxs-lookup"><span data-stu-id="1f515-173">Input</span></span> | <span data-ttu-id="1f515-174">1 à 8</span><span class="sxs-lookup"><span data-stu-id="1f515-174">1 to 8</span></span> | <span data-ttu-id="1f515-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1f515-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1f515-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="1f515-176">OutputTensor</span></span> | <span data-ttu-id="1f515-177">Output</span><span class="sxs-lookup"><span data-stu-id="1f515-177">Output</span></span> | <span data-ttu-id="1f515-178">1 à 8</span><span class="sxs-lookup"><span data-stu-id="1f515-178">1 to 8</span></span> | <span data-ttu-id="1f515-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1f515-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="1f515-180">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1f515-180">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="1f515-181">Tenseur</span><span class="sxs-lookup"><span data-stu-id="1f515-181">Tensor</span></span> | <span data-ttu-id="1f515-182">Type</span><span class="sxs-lookup"><span data-stu-id="1f515-182">Kind</span></span> | <span data-ttu-id="1f515-183">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="1f515-183">Supported dimension counts</span></span> | <span data-ttu-id="1f515-184">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f515-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1f515-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="1f515-185">InputTensor</span></span> | <span data-ttu-id="1f515-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="1f515-186">Input</span></span> | <span data-ttu-id="1f515-187">4 à 5</span><span class="sxs-lookup"><span data-stu-id="1f515-187">4 to 5</span></span> | <span data-ttu-id="1f515-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1f515-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1f515-189">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="1f515-189">OutputTensor</span></span> | <span data-ttu-id="1f515-190">Output</span><span class="sxs-lookup"><span data-stu-id="1f515-190">Output</span></span> | <span data-ttu-id="1f515-191">4 à 5</span><span class="sxs-lookup"><span data-stu-id="1f515-191">4 to 5</span></span> | <span data-ttu-id="1f515-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1f515-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="1f515-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f515-193">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1f515-194">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="1f515-194">**Header**</span></span> | <span data-ttu-id="1f515-195">directml. h</span><span class="sxs-lookup"><span data-stu-id="1f515-195">directml.h</span></span> |