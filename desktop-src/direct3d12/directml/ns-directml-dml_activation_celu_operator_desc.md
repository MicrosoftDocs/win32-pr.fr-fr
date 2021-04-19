---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTIVATION_CELU_OPERATOR_DESC
description: Exécute la fonction d’activation d’unité linéaire exponentielle (CELU) en continu dérivables sur chaque élément dans *InputTensor*, en plaçant le résultat dans l’élément correspondant de *OutputTensor*.
helpviewer_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- DML_ACTIVATION_CELU_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_CELU_OPERATOR_DESC, DML_ACTIVATION_CELU_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
ms.openlocfilehash: d474bd44c8a830117bb62927f4bda954a753b612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106525779"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a><span data-ttu-id="e08cb-103">Structure DML_ACTIVATION_CELU_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="e08cb-103">DML_ACTIVATION_CELU_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="e08cb-104">Exécute la fonction d’activation d’unité linéaire exponentielle (CELU) en continu dérivables sur chaque élément dans *InputTensor*, en plaçant le résultat dans l’élément correspondant de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="e08cb-104">Performs the continuously differentiable exponential linear unit (CELU) activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

<span data-ttu-id="e08cb-105">Où :</span><span class="sxs-lookup"><span data-stu-id="e08cb-105">Where:</span></span>
* <span data-ttu-id="e08cb-106">exp (x) est la fonction d’élévation naturelle</span><span class="sxs-lookup"><span data-stu-id="e08cb-106">exp(x) is the natural exponentiation function</span></span>
* <span data-ttu-id="e08cb-107">Max (a, b) retourne la plus grande des deux valeurs a, b</span><span class="sxs-lookup"><span data-stu-id="e08cb-107">max(a,b) returns the larger of the two values a,b</span></span>
* <span data-ttu-id="e08cb-108">min (a, b) retourne la plus petite des deux valeurs a, b</span><span class="sxs-lookup"><span data-stu-id="e08cb-108">min(a,b) returns the smaller of the two values a,b</span></span>

<span data-ttu-id="e08cb-109">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que le tenseur de sortie est autorisé à aliaser les *InputTensor* pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="e08cb-109">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e08cb-110">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="e08cb-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="e08cb-111">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e08cb-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e08cb-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e08cb-112">Syntax</span></span>
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a><span data-ttu-id="e08cb-113">Membres</span><span class="sxs-lookup"><span data-stu-id="e08cb-113">Members</span></span>

`InputTensor`

<span data-ttu-id="e08cb-114">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e08cb-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e08cb-115">Tenseur d’entrée à partir duquel effectuer la lecture.</span><span class="sxs-lookup"><span data-stu-id="e08cb-115">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="e08cb-116">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="e08cb-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="e08cb-117">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="e08cb-117">The output tensor to write the results to.</span></span>

`Alpha`

<span data-ttu-id="e08cb-118">Type : <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="e08cb-118">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="e08cb-119">Coefficient alpha.</span><span class="sxs-lookup"><span data-stu-id="e08cb-119">The alpha coefficient.</span></span> <span data-ttu-id="e08cb-120">La valeur par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="e08cb-120">A typical default for this value is 1.0.</span></span>

## <a name="availability"></a><span data-ttu-id="e08cb-121">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="e08cb-121">Availability</span></span>
<span data-ttu-id="e08cb-122">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="e08cb-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e08cb-123">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="e08cb-123">Tensor constraints</span></span>
<span data-ttu-id="e08cb-124">*InputTensor* et *OutputTensor* doivent avoir les mêmes *types de données*, *DimensionCount* et *tailles*.</span><span class="sxs-lookup"><span data-stu-id="e08cb-124">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="e08cb-125">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="e08cb-125">Tensor support</span></span>
| <span data-ttu-id="e08cb-126">Tenseur</span><span class="sxs-lookup"><span data-stu-id="e08cb-126">Tensor</span></span> | <span data-ttu-id="e08cb-127">Type</span><span class="sxs-lookup"><span data-stu-id="e08cb-127">Kind</span></span> | <span data-ttu-id="e08cb-128">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="e08cb-128">Supported Dimension Counts</span></span> | <span data-ttu-id="e08cb-129">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="e08cb-129">Supported Data Types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="e08cb-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="e08cb-130">InputTensor</span></span> | <span data-ttu-id="e08cb-131">Entrée</span><span class="sxs-lookup"><span data-stu-id="e08cb-131">Input</span></span> | <span data-ttu-id="e08cb-132">1 à 8</span><span class="sxs-lookup"><span data-stu-id="e08cb-132">1 to 8</span></span> | <span data-ttu-id="e08cb-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e08cb-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="e08cb-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="e08cb-134">OutputTensor</span></span> | <span data-ttu-id="e08cb-135">Output</span><span class="sxs-lookup"><span data-stu-id="e08cb-135">Output</span></span> | <span data-ttu-id="e08cb-136">1 à 8</span><span class="sxs-lookup"><span data-stu-id="e08cb-136">1 to 8</span></span> | <span data-ttu-id="e08cb-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="e08cb-137">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="e08cb-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e08cb-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e08cb-139">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="e08cb-139">**Header**</span></span> | <span data-ttu-id="e08cb-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="e08cb-140">directml.h</span></span> |