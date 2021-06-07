---
UID: NS:directml.DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
description: Calcule l’opération de bits or entre chaque élément correspondant des dizaines d’entrée et écrit le résultat dans le tenseur de sortie.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.openlocfilehash: 7138c6647e1bd4df5d8957468ca67f103f4a3f5a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417396"
---
# <a name="dml_element_wise_bit_or_operator_desc-structure-directmlh"></a><span data-ttu-id="82de8-103">Structure DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="82de8-103">DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="82de8-104">Calcule l’opération de bits or entre chaque élément correspondant des dizaines d’entrée et écrit le résultat dans le tenseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="82de8-104">Computes the bitwise OR between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="82de8-105">Les tenseur d’entrée et de sortie doivent avoir les mêmes *DimensionCount*, *taille* et *type de données*.</span><span class="sxs-lookup"><span data-stu-id="82de8-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="82de8-106">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que le tenseur de sortie est autorisé à effectuer un alias d’un ou plusieurs des dizaines d’entrée pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="82de8-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82de8-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="82de8-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="82de8-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="82de8-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="82de8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82de8-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="82de8-110">Membres</span><span class="sxs-lookup"><span data-stu-id="82de8-110">Members</span></span>

`ATensor`

<span data-ttu-id="82de8-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="82de8-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="82de8-112">Tenseur contenant les entrées côté gauche.</span><span class="sxs-lookup"><span data-stu-id="82de8-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="82de8-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="82de8-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="82de8-114">Tenseur contenant les entrées côté droit.</span><span class="sxs-lookup"><span data-stu-id="82de8-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="82de8-115">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="82de8-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="82de8-116">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="82de8-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="82de8-117">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="82de8-117">Availability</span></span>
<span data-ttu-id="82de8-118">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="82de8-118">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="82de8-119">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="82de8-119">Tensor constraints</span></span>
<span data-ttu-id="82de8-120">*ATensor*, *BTensor* et *OutputTensor* doivent avoir le même *type de données*, *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="82de8-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="82de8-121">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="82de8-121">Tensor support</span></span>
| <span data-ttu-id="82de8-122">Tenseur</span><span class="sxs-lookup"><span data-stu-id="82de8-122">Tensor</span></span> | <span data-ttu-id="82de8-123">Type</span><span class="sxs-lookup"><span data-stu-id="82de8-123">Kind</span></span> | <span data-ttu-id="82de8-124">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="82de8-124">Supported dimension counts</span></span> | <span data-ttu-id="82de8-125">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="82de8-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="82de8-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="82de8-126">ATensor</span></span> | <span data-ttu-id="82de8-127">Entrée</span><span class="sxs-lookup"><span data-stu-id="82de8-127">Input</span></span> | <span data-ttu-id="82de8-128">1 à 8</span><span class="sxs-lookup"><span data-stu-id="82de8-128">1 to 8</span></span> | <span data-ttu-id="82de8-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="82de8-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="82de8-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="82de8-130">BTensor</span></span> | <span data-ttu-id="82de8-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="82de8-131">Input</span></span> | <span data-ttu-id="82de8-132">1 à 8</span><span class="sxs-lookup"><span data-stu-id="82de8-132">1 to 8</span></span> | <span data-ttu-id="82de8-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="82de8-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="82de8-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="82de8-134">OutputTensor</span></span> | <span data-ttu-id="82de8-135">Sortie</span><span class="sxs-lookup"><span data-stu-id="82de8-135">Output</span></span> | <span data-ttu-id="82de8-136">1 à 8</span><span class="sxs-lookup"><span data-stu-id="82de8-136">1 to 8</span></span> | <span data-ttu-id="82de8-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="82de8-137">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="82de8-138">Spécifications</span><span class="sxs-lookup"><span data-stu-id="82de8-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="82de8-139">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="82de8-139">**Header**</span></span> | <span data-ttu-id="82de8-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="82de8-140">directml.h</span></span> |