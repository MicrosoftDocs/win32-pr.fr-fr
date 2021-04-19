---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Calcule les coordonnées à N dimensions de tous les éléments non nuls du tenseur d’entrée.
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: a662ac3b341c07e512e11dcc15cbc9b11ec5f405
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106523742"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a>Structure DML_NONZERO_COORDINATES_OPERATOR_DESC (directml. h)

Calcule les coordonnées à N dimensions de tous les éléments non nuls du tenseur d’entrée.

Cet opérateur produit une matrice MxN de valeurs, où chaque ligne M contient une coordonnée N-dimensionnel d’une valeur différente de zéro de l’entrée. Lors de l’utilisation des entrées **FLOAT32** ou **FLOAT16** , les valeurs négatives et positives 0 (0.0 f et-0.0 f) sont traitées comme zéro dans le cadre de cet opérateur.

L’opérateur exige que le *OutputCoordinatesTensor* ait une taille suffisamment grande pour prendre en compte un scénario le plus défavorable lorsque chaque élément de l’entrée est différent de zéro. Cet opérateur retourne le nombre d’éléments non nuls via *OutputCountTensor*, que les appelants peuvent inspecter pour déterminer le nombre de coordonnées écrites dans le *OutputCoordinatesTensor*.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur d’entrée.

`OutputCountTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie qui contient le nombre d’éléments non nuls dans le tenseur d’entrée. Ce tenseur doit être un scalaire &mdash; , c’est-à-dire que les tailles de ce tenseur doivent toutes être 1. Le type de ce tenseur doit être **UInt32**.

`OutputCoordinatesTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie qui contient les coordonnées à N dimensions des éléments d’entrée qui ne sont pas nuls. 

Ce tenseur doit avoir une *taille* de `{1,1,M,N}` (si *DimensionCount* est 4), `{1,1,1,M,N}` ou (si *DimensionCount* est 5), où M est le nombre total d’éléments dans le *InputTensor*, et N est supérieur ou égal au *rang effectif* de *InputTensor*, jusqu’à la *DimensionCount* de l’entrée.

Le rang effectif d’un tenseur est déterminé par le *DimensionCount* de ce tenseur, à l’exception des principales dimensions de taille 1. Par exemple, un tenseur avec la taille de `{1,2,3,4}` a le rang 3 effectif, tout comme un tenseur avec des tailles de `{1,1,5,5,5}` . Un tenseur avec des tailles `{1,1,1,1}` a un rang effectif égal à 0.

Prenons l’exemple d’un *InputTensor* avec des *tailles* de `{1,1,12,5}` . Ce tenseur d’entrée contient 60 éléments et a un rang effectif de 2. Dans cet exemple, toutes les tailles valides de *OutputCoordinatesTensor* se présentent sous la forme `{1,1,60,N}` , où n >= 2 mais pas supérieur à *DimensionCount* (4 dans cet exemple).

Les coordonnées écrites dans cet tenseur sont garanties par ordre croissant d’index d’élément. Par exemple, si l’tenseur d’entrée a 3 valeurs non null au niveau des coordonnées {1,0} , {1,2} et {0,5} , les valeurs écrites dans le *OutputCoordinatesTensor* sont `[[0,5], [1,0], [1,2]]` .

Bien que ce tenseur nécessite que sa dimension M soit égale au nombre d’éléments dans le tenseur d’entrée, cet opérateur écrira uniquement un maximum d’éléments OutputCount dans ce tenseur. Le OutputCount est retourné via le *OutputCountTensor* scalaire.

> [!NOTE]
> Les éléments restants de ce tenseur au-delà du OutputCount ne sont pas définis une fois cet opérateur terminé. Vous ne devez pas compter sur les valeurs de ces éléments.

## <a name="example"></a>Exemple

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputTensor*, *OutputCoordinatesTensor* et `OutputCountTensor` doivent avoir le même *DimensionCount*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Dimensions | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrée | {[D0], D1, D2, D3, D4} | 4 à 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputCountTensor | Output | {[1], 1, 1, 1, 1} | 4 à 5 | UINT32 |
| OutputCoordinatesTensor | Output | {[1], 1, 1, M, N} | 4 à 5 | UINT32 |

## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |