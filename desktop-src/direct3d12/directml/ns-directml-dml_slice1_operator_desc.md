---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Extrait une sous-région unique (« Slice ») d’un tenseur d’entrée.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: f34525865be9541da879e66e88c29d4a2ab74f00
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417184"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a>Structure DML_SLICE1_OPERATOR_DESC (directml. h)
Extrait une sous-région unique (« Slice ») d’un tenseur d’entrée.

La *fenêtre d’entrée* décrit les limites de l’entrée tenseur à prendre en compte dans la tranche. La fenêtre est définie à l’aide de trois valeurs pour chaque dimension.

- Le *décalage* marque le *début de la fenêtre* dans une dimension.
- La *taille* marque l’étendue de la fenêtre dans une dimension. La *fin de la fenêtre* dans une dimension est `offset + size - 1` .
- Le *Stride* indique comment parcourir les éléments d’une dimension.
  - L’amplitude du Stride indique le nombre d’éléments à avancer lors de la copie dans la fenêtre.
  - Si une Stride est positive, les éléments sont copiés à partir du *début* de la fenêtre dans la dimension.
  - Si une valeur Stride est négative, les éléments sont copiés à partir de la *fin* de la fenêtre de la dimension.

Le pseudo-code suivant illustre la façon dont les éléments sont copiés à l’aide de la fenêtre d’entrée. Notez comment les éléments d’une dimension sont copiés du début à la fin avec un Stride positif et copiés de fin à début avec un Stride négatif.

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

La fenêtre d’entrée ne doit pas être vide dans toutes les dimensions et les ne doit pas de fenêtre s’étendent au-delà des dimensions du tenseur d’entrée (les lectures hors limites ne sont pas autorisées). La taille et les Strides de la fenêtre limitent efficacement le nombre d’éléments qui peuvent être copiés à partir de chaque dimension `i` du tenseur d’entrée.

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

Le tenseur de sortie n’est pas requis pour copier tous les éléments accessibles dans la fenêtre. La tranche est valide aussi longtemps que `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur à partir duquel extraire les tranches.


`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur dans lequel écrire les résultats de données découpées.


`DimensionCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de dimensions. Ce champ détermine la taille des tableaux *InputWindowOffsets*, *InputWindowSizes* et *InputWindowStrides* . Cette valeur doit correspondre à la *DimensionCount* des dizaines d’entrée et de sortie. Cette valeur doit être comprise entre 1 et 8 inclus, à partir de `DML_FEATURE_LEVEL_3_0` ; les niveaux de fonctionnalités antérieurs nécessitent une valeur de 4 ou 5.


`InputWindowOffsets`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Tableau contenant le début (éléments) de la fenêtre d’entrée dans chaque dimension. Les valeurs du tableau doivent satisfaire la contrainte `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowSizes`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Tableau contenant l’étendue (en éléments) de la fenêtre d’entrée dans chaque dimension. Les valeurs du tableau doivent satisfaire la contrainte `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowStrides`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Tableau contenant le Stride de la tranche le long de chaque dimension du tenseur d’entrée, en éléments. L’amplitude du Stride indique le nombre d’éléments à avancer lors de la copie dans la fenêtre d’entrée. Le signe du Stride détermine si les éléments sont copiés à partir du début de la fenêtre (Stride positif) ou jusqu’à la fin de la fenêtre (Stride négative). Les Strides ne peuvent pas être 0.

## <a name="examples"></a>Exemples

Les exemples suivants utilisent ce même tenseur d’entrée.

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a>Exemple 1. Tranche strided avec des Strides positifs

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

Les éléments copiés sont calculés comme suit. 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a>Exemple 2. Tranche strided avec des Strides négatifs

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

Rappelez-vous que les dimensions avec des Strides de fenêtre négatifs commencent à copier à la fin de la fenêtre d’entrée pour cette dimension ; pour ce faire, ajoutez `InputWindowSize[i] - 1` au décalage de la fenêtre. Les dimensions avec un Stride positif commencent simplement à `InputWindowOffset[i]` .
- L’axe 0 (Stride de la `+1` fenêtre) commence la copie à `InputWindowOffsets[0] = 0` . 
- L’axe 1 ( `+1` fenêtre Stride) commence la copie à `InputWindowOffsets[1] = 0` . 
- L’axe 2 (Stride de la `-2` fenêtre) commence la copie à `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` . 
- L’axe 3 (Stride de la `+2` fenêtre) commence la copie à `InputWindowOffsets[3] = 1` . 

Les éléments copiés sont calculés comme suit. 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a>Remarques
Cet opérateur est semblable à [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), mais il diffère de deux façons importantes.

- Les Strides de secteur peuvent être négatifs, ce qui permet d’inverser les valeurs le long des dimensions.
- Les tailles des fenêtres d’entrée ne sont pas nécessairement les mêmes que celles de la sortie tenseur.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputTensor* et *OutputTensor* doivent avoir le même *type de données* et *DimensionCount*.

## <a name="tensor-support"></a>Support tenseur
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 et versions ultérieures
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Sortie | 1 à 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 et versions ultérieures
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 à 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Sortie | 4 à 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |