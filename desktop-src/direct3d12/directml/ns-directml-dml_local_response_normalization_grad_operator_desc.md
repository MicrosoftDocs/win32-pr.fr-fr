---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour la [normalisation de réponse locale](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: eecf849a06ee8e99ac9c015ecd4568496120b2d9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804438"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="77fd7-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="77fd7-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="77fd7-104">Calcule les dégradés de la rétropropagation pour la [normalisation de réponse locale](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="77fd7-104">Computes backpropagation gradients for [local response normalization](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span></span>

<span data-ttu-id="77fd7-105">Le type de données et la taille de tous les dizaines doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="77fd7-105">The data type and size of all tensors must be the same.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77fd7-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="77fd7-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="77fd7-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="77fd7-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="77fd7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77fd7-108">Syntax</span></span>
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a><span data-ttu-id="77fd7-109">Membres</span><span class="sxs-lookup"><span data-stu-id="77fd7-109">Members</span></span>

`InputTensor`

<span data-ttu-id="77fd7-110">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="77fd7-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="77fd7-111">Tenseur contenant les données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="77fd7-111">The tensor containing the input data.</span></span> <span data-ttu-id="77fd7-112">Les *tailles* de ce tenseur doivent être `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="77fd7-112">This tensor's *Sizes* should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`InputGradientTensor`

<span data-ttu-id="77fd7-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="77fd7-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="77fd7-114">Tenseur de dégradé entrant.</span><span class="sxs-lookup"><span data-stu-id="77fd7-114">The incoming gradient tensor.</span></span> <span data-ttu-id="77fd7-115">Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente.</span><span class="sxs-lookup"><span data-stu-id="77fd7-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span>

`OutputGradientTensor`

<span data-ttu-id="77fd7-116">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="77fd7-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="77fd7-117">Tenseur de sortie contenant les dégradés de la page.</span><span class="sxs-lookup"><span data-stu-id="77fd7-117">An output tensor containing the backpropagated gradients.</span></span>

`CrossChannel`

<span data-ttu-id="77fd7-118">Type : **[bool](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77fd7-118">Type: **[BOOL](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="77fd7-119">**True** si la couche LRN est additionnée sur plusieurs canaux ; **False** si la couche LRN est additionnée dans les dimensions spatiales.</span><span class="sxs-lookup"><span data-stu-id="77fd7-119">**TRUE** if the LRN layer sums across channels; **FALSE** if the LRN layer sums across spatial dimensions.</span></span>

`LocalSize`

<span data-ttu-id="77fd7-120">Type : **[uint](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77fd7-120">Type: **[UINT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="77fd7-121">Nombre maximal d’éléments à additionner par dimension (la région locale est découpée de manière à ce que tous les éléments soient dans les limites).</span><span class="sxs-lookup"><span data-stu-id="77fd7-121">The maximum number of elements to sum over per dimension (the local region is clipped so that all elements are within bounds).</span></span> <span data-ttu-id="77fd7-122">Si *CrossChannel* a la **valeur true**, il s’agit de la largeur et de la hauteur de la région locale.</span><span class="sxs-lookup"><span data-stu-id="77fd7-122">If *CrossChannel* is **TRUE**, then this is the width and height of the local region.</span></span> <span data-ttu-id="77fd7-123">Si *CrossChannel* a la **valeur false**, il s’agit du nombre d’éléments dans la région locale.</span><span class="sxs-lookup"><span data-stu-id="77fd7-123">If *CrossChannel* is **FALSE**, then this is the number of elements in the local region.</span></span> <span data-ttu-id="77fd7-124">La valeur doit être au moins à 1.</span><span class="sxs-lookup"><span data-stu-id="77fd7-124">This value must be at least 1.</span></span>

`Alpha`

<span data-ttu-id="77fd7-125">Type : **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77fd7-125">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="77fd7-126">Valeur du paramètre de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="77fd7-126">The value of the scaling parameter.</span></span> <span data-ttu-id="77fd7-127">Nous recommandons la valeur par défaut 0,0001.</span><span class="sxs-lookup"><span data-stu-id="77fd7-127">We recommend a value of 0.0001 as default.</span></span>

`Beta`

<span data-ttu-id="77fd7-128">Type : **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77fd7-128">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="77fd7-129">Valeur de l’exposant.</span><span class="sxs-lookup"><span data-stu-id="77fd7-129">The value of the exponent.</span></span> <span data-ttu-id="77fd7-130">Nous recommandons la valeur par défaut 0,75.</span><span class="sxs-lookup"><span data-stu-id="77fd7-130">We recommend a value of 0.75 as default.</span></span>

`Bias`

<span data-ttu-id="77fd7-131">Type : **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="77fd7-131">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="77fd7-132">Valeur de Bias.</span><span class="sxs-lookup"><span data-stu-id="77fd7-132">The value of bias.</span></span> <span data-ttu-id="77fd7-133">Nous recommandons la valeur par défaut 1.</span><span class="sxs-lookup"><span data-stu-id="77fd7-133">We recommend a value of 1 as default.</span></span>

## <a name="availability"></a><span data-ttu-id="77fd7-134">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="77fd7-134">Availability</span></span>
<span data-ttu-id="77fd7-135">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="77fd7-135">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="77fd7-136">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="77fd7-136">Tensor constraints</span></span>
<span data-ttu-id="77fd7-137">*InputGradientTensor*, *InputTensor* et *OutputGradientTensor* doivent avoir le même *type de données* et les mêmes *tailles*.</span><span class="sxs-lookup"><span data-stu-id="77fd7-137">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="77fd7-138">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="77fd7-138">Tensor support</span></span>
| <span data-ttu-id="77fd7-139">Tenseur</span><span class="sxs-lookup"><span data-stu-id="77fd7-139">Tensor</span></span> | <span data-ttu-id="77fd7-140">Type</span><span class="sxs-lookup"><span data-stu-id="77fd7-140">Kind</span></span> | <span data-ttu-id="77fd7-141">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="77fd7-141">Supported dimension counts</span></span> | <span data-ttu-id="77fd7-142">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="77fd7-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="77fd7-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="77fd7-143">InputTensor</span></span> | <span data-ttu-id="77fd7-144">Entrée</span><span class="sxs-lookup"><span data-stu-id="77fd7-144">Input</span></span> | <span data-ttu-id="77fd7-145">4</span><span class="sxs-lookup"><span data-stu-id="77fd7-145">4</span></span> | <span data-ttu-id="77fd7-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="77fd7-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="77fd7-147">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="77fd7-147">InputGradientTensor</span></span> | <span data-ttu-id="77fd7-148">Entrée</span><span class="sxs-lookup"><span data-stu-id="77fd7-148">Input</span></span> | <span data-ttu-id="77fd7-149">4</span><span class="sxs-lookup"><span data-stu-id="77fd7-149">4</span></span> | <span data-ttu-id="77fd7-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="77fd7-150">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="77fd7-151">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="77fd7-151">OutputGradientTensor</span></span> | <span data-ttu-id="77fd7-152">Output</span><span class="sxs-lookup"><span data-stu-id="77fd7-152">Output</span></span> | <span data-ttu-id="77fd7-153">4</span><span class="sxs-lookup"><span data-stu-id="77fd7-153">4</span></span> | <span data-ttu-id="77fd7-154">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="77fd7-154">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="77fd7-155">Spécifications</span><span class="sxs-lookup"><span data-stu-id="77fd7-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="77fd7-156">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="77fd7-156">**Header**</span></span> | <span data-ttu-id="77fd7-157">directml. h</span><span class="sxs-lookup"><span data-stu-id="77fd7-157">directml.h</span></span> |
