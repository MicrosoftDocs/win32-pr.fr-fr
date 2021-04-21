---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Exécute une fonction de multiplication de matrice sur des données de type entier.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802837"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a>Structure DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC (directml. h)
Exécute une fonction de multiplication de matrice sur des données de type entier.

Cet opérateur exige que la matrice multiplie les dizaines d’entrée par 4D, qui sont mis en forme en tant que `{ BatchCount, ChannelCount, Height, Width }` . L’opérateur de multiplication de matrice effectue un nombre BatchCount * ChannelCount de multiplications de matrices indépendantes.

Par exemple, si *ATensor* a *une taille de* , et que BTensor a une taille de, `{ BatchCount, ChannelCount, M, K }` et que   `{ BatchCount, ChannelCount, K, N }` *OutputTensor* a une *taille* de, `{ BatchCount, ChannelCount, M, N }` alors l’opérateur de multiplication de matrice effectuera BatchCount * ChannelCount des multiplications de matrices indépendantes {M, K} x {K, N} = {m, n}.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Membres

`ATensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données. Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, M, K }` .


`AZeroPointTensor`

Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur facultatif contenant les données de point zéro ATensor. Les dimensions attendues du `AZeroPointTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise. Ces valeurs de zéro point sont utilisées pour déquantifier les valeurs de *ATensor* .


`BTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données B. Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, K, N }` .


`BZeroPointTensor`

Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur facultatif contenant les données de point zéro *BTensor* . Les dimensions attendues du `BZeroPointTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, 1, N }` si la quantification par colonne est requise. Ces valeurs de zéro point sont utilisées pour déquantifier les valeurs de BTensor.


`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur avec lequel écrire les résultats. Les dimensions de ce tenseur sont `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
* *ATensor* et `AZeroPointTensor` doivent avoir le même *type de données*.
* *BTensor* et `BZeroPointTensor` doivent avoir le même *type de données*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Dimensions | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| ATensor | Entrée | {BatchCount, ChannelCount, M, K} | 4 | INT8, UINT8 |
| AZeroPointTensor | Entrée facultative | {1, 1, AZeroPointCount, 1} | 4 | INT8, UINT8 |
| BTensor | Entrée | {BatchCount, ChannelCount, K, N} | 4 | INT8, UINT8 |
| BZeroPointTensor | Entrée facultative | {1, 1, 1, BZeroPointCount} | 4 | INT8, UINT8 |
| OutputTensor | Output | {BatchCount, ChannelCount, M, N} | 4 | INT32 |



## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |