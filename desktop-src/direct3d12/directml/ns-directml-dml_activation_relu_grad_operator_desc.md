---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour une unité linéaire redressée (ReLU).
helpviewer_keywords:
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC, DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.openlocfilehash: 567a1de50c1c91de83a9fda2978f83af8daf1a6e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106537156"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="15eb9-103">Structure DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="15eb9-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="15eb9-104">Calcule les dégradés de la rétropropagation pour une unité linéaire redressée (ReLU).</span><span class="sxs-lookup"><span data-stu-id="15eb9-104">Computes backpropagation gradients for a rectified linear unit (ReLU).</span></span> <span data-ttu-id="15eb9-105">Cet opérateur effectue le calcul suivant au niveau des éléments.</span><span class="sxs-lookup"><span data-stu-id="15eb9-105">This operator performs the following element-wise computation.</span></span>

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

<span data-ttu-id="15eb9-106">L’opérateur de passe en aval correspondant est [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="15eb9-106">The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15eb9-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="15eb9-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="15eb9-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="15eb9-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="15eb9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15eb9-109">Syntax</span></span>
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a><span data-ttu-id="15eb9-110">Membres</span><span class="sxs-lookup"><span data-stu-id="15eb9-110">Members</span></span>

`InputTensor`

<span data-ttu-id="15eb9-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="15eb9-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="15eb9-112">Tenseur d’entrée (fonctionnalité).</span><span class="sxs-lookup"><span data-stu-id="15eb9-112">The input (feature) tensor.</span></span> <span data-ttu-id="15eb9-113">Il s’agit généralement de la même entrée que celle qui a été fournie pendant la passe en avant (voir [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="15eb9-113">This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span></span>

`InputGradientTensor`

<span data-ttu-id="15eb9-114">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="15eb9-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="15eb9-115">Tenseur de dégradé entrant.</span><span class="sxs-lookup"><span data-stu-id="15eb9-115">The incoming gradient tensor.</span></span> <span data-ttu-id="15eb9-116">Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente.</span><span class="sxs-lookup"><span data-stu-id="15eb9-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="15eb9-117">Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="15eb9-117">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

`OutputTensor`

<span data-ttu-id="15eb9-118">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="15eb9-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="15eb9-119">Tenseur de sortie contenant les dégradés de la page.</span><span class="sxs-lookup"><span data-stu-id="15eb9-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="15eb9-120">Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="15eb9-120">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

## <a name="availability"></a><span data-ttu-id="15eb9-121">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="15eb9-121">Availability</span></span>
<span data-ttu-id="15eb9-122">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="15eb9-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="15eb9-123">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="15eb9-123">Tensor constraints</span></span>
<span data-ttu-id="15eb9-124">*InputGradientTensor*, *InputTensor* et *OutputGradientTensor* doivent avoir le même *type de données*, *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="15eb9-124">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="15eb9-125">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="15eb9-125">Tensor support</span></span>
| <span data-ttu-id="15eb9-126">Tenseur</span><span class="sxs-lookup"><span data-stu-id="15eb9-126">Tensor</span></span> | <span data-ttu-id="15eb9-127">Type</span><span class="sxs-lookup"><span data-stu-id="15eb9-127">Kind</span></span> | <span data-ttu-id="15eb9-128">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="15eb9-128">Supported dimension counts</span></span> | <span data-ttu-id="15eb9-129">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="15eb9-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="15eb9-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="15eb9-130">InputTensor</span></span> | <span data-ttu-id="15eb9-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="15eb9-131">Input</span></span> | <span data-ttu-id="15eb9-132">1 à 8</span><span class="sxs-lookup"><span data-stu-id="15eb9-132">1 to 8</span></span> | <span data-ttu-id="15eb9-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="15eb9-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="15eb9-134">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="15eb9-134">InputGradientTensor</span></span> | <span data-ttu-id="15eb9-135">Entrée</span><span class="sxs-lookup"><span data-stu-id="15eb9-135">Input</span></span> | <span data-ttu-id="15eb9-136">1 à 8</span><span class="sxs-lookup"><span data-stu-id="15eb9-136">1 to 8</span></span> | <span data-ttu-id="15eb9-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="15eb9-137">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="15eb9-138">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="15eb9-138">OutputGradientTensor</span></span> | <span data-ttu-id="15eb9-139">Output</span><span class="sxs-lookup"><span data-stu-id="15eb9-139">Output</span></span> | <span data-ttu-id="15eb9-140">1 à 8</span><span class="sxs-lookup"><span data-stu-id="15eb9-140">1 to 8</span></span> | <span data-ttu-id="15eb9-141">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="15eb9-141">FLOAT32, FLOAT16</span></span> |

## <a name="see-also"></a><span data-ttu-id="15eb9-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15eb9-142">See also</span></span>
[<span data-ttu-id="15eb9-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="15eb9-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a><span data-ttu-id="15eb9-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15eb9-144">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="15eb9-145">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="15eb9-145">**Header**</span></span> | <span data-ttu-id="15eb9-146">directml. h</span><span class="sxs-lookup"><span data-stu-id="15eb9-146">directml.h</span></span> |