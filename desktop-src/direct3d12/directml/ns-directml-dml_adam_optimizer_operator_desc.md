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
# <a name="dml_adam_optimizer_operator_desc-structure-directmlh"></a>Structure DML_ADAM_OPTIMIZER_OPERATOR_DESC (directml. h)

Calcule les pondérations mises à jour (paramètres) à l’aide des dégradés fournis, en fonction de l’algorithme Adam (**Ada** ptive **M** oment estimation). Cet opérateur est un optimiseur et est généralement utilisé dans l’étape de mise à jour du poids d’une boucle d’apprentissage pour effectuer une descente de dégradé.

Cet opérateur effectue le calcul suivant :

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

En plus de calculer les paramètres de pondération mis à jour (retournés dans *OutputParametersTensor*), cet opérateur retourne également les estimations des première et deuxième heure mises à jour dans *OutputFirstMomentTensor* et *OutputSecondMomentTensor*, respectivement. En règle générale, vous devez stocker ces estimations des premières et des secondes, et les fournir en tant qu’entrées au cours de l’étape de formation suivante.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
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

## <a name="members"></a>Membres

`InputParametersTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les paramètres (pondérations) auxquels appliquer cet optimiseur. Les estimations du gradient, du premier et du deuxième moment, de l’étape de formation actuelle, ainsi que des hyperparamètres *LearningRate*, *beta1* et *bêta2*, sont utilisées par cet opérateur pour effectuer une descente du gradient sur les valeurs de poids fournies dans ce tenseur.

`InputFirstMomentTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant la première estimation du dégradé pour chaque valeur de poids. Ces valeurs sont généralement obtenues à la suite d’une exécution précédente de cet opérateur, via *OutputFirstMomentTensor*.

Lors de l’application de cet optimiseur à un ensemble de pondérations pour la première fois (par exemple, au cours de l’étape de formation initiale), les valeurs de ce tenseur doivent généralement être initialisées à zéro. Les exécutions suivantes doivent utiliser les valeurs retournées dans *OutputFirstMomentTensor*.

Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.

`InputSecondMomentTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant l’estimation du deuxième moment du dégradé pour chaque valeur de poids. Ces valeurs sont généralement obtenues à la suite d’une exécution précédente de cet opérateur, via *OutputSecondMomentTensor*.

Lors de l’application de cet optimiseur à un ensemble de pondérations pour la première fois (par exemple, au cours de l’étape de formation initiale), les valeurs de ce tenseur doivent généralement être initialisées à zéro. Les exécutions suivantes doivent utiliser les valeurs retournées dans *OutputSecondMomentTensor*.

Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.

`GradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Les dégradés à appliquer aux paramètres d’entrée (pondérations) pour la descente de dégradé. Les dégradés sont généralement obtenus dans une passe de rétropropagation au cours de l’apprentissage.

Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.

`TrainingStepTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur scalaire contenant une valeur entière représentant le nombre d’étapes d’apprentissage en cours. Cette valeur, ainsi que la bêta *2 et bêta2* , sont utilisées pour calculer la dégradation exponentielle du premier et du deuxième cours estimés. 

En général, la valeur de l’étape de formation commence à 0 au début de l’apprentissage et est incrémentée de 1 à chaque étape de formation consécutive. Cet opérateur ne met pas à jour la valeur de l’étape d’apprentissage ; vous devez le faire manuellement, par exemple à l’aide de [DML_OPERATOR_ELEMENT_WISE_ADD](/windows/win32/api/directml/ns-directml-dml_element_wise_add_operator_desc).

Ce tenseur doit être une valeur scalaire (autrement dit, toutes les *tailles* égales à 1) et un type de données [**DML_TENSOR_DATA_TYPE_UINT32**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type).

`OutputParametersTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie qui contient les valeurs de paramètre (poids) mises à jour après l’application de la descente de dégradé.

Pendant la liaison, ce tenseur est autorisé à utiliser un alias pour un tenseur d’entrée éligible, qui peut être utilisé pour effectuer une mise à jour sur place de ce tenseur. Pour plus d’informations, consultez la section [Notes](#remarks) .

Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.

`OutputFirstMomentTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie contenant des estimations de premier moment mises à jour. Vous devez stocker les valeurs de ce tenseur et les fournir dans *InputFirstMomentTensor* au cours de l’étape de formation suivante.

Pendant la liaison, ce tenseur est autorisé à utiliser un alias pour un tenseur d’entrée éligible, qui peut être utilisé pour effectuer une mise à jour sur place de ce tenseur. Pour plus d’informations, consultez la section [Notes](#remarks) .

Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.

`OutputSecondMomentTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie contenant des estimations de deuxième heure mises à jour. Vous devez stocker les valeurs de ce tenseur et les fournir dans *InputSecondMomentTensor* au cours de l’étape de formation suivante.

Pendant la liaison, ce tenseur est autorisé à utiliser un alias pour un tenseur d’entrée éligible, qui peut être utilisé pour effectuer une mise à jour sur place de ce tenseur. Pour plus d’informations, consultez la section [Notes](#remarks) .

Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputParametersTensor*.

`LearningRate`

Type : **float**

Taux d’apprentissage, également communément appelé *taille d’étape*. Le taux d’apprentissage est un hyperparamètre qui détermine l’amplitude de la mise à jour du poids le long du vecteur de dégradé à chaque étape de l’apprentissage.

`Beta1`

Type : **float**

Hyperparamètre représentant la vitesse de dégradation exponentielle de l’estimation du premier moment du dégradé. Cette valeur doit être comprise entre 0,0 et 1,0. Une valeur de 0,9 f est typique.

`Beta2`

Type : **float**

Hyperparamètre représentant la vitesse de dégradation exponentielle de l’estimation du deuxième moment du dégradé. Cette valeur doit être comprise entre 0,0 et 1,0. La valeur 0,999 f est standard.

`Epsilon`

Type : **float**

Petite valeur utilisée pour aider à la stabilité numérique en empêchant la division par zéro. Pour les entrées à virgule flottante 32 bits, les valeurs standard sont 1e-8 ou `FLT_EPSILON` .

## <a name="remarks"></a>Remarques
Cet opérateur prend en charge l’exécution sur place, ce qui signifie que chaque tenseur de sortie est autorisé à aliaser un tenseur d’entrée éligible pendant la liaison. Par exemple, il est possible de lier la même ressource pour *InputParametersTensor* et *OutputParametersTensor* afin d’obtenir efficacement une mise à jour sur place des paramètres d’entrée. Tous les dizaines de temps d’entrée de cet opérateur, à l’exception de *TrainingStepTensor*, peuvent être associés à un alias de cette manière.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Contraintes tenseur
* *GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor*, *OutputSecondMomentTensor* et *TrainingStepTensor* doivent avoir le même *type de données*.
* *GradientTensor*, *InputFirstMomentTensor*, *InputParametersTensor*, *InputSecondMomentTensor*, *OutputFirstMomentTensor*, *OutputParametersTensor* et *OutputSecondMomentTensor* doivent avoir la même *taille*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Dimensions | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputParametersTensor | Entrée | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| InputFirstMomentTensor | Entrée | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| InputSecondMomentTensor | Entrée | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| GradientTensor | Entrée | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| TrainingStepTensor | Entrée | {1, 1, 1,1} | 4 | FLOAT32, FLOAT16 |
| OutputParametersTensor | Sortie | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| OutputFirstMomentTensor | Sortie | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |
| OutputSecondMomentTensor | Sortie | {D0, D1, D2, D3} | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |