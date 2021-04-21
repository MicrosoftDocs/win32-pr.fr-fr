---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour le regroupement moyen (voir [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 5c2803fc300ca862d54a74aee1c864e9097e3d8e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803364"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="21d24-103">Structure DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="21d24-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="21d24-104">Calcule les dégradés de la rétropropagation pour le regroupement moyen (voir [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="21d24-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="21d24-105">Imaginez un **DML_AVERAGE_POOLING_OPERATOR_DESC** 2x2, sans remplissage et un Stride de 1, qui effectue les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="21d24-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="21d24-106">Chaque fenêtre 2x2 dans le tenseur d’entrée est calculée pour produire un élément de la sortie (en lisant des zéros pour les éléments situés au-delà du bord).</span><span class="sxs-lookup"><span data-stu-id="21d24-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="21d24-107">Voici un exemple de la sortie de **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** données similaires.</span><span class="sxs-lookup"><span data-stu-id="21d24-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="21d24-108">Notez que les valeurs de *OutputGradientTensor* représentent les contributions pondérées de cet élément au *OutputTensor* au cours de l’opérateur de [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) d’origine.</span><span class="sxs-lookup"><span data-stu-id="21d24-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21d24-109">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="21d24-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="21d24-110">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="21d24-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="21d24-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21d24-111">Syntax</span></span>

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a><span data-ttu-id="21d24-112">Membres</span><span class="sxs-lookup"><span data-stu-id="21d24-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="21d24-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="21d24-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="21d24-114">Tenseur de dégradé entrant.</span><span class="sxs-lookup"><span data-stu-id="21d24-114">The incoming gradient tensor.</span></span> <span data-ttu-id="21d24-115">Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente.</span><span class="sxs-lookup"><span data-stu-id="21d24-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="21d24-116">En général, ce tenseur a la même taille que la *sortie* de la [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) correspondante dans la passe de transfert.</span><span class="sxs-lookup"><span data-stu-id="21d24-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="21d24-117">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="21d24-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="21d24-118">Tenseur de sortie contenant les dégradés de la page.</span><span class="sxs-lookup"><span data-stu-id="21d24-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="21d24-119">En général, ce tenseur a la même taille que l' *entrée* de la [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) correspondante dans la passe en avant.</span><span class="sxs-lookup"><span data-stu-id="21d24-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="21d24-120">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="21d24-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="21d24-121">Nombre d’éléments dans les tableaux *Strides*, *Windows*, *StartPadding* et *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="21d24-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="21d24-122">Cette valeur doit être égale au nombre de dimensions spatiales.</span><span class="sxs-lookup"><span data-stu-id="21d24-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="21d24-123">Le nombre de dimensions spatiales est 2 si des dizaines 4D sont fournis, ou 3 si les dizaines de 5D sont fournis.</span><span class="sxs-lookup"><span data-stu-id="21d24-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="21d24-124">Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="21d24-124">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="21d24-125">Consultez la section *Strides* dans [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="21d24-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="21d24-126">Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="21d24-126">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="21d24-127">Consultez *Windows* dans [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="21d24-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="21d24-128">Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="21d24-128">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="21d24-129">Consultez *StartPadding* dans [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="21d24-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="21d24-130">Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="21d24-130">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="21d24-131">Consultez *EndPadding* dans [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="21d24-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="21d24-132">Type : <b> <a href="/windows/win32/winprog/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="21d24-132">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="21d24-133">Consultez *IncludePadding* dans [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="21d24-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="21d24-134">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="21d24-134">Availability</span></span>
<span data-ttu-id="21d24-135">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="21d24-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="21d24-136">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="21d24-136">Tensor constraints</span></span>
<span data-ttu-id="21d24-137">*InputGradientTensor* et *OutputGradientTensor* doivent avoir le même *type de données* et *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="21d24-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="21d24-138">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="21d24-138">Tensor support</span></span>
| <span data-ttu-id="21d24-139">Tenseur</span><span class="sxs-lookup"><span data-stu-id="21d24-139">Tensor</span></span> | <span data-ttu-id="21d24-140">Type</span><span class="sxs-lookup"><span data-stu-id="21d24-140">Kind</span></span> | <span data-ttu-id="21d24-141">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="21d24-141">Supported dimension counts</span></span> | <span data-ttu-id="21d24-142">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="21d24-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="21d24-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="21d24-143">InputGradientTensor</span></span> | <span data-ttu-id="21d24-144">Entrée</span><span class="sxs-lookup"><span data-stu-id="21d24-144">Input</span></span> | <span data-ttu-id="21d24-145">4 à 5</span><span class="sxs-lookup"><span data-stu-id="21d24-145">4 to 5</span></span> | <span data-ttu-id="21d24-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="21d24-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="21d24-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="21d24-147">OutputGradientTensor</span></span> | <span data-ttu-id="21d24-148">Output</span><span class="sxs-lookup"><span data-stu-id="21d24-148">Output</span></span> | <span data-ttu-id="21d24-149">4 à 5</span><span class="sxs-lookup"><span data-stu-id="21d24-149">4 to 5</span></span> | <span data-ttu-id="21d24-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="21d24-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="21d24-151">Spécifications</span><span class="sxs-lookup"><span data-stu-id="21d24-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="21d24-152">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="21d24-152">**Header**</span></span> | <span data-ttu-id="21d24-153">directml. h</span><span class="sxs-lookup"><span data-stu-id="21d24-153">directml.h</span></span> |