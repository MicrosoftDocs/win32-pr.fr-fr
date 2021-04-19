---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Exécute une fonction de multiplication de matrice sur des données quantifiées. Cet opérateur est mathématiquement équivalent à déquantifier les entrées, à effectuer une multiplication de matrice, puis à quantifier la sortie.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: d0b20a37bca6ddf6083b116b53290a6b6b2084f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106538037"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="50258-104">Structure DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="50258-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="50258-105">Exécute une fonction de multiplication de matrice sur des données quantifiées.</span><span class="sxs-lookup"><span data-stu-id="50258-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="50258-106">Cet opérateur est mathématiquement équivalent à déquantifier les entrées, à effectuer une multiplication de matrice, puis à quantifier la sortie.</span><span class="sxs-lookup"><span data-stu-id="50258-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="50258-107">Cet opérateur exige que la matrice multiplie les dizaines d’entrée par 4D qui sont mis en forme en tant que `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="50258-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="50258-108">L’opérateur de multiplication de matrice effectue un nombre BatchCount \* ChannelCount de multiplications de matrices indépendantes.</span><span class="sxs-lookup"><span data-stu-id="50258-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="50258-109">Par exemple, si *ATensor* a *une taille de* , et que BTensor a une taille de, `{ BatchCount, ChannelCount, M, K }` et que   `{ BatchCount, ChannelCount, K, N }` *OutputTensor* a une *taille* de, `{ BatchCount, ChannelCount, M, N }` alors l’opérateur de multiplication de matrice effectuera BatchCount \* ChannelCount des multiplications de matrices indépendantes {M, K} x {K, N} = {m, n}.</span><span class="sxs-lookup"><span data-stu-id="50258-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="50258-110">Dequantifier la fonction</span><span class="sxs-lookup"><span data-stu-id="50258-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="50258-111">Fonction quantifier</span><span class="sxs-lookup"><span data-stu-id="50258-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="50258-112">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="50258-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="50258-113">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="50258-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="50258-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50258-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="50258-115">Membres</span><span class="sxs-lookup"><span data-stu-id="50258-115">Members</span></span>

`ATensor`

<span data-ttu-id="50258-116">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="50258-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="50258-117">Tenseur contenant les données.</span><span class="sxs-lookup"><span data-stu-id="50258-117">A tensor containing the A data.</span></span> <span data-ttu-id="50258-118">Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="50258-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="50258-119">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="50258-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="50258-120">Tenseur contenant les données de mise à l’échelle ATensor.</span><span class="sxs-lookup"><span data-stu-id="50258-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="50258-121">Les dimensions attendues du `AScaleTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="50258-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="50258-122">Ces valeurs de mise à l’échelle sont utilisées pour déquantifier les valeurs A.</span><span class="sxs-lookup"><span data-stu-id="50258-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="50258-123">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="50258-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="50258-124">Tenseur facultatif contenant les données de point zéro *ATensor* .</span><span class="sxs-lookup"><span data-stu-id="50258-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="50258-125">Les dimensions attendues du AZeroPointTensor sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="50258-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="50258-126">Ces valeurs de zéro point sont utilisées pour déquantifier les valeurs de ATensor.</span><span class="sxs-lookup"><span data-stu-id="50258-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="50258-127">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="50258-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="50258-128">Tenseur contenant les données B.</span><span class="sxs-lookup"><span data-stu-id="50258-128">A tensor containing the B data.</span></span> <span data-ttu-id="50258-129">Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="50258-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="50258-130">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="50258-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="50258-131">Tenseur contenant les données de mise à l’échelle *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="50258-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="50258-132">Les dimensions attendues du `BScaleTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, 1, N }` si la quantification par colonne est requise.</span><span class="sxs-lookup"><span data-stu-id="50258-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="50258-133">Ces valeurs de mise à l’échelle sont utilisées pour déquantifier les valeurs *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="50258-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="50258-134">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="50258-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="50258-135">Tenseur facultatif contenant les données de point zéro *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="50258-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="50258-136">Les dimensions attendues du `BZeroPointTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, 1, N }` si la quantification par colonne est requise.</span><span class="sxs-lookup"><span data-stu-id="50258-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="50258-137">Ces valeurs de zéro point sont utilisées pour déquantifier les valeurs de *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="50258-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="50258-138">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="50258-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="50258-139">Tenseur contenant les données de mise à l’échelle du filtre.</span><span class="sxs-lookup"><span data-stu-id="50258-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="50258-140">Les dimensions attendues du `OutputScaleTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="50258-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="50258-141">Cette valeur de mise à l’échelle est utilisée pour déquantifier les valeurs de filtre.</span><span class="sxs-lookup"><span data-stu-id="50258-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="50258-142">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="50258-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="50258-143">Tenseur facultatif contenant les données de point zéro du filtre.</span><span class="sxs-lookup"><span data-stu-id="50258-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="50258-144">Les dimensions attendues du `OutputZeroPointTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="50258-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="50258-145">Cette valeur de point zéro est utilisée pour déquantifier les valeurs de filtre.</span><span class="sxs-lookup"><span data-stu-id="50258-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="50258-146">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="50258-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="50258-147">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="50258-147">A tensor to write the results to.</span></span> <span data-ttu-id="50258-148">Les dimensions de ce tenseur sont `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="50258-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="50258-149">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="50258-149">Availability</span></span>
<span data-ttu-id="50258-150">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="50258-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="50258-151">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="50258-151">Tensor constraints</span></span>
* <span data-ttu-id="50258-152">*ATensor* et `AZeroPointTensor` doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="50258-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="50258-153">*BTensor* et `BZeroPointTensor` doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="50258-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="50258-154">*OutputTensor* et `OutputZeroPointTensor` doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="50258-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="50258-155">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="50258-155">Tensor support</span></span>
| <span data-ttu-id="50258-156">Tenseur</span><span class="sxs-lookup"><span data-stu-id="50258-156">Tensor</span></span> | <span data-ttu-id="50258-157">Type</span><span class="sxs-lookup"><span data-stu-id="50258-157">Kind</span></span> | <span data-ttu-id="50258-158">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="50258-158">Supported dimension counts</span></span> | <span data-ttu-id="50258-159">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="50258-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="50258-160">ATensor</span><span class="sxs-lookup"><span data-stu-id="50258-160">ATensor</span></span> | <span data-ttu-id="50258-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="50258-161">Input</span></span> | <span data-ttu-id="50258-162">4</span><span class="sxs-lookup"><span data-stu-id="50258-162">4</span></span> | <span data-ttu-id="50258-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="50258-163">INT8, UINT8</span></span> |
| <span data-ttu-id="50258-164">AScaleTensor</span><span class="sxs-lookup"><span data-stu-id="50258-164">AScaleTensor</span></span> | <span data-ttu-id="50258-165">Entrée</span><span class="sxs-lookup"><span data-stu-id="50258-165">Input</span></span> | <span data-ttu-id="50258-166">4</span><span class="sxs-lookup"><span data-stu-id="50258-166">4</span></span> | <span data-ttu-id="50258-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="50258-167">FLOAT32</span></span> |
| <span data-ttu-id="50258-168">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="50258-168">AZeroPointTensor</span></span> | <span data-ttu-id="50258-169">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="50258-169">Optional input</span></span> | <span data-ttu-id="50258-170">4</span><span class="sxs-lookup"><span data-stu-id="50258-170">4</span></span> | <span data-ttu-id="50258-171">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="50258-171">INT8, UINT8</span></span> |
| <span data-ttu-id="50258-172">BTensor</span><span class="sxs-lookup"><span data-stu-id="50258-172">BTensor</span></span> | <span data-ttu-id="50258-173">Entrée</span><span class="sxs-lookup"><span data-stu-id="50258-173">Input</span></span> | <span data-ttu-id="50258-174">4</span><span class="sxs-lookup"><span data-stu-id="50258-174">4</span></span> | <span data-ttu-id="50258-175">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="50258-175">INT8, UINT8</span></span> |
| <span data-ttu-id="50258-176">BScaleTensor</span><span class="sxs-lookup"><span data-stu-id="50258-176">BScaleTensor</span></span> | <span data-ttu-id="50258-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="50258-177">Input</span></span> | <span data-ttu-id="50258-178">4</span><span class="sxs-lookup"><span data-stu-id="50258-178">4</span></span> | <span data-ttu-id="50258-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="50258-179">FLOAT32</span></span> |
| <span data-ttu-id="50258-180">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="50258-180">BZeroPointTensor</span></span> | <span data-ttu-id="50258-181">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="50258-181">Optional input</span></span> | <span data-ttu-id="50258-182">4</span><span class="sxs-lookup"><span data-stu-id="50258-182">4</span></span> | <span data-ttu-id="50258-183">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="50258-183">INT8, UINT8</span></span> |
| <span data-ttu-id="50258-184">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="50258-184">OutputScaleTensor</span></span> | <span data-ttu-id="50258-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="50258-185">Input</span></span> | <span data-ttu-id="50258-186">4</span><span class="sxs-lookup"><span data-stu-id="50258-186">4</span></span> | <span data-ttu-id="50258-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="50258-187">FLOAT32</span></span> |
| <span data-ttu-id="50258-188">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="50258-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="50258-189">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="50258-189">Optional input</span></span> | <span data-ttu-id="50258-190">4</span><span class="sxs-lookup"><span data-stu-id="50258-190">4</span></span> | <span data-ttu-id="50258-191">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="50258-191">INT8, UINT8</span></span> |
| <span data-ttu-id="50258-192">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="50258-192">OutputTensor</span></span> | <span data-ttu-id="50258-193">Output</span><span class="sxs-lookup"><span data-stu-id="50258-193">Output</span></span> | <span data-ttu-id="50258-194">4</span><span class="sxs-lookup"><span data-stu-id="50258-194">4</span></span> | <span data-ttu-id="50258-195">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="50258-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="50258-196">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50258-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="50258-197">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="50258-197">**Header**</span></span> | <span data-ttu-id="50258-198">directml. h</span><span class="sxs-lookup"><span data-stu-id="50258-198">directml.h</span></span> |