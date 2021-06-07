---
UID: NS:directml.DML_ADAM_OPTIMIZER_OPERATOR_DESC
title: DML_ADAM_OPTIMIZER_OPERATOR_DESC
description: Calcule les pondérations mises à jour (paramètres) à l’aide des dégradés fournis, en fonction de l’algorithme Adam (**Ada** ptive **M** oment estimation). Cet opérateur est un optimiseur et est généralement utilisé dans l’étape de mise à jour du poids d’une boucle d’apprentissage pour effectuer une descente de dégradé.
helpviewer_keywords:
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- DML_ADAM_OPTIMIZER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ADAM_OPTIMIZER_OPERATOR_DESC, DML_ADAM_OPTIMIZER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
- directml/DML_ADAM_OPTIMIZER_OPERATOR_DESC
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
- DML_ADAM_OPTIMIZER_OPERATOR_DESC
ms.openlocfilehash: 9943f70bd3d62faf57f4eca83f9f09ce0119881a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417345"
---
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a><span data-ttu-id="f40b5-104">Structure DML_ADAM_OPTIMIZER_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="f40b5-104">DML_ADAM_OPTIMIZER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f40b5-105">Calcule les pondérations mises à jour (paramètres) à l’aide des dégradés fournis, en fonction de l’algorithme Adam (**Ada** ptive **M** oment estimation).</span><span class="sxs-lookup"><span data-stu-id="f40b5-105">Computes updated weights (parameters) using the supplied gradients, based on the Adam (**ADA** ptive **M** oment estimation) algorithm.</span></span> <span data-ttu-id="f40b5-106">Cet opérateur est un optimiseur et est généralement utilisé dans l’étape de mise à jour du poids d’une boucle d’apprentissage pour effectuer une descente de dégradé.</span><span class="sxs-lookup"><span data-stu-id="f40b5-106">This operator is an optimizer, and is typically used in the weight update step of a training loop to perform gradient descent.</span></span>

<span data-ttu-id="f40b5-107">Cet opérateur effectue le calcul suivant :</span><span class="sxs-lookup"><span data-stu-id="f40b5-107">This operator performs the following computation:</span></span>

```
X = InputParametersTensor
M = InputFirstMomentTensor
V = InputSecondMomentTensor
G = GradientTensor
T = TrainingStepTensor

// Compute updated first and second moment estimates.
M = Beta1 * M + (1.0 - Beta1) * G
V = Beta2 * V + (1.0 - Beta2) * G * G

// Compute bias correction factor for first and second moment estimates.
Alpha = sqrt(1.0 - pow(Beta2, T)) / (1.0 - pow(Beta1, T))

X -= LearningRate * Alpha * M / (sqrt(V) + Epsilon)

OutputParametersTensor = X
OutputFirstMomentTensor = M
OutputSecondMomentTensor = V
```

<span data-ttu-id="f40b5-108">En plus de calculer les paramètres de pondération mis à jour (retournés dans *OutputParametersTensor*), cet opérateur retourne également les estimations des première et deuxième heure mises à jour dans *OutputFirstMomentTensor* et *OutputSecondMomentTensor*, respectivement.</span><span class="sxs-lookup"><span data-stu-id="f40b5-108">In addition to computing the updated weight parameters (returned in *OutputParametersTensor*), this operator also returns the updated first and second moment estimates in *OutputFirstMomentTensor* and *OutputSecondMomentTensor*, respectively.</span></span> <span data-ttu-id="f40b5-109">En règle générale, vous devez stocker ces estimations des premières et des secondes, et les fournir en tant qu’entrées au cours de l’étape de formation suivante.</span><span class="sxs-lookup"><span data-stu-id="f40b5-109">Typically, you should store these first and second moment estimates, and supply them as inputs during the subsequent training step.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f40b5-110">Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f40b5-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f40b5-111">Consultez également [l’historique des versions DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="f40b5-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f40b5-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f40b5-112">Syntax</span></span>
```cpp
struct DML_ADAM_OPTIMIZER_OPERATOR_DESC
{ 
  const DML_TENSOR_DESC* InputParametersTensor;
  const DML_TENSOR_DESC* InputFirstMomentTensor;
  const DML_TENSOR_DESC* InputSecondMomentTensor;
  const DML_TENSOR_DESC* GradientTensor;
  const DML_TENSOR_DESC* TrainingStepTensor;
  const DML_TENSOR_DESC* OutputParametersTensor;
  const DML_TENSOR_DESC* OutputFirstMomentTensor;
  const DML_TENSOR_DESC* OutputSecondMomentTensor;
  FLOAT LearningRate;
  FLOAT Beta1;
  FLOAT Beta2;
  FLOAT Epsilon;
};
```

## <a name="members"></a><span data-ttu-id="f40b5-113">Membres</span><span class="sxs-lookup"><span data-stu-id="f40b5-113">Members</span></span>

`InputParametersTensor`

<span data-ttu-id="f40b5-114">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f40b5-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f40b5-115">Tenseur contenant les paramètres (pondérations) auxquels appliquer cet optimiseur.</span><span class="sxs-lookup"><span data-stu-id="f40b5-115">A tensor containing the parameters (weights) to apply this optimizer to.</span></span> <span data-ttu-id="f40b5-116">Les estimations du gradient, du premier et du deuxième moment, de l’étape de formation actuelle, ainsi que des hyperparamètres *LearningRate*, *beta1* et *bêta2*, sont utilisées par cet opérateur pour effectuer une descente du gradient sur les valeurs de poids fournies dans ce tenseur.</span><span class="sxs-lookup"><span data-stu-id="f40b5-116">The gradient, first, and second moment estimates, current training step, as well as hyperparameters *LearningRate*, *Beta1*, and *Beta2*, are used by this operator to perform gradient descent on the weight values supplied in this tensor.</span></span>

`InputFirstMomentTensor`

<span data-ttu-id="f40b5-117">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f40b5-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f40b5-118">Tenseur contenant la première estimation du dégradé pour chaque valeur de poids.</span><span class="sxs-lookup"><span data-stu-id="f40b5-118">A tensor containing the first moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="f40b5-119">Ces valeurs sont généralement obtenues à la suite d’une exécution précédente de cet opérateur, via *OutputFirstMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-119">These values are typically obtained as the result of a previous execution of this operator, via the *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="f40b5-120">Lors de l’application de cet optimiseur à un ensemble de pondérations pour la première fois (par exemple, au cours de l’étape de formation initiale), les valeurs de ce tenseur doivent généralement être initialisées à zéro.</span><span class="sxs-lookup"><span data-stu-id="f40b5-120">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="f40b5-121">Les exécutions suivantes doivent utiliser les valeurs retournées dans *OutputFirstMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-121">Subsequent executions should use the values returned in *OutputFirstMomentTensor*.</span></span>

<span data-ttu-id="f40b5-122">Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-122">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`InputSecondMomentTensor`

<span data-ttu-id="f40b5-123">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f40b5-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f40b5-124">Tenseur contenant l’estimation du deuxième moment du dégradé pour chaque valeur de poids.</span><span class="sxs-lookup"><span data-stu-id="f40b5-124">A tensor containing the second moment estimate of the gradient for each weight value.</span></span> <span data-ttu-id="f40b5-125">Ces valeurs sont généralement obtenues à la suite d’une exécution précédente de cet opérateur, via *OutputSecondMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-125">These values are typically obtained as the result of a previous execution of this operator, via the *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="f40b5-126">Lors de l’application de cet optimiseur à un ensemble de pondérations pour la première fois (par exemple, au cours de l’étape de formation initiale), les valeurs de ce tenseur doivent généralement être initialisées à zéro.</span><span class="sxs-lookup"><span data-stu-id="f40b5-126">When applying this optimizer to a set of weights for the first time (for example, during the initial training step) the values of this tensor should typically be initialized to zero.</span></span> <span data-ttu-id="f40b5-127">Les exécutions suivantes doivent utiliser les valeurs retournées dans *OutputSecondMomentTensor*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-127">Subsequent executions should use the values returned in *OutputSecondMomentTensor*.</span></span>

<span data-ttu-id="f40b5-128">Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-128">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`GradientTensor`

<span data-ttu-id="f40b5-129">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f40b5-129">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f40b5-130">Les dégradés à appliquer aux paramètres d’entrée (pondérations) pour la descente de dégradé.</span><span class="sxs-lookup"><span data-stu-id="f40b5-130">The gradients to apply to the input parameters (weights) for gradient descent.</span></span> <span data-ttu-id="f40b5-131">Les dégradés sont généralement obtenus dans une passe de rétropropagation au cours de l’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="f40b5-131">Gradients are typically obtained in a backpropagation pass during training.</span></span>

<span data-ttu-id="f40b5-132">Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-132">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`TrainingStepTensor`

<span data-ttu-id="f40b5-133">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f40b5-133">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f40b5-134">Tenseur scalaire contenant une valeur entière représentant le nombre d’étapes d’apprentissage en cours.</span><span class="sxs-lookup"><span data-stu-id="f40b5-134">A scalar tensor containing a single integer value representing the current training step count.</span></span> <span data-ttu-id="f40b5-135">Cette valeur, ainsi que la bêta *2 et bêta2* , sont utilisées pour calculer la dégradation exponentielle du premier et du deuxième cours estimés. </span><span class="sxs-lookup"><span data-stu-id="f40b5-135">This value along with *Beta1* and *Beta2* is used to compute the exponential decay of the first and second moment estimate tensors.</span></span>

<span data-ttu-id="f40b5-136">En général, la valeur de l’étape de formation commence à 0 au début de l’apprentissage et est incrémentée de 1 à chaque étape de formation consécutive.</span><span class="sxs-lookup"><span data-stu-id="f40b5-136">Typically the training step value starts at 0 at the beginning of training, and is incremented by 1 on each successive training step.</span></span> <span data-ttu-id="f40b5-137">Cet opérateur ne met pas à jour la valeur de l’étape d’apprentissage ; vous devez le faire manuellement, par exemple à l’aide de [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="f40b5-137">This operator doesn't update the training step value; you should do that manually, for example using [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).</span></span>

<span data-ttu-id="f40b5-138">Ce tenseur doit être une valeur scalaire (autrement dit, toutes les *tailles* égales à 1) et un type de données [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span><span class="sxs-lookup"><span data-stu-id="f40b5-138">This tensor must be a scalar (that is, all *Sizes* equal to 1) and have data type [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).</span></span>

`OutputParametersTensor`

<span data-ttu-id="f40b5-139">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f40b5-139">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f40b5-140">Tenseur de sortie qui contient les valeurs de paramètre (poids) mises à jour après l’application de la descente de dégradé.</span><span class="sxs-lookup"><span data-stu-id="f40b5-140">An output tensor that holds the updated parameter (weight) values after gradient descent is applied.</span></span>

<span data-ttu-id="f40b5-141">Pendant la liaison, ce tenseur est autorisé à utiliser un alias pour un tenseur d’entrée éligible, qui peut être utilisé pour effectuer une mise à jour sur place de ce tenseur.</span><span class="sxs-lookup"><span data-stu-id="f40b5-141">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="f40b5-142">Pour plus d’informations, consultez la section [Notes](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="f40b5-142">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="f40b5-143">Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-143">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputFirstMomentTensor`

<span data-ttu-id="f40b5-144">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f40b5-144">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f40b5-145">Tenseur de sortie contenant des estimations de premier moment mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f40b5-145">An output tensor containing updated first moment estimates.</span></span> <span data-ttu-id="f40b5-146">Vous devez stocker les valeurs de ce tenseur et les fournir dans *InputFirstMomentTensor* au cours de l’étape de formation suivante.</span><span class="sxs-lookup"><span data-stu-id="f40b5-146">You should store the values of this tensor, and supply them in *InputFirstMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="f40b5-147">Pendant la liaison, ce tenseur est autorisé à utiliser un alias pour un tenseur d’entrée éligible, qui peut être utilisé pour effectuer une mise à jour sur place de ce tenseur.</span><span class="sxs-lookup"><span data-stu-id="f40b5-147">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="f40b5-148">Pour plus d’informations, consultez la section [Notes](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="f40b5-148">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="f40b5-149">Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-149">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`OutputSecondMomentTensor`

<span data-ttu-id="f40b5-150">Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f40b5-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f40b5-151">Tenseur de sortie contenant des estimations de deuxième heure mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f40b5-151">An output tensor containing updated second moment estimates.</span></span> <span data-ttu-id="f40b5-152">Vous devez stocker les valeurs de ce tenseur et les fournir dans *InputSecondMomentTensor* au cours de l’étape de formation suivante.</span><span class="sxs-lookup"><span data-stu-id="f40b5-152">You should store the values of this tensor and supply them in *InputSecondMomentTensor* during the subsequent training step.</span></span>

<span data-ttu-id="f40b5-153">Pendant la liaison, ce tenseur est autorisé à utiliser un alias pour un tenseur d’entrée éligible, qui peut être utilisé pour effectuer une mise à jour sur place de ce tenseur.</span><span class="sxs-lookup"><span data-stu-id="f40b5-153">During binding, this tensor is permitted to alias an eligible input tensor, which can be used to perform an in-place update of this tensor.</span></span> <span data-ttu-id="f40b5-154">Pour plus d’informations, consultez la section [Notes](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="f40b5-154">See the [Remarks](#remarks) section for more details.</span></span>

<span data-ttu-id="f40b5-155">Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-155">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputParametersTensor*.</span></span>

`LearningRate`

<span data-ttu-id="f40b5-156">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f40b5-156">Type: **float**</span></span>

<span data-ttu-id="f40b5-157">Taux d’apprentissage, également communément appelé *taille d’étape*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-157">The learning rate, also commonly referred to as the *step size*.</span></span> <span data-ttu-id="f40b5-158">Le taux d’apprentissage est un hyperparamètre qui détermine l’amplitude de la mise à jour du poids le long du vecteur de dégradé à chaque étape de l’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="f40b5-158">The learning rate is a hyperparameter that determines the magnitude of the weight update along the gradient vector on each training step.</span></span>

`Beta1`

<span data-ttu-id="f40b5-159">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f40b5-159">Type: **float**</span></span>

<span data-ttu-id="f40b5-160">Hyperparamètre représentant la vitesse de dégradation exponentielle de l’estimation du premier moment du dégradé.</span><span class="sxs-lookup"><span data-stu-id="f40b5-160">A hyperparameter representing the exponential decay rate of the gradient's first moment estimate.</span></span> <span data-ttu-id="f40b5-161">Cette valeur doit être comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="f40b5-161">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="f40b5-162">Une valeur de 0,9 f est typique.</span><span class="sxs-lookup"><span data-stu-id="f40b5-162">A value of 0.9f is typical.</span></span>

`Beta2`

<span data-ttu-id="f40b5-163">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f40b5-163">Type: **float**</span></span>

<span data-ttu-id="f40b5-164">Hyperparamètre représentant la vitesse de dégradation exponentielle de l’estimation du deuxième moment du dégradé.</span><span class="sxs-lookup"><span data-stu-id="f40b5-164">A hyperparameter representing the exponential decay rate of the gradient's second moment estimate.</span></span> <span data-ttu-id="f40b5-165">Cette valeur doit être comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="f40b5-165">This value should be between 0.0 and 1.0.</span></span> <span data-ttu-id="f40b5-166">La valeur 0,999 f est standard.</span><span class="sxs-lookup"><span data-stu-id="f40b5-166">A value of 0.999f is typical.</span></span>

`Epsilon`

<span data-ttu-id="f40b5-167">Type : **float**</span><span class="sxs-lookup"><span data-stu-id="f40b5-167">Type: **float**</span></span>

<span data-ttu-id="f40b5-168">Petite valeur utilisée pour aider à la stabilité numérique en empêchant la division par zéro.</span><span class="sxs-lookup"><span data-stu-id="f40b5-168">A small value used to help numerical stability by preventing division-by-zero.</span></span> <span data-ttu-id="f40b5-169">Pour les entrées à virgule flottante 32 bits, les valeurs standard sont 1e-8 ou `FLT_EPSILON` .</span><span class="sxs-lookup"><span data-stu-id="f40b5-169">For 32-bit floating-point inputs, typical values include 1e-8 or `FLT_EPSILON`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f40b5-170">Remarques</span><span class="sxs-lookup"><span data-stu-id="f40b5-170">Remarks</span></span>
<span data-ttu-id="f40b5-171">Cet opérateur prend en charge l’exécution sur place, ce qui signifie que chaque tenseur de sortie est autorisé à aliaser un tenseur d’entrée éligible pendant la liaison.</span><span class="sxs-lookup"><span data-stu-id="f40b5-171">This operator supports in-place execution, meaning that each output tensor is permitted to alias an eligible input tensor during binding.</span></span> <span data-ttu-id="f40b5-172">Par exemple, il est possible de lier la même ressource pour *InputParametersTensor* et *OutputParametersTensor* afin d’obtenir efficacement une mise à jour sur place des paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="f40b5-172">For example, it's possible to bind the same resource for both the *InputParametersTensor* and *OutputParametersTensor* in order to effectively achieve an in-place update of the input parameters.</span></span> <span data-ttu-id="f40b5-173">Tous les dizaines de temps d’entrée de cet opérateur, à l’exception de *TrainingStepTensor*, peuvent être associés à un alias de cette manière.</span><span class="sxs-lookup"><span data-stu-id="f40b5-173">All of this operator's input tensors, with the exception of the *TrainingStepTensor*, are eligible to be aliased in this way.</span></span>

## <a name="availability"></a><span data-ttu-id="f40b5-174">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="f40b5-174">Availability</span></span>
<span data-ttu-id="f40b5-175">Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="f40b5-175">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f40b5-176">Contraintes tenseur</span><span class="sxs-lookup"><span data-stu-id="f40b5-176">Tensor constraints</span></span>
* <span data-ttu-id="f40b5-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor* et *TrainingStepTensor* doivent avoir le même *type de données*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-177">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor*, and *TrainingStepTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="f40b5-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor* et *OutputSecondMomentTensor* doivent avoir la même *taille*.</span><span class="sxs-lookup"><span data-stu-id="f40b5-178">*GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, and *OutputSecondMomentTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f40b5-179">Support tenseur</span><span class="sxs-lookup"><span data-stu-id="f40b5-179">Tensor support</span></span>
| <span data-ttu-id="f40b5-180">Tenseur</span><span class="sxs-lookup"><span data-stu-id="f40b5-180">Tensor</span></span> | <span data-ttu-id="f40b5-181">Type</span><span class="sxs-lookup"><span data-stu-id="f40b5-181">Kind</span></span> | <span data-ttu-id="f40b5-182">Dimensions</span><span class="sxs-lookup"><span data-stu-id="f40b5-182">Dimensions</span></span> | <span data-ttu-id="f40b5-183">Nombre de dimensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="f40b5-183">Supported dimension counts</span></span> | <span data-ttu-id="f40b5-184">Types de données pris en charge</span><span class="sxs-lookup"><span data-stu-id="f40b5-184">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="f40b5-185">InputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="f40b5-185">InputParametersTensor</span></span> | <span data-ttu-id="f40b5-186">Entrée</span><span class="sxs-lookup"><span data-stu-id="f40b5-186">Input</span></span> | <span data-ttu-id="f40b5-187">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="f40b5-187">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="f40b5-188">4</span><span class="sxs-lookup"><span data-stu-id="f40b5-188">4</span></span> | <span data-ttu-id="f40b5-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f40b5-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f40b5-190">InputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="f40b5-190">InputFirstMomentTensor</span></span> | <span data-ttu-id="f40b5-191">Entrée</span><span class="sxs-lookup"><span data-stu-id="f40b5-191">Input</span></span> | <span data-ttu-id="f40b5-192">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="f40b5-192">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="f40b5-193">4</span><span class="sxs-lookup"><span data-stu-id="f40b5-193">4</span></span> | <span data-ttu-id="f40b5-194">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f40b5-194">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f40b5-195">InputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="f40b5-195">InputSecondMomentTensor</span></span> | <span data-ttu-id="f40b5-196">Entrée</span><span class="sxs-lookup"><span data-stu-id="f40b5-196">Input</span></span> | <span data-ttu-id="f40b5-197">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="f40b5-197">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="f40b5-198">4</span><span class="sxs-lookup"><span data-stu-id="f40b5-198">4</span></span> | <span data-ttu-id="f40b5-199">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f40b5-199">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f40b5-200">GradientTensor</span><span class="sxs-lookup"><span data-stu-id="f40b5-200">GradientTensor</span></span> | <span data-ttu-id="f40b5-201">Entrée</span><span class="sxs-lookup"><span data-stu-id="f40b5-201">Input</span></span> | <span data-ttu-id="f40b5-202">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="f40b5-202">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="f40b5-203">4</span><span class="sxs-lookup"><span data-stu-id="f40b5-203">4</span></span> | <span data-ttu-id="f40b5-204">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f40b5-204">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f40b5-205">TrainingStepTensor</span><span class="sxs-lookup"><span data-stu-id="f40b5-205">TrainingStepTensor</span></span> | <span data-ttu-id="f40b5-206">Entrée</span><span class="sxs-lookup"><span data-stu-id="f40b5-206">Input</span></span> | <span data-ttu-id="f40b5-207">{1, 1, 1,1}</span><span class="sxs-lookup"><span data-stu-id="f40b5-207">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="f40b5-208">4</span><span class="sxs-lookup"><span data-stu-id="f40b5-208">4</span></span> | <span data-ttu-id="f40b5-209">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f40b5-209">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f40b5-210">OutputParametersTensor</span><span class="sxs-lookup"><span data-stu-id="f40b5-210">OutputParametersTensor</span></span> | <span data-ttu-id="f40b5-211">Sortie</span><span class="sxs-lookup"><span data-stu-id="f40b5-211">Output</span></span> | <span data-ttu-id="f40b5-212">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="f40b5-212">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="f40b5-213">4</span><span class="sxs-lookup"><span data-stu-id="f40b5-213">4</span></span> | <span data-ttu-id="f40b5-214">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f40b5-214">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f40b5-215">OutputFirstMomentTensor</span><span class="sxs-lookup"><span data-stu-id="f40b5-215">OutputFirstMomentTensor</span></span> | <span data-ttu-id="f40b5-216">Sortie</span><span class="sxs-lookup"><span data-stu-id="f40b5-216">Output</span></span> | <span data-ttu-id="f40b5-217">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="f40b5-217">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="f40b5-218">4</span><span class="sxs-lookup"><span data-stu-id="f40b5-218">4</span></span> | <span data-ttu-id="f40b5-219">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f40b5-219">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f40b5-220">OutputSecondMomentTensor</span><span class="sxs-lookup"><span data-stu-id="f40b5-220">OutputSecondMomentTensor</span></span> | <span data-ttu-id="f40b5-221">Sortie</span><span class="sxs-lookup"><span data-stu-id="f40b5-221">Output</span></span> | <span data-ttu-id="f40b5-222">{D0, D1, D2, D3}</span><span class="sxs-lookup"><span data-stu-id="f40b5-222">{ D0, D1, D2, D3 }</span></span> | <span data-ttu-id="f40b5-223">4</span><span class="sxs-lookup"><span data-stu-id="f40b5-223">4</span></span> | <span data-ttu-id="f40b5-224">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f40b5-224">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="f40b5-225">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f40b5-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f40b5-226">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="f40b5-226">**Header**</span></span> | <span data-ttu-id="f40b5-227">directml. h</span><span class="sxs-lookup"><span data-stu-id="f40b5-227">directml.h</span></span> |