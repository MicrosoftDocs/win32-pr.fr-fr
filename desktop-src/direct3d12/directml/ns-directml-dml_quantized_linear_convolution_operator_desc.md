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
ms.openlocfilehash: 01193b19744f413690a3cb5ecccbb8fa60626cb0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106539785"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="cbd0d-105">Structure DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="cbd0d-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="cbd0d-106">Effectue une convolution du *FilterTensor* avec *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="cbd0d-107">Cet opérateur effectue une convolution ascendante sur les données quantifiées.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="cbd0d-108">Cet opérateur est mathématiquement équivalent à déquantifier les entrées, convolving, puis quantifier la sortie.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="cbd0d-109">Les fonctions de quantification linéaire utilisées par cet opérateur sont les fonctions de quantification linéaire</span><span class="sxs-lookup"><span data-stu-id="cbd0d-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="cbd0d-110">Dequantifier la fonction</span><span class="sxs-lookup"><span data-stu-id="cbd0d-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="cbd0d-111">Fonction quantifier</span><span class="sxs-lookup"><span data-stu-id="cbd0d-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="cbd0d-112">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="cbd0d-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="cbd0d-113">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="cbd0d-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd0d-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbd0d-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="cbd0d-115">Membres</span><span class="sxs-lookup"><span data-stu-id="cbd0d-115">Members</span></span>

`InputTensor`

