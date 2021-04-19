---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour le rééchantillonnage (voir [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 5808381f2e812ac20399b46672e51acd063bc6a5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106520225"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="03819-103">Structure DML_RESAMPLE_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="03819-103">DML_RESAMPLE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="03819-104">Calcule les dégradés de la rétropropagation pour le rééchantillonnage (voir [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="03819-104">Computes backpropagation gradients for Resample (see [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span></span>

<span data-ttu-id="03819-105">**DML_RESAMPLE1_OPERATOR_DESC** redimensionne les dimensions arbitraires du tenseur d’entrée à l’aide de l’échantillonnage ou de l’interpolation bilinéaire le plus proche voisin.</span><span class="sxs-lookup"><span data-stu-id="03819-105">**DML_RESAMPLE1_OPERATOR_DESC** rescales arbitrary dimensions of the input tensor using either nearest-neighbor sampling or bilinear interpolation.</span></span> <span data-ttu-id="03819-106">Étant donné un *InputGradientTensor* avec la même taille que la *sortie* d’un **DML_RESAMPLE1_OPERATOR_DESC** équivalent, cet opérateur produit un *OutputGradientTensor* avec les mêmes tailles que l' *entrée* de l' **DML_RESAMPLE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="03819-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_RESAMPLE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of the **DML_RESAMPLE1_OPERATOR_DESC**.</span></span>

<span data-ttu-id="03819-107">Par exemple, considérez un **DML_RESAMPLE1_OPERATOR_DESC** qui effectue une mise à l’échelle voisine la plus proche de 1,5 x dans la largeur, et 0,5 x dans la hauteur.</span><span class="sxs-lookup"><span data-stu-id="03819-107">As an example, consider a **DML_RESAMPLE1_OPERATOR_DESC** that performs a nearest-neighbor scaling of 1.5x in the width, and 0.5x in the height.</span></span>

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

<span data-ttu-id="03819-108">Notez que l’élément 0 du tenseur d’entrée (avec la valeur 1) contribue à deux éléments dans la sortie, le premier élément (avec la valeur 2) contribue à un élément dans la sortie, et les 2e et 3e éléments (avec les valeurs 3 et 4) contribuent à aucun élément de la sortie.</span><span class="sxs-lookup"><span data-stu-id="03819-108">Notice how the 0th element of the input tensor (with value 1) contributes to two elements in the output, the 1st element (with value 2) contributes to one element in the output, and the 2nd and 3rd elements (with values 3 and 4) contribute to no elements of the output.</span></span>

<span data-ttu-id="03819-109">Le **DML_RESAMPLE_GRAD_OPERATOR_DESC** correspondant doit effectuer les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="03819-109">The corresponding **DML_RESAMPLE_GRAD_OPERATOR_DESC** would perform the following.</span></span>

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

<span data-ttu-id="03819-110">Notez que les valeurs de *OutputGradientTensor* représentent les contributions pondérées de cet élément au *OutputTensor* au cours de l’opérateur de **DML_RESAMPLE1_OPERATOR_DESC** d’origine.</span><span class="sxs-lookup"><span data-stu-id="03819-110">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original **DML_RESAMPLE1_OPERATOR_DESC** operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03819-111">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="03819-111">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="03819-112">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="03819-112">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="03819-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03819-113">Syntax</span></span>

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a><span data-ttu-id="03819-114">Membres</span><span class="sxs-lookup"><span data-stu-id="03819-114">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="03819-115">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="03819-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="03819-116">Tenseur de dégradé entrant.</span><span class="sxs-lookup"><span data-stu-id="03819-116">The incoming gradient tensor.</span></span> <span data-ttu-id="03819-117">Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente.</span><span class="sxs-lookup"><span data-stu-id="03819-117">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="03819-118">En général, ce tenseur a la même taille que la *sortie* de la [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) correspondante dans la passe de transfert.</span><span class="sxs-lookup"><span data-stu-id="03819-118">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="03819-119">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="03819-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="03819-120">Tenseur de sortie contenant les dégradés de la page.</span><span class="sxs-lookup"><span data-stu-id="03819-120">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="03819-121">En général, ce tenseur a la même taille que l' *entrée* de la [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) correspondante dans la passe en avant.</span><span class="sxs-lookup"><span data-stu-id="03819-121">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`InterpolationMode`

<span data-ttu-id="03819-122">Type : [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="03819-122">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="03819-123">Consultez *InterpolationMode* dans [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="03819-123">See *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`DimensionCount`

<span data-ttu-id="03819-124">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="03819-124">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="03819-125">Nombre d’éléments dans les tableaux *échelles*, *InputPixelOffsets* et *OutputPixelOffsets* .</span><span class="sxs-lookup"><span data-stu-id="03819-125">The number of elements in the *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* arrays.</span></span> <span data-ttu-id="03819-126">Cette valeur doit être égale à la valeur de *DimensionCount* fournie dans *InputGradientTensor* et *OutputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="03819-126">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`Scales`

<span data-ttu-id="03819-127">Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="03819-127">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="03819-128">Consultez mettre à l' *échelle* dans [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="03819-128">See *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`InputPixelOffsets`

<span data-ttu-id="03819-129">Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="03819-129">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="03819-130">Consultez *InputPixelOffsets* dans [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="03819-130">See *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`OutputPixelOffsets`

<span data-ttu-id="03819-131">Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="03819-131">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="03819-132">Consultez *OutputPixelOffsets* dans [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="03819-132">See *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="03819-133">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="03819-133">Availability</span></span>
<span data-ttu-id="03819-134">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="03819-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="03819-135">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="03819-135">Tensor constraints</span></span>
<span data-ttu-id="03819-136">*InputGradientTensor* et *OutputGradientTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="03819-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="03819-137">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="03819-137">Tensor support</span></span>
| <span data-ttu-id="03819-138">Tenseur</span><span class="sxs-lookup"><span data-stu-id="03819-138">Tensor</span></span> | <span data-ttu-id="03819-139">Type</span><span class="sxs-lookup"><span data-stu-id="03819-139">Kind</span></span> | <span data-ttu-id="03819-140">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="03819-140">Supported dimension counts</span></span> | <span data-ttu-id="03819-141">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="03819-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="03819-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="03819-142">InputGradientTensor</span></span> | <span data-ttu-id="03819-143">Entrée</span><span class="sxs-lookup"><span data-stu-id="03819-143">Input</span></span> | <span data-ttu-id="03819-144">4</span><span class="sxs-lookup"><span data-stu-id="03819-144">4</span></span> | <span data-ttu-id="03819-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="03819-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="03819-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="03819-146">OutputGradientTensor</span></span> | <span data-ttu-id="03819-147">Output</span><span class="sxs-lookup"><span data-stu-id="03819-147">Output</span></span> | <span data-ttu-id="03819-148">4</span><span class="sxs-lookup"><span data-stu-id="03819-148">4</span></span> | <span data-ttu-id="03819-149">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="03819-149">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="03819-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03819-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="03819-151">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="03819-151">**Header**</span></span> | <span data-ttu-id="03819-152">directml. h</span><span class="sxs-lookup"><span data-stu-id="03819-152">directml.h</span></span> |