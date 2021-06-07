---
UID: NS:directml.DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
title: DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
description: Remplit un tenseur avec une séquence.
helpviewer_keywords:
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure
- direct3d12.dml_fill_value_sequence_operator_desc
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
ms.openlocfilehash: 17b503630db2108dc4d9d2f5c2f32f7e324189d1
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417309"
---
# <a name="dml_fill_value_sequence_operator_desc-structure-directmlh"></a><span data-ttu-id="8fe1c-103">Structure DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="8fe1c-103">DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="8fe1c-104">Remplit un tenseur avec une séquence.</span><span class="sxs-lookup"><span data-stu-id="8fe1c-104">Fills a tensor with a sequence.</span></span> <span data-ttu-id="8fe1c-105">Cet opérateur effectue le pseudo-code suivant.</span><span class="sxs-lookup"><span data-stu-id="8fe1c-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
    Value += Delta
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="8fe1c-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8fe1c-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="8fe1c-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="8fe1c-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe1c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fe1c-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      ValueStart;
  DML_SCALAR_UNION      ValueDelta;
};
```



## <a name="members"></a><span data-ttu-id="8fe1c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="8fe1c-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="8fe1c-110">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8fe1c-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8fe1c-111">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="8fe1c-111">The tensor to write the results to.</span></span> <span data-ttu-id="8fe1c-112">Ce tenseur peut avoir n’importe quelle taille.</span><span class="sxs-lookup"><span data-stu-id="8fe1c-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="8fe1c-113">Type : **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="8fe1c-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="8fe1c-114">Type de données du champ de *valeur* , qui doit correspondre à *OutputTensor. DataType*.</span><span class="sxs-lookup"><span data-stu-id="8fe1c-114">The data type of *Value* field, which must match *OutputTensor.DataType*.</span></span>


`ValueStart`

<span data-ttu-id="8fe1c-115">Type : **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="8fe1c-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="8fe1c-116">Valeur initiale pour remplir le premier élément de la sortie, avec *ValueDataType* déterminant comment interpréter le champ.</span><span class="sxs-lookup"><span data-stu-id="8fe1c-116">The initial value to fill the first element in the output, with *ValueDataType* determining how to interpret the field.</span></span>


`ValueDelta`

<span data-ttu-id="8fe1c-117">Type : **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="8fe1c-117">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="8fe1c-118">Étape à ajouter à la valeur pour chaque élément écrit, avec *ValueDataType* déterminant comment interpréter le champ.</span><span class="sxs-lookup"><span data-stu-id="8fe1c-118">A step to add to the value for each element written, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="8fe1c-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="8fe1c-119">Examples</span></span>

### <a name="example-1-1d-ascending-step"></a><span data-ttu-id="8fe1c-120">Exemple 1.</span><span class="sxs-lookup"><span data-stu-id="8fe1c-120">Example 1.</span></span> <span data-ttu-id="8fe1c-121">étape d’ordre croissant 1D</span><span class="sxs-lookup"><span data-stu-id="8fe1c-121">1D ascending step</span></span>

```
ValueStart = 3
ValueDelta = 2
ValueDataType = DML_TENSOR_DATA_TYPE_FLOAT32

OutputTensor: (Sizes:{1,1,1,3}, DataType:FLOAT32)
    [[[[3, 5, 7]]]]
```

### <a name="example-2-2d-ascending-step"></a><span data-ttu-id="8fe1c-122">Exemple 2.</span><span class="sxs-lookup"><span data-stu-id="8fe1c-122">Example 2.</span></span> <span data-ttu-id="8fe1c-123">étape croissante 2D</span><span class="sxs-lookup"><span data-stu-id="8fe1c-123">2D ascending step</span></span>

```
ValueStart = 10
ValueDelta = -2
ValueDataType = DML_TENSOR_DATA_TYPE_UINT8

OutputTensor: (Sizes:{1,1,2,2}, DataType:UINT8)
    [[[[10, 8],
       [ 6, 4]]]]
```

## <a name="availability"></a><span data-ttu-id="8fe1c-124">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="8fe1c-124">Availability</span></span>
<span data-ttu-id="8fe1c-125">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="8fe1c-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8fe1c-126">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="8fe1c-126">Tensor support</span></span>
| <span data-ttu-id="8fe1c-127">Tenseur</span><span class="sxs-lookup"><span data-stu-id="8fe1c-127">Tensor</span></span> | <span data-ttu-id="8fe1c-128">Type</span><span class="sxs-lookup"><span data-stu-id="8fe1c-128">Kind</span></span> | <span data-ttu-id="8fe1c-129">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="8fe1c-129">Supported dimension counts</span></span> | <span data-ttu-id="8fe1c-130">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe1c-130">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8fe1c-131">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8fe1c-131">OutputTensor</span></span> | <span data-ttu-id="8fe1c-132">Sortie</span><span class="sxs-lookup"><span data-stu-id="8fe1c-132">Output</span></span> | <span data-ttu-id="8fe1c-133">4</span><span class="sxs-lookup"><span data-stu-id="8fe1c-133">4</span></span> | <span data-ttu-id="8fe1c-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8fe1c-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="8fe1c-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8fe1c-135">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8fe1c-136">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="8fe1c-136">**Header**</span></span> | <span data-ttu-id="8fe1c-137">directml. h</span><span class="sxs-lookup"><span data-stu-id="8fe1c-137">directml.h</span></span> |