<span data-ttu-id="cbd0d-116">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbd0d-117">Tenseur contenant les données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-117">A tensor containing the input data.</span></span> <span data-ttu-id="cbd0d-118">Les dimensions attendues du *InputTensor* sont `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="cbd0d-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="cbd0d-119">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbd0d-120">Tenseur contenant les données d’échelle d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="cbd0d-121">Les dimensions attendues de `InputScaleTensor` sont `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cbd0d-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cbd0d-122">Cette valeur de mise à l’échelle est utilisée pour déquantifier les valeurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="cbd0d-123">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbd0d-124">Tenseur facultatif contenant les données de point zéro en entrée.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="cbd0d-125">Les dimensions attendues du *InputZeroPointTensor* sont `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cbd0d-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cbd0d-126">Cette valeur de point zéro est utilisée pour déquantifier les valeurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="cbd0d-127">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbd0d-128">Tenseur contenant les données de filtre.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-128">A tensor containing the filter data.</span></span> <span data-ttu-id="cbd0d-129">Les dimensions attendues du *FilterTensor* sont `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="cbd0d-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="cbd0d-130">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbd0d-131">Tenseur contenant les données de mise à l’échelle du filtre.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="cbd0d-132">Les dimensions attendues du `FilterScaleTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, OutputChannelCount, 1, 1 }` si la quantification par canal est requise.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="cbd0d-133">Cette valeur de mise à l’échelle est utilisée pour déquantifier les valeurs de filtre.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="cbd0d-134">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbd0d-135">Tenseur facultatif contenant les données de point zéro du filtre.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="cbd0d-136">Les dimensions attendues du *FilterZeroPointTensor* sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, OutputChannelCount, 1, 1 }` si la quantification par canal est requise.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="cbd0d-137">Cette valeur de point zéro est utilisée pour déquantifier les valeurs de filtre.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="cbd0d-138">Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbd0d-139">Tenseur contenant les données de biais.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-139">A tensor containing the bias data.</span></span> <span data-ttu-id="cbd0d-140">Le tenseur Bias est un tenseur contenant des données qui sont diffusées dans le tenseur de sortie à la fin de la convolution qui est ajoutée au résultat.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="cbd0d-141">Les dimensions attendues du BiasTensor sont `{ 1, OutputChannelCount, 1, 1 }` pour le 4D.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="cbd0d-142">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbd0d-143">Tenseur contenant les données d’échelle de sortie.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="cbd0d-144">Les dimensions attendues du OutputScaleTensor sont `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cbd0d-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cbd0d-145">Cette valeur d’échelle d’entrée est utilisée pour quantifier les valeurs de la convolution.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="cbd0d-146">Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbd0d-147">Tenseur facultatif contenant les données de point zéro du filtre.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="cbd0d-148">Les dimensions attendues du OutputZeroPointTensor sont `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="cbd0d-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="cbd0d-149">Cette valeur de point zéro d’entrée est utilisée pour quantifier les valeurs de sortie de la convolution.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="cbd0d-150">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cbd0d-151">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-151">A tensor to write the results to.</span></span> <span data-ttu-id="cbd0d-152">Les dimensions attendues du OutputTensor sont `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="cbd0d-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="cbd0d-153">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cbd0d-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="cbd0d-154">Nombre de dimensions spatiales pour l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="cbd0d-155">Les dimensions spatiales sont les dimensions inférieures du filtre de convolution tenseur *FilterTensor*.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="cbd0d-156">Cette valeur détermine également la taille des tableaux *Strides*, *dilatations*, *StartPadding* et *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="cbd0d-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="cbd0d-157">Seule une valeur de 2 est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="cbd0d-158">Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-158">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cbd0d-159">Strides de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-159">The strides of the convolution operation.</span></span> <span data-ttu-id="cbd0d-160">Ces Strides sont appliqués au filtre de convolution.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="cbd0d-161">Ils sont distincts des Strides tenseur inclus dans [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="cbd0d-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="cbd0d-162">Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-162">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cbd0d-163">Dilatations de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="cbd0d-164">Les dilatations sont des Strides appliqués aux éléments du noyau de filtre.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="cbd0d-165">Cela a pour effet de simuler un plus grand noyau de filtre en remplissant les éléments de noyau de filtre internes avec des zéros.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="cbd0d-166">Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-166">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cbd0d-167">Valeurs de remplissage à appliquer au début de chaque dimension spatiale du filtre et tenseur d’entrée de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="cbd0d-168">Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cbd0d-168">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="cbd0d-169">Valeurs de remplissage à appliquer à la fin de chaque dimension spatiale du filtre et tenseur d’entrée de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="cbd0d-170">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cbd0d-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="cbd0d-171">Nombre de groupes dans lesquels diviser l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="cbd0d-172">*GroupCount* peut être utilisé pour obtenir une convolution de profondeur en définissant le *GroupCount* égal au nombre de canaux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="cbd0d-173">Cela divise la convolution en une convolution distincte par canal d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="cbd0d-174">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="cbd0d-174">Availability</span></span>
<span data-ttu-id="cbd0d-175">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="cbd0d-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cbd0d-176">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="cbd0d-176">Tensor constraints</span></span>
* <span data-ttu-id="cbd0d-177">*FilterTensor* et *FilterZeroPointTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="cbd0d-178">*InputTensor* et *InputZeroPointTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="cbd0d-179">*OutputTensor* et `OutputZeroPointTensor` doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="cbd0d-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cbd0d-180">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="cbd0d-180">Tensor support</span></span>
| <span data-ttu-id="cbd0d-181">Tenseur</span><span class="sxs-lookup"><span data-stu-id="cbd0d-181">Tensor</span></span> | <span data-ttu-id="cbd0d-182">Type</span><span class="sxs-lookup"><span data-stu-id="cbd0d-182">Kind</span></span> | <span data-ttu-id="cbd0d-183">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="cbd0d-183">Supported dimension counts</span></span> | <span data-ttu-id="cbd0d-184">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbd0d-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cbd0d-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="cbd0d-185">InputTensor</span></span> | <span data-ttu-id="cbd0d-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="cbd0d-186">Input</span></span> | <span data-ttu-id="cbd0d-187">4</span><span class="sxs-lookup"><span data-stu-id="cbd0d-187">4</span></span> | <span data-ttu-id="cbd0d-188">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cbd0d-188">INT8, UINT8</span></span> |
| <span data-ttu-id="cbd0d-189">InputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cbd0d-189">InputScaleTensor</span></span> | <span data-ttu-id="cbd0d-190">Entrée</span><span class="sxs-lookup"><span data-stu-id="cbd0d-190">Input</span></span> | <span data-ttu-id="cbd0d-191">4</span><span class="sxs-lookup"><span data-stu-id="cbd0d-191">4</span></span> | <span data-ttu-id="cbd0d-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cbd0d-192">FLOAT32</span></span> |
| <span data-ttu-id="cbd0d-193">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cbd0d-193">InputZeroPointTensor</span></span> | <span data-ttu-id="cbd0d-194">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="cbd0d-194">Optional input</span></span> | <span data-ttu-id="cbd0d-195">4</span><span class="sxs-lookup"><span data-stu-id="cbd0d-195">4</span></span> | <span data-ttu-id="cbd0d-196">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cbd0d-196">INT8, UINT8</span></span> |
| <span data-ttu-id="cbd0d-197">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="cbd0d-197">FilterTensor</span></span> | <span data-ttu-id="cbd0d-198">Entrée</span><span class="sxs-lookup"><span data-stu-id="cbd0d-198">Input</span></span> | <span data-ttu-id="cbd0d-199">4</span><span class="sxs-lookup"><span data-stu-id="cbd0d-199">4</span></span> | <span data-ttu-id="cbd0d-200">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cbd0d-200">INT8, UINT8</span></span> |
| <span data-ttu-id="cbd0d-201">FilterScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cbd0d-201">FilterScaleTensor</span></span> | <span data-ttu-id="cbd0d-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="cbd0d-202">Input</span></span> | <span data-ttu-id="cbd0d-203">4</span><span class="sxs-lookup"><span data-stu-id="cbd0d-203">4</span></span> | <span data-ttu-id="cbd0d-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cbd0d-204">FLOAT32</span></span> |
| <span data-ttu-id="cbd0d-205">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cbd0d-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="cbd0d-206">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="cbd0d-206">Optional input</span></span> | <span data-ttu-id="cbd0d-207">4</span><span class="sxs-lookup"><span data-stu-id="cbd0d-207">4</span></span> | <span data-ttu-id="cbd0d-208">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cbd0d-208">INT8, UINT8</span></span> |
| <span data-ttu-id="cbd0d-209">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="cbd0d-209">BiasTensor</span></span> | <span data-ttu-id="cbd0d-210">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="cbd0d-210">Optional input</span></span> | <span data-ttu-id="cbd0d-211">4</span><span class="sxs-lookup"><span data-stu-id="cbd0d-211">4</span></span> | <span data-ttu-id="cbd0d-212">INT32</span><span class="sxs-lookup"><span data-stu-id="cbd0d-212">INT32</span></span> |
| <span data-ttu-id="cbd0d-213">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cbd0d-213">OutputScaleTensor</span></span> | <span data-ttu-id="cbd0d-214">Entrée</span><span class="sxs-lookup"><span data-stu-id="cbd0d-214">Input</span></span> | <span data-ttu-id="cbd0d-215">4</span><span class="sxs-lookup"><span data-stu-id="cbd0d-215">4</span></span> | <span data-ttu-id="cbd0d-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="cbd0d-216">FLOAT32</span></span> |
| <span data-ttu-id="cbd0d-217">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="cbd0d-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="cbd0d-218">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="cbd0d-218">Optional input</span></span> | <span data-ttu-id="cbd0d-219">4</span><span class="sxs-lookup"><span data-stu-id="cbd0d-219">4</span></span> | <span data-ttu-id="cbd0d-220">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cbd0d-220">INT8, UINT8</span></span> |
| <span data-ttu-id="cbd0d-221">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cbd0d-221">OutputTensor</span></span> | <span data-ttu-id="cbd0d-222">Output</span><span class="sxs-lookup"><span data-stu-id="cbd0d-222">Output</span></span> | <span data-ttu-id="cbd0d-223">4</span><span class="sxs-lookup"><span data-stu-id="cbd0d-223">4</span></span> | <span data-ttu-id="cbd0d-224">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="cbd0d-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="cbd0d-225">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbd0d-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cbd0d-226">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="cbd0d-226">**Header**</span></span> | <span data-ttu-id="cbd0d-227">directml. h</span><span class="sxs-lookup"><span data-stu-id="cbd0d-227">directml.h</span></span> |