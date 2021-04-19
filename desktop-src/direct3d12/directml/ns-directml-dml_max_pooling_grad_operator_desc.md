---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour le regroupement Max (voir [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
helpviewer_keywords:
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- DML_MAX_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_MAX_POOLING_GRAD_OPERATOR_DESC, DML_MAX_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: b7314cb6b9456d9ac9f99e90100085e86f88ffd9
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106524783"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="6977c-103">Structure DML_MAX_POOLING_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="6977c-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="6977c-104">Calcule les dégradés de la rétropropagation pour le regroupement Max (voir [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span><span class="sxs-lookup"><span data-stu-id="6977c-104">Computes backpropagation gradients for max pooling (see [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span></span>

<span data-ttu-id="6977c-105">Imaginez un **DML_MAX_POOLING2_OPERATOR_DESC** 2x2 sans remplissage ni dilatations et une Stride de 1, qui effectue les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="6977c-105">Consider a 2x2 **DML_MAX_POOLING2_OPERATOR_DESC** without padding nor dilations and a stride of 1, which performs the following.</span></span>

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

<span data-ttu-id="6977c-106">Le plus grand élément de chaque fenêtre 2x2 dans le tenseur d’entrée génère un élément de la sortie.</span><span class="sxs-lookup"><span data-stu-id="6977c-106">The largest element of each 2x2 window in the input tensor produces one element of the output.</span></span> <span data-ttu-id="6977c-107">Voici un exemple de la sortie de **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, en fonction de paramètres similaires.</span><span class="sxs-lookup"><span data-stu-id="6977c-107">Below is an example of the output of **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, given similar parameters.</span></span>

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

<span data-ttu-id="6977c-108">En effet, cet opérateur utilise *InputTensor* pour déterminer l’index du plus grand élément de chaque fenêtre et distribue les valeurs de *InputGradientTensor* dans le *OutputGradientTensor* en fonction de ces index.</span><span class="sxs-lookup"><span data-stu-id="6977c-108">In effect, this operator uses the *InputTensor* to determine the index of the largest element from each window, and distributes the values of *InputGradientTensor* into the *OutputGradientTensor* based on these indices.</span></span> <span data-ttu-id="6977c-109">Lorsque les index se chevauchent, les valeurs sont additionnées.</span><span class="sxs-lookup"><span data-stu-id="6977c-109">Where indices overlap, the values are summed.</span></span> <span data-ttu-id="6977c-110">Tous les éléments de sortie non référencés sont mis à zéro.</span><span class="sxs-lookup"><span data-stu-id="6977c-110">Any unreferenced output elements are zeroed.</span></span>

<span data-ttu-id="6977c-111">Dans le cas d’un lien (où plusieurs éléments d’une fenêtre ont la même valeur maximale), l’élément avec l’index d’élément logique le plus bas est choisi.</span><span class="sxs-lookup"><span data-stu-id="6977c-111">In the case of a tie (where more than one element in a window has the same maximum value), the element with the lowest logical element index is chosen.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6977c-112">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="6977c-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="6977c-113">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="6977c-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6977c-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6977c-114">Syntax</span></span>

```cpp
struct DML_MAX_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  _Field_size_(DimensionCount) const UINT* Dilations;
};
```

## <a name="members"></a><span data-ttu-id="6977c-115">Membres</span><span class="sxs-lookup"><span data-stu-id="6977c-115">Members</span></span>

`InputTensor`

<span data-ttu-id="6977c-116">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6977c-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6977c-117">La fonctionnalité d’entrée tenseur.</span><span class="sxs-lookup"><span data-stu-id="6977c-117">The input feature tensor.</span></span> <span data-ttu-id="6977c-118">Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *InputTensor* pour [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="6977c-118">This is typically the same tensor that was provided as the *InputTensor* to [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="6977c-119">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6977c-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6977c-120">Tenseur de dégradé entrant.</span><span class="sxs-lookup"><span data-stu-id="6977c-120">The incoming gradient tensor.</span></span> <span data-ttu-id="6977c-121">Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente.</span><span class="sxs-lookup"><span data-stu-id="6977c-121">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="6977c-122">En général, ce tenseur a la même taille que la *sortie* de la [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) correspondante dans la passe de transfert.</span><span class="sxs-lookup"><span data-stu-id="6977c-122">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="6977c-123">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6977c-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6977c-124">Tenseur de sortie contenant les dégradés de la page.</span><span class="sxs-lookup"><span data-stu-id="6977c-124">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="6977c-125">En général, ce tenseur a la même taille que l' *entrée* de la [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) correspondante dans la passe en avant.</span><span class="sxs-lookup"><span data-stu-id="6977c-125">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="6977c-126">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="6977c-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="6977c-127">Nombre d’éléments dans les tableaux *Strides*, *Windows*, *StartPadding*, *EndPadding* et *dilatations* .</span><span class="sxs-lookup"><span data-stu-id="6977c-127">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, *EndPadding*, and *Dilations* arrays.</span></span> <span data-ttu-id="6977c-128">Cette valeur doit être égale au nombre de dimensions spatiales (InputTensor DimensionCount-2).</span><span class="sxs-lookup"><span data-stu-id="6977c-128">This value must equal the spatial dimension count (InputTensor's DimensionCount - 2).</span></span> <span data-ttu-id="6977c-129">Étant donné que cet opérateur ne prend en charge que les dizaines de 4D, la seule valeur valide pour ce paramètre est 2.</span><span class="sxs-lookup"><span data-stu-id="6977c-129">As this operator only supports 4D tensors, the only valid value for this parameter is 2.</span></span>

`Strides`

<span data-ttu-id="6977c-130">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="6977c-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="6977c-131">Consultez la section *Strides* dans [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="6977c-131">See *Strides* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`WindowSize`

<span data-ttu-id="6977c-132">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="6977c-132">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="6977c-133">Consultez *Windows* dans [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="6977c-133">See *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`StartPadding`

<span data-ttu-id="6977c-134">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="6977c-134">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="6977c-135">Consultez *StartPadding* dans [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="6977c-135">See *StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`EndPadding`

<span data-ttu-id="6977c-136">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="6977c-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="6977c-137">Consultez *EndPadding* dans [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="6977c-137">See *EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`Dilations`

<span data-ttu-id="6977c-138">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="6977c-138">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="6977c-139">Consultez les *dilatations* dans [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="6977c-139">See *Dilations* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

## <a name="availability"></a><span data-ttu-id="6977c-140">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="6977c-140">Availability</span></span>
<span data-ttu-id="6977c-141">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="6977c-141">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6977c-142">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="6977c-142">Tensor constraints</span></span>
* <span data-ttu-id="6977c-143">*InputTensor* et *OutputGradientTensor* doivent avoir la même *taille*.</span><span class="sxs-lookup"><span data-stu-id="6977c-143">*InputTensor* and *OutputGradientTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="6977c-144">*InputGradientTensor*, *InputTensor* et *OutputGradientTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="6977c-144">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6977c-145">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="6977c-145">Tensor support</span></span>
| <span data-ttu-id="6977c-146">Tenseur</span><span class="sxs-lookup"><span data-stu-id="6977c-146">Tensor</span></span> | <span data-ttu-id="6977c-147">Type</span><span class="sxs-lookup"><span data-stu-id="6977c-147">Kind</span></span> | <span data-ttu-id="6977c-148">Dimensions</span><span class="sxs-lookup"><span data-stu-id="6977c-148">Dimensions</span></span> | <span data-ttu-id="6977c-149">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="6977c-149">Supported dimension counts</span></span> | <span data-ttu-id="6977c-150">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="6977c-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="6977c-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="6977c-151">InputTensor</span></span> | <span data-ttu-id="6977c-152">Entrée</span><span class="sxs-lookup"><span data-stu-id="6977c-152">Input</span></span> | <span data-ttu-id="6977c-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="6977c-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="6977c-154">4</span><span class="sxs-lookup"><span data-stu-id="6977c-154">4</span></span> | <span data-ttu-id="6977c-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6977c-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6977c-156">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="6977c-156">InputGradientTensor</span></span> | <span data-ttu-id="6977c-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="6977c-157">Input</span></span> | <span data-ttu-id="6977c-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="6977c-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="6977c-159">4</span><span class="sxs-lookup"><span data-stu-id="6977c-159">4</span></span> | <span data-ttu-id="6977c-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6977c-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6977c-161">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="6977c-161">OutputGradientTensor</span></span> | <span data-ttu-id="6977c-162">Output</span><span class="sxs-lookup"><span data-stu-id="6977c-162">Output</span></span> | <span data-ttu-id="6977c-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="6977c-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="6977c-164">4</span><span class="sxs-lookup"><span data-stu-id="6977c-164">4</span></span> | <span data-ttu-id="6977c-165">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6977c-165">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="6977c-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6977c-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6977c-167">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="6977c-167">**Header**</span></span> | <span data-ttu-id="6977c-168">directml. h</span><span class="sxs-lookup"><span data-stu-id="6977c-168">directml.h</span></span> |