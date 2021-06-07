---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Arrondit chaque élément de *InputTensor* à une valeur entière, en plaçant le résultat dans l’élément correspondant de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure
- direct3d12.dml_element_wise_round_operator_desc
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.openlocfilehash: cb9414d0c3e628fa95784480c7402b242d12095b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417384"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a><span data-ttu-id="12a87-103">Structure DML_ELEMENT_WISE_ROUND_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="12a87-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="12a87-104">Arrondit chaque élément de *InputTensor* à une valeur entière, en plaçant le résultat dans l’élément correspondant de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="12a87-104">Rounds each element of *InputTensor* to an integer value, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="12a87-105">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que *OutputTensor* est autorisé à aliaser *InputTensor* pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="12a87-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12a87-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="12a87-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="12a87-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="12a87-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="12a87-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12a87-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a><span data-ttu-id="12a87-109">Membres</span><span class="sxs-lookup"><span data-stu-id="12a87-109">Members</span></span>

`InputTensor`

<span data-ttu-id="12a87-110">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="12a87-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="12a87-111">Tenseur d’entrée à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="12a87-111">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="12a87-112">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="12a87-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="12a87-113">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="12a87-113">The output tensor to write the results to.</span></span>


`RoundingMode`

<span data-ttu-id="12a87-114">Type : **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span><span class="sxs-lookup"><span data-stu-id="12a87-114">Type: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span></span>

<span data-ttu-id="12a87-115">[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) déterminant la direction vers laquelle arrondir.</span><span class="sxs-lookup"><span data-stu-id="12a87-115">A [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determining the direction to round towards.</span></span>

* <span data-ttu-id="12a87-116">Si **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: les valeurs sont arrondies à l’entier le plus proche, avec des valeurs à mi-chemin (par exemple, 0,5) arrondies vers l’entier pair le plus proche.</span><span class="sxs-lookup"><span data-stu-id="12a87-116">If **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded toward the nearest even integer.</span></span>
* <span data-ttu-id="12a87-117">Si **DML_ROUNDING_MODE_TOWARD_ZERO**: les valeurs sont arrondies vers zéro.</span><span class="sxs-lookup"><span data-stu-id="12a87-117">If **DML_ROUNDING_MODE_TOWARD_ZERO**: values are rounded toward zero.</span></span> <span data-ttu-id="12a87-118">Cela tronque la partie fractionnaire.</span><span class="sxs-lookup"><span data-stu-id="12a87-118">This effectively truncates the fractional part.</span></span>
* <span data-ttu-id="12a87-119">Si **DML_ROUNDING_MODE_TOWARD_INFINITY**: les valeurs sont arrondies à l’entier le plus proche, les valeurs à mi (par exemple, 0,5) étant arrondies de zéro (vers l’infini positif ou négatif, selon le signe de la valeur).</span><span class="sxs-lookup"><span data-stu-id="12a87-119">If **DML_ROUNDING_MODE_TOWARD_INFINITY**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded away from zero (toward positive or negative infinity, depending on the sign of the value).</span></span>

## <a name="availability"></a><span data-ttu-id="12a87-120">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="12a87-120">Availability</span></span>
<span data-ttu-id="12a87-121">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="12a87-121">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="12a87-122">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="12a87-122">Tensor constraints</span></span>
<span data-ttu-id="12a87-123">*InputTensor* et *OutputTensor* doivent avoir les mêmes *types de données*, *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="12a87-123">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="12a87-124">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="12a87-124">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="12a87-125">DML_FEATURE_LEVEL_3_0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="12a87-125">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="12a87-126">Tenseur</span><span class="sxs-lookup"><span data-stu-id="12a87-126">Tensor</span></span> | <span data-ttu-id="12a87-127">Type</span><span class="sxs-lookup"><span data-stu-id="12a87-127">Kind</span></span> | <span data-ttu-id="12a87-128">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="12a87-128">Supported dimension counts</span></span> | <span data-ttu-id="12a87-129">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="12a87-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="12a87-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="12a87-130">InputTensor</span></span> | <span data-ttu-id="12a87-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="12a87-131">Input</span></span> | <span data-ttu-id="12a87-132">1 à 8</span><span class="sxs-lookup"><span data-stu-id="12a87-132">1 to 8</span></span> | <span data-ttu-id="12a87-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="12a87-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="12a87-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="12a87-134">OutputTensor</span></span> | <span data-ttu-id="12a87-135">Sortie</span><span class="sxs-lookup"><span data-stu-id="12a87-135">Output</span></span> | <span data-ttu-id="12a87-136">1 à 8</span><span class="sxs-lookup"><span data-stu-id="12a87-136">1 to 8</span></span> | <span data-ttu-id="12a87-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="12a87-137">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="12a87-138">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="12a87-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="12a87-139">Tenseur</span><span class="sxs-lookup"><span data-stu-id="12a87-139">Tensor</span></span> | <span data-ttu-id="12a87-140">Type</span><span class="sxs-lookup"><span data-stu-id="12a87-140">Kind</span></span> | <span data-ttu-id="12a87-141">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="12a87-141">Supported dimension counts</span></span> | <span data-ttu-id="12a87-142">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="12a87-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="12a87-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="12a87-143">InputTensor</span></span> | <span data-ttu-id="12a87-144">Entrée</span><span class="sxs-lookup"><span data-stu-id="12a87-144">Input</span></span> | <span data-ttu-id="12a87-145">4</span><span class="sxs-lookup"><span data-stu-id="12a87-145">4</span></span> | <span data-ttu-id="12a87-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="12a87-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="12a87-147">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="12a87-147">OutputTensor</span></span> | <span data-ttu-id="12a87-148">Sortie</span><span class="sxs-lookup"><span data-stu-id="12a87-148">Output</span></span> | <span data-ttu-id="12a87-149">4</span><span class="sxs-lookup"><span data-stu-id="12a87-149">4</span></span> | <span data-ttu-id="12a87-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="12a87-150">FLOAT32, FLOAT16</span></span> |



## <a name="requirements"></a><span data-ttu-id="12a87-151">Spécifications</span><span class="sxs-lookup"><span data-stu-id="12a87-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="12a87-152">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="12a87-152">**Header**</span></span> | <span data-ttu-id="12a87-153">directml. h</span><span class="sxs-lookup"><span data-stu-id="12a87-153">directml.h</span></span> |