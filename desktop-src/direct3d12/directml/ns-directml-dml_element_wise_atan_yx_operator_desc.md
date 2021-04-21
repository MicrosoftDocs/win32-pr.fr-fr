---
UID: NS:directml.DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
title: DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
description: Calcule l’arctangente à 2 arguments pour chaque élément de *ATensor* et *BTensor*, où *ATensor* est l' *axe Y* et *BTensor* est l' *axe X*, en plaçant le résultat dans l’élément correspondant de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.openlocfilehash: 6031f08dc99db943d26ab5212896b4fb44987269
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804451"
---
# <a name="dml_element_wise_atan_yx_operator_desc-directmlh"></a><span data-ttu-id="7f2c8-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="7f2c8-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="7f2c8-104">Calcule l’arctangente à 2 arguments pour chaque élément de *ATensor* et *BTensor*, où *ATensor* est l' *axe Y* et *BTensor* est l' *axe X*, en plaçant le résultat dans l’élément correspondant de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="7f2c8-104">Computes the 2-argument arctangent for each element of *ATensor* and *BTensor*, where *ATensor* is the *Y-axis* and *BTensor* is the *X-axis*, placing the result into the corresponding element of *OutputTensor*.</span></span> <span data-ttu-id="7f2c8-105">Cet opérateur n’est pas défini pour l’origine (autrement dit, quand *ATensor* et *BTensor* sont tous deux 0 pour les éléments correspondants).</span><span class="sxs-lookup"><span data-stu-id="7f2c8-105">This operator is undefined for the origin (that is, when *ATensor* and *BTensor* are both 0 for corresponding elements).</span></span>

![GRU_Forward](../images/atan2.png)

```
f(y, x) = atan2(y, x)
```

<span data-ttu-id="7f2c8-107">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que le tenseur de sortie est autorisé à aliaser *ATensor* ou *BTensor* pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="7f2c8-107">This operator supports in-place execution, meaning that the output tensor is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f2c8-108">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7f2c8-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="7f2c8-109">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="7f2c8-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f2c8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f2c8-110">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="7f2c8-111">Membres</span><span class="sxs-lookup"><span data-stu-id="7f2c8-111">Members</span></span>

`ATensor`

<span data-ttu-id="7f2c8-112">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7f2c8-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7f2c8-113">Tenseur d’entrée à partir duquel lire les valeurs de l’axe des Y.</span><span class="sxs-lookup"><span data-stu-id="7f2c8-113">The input tensor to read the Y-axis values from.</span></span>

`BTensor`

<span data-ttu-id="7f2c8-114">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7f2c8-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7f2c8-115">Tenseur d’entrée à partir duquel lire les valeurs de l’axe des X.</span><span class="sxs-lookup"><span data-stu-id="7f2c8-115">The input tensor to read the X-axis values from.</span></span>

`OutputTensor`

<span data-ttu-id="7f2c8-116">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7f2c8-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7f2c8-117">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="7f2c8-117">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="7f2c8-118">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="7f2c8-118">Availability</span></span>
<span data-ttu-id="7f2c8-119">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="7f2c8-119">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="7f2c8-120">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="7f2c8-120">Tensor constraints</span></span>
<span data-ttu-id="7f2c8-121">*ATensor*, *BTensor* et *OutputTensor* doivent avoir le même *type de données*, *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="7f2c8-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="7f2c8-122">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="7f2c8-122">Tensor support</span></span>
| <span data-ttu-id="7f2c8-123">Tenseur</span><span class="sxs-lookup"><span data-stu-id="7f2c8-123">Tensor</span></span> | <span data-ttu-id="7f2c8-124">Type</span><span class="sxs-lookup"><span data-stu-id="7f2c8-124">Kind</span></span> | <span data-ttu-id="7f2c8-125">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="7f2c8-125">Supported dimension counts</span></span> | <span data-ttu-id="7f2c8-126">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f2c8-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="7f2c8-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="7f2c8-127">ATensor</span></span> | <span data-ttu-id="7f2c8-128">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f2c8-128">Input</span></span> | <span data-ttu-id="7f2c8-129">1 à 8</span><span class="sxs-lookup"><span data-stu-id="7f2c8-129">1 to 8</span></span> | <span data-ttu-id="7f2c8-130">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="7f2c8-130">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="7f2c8-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="7f2c8-131">BTensor</span></span> | <span data-ttu-id="7f2c8-132">Entrée</span><span class="sxs-lookup"><span data-stu-id="7f2c8-132">Input</span></span> | <span data-ttu-id="7f2c8-133">1 à 8</span><span class="sxs-lookup"><span data-stu-id="7f2c8-133">1 to 8</span></span> | <span data-ttu-id="7f2c8-134">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="7f2c8-134">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="7f2c8-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="7f2c8-135">OutputTensor</span></span> | <span data-ttu-id="7f2c8-136">Output</span><span class="sxs-lookup"><span data-stu-id="7f2c8-136">Output</span></span> | <span data-ttu-id="7f2c8-137">1 à 8</span><span class="sxs-lookup"><span data-stu-id="7f2c8-137">1 to 8</span></span> | <span data-ttu-id="7f2c8-138">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="7f2c8-138">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="7f2c8-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7f2c8-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7f2c8-140">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="7f2c8-140">**Header**</span></span> | <span data-ttu-id="7f2c8-141">directml. h</span><span class="sxs-lookup"><span data-stu-id="7f2c8-141">directml.h</span></span> |
