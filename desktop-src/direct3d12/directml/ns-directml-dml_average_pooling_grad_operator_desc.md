---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour le regroupement moyen (voir [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: aaa2b5d2becac421214afe7c643426c1c93cf899
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550484"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a>Structure DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC (directml. h)

Calcule les dégradés de la rétropropagation pour le regroupement moyen (voir [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).

Imaginez un **DML_AVERAGE_POOLING_OPERATOR_DESC** 2x2, sans remplissage et un Stride de 1, qui effectue les opérations suivantes.

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

Chaque fenêtre 2x2 dans le tenseur d’entrée est calculée pour produire un élément de la sortie (en lisant des zéros pour les éléments situés au-delà du bord). Voici un exemple de la sortie de **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** données similaires.

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

Notez que les valeurs de *OutputGradientTensor* représentent les contributions pondérées de cet élément au *OutputTensor* au cours de l’opérateur de [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) d’origine.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a>Membres

`InputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de dégradé entrant. Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente. En général, ce tenseur a la même taille que la *sortie* de la [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) correspondante dans la passe de transfert.

`OutputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie contenant les dégradés de la page. En général, ce tenseur a la même taille que l' *entrée* de la [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) correspondante dans la passe en avant.

`DimensionCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre d’éléments dans les tableaux *Strides*, *Windows*, *StartPadding* et *EndPadding* . Cette valeur doit être égale au nombre de dimensions spatiales. Le nombre de dimensions spatiales est 2 si des dizaines 4D sont fournis, ou 3 si les dizaines de 5D sont fournis.

`Strides`

Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***

Consultez la section *Strides* dans [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`WindowSize`

Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***

Consultez *Windows* dans [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`StartPadding`

Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***

Consultez *StartPadding* dans [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`EndPadding`

Type : \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***

Consultez *EndPadding* dans [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`IncludePadding`

Type : <b> <a href="/windows/win32/winprog/windows-data-types">bool</a></b>

Consultez *IncludePadding* dans [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputGradientTensor* et *OutputGradientTensor* doivent avoir le même *type de données* et *DimensionCount*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Entrée | 4 à 5 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | 4 à 5 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |