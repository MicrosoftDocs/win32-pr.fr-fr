---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Additionne les éléments d’un tenseur le long d’un axe, en écrivant le haut de la somme en cours dans le tenseur de sortie.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 2862a2add207b0bb6c41f5c1aabbc390797cba23
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803351"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a>Structure DML_CUMULATIVE_SUMMATION_OPERATOR_DESC (directml. h)

Additionne les éléments d’un tenseur le long d’un axe, en écrivant le haut de la somme en cours dans le tenseur de sortie.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur d’entrée contenant les éléments à additionner.

`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie dans lequel écrire les sommes cumulées qui en résultent. Ce tenseur doit avoir les mêmes tailles et le même type de données que le *InputTensor*.

`Axis`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Index de la dimension sur laquelle somme les éléments. Cette valeur doit être inférieure à la *DimensionCount* du *InputTensor*.

`AxisDirection`

Type : **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

L’une des valeurs de l’énumération [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) . Si la valeur est **DML_AXIS_DIRECTION_INCREASING**, la somme se produit en parcourant le tenseur le long de l’axe spécifié par l’index d’élément croissant. Si la valeur est **DML_AXIS_DIRECTION_DECREASING**, l’inverse est vrai et la somme se produit en parcourant les éléments par ordre décroissant d’index.

`HasExclusiveSum`

Type : <b> <a href="/windows/win32/winprog/windows-data-types">bool</a></b>

Si la valeur est **true**, la valeur de l’élément actuel est exclue lors de l’écriture du Tally en cours d’exécution dans le tenseur de sortie. Si la valeur est **false**, la valeur de l’élément actuel est incluse dans le Tally en cours d’exécution.

## <a name="examples"></a>Exemples

Les exemples de cette section utilisent tous un tenseur d’entrée avec les propriétés suivantes.

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-summation-across-horizontal-slivers"></a>Exemple 1. Somme cumulée sur des éclats horizontaux

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  3,  6, 11],     // i.e. [2, 2+1, 2+1+3, 2+1+3+5]
   [3, 11, 18, 21],     //      [...                   ]
   [9, 15, 17, 21]]]]   //      [...                   ]
```

### <a name="example-2-exclusive-sums"></a>Exemple 2. Sommes exclusives

La définition de *HasExclusiveSum* sur **true** a pour effet d’exclure la valeur de l’élément actuel de la Tally en cours d’exécution lors de l’écriture dans le tenseur de sortie.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[0, 2,  3,  6],      // Notice the sum is written before adding the input,
   [0, 3, 11, 18],      // and the final total is not written to any output.
   [0, 9, 15, 17]]]]
```

### <a name="example-3-axis-direction"></a>Exemple 3. Direction de l’axe

La définition de *AxisDirection* sur [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) a pour effet d’inverser l’ordre de traversée des éléments lors du calcul de la Tally en cours d’exécution.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[11,  9,  8,  5],    // i.e. [2+1+3+5, 1+3+5, 3+5, 5]
   [21, 18, 10,  3],    //      [...                   ]
   [21, 12,  6,  4]]]]  //      [...                   ]
```

### <a name="example-4-summing-along-a-different-axis"></a>Exemple 4 : Somme sur un axe différent

Dans cet exemple, la somme se produit verticalement, le long de l’axe de la hauteur (deuxième dimension).

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 5,  9, 10,  8],   //      [2+3,  ...]
   [14, 15, 12, 12]]]] //      [2+3+9 ...]
```

## <a name="remarks"></a>Notes 
Cet opérateur prend en charge l’exécution sur place, ce qui signifie que le *OutputTensor* est autorisé à aliaser le *InputTensor* au cours de la liaison.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputTensor* et *OutputTensor* doivent avoir le même *type de données* et les mêmes *tailles*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |
