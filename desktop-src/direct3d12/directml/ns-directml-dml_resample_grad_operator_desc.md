---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour le rééchantillonnage (voir [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: ff2660257fa619edb72f10efb419f3c15f43fbde
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417360"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a>Structure DML_RESAMPLE_GRAD_OPERATOR_DESC (directml. h)

Calcule les dégradés de la rétropropagation pour le rééchantillonnage (voir [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).

**DML_RESAMPLE1_OPERATOR_DESC** redimensionne les dimensions arbitraires du tenseur d’entrée à l’aide de l’échantillonnage ou de l’interpolation bilinéaire le plus proche voisin. Étant donné un *InputGradientTensor* avec la même taille que la *sortie* d’un **DML_RESAMPLE1_OPERATOR_DESC** équivalent, cet opérateur produit un *OutputGradientTensor* avec les mêmes tailles que l' *entrée* de l' **DML_RESAMPLE1_OPERATOR_DESC**.

Par exemple, considérez un **DML_RESAMPLE1_OPERATOR_DESC** qui effectue une mise à l’échelle voisine la plus proche de 1,5 x dans la largeur, et 0,5 x dans la hauteur.

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

Notez que l’élément 0 du tenseur d’entrée (avec la valeur 1) contribue à deux éléments dans la sortie, le premier élément (avec la valeur 2) contribue à un élément dans la sortie, et les 2e et 3e éléments (avec les valeurs 3 et 4) contribuent à aucun élément de la sortie.

Le **DML_RESAMPLE_GRAD_OPERATOR_DESC** correspondant doit effectuer les opérations suivantes.

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

Notez que les valeurs de *OutputGradientTensor* représentent les contributions pondérées de cet élément au *OutputTensor* au cours de l’opérateur de **DML_RESAMPLE1_OPERATOR_DESC** d’origine.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a>Membres

`InputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de dégradé entrant. Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente. En général, ce tenseur a la même taille que la *sortie* de la [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) correspondante dans la passe de transfert.

`OutputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie contenant les dégradés de la page. En général, ce tenseur a la même taille que l' *entrée* de la [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) correspondante dans la passe en avant.

`InterpolationMode`

Type : [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Consultez *InterpolationMode* dans [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`DimensionCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre d’éléments dans les tableaux *échelles*, *InputPixelOffsets* et *OutputPixelOffsets* . Cette valeur doit être égale à la valeur de *DimensionCount* fournie dans *InputGradientTensor* et *OutputGradientTensor*.

`Scales`

Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

Consultez mettre à l' *échelle* dans [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`InputPixelOffsets`

Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

Consultez *InputPixelOffsets* dans [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`OutputPixelOffsets`

Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

Consultez *OutputPixelOffsets* dans [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputGradientTensor* et *OutputGradientTensor* doivent avoir le même *type de données*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Entrée | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Sortie | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |