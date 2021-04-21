---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Rééchantillonne les éléments de la source vers le tenseur de destination, en utilisant les facteurs de mise à l’échelle pour calculer la taille du tenseur de destination. Vous pouvez utiliser le mode d’interpolation linéaire ou le voisin le plus proche.
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: ac98813e15ab3dac71a9f8395333160ce37778b0
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804060"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a><span data-ttu-id="f0e83-104">Structure DML_RESAMPLE1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="f0e83-104">DML_RESAMPLE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="f0e83-105">Rééchantillonne les éléments de la source vers le tenseur de destination, en utilisant les facteurs de mise à l’échelle pour calculer la taille du tenseur de destination.</span><span class="sxs-lookup"><span data-stu-id="f0e83-105">Resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size.</span></span> <span data-ttu-id="f0e83-106">Vous pouvez utiliser le mode d’interpolation linéaire ou le voisin le plus proche.</span><span class="sxs-lookup"><span data-stu-id="f0e83-106">You can use a linear or nearest-neighbor interpolation mode.</span></span> <span data-ttu-id="f0e83-107">L’opérateur prend en charge l’interpolation sur plusieurs dimensions, pas seulement 2D.</span><span class="sxs-lookup"><span data-stu-id="f0e83-107">The operator supports interpolation across multiple dimensions, not just 2D.</span></span> <span data-ttu-id="f0e83-108">Vous pouvez conserver la même taille spatiale, mais interpoler entre les canaux ou les lots.</span><span class="sxs-lookup"><span data-stu-id="f0e83-108">So you can keep the same spatial size, but interpolate across channels or across batches.</span></span> <span data-ttu-id="f0e83-109">La relation entre les coordonnées d’entrée et de sortie est la suivante.</span><span class="sxs-lookup"><span data-stu-id="f0e83-109">The relationship between the input and output coordinates is the following.</span></span>

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> <span data-ttu-id="f0e83-110">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f0e83-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f0e83-111">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="f0e83-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e83-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0e83-112">Syntax</span></span>
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a><span data-ttu-id="f0e83-113">Membres</span><span class="sxs-lookup"><span data-stu-id="f0e83-113">Members</span></span>

`InputTensor`

<span data-ttu-id="f0e83-114">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f0e83-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f0e83-115">Tenseur contenant les données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f0e83-115">The tensor containing the input data.</span></span>


`OutputTensor`

<span data-ttu-id="f0e83-116">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f0e83-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f0e83-117">Tenseur dans lequel écrire les données de sortie.</span><span class="sxs-lookup"><span data-stu-id="f0e83-117">The tensor to write the output data to.</span></span>


`InterpolationMode`

<span data-ttu-id="f0e83-118">Type : [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="f0e83-118">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="f0e83-119">Ce champ détermine le type d’interpolation utilisé pour choisir les pixels de sortie.</span><span class="sxs-lookup"><span data-stu-id="f0e83-119">This field determines the kind of interpolation used to choose output pixels.</span></span>

- <span data-ttu-id="f0e83-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span><span class="sxs-lookup"><span data-stu-id="f0e83-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span></span> <span data-ttu-id="f0e83-121">Utilise l’algorithme *voisin le plus proche* , qui choisit l’élément d’entrée le plus proche du centre de pixels correspondant pour chaque élément de sortie.</span><span class="sxs-lookup"><span data-stu-id="f0e83-121">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>

- <span data-ttu-id="f0e83-122">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="f0e83-122">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="f0e83-123">Utilise l’algorithme *Quadrilinear* , qui calcule l’élément de sortie en appliquant la moyenne pondérée des 2 éléments d’entrée voisins les plus proches par dimension.</span><span class="sxs-lookup"><span data-stu-id="f0e83-123">Uses the *Quadrilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="f0e83-124">Étant donné que les 4 dimensions peuvent être rééchantillonnées, la moyenne pondérée est calculée sur un total de 16 éléments d’entrée pour chaque élément de sortie.</span><span class="sxs-lookup"><span data-stu-id="f0e83-124">Since all 4 dimensions can be resampled, the weighted average is computed on a total of 16 input elements for each output element.</span></span>


`DimensionCount`

<span data-ttu-id="f0e83-125">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f0e83-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f0e83-126">Nombre de valeurs dans les tableaux dont les *échelles*, *InputPixelOffsets* et *OutputPixelOffsets* pointent.</span><span class="sxs-lookup"><span data-stu-id="f0e83-126">The number of values in the arrays that *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* point to.</span></span> <span data-ttu-id="f0e83-127">Cette valeur doit correspondre au nombre de dimensions de *InputTensor* et *OutputTensor*, qui doit être 4.</span><span class="sxs-lookup"><span data-stu-id="f0e83-127">This value must match the dimension count of *InputTensor* and *OutputTensor*, which has to be 4.</span></span>


`Scales`

<span data-ttu-id="f0e83-128">Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="f0e83-128">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="f0e83-129">Échelles à appliquer lors du rééchantillonnage de l’entrée, où Scales > 1 augmente l’image et met à l’échelle < 1 pour réduire l’image de cette dimension.</span><span class="sxs-lookup"><span data-stu-id="f0e83-129">The scales to apply when resampling the input, where scales > 1 scale up the image and scales < 1 scale down the image for that dimension.</span></span> <span data-ttu-id="f0e83-130">Notez que les échelles n’ont pas besoin d’être exactement `OutputSize / InputSize` .</span><span class="sxs-lookup"><span data-stu-id="f0e83-130">Note that the scales don't need to be exactly `OutputSize / InputSize`.</span></span> <span data-ttu-id="f0e83-131">Si l’entrée après la mise à l’échelle est supérieure à la limite de sortie, nous la découperons à la taille de sortie.</span><span class="sxs-lookup"><span data-stu-id="f0e83-131">If the input after scaling is larger than the output bound, then we crop it to the output size.</span></span> <span data-ttu-id="f0e83-132">En revanche, si l’entrée après la mise à l’échelle est plus petite que la limite de sortie, les bords de sortie sont bloqués.</span><span class="sxs-lookup"><span data-stu-id="f0e83-132">On the other hand, if the input after scaling is smaller than the output bound, the output edges are clamped.</span></span>


`InputPixelOffsets`

<span data-ttu-id="f0e83-133">Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="f0e83-133">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="f0e83-134">Offsets à appliquer aux pixels d’entrée avant le rééchantillonnage.</span><span class="sxs-lookup"><span data-stu-id="f0e83-134">The offsets to apply to the input pixels before resampling.</span></span> <span data-ttu-id="f0e83-135">Lorsque cette valeur est `0` , le coin supérieur gauche du pixel est utilisé à la place de son centre, ce qui n’entraîne généralement pas le résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="f0e83-135">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="f0e83-136">Pour rééchantillonner l’image à l’aide du Centre des pixels et pour avoir le même comportement que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), cette valeur doit être `0.5` .</span><span class="sxs-lookup"><span data-stu-id="f0e83-136">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `0.5`.</span></span>


`OutputPixelOffsets`

<span data-ttu-id="f0e83-137">Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="f0e83-137">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="f0e83-138">Offsets à appliquer aux pixels de sortie après le rééchantillonnage.</span><span class="sxs-lookup"><span data-stu-id="f0e83-138">The offsets to apply to the output pixels after resampling.</span></span> <span data-ttu-id="f0e83-139">Lorsque cette valeur est `0` , le coin supérieur gauche du pixel est utilisé à la place de son centre, ce qui n’entraîne généralement pas le résultat attendu.</span><span class="sxs-lookup"><span data-stu-id="f0e83-139">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="f0e83-140">Pour rééchantillonner l’image à l’aide du Centre des pixels et pour avoir le même comportement que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), cette valeur doit être `-0.5` .</span><span class="sxs-lookup"><span data-stu-id="f0e83-140">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `-0.5`.</span></span>


## <a name="remarks"></a><span data-ttu-id="f0e83-141">Notes </span><span class="sxs-lookup"><span data-stu-id="f0e83-141">Remarks</span></span>
<span data-ttu-id="f0e83-142">Lorsque les *InputPixelOffsets* sont définis sur 0,5 et que les *OutputPixelOffsets* sont définis sur-0,5, cet opérateur équivaut à [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="f0e83-142">When the *InputPixelOffsets* are set to 0.5, and the *OutputPixelOffsets* are set to -0.5, this operator is equivalent to [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="f0e83-143">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="f0e83-143">Availability</span></span>
<span data-ttu-id="f0e83-144">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="f0e83-144">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f0e83-145">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="f0e83-145">Tensor constraints</span></span>
<span data-ttu-id="f0e83-146">*InputTensor* et *OutputTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="f0e83-146">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f0e83-147">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="f0e83-147">Tensor support</span></span>
| <span data-ttu-id="f0e83-148">Tenseur</span><span class="sxs-lookup"><span data-stu-id="f0e83-148">Tensor</span></span> | <span data-ttu-id="f0e83-149">Type</span><span class="sxs-lookup"><span data-stu-id="f0e83-149">Kind</span></span> | <span data-ttu-id="f0e83-150">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="f0e83-150">Supported dimension counts</span></span> | <span data-ttu-id="f0e83-151">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0e83-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f0e83-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f0e83-152">InputTensor</span></span> | <span data-ttu-id="f0e83-153">Entrée</span><span class="sxs-lookup"><span data-stu-id="f0e83-153">Input</span></span> | <span data-ttu-id="f0e83-154">4</span><span class="sxs-lookup"><span data-stu-id="f0e83-154">4</span></span> | <span data-ttu-id="f0e83-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f0e83-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f0e83-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f0e83-156">OutputTensor</span></span> | <span data-ttu-id="f0e83-157">Output</span><span class="sxs-lookup"><span data-stu-id="f0e83-157">Output</span></span> | <span data-ttu-id="f0e83-158">4</span><span class="sxs-lookup"><span data-stu-id="f0e83-158">4</span></span> | <span data-ttu-id="f0e83-159">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f0e83-159">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="f0e83-160">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f0e83-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f0e83-161">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="f0e83-161">**Header**</span></span> | <span data-ttu-id="f0e83-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="f0e83-162">directml.h</span></span> |