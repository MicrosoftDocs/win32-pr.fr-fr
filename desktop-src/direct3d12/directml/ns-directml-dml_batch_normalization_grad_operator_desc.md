---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour la [normalisation du lot](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: 2b94ac1dcf389d424aaf74d615f36cdf7acc804c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550434"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="fe2ca-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="fe2ca-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="fe2ca-104">Calcule les dégradés de la rétropropagation pour la [normalisation du lot](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="fe2ca-104">Computes backpropagation gradients for [batch normalization](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span></span> <span data-ttu-id="fe2ca-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** effectue plusieurs calculs, qui sont détaillés dans les descriptions de sortie distinctes.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** performs multiple computations, which are detailed in the separate output descriptions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe2ca-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="fe2ca-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="fe2ca-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2ca-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe2ca-108">Syntax</span></span>
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a><span data-ttu-id="fe2ca-109">Membres</span><span class="sxs-lookup"><span data-stu-id="fe2ca-109">Members</span></span>

`InputTensor`

<span data-ttu-id="fe2ca-110">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe2ca-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe2ca-111">Tenseur contenant les données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-111">A tensor containing the input data.</span></span> <span data-ttu-id="fe2ca-112">Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *InputTensor* pour [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-112">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="fe2ca-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe2ca-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe2ca-114">Tenseur de dégradé entrant.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-114">The incoming gradient tensor.</span></span> <span data-ttu-id="fe2ca-115">Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="fe2ca-116">Ce tenseur doit avoir les mêmes tailles de dimension que *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-116">This tensor must have the same dimension sizes as *InputTensor*.</span></span>

`MeanTensor`

<span data-ttu-id="fe2ca-117">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe2ca-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe2ca-118">Tenseur contenant les données moyennes.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-118">A tensor containing the mean data.</span></span> <span data-ttu-id="fe2ca-119">Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *MeanTensor* pour [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-119">This is typically the same tensor that was provided as the *MeanTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="fe2ca-120">Toutes les dimensions qui n’ont pas la même taille que la dimension correspondante de *InputTensor* doivent avoir une taille de 1 afin qu’elles puissent être diffusées pour correspondre à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-120">Any dimensions that don't have the same size as the corresponding dimension of *InputTensor* must have a size of 1 so that they can be broadcast to match the input.</span></span>

<span data-ttu-id="fe2ca-121">Par exemple, les tailles suivantes sont acceptables.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-121">For example, the following sizes are acceptable.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

<span data-ttu-id="fe2ca-122">Voici une erreur dans la mesure où, pour être compatible avec la diffusion, toutes les dimensions qui ne correspondent pas doivent être de taille 1.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-122">The following is an error since, in order to be broadcast compatible, any dimensions that don't match must be size 1.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

<span data-ttu-id="fe2ca-123">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe2ca-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe2ca-124">Tenseur contenant les données de variance.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-124">A tensor containing the variance data.</span></span> <span data-ttu-id="fe2ca-125">Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *VarianceTensor* pour [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-125">This is typically the same tensor that was provided as the *VarianceTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="fe2ca-126">Ce tenseur doit avoir les mêmes tailles de dimension que *MeanTensor*.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-126">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`ScaleTensor`

<span data-ttu-id="fe2ca-127">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe2ca-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe2ca-128">Tenseur contenant les données d’échelle.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-128">A tensor containing the scale data.</span></span> <span data-ttu-id="fe2ca-129">Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *ScaleTensor* pour [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-129">This is typically the same tensor that was provided as the *ScaleTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="fe2ca-130">Ce tenseur doit avoir les mêmes tailles de dimension que *MeanTensor*.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-130">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`OutputGradientTensor`

<span data-ttu-id="fe2ca-131">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe2ca-131">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe2ca-132">Pour chaque valeur correspondante dans les entrées, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .</span><span class="sxs-lookup"><span data-stu-id="fe2ca-132">For every corresponding value in the inputs, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))`.</span></span>

<span data-ttu-id="fe2ca-133">Ce tenseur doit avoir les mêmes tailles de dimension que *InputTensor* / *InputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-133">This tensor must have the same dimension sizes as *InputTensor*/*InputGradientTensor*.</span></span>

`OutputScaleGradientTensor`

<span data-ttu-id="fe2ca-134">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe2ca-134">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe2ca-135">Ce tenseur doit avoir les mêmes tailles de dimension que *MeanTensor* / *VarianceTensor* / *ScaleTensor'*.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-135">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="fe2ca-136">Le calcul suivant est effectué ou chaque valeur correspondante dans les entrées.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-136">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

<span data-ttu-id="fe2ca-137">Le `sum` est calculé sur toutes les dimensions qui doivent être diffusées.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-137">The `sum` is computed across any dimensions that need to be broadcast.</span></span> <span data-ttu-id="fe2ca-138">Si aucune diffusion n’est nécessaire, aucune somme n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-138">If there is no broadcast needed, then no sum is needed.</span></span>

<span data-ttu-id="fe2ca-139">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-139">Here's an example.</span></span>

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

<span data-ttu-id="fe2ca-140">L’élément [0, **0, 0**, 0] de `OutputScaleGradientTensor` est la somme de `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` pour tous les éléments 90 (3 \* 5 \* 6) [[0, 2], **0**, [0,4], [0,5]].</span><span class="sxs-lookup"><span data-stu-id="fe2ca-140">Element [0, **0**, 0, 0] of `OutputScaleGradientTensor` is the sum of `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` for all 90 (3\*5\*6) elements [[0,2], **0**, [0,4], [0,5]].</span></span>

`OutputBiasGradientTensor`

<span data-ttu-id="fe2ca-141">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fe2ca-141">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fe2ca-142">Ce tenseur doit avoir les mêmes tailles de dimension que *MeanTensor* / *VarianceTensor* / *ScaleTensor'*.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-142">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="fe2ca-143">Le calcul suivant est effectué ou chaque valeur correspondante dans les entrées.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-143">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputBiasGradient = sum(InputGradient)`  

<span data-ttu-id="fe2ca-144">Le `sum` est calculé sur toutes les dimensions qui doivent être diffusées (Voir l’exemple pour *OutputScaleGradientTensor*).</span><span class="sxs-lookup"><span data-stu-id="fe2ca-144">The `sum` is computed across any dimensions that need to be broadcast (see the example for *OutputScaleGradientTensor*).</span></span> <span data-ttu-id="fe2ca-145">Si aucune diffusion n’est nécessaire, aucune somme n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-145">If there is no broadcast needed, then no sum is needed.</span></span>

`Epsilon`

<span data-ttu-id="fe2ca-146">Type : **[float](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe2ca-146">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe2ca-147">Petite valeur ajoutée à la variance pour éviter la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-147">A small value added to the variance to avoid zero.</span></span>

## <a name="availability"></a><span data-ttu-id="fe2ca-148">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="fe2ca-148">Availability</span></span>
<span data-ttu-id="fe2ca-149">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="fe2ca-149">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="fe2ca-150">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="fe2ca-150">Tensor constraints</span></span>
<span data-ttu-id="fe2ca-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor* et *VarianceTensor* doivent avoir le même *type de données* et *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="fe2ca-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="fe2ca-152">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="fe2ca-152">Tensor support</span></span>
| <span data-ttu-id="fe2ca-153">Tenseur</span><span class="sxs-lookup"><span data-stu-id="fe2ca-153">Tensor</span></span> | <span data-ttu-id="fe2ca-154">Type</span><span class="sxs-lookup"><span data-stu-id="fe2ca-154">Kind</span></span> | <span data-ttu-id="fe2ca-155">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="fe2ca-155">Supported dimension counts</span></span> | <span data-ttu-id="fe2ca-156">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe2ca-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fe2ca-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="fe2ca-157">InputTensor</span></span> | <span data-ttu-id="fe2ca-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="fe2ca-158">Input</span></span> | <span data-ttu-id="fe2ca-159">1 à 8</span><span class="sxs-lookup"><span data-stu-id="fe2ca-159">1 to 8</span></span> | <span data-ttu-id="fe2ca-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="fe2ca-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="fe2ca-161">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="fe2ca-161">InputGradientTensor</span></span> | <span data-ttu-id="fe2ca-162">Entrée</span><span class="sxs-lookup"><span data-stu-id="fe2ca-162">Input</span></span> | <span data-ttu-id="fe2ca-163">1 à 8</span><span class="sxs-lookup"><span data-stu-id="fe2ca-163">1 to 8</span></span> | <span data-ttu-id="fe2ca-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="fe2ca-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="fe2ca-165">MeanTensor</span><span class="sxs-lookup"><span data-stu-id="fe2ca-165">MeanTensor</span></span> | <span data-ttu-id="fe2ca-166">Entrée</span><span class="sxs-lookup"><span data-stu-id="fe2ca-166">Input</span></span> | <span data-ttu-id="fe2ca-167">1 à 8</span><span class="sxs-lookup"><span data-stu-id="fe2ca-167">1 to 8</span></span> | <span data-ttu-id="fe2ca-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="fe2ca-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="fe2ca-169">VarianceTensor</span><span class="sxs-lookup"><span data-stu-id="fe2ca-169">VarianceTensor</span></span> | <span data-ttu-id="fe2ca-170">Entrée</span><span class="sxs-lookup"><span data-stu-id="fe2ca-170">Input</span></span> | <span data-ttu-id="fe2ca-171">1 à 8</span><span class="sxs-lookup"><span data-stu-id="fe2ca-171">1 to 8</span></span> | <span data-ttu-id="fe2ca-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="fe2ca-172">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="fe2ca-173">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="fe2ca-173">ScaleTensor</span></span> | <span data-ttu-id="fe2ca-174">Entrée</span><span class="sxs-lookup"><span data-stu-id="fe2ca-174">Input</span></span> | <span data-ttu-id="fe2ca-175">1 à 8</span><span class="sxs-lookup"><span data-stu-id="fe2ca-175">1 to 8</span></span> | <span data-ttu-id="fe2ca-176">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="fe2ca-176">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="fe2ca-177">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="fe2ca-177">OutputGradientTensor</span></span> | <span data-ttu-id="fe2ca-178">Output</span><span class="sxs-lookup"><span data-stu-id="fe2ca-178">Output</span></span> | <span data-ttu-id="fe2ca-179">1 à 8</span><span class="sxs-lookup"><span data-stu-id="fe2ca-179">1 to 8</span></span> | <span data-ttu-id="fe2ca-180">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="fe2ca-180">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="fe2ca-181">OutputScaleGradientTensor</span><span class="sxs-lookup"><span data-stu-id="fe2ca-181">OutputScaleGradientTensor</span></span> | <span data-ttu-id="fe2ca-182">Output</span><span class="sxs-lookup"><span data-stu-id="fe2ca-182">Output</span></span> | <span data-ttu-id="fe2ca-183">1 à 8</span><span class="sxs-lookup"><span data-stu-id="fe2ca-183">1 to 8</span></span> | <span data-ttu-id="fe2ca-184">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="fe2ca-184">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="fe2ca-185">OutputBiasGradientTensor</span><span class="sxs-lookup"><span data-stu-id="fe2ca-185">OutputBiasGradientTensor</span></span> | <span data-ttu-id="fe2ca-186">Output</span><span class="sxs-lookup"><span data-stu-id="fe2ca-186">Output</span></span> | <span data-ttu-id="fe2ca-187">1 à 8</span><span class="sxs-lookup"><span data-stu-id="fe2ca-187">1 to 8</span></span> | <span data-ttu-id="fe2ca-188">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="fe2ca-188">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="fe2ca-189">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe2ca-189">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fe2ca-190">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="fe2ca-190">**Header**</span></span> | <span data-ttu-id="fe2ca-191">directml. h</span><span class="sxs-lookup"><span data-stu-id="fe2ca-191">directml.h</span></span> |