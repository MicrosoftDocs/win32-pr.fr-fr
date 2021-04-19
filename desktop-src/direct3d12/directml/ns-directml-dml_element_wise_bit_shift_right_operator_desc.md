---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
description: Effectue un décalage logique vers la droite de chaque élément de *ATensor* par un nombre de bits donné par l’élément correspondant de *BTensor*, en plaçant le résultat dans l’élément correspondant de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_right_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.openlocfilehash: 447b0f685b51bf8b146644de3b5f65390a492ffd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106525784"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a><span data-ttu-id="1cf44-103">Structure DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="1cf44-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="1cf44-104">Effectue un décalage logique vers la droite de chaque élément de *ATensor* par un nombre de bits donné par l’élément correspondant de *BTensor*, en plaçant le résultat dans l’élément correspondant de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="1cf44-104">Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >> b)
```

<span data-ttu-id="1cf44-105">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que *OutputTensor* est autorisé à aliaser l’un des dizaines d’entrée pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="1cf44-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1cf44-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="1cf44-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="1cf44-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="1cf44-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf44-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cf44-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="1cf44-109">Membres</span><span class="sxs-lookup"><span data-stu-id="1cf44-109">Members</span></span>

`ATensor`

<span data-ttu-id="1cf44-110">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1cf44-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1cf44-111">Tenseur contenant les entrées côté gauche.</span><span class="sxs-lookup"><span data-stu-id="1cf44-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="1cf44-112">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1cf44-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1cf44-113">Tenseur contenant les entrées côté droit.</span><span class="sxs-lookup"><span data-stu-id="1cf44-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="1cf44-114">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1cf44-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1cf44-115">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="1cf44-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="1cf44-116">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="1cf44-116">Availability</span></span>
<span data-ttu-id="1cf44-117">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="1cf44-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="1cf44-118">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="1cf44-118">Tensor constraints</span></span>
<span data-ttu-id="1cf44-119">*ATensor*, *BTensor* et *OutputTensor* doivent avoir le même *type de données*, *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="1cf44-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="1cf44-120">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="1cf44-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="1cf44-121">DML_FEATURE_LEVEL_3_0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1cf44-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="1cf44-122">Tenseur</span><span class="sxs-lookup"><span data-stu-id="1cf44-122">Tensor</span></span> | <span data-ttu-id="1cf44-123">Type</span><span class="sxs-lookup"><span data-stu-id="1cf44-123">Kind</span></span> | <span data-ttu-id="1cf44-124">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="1cf44-124">Supported dimension counts</span></span> | <span data-ttu-id="1cf44-125">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cf44-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1cf44-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="1cf44-126">ATensor</span></span> | <span data-ttu-id="1cf44-127">Entrée</span><span class="sxs-lookup"><span data-stu-id="1cf44-127">Input</span></span> | <span data-ttu-id="1cf44-128">1 à 8</span><span class="sxs-lookup"><span data-stu-id="1cf44-128">1 to 8</span></span> | <span data-ttu-id="1cf44-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1cf44-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1cf44-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="1cf44-130">BTensor</span></span> | <span data-ttu-id="1cf44-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="1cf44-131">Input</span></span> | <span data-ttu-id="1cf44-132">1 à 8</span><span class="sxs-lookup"><span data-stu-id="1cf44-132">1 to 8</span></span> | <span data-ttu-id="1cf44-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1cf44-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1cf44-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="1cf44-134">OutputTensor</span></span> | <span data-ttu-id="1cf44-135">Output</span><span class="sxs-lookup"><span data-stu-id="1cf44-135">Output</span></span> | <span data-ttu-id="1cf44-136">1 à 8</span><span class="sxs-lookup"><span data-stu-id="1cf44-136">1 to 8</span></span> | <span data-ttu-id="1cf44-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1cf44-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="1cf44-138">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="1cf44-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="1cf44-139">Tenseur</span><span class="sxs-lookup"><span data-stu-id="1cf44-139">Tensor</span></span> | <span data-ttu-id="1cf44-140">Type</span><span class="sxs-lookup"><span data-stu-id="1cf44-140">Kind</span></span> | <span data-ttu-id="1cf44-141">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="1cf44-141">Supported dimension counts</span></span> | <span data-ttu-id="1cf44-142">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cf44-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1cf44-143">ATensor</span><span class="sxs-lookup"><span data-stu-id="1cf44-143">ATensor</span></span> | <span data-ttu-id="1cf44-144">Entrée</span><span class="sxs-lookup"><span data-stu-id="1cf44-144">Input</span></span> | <span data-ttu-id="1cf44-145">4</span><span class="sxs-lookup"><span data-stu-id="1cf44-145">4</span></span> | <span data-ttu-id="1cf44-146">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1cf44-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1cf44-147">BTensor</span><span class="sxs-lookup"><span data-stu-id="1cf44-147">BTensor</span></span> | <span data-ttu-id="1cf44-148">Entrée</span><span class="sxs-lookup"><span data-stu-id="1cf44-148">Input</span></span> | <span data-ttu-id="1cf44-149">4</span><span class="sxs-lookup"><span data-stu-id="1cf44-149">4</span></span> | <span data-ttu-id="1cf44-150">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1cf44-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1cf44-151">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="1cf44-151">OutputTensor</span></span> | <span data-ttu-id="1cf44-152">Output</span><span class="sxs-lookup"><span data-stu-id="1cf44-152">Output</span></span> | <span data-ttu-id="1cf44-153">4</span><span class="sxs-lookup"><span data-stu-id="1cf44-153">4</span></span> | <span data-ttu-id="1cf44-154">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1cf44-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="1cf44-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cf44-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1cf44-156">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="1cf44-156">**Header**</span></span> | <span data-ttu-id="1cf44-157">directml. h</span><span class="sxs-lookup"><span data-stu-id="1cf44-157">directml.h</span></span> |