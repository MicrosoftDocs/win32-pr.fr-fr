---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Effectue une convolution du *FilterTensor* avec *InputTensor*. Cet opérateur effectue une convolution ascendante sur les données quantifiées. Cet opérateur est mathématiquement équivalent à déquantifier les entrées, convolving, puis quantifier la sortie.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 5b98e1f57268cab70c2fb672991bce3d67419db8
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549783"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="2aa5f-105">Structure DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="2aa5f-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="2aa5f-106">Effectue une convolution du *FilterTensor* avec *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="2aa5f-107">Cet opérateur effectue une convolution ascendante sur les données quantifiées.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="2aa5f-108">Cet opérateur est mathématiquement équivalent à déquantifier les entrées, convolving, puis quantifier la sortie.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="2aa5f-109">Les fonctions de quantification linéaire utilisées par cet opérateur sont les fonctions de quantification linéaire</span><span class="sxs-lookup"><span data-stu-id="2aa5f-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="2aa5f-110">Dequantifier la fonction</span><span class="sxs-lookup"><span data-stu-id="2aa5f-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="2aa5f-111">Fonction quantifier</span><span class="sxs-lookup"><span data-stu-id="2aa5f-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="2aa5f-112">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="2aa5f-113">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="2aa5f-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2aa5f-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2aa5f-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a><span data-ttu-id="2aa5f-115">Membres</span><span class="sxs-lookup"><span data-stu-id="2aa5f-115">Members</span></span>

`InputTensor`

<span data-ttu-id="2aa5f-116">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2aa5f-117">Tenseur contenant les données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-117">A tensor containing the input data.</span></span> <span data-ttu-id="2aa5f-118">Les dimensions attendues du *InputTensor* sont `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="2aa5f-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="2aa5f-119">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2aa5f-120">Tenseur contenant les données d’échelle d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="2aa5f-121">Les dimensions attendues de `InputScaleTensor` sont `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="2aa5f-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="2aa5f-122">Cette valeur de mise à l’échelle est utilisée pour déquantifier les valeurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="2aa5f-123">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2aa5f-124">Tenseur facultatif contenant les données de point zéro en entrée.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="2aa5f-125">Les dimensions attendues du *InputZeroPointTensor* sont `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="2aa5f-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="2aa5f-126">Cette valeur de point zéro est utilisée pour déquantifier les valeurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="2aa5f-127">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2aa5f-128">Tenseur contenant les données de filtre.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-128">A tensor containing the filter data.</span></span> <span data-ttu-id="2aa5f-129">Les dimensions attendues du *FilterTensor* sont `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="2aa5f-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="2aa5f-130">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2aa5f-131">Tenseur contenant les données de mise à l’échelle du filtre.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="2aa5f-132">Les dimensions attendues du `FilterScaleTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, OutputChannelCount, 1, 1 }` si la quantification par canal est requise.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="2aa5f-133">Cette valeur de mise à l’échelle est utilisée pour déquantifier les valeurs de filtre.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="2aa5f-134">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2aa5f-135">Tenseur facultatif contenant les données de point zéro du filtre.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="2aa5f-136">Les dimensions attendues du *FilterZeroPointTensor* sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, OutputChannelCount, 1, 1 }` si la quantification par canal est requise.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="2aa5f-137">Cette valeur de point zéro est utilisée pour déquantifier les valeurs de filtre.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="2aa5f-138">Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2aa5f-139">Tenseur contenant les données de biais.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-139">A tensor containing the bias data.</span></span> <span data-ttu-id="2aa5f-140">Le tenseur Bias est un tenseur contenant des données qui sont diffusées dans le tenseur de sortie à la fin de la convolution qui est ajoutée au résultat.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="2aa5f-141">Les dimensions attendues du BiasTensor sont `{ 1, OutputChannelCount, 1, 1 }` pour le 4D.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="2aa5f-142">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2aa5f-143">Tenseur contenant les données d’échelle de sortie.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="2aa5f-144">Les dimensions attendues du OutputScaleTensor sont `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="2aa5f-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="2aa5f-145">Cette valeur d’échelle d’entrée est utilisée pour quantifier les valeurs de la convolution.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="2aa5f-146">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2aa5f-147">Tenseur facultatif contenant les données de point zéro du filtre.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="2aa5f-148">Les dimensions attendues du OutputZeroPointTensor sont `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="2aa5f-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="2aa5f-149">Cette valeur de point zéro d’entrée est utilisée pour quantifier les valeurs de sortie de la convolution.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="2aa5f-150">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2aa5f-151">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-151">A tensor to write the results to.</span></span> <span data-ttu-id="2aa5f-152">Les dimensions attendues du OutputTensor sont `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="2aa5f-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="2aa5f-153">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="2aa5f-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="2aa5f-154">Nombre de dimensions spatiales pour l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="2aa5f-155">Les dimensions spatiales sont les dimensions inférieures du filtre de convolution tenseur *FilterTensor*.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="2aa5f-156">Cette valeur détermine également la taille des tableaux *Strides*, *dilatations*, *StartPadding* et *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="2aa5f-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="2aa5f-157">Seule une valeur de 2 est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="2aa5f-158">Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-158">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2aa5f-159">Strides de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-159">The strides of the convolution operation.</span></span> <span data-ttu-id="2aa5f-160">Ces Strides sont appliqués au filtre de convolution.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="2aa5f-161">Ils sont distincts des Strides tenseur inclus dans [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="2aa5f-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="2aa5f-162">Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-162">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2aa5f-163">Dilatations de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="2aa5f-164">Les dilatations sont des Strides appliqués aux éléments du noyau de filtre.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="2aa5f-165">Cela a pour effet de simuler un plus grand noyau de filtre en remplissant les éléments de noyau de filtre internes avec des zéros.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="2aa5f-166">Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-166">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2aa5f-167">Valeurs de remplissage à appliquer au début de chaque dimension spatiale du filtre et tenseur d’entrée de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="2aa5f-168">Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2aa5f-168">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2aa5f-169">Valeurs de remplissage à appliquer à la fin de chaque dimension spatiale du filtre et tenseur d’entrée de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="2aa5f-170">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="2aa5f-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="2aa5f-171">Nombre de groupes dans lesquels diviser l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="2aa5f-172">*GroupCount* peut être utilisé pour obtenir une convolution de profondeur en définissant le *GroupCount* égal au nombre de canaux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="2aa5f-173">Cela divise la convolution en une convolution distincte par canal d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="2aa5f-174">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="2aa5f-174">Availability</span></span>
<span data-ttu-id="2aa5f-175">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="2aa5f-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2aa5f-176">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="2aa5f-176">Tensor constraints</span></span>
* <span data-ttu-id="2aa5f-177">*FilterTensor* et *FilterZeroPointTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="2aa5f-178">*InputTensor* et *InputZeroPointTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="2aa5f-179">*OutputTensor* et `OutputZeroPointTensor` doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="2aa5f-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="2aa5f-180">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="2aa5f-180">Tensor support</span></span>
| <span data-ttu-id="2aa5f-181">Tenseur</span><span class="sxs-lookup"><span data-stu-id="2aa5f-181">Tensor</span></span> | <span data-ttu-id="2aa5f-182">Type</span><span class="sxs-lookup"><span data-stu-id="2aa5f-182">Kind</span></span> | <span data-ttu-id="2aa5f-183">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="2aa5f-183">Supported dimension counts</span></span> | <span data-ttu-id="2aa5f-184">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="2aa5f-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="2aa5f-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="2aa5f-185">InputTensor</span></span> | <span data-ttu-id="2aa5f-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="2aa5f-186">Input</span></span> | <span data-ttu-id="2aa5f-187">4</span><span class="sxs-lookup"><span data-stu-id="2aa5f-187">4</span></span> | <span data-ttu-id="2aa5f-188">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="2aa5f-188">INT8, UINT8</span></span> |
| <span data-ttu-id="2aa5f-189">InputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="2aa5f-189">InputScaleTensor</span></span> | <span data-ttu-id="2aa5f-190">Entrée</span><span class="sxs-lookup"><span data-stu-id="2aa5f-190">Input</span></span> | <span data-ttu-id="2aa5f-191">4</span><span class="sxs-lookup"><span data-stu-id="2aa5f-191">4</span></span> | <span data-ttu-id="2aa5f-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="2aa5f-192">FLOAT32</span></span> |
| <span data-ttu-id="2aa5f-193">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="2aa5f-193">InputZeroPointTensor</span></span> | <span data-ttu-id="2aa5f-194">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="2aa5f-194">Optional input</span></span> | <span data-ttu-id="2aa5f-195">4</span><span class="sxs-lookup"><span data-stu-id="2aa5f-195">4</span></span> | <span data-ttu-id="2aa5f-196">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="2aa5f-196">INT8, UINT8</span></span> |
| <span data-ttu-id="2aa5f-197">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="2aa5f-197">FilterTensor</span></span> | <span data-ttu-id="2aa5f-198">Entrée</span><span class="sxs-lookup"><span data-stu-id="2aa5f-198">Input</span></span> | <span data-ttu-id="2aa5f-199">4</span><span class="sxs-lookup"><span data-stu-id="2aa5f-199">4</span></span> | <span data-ttu-id="2aa5f-200">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="2aa5f-200">INT8, UINT8</span></span> |
| <span data-ttu-id="2aa5f-201">FilterScaleTensor</span><span class="sxs-lookup"><span data-stu-id="2aa5f-201">FilterScaleTensor</span></span> | <span data-ttu-id="2aa5f-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="2aa5f-202">Input</span></span> | <span data-ttu-id="2aa5f-203">4</span><span class="sxs-lookup"><span data-stu-id="2aa5f-203">4</span></span> | <span data-ttu-id="2aa5f-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="2aa5f-204">FLOAT32</span></span> |
| <span data-ttu-id="2aa5f-205">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="2aa5f-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="2aa5f-206">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="2aa5f-206">Optional input</span></span> | <span data-ttu-id="2aa5f-207">4</span><span class="sxs-lookup"><span data-stu-id="2aa5f-207">4</span></span> | <span data-ttu-id="2aa5f-208">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="2aa5f-208">INT8, UINT8</span></span> |
| <span data-ttu-id="2aa5f-209">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="2aa5f-209">BiasTensor</span></span> | <span data-ttu-id="2aa5f-210">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="2aa5f-210">Optional input</span></span> | <span data-ttu-id="2aa5f-211">4</span><span class="sxs-lookup"><span data-stu-id="2aa5f-211">4</span></span> | <span data-ttu-id="2aa5f-212">INT32</span><span class="sxs-lookup"><span data-stu-id="2aa5f-212">INT32</span></span> |
| <span data-ttu-id="2aa5f-213">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="2aa5f-213">OutputScaleTensor</span></span> | <span data-ttu-id="2aa5f-214">Entrée</span><span class="sxs-lookup"><span data-stu-id="2aa5f-214">Input</span></span> | <span data-ttu-id="2aa5f-215">4</span><span class="sxs-lookup"><span data-stu-id="2aa5f-215">4</span></span> | <span data-ttu-id="2aa5f-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="2aa5f-216">FLOAT32</span></span> |
| <span data-ttu-id="2aa5f-217">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="2aa5f-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="2aa5f-218">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="2aa5f-218">Optional input</span></span> | <span data-ttu-id="2aa5f-219">4</span><span class="sxs-lookup"><span data-stu-id="2aa5f-219">4</span></span> | <span data-ttu-id="2aa5f-220">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="2aa5f-220">INT8, UINT8</span></span> |
| <span data-ttu-id="2aa5f-221">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="2aa5f-221">OutputTensor</span></span> | <span data-ttu-id="2aa5f-222">Output</span><span class="sxs-lookup"><span data-stu-id="2aa5f-222">Output</span></span> | <span data-ttu-id="2aa5f-223">4</span><span class="sxs-lookup"><span data-stu-id="2aa5f-223">4</span></span> | <span data-ttu-id="2aa5f-224">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="2aa5f-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="2aa5f-225">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2aa5f-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2aa5f-226">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="2aa5f-226">**Header**</span></span> | <span data-ttu-id="2aa5f-227">directml. h</span><span class="sxs-lookup"><span data-stu-id="2aa5f-227">directml.h</span></span> |