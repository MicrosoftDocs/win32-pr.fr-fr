---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcule les dégradés de la rétropropagation pour la [normalisation de réponse locale](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: eecf849a06ee8e99ac9c015ecd4568496120b2d9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804438"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a>DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml. h)

Calcule les dégradés de la rétropropagation pour la [normalisation de réponse locale](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).

Le type de données et la taille de tous les dizaines doivent être identiques.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,5 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données d’entrée. Les *tailles* de ce tenseur doivent être `{ BatchCount, ChannelCount, Height, Width }` .

`InputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de dégradé entrant. Elle est généralement obtenue à partir de la sortie de la rétropropagation d’une couche précédente.

`OutputGradientTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur de sortie contenant les dégradés de la page.

`CrossChannel`

Type : **[bool](/windows/win32/winprog/windows-data-types)**

**True** si la couche LRN est additionnée sur plusieurs canaux ; **False** si la couche LRN est additionnée dans les dimensions spatiales.

`LocalSize`

Type : **[uint](/windows/win32/winprog/windows-data-types)**

Nombre maximal d’éléments à additionner par dimension (la région locale est découpée de manière à ce que tous les éléments soient dans les limites). Si *CrossChannel* a la **valeur true**, il s’agit de la largeur et de la hauteur de la région locale. Si *CrossChannel* a la **valeur false**, il s’agit du nombre d’éléments dans la région locale. La valeur doit être au moins à 1.

`Alpha`

Type : **[float](/windows/win32/winprog/windows-data-types)**

Valeur du paramètre de mise à l’échelle. Nous recommandons la valeur par défaut 0,0001.

`Beta`

Type : **[float](/windows/win32/winprog/windows-data-types)**

Valeur de l’exposant. Nous recommandons la valeur par défaut 0,75.

`Bias`

Type : **[float](/windows/win32/winprog/windows-data-types)**

Valeur de Bias. Nous recommandons la valeur par défaut 1.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputGradientTensor*, *InputTensor* et *OutputGradientTensor* doivent avoir le même *type de données* et les mêmes *tailles*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 | FLOAT32, FLOAT16 |
| InputGradientTensor | Entrée | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |
