---
UID: NS:directml.DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
title: DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
description: Remplit un tenseur avec la *valeur* de constante donnée.
helpviewer_keywords:
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure
- direct3d12.dml_fill_value_constant_operator_desc
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.openlocfilehash: d2b69f1f6b1c9768c24cab9a58bba3c3cadb04bb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106542076"
---
# <a name="dml_fill_value_constant_operator_desc-structure-directmlh"></a><span data-ttu-id="9bfbb-103">Structure DML_FILL_VALUE_CONSTANT_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="9bfbb-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="9bfbb-104">Remplit un tenseur avec la *valeur* de constante donnée.</span><span class="sxs-lookup"><span data-stu-id="9bfbb-104">Fills a tensor with the given constant *Value*.</span></span> <span data-ttu-id="9bfbb-105">Cet opérateur effectue le pseudo-code suivant.</span><span class="sxs-lookup"><span data-stu-id="9bfbb-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="9bfbb-106">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="9bfbb-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="9bfbb-107">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="9bfbb-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9bfbb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9bfbb-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_CONSTANT_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      Value;
};
```



## <a name="members"></a><span data-ttu-id="9bfbb-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9bfbb-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="9bfbb-110">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9bfbb-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9bfbb-111">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="9bfbb-111">The tensor to write the results to.</span></span> <span data-ttu-id="9bfbb-112">Ce tenseur peut avoir n’importe quelle taille.</span><span class="sxs-lookup"><span data-stu-id="9bfbb-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="9bfbb-113">Type : **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="9bfbb-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="9bfbb-114">Type de données du champ de *valeur* , qui doit correspondre à *OutputTensor. DataType*.</span><span class="sxs-lookup"><span data-stu-id="9bfbb-114">The data type of the *Value* field, which must match *OutputTensor.DataType*.</span></span>


`Value`

<span data-ttu-id="9bfbb-115">Type : **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="9bfbb-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="9bfbb-116">Valeur de constante pour remplir la sortie, avec *ValueDataType* déterminant comment interpréter le champ.</span><span class="sxs-lookup"><span data-stu-id="9bfbb-116">A constant value to fill the output, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="9bfbb-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="9bfbb-117">Examples</span></span>

```
Value = 13.0

OutputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
    [[[[13.0f, 13.0f, 13.0f, 13.0f],
       [13.0f, 13.0f, 13.0f, 13.0f]]]]
```

## <a name="availability"></a><span data-ttu-id="9bfbb-118">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="9bfbb-118">Availability</span></span>
<span data-ttu-id="9bfbb-119">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="9bfbb-119">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="9bfbb-120">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="9bfbb-120">Tensor support</span></span>
| <span data-ttu-id="9bfbb-121">Tenseur</span><span class="sxs-lookup"><span data-stu-id="9bfbb-121">Tensor</span></span> | <span data-ttu-id="9bfbb-122">Type</span><span class="sxs-lookup"><span data-stu-id="9bfbb-122">Kind</span></span> | <span data-ttu-id="9bfbb-123">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="9bfbb-123">Supported dimension counts</span></span> | <span data-ttu-id="9bfbb-124">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="9bfbb-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="9bfbb-125">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="9bfbb-125">OutputTensor</span></span> | <span data-ttu-id="9bfbb-126">Output</span><span class="sxs-lookup"><span data-stu-id="9bfbb-126">Output</span></span> | <span data-ttu-id="9bfbb-127">4</span><span class="sxs-lookup"><span data-stu-id="9bfbb-127">4</span></span> | <span data-ttu-id="9bfbb-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="9bfbb-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="9bfbb-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bfbb-129">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9bfbb-130">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="9bfbb-130">**Header**</span></span> | <span data-ttu-id="9bfbb-131">directml. h</span><span class="sxs-lookup"><span data-stu-id="9bfbb-131">directml.h</span></span> |