---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour la [normalisation du lot](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: ba12541514c8121d483236afa2163a04bd991288
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804464"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a>DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml. h)

Calcule les dégradés de la rétropropagation pour la [normalisation du lot](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc). **DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** effectue plusieurs calculs, qui sont détaillés dans les descriptions de sortie distinctes.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,5 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données d’entrée. Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *InputTensor* pour [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) à l’étape suivante.

`InputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de dégradé entrant. Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente. Ce tenseur doit avoir les mêmes tailles de dimension que *InputTensor*.

`MeanTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données moyennes. Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *MeanTensor* pour [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) à l’étape suivante.

Toutes les dimensions qui n’ont pas la même taille que la dimension correspondante de *InputTensor* doivent avoir une taille de 1 afin qu’elles puissent être diffusées pour correspondre à l’entrée.

Par exemple, les tailles suivantes sont acceptables.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

Voici une erreur dans la mesure où, pour être compatible avec la diffusion, toutes les dimensions qui ne correspondent pas doivent être de taille 1.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données de variance. Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *VarianceTensor* pour [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) à l’étape suivante. Ce tenseur doit avoir les mêmes tailles de dimension que *MeanTensor*.

`ScaleTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données d’échelle. Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *ScaleTensor* pour [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) à l’étape suivante. Ce tenseur doit avoir les mêmes tailles de dimension que *MeanTensor*.

`OutputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Pour chaque valeur correspondante dans les entrées, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .

Ce tenseur doit avoir les mêmes tailles de dimension que *InputTensor* / *InputGradientTensor*.

`OutputScaleGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ce tenseur doit avoir les mêmes tailles de dimension que *MeanTensor* / *VarianceTensor* / *ScaleTensor'*.

Le calcul suivant est effectué ou chaque valeur correspondante dans les entrées.

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

Le `sum` est calculé sur toutes les dimensions qui doivent être diffusées. Si aucune diffusion n’est nécessaire, aucune somme n’est nécessaire.

Voici un exemple.

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

L’élément [0, **0, 0**, 0] de `OutputScaleGradientTensor` est la somme de `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` pour tous les éléments 90 (3 \* 5 \* 6) [[0, 2], **0**, [0,4], [0,5]].

`OutputBiasGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Ce tenseur doit avoir les mêmes tailles de dimension que *MeanTensor* / *VarianceTensor* / *ScaleTensor'*.

Le calcul suivant est effectué ou chaque valeur correspondante dans les entrées.

`OutputBiasGradient = sum(InputGradient)`  

Le `sum` est calculé sur toutes les dimensions qui doivent être diffusées (Voir l’exemple pour *OutputScaleGradientTensor*). Si aucune diffusion n’est nécessaire, aucune somme n’est nécessaire.

`Epsilon`

Type : **[float](/windows/win32/winprog/windows-data-types)**

Petite valeur ajoutée à la variance pour éviter la valeur zéro.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor* et *VarianceTensor* doivent avoir le même *type de données* et *DimensionCount*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16 |
| InputGradientTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16 |
| MeanTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16 |
| VarianceTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | 1 à 8 | FLOAT32, FLOAT16 |
| OutputScaleGradientTensor | Output | 1 à 8 | FLOAT32, FLOAT16 |
| OutputBiasGradientTensor | Output | 1 à 8 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |
