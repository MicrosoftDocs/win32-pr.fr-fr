---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Calcule la valeur maximale sur les éléments au sein de la fenêtre glissante sur le tenseur d’entrée, et retourne éventuellement les index des valeurs maximales sélectionnées.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803672"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a>Structure DML_MAX_POOLING2_OPERATOR_DESC (directml. h)
Calcule la valeur maximale sur les éléments au sein de la fenêtre glissante sur le tenseur d’entrée, et retourne éventuellement les index des valeurs maximales sélectionnées.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tenseur d’entrée de *tailles* `{ BatchCount, ChannelCount, Height, Width }` si *InputTensor. DimensionCount* est 4 et `{ BatchCount, ChannelCount, Depth, Height, Weight } ` si *InputTensor. DimensionCount* est 5.


`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie dans lequel écrire les résultats. Les tailles du tenseur de sortie peuvent être calculées comme suit.

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie facultative des index sur le tenseur d’entrée *InputTensor* des valeurs maximales produites et stockées dans le *OutputTensor*. Ces valeurs d’index sont de base zéro et traitent le tenseur d’entrée comme un tableau unidimensionnel contigu. Lorsque plusieurs éléments de la fenêtre glissante ont la même valeur, les valeurs égales ultérieures sont ignorées et l’index pointe vers la première valeur rencontrée. *OutputTensor* et *OutputIndicesTensor* ont les mêmes tailles de tenseur.


`DimensionCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de dimensions spatiales du *InputTensor* d’entrée tenseur, qui correspond également au nombre de dimensions de la fenêtre glissante *Windows*. Cette valeur détermine également la taille des tableaux *Strides*, *StartPadding* et *EndPadding* . Elle doit être définie sur 2 lorsque *InputTensor* est 4D et 3 lorsqu’il s’agit d’un 5D tenseur.


`Strides`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Strides pour les dimensions de fenêtre glissante de tailles `{ Height, Width }` lorsque *DimensionCount* a la valeur 2, ou `{ Depth, Height, Width }` lorsque la valeur 3 est affectée à.


`WindowSize`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Dimensions de la fenêtre glissante dans `{ Height, Width }` lorsque *DimensionCount* a la valeur 2, ou `{ Depth, Height, Width }` lorsque la valeur est égale à 3.


`StartPadding`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Nombre d’éléments de remplissage à appliquer au début de chaque dimension spatiale du *InputTensor* d’entrée tenseur. Les valeurs se trouvent dans `{ Height, Width }` lorsque *DimensionCount* a la valeur 2, ou lorsque la `{ Depth, Height, Width }` valeur est égale à 3.


`EndPadding`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Nombre d’éléments de remplissage à appliquer à la fin de chaque dimension spatiale du *InputTensor* d’entrée tenseur. Les valeurs se trouvent dans `{ Height, Width }` lorsque *DimensionCount* a la valeur 2, ou lorsque la `{ Depth, Height, Width }` valeur est égale à 3.


`Dilations`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Valeurs pour chaque dimension spatiale du tenseur d’entrée *InputTensor* par lequel un élément de la fenêtre glissante est sélectionné pour chaque élément de cette valeur. Les valeurs se trouvent dans `{ Height, Width }` lorsque *DimensionCount* a la valeur 2, ou lorsque la `{ Depth, Height, Width }` valeur est égale à 3.


## <a name="remarks"></a>Notes 
**DML_MAX_POOLING2_OPERATOR_DESC** remplace la version antérieure [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) par des *dilatations* de tableau constantes supplémentaires. Les deux versions sont équivalentes lorsque la valeur de *dilatations* est définie sur `{ 1,1 }` pour une entrée 4D, ou `{ 1,1,1 }` pour les fonctionnalités d’entrée de 5D.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
* *InputTensor*, *OutputIndicesTensor* et *OutputTensor* doivent avoir le même *DimensionCount*.
* *InputTensor* et *OutputTensor* doivent avoir le même *type de données*.

## <a name="tensor-support"></a>Support tenseur
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 et versions ultérieures
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 à 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputTensor | Output | 4 à 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputIndicesTensor | Sortie facultative | 4 à 5 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 et versions ultérieures
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 à 5 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 à 5 | FLOAT32, FLOAT16 |
| OutputIndicesTensor | Sortie facultative | 4 à 5 | UINT32 |


## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 2004 (10,0 ; Build 19041) |
| **Serveur minimal pris en charge** | Windows Server, version 2004 (10,0 ; Build 19041) |
| **En-tête** | directml. h |