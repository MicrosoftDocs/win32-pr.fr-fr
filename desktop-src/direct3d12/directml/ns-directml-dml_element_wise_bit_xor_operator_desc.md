---
UID: NS:directml.DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
description: Calcule l’opérateur de bits XOR (or exclusif) entre chaque élément correspondant des dizaines d’entrée et écrit le résultat dans le tenseur de sortie.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.openlocfilehash: fcedb2c33f1c63196a9e6783daaa9f2d863e99f0
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803184"
---
# <a name="dml_element_wise_bit_xor_operator_desc-structure-directmlh"></a><span data-ttu-id="433e7-103">Structure DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="433e7-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="433e7-104">Calcule l’opérateur de bits XOR (or exclusif) entre chaque élément correspondant des dizaines d’entrée et écrit le résultat dans le tenseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="433e7-104">Computes the bitwise XOR (eXclusive OR) between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="433e7-105">Les tenseur d’entrée et de sortie doivent avoir les mêmes *DimensionCount*, *taille* et *type de données*.</span><span class="sxs-lookup"><span data-stu-id="433e7-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="433e7-106">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que le tenseur de sortie est autorisé à effectuer un alias d’un ou plusieurs des dizaines d’entrée pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="433e7-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="433e7-107">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="433e7-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="433e7-108">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="433e7-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="433e7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="433e7-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="433e7-110">Membres</span><span class="sxs-lookup"><span data-stu-id="433e7-110">Members</span></span>

`ATensor`

<span data-ttu-id="433e7-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="433e7-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="433e7-112">Tenseur contenant les entrées côté gauche.</span><span class="sxs-lookup"><span data-stu-id="433e7-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="433e7-113">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="433e7-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="433e7-114">Tenseur contenant les entrées côté droit.</span><span class="sxs-lookup"><span data-stu-id="433e7-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="433e7-115">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="433e7-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="433e7-116">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="433e7-116">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="433e7-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="433e7-117">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="433e7-118">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="433e7-118">Availability</span></span>
<span data-ttu-id="433e7-119">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="433e7-119">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="433e7-120">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="433e7-120">Tensor constraints</span></span>
<span data-ttu-id="433e7-121">*ATensor*, *BTensor* et *OutputTensor* doivent avoir le même *type de données*, *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="433e7-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="433e7-122">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="433e7-122">Tensor support</span></span>
| <span data-ttu-id="433e7-123">Tenseur</span><span class="sxs-lookup"><span data-stu-id="433e7-123">Tensor</span></span> | <span data-ttu-id="433e7-124">Type</span><span class="sxs-lookup"><span data-stu-id="433e7-124">Kind</span></span> | <span data-ttu-id="433e7-125">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="433e7-125">Supported dimension counts</span></span> | <span data-ttu-id="433e7-126">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="433e7-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="433e7-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="433e7-127">ATensor</span></span> | <span data-ttu-id="433e7-128">Entrée</span><span class="sxs-lookup"><span data-stu-id="433e7-128">Input</span></span> | <span data-ttu-id="433e7-129">1 à 8</span><span class="sxs-lookup"><span data-stu-id="433e7-129">1 to 8</span></span> | <span data-ttu-id="433e7-130">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="433e7-130">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="433e7-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="433e7-131">BTensor</span></span> | <span data-ttu-id="433e7-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="433e7-132">Input</span></span> | <span data-ttu-id="433e7-133">1 à 8</span><span class="sxs-lookup"><span data-stu-id="433e7-133">1 to 8</span></span> | <span data-ttu-id="433e7-134">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="433e7-134">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="433e7-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="433e7-135">OutputTensor</span></span> | <span data-ttu-id="433e7-136">Output</span><span class="sxs-lookup"><span data-stu-id="433e7-136">Output</span></span> | <span data-ttu-id="433e7-137">1 à 8</span><span class="sxs-lookup"><span data-stu-id="433e7-137">1 to 8</span></span> | <span data-ttu-id="433e7-138">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="433e7-138">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="433e7-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="433e7-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="433e7-140">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="433e7-140">**Header**</span></span> | <span data-ttu-id="433e7-141">directml. h</span><span class="sxs-lookup"><span data-stu-id="433e7-141">directml.h</span></span> |