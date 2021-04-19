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
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106531445"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="cefbc-104">Structure DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="cefbc-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="cefbc-105">Exécute une fonction de normalisation de variance moyenne sur le tenseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cefbc-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="cefbc-106">Cet opérateur calcule la moyenne et la variance du tenseur d’entrée pour effectuer la normalisation.</span><span class="sxs-lookup"><span data-stu-id="cefbc-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="cefbc-107">Cet opérateur effectue le calcul suivant.</span><span class="sxs-lookup"><span data-stu-id="cefbc-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="cefbc-108">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="cefbc-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="cefbc-109">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="cefbc-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cefbc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cefbc-110">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="cefbc-111">Membres</span><span class="sxs-lookup"><span data-stu-id="cefbc-111">Members</span></span>

`InputTensor`

<span data-ttu-id="cefbc-112">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cefbc-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cefbc-113">Tenseur contenant les données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cefbc-113">A tensor containing the Input data.</span></span> <span data-ttu-id="cefbc-114">Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="cefbc-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`ScaleTensor`

<span data-ttu-id="cefbc-115">Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cefbc-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cefbc-116">Tenseur facultatif contenant les données de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="cefbc-116">An optional tensor containing the Scale data.</span></span> <span data-ttu-id="cefbc-117">Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="cefbc-117">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="cefbc-118">Toutes les dimensions peuvent être remplacées par 1 pour diffuser dans cette dimension.</span><span class="sxs-lookup"><span data-stu-id="cefbc-118">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="cefbc-119">Ce tenseur est requis si le *BiasTensor* est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cefbc-119">This tensor is required if the *BiasTensor* is used.</span></span>


`BiasTensor`

<span data-ttu-id="cefbc-120">Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cefbc-120">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cefbc-121">Tenseur facultatif contenant les données de biais.</span><span class="sxs-lookup"><span data-stu-id="cefbc-121">An optional tensor containing the bias data.</span></span> <span data-ttu-id="cefbc-122">Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="cefbc-122">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="cefbc-123">Toutes les dimensions peuvent être remplacées par 1 pour diffuser dans cette dimension.</span><span class="sxs-lookup"><span data-stu-id="cefbc-123">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="cefbc-124">Ce tenseur est requis si le *ScaleTensor* est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cefbc-124">This tensor is required if the *ScaleTensor* is used.</span></span>


`OutputTensor`

<span data-ttu-id="cefbc-125">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cefbc-125">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cefbc-126">Tenseur dans lequel écrire les résultats.</span><span class="sxs-lookup"><span data-stu-id="cefbc-126">A tensor to write the results to.</span></span> <span data-ttu-id="cefbc-127">Les dimensions de ce tenseur sont `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="cefbc-127">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`AxisCount`

<span data-ttu-id="cefbc-128">Type : <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="cefbc-128">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="cefbc-129">Nombre d’axes.</span><span class="sxs-lookup"><span data-stu-id="cefbc-129">The number of axes.</span></span> <span data-ttu-id="cefbc-130">Ce champ détermine la taille du tableau *axes* .</span><span class="sxs-lookup"><span data-stu-id="cefbc-130">This field determines the size of the *Axes* array.</span></span>


`Axes`

<span data-ttu-id="cefbc-131">Type : \_ \_ taille \_ de champ (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cefbc-131">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span> 

<span data-ttu-id="cefbc-132">Axes sur lesquels calculer la moyenne et la variance.</span><span class="sxs-lookup"><span data-stu-id="cefbc-132">The axes along which to calculate the Mean and Variance.</span></span>


`NormalizeVariance`

<span data-ttu-id="cefbc-133">Type : <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="cefbc-133">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="cefbc-134">**True** si la couche de normalisation comprend une variance dans le calcul de normalisation.</span><span class="sxs-lookup"><span data-stu-id="cefbc-134">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="cefbc-135">Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="cefbc-135">Otherwise, **FALSE**.</span></span> <span data-ttu-id="cefbc-136">Si la **valeur est false**, l’équation de normalisation est `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="cefbc-136">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>


`Epsilon`

<span data-ttu-id="cefbc-137">Type : <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="cefbc-137">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="cefbc-138">Valeur Epsilon à utiliser pour éviter la division par zéro.</span><span class="sxs-lookup"><span data-stu-id="cefbc-138">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="cefbc-139">La valeur par défaut 0,00001 est recommandée.</span><span class="sxs-lookup"><span data-stu-id="cefbc-139">A value of 0.00001 is recommended as default.</span></span>


`FusedActivation`

<span data-ttu-id="cefbc-140">Type : \_ MAYBENULL \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cefbc-140">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="cefbc-141">Couche d’activation fusionnée facultative à appliquer après la normalisation.</span><span class="sxs-lookup"><span data-stu-id="cefbc-141">An optional fused activation layer to apply after the normalization.</span></span>


