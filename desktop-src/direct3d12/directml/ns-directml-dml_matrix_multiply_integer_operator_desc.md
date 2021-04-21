---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Exécute une fonction de multiplication de matrice sur des données de type entier.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802837"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="ded4b-103">Structure DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="ded4b-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="ded4b-104">Exécute une fonction de multiplication de matrice sur des données de type entier.</span><span class="sxs-lookup"><span data-stu-id="ded4b-104">Performs a matrix multiplication function on integer data.</span></span>

<span data-ttu-id="ded4b-105">Cet opérateur exige que la matrice multiplie les dizaines d’entrée par 4D, qui sont mis en forme en tant que `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="ded4b-105">This operator requires the matrix multiply input tensors to be 4D, which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="ded4b-106">L’opérateur de multiplication de matrice effectue un nombre BatchCount \* ChannelCount de multiplications de matrices indépendantes.</span><span class="sxs-lookup"><span data-stu-id="ded4b-106">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span>

<span data-ttu-id="ded4b-107">Par exemple, si *ATensor* a *une taille de* , et que BTensor a une taille de, `{ BatchCount, ChannelCount, M, K }` et que   `{ BatchCount, ChannelCount, K, N }` *OutputTensor* a une *taille* de, `{ BatchCount, ChannelCount, M, N }` alors l’opérateur de multiplication de matrice effectuera BatchCount \* ChannelCount des multiplications de matrices indépendantes {M, K} x {K, N} = {m, n}.</span><span class="sxs-lookup"><span data-stu-id="ded4b-107">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ded4b-108">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ded4b-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ded4b-109">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ded4b-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ded4b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ded4b-110">Syntax</span></span>
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="ded4b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="ded4b-111">Members</span></span>

`ATensor`

<span data-ttu-id="ded4b-112">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ded4b-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ded4b-113">Tenseur contenant les données.</span><span class="sxs-lookup"><span data-stu-id="ded4b-113">A tensor containing the A data.</span></span> <span data-ttu-id="ded4b-114">Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="ded4b-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AZeroPointTensor`

<span data-ttu-id="ded4b-115">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ded4b-115">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ded4b-116">Tenseur facultatif contenant les données de point zéro ATensor.</span><span class="sxs-lookup"><span data-stu-id="ded4b-116">An optional tensor containing the ATensor zero point data.</span></span> <span data-ttu-id="ded4b-117">Les dimensions attendues du `AZeroPointTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise.</span><span class="sxs-lookup"><span data-stu-id="ded4b-117">The expected dimensions of the `AZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required.</span></span> <span data-ttu-id="ded4b-118">Ces valeurs de zéro point sont utilisées pour déquantifier les valeurs de *ATensor* .</span><span class="sxs-lookup"><span data-stu-id="ded4b-118">These zero point values are used for dequantizing the *ATensor* values.</span></span>


`BTensor`

<span data-ttu-id="ded4b-119">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ded4b-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ded4b-120">Tenseur contenant les données B.</span><span class="sxs-lookup"><span data-stu-id="ded4b-120">A tensor containing the B data.</span></span> <span data-ttu-id="ded4b-121">Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="ded4b-121">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BZeroPointTensor`

<span data-ttu-id="ded4b-122">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ded4b-122">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ded4b-123">Tenseur facultatif contenant les données de point zéro *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="ded4b-123">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="ded4b-124">Les dimensions attendues du `BZeroPointTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, 1, N }` si la quantification par colonne est requise.</span><span class="sxs-lookup"><span data-stu-id="ded4b-124">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="ded4b-125">Ces valeurs de zéro point sont utilisées pour déquantifier les valeurs de BTensor.</span><span class="sxs-lookup"><span data-stu-id="ded4b-125">These zero point values are used for dequantizing the BTensor values.</span></span>


`OutputTensor`

<span data-ttu-id="ded4b-126">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ded4b-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ded4b-127">Tenseur avec lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="ded4b-127">A tensor with which to write the results to.</span></span> <span data-ttu-id="ded4b-128">Les dimensions de ce tenseur sont `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="ded4b-128">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="ded4b-129">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="ded4b-129">Availability</span></span>
<span data-ttu-id="ded4b-130">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="ded4b-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ded4b-131">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="ded4b-131">Tensor constraints</span></span>
* <span data-ttu-id="ded4b-132">*ATensor* et `AZeroPointTensor` doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="ded4b-132">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="ded4b-133">*BTensor* et `BZeroPointTensor` doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="ded4b-133">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ded4b-134">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="ded4b-134">Tensor support</span></span>
| <span data-ttu-id="ded4b-135">Tenseur</span><span class="sxs-lookup"><span data-stu-id="ded4b-135">Tensor</span></span> | <span data-ttu-id="ded4b-136">Type</span><span class="sxs-lookup"><span data-stu-id="ded4b-136">Kind</span></span> | <span data-ttu-id="ded4b-137">Dimensions</span><span class="sxs-lookup"><span data-stu-id="ded4b-137">Dimensions</span></span> | <span data-ttu-id="ded4b-138">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="ded4b-138">Supported dimension counts</span></span> | <span data-ttu-id="ded4b-139">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="ded4b-139">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="ded4b-140">ATensor</span><span class="sxs-lookup"><span data-stu-id="ded4b-140">ATensor</span></span> | <span data-ttu-id="ded4b-141">Entrée</span><span class="sxs-lookup"><span data-stu-id="ded4b-141">Input</span></span> | <span data-ttu-id="ded4b-142">{BatchCount, ChannelCount, M, K}</span><span class="sxs-lookup"><span data-stu-id="ded4b-142">{ BatchCount, ChannelCount, M, K }</span></span> | <span data-ttu-id="ded4b-143">4</span><span class="sxs-lookup"><span data-stu-id="ded4b-143">4</span></span> | <span data-ttu-id="ded4b-144">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ded4b-144">INT8, UINT8</span></span> |
| <span data-ttu-id="ded4b-145">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="ded4b-145">AZeroPointTensor</span></span> | <span data-ttu-id="ded4b-146">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="ded4b-146">Optional input</span></span> | <span data-ttu-id="ded4b-147">{1, 1, AZeroPointCount, 1}</span><span class="sxs-lookup"><span data-stu-id="ded4b-147">{ 1, 1, AZeroPointCount, 1 }</span></span> | <span data-ttu-id="ded4b-148">4</span><span class="sxs-lookup"><span data-stu-id="ded4b-148">4</span></span> | <span data-ttu-id="ded4b-149">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ded4b-149">INT8, UINT8</span></span> |
| <span data-ttu-id="ded4b-150">BTensor</span><span class="sxs-lookup"><span data-stu-id="ded4b-150">BTensor</span></span> | <span data-ttu-id="ded4b-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="ded4b-151">Input</span></span> | <span data-ttu-id="ded4b-152">{BatchCount, ChannelCount, K, N}</span><span class="sxs-lookup"><span data-stu-id="ded4b-152">{ BatchCount, ChannelCount, K, N }</span></span> | <span data-ttu-id="ded4b-153">4</span><span class="sxs-lookup"><span data-stu-id="ded4b-153">4</span></span> | <span data-ttu-id="ded4b-154">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ded4b-154">INT8, UINT8</span></span> |
| <span data-ttu-id="ded4b-155">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="ded4b-155">BZeroPointTensor</span></span> | <span data-ttu-id="ded4b-156">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="ded4b-156">Optional input</span></span> | <span data-ttu-id="ded4b-157">{1, 1, 1, BZeroPointCount}</span><span class="sxs-lookup"><span data-stu-id="ded4b-157">{ 1, 1, 1, BZeroPointCount }</span></span> | <span data-ttu-id="ded4b-158">4</span><span class="sxs-lookup"><span data-stu-id="ded4b-158">4</span></span> | <span data-ttu-id="ded4b-159">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ded4b-159">INT8, UINT8</span></span> |
| <span data-ttu-id="ded4b-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="ded4b-160">OutputTensor</span></span> | <span data-ttu-id="ded4b-161">Output</span><span class="sxs-lookup"><span data-stu-id="ded4b-161">Output</span></span> | <span data-ttu-id="ded4b-162">{BatchCount, ChannelCount, M, N}</span><span class="sxs-lookup"><span data-stu-id="ded4b-162">{ BatchCount, ChannelCount, M, N }</span></span> | <span data-ttu-id="ded4b-163">4</span><span class="sxs-lookup"><span data-stu-id="ded4b-163">4</span></span> | <span data-ttu-id="ded4b-164">INT32</span><span class="sxs-lookup"><span data-stu-id="ded4b-164">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="ded4b-165">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ded4b-165">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ded4b-166">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="ded4b-166">**Header**</span></span> | <span data-ttu-id="ded4b-167">directml. h</span><span class="sxs-lookup"><span data-stu-id="ded4b-167">directml.h</span></span> |