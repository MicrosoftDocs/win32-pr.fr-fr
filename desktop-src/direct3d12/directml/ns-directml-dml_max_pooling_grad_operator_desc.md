---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour le regroupement Max (voir [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
helpviewer_keywords:
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- DML_MAX_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_MAX_POOLING_GRAD_OPERATOR_DESC, DML_MAX_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 3b0b10fa8ee17c9d06e779c3c990f134bc4ae669
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803426"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a>Structure DML_MAX_POOLING_GRAD_OPERATOR_DESC (directml. h)

Calcule les dégradés de la rétropropagation pour le regroupement Max (voir [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).

Imaginez un **DML_MAX_POOLING2_OPERATOR_DESC** 2x2 sans remplissage ni dilatations et une Stride de 1, qui effectue les opérations suivantes.

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

Le plus grand élément de chaque fenêtre 2x2 dans le tenseur d’entrée génère un élément de la sortie. Voici un exemple de la sortie de **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, en fonction de paramètres similaires.

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

En effet, cet opérateur utilise *InputTensor* pour déterminer l’index du plus grand élément de chaque fenêtre et distribue les valeurs de *InputGradientTensor* dans le *OutputGradientTensor* en fonction de ces index. Lorsque les index se chevauchent, les valeurs sont additionnées. Tous les éléments de sortie non référencés sont mis à zéro.

Dans le cas d’un lien (où plusieurs éléments d’une fenêtre ont la même valeur maximale), l’élément avec l’index d’élément logique le plus bas est choisi.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe

```cpp
struct DML_MAX_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  _Field_size_(DimensionCount) const UINT* Dilations;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

La fonctionnalité d’entrée tenseur. Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *InputTensor* pour [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) à l’étape suivante.

`InputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de dégradé entrant. Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente. En général, ce tenseur a la même taille que la *sortie* de la [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) correspondante dans la passe de transfert.

`OutputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie contenant les dégradés de la page. En général, ce tenseur a la même taille que l' *entrée* de la [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) correspondante dans la passe en avant.

`DimensionCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre d’éléments dans les tableaux *Strides*, *Windows*, *StartPadding*, *EndPadding* et *dilatations* . Cette valeur doit être égale au nombre de dimensions spatiales (InputTensor DimensionCount-2). Étant donné que cet opérateur ne prend en charge que les dizaines de 4D, la seule valeur valide pour ce paramètre est 2.

`Strides`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consultez la section *Strides* dans [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`WindowSize`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consultez *Windows* dans [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`StartPadding`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consultez *StartPadding* dans [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`EndPadding`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consultez *EndPadding* dans [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

`Dilations`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consultez les *dilatations* dans [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Contraintes tenseur
* *InputTensor* et *OutputGradientTensor* doivent avoir la même *taille*.
* *InputGradientTensor*, *InputTensor* et *OutputGradientTensor* doivent avoir le même *type de données*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Dimensions | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrée | { BatchCount, ChannelCount, InputHeight, InputWidth } | 4 | FLOAT32, FLOAT16 |
| InputGradientTensor | Entrée | { BatchCount, ChannelCount, OutputHeight, OutputWidth } | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | { BatchCount, ChannelCount, InputHeight, InputWidth } | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |