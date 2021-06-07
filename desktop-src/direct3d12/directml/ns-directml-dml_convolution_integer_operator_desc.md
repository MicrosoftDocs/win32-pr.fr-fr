---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Effectue une convolution du *FilterTensor* avec *InputTensor*. Cet opérateur effectue une convolution ascendante sur des données de type entier.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f4045598dd1aa050479fec8e5732fe5c0a4e77ee
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417312"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="e84fa-104">Structure DML_CONVOLUTION_INTEGER_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="e84fa-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e84fa-105">Effectue une convolution du *FilterTensor* avec *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="e84fa-105">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="e84fa-106">Cet opérateur effectue une convolution ascendante sur des données de type entier.</span><span class="sxs-lookup"><span data-stu-id="e84fa-106">This operator performs forward convolution on integer data.</span></span> <span data-ttu-id="e84fa-107">Des dizaines de points nuls facultatifs peuvent également être utilisés pour soustraire les valeurs de point zéro des tenseur d’entrée et de filtre.</span><span class="sxs-lookup"><span data-stu-id="e84fa-107">Optional zero point tensors can also be used to subtract zero point values from the input and filter tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e84fa-108">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e84fa-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e84fa-109">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e84fa-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e84fa-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e84fa-110">Syntax</span></span>
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```

## <a name="members"></a><span data-ttu-id="e84fa-111">Membres</span><span class="sxs-lookup"><span data-stu-id="e84fa-111">Members</span></span>

`InputTensor`

<span data-ttu-id="e84fa-112">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e84fa-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e84fa-113">Tenseur contenant les données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e84fa-113">A tensor containing the input data.</span></span> <span data-ttu-id="e84fa-114">Les dimensions attendues du *InputTensor* sont `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="e84fa-114">The expected dimensions of the *InputTensor* are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="e84fa-115">Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e84fa-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e84fa-116">Tenseur facultatif contenant les données de point zéro en entrée.</span><span class="sxs-lookup"><span data-stu-id="e84fa-116">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="e84fa-117">Les dimensions attendues du *InputZeroPointTensor* sont `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="e84fa-117">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span>


`FilterTensor`

