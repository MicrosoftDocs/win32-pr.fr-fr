---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Effectue une convolution du *FilterTensor* avec *InputTensor*. Cet opérateur effectue une convolution ascendante sur des données de type entier.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: c16690ea1e3049ffeba398bbbaca2003f965a832
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106524759"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a>Structure DML_CONVOLUTION_INTEGER_OPERATOR_DESC (directml. h)

Effectue une convolution du *FilterTensor* avec *InputTensor*. Cet opérateur effectue une convolution ascendante sur des données de type entier. Des dizaines de points nuls facultatifs peuvent également être utilisés pour soustraire les valeurs de point zéro des tenseur d’entrée et de filtre.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données d’entrée. Les dimensions attendues du *InputTensor* sont `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputZeroPointTensor`

Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur facultatif contenant les données de point zéro en entrée. Les dimensions attendues du *InputZeroPointTensor* sont `{ 1, 1, 1, 1 }` .


`FilterTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données de filtre. Les dimensions attendues du *FilterTensor* sont `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterZeroPointTensor`

Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur facultatif contenant les données de point zéro du filtre. Les dimensions attendues du *FilterZeroPointTensor* sont `{ 1, 1, 1, 1 }` si la quantification par tenseur est requise, ou `{ 1, OutputChannelCount, 1, 1 }` si la quantification par canal est requise.


`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur dans lequel écrire les résultats. Les dimensions attendues du *OutputTensor* sont `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de dimensions spatiales pour l’opération de convolution. Les dimensions spatiales sont les dimensions inférieures de la convolution *FilterTensor*. Cette valeur détermine également la taille des tableaux *Strides*, *dilatations*, *StartPadding* et *EndPadding* . Seule une valeur de 2 est prise en charge.


`Strides`

Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Tableau contenant les Strides de l’opération de convolution. Ces Strides sont appliqués au filtre de convolution. Ils sont distincts des Strides tenseur inclus dans [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).


`Dilations`

Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Tableau contenant les dilatations de l’opération de convolution. Les dilatations sont des Strides appliqués aux éléments du noyau de filtre. Cela a pour effet de simuler un plus grand noyau de filtre en remplissant les éléments de noyau de filtre internes avec des zéros.


`StartPadding`

Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Tableau contenant les valeurs de remplissage à appliquer au début de chaque dimension spatiale du filtre et tenseur d’entrée de l’opération de convolution.


`EndPadding`

Type : \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Tableau contenant les valeurs de remplissage à appliquer à la fin de chaque dimension spatiale du filtre et tenseur d’entrée de l’opération de convolution.


`GroupCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de groupes dans lesquels diviser l’opération de convolution. *GroupCount* peut être utilisé pour obtenir une convolution de profondeur en définissant le *GroupCount* égal au nombre de canaux d’entrée. Cela divise la convolution en une convolution distincte par canal d’entrée.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
* *FilterTensor* et *FilterZeroPointTensor* doivent avoir le même *type de données*.
* *InputTensor* et *InputZeroPointTensor* doivent avoir le même *type de données*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Dimensions | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrée | { BatchCount, InputChannelCount, InputHeight, InputWidth } | 4 | INT8, UINT8 |
| InputZeroPointTensor | Entrée facultative | {1, 1, 1,1} | 4 | INT8, UINT8 |
| FilterTensor | Entrée | { FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth } | 4 | INT8, UINT8 |
| FilterZeroPointTensor | Entrée facultative | {1, FilterZeroPointChannelCount, 1,1} | 4 | INT8, UINT8 |
| OutputTensor | Output | { BatchCount, OutputChannelCount, OutputHeight, OutputWidth } | 4 | INT32 |



## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |