---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Effectue une opération d’alignement du ROI, comme décrit dans le [document R-CNN du masque](https://arxiv.org/abs/1703.06870). En résumé, l’opération extrait les cultures de l’image d’entrée tenseur et les redimensionne sur une taille de sortie commune spécifiée par les 2 dernières dimensions de *OutputTensor* à l’aide de la *InterpolationMode* spécifiée.
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: b9004a77d3b325dd3394d1a3a6b596e94997e9fd
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804013"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a><span data-ttu-id="97480-104">Structure DML_ROI_ALIGN_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="97480-104">DML_ROI_ALIGN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="97480-105">Effectue une opération d’alignement du ROI, comme décrit dans le [document R-CNN du masque](https://arxiv.org/abs/1703.06870).</span><span class="sxs-lookup"><span data-stu-id="97480-105">Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870).</span></span> <span data-ttu-id="97480-106">En résumé, l’opération extrait les cultures de l’image d’entrée tenseur et les redimensionne sur une taille de sortie commune spécifiée par les 2 dernières dimensions de *OutputTensor* à l’aide de la *InterpolationMode* spécifiée.</span><span class="sxs-lookup"><span data-stu-id="97480-106">In summary, the operation extracts crops from the input image tensor and resizes them to a common output size specified by the last 2 dimensions of *OutputTensor* using the specified *InterpolationMode*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97480-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="97480-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="97480-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="97480-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="97480-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97480-109">Syntax</span></span>

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a><span data-ttu-id="97480-110">Membres</span><span class="sxs-lookup"><span data-stu-id="97480-110">Members</span></span>

`InputTensor`

<span data-ttu-id="97480-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="97480-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="97480-112">Tenseur contenant les données d’entrée avec des dimensions `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="97480-112">A tensor containing the input data with dimensions `{ BatchCount, ChannelCount, InputHeight, InputWidth }`.</span></span>

`ROITensor`

<span data-ttu-id="97480-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="97480-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="97480-114">Tenseur contenant les données relatives aux régions d’intérêt (ROI).</span><span class="sxs-lookup"><span data-stu-id="97480-114">A tensor containing the regions of interest (ROI) data.</span></span> <span data-ttu-id="97480-115">Les dimensions autorisées de `ROITensor` sont `{ NumROIs, 4 }` , `{ 1, NumROIs, 4 }` ou `{ 1, 1, NumROIs, 4 }` .</span><span class="sxs-lookup"><span data-stu-id="97480-115">The allowed dimensions of `ROITensor` are `{ NumROIs, 4 }`, `{ 1, NumROIs, 4 }`, or `{ 1, 1, NumROIs, 4 }`.</span></span> <span data-ttu-id="97480-116">Pour chaque retour sur investissement, les valeurs sont les coordonnées de ses angles supérieur gauche et inférieur droit dans l’ordre `[x1, y1, x2, y2]` .</span><span class="sxs-lookup"><span data-stu-id="97480-116">For each ROI, the values will be the coordinates of its top-left and bottom-right corners in the order `[x1, y1, x2, y2]`.</span></span>

`BatchIndicesTensor`

<span data-ttu-id="97480-117">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="97480-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="97480-118">Tenseur contenant les index de lot à partir desquels extraire le ROIs.</span><span class="sxs-lookup"><span data-stu-id="97480-118">A tensor containing the batch indices to extract the ROIs from.</span></span> <span data-ttu-id="97480-119">Les dimensions autorisées de `BatchIndicesTensor` sont `{ NumROIs }` , `{ 1, NumROIs }` , `{ 1, 1, NumROIs }` ou `{ 1, 1, 1, NumROIs }` .</span><span class="sxs-lookup"><span data-stu-id="97480-119">The allowed dimensions of `BatchIndicesTensor` are `{ NumROIs }`, `{ 1, NumROIs }`, `{ 1, 1, NumROIs }`, or `{ 1, 1, 1, NumROIs }`.</span></span> <span data-ttu-id="97480-120">Chaque valeur est l’index d’un lot à partir de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="97480-120">Each value is the index of a batch from *InputTensor*.</span></span> <span data-ttu-id="97480-121">Le comportement n’est pas défini si les valeurs ne sont pas comprises dans la plage [0, BatchCount).</span><span class="sxs-lookup"><span data-stu-id="97480-121">The behavior is undefined if the values are not in the range [0, BatchCount).</span></span>

`OutputTensor`

<span data-ttu-id="97480-122">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="97480-122">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="97480-123">Tenseur contenant les données de sortie.</span><span class="sxs-lookup"><span data-stu-id="97480-123">A tensor containing the output data.</span></span> <span data-ttu-id="97480-124">Les dimensions attendues de *OutputTensor* sont `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="97480-124">The expected dimensions of *OutputTensor* are `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }`.</span></span>

`ReductionFunction`

<span data-ttu-id="97480-125">Type : **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span><span class="sxs-lookup"><span data-stu-id="97480-125">Type: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span></span>

<span data-ttu-id="97480-126">Fonction de réduction à utiliser lors de la réduction de tous les échantillons d’entrée qui contribuent à un élément de sortie ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) ou **DML_REDUCE_FUNCTION_MAX**).</span><span class="sxs-lookup"><span data-stu-id="97480-126">The reduction function to use when reducing across all input samples that contribute to an output element ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) or **DML_REDUCE_FUNCTION_MAX**).</span></span> <span data-ttu-id="97480-127">Le nombre d’échantillons d’entrée à réduire dans est limité par *MinimumSamplesPerOutput* et *MaximumSamplesPerOutput*.</span><span class="sxs-lookup"><span data-stu-id="97480-127">The number of input samples to reduce across is bounded by *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`InterpolationMode`

<span data-ttu-id="97480-128">Type : **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span><span class="sxs-lookup"><span data-stu-id="97480-128">Type: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span></span>

<span data-ttu-id="97480-129">Mode d’interpolation à utiliser lors du redimensionnement des régions.</span><span class="sxs-lookup"><span data-stu-id="97480-129">The interpolation mode to use when resizing the regions.</span></span>

- <span data-ttu-id="97480-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span><span class="sxs-lookup"><span data-stu-id="97480-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span></span> <span data-ttu-id="97480-131">Utilise l’algorithme *voisin le plus proche* , qui choisit l’élément d’entrée le plus proche du centre de pixels correspondant pour chaque élément de sortie.</span><span class="sxs-lookup"><span data-stu-id="97480-131">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>
- <span data-ttu-id="97480-132">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="97480-132">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="97480-133">Utilise l’algorithme *bilinéaire* , qui calcule l’élément de sortie en appliquant la moyenne pondérée des 2 éléments d’entrée voisins les plus proches par dimension.</span><span class="sxs-lookup"><span data-stu-id="97480-133">Uses the *Bilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="97480-134">Étant donné que seules 2 dimensions sont redimensionnées, la moyenne pondérée est calculée sur un total de 4 éléments d’entrée pour chaque élément de sortie.</span><span class="sxs-lookup"><span data-stu-id="97480-134">Since only 2 dimensions are resized, the weighted average is computed on a total of 4 input elements for each output element.</span></span>

`SpatialScaleX`

<span data-ttu-id="97480-135">Type : <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="97480-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="97480-136">Composant X (ou largeur) du facteur d’échelle pour multiplier les coordonnées *ROITensor* par afin de les rendre proportionnées à *InputHeight* et *InputWidth*.</span><span class="sxs-lookup"><span data-stu-id="97480-136">The X (or width) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="97480-137">Par exemple, si *ROITensor* contient des coordonnées normalisées (valeurs dans la plage [0.. 1]), *SpatialScaleX* aurait généralement la même valeur que *InputWidth*.</span><span class="sxs-lookup"><span data-stu-id="97480-137">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), then *SpatialScaleX* would usually have the same value as *InputWidth*.</span></span>

`SpatialScaleY`

<span data-ttu-id="97480-138">Type : <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="97480-138">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="97480-139">Le composant Y (ou hauteur) du facteur d’échelle pour multiplier les coordonnées *ROITensor* par afin de les rendre proportionnées à *InputHeight* et *InputWidth*.</span><span class="sxs-lookup"><span data-stu-id="97480-139">The Y (or height) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="97480-140">Par exemple, si *ROITensor* contient des coordonnées normalisées (valeurs dans la plage [0.. 1]), *SpatialScaleY* aurait généralement la même valeur que *InputHeight*.</span><span class="sxs-lookup"><span data-stu-id="97480-140">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), *SpatialScaleY* would usually have the same value as *InputHeight*.</span></span>

`OutOfBoundsInputValue`

<span data-ttu-id="97480-141">Type : <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="97480-141">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="97480-142">Valeur à lire à partir de *InputTensor* lorsque les rois sont en dehors des limites de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="97480-142">The value to read from *InputTensor* when the ROIs are outside the bounds of *InputTensor*.</span></span> <span data-ttu-id="97480-143">Cela peut se produire lorsque les valeurs obtenues après la mise à l’échelle de *ROITensor* par *SpatialScaleX* et *SpatialScaleY* sont supérieures à *InputWidth* et *InputHeight*.</span><span class="sxs-lookup"><span data-stu-id="97480-143">This can happen when the values obtained after scaling *ROITensor* by *SpatialScaleX* and *SpatialScaleY* are bigger than *InputWidth* and *InputHeight*.</span></span>

`MinimumSamplesPerOutput`

<span data-ttu-id="97480-144">Type : <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="97480-144">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="97480-145">Nombre minimal d’exemples d’entrée à utiliser pour chaque élément de sortie.</span><span class="sxs-lookup"><span data-stu-id="97480-145">The minimum number of input samples to use for every output element.</span></span> <span data-ttu-id="97480-146">L’opérateur calcule le nombre d’échantillons d’entrée en procédant de la `ScaledCropSize / OutputSize` sorte, puis le bride à *MinimumSamplesPerOutput* et *MaximumSamplesPerOutput*.</span><span class="sxs-lookup"><span data-stu-id="97480-146">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`MaximumSamplesPerOutput`

<span data-ttu-id="97480-147">Type : <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="97480-147">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="97480-148">Nombre maximal d’échantillons d’entrée à utiliser pour chaque élément de sortie.</span><span class="sxs-lookup"><span data-stu-id="97480-148">The maximum number of input samples to use for every output element.</span></span> <span data-ttu-id="97480-149">L’opérateur calcule le nombre d’échantillons d’entrée en procédant de la `ScaledCropSize / OutputSize` sorte, puis le bride à *MinimumSamplesPerOutput* et *MaximumSamplesPerOutput*.</span><span class="sxs-lookup"><span data-stu-id="97480-149">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

## <a name="availability"></a><span data-ttu-id="97480-150">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="97480-150">Availability</span></span>
<span data-ttu-id="97480-151">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="97480-151">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="97480-152">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="97480-152">Tensor constraints</span></span>
<span data-ttu-id="97480-153">*InputTensor*, *OutputTensor* et *ROITensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="97480-153">*InputTensor*, *OutputTensor*, and *ROITensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="97480-154">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="97480-154">Tensor support</span></span>
| <span data-ttu-id="97480-155">Tenseur</span><span class="sxs-lookup"><span data-stu-id="97480-155">Tensor</span></span> | <span data-ttu-id="97480-156">Type</span><span class="sxs-lookup"><span data-stu-id="97480-156">Kind</span></span> | <span data-ttu-id="97480-157">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="97480-157">Supported dimension counts</span></span> | <span data-ttu-id="97480-158">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="97480-158">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="97480-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="97480-159">InputTensor</span></span> | <span data-ttu-id="97480-160">Entrée</span><span class="sxs-lookup"><span data-stu-id="97480-160">Input</span></span> | <span data-ttu-id="97480-161">4</span><span class="sxs-lookup"><span data-stu-id="97480-161">4</span></span> | <span data-ttu-id="97480-162">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="97480-162">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="97480-163">ROITensor</span><span class="sxs-lookup"><span data-stu-id="97480-163">ROITensor</span></span> | <span data-ttu-id="97480-164">Entrée</span><span class="sxs-lookup"><span data-stu-id="97480-164">Input</span></span> | <span data-ttu-id="97480-165">2 à 4</span><span class="sxs-lookup"><span data-stu-id="97480-165">2 to 4</span></span> | <span data-ttu-id="97480-166">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="97480-166">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="97480-167">BatchIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="97480-167">BatchIndicesTensor</span></span> | <span data-ttu-id="97480-168">Entrée</span><span class="sxs-lookup"><span data-stu-id="97480-168">Input</span></span> | <span data-ttu-id="97480-169">1 à 4</span><span class="sxs-lookup"><span data-stu-id="97480-169">1 to 4</span></span> | <span data-ttu-id="97480-170">UINT32</span><span class="sxs-lookup"><span data-stu-id="97480-170">UINT32</span></span> |
| <span data-ttu-id="97480-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="97480-171">OutputTensor</span></span> | <span data-ttu-id="97480-172">Output</span><span class="sxs-lookup"><span data-stu-id="97480-172">Output</span></span> | <span data-ttu-id="97480-173">4</span><span class="sxs-lookup"><span data-stu-id="97480-173">4</span></span> | <span data-ttu-id="97480-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="97480-174">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="97480-175">Spécifications</span><span class="sxs-lookup"><span data-stu-id="97480-175">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="97480-176">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="97480-176">**Header**</span></span> | <span data-ttu-id="97480-177">directml. h</span><span class="sxs-lookup"><span data-stu-id="97480-177">directml.h</span></span> |