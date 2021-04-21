---
title: Utilisation d’opérateurs fusionnés pour améliorer les performances
description: Certains opérateurs DirectML prennent en charge un concept connu sous le nom de *fusion*. La fusion d’opérateur est un moyen d’améliorer les performances en fusionnant un opérateur (en général, une fonction d’activation) dans un opérateur différent afin qu’ils soient exécutés ensemble sans nécessiter d’aller-retour vers la mémoire.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: bba4a9d0ef5c69976a5a344432bf82d31b00c0c7
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803987"
---
# <a name="using-fused-operators-to-improve-performance"></a><span data-ttu-id="19564-104">Utilisation d’opérateurs fusionnés pour améliorer les performances</span><span class="sxs-lookup"><span data-stu-id="19564-104">Using fused operators to improve performance</span></span>

<span data-ttu-id="19564-105">Certains opérateurs DirectML prennent en charge un concept connu sous le nom de *fusion*.</span><span class="sxs-lookup"><span data-stu-id="19564-105">Some DirectML operators support a concept known as *fusion*.</span></span> <span data-ttu-id="19564-106">La fusion d’opérateur est un moyen d’améliorer les performances en fusionnant un opérateur (en général, une fonction d’activation) dans un opérateur différent afin qu’ils soient exécutés ensemble sans nécessiter d’aller-retour vers la mémoire.</span><span class="sxs-lookup"><span data-stu-id="19564-106">Operator fusion is a way to improve performance by merging one operator (typically, an activation function) into a different operator so that they are executed together without requiring a roundtrip to memory.</span></span>

## <a name="when-to-fuse-activations"></a><span data-ttu-id="19564-107">Quand fusibles d’activations</span><span class="sxs-lookup"><span data-stu-id="19564-107">When to fuse activations</span></span>

<span data-ttu-id="19564-108">Les activations fusionnées sont une optimisation des performances.</span><span class="sxs-lookup"><span data-stu-id="19564-108">Fused activations are a performance optimization.</span></span> <span data-ttu-id="19564-109">Un scénario très courant dans de nombreux modèles de Machine Learning (ML) consiste à appliquer une non-linéarité (une fonction d’activation) à la sortie de chaque couche du modèle.</span><span class="sxs-lookup"><span data-stu-id="19564-109">An extremely common scenario in many machine learning (ML) models is to apply a nonlinearity (an activation function) to the output of each layer in the model.</span></span>

<span data-ttu-id="19564-110">En règle générale, cela nécessite un aller-retour vers la mémoire graphique.</span><span class="sxs-lookup"><span data-stu-id="19564-110">Ordinarily, this requires a roundtrip to graphics memory.</span></span> <span data-ttu-id="19564-111">Par exemple, si une convolution est suivie d’une activation non fusionnée de relu, le GPU doit attendre que les résultats de la convolution soient écrits dans la mémoire GPU avant de commencer à calculer la couche d’activation relu.</span><span class="sxs-lookup"><span data-stu-id="19564-111">For example if a Convolution is followed by a non-fused Relu activation, then the GPU must wait for the results of the Convolution to be written into GPU memory before it can begin computing the Relu activation layer.</span></span> <span data-ttu-id="19564-112">Étant donné que la charge de travail de calcul de la plupart des fonctions d’activation a tendance à être faible, ce bouclage vers la mémoire graphique peut être un goulot d’étranglement des performances majeur.</span><span class="sxs-lookup"><span data-stu-id="19564-112">As the compute workload of most activation functions tends to be small, this roundtrip to graphics memory can be a major performance bottleneck.</span></span>

<span data-ttu-id="19564-113">La fusion d’opérateur permet à la fonction d’activation (relu dans l’exemple ci-dessus) d’être exécutée dans le cadre de l’opérateur précédent (convolution, par exemple).</span><span class="sxs-lookup"><span data-stu-id="19564-113">Operator fusion allows the activation function (Relu in the above example) to be performed as part of the preceding operator (Convolution, for example).</span></span> <span data-ttu-id="19564-114">Cela permet au GPU de calculer la fonction d’activation sans attendre que les résultats de l’opérateur précédent soient écrits en mémoire &mdash; , ce qui améliore les performances.</span><span class="sxs-lookup"><span data-stu-id="19564-114">This allows the GPU to compute the activation function without waiting for the results of the preceding operator to be written into memory&mdash;and that improves performance.</span></span>