## <a name="remarks"></a><span data-ttu-id="cefbc-142">Notes</span><span class="sxs-lookup"><span data-stu-id="cefbc-142">Remarks</span></span>
<span data-ttu-id="cefbc-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** est un sur-ensemble de fonctionnalités de [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="cefbc-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="cefbc-144">Ici, la définition du tableau **axes** sur `{ 0, 2, 3 }` est l’équivalent de la définition de *CrossChannel* sur **false** dans **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; la définition du tableau **axes** sur équivaut à `{ 1, 2, 3 }` définir *CrossChannel* sur **true**.</span><span class="sxs-lookup"><span data-stu-id="cefbc-144">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="cefbc-145">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="cefbc-145">Availability</span></span>
<span data-ttu-id="cefbc-146">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="cefbc-146">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cefbc-147">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="cefbc-147">Tensor constraints</span></span>
* <span data-ttu-id="cefbc-148">*InputTensor* et *OutputTensor* doivent avoir la même *taille*.</span><span class="sxs-lookup"><span data-stu-id="cefbc-148">*InputTensor* and *OutputTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="cefbc-149">*BiasTensor*, *InputTensor*, *OutputTensor* et *ScaleTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="cefbc-149">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cefbc-150">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="cefbc-150">Tensor support</span></span>
| <span data-ttu-id="cefbc-151">Tenseur</span><span class="sxs-lookup"><span data-stu-id="cefbc-151">Tensor</span></span> | <span data-ttu-id="cefbc-152">Type</span><span class="sxs-lookup"><span data-stu-id="cefbc-152">Kind</span></span> | <span data-ttu-id="cefbc-153">Dimensions</span><span class="sxs-lookup"><span data-stu-id="cefbc-153">Dimensions</span></span> | <span data-ttu-id="cefbc-154">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="cefbc-154">Supported dimension counts</span></span> | <span data-ttu-id="cefbc-155">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="cefbc-155">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="cefbc-156">InputTensor</span><span class="sxs-lookup"><span data-stu-id="cefbc-156">InputTensor</span></span> | <span data-ttu-id="cefbc-157">Entrée</span><span class="sxs-lookup"><span data-stu-id="cefbc-157">Input</span></span> | <span data-ttu-id="cefbc-158">{BatchCount, ChannelCount, hauteur, largeur}</span><span class="sxs-lookup"><span data-stu-id="cefbc-158">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="cefbc-159">4</span><span class="sxs-lookup"><span data-stu-id="cefbc-159">4</span></span> | <span data-ttu-id="cefbc-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cefbc-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cefbc-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cefbc-161">ScaleTensor</span></span> | <span data-ttu-id="cefbc-162">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="cefbc-162">Optional input</span></span> | <span data-ttu-id="cefbc-163">{ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth}</span><span class="sxs-lookup"><span data-stu-id="cefbc-163">{ ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth }</span></span> | <span data-ttu-id="cefbc-164">4</span><span class="sxs-lookup"><span data-stu-id="cefbc-164">4</span></span> | <span data-ttu-id="cefbc-165">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cefbc-165">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cefbc-166">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="cefbc-166">BiasTensor</span></span> | <span data-ttu-id="cefbc-167">Entrée facultative</span><span class="sxs-lookup"><span data-stu-id="cefbc-167">Optional input</span></span> | <span data-ttu-id="cefbc-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span><span class="sxs-lookup"><span data-stu-id="cefbc-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span></span> | <span data-ttu-id="cefbc-169">4</span><span class="sxs-lookup"><span data-stu-id="cefbc-169">4</span></span> | <span data-ttu-id="cefbc-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cefbc-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cefbc-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cefbc-171">OutputTensor</span></span> | <span data-ttu-id="cefbc-172">Output</span><span class="sxs-lookup"><span data-stu-id="cefbc-172">Output</span></span> | <span data-ttu-id="cefbc-173">{BatchCount, ChannelCount, hauteur, largeur}</span><span class="sxs-lookup"><span data-stu-id="cefbc-173">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="cefbc-174">4</span><span class="sxs-lookup"><span data-stu-id="cefbc-174">4</span></span> | <span data-ttu-id="cefbc-175">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cefbc-175">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="cefbc-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cefbc-176">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cefbc-177">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="cefbc-177">**Header**</span></span> | <span data-ttu-id="cefbc-178">directml. h</span><span class="sxs-lookup"><span data-stu-id="cefbc-178">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="cefbc-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cefbc-179">See also</span></span>

[<span data-ttu-id="cefbc-180">Utilisation d’opérateurs fusionnés pour améliorer les performances</span><span class="sxs-lookup"><span data-stu-id="cefbc-180">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)