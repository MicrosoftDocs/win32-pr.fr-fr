---
UID: NS:directml.DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
title: DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
description: Soustrait chaque élément de *BTensor* de l’élément correspondant de *ATensor*, multiplie le résultat par lui-même et place le résultat dans l’élément correspondant de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.openlocfilehash: 3e3e7ab8f222f42def82a168ed861e58347f3b20
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804442"
---
# <a name="dml_element_wise_difference_square_operator_desc-directmlh"></a><span data-ttu-id="9abad-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="9abad-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="9abad-104">Soustrait chaque élément de *BTensor* de l’élément correspondant de *ATensor*, multiplie le résultat par lui-même et place le résultat dans l’élément correspondant de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="9abad-104">Subtracts each element of *BTensor* from the corresponding element of *ATensor*, multiplies the result by itself, and places the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a - b) * (a - b)
```

<span data-ttu-id="9abad-105">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que *OutputTensor* est autorisé à aliaser *ATensor* ou *BTensor* pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="9abad-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9abad-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9abad-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="9abad-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="9abad-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9abad-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9abad-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="9abad-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9abad-109">Members</span></span>

`ATensor`

<span data-ttu-id="9abad-110">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9abad-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9abad-111">Tenseur contenant les entrées côté gauche.</span><span class="sxs-lookup"><span data-stu-id="9abad-111">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="9abad-112">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9abad-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9abad-113">Tenseur contenant les entrées côté droit.</span><span class="sxs-lookup"><span data-stu-id="9abad-113">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="9abad-114">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9abad-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9abad-115">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="9abad-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="9abad-116">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="9abad-116">Availability</span></span>
<span data-ttu-id="9abad-117">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="9abad-117">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="9abad-118">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="9abad-118">Tensor constraints</span></span>
<span data-ttu-id="9abad-119">*ATensor*, *BTensor* et *OutputTensor* doivent avoir le même *type de données*, *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="9abad-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="9abad-120">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="9abad-120">Tensor support</span></span>
| <span data-ttu-id="9abad-121">Tenseur</span><span class="sxs-lookup"><span data-stu-id="9abad-121">Tensor</span></span> | <span data-ttu-id="9abad-122">Type</span><span class="sxs-lookup"><span data-stu-id="9abad-122">Kind</span></span> | <span data-ttu-id="9abad-123">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="9abad-123">Supported dimension counts</span></span> | <span data-ttu-id="9abad-124">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="9abad-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="9abad-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="9abad-125">ATensor</span></span> | <span data-ttu-id="9abad-126">Entrée</span><span class="sxs-lookup"><span data-stu-id="9abad-126">Input</span></span> | <span data-ttu-id="9abad-127">1 à 8</span><span class="sxs-lookup"><span data-stu-id="9abad-127">1 to 8</span></span> | <span data-ttu-id="9abad-128">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="9abad-128">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="9abad-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="9abad-129">BTensor</span></span> | <span data-ttu-id="9abad-130">Entrée</span><span class="sxs-lookup"><span data-stu-id="9abad-130">Input</span></span> | <span data-ttu-id="9abad-131">1 à 8</span><span class="sxs-lookup"><span data-stu-id="9abad-131">1 to 8</span></span> | <span data-ttu-id="9abad-132">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="9abad-132">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="9abad-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="9abad-133">OutputTensor</span></span> | <span data-ttu-id="9abad-134">Output</span><span class="sxs-lookup"><span data-stu-id="9abad-134">Output</span></span> | <span data-ttu-id="9abad-135">1 à 8</span><span class="sxs-lookup"><span data-stu-id="9abad-135">1 to 8</span></span> | <span data-ttu-id="9abad-136">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="9abad-136">FLOAT32, FLOAT16, INT32, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="9abad-137">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9abad-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9abad-138">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="9abad-138">**Header**</span></span> | <span data-ttu-id="9abad-139">directml. h</span><span class="sxs-lookup"><span data-stu-id="9abad-139">directml.h</span></span> |