<span data-ttu-id="19564-115">Étant donné que les activations fusionnées produisent le même résultat, mais sont plus rapides dans de nombreux cas, nous vous recommandons d’éliminer les couches d’activation en les fusionnant dans leur opérateur précédent, dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="19564-115">Because fused activations produce the same result, but are faster in many cases, we recommend that you eliminate activation layers by fusing them into their preceding operator wherever possible.</span></span>

## <a name="how-to-fuse-activations"></a><span data-ttu-id="19564-116">Comment fusibler des activations</span><span class="sxs-lookup"><span data-stu-id="19564-116">How to fuse activations</span></span>

<span data-ttu-id="19564-117">Les opérateurs qui prennent en charge les activations fusionnées ont un paramètre facultatif supplémentaire dans leur struct d’opérateur, `const DML_OPERATOR_DESC* FusedActivation` .</span><span class="sxs-lookup"><span data-stu-id="19564-117">Operators that support fused activations have an additional optional parameter in their operator struct, `const DML_OPERATOR_DESC* FusedActivation`.</span></span> <span data-ttu-id="19564-118">La convolution, par exemple, prend en charge l’activation fusionnée et possède un *FusedActivation* correspondant dans sa description d’opérateur (voir [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="19564-118">Convolution, for example, supports fused activation, and it has a corresponding *FusedActivation* in its operator description (see [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).</span></span>

```cpp
struct DML_CONVOLUTION_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* FilterTensor;
    \_Maybenull\_ const DML_TENSOR_DESC* BiasTensor;
    const DML_TENSOR_DESC* OutputTensor;
    DML_CONVOLUTION_MODE Mode;
    DML_CONVOLUTION_DIRECTION Direction;
    UINT DimensionCount;
    _Field_size_(DimensionCount) const UINT* Strides;
    _Field_size_(DimensionCount) const UINT* Dilations;
    _Field_size_(DimensionCount) const UINT* StartPadding;
    _Field_size_(DimensionCount) const UINT* EndPadding;
    _Field_size_(DimensionCount) const UINT* OutputPadding;
    UINT GroupCount;
    \_Maybenull\_ const DML_OPERATOR_DESC* FusedActivation;
};
```

<span data-ttu-id="19564-119">Pour fusionner une activation, construisez une [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) qui décrit le type d’activation à fusionner.</span><span class="sxs-lookup"><span data-stu-id="19564-119">To fuse an activation, construct a [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) that describes the type of activation to be fused.</span></span> <span data-ttu-id="19564-120">Par exemple, pour fusibler une fonction relu, le type d’opérateur approprié serait [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span><span class="sxs-lookup"><span data-stu-id="19564-120">For example to fuse a Relu function, the correct operator type would be [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

> [!NOTE]
> <span data-ttu-id="19564-121">Lors de la construction de la description de l’opérateur pour la fonction d’activation, vous devez définir les paramètres *InputTensor* et *OutputTensor* pour la fonction d’activation sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="19564-121">When constructing the operator description for the activation function, you must set the *InputTensor* and *OutputTensor* parameters for the activation function to **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="19564-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="19564-122">Example</span></span>

```cpp
DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC leakyReluDesc;
leakyReluDesc.InputTensor = nullptr;
leakyReluDesc.OutputTensor = nullptr;
leakyReluDesc.Alpha = 0.01f;

DML_OPERATOR_DESC activationDesc = { DML_OPERATOR_ACTIVATION_LEAKY_RELU, &leakyReluDesc };

DML_CONVOLUTION_OPERATOR_DESC convDesc;
// ...
convDesc.FusedActivation = &activationDesc;
```

<span data-ttu-id="19564-123">Pour obtenir un exemple complet, l' [exemple DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples) utilise des activations fusionnées pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="19564-123">For a complete example, the [DirectMLSuperResolution sample](https://github.com/microsoft/DirectML/tree/master/Samples) utilizes fused activations to improve performance.</span></span>

## <a name="operators-that-support-fused-activation"></a><span data-ttu-id="19564-124">Opérateurs qui prennent en charge l’activation fusionnée</span><span class="sxs-lookup"><span data-stu-id="19564-124">Operators that support fused activation</span></span>

* [<span data-ttu-id="19564-125">DML_OPERATOR_CONVOLUTION</span><span class="sxs-lookup"><span data-stu-id="19564-125">DML_OPERATOR_CONVOLUTION</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="19564-126">**DML_OPERATOR_GEMM**</span><span class="sxs-lookup"><span data-stu-id="19564-126">**DML_OPERATOR_GEMM**</span></span>
* <span data-ttu-id="19564-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="19564-127">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="19564-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** et **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="19564-128">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** and **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="19564-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="19564-129">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>

## <a name="activations-that-are-supported-for-fusion"></a><span data-ttu-id="19564-130">Activations prises en charge pour la fusion</span><span class="sxs-lookup"><span data-stu-id="19564-130">Activations that are supported for fusion</span></span>

* [<span data-ttu-id="19564-131">DML_OPERATOR_ACTIVATION_ELU</span><span class="sxs-lookup"><span data-stu-id="19564-131">DML_OPERATOR_ACTIVATION_ELU</span></span>](/windows/win32/api/directml/ne-directml-dml_operator_type)
* <span data-ttu-id="19564-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="19564-132">**DML_OPERATOR_ACTIVATION_HARD_SIGMOID**</span></span>
* <span data-ttu-id="19564-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="19564-133">**DML_OPERATOR_ACTIVATION_IDENTITY**</span></span>
* <span data-ttu-id="19564-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span><span class="sxs-lookup"><span data-stu-id="19564-134">**DML_OPERATOR_ACTIVATION_LEAKY_RELU**</span></span>
* <span data-ttu-id="19564-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="19564-135">**DML_OPERATOR_ACTIVATION_LINEAR**</span></span>
* <span data-ttu-id="19564-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="19564-136">**DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**</span></span>
* <span data-ttu-id="19564-137">**DML_OPERATOR_ACTIVATION_RELU**</span><span class="sxs-lookup"><span data-stu-id="19564-137">**DML_OPERATOR_ACTIVATION_RELU**</span></span>
* <span data-ttu-id="19564-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span><span class="sxs-lookup"><span data-stu-id="19564-138">**DML_OPERATOR_ACTIVATION_SCALED_ELU**</span></span>
* <span data-ttu-id="19564-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span><span class="sxs-lookup"><span data-stu-id="19564-139">**DML_OPERATOR_ACTIVATION_SCALED_TANH**</span></span>
* <span data-ttu-id="19564-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span><span class="sxs-lookup"><span data-stu-id="19564-140">**DML_OPERATOR_ACTIVATION_SIGMOID**</span></span>
* <span data-ttu-id="19564-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span><span class="sxs-lookup"><span data-stu-id="19564-141">**DML_OPERATOR_ACTIVATION_SOFTPLUS**</span></span>
* <span data-ttu-id="19564-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span><span class="sxs-lookup"><span data-stu-id="19564-142">**DML_OPERATOR_ACTIVATION_SOFTSIGN**</span></span>
* <span data-ttu-id="19564-143">**DML_OPERATOR_ACTIVATION_TANH**</span><span class="sxs-lookup"><span data-stu-id="19564-143">**DML_OPERATOR_ACTIVATION_TANH**</span></span>
* <span data-ttu-id="19564-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span><span class="sxs-lookup"><span data-stu-id="19564-144">**DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**</span></span>
* <span data-ttu-id="19564-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="19564-145">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="19564-146">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="19564-146">**DML_OPERATOR_ACTIVATION_CELU**</span></span>

<span data-ttu-id="19564-147">Les opérateurs qui ne sont pas dans cette liste ne sont pas pris en charge pour l’activation fusionnée.</span><span class="sxs-lookup"><span data-stu-id="19564-147">Any operators not in this list are not supported for fused activation.</span></span>

## <a name="see-also"></a><span data-ttu-id="19564-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19564-148">See also</span></span>

* [<span data-ttu-id="19564-149">Exemple DirectMLSuperResolution</span><span class="sxs-lookup"><span data-stu-id="19564-149">DirectMLSuperResolution sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples)    
* [<span data-ttu-id="19564-150">DML_CONVOLUTION_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="19564-150">DML_CONVOLUTION_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
