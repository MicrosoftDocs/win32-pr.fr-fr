---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Recueille des éléments à partir du tenseur d’entrée, en utilisant les index tenseur pour remapper les index à des sous-blocs complets de l’entrée. | DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 8e74078eaf55f209fba92ba97737d22047a5e67c
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417269"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a>Structure DML_GATHER_ND_OPERATOR_DESC (directml. h)

Recueille des éléments à partir du tenseur d’entrée, en utilisant les index tenseur pour remapper les index à des sous-blocs complets de l’entrée. Cet opérateur effectue le pseudocode suivant, où « ... » représente une série de coordonnées, avec le comportement exact qui dépend du nombre de dimensions d’entrée et d’index.

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur à partir duquel effectuer la lecture.


`IndicesTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les index. Le *DimensionCount* de ce tenseur doit correspondre à *InputTensor. DimensionCount*. La dernière dimension du *IndicesTensor* est en fait le nombre de coordonnées par tuple d’index et ne peut pas dépasser *InputTensor. DimensionCount*. Par exemple, un tenseur d’index de *tailles* `{1,4,5,2}` avec *IndicesDimensionCount* = 3 représente un tableau à de tuples à 2 coordonnées qui sont indexés dans *InputTensor*.

À compter de `DML_FEATURE_LEVEL_3_0` , cet opérateur prend en charge les valeurs d’index négatives lors de l’utilisation d’un type intégral signé avec ce tenseur. Les indices négatifs sont interprétés comme étant relatifs à la fin de la dimension respective. Par exemple, un index de-1 fait référence au dernier élément de cette dimension.


`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur dans lequel écrire les résultats. Le *DimensionCount* et le *type de données* de ce tenseur doivent correspondre à *InputTensor. DimensionCount*. Les *OutputTensor. Sizes* attendues sont la concaténation des segments de début *IndicesTensor. Sizes* et *InputTensor. Sizes* segment de fin à yield :

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

Les dimensions de sortie sont alignées à droite, avec les valeurs les plus grandes ajoutées si nécessaire pour répondre à *OutputTensor. DimensionCount*.

Voici un exemple.

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```


`InputDimensionCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de dimensions d’entrée réelles dans le *InputTensor* après avoir ignoré les éléments de début non significatifs, à partir de `[1, *InputTensor.DimensionCount*]` . Par exemple, étant donné *InputTensor. Sizes*  =  `{1,1,4,6}` et `InputDimensionCount` = 3, les index significatifs réels sont `{1,4,6}` .


`IndicesDimensionCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de dimensions d’index réelles dans le *IndicesTensor* après avoir ignoré les éléments de début non significatifs, à partir de [1, *IndicesTensor. DimensionCount*]. Par exemple, étant donné *IndicesTensor. Sizes*  =  `{1,1,4,6}` et *IndicesDimensionCount* = 3, les index significatifs réels sont `{1,4,6}` .

## <a name="examples"></a>Exemples

### <a name="example-1-1d-remapping"></a>Exemple 1. remappage 1D

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a>Exemple 2. remappage 2D

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a>Remarques
Une version plus récente de cet opérateur, `DML_OPERATOR_GATHER_ND1` , a été introduite dans `DML_FEATURE_LEVEL_3_0` .

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
* *IndicesTensor*, *InputTensor* et *OutputTensor* doivent avoir le même *DimensionCount*.
* *InputTensor* et *OutputTensor* doivent avoir le même *type de données*.

## <a name="tensor-support"></a>Support tenseur
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 et versions ultérieures
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrée | 1 à 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Sortie | 1 à 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 et versions ultérieures
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrée | 4 | UINT32 |
| OutputTensor | Sortie | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |
