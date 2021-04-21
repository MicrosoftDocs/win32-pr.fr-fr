---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Exécute une fonction de multiplication de matrice sur des données quantifiées. Cet opérateur est mathématiquement équivalent à déquantifier les entrées, à effectuer une multiplication de matrice, puis à quantifier la sortie.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803568"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a>Structure DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC (directml. h)
Exécute une fonction de multiplication de matrice sur des données quantifiées. Cet opérateur est mathématiquement équivalent à déquantifier les entrées, à effectuer une multiplication de matrice, puis à quantifier la sortie.

Cet opérateur exige que la matrice multiplie les dizaines d’entrée par 4D qui sont mis en forme en tant que `{ BatchCount, ChannelCount, Height, Width }` . L’opérateur de multiplication de matrice effectue un nombre BatchCount * ChannelCount de multiplications de matrices indépendantes. 

Par exemple, si *ATensor* a *une taille de* , et que BTensor a une taille de, `{ BatchCount, ChannelCount, M, K }` et que   `{ BatchCount, ChannelCount, K, N }` *OutputTensor* a une *taille* de, `{ BatchCount, ChannelCount, M, N }` alors l’opérateur de multiplication de matrice effectuera BatchCount * ChannelCount des multiplications de matrices indépendantes {M, K} x {K, N} = {m, n}. 

### <a name="dequantize-function"></a>Dequantifier la fonction

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Fonction quantifier

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Membres

`ATensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données. Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, M, K }` .


`AScaleTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données de mise à l’échelle ATensor. Les dimensions attendues du `AScaleTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise. Ces valeurs de mise à l’échelle sont utilisées pour déquantifier les valeurs A.


`AZeroPointTensor`

Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur facultatif contenant les données de point zéro *ATensor* . Les dimensions attendues du AZeroPointTensor sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise. Ces valeurs de zéro point sont utilisées pour déquantifier les valeurs de ATensor.


`BTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données B. Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, K, N }` .


`BScaleTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données de mise à l’échelle *BTensor* . Les dimensions attendues du `BScaleTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, 1, N }` si la quantification par colonne est requise. Ces valeurs de mise à l’échelle sont utilisées pour déquantifier les valeurs *BTensor* .


`BZeroPointTensor`

Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur facultatif contenant les données de point zéro *BTensor* . Les dimensions attendues du `BZeroPointTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, 1, N }` si la quantification par colonne est requise. Ces valeurs de zéro point sont utilisées pour déquantifier les valeurs de *BTensor* .


`OutputScaleTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données de mise à l’échelle du filtre. Les dimensions attendues du `OutputScaleTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise. Cette valeur de mise à l’échelle est utilisée pour déquantifier les valeurs de filtre.


`OutputZeroPointTensor`

Type : _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur facultatif contenant les données de point zéro du filtre. Les dimensions attendues du `OutputZeroPointTensor` sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise ou `{ 1, 1, M, 1 }` si la quantification par ligne est requise. Cette valeur de point zéro est utilisée pour déquantifier les valeurs de filtre.


`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur dans lequel écrire les résultats. Les dimensions de ce tenseur sont `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
* *ATensor* et `AZeroPointTensor` doivent avoir le même *type de données*.
* *BTensor* et `BZeroPointTensor` doivent avoir le même *type de données*.
* *OutputTensor* et `OutputZeroPointTensor` doivent avoir le même *type de données*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Entrée | 4 | INT8, UINT8 |
| AScaleTensor | Entrée | 4 | FLOAT32 |
| AZeroPointTensor | Entrée facultative | 4 | INT8, UINT8 |
| BTensor | Entrée | 4 | INT8, UINT8 |
| BScaleTensor | Entrée | 4 | FLOAT32 |
| BZeroPointTensor | Entrée facultative | 4 | INT8, UINT8 |
| OutputScaleTensor | Entrée | 4 | FLOAT32 |
| OutputZeroPointTensor | Entrée facultative | 4 | INT8, UINT8 |
| OutputTensor | Output | 4 | INT8, UINT8 |



## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |