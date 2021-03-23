---
title: Utilisation d’opérateurs fusionnés pour améliorer les performances
description: Certains opérateurs DirectML prennent en charge un concept connu sous le nom de *fusion*. La fusion d’opérateur est un moyen d’améliorer les performances en fusionnant un opérateur (en général, une fonction d’activation) dans un opérateur différent afin qu’ils soient exécutés ensemble sans nécessiter d’aller-retour vers la mémoire.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: b692727d52e252bb3752573e692bcf5beda794e2
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548624"
---
# <a name="using-fused-operators-to-improve-performance"></a>Utilisation d’opérateurs fusionnés pour améliorer les performances

Certains opérateurs DirectML prennent en charge un concept connu sous le nom de *fusion*. La fusion d’opérateur est un moyen d’améliorer les performances en fusionnant un opérateur (en général, une fonction d’activation) dans un opérateur différent afin qu’ils soient exécutés ensemble sans nécessiter d’aller-retour vers la mémoire.

## <a name="when-to-fuse-activations"></a>Quand fusibles d’activations

Les activations fusionnées sont une optimisation des performances. Un scénario très courant dans de nombreux modèles de Machine Learning (ML) consiste à appliquer une non-linéarité (une fonction d’activation) à la sortie de chaque couche du modèle.

En règle générale, cela nécessite un aller-retour vers la mémoire graphique. Par exemple, si une convolution est suivie d’une activation non fusionnée de relu, le GPU doit attendre que les résultats de la convolution soient écrits dans la mémoire GPU avant de commencer à calculer la couche d’activation relu. Étant donné que la charge de travail de calcul de la plupart des fonctions d’activation a tendance à être faible, ce bouclage vers la mémoire graphique peut être un goulot d’étranglement des performances majeur.

La fusion d’opérateur permet à la fonction d’activation (relu dans l’exemple ci-dessus) d’être exécutée dans le cadre de l’opérateur précédent (convolution, par exemple). Cela permet au GPU de calculer la fonction d’activation sans attendre que les résultats de l’opérateur précédent soient écrits en mémoire &mdash; , ce qui améliore les performances.

Étant donné que les activations fusionnées produisent le même résultat, mais sont plus rapides dans de nombreux cas, nous vous recommandons d’éliminer les couches d’activation en les fusionnant dans leur opérateur précédent, dans la mesure du possible.

## <a name="how-to-fuse-activations"></a>Comment fusibler des activations

Les opérateurs qui prennent en charge les activations fusionnées ont un paramètre facultatif supplémentaire dans leur struct d’opérateur, `const DML_OPERATOR_DESC* FusedActivation` . La convolution, par exemple, prend en charge l’activation fusionnée et possède un *FusedActivation* correspondant dans sa description d’opérateur (voir [DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)).

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

Pour fusionner une activation, construisez une [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) qui décrit le type d’activation à fusionner. Par exemple, pour fusibler une fonction relu, le type d’opérateur approprié serait [DML_OPERATOR_ACTIVATION_RELU](/windows/win32/api/directml/ne-directml-dml_operator_type).

> [!NOTE]
> Lors de la construction de la description de l’opérateur pour la fonction d’activation, vous devez définir les paramètres *InputTensor* et *OutputTensor* pour la fonction d’activation sur la **valeur null**.

## <a name="example"></a>Exemple

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

Pour obtenir un exemple complet, l' [exemple DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples) utilise des activations fusionnées pour améliorer les performances.

## <a name="operators-that-support-fused-activation"></a>Opérateurs qui prennent en charge l’activation fusionnée

* [DML_OPERATOR_CONVOLUTION](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_GEMM**
* **DML_OPERATOR_BATCH_NORMALIZATION**
* **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION** et **DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**
* **DML_OPERATOR_ELEMENT_WISE_ADD1**

## <a name="activations-that-are-supported-for-fusion"></a>Activations prises en charge pour la fusion

* [DML_OPERATOR_ACTIVATION_ELU](/windows/win32/api/directml/ne-directml-dml_operator_type)
* **DML_OPERATOR_ACTIVATION_HARD_SIGMOID**
* **DML_OPERATOR_ACTIVATION_IDENTITY**
* **DML_OPERATOR_ACTIVATION_LEAKY_RELU**
* **DML_OPERATOR_ACTIVATION_LINEAR**
* **DML_OPERATOR_ACTIVATION_PARAMETRIC_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_RELU**
* **DML_OPERATOR_ACTIVATION_SCALED_ELU**
* **DML_OPERATOR_ACTIVATION_SCALED_TANH**
* **DML_OPERATOR_ACTIVATION_SIGMOID**
* **DML_OPERATOR_ACTIVATION_SOFTPLUS**
* **DML_OPERATOR_ACTIVATION_SOFTSIGN**
* **DML_OPERATOR_ACTIVATION_TANH**
* **DML_OPERATOR_ACTIVATION_THRESHOLDED_RELU**
* **DML_OPERATOR_ACTIVATION_SHRINK**
* **DML_OPERATOR_ACTIVATION_CELU**

Les opérateurs qui ne sont pas dans cette liste ne sont pas pris en charge pour l’activation fusionnée.

## <a name="see-also"></a>Voir aussi

[Exemple DirectMLSuperResolution](https://github.com/microsoft/DirectML/tree/master/Samples)    
[DML_CONVOLUTION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_convolution_operator_desc)
