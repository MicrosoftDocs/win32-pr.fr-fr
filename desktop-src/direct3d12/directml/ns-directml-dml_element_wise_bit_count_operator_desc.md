---
UID: NS:directml.DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
description: Calcule l’opération NOT au niveau du bit pour chaque élément du tenseur d’entrée, puis écrit le résultat dans le tenseur de sortie.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.openlocfilehash: 070fc901c006ce1f18429e79eab635a5360c4af7
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803242"
---
# <a name="dml_element_wise_bit_not_operator_desc-structure-directmlh"></a><span data-ttu-id="5b072-103">Structure DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="5b072-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5b072-104">Calcule l’opération NOT au niveau du bit pour chaque élément du tenseur d’entrée, puis écrit le résultat dans le tenseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="5b072-104">Computes the bitwise NOT for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="5b072-105">Les tenseur d’entrée et de sortie doivent avoir les mêmes *DimensionCount*, *taille* et *type de données*.</span><span class="sxs-lookup"><span data-stu-id="5b072-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="5b072-106">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que le tenseur de sortie est autorisé à aliaser le tenseur d’entrée pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="5b072-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias the input tensor during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b072-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5b072-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5b072-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5b072-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b072-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b072-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="5b072-110">Membres</span><span class="sxs-lookup"><span data-stu-id="5b072-110">Members</span></span>

`InputTensor`

<span data-ttu-id="5b072-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b072-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b072-112">Tenseur d’entrée à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="5b072-112">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="5b072-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b072-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b072-114">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="5b072-114">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="5b072-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="5b072-115">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="5b072-116">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="5b072-116">Availability</span></span>
<span data-ttu-id="5b072-117">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="5b072-117">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5b072-118">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="5b072-118">Tensor constraints</span></span>
<span data-ttu-id="5b072-119">*InputTensor* et *OutputTensor* doivent avoir les mêmes *types de données*, *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="5b072-119">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5b072-120">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="5b072-120">Tensor support</span></span>
| <span data-ttu-id="5b072-121">Tenseur</span><span class="sxs-lookup"><span data-stu-id="5b072-121">Tensor</span></span> | <span data-ttu-id="5b072-122">Type</span><span class="sxs-lookup"><span data-stu-id="5b072-122">Kind</span></span> | <span data-ttu-id="5b072-123">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="5b072-123">Supported dimension counts</span></span> | <span data-ttu-id="5b072-124">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b072-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5b072-125">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5b072-125">InputTensor</span></span> | <span data-ttu-id="5b072-126">Entrée</span><span class="sxs-lookup"><span data-stu-id="5b072-126">Input</span></span> | <span data-ttu-id="5b072-127">1 à 8</span><span class="sxs-lookup"><span data-stu-id="5b072-127">1 to 8</span></span> | <span data-ttu-id="5b072-128">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5b072-128">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5b072-129">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5b072-129">OutputTensor</span></span> | <span data-ttu-id="5b072-130">Output</span><span class="sxs-lookup"><span data-stu-id="5b072-130">Output</span></span> | <span data-ttu-id="5b072-131">1 à 8</span><span class="sxs-lookup"><span data-stu-id="5b072-131">1 to 8</span></span> | <span data-ttu-id="5b072-132">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5b072-132">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="5b072-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5b072-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5b072-134">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="5b072-134">**Header**</span></span> | <span data-ttu-id="5b072-135">directml. h</span><span class="sxs-lookup"><span data-stu-id="5b072-135">directml.h</span></span> |