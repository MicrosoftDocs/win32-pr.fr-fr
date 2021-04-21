---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour la tranche (voir [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: a22efe9b0b74f5fdc7b498b97784086f40f243b9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803969"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="8ba73-103">Structure DML_SLICE_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="8ba73-103">DML_SLICE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="8ba73-104">Calcule les dégradés de la rétropropagation pour la tranche (voir [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="8ba73-104">Computes backpropagation gradients for Slice (see [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span></span>

<span data-ttu-id="8ba73-105">Rappelez-vous que [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extrait une sous-région d’un tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8ba73-105">Recall that [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extracts a subregion of an input tensor.</span></span> <span data-ttu-id="8ba73-106">Étant donné un *InputGradientTensor* avec les mêmes tailles que la *sortie* d’un **DML_SLICE1_OPERATOR_DESC** équivalent, cet opérateur produit un *OutputGradientTensor* avec les mêmes tailles que l' *entrée* de **DML_SLICE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="8ba73-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_SLICE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of **DML_SLICE1_OPERATOR_DESC**.</span></span> <span data-ttu-id="8ba73-107">Les éléments découpés sont propagés à la sortie, et tous les autres éléments ont la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="8ba73-107">The sliced elements are propagated to the output, and all other elements are set to 0.</span></span>

<span data-ttu-id="8ba73-108">Par exemple, considérez un **DML_SLICE1_OPERATOR_DESC** qui extrait les éléments suivants à partir d’un tenseur :</span><span class="sxs-lookup"><span data-stu-id="8ba73-108">As an example, consider a **DML_SLICE1_OPERATOR_DESC** that extracts the following elements from a tensor:</span></span>

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

<span data-ttu-id="8ba73-109">Si vous fournissez la même taille de *InputWindowOffsets* /  /  que dans l’exemple ci-dessus, cet opérateur effectuerait ensuite la transformation suivante.</span><span class="sxs-lookup"><span data-stu-id="8ba73-109">If provided the same *InputWindowOffsets*/*Sizes*/*Strides* as in the above example, this operator would then perform the following transform.</span></span>

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> <span data-ttu-id="8ba73-110">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8ba73-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="8ba73-111">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="8ba73-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba73-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ba73-112">Syntax</span></span>

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a><span data-ttu-id="8ba73-113">Membres</span><span class="sxs-lookup"><span data-stu-id="8ba73-113">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="8ba73-114">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8ba73-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8ba73-115">Tenseur de dégradé entrant.</span><span class="sxs-lookup"><span data-stu-id="8ba73-115">The incoming gradient tensor.</span></span> <span data-ttu-id="8ba73-116">Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente.</span><span class="sxs-lookup"><span data-stu-id="8ba73-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="8ba73-117">En règle générale, ce tenseur a la même taille que la *sortie* de la [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) correspondante dans la passe de transfert.</span><span class="sxs-lookup"><span data-stu-id="8ba73-117">Typically, this tensor would have the same sizes as the *output* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="8ba73-118">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8ba73-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8ba73-119">Tenseur de sortie contenant les dégradés de la page.</span><span class="sxs-lookup"><span data-stu-id="8ba73-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="8ba73-120">En règle générale, ce tenseur aurait les mêmes tailles que l' *entrée* de la [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) correspondante dans la passe en avant.</span><span class="sxs-lookup"><span data-stu-id="8ba73-120">Typically, this tensor would have the same sizes as the *input* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="8ba73-121">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8ba73-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="8ba73-122">Nombre d’éléments dans les tableaux *InputWindowOffsets*, *InputWindowSizes* et *InputWindowStrides* .</span><span class="sxs-lookup"><span data-stu-id="8ba73-122">The number of elements in the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="8ba73-123">Cette valeur doit être égale à la valeur de *DimensionCount* fournie dans *InputGradientTensor* et *OutputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="8ba73-123">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`InputWindowOffsets`

<span data-ttu-id="8ba73-124">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8ba73-124">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8ba73-125">Consultez *InputWindowOffsets* dans [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="8ba73-125">See *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowSizes`

<span data-ttu-id="8ba73-126">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8ba73-126">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8ba73-127">Consultez *InputWindowSizes* dans [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="8ba73-127">See *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowStrides`

<span data-ttu-id="8ba73-128">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="8ba73-128">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="8ba73-129">Consultez *InputWindowStrides* dans [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="8ba73-129">See *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

<span data-ttu-id="8ba73-130">Notez que contrairement à **DML_SLICE1_OPERATOR_DESC**, cet opérateur requiert des Strides non nuls.</span><span class="sxs-lookup"><span data-stu-id="8ba73-130">Note that unlike **DML_SLICE1_OPERATOR_DESC**, this operator requires non-zero strides.</span></span> <span data-ttu-id="8ba73-131">En effet, avec une Stride zéro, il est ambigu quant à l’élément d’entrée qui doit être mappé à chaque élément de sortie, et par conséquent, la rétropropagation ne peut pas être exécutée.</span><span class="sxs-lookup"><span data-stu-id="8ba73-131">That's because with a zero stride, it's ambiguous as to which input element should map to each output element, and therefore backpropagation can't be performed.</span></span> <span data-ttu-id="8ba73-132">Comme **DML_SLICE1_OPERATOR_DESC**, les Strides négatifs inversent la direction de la fenêtre d’entrée le long de cet axe.</span><span class="sxs-lookup"><span data-stu-id="8ba73-132">Like **DML_SLICE1_OPERATOR_DESC**, negative strides flip the input window direction along that axis.</span></span>

## <a name="availability"></a><span data-ttu-id="8ba73-133">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="8ba73-133">Availability</span></span>
<span data-ttu-id="8ba73-134">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="8ba73-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8ba73-135">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="8ba73-135">Tensor constraints</span></span>
<span data-ttu-id="8ba73-136">*InputGradientTensor* et *OutputGradientTensor* doivent avoir le même *type de données* et *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="8ba73-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8ba73-137">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="8ba73-137">Tensor support</span></span>
| <span data-ttu-id="8ba73-138">Tenseur</span><span class="sxs-lookup"><span data-stu-id="8ba73-138">Tensor</span></span> | <span data-ttu-id="8ba73-139">Type</span><span class="sxs-lookup"><span data-stu-id="8ba73-139">Kind</span></span> | <span data-ttu-id="8ba73-140">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="8ba73-140">Supported dimension counts</span></span> | <span data-ttu-id="8ba73-141">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ba73-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8ba73-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="8ba73-142">InputGradientTensor</span></span> | <span data-ttu-id="8ba73-143">Entrée</span><span class="sxs-lookup"><span data-stu-id="8ba73-143">Input</span></span> | <span data-ttu-id="8ba73-144">1 à 8</span><span class="sxs-lookup"><span data-stu-id="8ba73-144">1 to 8</span></span> | <span data-ttu-id="8ba73-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8ba73-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8ba73-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="8ba73-146">OutputGradientTensor</span></span> | <span data-ttu-id="8ba73-147">Output</span><span class="sxs-lookup"><span data-stu-id="8ba73-147">Output</span></span> | <span data-ttu-id="8ba73-148">1 à 8</span><span class="sxs-lookup"><span data-stu-id="8ba73-148">1 to 8</span></span> | <span data-ttu-id="8ba73-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8ba73-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="8ba73-150">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8ba73-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8ba73-151">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="8ba73-151">**Header**</span></span> | <span data-ttu-id="8ba73-152">directml. h</span><span class="sxs-lookup"><span data-stu-id="8ba73-152">directml.h</span></span> |