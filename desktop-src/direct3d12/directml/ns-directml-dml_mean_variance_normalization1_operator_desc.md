---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Exécute une fonction de normalisation de variance moyenne sur le tenseur d’entrée. Cet opérateur calcule la moyenne et la variance du tenseur d’entrée pour effectuer la normalisation.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106531445"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>Structure DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (directml. h)
Exécute une fonction de normalisation de variance moyenne sur le tenseur d’entrée. Cet opérateur calcule la moyenne et la variance du tenseur d’entrée pour effectuer la normalisation. Cet opérateur effectue le calcul suivant.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```



## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données d’entrée. Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, Height, Width }` .


`ScaleTensor`

Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur facultatif contenant les données de mise à l’échelle. Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, Height, Width }` . Toutes les dimensions peuvent être remplacées par 1 pour diffuser dans cette dimension. Ce tenseur est requis si le *BiasTensor* est utilisé.


`BiasTensor`

Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur facultatif contenant les données de biais. Les dimensions de ce tenseur doivent être `{ BatchCount, ChannelCount, Height, Width }` . Toutes les dimensions peuvent être remplacées par 1 pour diffuser dans cette dimension. Ce tenseur est requis si le *ScaleTensor* est utilisé.


`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur dans lequel écrire les résultats. Les dimensions de ce tenseur sont `{ BatchCount, ChannelCount, Height, Width }` .


`AxisCount`

Type : <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b>

Nombre d’axes. Ce champ détermine la taille du tableau *axes* .


`Axes`

Type : \_ \_ taille \_ de champ (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \*** 

Axes sur lesquels calculer la moyenne et la variance.


`NormalizeVariance`

Type : <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b>

**True** si la couche de normalisation comprend une variance dans le calcul de normalisation. Sinon, **false**. Si la **valeur est false**, l’équation de normalisation est `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .


`Epsilon`

Type : <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b>

Valeur Epsilon à utiliser pour éviter la division par zéro. La valeur par défaut 0,00001 est recommandée.


`FusedActivation`

Type : \_ MAYBENULL \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

Couche d’activation fusionnée facultative à appliquer après la normalisation.


## <a name="remarks"></a>Notes
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** est un sur-ensemble de fonctionnalités de [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). Ici, la définition du tableau **axes** sur `{ 0, 2, 3 }` est l’équivalent de la définition de *CrossChannel* sur **false** dans **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; la définition du tableau **axes** sur équivaut à `{ 1, 2, 3 }` définir *CrossChannel* sur **true**.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
* *InputTensor* et *OutputTensor* doivent avoir la même *taille*.
* *BiasTensor*, *InputTensor*, *OutputTensor* et *ScaleTensor* doivent avoir le même *type de données*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Dimensions | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrée | {BatchCount, ChannelCount, hauteur, largeur} | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrée facultative | {ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth} | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Entrée facultative | { BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth } | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | {BatchCount, ChannelCount, hauteur, largeur} | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |

## <a name="see-also"></a>Voir aussi

[Utilisation d’opérateurs fusionnés pour améliorer les performances](../dml-fused-activations.md)