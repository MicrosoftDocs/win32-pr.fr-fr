---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: Génère les index des éléments de valeur minimale dans une ou plusieurs dimensions du tenseur d’entrée.
helpviewer_keywords:
- DML_ARGMIN_OPERATOR_DESC
- DML_ARGMIN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMIN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMIN_OPERATOR_DESC, DML_ARGMIN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
- directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
ms.openlocfilehash: 30d281c6ab35675e0cfce80b7eb025292c501041
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106532346"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a>Structure DML_ARGMIN_OPERATOR_DESC (directml. h)

Génère les index des éléments de valeur minimale dans une ou plusieurs dimensions du tenseur d’entrée.

Chaque élément de sortie est le résultat de l’application d’une réduction *argmin* sur un sous-ensemble du tenseur d’entrée. La fonction *argmin* génère l’index de l’élément de valeur minimale dans un jeu d’éléments d’entrée. Les éléments d’entrée impliqués dans chaque réduction sont déterminés par les axes d’entrée fournis. De même, chaque index de sortie est relatif aux axes d’entrée fournis. Si tous les axes d’entrée sont spécifiés, l’opérateur applique une seule réduction *argmin* et produit un seul élément Output.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_ARGMIN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur à partir duquel effectuer la lecture.

`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur dans lequel écrire les résultats. Chaque élément de sortie est le résultat d’une réduction *argmin* sur un sous-ensemble d’éléments du *InputTensor*.

- *DimensionCount* doit correspondre à *InputTensor. DimensionCount* (le rang du tenseur d’entrée est préservé).
- Les *tailles* doivent correspondre à *InputTensor.* sizes, à l’exception des dimensions incluses dans les *axes* réduits, qui doivent être de taille 1.

`AxisCount`

Type : **[uint](/windows/desktop/WinProg/windows-data-types)**

Nombre d’axes à réduire. Ce champ détermine la taille du tableau *axes* .

`Axes`

Type : \_ Field_size \_ (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Axes avec lesquels réduire. Les valeurs doivent être comprises dans la plage `[0, InputTensor.DimensionCount - 1]` .

`AxisDirection`

DML_AXIS_DIRECTION AxisDirection ;

Type : **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

Détermine l’index à sélectionner lorsque plusieurs éléments d’entrée ont la même valeur.
- **DML_AXIS_DIRECTION_INCREASING** retourne l’index du premier élément à valeur minimale (par exemple, `argmin({1,2,3,2,1}) = 0` )
- **DML_AXIS_DIRECTION_DECREASING** retourne l’index du dernier élément à valeur minimale (par exemple, `argmin({1,2,3,2,1}) = 4` )

## <a name="examples"></a>Exemples

Les exemples de cette section utilisent tous ce même tenseur d’entrée à deux dimensions.

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a>Exemple 1. Application de *argmin* à des colonnes

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a>Exemple 2. Application de *argmin* à des lignes

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a>Exemple 3. Application de *argmin* à tous les axes (le tenseur entier)

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a>Notes
Les tailles de tenseur de sortie doivent être les mêmes que les tailles de tenseur d’entrée, à l’exception des axes réduits, qui doivent être 1.

Quand *AxisDirection* est [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), cette API est équivalente à [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) avec [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).

Un sous-ensemble de cette fonctionnalité est exposé via l’opérateur [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) et est pris en charge sur les niveaux de fonctionnalité DirectML antérieurs.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputTensor* et *OutputTensor* doivent avoir le même *DimensionCount*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 à 8 | INT64, INT32, UINT64, UINT32 |

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |