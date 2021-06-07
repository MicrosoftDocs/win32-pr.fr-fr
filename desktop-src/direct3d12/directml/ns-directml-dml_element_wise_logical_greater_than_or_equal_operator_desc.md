---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
description: Effectue une logique *supérieure ou égale à* sur chaque paire d’éléments correspondants des dizaines d’entrée, en plaçant le résultat (1 pour true, 0 pour false) dans l’élément correspondant de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: 4c20580a67117e6a605dfb0bf6611aca5cfd9e56
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417385"
---
# <a name="dml_element_wise_logical_greater_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="5dc7d-103">Structure DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="5dc7d-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5dc7d-104">Effectue une logique *supérieure ou égale à* sur chaque paire d’éléments correspondants des dizaines d’entrée, en plaçant le résultat (1 pour true, 0 pour false) dans l’élément correspondant de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="5dc7d-104">Performs a logical *greater than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >= b)
```

> [!IMPORTANT]
> <span data-ttu-id="5dc7d-105">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5dc7d-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5dc7d-106">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5dc7d-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc7d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5dc7d-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="5dc7d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5dc7d-108">Members</span></span>

`ATensor`

<span data-ttu-id="5dc7d-109">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5dc7d-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5dc7d-110">Tenseur contenant les entrées côté gauche.</span><span class="sxs-lookup"><span data-stu-id="5dc7d-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="5dc7d-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5dc7d-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5dc7d-112">Tenseur contenant les entrées côté droit.</span><span class="sxs-lookup"><span data-stu-id="5dc7d-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="5dc7d-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5dc7d-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5dc7d-114">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="5dc7d-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="5dc7d-115">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="5dc7d-115">Availability</span></span>
<span data-ttu-id="5dc7d-116">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="5dc7d-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5dc7d-117">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="5dc7d-117">Tensor constraints</span></span>
* <span data-ttu-id="5dc7d-118">*ATensor* et *BTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="5dc7d-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="5dc7d-119">*ATensor*, *BTensor* et *OutputTensor* doivent avoir les mêmes *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="5dc7d-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5dc7d-120">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="5dc7d-120">Tensor support</span></span>
| <span data-ttu-id="5dc7d-121">Tenseur</span><span class="sxs-lookup"><span data-stu-id="5dc7d-121">Tensor</span></span> | <span data-ttu-id="5dc7d-122">Type</span><span class="sxs-lookup"><span data-stu-id="5dc7d-122">Kind</span></span> | <span data-ttu-id="5dc7d-123">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="5dc7d-123">Supported dimension counts</span></span> | <span data-ttu-id="5dc7d-124">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dc7d-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5dc7d-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="5dc7d-125">ATensor</span></span> | <span data-ttu-id="5dc7d-126">Entrée</span><span class="sxs-lookup"><span data-stu-id="5dc7d-126">Input</span></span> | <span data-ttu-id="5dc7d-127">1 à 8</span><span class="sxs-lookup"><span data-stu-id="5dc7d-127">1 to 8</span></span> | <span data-ttu-id="5dc7d-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5dc7d-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5dc7d-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="5dc7d-129">BTensor</span></span> | <span data-ttu-id="5dc7d-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="5dc7d-130">Input</span></span> | <span data-ttu-id="5dc7d-131">1 à 8</span><span class="sxs-lookup"><span data-stu-id="5dc7d-131">1 to 8</span></span> | <span data-ttu-id="5dc7d-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5dc7d-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5dc7d-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5dc7d-133">OutputTensor</span></span> | <span data-ttu-id="5dc7d-134">Sortie</span><span class="sxs-lookup"><span data-stu-id="5dc7d-134">Output</span></span> | <span data-ttu-id="5dc7d-135">1 à 8</span><span class="sxs-lookup"><span data-stu-id="5dc7d-135">1 to 8</span></span> | <span data-ttu-id="5dc7d-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="5dc7d-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="5dc7d-137">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5dc7d-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5dc7d-138">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="5dc7d-138">**Header**</span></span> | <span data-ttu-id="5dc7d-139">directml. h</span><span class="sxs-lookup"><span data-stu-id="5dc7d-139">directml.h</span></span> |