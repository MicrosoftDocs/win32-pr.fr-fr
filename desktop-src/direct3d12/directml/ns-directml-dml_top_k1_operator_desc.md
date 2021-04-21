---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Sélectionne les éléments *K* les plus grands ou les plus petits de chaque séquence le long d’un axe du *InputTensor*, puis retourne les valeurs et les index de ces éléments dans *OutputValueTensor* et *OutputIndexTensor*, respectivement.
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 599541032e0f1711c0e747a4ca5906391849a932
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803815"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a>Structure DML_TOP_K1_OPERATOR_DESC (directml. h)
Sélectionne les éléments *K* les plus grands ou les plus petits de chaque séquence le long d’un axe du *InputTensor*, puis retourne les valeurs et les index de ces éléments dans *OutputValueTensor* et *OutputIndexTensor*, respectivement. Une *séquence* fait référence à l’un des ensembles d’éléments qui existent le long de la dimension d' *axe* du *InputTensor*.

Le choix de sélectionner les éléments les plus importants ou les plus petits éléments K peut être contrôlé à l’aide de *AxisDirection*.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur d’entrée contenant les éléments à sélectionner.

`OutputValueTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie dans lequel écrire les valeurs des premiers éléments *K* . Les *K* premiers éléments sont sélectionnés selon qu’ils sont le plus grand ou le plus petit, en fonction de la valeur de *AxisDirection*. Ce tenseur doit avoir des tailles égales à *InputTensor*, *à l’exception* de la dimension spécifiée par le paramètre *Axis* , qui doit avoir une taille égale à *K*.

Les valeurs *K* sélectionnées à partir de chaque séquence d’entrée sont systématiquement triées par ordre décroissant (du plus grand au plus petit) si *AxisDirection* est [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md). Dans le cas contraire, l’inverse est vrai et les valeurs sélectionnées sont systématiquement triées par ordre croissant (du plus petit au plus grand).

`OutputIndexTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie dans lequel écrire les index des premiers éléments *K* . Ce tenseur doit avoir des tailles égales à *InputTensor*, *à l’exception* de la dimension spécifiée par le paramètre *Axis* , qui doit avoir une taille égale à *K*.

Les index retournés dans ce tenseur sont mesurés par rapport au début de leur séquence (par opposition au début du tenseur). Par exemple, un index de 0 fait toujours référence au premier élément pour toutes les séquences d’un axe.

Dans les cas où deux ou plusieurs éléments de la clause TOP-K ont la même valeur (autrement dit, en cas d’égalité), les index des deux éléments sont inclus et sont assurés d’être classés par ordre croissant des index des éléments. Notez que cela est vrai, quelle que soit la valeur de *AxisDirection*.

`Axis`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Index de la dimension dans laquelle sélectionner les éléments. Cette valeur doit être inférieure à la *DimensionCount* du *InputTensor*.

`K`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre d’éléments à sélectionner. *K* doit être supérieur à 0, mais inférieur au nombre d’éléments dans *InputTensor* le long de la dimension spécifiée par *Axis*.

`AxisDirection`

Type : **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Valeur de l’énumération [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) . Si la valeur est **DML_AXIS_DIRECTION_INCREASING**, cet opérateur retourne les *plus petits* éléments *K* par ordre de valeur d’incrément. Dans le cas contraire, elle retourne les éléments *K* les *plus importants* dans l’ordre décroissant.

## <a name="examples"></a>Exemples

### <a name="example-1"></a>Exemple 1

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a>Exemple 2. Utilisation d’un autre axe

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a>Exemple 3. Valeurs liées

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a>Exemple 4 : Incrémentation de la direction de l’axe

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a>Notes 
Quand *AxisDirection* a la valeur [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), cet opérateur équivaut à [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur

* *InputTensor*, *OutputIndexTensor* et *OutputValueTensor* doivent avoir le même *DimensionCount*.
* *InputTensor* et *OutputValueTensor* doivent avoir le même *type de données*.

## <a name="tensor-support"></a>Support tenseur

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 et versions ultérieures

| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputValueTensor | Output | 1 à 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputIndexTensor | Output | 1 à 8 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 et versions ultérieures

| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputValueTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputIndexTensor | Output | 4 | UINT32 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |
