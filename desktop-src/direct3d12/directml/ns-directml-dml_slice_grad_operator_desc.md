---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour la tranche (voir [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: a22efe9b0b74f5fdc7b498b97784086f40f243b9
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417288"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a>Structure DML_SLICE_GRAD_OPERATOR_DESC (directml. h)

Calcule les dégradés de la rétropropagation pour la tranche (voir [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).

Rappelez-vous que [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extrait une sous-région d’un tenseur d’entrée. Étant donné un *InputGradientTensor* avec les mêmes tailles que la *sortie* d’un **DML_SLICE1_OPERATOR_DESC** équivalent, cet opérateur produit un *OutputGradientTensor* avec les mêmes tailles que l' *entrée* de **DML_SLICE1_OPERATOR_DESC**. Les éléments découpés sont propagés à la sortie, et tous les autres éléments ont la valeur 0.

Par exemple, considérez un **DML_SLICE1_OPERATOR_DESC** qui extrait les éléments suivants à partir d’un tenseur :

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

Si vous fournissez la même taille de *InputWindowOffsets* /  /  que dans l’exemple ci-dessus, cet opérateur effectuerait ensuite la transformation suivante.

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a>Membres

`InputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de dégradé entrant. Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente. En règle générale, ce tenseur a la même taille que la *sortie* de la [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) correspondante dans la passe de transfert.

`OutputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie contenant les dégradés de la page. En règle générale, ce tenseur aurait les mêmes tailles que l' *entrée* de la [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) correspondante dans la passe en avant.

`DimensionCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre d’éléments dans les tableaux *InputWindowOffsets*, *InputWindowSizes* et *InputWindowStrides* . Cette valeur doit être égale à la valeur de *DimensionCount* fournie dans *InputGradientTensor* et *OutputGradientTensor*.

`InputWindowOffsets`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consultez *InputWindowOffsets* dans [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowSizes`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consultez *InputWindowSizes* dans [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

`InputWindowStrides`

Type : \_ \_ taille \_ de champ (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Consultez *InputWindowStrides* dans [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).

Notez que contrairement à **DML_SLICE1_OPERATOR_DESC**, cet opérateur requiert des Strides non nuls. En effet, avec une Stride zéro, il est ambigu quant à l’élément d’entrée qui doit être mappé à chaque élément de sortie, et par conséquent, la rétropropagation ne peut pas être exécutée. Comme **DML_SLICE1_OPERATOR_DESC**, les Strides négatifs inversent la direction de la fenêtre d’entrée le long de cet axe.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputGradientTensor* et *OutputGradientTensor* doivent avoir le même *type de données* et *DimensionCount*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputGradientTensor | Sortie | 1 à 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |