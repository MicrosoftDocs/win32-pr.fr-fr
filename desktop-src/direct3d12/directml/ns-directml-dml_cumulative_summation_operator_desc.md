---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Additionne les éléments d’un tenseur le long d’un axe, en écrivant le haut de la somme en cours dans le tenseur de sortie.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 955e70a8cfbb57995d77d73567238d082b96999b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106520224"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="74328-103">Structure DML_CUMULATIVE_SUMMATION_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="74328-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="74328-104">Additionne les éléments d’un tenseur le long d’un axe, en écrivant le haut de la somme en cours dans le tenseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="74328-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74328-105">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="74328-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="74328-106">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="74328-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="74328-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74328-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```



## <a name="members"></a><span data-ttu-id="74328-108">Membres</span><span class="sxs-lookup"><span data-stu-id="74328-108">Members</span></span>

`InputTensor`

<span data-ttu-id="74328-109">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="74328-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="74328-110">Tenseur d’entrée contenant les éléments à additionner.</span><span class="sxs-lookup"><span data-stu-id="74328-110">The input tensor containing elements to be summed.</span></span>


`OutputTensor`

<span data-ttu-id="74328-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="74328-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="74328-112">Tenseur de sortie dans lequel écrire les sommes cumulées qui en résultent.</span><span class="sxs-lookup"><span data-stu-id="74328-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="74328-113">Ce tenseur doit avoir les mêmes tailles et le même type de données que le *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="74328-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="74328-114">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="74328-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="74328-115">Index de la dimension sur laquelle somme les éléments.</span><span class="sxs-lookup"><span data-stu-id="74328-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="74328-116">Cette valeur doit être inférieure à la *DimensionCount* du *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="74328-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`AxisDirection`

<span data-ttu-id="74328-117">Type : **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="74328-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="74328-118">L’une des valeurs de l’énumération [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="74328-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="74328-119">Si la valeur est **DML_AXIS_DIRECTION_INCREASING**, la somme se produit en parcourant le tenseur le long de l’axe spécifié par l’index d’élément croissant.</span><span class="sxs-lookup"><span data-stu-id="74328-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="74328-120">Si la valeur est **DML_AXIS_DIRECTION_DECREASING**, l’inverse est vrai et la somme se produit en parcourant les éléments par ordre décroissant d’index.</span><span class="sxs-lookup"><span data-stu-id="74328-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>


`HasExclusiveSum`




## <a name="remarks"></a><span data-ttu-id="74328-121">Notes</span><span class="sxs-lookup"><span data-stu-id="74328-121">Remarks</span></span>
<span data-ttu-id="74328-122">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que le *OutputTensor* est autorisé à aliaser le *InputTensor* au cours de la liaison.</span><span class="sxs-lookup"><span data-stu-id="74328-122">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="74328-123">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="74328-123">Availability</span></span>
<span data-ttu-id="74328-124">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="74328-124">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="74328-125">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="74328-125">Tensor constraints</span></span>
<span data-ttu-id="74328-126">*InputTensor* et *OutputTensor* doivent avoir le même *type de données* et les mêmes *tailles*.</span><span class="sxs-lookup"><span data-stu-id="74328-126">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="74328-127">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="74328-127">Tensor support</span></span>
| <span data-ttu-id="74328-128">Tenseur</span><span class="sxs-lookup"><span data-stu-id="74328-128">Tensor</span></span> | <span data-ttu-id="74328-129">Type</span><span class="sxs-lookup"><span data-stu-id="74328-129">Kind</span></span> | <span data-ttu-id="74328-130">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="74328-130">Supported dimension counts</span></span> | <span data-ttu-id="74328-131">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="74328-131">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="74328-132">InputTensor</span><span class="sxs-lookup"><span data-stu-id="74328-132">InputTensor</span></span> | <span data-ttu-id="74328-133">Entrée</span><span class="sxs-lookup"><span data-stu-id="74328-133">Input</span></span> | <span data-ttu-id="74328-134">4</span><span class="sxs-lookup"><span data-stu-id="74328-134">4</span></span> | <span data-ttu-id="74328-135">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="74328-135">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="74328-136">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="74328-136">OutputTensor</span></span> | <span data-ttu-id="74328-137">Output</span><span class="sxs-lookup"><span data-stu-id="74328-137">Output</span></span> | <span data-ttu-id="74328-138">4</span><span class="sxs-lookup"><span data-stu-id="74328-138">4</span></span> | <span data-ttu-id="74328-139">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="74328-139">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="74328-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74328-140">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="74328-141">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="74328-141">**Header**</span></span> | <span data-ttu-id="74328-142">directml. h</span><span class="sxs-lookup"><span data-stu-id="74328-142">directml.h</span></span> |