<span data-ttu-id="e84fa-118">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e84fa-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e84fa-119">Tenseur contenant les données de filtre.</span><span class="sxs-lookup"><span data-stu-id="e84fa-119">A tensor containing the filter data.</span></span> <span data-ttu-id="e84fa-120">Les dimensions attendues du *FilterTensor* sont `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="e84fa-120">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="e84fa-121">Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e84fa-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e84fa-122">Tenseur facultatif contenant les données de point zéro du filtre.</span><span class="sxs-lookup"><span data-stu-id="e84fa-122">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="e84fa-123">Les dimensions attendues du *FilterZeroPointTensor* sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, OutputChannelCount, 1, 1 }` si la quantification par canal est requise.</span><span class="sxs-lookup"><span data-stu-id="e84fa-123">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per-channel quantization is required.</span></span>


`OutputTensor`

<span data-ttu-id="e84fa-124">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e84fa-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e84fa-125">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="e84fa-125">The tensor to write the results to.</span></span> <span data-ttu-id="e84fa-126">Les dimensions attendues du *OutputTensor* sont `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="e84fa-126">The expected dimensions of the *OutputTensor* are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="e84fa-127">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="e84fa-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="e84fa-128">Nombre de dimensions spatiales pour l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="e84fa-128">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="e84fa-129">Les dimensions spatiales sont les dimensions inférieures de la convolution *FilterTensor*.</span><span class="sxs-lookup"><span data-stu-id="e84fa-129">Spatial dimensions are the lower dimensions of the convolution *FilterTensor*.</span></span> <span data-ttu-id="e84fa-130">Cette valeur détermine également la taille des tableaux *Strides*, *dilatations*, *StartPadding* et *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="e84fa-130">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="e84fa-131">Seule une valeur de 2 est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e84fa-131">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="e84fa-132">Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e84fa-132">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e84fa-133">Tableau contenant les Strides de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="e84fa-133">An array containing the strides of the convolution operation.</span></span> <span data-ttu-id="e84fa-134">Ces Strides sont appliqués au filtre de convolution.</span><span class="sxs-lookup"><span data-stu-id="e84fa-134">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="e84fa-135">Ils sont distincts des Strides tenseur inclus dans [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="e84fa-135">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="e84fa-136">Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e84fa-136">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e84fa-137">Tableau contenant les dilatations de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="e84fa-137">An array containing the dilations of the convolution operation.</span></span> <span data-ttu-id="e84fa-138">Les dilatations sont des Strides appliqués aux éléments du noyau de filtre.</span><span class="sxs-lookup"><span data-stu-id="e84fa-138">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="e84fa-139">Cela a pour effet de simuler un plus grand noyau de filtre en remplissant les éléments de noyau de filtre internes avec des zéros.</span><span class="sxs-lookup"><span data-stu-id="e84fa-139">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="e84fa-140">Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e84fa-140">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e84fa-141">Tableau contenant les valeurs de remplissage à appliquer au début de chaque dimension spatiale du filtre et tenseur d’entrée de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="e84fa-141">An array containing the padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="e84fa-142">Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e84fa-142">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e84fa-143">Tableau contenant les valeurs de remplissage à appliquer à la fin de chaque dimension spatiale du filtre et tenseur d’entrée de l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="e84fa-143">An array containing the padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="e84fa-144">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="e84fa-144">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="e84fa-145">Nombre de groupes dans lesquels diviser l’opération de convolution.</span><span class="sxs-lookup"><span data-stu-id="e84fa-145">The number of groups which to divide the convolution operation up into.</span></span> <span data-ttu-id="e84fa-146">*GroupCount* peut être utilisé pour obtenir une convolution de profondeur en définissant le *GroupCount* égal au nombre de canaux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e84fa-146">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="e84fa-147">Cela divise la convolution en une convolution distincte par canal d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e84fa-147">This divides the convolution up into a separate convolution per input channel.</span></span>

## <a name="availability"></a><span data-ttu-id="e84fa-148">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="e84fa-148">Availability</span></span>
<span data-ttu-id="e84fa-149">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="e84fa-149">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e84fa-150">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="e84fa-150">Tensor constraints</span></span>
* <span data-ttu-id="e84fa-151">*FilterTensor* et *FilterZeroPointTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="e84fa-151">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="e84fa-152">*InputTensor* et *InputZeroPointTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="e84fa-152">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e84fa-153">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="e84fa-153">Tensor support</span></span>
| <span data-ttu-id="e84fa-154">Tenseur</span><span class="sxs-lookup"><span data-stu-id="e84fa-154">Tensor</span></span> | <span data-ttu-id="e84fa-155">Type</span><span class="sxs-lookup"><span data-stu-id="e84fa-155">Kind</span></span> | <span data-ttu-id="e84fa-156">Dimensions</span><span class="sxs-lookup"><span data-stu-id="e84fa-156">Dimensions</span></span> | <span data-ttu-id="e84fa-157">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="e84fa-157">Supported dimension counts</span></span> | <span data-ttu-id="e84fa-158">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="e84fa-158">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="e84fa-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="e84fa-159">InputTensor</span></span> | <span data-ttu-id="e84fa-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="e84fa-160">Input</span></span> | <span data-ttu-id="e84fa-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="e84fa-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="e84fa-162">4</span><span class="sxs-lookup"><span data-stu-id="e84fa-162">4</span></span> | <span data-ttu-id="e84fa-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="e84fa-163">INT8, UINT8</span></span> |
| <span data-ttu-id="e84fa-164">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="e84fa-164">InputZeroPointTensor</span></span> | <span data-ttu-id="e84fa-165">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="e84fa-165">Optional input</span></span> | <span data-ttu-id="e84fa-166">{1, 1, 1,1}</span><span class="sxs-lookup"><span data-stu-id="e84fa-166">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="e84fa-167">4</span><span class="sxs-lookup"><span data-stu-id="e84fa-167">4</span></span> | <span data-ttu-id="e84fa-168">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="e84fa-168">INT8, UINT8</span></span> |
| <span data-ttu-id="e84fa-169">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="e84fa-169">FilterTensor</span></span> | <span data-ttu-id="e84fa-170">Entrée</span><span class="sxs-lookup"><span data-stu-id="e84fa-170">Input</span></span> | <span data-ttu-id="e84fa-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span><span class="sxs-lookup"><span data-stu-id="e84fa-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span></span> | <span data-ttu-id="e84fa-172">4</span><span class="sxs-lookup"><span data-stu-id="e84fa-172">4</span></span> | <span data-ttu-id="e84fa-173">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="e84fa-173">INT8, UINT8</span></span> |
| <span data-ttu-id="e84fa-174">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="e84fa-174">FilterZeroPointTensor</span></span> | <span data-ttu-id="e84fa-175">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="e84fa-175">Optional input</span></span> | <span data-ttu-id="e84fa-176">{1, FilterZeroPointChannelCount, 1,1}</span><span class="sxs-lookup"><span data-stu-id="e84fa-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span></span> | <span data-ttu-id="e84fa-177">4</span><span class="sxs-lookup"><span data-stu-id="e84fa-177">4</span></span> | <span data-ttu-id="e84fa-178">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="e84fa-178">INT8, UINT8</span></span> |
| <span data-ttu-id="e84fa-179">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e84fa-179">OutputTensor</span></span> | <span data-ttu-id="e84fa-180">Sortie</span><span class="sxs-lookup"><span data-stu-id="e84fa-180">Output</span></span> | <span data-ttu-id="e84fa-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="e84fa-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="e84fa-182">4</span><span class="sxs-lookup"><span data-stu-id="e84fa-182">4</span></span> | <span data-ttu-id="e84fa-183">INT32</span><span class="sxs-lookup"><span data-stu-id="e84fa-183">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="e84fa-184">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e84fa-184">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e84fa-185">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="e84fa-185">**Header**</span></span> | <span data-ttu-id="e84fa-186">directml. h</span><span class="sxs-lookup"><span data-stu-id="e84fa-186">directml.h</span></span> |