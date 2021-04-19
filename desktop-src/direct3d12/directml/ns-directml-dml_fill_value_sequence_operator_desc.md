---
UID: NS:directml.DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
title: DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
description: Remplit un tenseur avec une séquence.
helpviewer_keywords:
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure
- direct3d12.dml_fill_value_sequence_operator_desc
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
ms.openlocfilehash: ec356568c0860d330234cd990e8cf42ff4ccd120
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106538240"
---
# <a name="dml_fill_value_sequence_operator_desc-structure-directmlh"></a>Structure DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC (directml. h)

Remplit un tenseur avec une séquence. Cet opérateur effectue le pseudo-code suivant.

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
    Value += Delta
endfor
```

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      ValueStart;
  DML_SCALAR_UNION      ValueDelta;
};
```



## <a name="members"></a>Membres

`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur dans lequel écrire les résultats. Ce tenseur peut avoir n’importe quelle taille.


`ValueDataType`

Type : **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**

Type de données du champ de *valeur* , qui doit correspondre à *OutputTensor. DataType*.


`ValueStart`

Type : **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**

Valeur initiale pour remplir le premier élément de la sortie, avec *ValueDataType* déterminant comment interpréter le champ.


`ValueDelta`

Type : **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**

Étape à ajouter à la valeur pour chaque élément écrit, avec *ValueDataType* déterminant comment interpréter le champ.

## <a name="examples"></a>Exemples

### <a name="example-1-1d-ascending-step"></a>Exemple 1. étape d’ordre croissant 1D

```
ValueStart = 3
ValueDelta = 2
ValueDataType = DML_TENSOR_DATA_TYPE_FLOAT32

OutputTensor: (Sizes:{1,1,1,3}, DataType:FLOAT32)
    [[[[3, 5, 7]]]]
```

### <a name="example-2-2d-ascending-step"></a>Exemple 2. étape croissante 2D

```
ValueStart = 10
ValueDelta = -2
ValueDataType = DML_TENSOR_DATA_TYPE_UINT8

OutputTensor: (Sizes:{1,1,2,2}, DataType:UINT8)
    [[[[10, 8],
       [ 6, 4]]]]
```

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |