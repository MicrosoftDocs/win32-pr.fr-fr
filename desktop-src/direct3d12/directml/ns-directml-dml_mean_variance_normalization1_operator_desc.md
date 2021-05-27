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
ms.openlocfilehash: ae22b004f1e879eb020ddcfe39a5f26481a508b0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549775"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a>Structure DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (directml. h)

Exécute une fonction de normalisation de variance moyenne sur le tenseur d’entrée. Cet opérateur calcule la moyenne et la variance du tenseur d’entrée pour effectuer la normalisation. Cet opérateur effectue le calcul suivant.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

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

Tenseur facultatif contenant les données de mise à l’échelle.

Si **DML_FEATURE_LEVEL** est inférieur à **DML_FEATURE_LEVEL_4_0**, les dimensions de ce tenseur doivent être `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` . Les dimensions ScaleBatchCount, ScaleHeight et ScaleWidth doivent correspondre à *InputTensor*, ou être définies sur 1 pour diffuser automatiquement ces dimensions sur l’entrée.

Si **DML_FEATURE_LEVEL** est supérieur ou égal à **DML_FEATURE_LEVEL_4_0**, toute dimension peut être définie sur 1 et être automatiquement diffusée pour correspondre à *InputTensor*.

Ce tenseur est requis si le *BiasTensor* est utilisé.

`BiasTensor`

Type : \_ MAYBENULL \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***


Tenseur facultatif contenant les données de biais.

Si **DML_FEATURE_LEVEL** est inférieur à **DML_FEATURE_LEVEL_4_0**, les dimensions de ce tenseur doivent être `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` . Les dimensions BiasBatchCount, BiasHeight et BiasWidth doivent correspondre à *InputTensor* ou être définies sur 1 pour diffuser automatiquement ces dimensions sur l’entrée.

Si **DML_FEATURE_LEVEL** est supérieur ou égal à **DML_FEATURE_LEVEL_4_0**, toute dimension peut être définie sur 1 et être automatiquement diffusée pour correspondre à *InputTensor*.

Ce tenseur est requis si le *ScaleTensor* est utilisé.

`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur dans lequel écrire les résultats. Les dimensions de ce tenseur sont `{ BatchCount, ChannelCount, Height, Width }` .

`AxisCount`

Type : <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b>

Nombre d’axes. Ce champ détermine la taille du tableau *axes* .

`Axes`

Type : \_ \_ taille \_ de champ (AxisCount) **const [uint](../../winprog/windows-data-types.md) \*** 

Axes sur lesquels calculer la moyenne et la variance.

`NormalizeVariance`

Type : <b> <a href="/windows/win32/winprog/windows-data-types">bool</a></b>

**True** si la couche de normalisation comprend une variance dans le calcul de normalisation. Sinon, **false**. Si la **valeur est false**, l’équation de normalisation est `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .

`Epsilon`

Type : <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b>

Valeur Epsilon à utiliser pour éviter la division par zéro. La valeur par défaut 0,00001 est recommandée.

`FusedActivation`

Type : \_ MAYBENULL \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***

Couche d’activation fusionnée facultative à appliquer après la normalisation.

## <a name="remarks"></a>Remarques
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** est un sur-ensemble de fonctionnalités de [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). Ici, la définition du tableau **axes** sur `{ 0, 2, 3 }` est l’équivalent de la définition de *CrossChannel* sur **false** dans **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; la définition du tableau **axes** sur équivaut à `{ 1, 2, 3 }` définir *CrossChannel* sur **true**.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur

*BiasTensor*, *InputTensor*, *OutputTensor* et *ScaleTensor* doivent avoir le même *type de données* et *DimensionCount*.

## <a name="tensor-support"></a>Support tenseur

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 et versions ultérieures

| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 1 à 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrée facultative | 1 à 8 | FLOAT32, FLOAT16 |
| BiasTensor | Entrée facultative | 1 à 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 1 à 8 | FLOAT32, FLOAT16 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 et versions ultérieures

| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrée facultative | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Entrée facultative | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |

## <a name="see-also"></a>Voir aussi

[Utilisation d’opérateurs fusionnés pour améliorer les performances](../dml-fused-activations.md)