---
UID: NS:directml.DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
description: Calcule le nombre de remplissages au niveau du bit (nombre de bits défini sur 1) pour chaque élément du tenseur d’entrée, puis écrit le résultat dans le tenseur de sortie.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.openlocfilehash: 4b292b1b6e12f4643e928022f59603fd75e080fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106522868"
---
# <a name="dml_element_wise_bit_count_operator_desc-structure-directmlh"></a><span data-ttu-id="1ee9c-103">Structure DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="1ee9c-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="1ee9c-104">Calcule le nombre de remplissages au niveau du bit (nombre de bits défini sur 1) pour chaque élément du tenseur d’entrée, puis écrit le résultat dans le tenseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-104">Computes the bitwise population count (the number of bits set to 1) for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="1ee9c-105">Les tenseur d’entrée et de sortie doivent avoir les mêmes *DimensionCount* et *tailles*, même si elles peuvent être différentes dans le *type de données*.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-105">The input and output tensor must have the same *DimensionCount* and *Sizes*, although they may differ in *DataType*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ee9c-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="1ee9c-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="1ee9c-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="1ee9c-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee9c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ee9c-108">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="1ee9c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="1ee9c-109">Members</span></span>

`InputTensor`

<span data-ttu-id="1ee9c-110">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1ee9c-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1ee9c-111">Tenseur d’entrée à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-111">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="1ee9c-112">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1ee9c-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1ee9c-113">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-113">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="1ee9c-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="1ee9c-114">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0,   123], // 0b0000000000, 0b0001111011
 [456, 789]] // 0b0111001000, 0b1100010101

OutputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0, 6],
 [4, 5]]
```

## <a name="availability"></a><span data-ttu-id="1ee9c-115">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="1ee9c-115">Availability</span></span>
<span data-ttu-id="1ee9c-116">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="1ee9c-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="1ee9c-117">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="1ee9c-117">Tensor constraints</span></span>
<span data-ttu-id="1ee9c-118">*InputTensor* et *OutputTensor* doivent avoir les mêmes *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="1ee9c-118">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="1ee9c-119">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="1ee9c-119">Tensor support</span></span>
| <span data-ttu-id="1ee9c-120">Tenseur</span><span class="sxs-lookup"><span data-stu-id="1ee9c-120">Tensor</span></span> | <span data-ttu-id="1ee9c-121">Type</span><span class="sxs-lookup"><span data-stu-id="1ee9c-121">Kind</span></span> | <span data-ttu-id="1ee9c-122">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="1ee9c-122">Supported dimension counts</span></span> | <span data-ttu-id="1ee9c-123">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ee9c-123">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1ee9c-124">InputTensor</span><span class="sxs-lookup"><span data-stu-id="1ee9c-124">InputTensor</span></span> | <span data-ttu-id="1ee9c-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="1ee9c-125">Input</span></span> | <span data-ttu-id="1ee9c-126">1 à 8</span><span class="sxs-lookup"><span data-stu-id="1ee9c-126">1 to 8</span></span> | <span data-ttu-id="1ee9c-127">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="1ee9c-127">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="1ee9c-128">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="1ee9c-128">OutputTensor</span></span> | <span data-ttu-id="1ee9c-129">Output</span><span class="sxs-lookup"><span data-stu-id="1ee9c-129">Output</span></span> | <span data-ttu-id="1ee9c-130">1 à 8</span><span class="sxs-lookup"><span data-stu-id="1ee9c-130">1 to 8</span></span> | <span data-ttu-id="1ee9c-131">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="1ee9c-131">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="1ee9c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ee9c-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1ee9c-133">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="1ee9c-133">**Header**</span></span> | <span data-ttu-id="1ee9c-134">directml. h</span><span class="sxs-lookup"><span data-stu-id="1ee9c-134">directml.h</span></span> |