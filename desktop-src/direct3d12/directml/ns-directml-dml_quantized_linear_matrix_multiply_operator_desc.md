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
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417361"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="ca709-104">Structure DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="ca709-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="ca709-105">Exécute une fonction de multiplication de matrice sur des données quantifiées.</span><span class="sxs-lookup"><span data-stu-id="ca709-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="ca709-106">Cet opérateur est mathématiquement équivalent à déquantifier les entrées, à effectuer une multiplication de matrice, puis à quantifier la sortie.</span><span class="sxs-lookup"><span data-stu-id="ca709-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="ca709-107">Cet opérateur exige que la matrice multiplie les dizaines d’entrée par 4D qui sont mis en forme en tant que `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="ca709-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="ca709-108">L’opérateur de multiplication de matrice effectue un nombre BatchCount \* ChannelCount de multiplications de matrices indépendantes.</span><span class="sxs-lookup"><span data-stu-id="ca709-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="ca709-109">Par exemple, si *ATensor* a *une taille de* , et que BTensor a une taille de, `{ BatchCount, ChannelCount, M, K }` et que   `{ BatchCount, ChannelCount, K, N }` *OutputTensor* a une *taille* de, `{ BatchCount, ChannelCount, M, N }` alors l’opérateur de multiplication de matrice effectuera BatchCount \* ChannelCount des multiplications de matrices indépendantes {M, K} x {K, N} = {m, n}.</span><span class="sxs-lookup"><span data-stu-id="ca709-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="ca709-110">Dequantifier la fonction</span><span class="sxs-lookup"><span data-stu-id="ca709-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="ca709-111">Fonction quantifier</span><span class="sxs-lookup"><span data-stu-id="ca709-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="ca709-112">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ca709-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ca709-113">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ca709-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca709-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca709-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="ca709-115">Membres</span><span class="sxs-lookup"><span data-stu-id="ca709-115">Members</span></span>

`ATensor`

<span data-ttu-id="ca709-116">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca709-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca709-117">Tenseur contenant les données.</span><span class="sxs-lookup"><span data-stu-id="ca709-117">A tensor containing the A data.</span></span> <span data-ttu-id="ca709-118">Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="ca709-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="ca709-119">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca709-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca709-120">Tenseur contenant les données de mise à l’échelle ATensor.</span><span class="sxs-lookup"><span data-stu-id="ca709-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="ca709-121">Les dimensions attendues du `AScaleTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="ca709-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="ca709-122">Ces valeurs de mise à l’échelle sont utilisées pour déquantifier les valeurs A.</span><span class="sxs-lookup"><span data-stu-id="ca709-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="ca709-123">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca709-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca709-124">Tenseur facultatif contenant les données de point zéro *ATensor* .</span><span class="sxs-lookup"><span data-stu-id="ca709-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="ca709-125">Les dimensions attendues du AZeroPointTensor sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="ca709-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="ca709-126">Ces valeurs de zéro point sont utilisées pour déquantifier les valeurs de ATensor.</span><span class="sxs-lookup"><span data-stu-id="ca709-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="ca709-127">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca709-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca709-128">Tenseur contenant les données B.</span><span class="sxs-lookup"><span data-stu-id="ca709-128">A tensor containing the B data.</span></span> <span data-ttu-id="ca709-129">Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="ca709-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="ca709-130">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca709-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca709-131">Tenseur contenant les données de mise à l’échelle *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="ca709-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="ca709-132">Les dimensions attendues du `BScaleTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, 1, N }` si la quantification par colonne est requise.</span><span class="sxs-lookup"><span data-stu-id="ca709-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="ca709-133">Ces valeurs de mise à l’échelle sont utilisées pour déquantifier les valeurs *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="ca709-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="ca709-134">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca709-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca709-135">Tenseur facultatif contenant les données de point zéro *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="ca709-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="ca709-136">Les dimensions attendues du `BZeroPointTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, 1, N }` si la quantification par colonne est requise.</span><span class="sxs-lookup"><span data-stu-id="ca709-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="ca709-137">Ces valeurs de zéro point sont utilisées pour déquantifier les valeurs de *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="ca709-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="ca709-138">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca709-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca709-139">Tenseur contenant les données de mise à l’échelle du filtre.</span><span class="sxs-lookup"><span data-stu-id="ca709-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="ca709-140">Les dimensions attendues du `OutputScaleTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="ca709-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="ca709-141">Cette valeur de mise à l’échelle est utilisée pour déquantifier les valeurs de filtre.</span><span class="sxs-lookup"><span data-stu-id="ca709-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="ca709-142">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca709-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca709-143">Tenseur facultatif contenant les données de point zéro du filtre.</span><span class="sxs-lookup"><span data-stu-id="ca709-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="ca709-144">Les dimensions attendues du `OutputZeroPointTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="ca709-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="ca709-145">Cette valeur de point zéro est utilisée pour déquantifier les valeurs de filtre.</span><span class="sxs-lookup"><span data-stu-id="ca709-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="ca709-146">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ca709-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ca709-147">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="ca709-147">A tensor to write the results to.</span></span> <span data-ttu-id="ca709-148">Les dimensions de ce tenseur sont `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="ca709-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="ca709-149">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="ca709-149">Availability</span></span>
<span data-ttu-id="ca709-150">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="ca709-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ca709-151">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="ca709-151">Tensor constraints</span></span>
* <span data-ttu-id="ca709-152">*ATensor* et `AZeroPointTensor` doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="ca709-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="ca709-153">*BTensor* et `BZeroPointTensor` doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="ca709-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="ca709-154">*OutputTensor* et `OutputZeroPointTensor` doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="ca709-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ca709-155">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="ca709-155">Tensor support</span></span>
| <span data-ttu-id="ca709-156">Tenseur</span><span class="sxs-lookup"><span data-stu-id="ca709-156">Tensor</span></span> | <span data-ttu-id="ca709-157">Type</span><span class="sxs-lookup"><span data-stu-id="ca709-157">Kind</span></span> | <span data-ttu-id="ca709-158">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="ca709-158">Supported dimension counts</span></span> | <span data-ttu-id="ca709-159">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca709-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ca709-160">ATensor</span><span class="sxs-lookup"><span data-stu-id="ca709-160">ATensor</span></span> | <span data-ttu-id="ca709-161">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca709-161">Input</span></span> | <span data-ttu-id="ca709-162">4</span><span class="sxs-lookup"><span data-stu-id="ca709-162">4</span></span> | <span data-ttu-id="ca709-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ca709-163">INT8, UINT8</span></span> |
| <span data-ttu-id="ca709-164">AScaleTensor</span><span class="sxs-lookup"><span data-stu-id="ca709-164">AScaleTensor</span></span> | <span data-ttu-id="ca709-165">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca709-165">Input</span></span> | <span data-ttu-id="ca709-166">4</span><span class="sxs-lookup"><span data-stu-id="ca709-166">4</span></span> | <span data-ttu-id="ca709-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="ca709-167">FLOAT32</span></span> |
| <span data-ttu-id="ca709-168">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="ca709-168">AZeroPointTensor</span></span> | <span data-ttu-id="ca709-169">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="ca709-169">Optional input</span></span> | <span data-ttu-id="ca709-170">4</span><span class="sxs-lookup"><span data-stu-id="ca709-170">4</span></span> | <span data-ttu-id="ca709-171">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ca709-171">INT8, UINT8</span></span> |
| <span data-ttu-id="ca709-172">BTensor</span><span class="sxs-lookup"><span data-stu-id="ca709-172">BTensor</span></span> | <span data-ttu-id="ca709-173">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca709-173">Input</span></span> | <span data-ttu-id="ca709-174">4</span><span class="sxs-lookup"><span data-stu-id="ca709-174">4</span></span> | <span data-ttu-id="ca709-175">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ca709-175">INT8, UINT8</span></span> |
| <span data-ttu-id="ca709-176">BScaleTensor</span><span class="sxs-lookup"><span data-stu-id="ca709-176">BScaleTensor</span></span> | <span data-ttu-id="ca709-177">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca709-177">Input</span></span> | <span data-ttu-id="ca709-178">4</span><span class="sxs-lookup"><span data-stu-id="ca709-178">4</span></span> | <span data-ttu-id="ca709-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="ca709-179">FLOAT32</span></span> |
| <span data-ttu-id="ca709-180">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="ca709-180">BZeroPointTensor</span></span> | <span data-ttu-id="ca709-181">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="ca709-181">Optional input</span></span> | <span data-ttu-id="ca709-182">4</span><span class="sxs-lookup"><span data-stu-id="ca709-182">4</span></span> | <span data-ttu-id="ca709-183">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ca709-183">INT8, UINT8</span></span> |
| <span data-ttu-id="ca709-184">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="ca709-184">OutputScaleTensor</span></span> | <span data-ttu-id="ca709-185">Entrée</span><span class="sxs-lookup"><span data-stu-id="ca709-185">Input</span></span> | <span data-ttu-id="ca709-186">4</span><span class="sxs-lookup"><span data-stu-id="ca709-186">4</span></span> | <span data-ttu-id="ca709-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="ca709-187">FLOAT32</span></span> |
| <span data-ttu-id="ca709-188">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="ca709-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="ca709-189">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="ca709-189">Optional input</span></span> | <span data-ttu-id="ca709-190">4</span><span class="sxs-lookup"><span data-stu-id="ca709-190">4</span></span> | <span data-ttu-id="ca709-191">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ca709-191">INT8, UINT8</span></span> |
| <span data-ttu-id="ca709-192">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="ca709-192">OutputTensor</span></span> | <span data-ttu-id="ca709-193">Sortie</span><span class="sxs-lookup"><span data-stu-id="ca709-193">Output</span></span> | <span data-ttu-id="ca709-194">4</span><span class="sxs-lookup"><span data-stu-id="ca709-194">4</span></span> | <span data-ttu-id="ca709-195">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ca709-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="ca709-196">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ca709-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ca709-197">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="ca709-197">**Header**</span></span> | <span data-ttu-id="ca709-198">directml. h</span><span class="sxs-lookup"><span data-stu-id="ca709-198">directml.h</span></span> |