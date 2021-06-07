---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Vérifie chaque élément de *InputTensor* pour IEEE-754-inf, inf, ou les deux, en fonction du *InfinityMode* donné et place le résultat (1 pour true, 0 pour false) dans l’élément correspondant de *OutputTensor*.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417317"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="38f85-103">Structure DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="38f85-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="38f85-104">Vérifie chaque élément de *InputTensor* pour IEEE-754-inf, inf, ou les deux, en fonction du *InfinityMode* donné et place le résultat (1 pour true, 0 pour false) dans l’élément correspondant de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="38f85-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="38f85-105">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="38f85-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="38f85-106">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="38f85-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="38f85-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38f85-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="38f85-108">Membres</span><span class="sxs-lookup"><span data-stu-id="38f85-108">Members</span></span>

`InputTensor`

<span data-ttu-id="38f85-109">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="38f85-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="38f85-110">Tenseur d’entrée à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="38f85-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="38f85-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="38f85-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="38f85-112">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="38f85-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="38f85-113">Type : **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="38f85-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="38f85-114">[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) déterminant le signe de l’infini à vérifier.</span><span class="sxs-lookup"><span data-stu-id="38f85-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="38f85-115">Si **DML_IS_INFINITY_MODE_EITHER**, la valeur 1 est retournée si l’élément est-inf ou inf, sinon 0.</span><span class="sxs-lookup"><span data-stu-id="38f85-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="38f85-116">Si **DML_IS_INFINITY_MODE_POSITIVE**, la valeur 1 est retournée si l’élément est inf, sinon 0.</span><span class="sxs-lookup"><span data-stu-id="38f85-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="38f85-117">Si **DML_IS_INFINITY_MODE_NEGATIVE**», 1 est retourné si l’élément est-inf, sinon 0.</span><span class="sxs-lookup"><span data-stu-id="38f85-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="38f85-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="38f85-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="38f85-119">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="38f85-119">Availability</span></span>
<span data-ttu-id="38f85-120">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="38f85-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="38f85-121">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="38f85-121">Tensor constraints</span></span>
<span data-ttu-id="38f85-122">*InputTensor* et *OutputTensor* doivent avoir les mêmes *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="38f85-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="38f85-123">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="38f85-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="38f85-124">DML_FEATURE_LEVEL_3_0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="38f85-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="38f85-125">Tenseur</span><span class="sxs-lookup"><span data-stu-id="38f85-125">Tensor</span></span> | <span data-ttu-id="38f85-126">Type</span><span class="sxs-lookup"><span data-stu-id="38f85-126">Kind</span></span> | <span data-ttu-id="38f85-127">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="38f85-127">Supported dimension counts</span></span> | <span data-ttu-id="38f85-128">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="38f85-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="38f85-129">InputTensor</span><span class="sxs-lookup"><span data-stu-id="38f85-129">InputTensor</span></span> | <span data-ttu-id="38f85-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="38f85-130">Input</span></span> | <span data-ttu-id="38f85-131">1 à 8</span><span class="sxs-lookup"><span data-stu-id="38f85-131">1 to 8</span></span> | <span data-ttu-id="38f85-132">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="38f85-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="38f85-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="38f85-133">OutputTensor</span></span> | <span data-ttu-id="38f85-134">Sortie</span><span class="sxs-lookup"><span data-stu-id="38f85-134">Output</span></span> | <span data-ttu-id="38f85-135">1 à 8</span><span class="sxs-lookup"><span data-stu-id="38f85-135">1 to 8</span></span> | <span data-ttu-id="38f85-136">DESTINÉES</span><span class="sxs-lookup"><span data-stu-id="38f85-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="38f85-137">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="38f85-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="38f85-138">Tenseur</span><span class="sxs-lookup"><span data-stu-id="38f85-138">Tensor</span></span> | <span data-ttu-id="38f85-139">Type</span><span class="sxs-lookup"><span data-stu-id="38f85-139">Kind</span></span> | <span data-ttu-id="38f85-140">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="38f85-140">Supported dimension counts</span></span> | <span data-ttu-id="38f85-141">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="38f85-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="38f85-142">InputTensor</span><span class="sxs-lookup"><span data-stu-id="38f85-142">InputTensor</span></span> | <span data-ttu-id="38f85-143">Entrée</span><span class="sxs-lookup"><span data-stu-id="38f85-143">Input</span></span> | <span data-ttu-id="38f85-144">4</span><span class="sxs-lookup"><span data-stu-id="38f85-144">4</span></span> | <span data-ttu-id="38f85-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="38f85-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="38f85-146">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="38f85-146">OutputTensor</span></span> | <span data-ttu-id="38f85-147">Sortie</span><span class="sxs-lookup"><span data-stu-id="38f85-147">Output</span></span> | <span data-ttu-id="38f85-148">4</span><span class="sxs-lookup"><span data-stu-id="38f85-148">4</span></span> | <span data-ttu-id="38f85-149">DESTINÉES</span><span class="sxs-lookup"><span data-stu-id="38f85-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="38f85-150">Spécifications</span><span class="sxs-lookup"><span data-stu-id="38f85-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="38f85-151">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="38f85-151">**Minimum supported client**</span></span> | <span data-ttu-id="38f85-152">Windows 10, version 2004 (10,0 ; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="38f85-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="38f85-153">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="38f85-153">**Minimum supported server**</span></span> | <span data-ttu-id="38f85-154">Windows Server, version 2004 (10,0 ; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="38f85-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="38f85-155">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="38f85-155">**Header**</span></span> | <span data-ttu-id="38f85-156">directml. h</span><span class="sxs-lookup"><span data-stu-id="38f85-156">directml.h</span></span> |