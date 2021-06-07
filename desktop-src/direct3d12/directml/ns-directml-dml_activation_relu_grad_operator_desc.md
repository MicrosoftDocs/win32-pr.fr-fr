---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour une unité linéaire redressée (ReLU).
helpviewer_keywords:
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC, DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.openlocfilehash: dea89f0e3366a07ee98f47703f07e2f5a9d4009d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417188"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a>Structure DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC (directml. h)

Calcule les dégradés de la rétropropagation pour une unité linéaire redressée (ReLU). Cet opérateur effectue le calcul suivant au niveau des éléments.

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

L’opérateur de passe en aval correspondant est [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur d’entrée (fonctionnalité). Il s’agit généralement de la même entrée que celle qui a été fournie pendant la passe en avant (voir [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).

`InputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de dégradé entrant. Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente. Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputTensor*.

`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie contenant les dégradés de la page. Les *tailles* et le *type de données* de ce tenseur doivent correspondre exactement à ceux du *InputTensor*.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputGradientTensor*, *InputTensor* et *OutputGradientTensor* doivent avoir le même *type de données*, *DimensionCount* et *tailles*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16 |
| InputGradientTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Sortie | 1 à 8 | FLOAT32, FLOAT16 |

## <a name="see-also"></a>Voir aussi
[DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |