---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour [le clip au niveau](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)de l’élément.
helpviewer_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure
- direct3d12.dml_element_wise_clip_grad_operator_desc
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.openlocfilehash: 224fbacdb8816a6aed6a7779c5c8ff991736ee6c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804446"
---
# <a name="dml_element_wise_clip_grad_operator_desc-directmlh"></a><span data-ttu-id="76f03-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="76f03-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="76f03-104">Calcule les dégradés de la rétropropagation pour [le clip au niveau](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc)de l’élément.</span><span class="sxs-lookup"><span data-stu-id="76f03-104">Computes backpropagation gradients for [element-wise clip](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).</span></span>

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

<span data-ttu-id="76f03-105">Cet opérateur prend en charge l’exécution sur place, ce qui signifie `OutputTensor` qu’il est autorisé à aliaser *InputTensor* pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="76f03-105">This operator supports in-place execution, meaning `OutputTensor` is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76f03-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="76f03-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="76f03-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="76f03-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="76f03-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76f03-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    FLOAT Min;
    FLOAT Max;
};
```

## <a name="members"></a><span data-ttu-id="76f03-109">Membres</span><span class="sxs-lookup"><span data-stu-id="76f03-109">Members</span></span>

`InputTensor`

<span data-ttu-id="76f03-110">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76f03-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76f03-111">La fonctionnalité d’entrée tenseur.</span><span class="sxs-lookup"><span data-stu-id="76f03-111">The input feature tensor.</span></span> <span data-ttu-id="76f03-112">Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *InputTensor* pour [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="76f03-112">This is typically the same tensor that was provided as the *InputTensor* to [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="76f03-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76f03-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76f03-114">Tenseur de dégradé entrant.</span><span class="sxs-lookup"><span data-stu-id="76f03-114">The incoming gradient tensor.</span></span> <span data-ttu-id="76f03-115">Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente.</span><span class="sxs-lookup"><span data-stu-id="76f03-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="76f03-116">En général, ce tenseur a la même taille que la *sortie* de la **DML_OPERATOR_ELEMENT_WISE_CLIP** correspondante dans la passe de transfert.</span><span class="sxs-lookup"><span data-stu-id="76f03-116">Typically this tensor would have the same sizes as the *output* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="76f03-117">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="76f03-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="76f03-118">Tenseur de sortie contenant les dégradés de la page.</span><span class="sxs-lookup"><span data-stu-id="76f03-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="76f03-119">En général, ce tenseur a la même taille que l' *entrée* de la **DML_OPERATOR_ELEMENT_WISE_CLIP** correspondante dans la passe en avant.</span><span class="sxs-lookup"><span data-stu-id="76f03-119">Typically this tensor would have the same sizes as the *input* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`Min`

<span data-ttu-id="76f03-120">Type : **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76f03-120">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="76f03-121">Valeur minimale.</span><span class="sxs-lookup"><span data-stu-id="76f03-121">The minimum value.</span></span> <span data-ttu-id="76f03-122">Si x est égal ou inférieur à cette valeur, le résultat du dégradé est 0.</span><span class="sxs-lookup"><span data-stu-id="76f03-122">If x is at or below this value, then the gradient result is 0.</span></span>

`Max`

<span data-ttu-id="76f03-123">Type : **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76f03-123">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="76f03-124">Valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="76f03-124">The maximum value.</span></span> <span data-ttu-id="76f03-125">Si x est au niveau ou au-dessus de cette valeur, le résultat du dégradé est 0.</span><span class="sxs-lookup"><span data-stu-id="76f03-125">If x is at or above this value, then the gradient result is 0.</span></span>

## <a name="availability"></a><span data-ttu-id="76f03-126">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="76f03-126">Availability</span></span>
<span data-ttu-id="76f03-127">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="76f03-127">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="76f03-128">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="76f03-128">Tensor constraints</span></span>
<span data-ttu-id="76f03-129">*InputGradientTensor*, *InputTensor* et *OutputGradientTensor* doivent avoir le même *type de données*, *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="76f03-129">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="76f03-130">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="76f03-130">Tensor support</span></span>
| <span data-ttu-id="76f03-131">Tenseur</span><span class="sxs-lookup"><span data-stu-id="76f03-131">Tensor</span></span> | <span data-ttu-id="76f03-132">Type</span><span class="sxs-lookup"><span data-stu-id="76f03-132">Kind</span></span> | <span data-ttu-id="76f03-133">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="76f03-133">Supported dimension counts</span></span> | <span data-ttu-id="76f03-134">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="76f03-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="76f03-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="76f03-135">InputTensor</span></span> | <span data-ttu-id="76f03-136">Entrée</span><span class="sxs-lookup"><span data-stu-id="76f03-136">Input</span></span> | <span data-ttu-id="76f03-137">1 à 8</span><span class="sxs-lookup"><span data-stu-id="76f03-137">1 to 8</span></span> | <span data-ttu-id="76f03-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="76f03-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="76f03-139">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="76f03-139">InputGradientTensor</span></span> | <span data-ttu-id="76f03-140">Entrée</span><span class="sxs-lookup"><span data-stu-id="76f03-140">Input</span></span> | <span data-ttu-id="76f03-141">1 à 8</span><span class="sxs-lookup"><span data-stu-id="76f03-141">1 to 8</span></span> | <span data-ttu-id="76f03-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="76f03-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="76f03-143">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="76f03-143">OutputGradientTensor</span></span> | <span data-ttu-id="76f03-144">Output</span><span class="sxs-lookup"><span data-stu-id="76f03-144">Output</span></span> | <span data-ttu-id="76f03-145">1 à 8</span><span class="sxs-lookup"><span data-stu-id="76f03-145">1 to 8</span></span> | <span data-ttu-id="76f03-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="76f03-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="76f03-147">Spécifications</span><span class="sxs-lookup"><span data-stu-id="76f03-147">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="76f03-148">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="76f03-148">**Header**</span></span> | <span data-ttu-id="76f03-149">directml. h</span><span class="sxs-lookup"><span data-stu-id="76f03-149">directml.h</span></span> |
