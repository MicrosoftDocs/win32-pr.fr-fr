---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Multiplie les éléments d’un tenseur le long d’un axe, en écrivant le Tally en cours d’exécution du produit dans le tenseur de sortie.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: cb4006a20dd25751c027ba97e63dcfc60c25faf6
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282558"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a>DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml. h)

Multiplie les éléments d’un tenseur le long d’un axe, en écrivant le Tally en cours d’exécution du produit dans le tenseur de sortie.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,5 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données d’entrée. Il s’agit généralement du même tenseur que celui qui a été fourni en tant que *InputTensor* pour [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) à l’étape suivante.

Tenseur d’entrée contenant les éléments à multiplier.

`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie dans lequel écrire les produits cumulatifs résultants. Ce tenseur doit avoir la même taille et le même type de données que *InputTensor*.

`Axis`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Index de la dimension sur laquelle multiplier les éléments. Cette valeur doit être inférieure à la *DimensionCount* du *InputTensor*.

`AxisDirection`

Type : **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

L’une des valeurs de l’énumération [DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction) . Si la valeur est **DML_AXIS_DIRECTION_INCREASING**, le produit se produit en parcourant le tenseur le long de l’axe spécifié par l’index d’élément croissant. Si la valeur est **DML_AXIS_DIRECTION_DECREASING**, l’inverse est vrai et le produit se produit en parcourant les éléments par ordre décroissant d’index.

`HasExclusiveProduct`

Type : <b> <a href="/windows/win32/winprog/windows-data-types">bool</a></b>

Si la valeur est **true**, la valeur de l’élément actuel est exclue lors de l’écriture du Tally en cours d’exécution dans le tenseur de sortie. Si la valeur est **false**, la valeur de l’élément actuel est incluse dans le Tally en cours d’exécution.

## <a name="examples"></a>Exemples

Les exemples de cette section utilisent tous ce même tenseur d’entrée.

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a>Exemple 1. Produit cumulatif sur des éclats horizontaux

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a>Exemple 2. Produits exclusifs

La définition de *HasExclusiveProduct* sur **true** a pour effet d’exclure la valeur de l’élément actuel de la Tally en cours d’exécution lors de l’écriture dans le tenseur de sortie.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a>Exemple 3. Direction de l’axe

La définition de *AxisDirection* sur [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/api/directml/ne-directml-dml_axis_direction) a pour effet d’inverser l’ordre de traversée des éléments lors du calcul de la Tally en cours d’exécution.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a>Exemple 4 : Multiplication sur un axe différent

Dans cet exemple, le produit se produit verticalement, le long de l’axe de la hauteur (deuxième dimension).

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a>Remarques
Cet opérateur prend en charge l’exécution sur place, ce qui signifie que le tenseur de sortie est autorisé à aliaser les *InputTensor* pendant la liaison.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputTensor* et *OutputTensor* doivent avoir les mêmes *types de données*, *DimensionCount* et *tailles*.

## <a name="tensor-support"></a>Support tenseur
### <a name="dml_feature_level_4_0-and-above"></a>DML_FEATURE_LEVEL_4_0 et versions ultérieures
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Output | 1 à 8 | FLOAT32, FLOAT16, UINT32, UINT16 |

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 et versions ultérieures
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |