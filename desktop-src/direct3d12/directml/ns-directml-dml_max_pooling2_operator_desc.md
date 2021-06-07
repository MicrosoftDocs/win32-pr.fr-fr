---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Calcule la valeur maximale sur les éléments au sein de la fenêtre glissante sur le tenseur d’entrée, et retourne éventuellement les index des valeurs maximales sélectionnées.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417264"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a><span data-ttu-id="4efbc-103">Structure DML_MAX_POOLING2_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="4efbc-103">DML_MAX_POOLING2_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="4efbc-104">Calcule la valeur maximale sur les éléments au sein de la fenêtre glissante sur le tenseur d’entrée, et retourne éventuellement les index des valeurs maximales sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="4efbc-104">Computes the maximum value across the elements within the sliding window over the input tensor, and optionally returns the indices of the maximum values selected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4efbc-105">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4efbc-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4efbc-106">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="4efbc-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4efbc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4efbc-107">Syntax</span></span>
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a><span data-ttu-id="4efbc-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4efbc-108">Members</span></span>

`InputTensor`

<span data-ttu-id="4efbc-109">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4efbc-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4efbc-110">Un tenseur d’entrée de *tailles* `{ BatchCount, ChannelCount, Height, Width }` si *InputTensor. DimensionCount* est 4 et `{ BatchCount, ChannelCount, Depth, Height, Weight } ` si *InputTensor. DimensionCount* est 5.</span><span class="sxs-lookup"><span data-stu-id="4efbc-110">An input tensor of *Sizes* `{ BatchCount, ChannelCount, Height, Width }` if *InputTensor.DimensionCount* is 4, and `{ BatchCount, ChannelCount, Depth, Height, Weight } `if *InputTensor.DimensionCount* is 5.</span></span>


`OutputTensor`

<span data-ttu-id="4efbc-111">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4efbc-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4efbc-112">Tenseur de sortie dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="4efbc-112">An output tensor to write the results to.</span></span> <span data-ttu-id="4efbc-113">Les tailles du tenseur de sortie peuvent être calculées comme suit.</span><span class="sxs-lookup"><span data-stu-id="4efbc-113">The sizes of the output tensor can be computed as follows.</span></span>

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

<span data-ttu-id="4efbc-114">Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4efbc-114">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4efbc-115">Tenseur de sortie facultative des index sur le tenseur d’entrée *InputTensor* des valeurs maximales produites et stockées dans le *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="4efbc-115">An optional output tensor of indices to the input tensor *InputTensor* of the maximum values produced and stored in the *OutputTensor*.</span></span> <span data-ttu-id="4efbc-116">Ces valeurs d’index sont de base zéro et traitent le tenseur d’entrée comme un tableau unidimensionnel contigu.</span><span class="sxs-lookup"><span data-stu-id="4efbc-116">These index values are zero-based and treat the input tensor as a contiguous one-dimensional array.</span></span> <span data-ttu-id="4efbc-117">Lorsque plusieurs éléments de la fenêtre glissante ont la même valeur, les valeurs égales ultérieures sont ignorées et l’index pointe vers la première valeur rencontrée.</span><span class="sxs-lookup"><span data-stu-id="4efbc-117">When multiple elements within the sliding window have the same value, the later equal values are ignored and the index points to the first value encountered.</span></span> <span data-ttu-id="4efbc-118">*OutputTensor* et *OutputIndicesTensor* ont les mêmes tailles de tenseur.</span><span class="sxs-lookup"><span data-stu-id="4efbc-118">Both the *OutputTensor* and *OutputIndicesTensor* have the same tensor sizes.</span></span>


`DimensionCount`

<span data-ttu-id="4efbc-119">Type : [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4efbc-119">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4efbc-120">Nombre de dimensions spatiales du *InputTensor* d’entrée tenseur, qui correspond également au nombre de dimensions de la fenêtre glissante *Windows*.</span><span class="sxs-lookup"><span data-stu-id="4efbc-120">The number of spatial dimensions of the input tensor *InputTensor*, which also corresponds to the number of dimensions of the sliding window *WindowSize*.</span></span> <span data-ttu-id="4efbc-121">Cette valeur détermine également la taille des tableaux *Strides*, *StartPadding* et *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="4efbc-121">This value also determines the size of the *Strides*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="4efbc-122">Elle doit être définie sur 2 lorsque *InputTensor* est 4D et 3 lorsqu’il s’agit d’un 5D tenseur.</span><span class="sxs-lookup"><span data-stu-id="4efbc-122">It should be set to 2 when *InputTensor* is 4D, and 3 when it's a 5D tensor.</span></span>


`Strides`

<span data-ttu-id="4efbc-123">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4efbc-123">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4efbc-124">Strides pour les dimensions de fenêtre glissante de tailles `{ Height, Width }` lorsque *DimensionCount* a la valeur 2, ou `{ Depth, Height, Width }` lorsque la valeur 3 est affectée à.</span><span class="sxs-lookup"><span data-stu-id="4efbc-124">The strides for the sliding window dimensions of sizes `{ Height, Width }` when the *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`WindowSize`

<span data-ttu-id="4efbc-125">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4efbc-125">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4efbc-126">Dimensions de la fenêtre glissante dans `{ Height, Width }` lorsque *DimensionCount* a la valeur 2, ou `{ Depth, Height, Width }` lorsque la valeur est égale à 3.</span><span class="sxs-lookup"><span data-stu-id="4efbc-126">The dimensions of the sliding window in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`StartPadding`

<span data-ttu-id="4efbc-127">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4efbc-127">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4efbc-128">Nombre d’éléments de remplissage à appliquer au début de chaque dimension spatiale du *InputTensor* d’entrée tenseur.</span><span class="sxs-lookup"><span data-stu-id="4efbc-128">The number of padding elements to be applied to the beginning of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="4efbc-129">Les valeurs se trouvent dans `{ Height, Width }` lorsque *DimensionCount* a la valeur 2, ou lorsque la `{ Depth, Height, Width }` valeur est égale à 3.</span><span class="sxs-lookup"><span data-stu-id="4efbc-129">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`EndPadding`

<span data-ttu-id="4efbc-130">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4efbc-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4efbc-131">Nombre d’éléments de remplissage à appliquer à la fin de chaque dimension spatiale du *InputTensor* d’entrée tenseur.</span><span class="sxs-lookup"><span data-stu-id="4efbc-131">The number of padding elements to be applied to the end of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="4efbc-132">Les valeurs se trouvent dans `{ Height, Width }` lorsque *DimensionCount* a la valeur 2, ou lorsque la `{ Depth, Height, Width }` valeur est égale à 3.</span><span class="sxs-lookup"><span data-stu-id="4efbc-132">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`Dilations`

<span data-ttu-id="4efbc-133">Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4efbc-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4efbc-134">Valeurs pour chaque dimension spatiale du tenseur d’entrée *InputTensor* par lequel un élément de la fenêtre glissante est sélectionné pour chaque élément de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="4efbc-134">The values for each spatial dimension of the input tensor *InputTensor* by which an element within the sliding window is selected for every elements of that value.</span></span> <span data-ttu-id="4efbc-135">Les valeurs se trouvent dans `{ Height, Width }` lorsque *DimensionCount* a la valeur 2, ou lorsque la `{ Depth, Height, Width }` valeur est égale à 3.</span><span class="sxs-lookup"><span data-stu-id="4efbc-135">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


## <a name="remarks"></a><span data-ttu-id="4efbc-136">Remarques</span><span class="sxs-lookup"><span data-stu-id="4efbc-136">Remarks</span></span>
<span data-ttu-id="4efbc-137">**DML_MAX_POOLING2_OPERATOR_DESC** remplace la version antérieure [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) par des *dilatations* de tableau constantes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4efbc-137">**DML_MAX_POOLING2_OPERATOR_DESC** supersedes the earlier version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) with an additional constant array *Dilations*.</span></span> <span data-ttu-id="4efbc-138">Les deux versions sont équivalentes lorsque la valeur de *dilatations* est définie sur `{ 1,1 }` pour une entrée 4D, ou `{ 1,1,1 }` pour les fonctionnalités d’entrée de 5D.</span><span class="sxs-lookup"><span data-stu-id="4efbc-138">The two versions are equivalent when *Dilations* is set to `{ 1,1 }` for 4D input, or `{ 1,1,1 }` for 5D input features.</span></span>

## <a name="availability"></a><span data-ttu-id="4efbc-139">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="4efbc-139">Availability</span></span>
<span data-ttu-id="4efbc-140">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="4efbc-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4efbc-141">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="4efbc-141">Tensor constraints</span></span>
* <span data-ttu-id="4efbc-142">*InputTensor*, *OutputIndicesTensor* et *OutputTensor* doivent avoir le même *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="4efbc-142">*InputTensor*, *OutputIndicesTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="4efbc-143">*InputTensor* et *OutputTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="4efbc-143">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4efbc-144">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="4efbc-144">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="4efbc-145">DML_FEATURE_LEVEL_3_0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="4efbc-145">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="4efbc-146">Tenseur</span><span class="sxs-lookup"><span data-stu-id="4efbc-146">Tensor</span></span> | <span data-ttu-id="4efbc-147">Type</span><span class="sxs-lookup"><span data-stu-id="4efbc-147">Kind</span></span> | <span data-ttu-id="4efbc-148">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="4efbc-148">Supported dimension counts</span></span> | <span data-ttu-id="4efbc-149">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="4efbc-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4efbc-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4efbc-150">InputTensor</span></span> | <span data-ttu-id="4efbc-151">Entrée</span><span class="sxs-lookup"><span data-stu-id="4efbc-151">Input</span></span> | <span data-ttu-id="4efbc-152">4 à 5</span><span class="sxs-lookup"><span data-stu-id="4efbc-152">4 to 5</span></span> | <span data-ttu-id="4efbc-153">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4efbc-153">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="4efbc-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="4efbc-154">OutputTensor</span></span> | <span data-ttu-id="4efbc-155">Sortie</span><span class="sxs-lookup"><span data-stu-id="4efbc-155">Output</span></span> | <span data-ttu-id="4efbc-156">4 à 5</span><span class="sxs-lookup"><span data-stu-id="4efbc-156">4 to 5</span></span> | <span data-ttu-id="4efbc-157">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4efbc-157">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="4efbc-158">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="4efbc-158">OutputIndicesTensor</span></span> | <span data-ttu-id="4efbc-159">Sortie facultative</span><span class="sxs-lookup"><span data-stu-id="4efbc-159">Optional output</span></span> | <span data-ttu-id="4efbc-160">4 à 5</span><span class="sxs-lookup"><span data-stu-id="4efbc-160">4 to 5</span></span> | <span data-ttu-id="4efbc-161">UINT32</span><span class="sxs-lookup"><span data-stu-id="4efbc-161">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="4efbc-162">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="4efbc-162">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="4efbc-163">Tenseur</span><span class="sxs-lookup"><span data-stu-id="4efbc-163">Tensor</span></span> | <span data-ttu-id="4efbc-164">Type</span><span class="sxs-lookup"><span data-stu-id="4efbc-164">Kind</span></span> | <span data-ttu-id="4efbc-165">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="4efbc-165">Supported dimension counts</span></span> | <span data-ttu-id="4efbc-166">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="4efbc-166">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4efbc-167">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4efbc-167">InputTensor</span></span> | <span data-ttu-id="4efbc-168">Entrée</span><span class="sxs-lookup"><span data-stu-id="4efbc-168">Input</span></span> | <span data-ttu-id="4efbc-169">4 à 5</span><span class="sxs-lookup"><span data-stu-id="4efbc-169">4 to 5</span></span> | <span data-ttu-id="4efbc-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4efbc-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="4efbc-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="4efbc-171">OutputTensor</span></span> | <span data-ttu-id="4efbc-172">Sortie</span><span class="sxs-lookup"><span data-stu-id="4efbc-172">Output</span></span> | <span data-ttu-id="4efbc-173">4 à 5</span><span class="sxs-lookup"><span data-stu-id="4efbc-173">4 to 5</span></span> | <span data-ttu-id="4efbc-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4efbc-174">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="4efbc-175">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="4efbc-175">OutputIndicesTensor</span></span> | <span data-ttu-id="4efbc-176">Sortie facultative</span><span class="sxs-lookup"><span data-stu-id="4efbc-176">Optional output</span></span> | <span data-ttu-id="4efbc-177">4 à 5</span><span class="sxs-lookup"><span data-stu-id="4efbc-177">4 to 5</span></span> | <span data-ttu-id="4efbc-178">UINT32</span><span class="sxs-lookup"><span data-stu-id="4efbc-178">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="4efbc-179">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4efbc-179">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4efbc-180">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="4efbc-180">**Minimum supported client**</span></span> | <span data-ttu-id="4efbc-181">Windows 10, version 2004 (10,0 ; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="4efbc-181">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="4efbc-182">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="4efbc-182">**Minimum supported server**</span></span> | <span data-ttu-id="4efbc-183">Windows Server, version 2004 (10,0 ; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="4efbc-183">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="4efbc-184">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="4efbc-184">**Header**</span></span> | <span data-ttu-id="4efbc-185">directml. h</span><span class="sxs-lookup"><span data-stu-id="4efbc-185">directml.h</span></span> |