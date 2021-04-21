---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Exécute une fonction de normalisation de variance moyenne sur le tenseur d’entrée. Cet opérateur calcule la moyenne et la variance du tenseur d’entrée pour effectuer la normalisation.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: 759bf25d4b6a97e70c6de7708a5c9fd0bccae439
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803399"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="63a7d-104">Structure DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="63a7d-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="63a7d-105">Exécute une fonction de normalisation de variance moyenne sur le tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="63a7d-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="63a7d-106">Cet opérateur calcule la moyenne et la variance du tenseur d’entrée pour effectuer la normalisation.</span><span class="sxs-lookup"><span data-stu-id="63a7d-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="63a7d-107">Cet opérateur effectue le calcul suivant.</span><span class="sxs-lookup"><span data-stu-id="63a7d-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="63a7d-108">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="63a7d-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="63a7d-109">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="63a7d-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="63a7d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63a7d-110">Syntax</span></span>
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```
## <a name="members"></a><span data-ttu-id="63a7d-111">Membres</span><span class="sxs-lookup"><span data-stu-id="63a7d-111">Members</span></span>

`InputTensor`

<span data-ttu-id="63a7d-112">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63a7d-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="63a7d-113">Tenseur contenant les données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="63a7d-113">A tensor containing the Input data.</span></span> <span data-ttu-id="63a7d-114">Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="63a7d-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="63a7d-115">Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63a7d-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="63a7d-116">Tenseur facultatif contenant les données de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="63a7d-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="63a7d-117">Si **DML_FEATURE_LEVEL** est inférieur à **DML_FEATURE_LEVEL_4_0**, les dimensions de ce tenseur doivent être `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` .</span><span class="sxs-lookup"><span data-stu-id="63a7d-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="63a7d-118">Les dimensions ScaleBatchCount, ScaleHeight et ScaleWidth doivent correspondre à *InputTensor*, ou être définies sur 1 pour diffuser automatiquement ces dimensions sur l’entrée.</span><span class="sxs-lookup"><span data-stu-id="63a7d-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="63a7d-119">Si **DML_FEATURE_LEVEL** est supérieur ou égal à **DML_FEATURE_LEVEL_4_0**, toute dimension peut être définie sur 1 et être automatiquement diffusée pour correspondre à *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="63a7d-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="63a7d-120">Ce tenseur est requis si le *BiasTensor* est utilisé.</span><span class="sxs-lookup"><span data-stu-id="63a7d-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="63a7d-121">Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63a7d-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="63a7d-122">Tenseur facultatif contenant les données de biais.</span><span class="sxs-lookup"><span data-stu-id="63a7d-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="63a7d-123">Si **DML_FEATURE_LEVEL** est inférieur à **DML_FEATURE_LEVEL_4_0**, les dimensions de ce tenseur doivent être `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` .</span><span class="sxs-lookup"><span data-stu-id="63a7d-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="63a7d-124">Les dimensions BiasBatchCount, BiasHeight et BiasWidth doivent correspondre à *InputTensor* ou être définies sur 1 pour diffuser automatiquement ces dimensions sur l’entrée.</span><span class="sxs-lookup"><span data-stu-id="63a7d-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="63a7d-125">Si **DML_FEATURE_LEVEL** est supérieur ou égal à **DML_FEATURE_LEVEL_4_0**, toute dimension peut être définie sur 1 et être automatiquement diffusée pour correspondre à *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="63a7d-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="63a7d-126">Ce tenseur est requis si le *ScaleTensor* est utilisé.</span><span class="sxs-lookup"><span data-stu-id="63a7d-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="63a7d-127">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63a7d-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="63a7d-128">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="63a7d-128">A tensor to write the results to.</span></span> <span data-ttu-id="63a7d-129">Les dimensions de ce tenseur sont `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="63a7d-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="63a7d-130">Type : <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="63a7d-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="63a7d-131">Nombre d’axes.</span><span class="sxs-lookup"><span data-stu-id="63a7d-131">The number of axes.</span></span> <span data-ttu-id="63a7d-132">Ce champ détermine la taille du tableau *axes* .</span><span class="sxs-lookup"><span data-stu-id="63a7d-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="63a7d-133">Type : \_ \_ taille \_ de champ (AxisCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="63a7d-133">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span> 

<span data-ttu-id="63a7d-134">Axes sur lesquels calculer la moyenne et la variance.</span><span class="sxs-lookup"><span data-stu-id="63a7d-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="63a7d-135">Type : <b> <a href="/windows/win32/winprog/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="63a7d-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="63a7d-136">**True** si la couche de normalisation comprend une variance dans le calcul de normalisation.</span><span class="sxs-lookup"><span data-stu-id="63a7d-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="63a7d-137">Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="63a7d-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="63a7d-138">Si la **valeur est false**, l’équation de normalisation est `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="63a7d-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="63a7d-139">Type : <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="63a7d-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="63a7d-140">Valeur Epsilon à utiliser pour éviter la division par zéro.</span><span class="sxs-lookup"><span data-stu-id="63a7d-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="63a7d-141">La valeur par défaut 0,00001 est recommandée.</span><span class="sxs-lookup"><span data-stu-id="63a7d-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="63a7d-142">Type : \_ MAYBENULL \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63a7d-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="63a7d-143">Couche d’activation fusionnée facultative à appliquer après la normalisation.</span><span class="sxs-lookup"><span data-stu-id="63a7d-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="63a7d-144">Notes </span><span class="sxs-lookup"><span data-stu-id="63a7d-144">Remarks</span></span>
<span data-ttu-id="63a7d-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** est un sur-ensemble de fonctionnalités de [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="63a7d-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="63a7d-146">Ici, la définition du tableau **axes** sur `{ 0, 2, 3 }` est l’équivalent de la définition de *CrossChannel* sur **false** dans **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; la définition du tableau **axes** sur équivaut à `{ 1, 2, 3 }` définir *CrossChannel* sur **true**.</span><span class="sxs-lookup"><span data-stu-id="63a7d-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="63a7d-147">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="63a7d-147">Availability</span></span>
<span data-ttu-id="63a7d-148">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="63a7d-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="63a7d-149">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="63a7d-149">Tensor constraints</span></span>

