---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Vérifie chaque élément de *InputTensor* pour IEEE-754-inf, inf, ou les deux, en fonction du *InfinityMode* donné et place le résultat (1 pour true, 0 pour false) dans l’élément correspondant de *OutputTensor*.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417317"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a>Structure DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC (directml. h)

Vérifie chaque élément de *InputTensor* pour IEEE-754-inf, inf, ou les deux, en fonction du *InfinityMode* donné et place le résultat (1 pour true, 0 pour false) dans l’élément correspondant de *OutputTensor*.

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur d’entrée à partir duquel effectuer la lecture.


`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie dans lequel écrire les résultats.


`InfinityMode`

Type : **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**

[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) déterminant le signe de l’infini à vérifier.

* Si **DML_IS_INFINITY_MODE_EITHER**, la valeur 1 est retournée si l’élément est-inf ou inf, sinon 0.
* Si **DML_IS_INFINITY_MODE_POSITIVE**, la valeur 1 est retournée si l’élément est inf, sinon 0.
* Si **DML_IS_INFINITY_MODE_NEGATIVE**», 1 est retourné si l’élément est-inf, sinon 0.


## <a name="remarks"></a>Remarques
## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputTensor* et *OutputTensor* doivent avoir les mêmes *DimensionCount* et *tailles*.

## <a name="tensor-support"></a>Support tenseur
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 et versions ultérieures
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16 |
| OutputTensor | Sortie | 1 à 8 | DESTINÉES |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 et versions ultérieures
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Sortie | 4 | DESTINÉES |


## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 2004 (10,0 ; Build 19041) |
| **Serveur minimal pris en charge** | Windows Server, version 2004 (10,0 ; Build 19041) |
| **En-tête** | directml. h |