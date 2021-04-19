---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Calcule les coordonnées à N dimensions de tous les éléments non nuls du tenseur d’entrée.
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: a662ac3b341c07e512e11dcc15cbc9b11ec5f405
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106523742"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a><span data-ttu-id="64b87-103">Structure DML_NONZERO_COORDINATES_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="64b87-103">DML_NONZERO_COORDINATES_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="64b87-104">Calcule les coordonnées à N dimensions de tous les éléments non nuls du tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="64b87-104">Computes the N-dimensional coordinates of all non-zero elements of the input tensor.</span></span>

<span data-ttu-id="64b87-105">Cet opérateur produit une matrice MxN de valeurs, où chaque ligne M contient une coordonnée N-dimensionnel d’une valeur différente de zéro de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="64b87-105">This operator produces an MxN matrix of values, where each row M contains an N-dimensional coordinate of a non-zero value from the input.</span></span> <span data-ttu-id="64b87-106">Lors de l’utilisation des entrées **FLOAT32** ou **FLOAT16** , les valeurs négatives et positives 0 (0.0 f et-0.0 f) sont traitées comme zéro dans le cadre de cet opérateur.</span><span class="sxs-lookup"><span data-stu-id="64b87-106">When using **FLOAT32** or **FLOAT16** inputs, both negative and positive 0 (0.0f and -0.0f) are treated as zero for the purposes of this operator.</span></span>

<span data-ttu-id="64b87-107">L’opérateur exige que le *OutputCoordinatesTensor* ait une taille suffisamment grande pour prendre en compte un scénario le plus défavorable lorsque chaque élément de l’entrée est différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="64b87-107">The operator requires that the *OutputCoordinatesTensor* has a size large enough to accommodate a worst-case scenario where every element of the input is non-zero.</span></span> <span data-ttu-id="64b87-108">Cet opérateur retourne le nombre d’éléments non nuls via *OutputCountTensor*, que les appelants peuvent inspecter pour déterminer le nombre de coordonnées écrites dans le *OutputCoordinatesTensor*.</span><span class="sxs-lookup"><span data-stu-id="64b87-108">This operator returns the count of of non-zero elements via the *OutputCountTensor*, which callers can inspect to determine the number of coordinates written to the *OutputCoordinatesTensor*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64b87-109">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="64b87-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="64b87-110">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="64b87-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="64b87-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64b87-111">Syntax</span></span>

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a><span data-ttu-id="64b87-112">Membres</span><span class="sxs-lookup"><span data-stu-id="64b87-112">Members</span></span>

`InputTensor`

<span data-ttu-id="64b87-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64b87-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64b87-114">Tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="64b87-114">An input tensor.</span></span>

`OutputCountTensor`

<span data-ttu-id="64b87-115">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64b87-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64b87-116">Tenseur de sortie qui contient le nombre d’éléments non nuls dans le tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="64b87-116">An output tensor that holds the count of non-zero elements in the input tensor.</span></span> <span data-ttu-id="64b87-117">Ce tenseur doit être un scalaire &mdash; , c’est-à-dire que les tailles de ce tenseur doivent toutes être 1.</span><span class="sxs-lookup"><span data-stu-id="64b87-117">This tensor must be a scalar&mdash;that is, the Sizes of this tensor must all be 1.</span></span> <span data-ttu-id="64b87-118">Le type de ce tenseur doit être **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="64b87-118">The type of this tensor must be **UINT32**.</span></span>

`OutputCoordinatesTensor`

<span data-ttu-id="64b87-119">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="64b87-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="64b87-120">Tenseur de sortie qui contient les coordonnées à N dimensions des éléments d’entrée qui ne sont pas nuls.</span><span class="sxs-lookup"><span data-stu-id="64b87-120">An output tensor that holds the N-dimensional coordinates of the input elements which are non-zero.</span></span> 

<span data-ttu-id="64b87-121">Ce tenseur doit avoir une *taille* de `{1,1,M,N}` (si *DimensionCount* est 4), `{1,1,1,M,N}` ou (si *DimensionCount* est 5), où M est le nombre total d’éléments dans le *InputTensor*, et N est supérieur ou égal au *rang effectif* de *InputTensor*, jusqu’à la *DimensionCount* de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="64b87-121">This tensor must have *Sizes* of `{1,1,M,N}` (if *DimensionCount* is 4), or `{1,1,1,M,N}` (if *DimensionCount* is 5), where M is the total number of elements in the *InputTensor*, and N is greater or equal to the *effective rank* of *InputTensor*, up to the *DimensionCount* of the input.</span></span>

<span data-ttu-id="64b87-122">Le rang effectif d’un tenseur est déterminé par le *DimensionCount* de ce tenseur, à l’exception des principales dimensions de taille 1.</span><span class="sxs-lookup"><span data-stu-id="64b87-122">The effective rank of a tensor is determined by the *DimensionCount* of that tensor excluding leading dimensions of size 1.</span></span> <span data-ttu-id="64b87-123">Par exemple, un tenseur avec la taille de `{1,2,3,4}` a le rang 3 effectif, tout comme un tenseur avec des tailles de `{1,1,5,5,5}` .</span><span class="sxs-lookup"><span data-stu-id="64b87-123">For example a tensor with sizes of `{1,2,3,4}` has effective rank 3, as does a tensor with sizes of `{1,1,5,5,5}`.</span></span> <span data-ttu-id="64b87-124">Un tenseur avec des tailles `{1,1,1,1}` a un rang effectif égal à 0.</span><span class="sxs-lookup"><span data-stu-id="64b87-124">A tensor with sizes `{1,1,1,1}` has effective rank 0.</span></span>

<span data-ttu-id="64b87-125">Prenons l’exemple d’un *InputTensor* avec des *tailles* de `{1,1,12,5}` .</span><span class="sxs-lookup"><span data-stu-id="64b87-125">Consider an *InputTensor* with *Sizes* of `{1,1,12,5}`.</span></span> <span data-ttu-id="64b87-126">Ce tenseur d’entrée contient 60 éléments et a un rang effectif de 2.</span><span class="sxs-lookup"><span data-stu-id="64b87-126">This input tensor contains 60 elements, and has an effective rank of 2.</span></span> <span data-ttu-id="64b87-127">Dans cet exemple, toutes les tailles valides de *OutputCoordinatesTensor* se présentent sous la forme `{1,1,60,N}` , où n >= 2 mais pas supérieur à *DimensionCount* (4 dans cet exemple).</span><span class="sxs-lookup"><span data-stu-id="64b87-127">In this example all valid sizes of *OutputCoordinatesTensor* are of the form `{1,1,60,N}`, where N >= 2 but no greater than the *DimensionCount* (4 in this example).</span></span>

<span data-ttu-id="64b87-128">Les coordonnées écrites dans cet tenseur sont garanties par ordre croissant d’index d’élément.</span><span class="sxs-lookup"><span data-stu-id="64b87-128">The coordinates written into this tensor are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="64b87-129">Par exemple, si l’tenseur d’entrée a 3 valeurs non null au niveau des coordonnées {1,0} , {1,2} et {0,5} , les valeurs écrites dans le *OutputCoordinatesTensor* sont `[[0,5], [1,0], [1,2]]` .</span><span class="sxs-lookup"><span data-stu-id="64b87-129">For example if the input tensor has 3 non-zero values at coordinates {1,0}, {1,2}, and {0,5}, the values written to the *OutputCoordinatesTensor* will be `[[0,5], [1,0], [1,2]]`.</span></span>

<span data-ttu-id="64b87-130">Bien que ce tenseur nécessite que sa dimension M soit égale au nombre d’éléments dans le tenseur d’entrée, cet opérateur écrira uniquement un maximum d’éléments OutputCount dans ce tenseur.</span><span class="sxs-lookup"><span data-stu-id="64b87-130">While this tensor requires its dimension M to equal the number of elements in the input tensor, this operator will only write a maximum of OutputCount elements to this tensor.</span></span> <span data-ttu-id="64b87-131">Le OutputCount est retourné via le *OutputCountTensor* scalaire.</span><span class="sxs-lookup"><span data-stu-id="64b87-131">The OutputCount is returned through the scalar *OutputCountTensor*.</span></span>

> [!NOTE]
> <span data-ttu-id="64b87-132">Les éléments restants de ce tenseur au-delà du OutputCount ne sont pas définis une fois cet opérateur terminé.</span><span class="sxs-lookup"><span data-stu-id="64b87-132">The remaining elements of this tensor beyond the OutputCount are undefined once this operator completes.</span></span> <span data-ttu-id="64b87-133">Vous ne devez pas compter sur les valeurs de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="64b87-133">You shouldn't rely on the values of these elements.</span></span>

## <a name="example"></a><span data-ttu-id="64b87-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="64b87-134">Example</span></span>

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a><span data-ttu-id="64b87-135">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="64b87-135">Availability</span></span>
<span data-ttu-id="64b87-136">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="64b87-136">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="64b87-137">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="64b87-137">Tensor constraints</span></span>
<span data-ttu-id="64b87-138">*InputTensor*, *OutputCoordinatesTensor* et `OutputCountTensor` doivent avoir le même *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="64b87-138">*InputTensor*, *OutputCoordinatesTensor*, and `OutputCountTensor` must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="64b87-139">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="64b87-139">Tensor support</span></span>
| <span data-ttu-id="64b87-140">Tenseur</span><span class="sxs-lookup"><span data-stu-id="64b87-140">Tensor</span></span> | <span data-ttu-id="64b87-141">Type</span><span class="sxs-lookup"><span data-stu-id="64b87-141">Kind</span></span> | <span data-ttu-id="64b87-142">Dimensions</span><span class="sxs-lookup"><span data-stu-id="64b87-142">Dimensions</span></span> | <span data-ttu-id="64b87-143">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="64b87-143">Supported dimension counts</span></span> | <span data-ttu-id="64b87-144">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="64b87-144">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="64b87-145">InputTensor</span><span class="sxs-lookup"><span data-stu-id="64b87-145">InputTensor</span></span> | <span data-ttu-id="64b87-146">Entrée</span><span class="sxs-lookup"><span data-stu-id="64b87-146">Input</span></span> | <span data-ttu-id="64b87-147">{[D0], D1, D2, D3, D4}</span><span class="sxs-lookup"><span data-stu-id="64b87-147">{ [D0], D1, D2, D3, D4 }</span></span> | <span data-ttu-id="64b87-148">4 à 5</span><span class="sxs-lookup"><span data-stu-id="64b87-148">4 to 5</span></span> | <span data-ttu-id="64b87-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="64b87-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="64b87-150">OutputCountTensor</span><span class="sxs-lookup"><span data-stu-id="64b87-150">OutputCountTensor</span></span> | <span data-ttu-id="64b87-151">Output</span><span class="sxs-lookup"><span data-stu-id="64b87-151">Output</span></span> | <span data-ttu-id="64b87-152">{[1], 1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="64b87-152">{ [1], 1, 1, 1, 1 }</span></span> | <span data-ttu-id="64b87-153">4 à 5</span><span class="sxs-lookup"><span data-stu-id="64b87-153">4 to 5</span></span> | <span data-ttu-id="64b87-154">UINT32</span><span class="sxs-lookup"><span data-stu-id="64b87-154">UINT32</span></span> |
| <span data-ttu-id="64b87-155">OutputCoordinatesTensor</span><span class="sxs-lookup"><span data-stu-id="64b87-155">OutputCoordinatesTensor</span></span> | <span data-ttu-id="64b87-156">Output</span><span class="sxs-lookup"><span data-stu-id="64b87-156">Output</span></span> | <span data-ttu-id="64b87-157">{[1], 1, 1, M, N}</span><span class="sxs-lookup"><span data-stu-id="64b87-157">{ [1], 1, 1, M, N }</span></span> | <span data-ttu-id="64b87-158">4 à 5</span><span class="sxs-lookup"><span data-stu-id="64b87-158">4 to 5</span></span> | <span data-ttu-id="64b87-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="64b87-159">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="64b87-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64b87-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="64b87-161">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="64b87-161">**Header**</span></span> | <span data-ttu-id="64b87-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="64b87-162">directml.h</span></span> |