<span data-ttu-id="63a7d-150">*BiasTensor*, *InputTensor*, *OutputTensor* et *ScaleTensor* doivent avoir le même *type de données* et *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="63a7d-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="63a7d-151">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="63a7d-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="63a7d-152">DML_FEATURE_LEVEL_3_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="63a7d-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="63a7d-153">Tenseur</span><span class="sxs-lookup"><span data-stu-id="63a7d-153">Tensor</span></span> | <span data-ttu-id="63a7d-154">Type</span><span class="sxs-lookup"><span data-stu-id="63a7d-154">Kind</span></span> | <span data-ttu-id="63a7d-155">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="63a7d-155">Supported dimension counts</span></span> | <span data-ttu-id="63a7d-156">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="63a7d-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="63a7d-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="63a7d-157">InputTensor</span></span> | <span data-ttu-id="63a7d-158">Entrée</span><span class="sxs-lookup"><span data-stu-id="63a7d-158">Input</span></span> | <span data-ttu-id="63a7d-159">1 à 8</span><span class="sxs-lookup"><span data-stu-id="63a7d-159">1 to 8</span></span> | <span data-ttu-id="63a7d-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63a7d-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="63a7d-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="63a7d-161">ScaleTensor</span></span> | <span data-ttu-id="63a7d-162">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="63a7d-162">Optional input</span></span> | <span data-ttu-id="63a7d-163">1 à 8</span><span class="sxs-lookup"><span data-stu-id="63a7d-163">1 to 8</span></span> | <span data-ttu-id="63a7d-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63a7d-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="63a7d-165">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="63a7d-165">BiasTensor</span></span> | <span data-ttu-id="63a7d-166">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="63a7d-166">Optional input</span></span> | <span data-ttu-id="63a7d-167">1 à 8</span><span class="sxs-lookup"><span data-stu-id="63a7d-167">1 to 8</span></span> | <span data-ttu-id="63a7d-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63a7d-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="63a7d-169">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="63a7d-169">OutputTensor</span></span> | <span data-ttu-id="63a7d-170">Output</span><span class="sxs-lookup"><span data-stu-id="63a7d-170">Output</span></span> | <span data-ttu-id="63a7d-171">1 à 8</span><span class="sxs-lookup"><span data-stu-id="63a7d-171">1 to 8</span></span> | <span data-ttu-id="63a7d-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63a7d-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="63a7d-173">DML_FEATURE_LEVEL_2_1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="63a7d-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="63a7d-174">Tenseur</span><span class="sxs-lookup"><span data-stu-id="63a7d-174">Tensor</span></span> | <span data-ttu-id="63a7d-175">Type</span><span class="sxs-lookup"><span data-stu-id="63a7d-175">Kind</span></span> | <span data-ttu-id="63a7d-176">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="63a7d-176">Supported dimension counts</span></span> | <span data-ttu-id="63a7d-177">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="63a7d-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="63a7d-178">InputTensor</span><span class="sxs-lookup"><span data-stu-id="63a7d-178">InputTensor</span></span> | <span data-ttu-id="63a7d-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="63a7d-179">Input</span></span> | <span data-ttu-id="63a7d-180">4</span><span class="sxs-lookup"><span data-stu-id="63a7d-180">4</span></span> | <span data-ttu-id="63a7d-181">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63a7d-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="63a7d-182">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="63a7d-182">ScaleTensor</span></span> | <span data-ttu-id="63a7d-183">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="63a7d-183">Optional input</span></span> | <span data-ttu-id="63a7d-184">4</span><span class="sxs-lookup"><span data-stu-id="63a7d-184">4</span></span> | <span data-ttu-id="63a7d-185">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63a7d-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="63a7d-186">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="63a7d-186">BiasTensor</span></span> | <span data-ttu-id="63a7d-187">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="63a7d-187">Optional input</span></span> | <span data-ttu-id="63a7d-188">4</span><span class="sxs-lookup"><span data-stu-id="63a7d-188">4</span></span> | <span data-ttu-id="63a7d-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63a7d-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="63a7d-190">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="63a7d-190">OutputTensor</span></span> | <span data-ttu-id="63a7d-191">Output</span><span class="sxs-lookup"><span data-stu-id="63a7d-191">Output</span></span> | <span data-ttu-id="63a7d-192">4</span><span class="sxs-lookup"><span data-stu-id="63a7d-192">4</span></span> | <span data-ttu-id="63a7d-193">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="63a7d-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="63a7d-194">Spécifications</span><span class="sxs-lookup"><span data-stu-id="63a7d-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="63a7d-195">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="63a7d-195">**Header**</span></span> | <span data-ttu-id="63a7d-196">directml. h</span><span class="sxs-lookup"><span data-stu-id="63a7d-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="63a7d-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63a7d-197">See also</span></span>

[<span data-ttu-id="63a7d-198">Utilisation d’opérateurs fusionnés pour améliorer les performances</span><span class="sxs-lookup"><span data-stu-id="63a7d-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)
