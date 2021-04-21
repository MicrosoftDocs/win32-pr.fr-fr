---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Effectue une opération d’alignement du ROI, comme décrit dans le [document R-CNN du masque](https://arxiv.org/abs/1703.06870). En résumé, l’opération extrait les cultures de l’image d’entrée tenseur et les redimensionne sur une taille de sortie commune spécifiée par les 2 dernières dimensions de *OutputTensor* à l’aide de la *InterpolationMode* spécifiée.
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: b9004a77d3b325dd3394d1a3a6b596e94997e9fd
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804013"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a>Structure DML_ROI_ALIGN_OPERATOR_DESC (directml. h)

Effectue une opération d’alignement du ROI, comme décrit dans le [document R-CNN du masque](https://arxiv.org/abs/1703.06870). En résumé, l’opération extrait les cultures de l’image d’entrée tenseur et les redimensionne sur une taille de sortie commune spécifiée par les 2 dernières dimensions de *OutputTensor* à l’aide de la *InterpolationMode* spécifiée.

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données d’entrée avec des dimensions `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .

`ROITensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données relatives aux régions d’intérêt (ROI). Les dimensions autorisées de `ROITensor` sont `{ NumROIs, 4 }` , `{ 1, NumROIs, 4 }` ou `{ 1, 1, NumROIs, 4 }` . Pour chaque retour sur investissement, les valeurs sont les coordonnées de ses angles supérieur gauche et inférieur droit dans l’ordre `[x1, y1, x2, y2]` .

`BatchIndicesTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les index de lot à partir desquels extraire le ROIs. Les dimensions autorisées de `BatchIndicesTensor` sont `{ NumROIs }` , `{ 1, NumROIs }` , `{ 1, 1, NumROIs }` ou `{ 1, 1, 1, NumROIs }` . Chaque valeur est l’index d’un lot à partir de *InputTensor*. Le comportement n’est pas défini si les valeurs ne sont pas comprises dans la plage [0, BatchCount).

`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données de sortie. Les dimensions attendues de *OutputTensor* sont `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .

`ReductionFunction`

Type : **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**

Fonction de réduction à utiliser lors de la réduction de tous les échantillons d’entrée qui contribuent à un élément de sortie ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) ou **DML_REDUCE_FUNCTION_MAX**). Le nombre d’échantillons d’entrée à réduire dans est limité par *MinimumSamplesPerOutput* et *MaximumSamplesPerOutput*.

`InterpolationMode`

Type : **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**

Mode d’interpolation à utiliser lors du redimensionnement des régions.

- [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode). Utilise l’algorithme *voisin le plus proche* , qui choisit l’élément d’entrée le plus proche du centre de pixels correspondant pour chaque élément de sortie.
- **DML_INTERPOLATION_MODE_LINEAR**. Utilise l’algorithme *bilinéaire* , qui calcule l’élément de sortie en appliquant la moyenne pondérée des 2 éléments d’entrée voisins les plus proches par dimension. Étant donné que seules 2 dimensions sont redimensionnées, la moyenne pondérée est calculée sur un total de 4 éléments d’entrée pour chaque élément de sortie.

`SpatialScaleX`

Type : <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b>

Composant X (ou largeur) du facteur d’échelle pour multiplier les coordonnées *ROITensor* par afin de les rendre proportionnées à *InputHeight* et *InputWidth*. Par exemple, si *ROITensor* contient des coordonnées normalisées (valeurs dans la plage [0.. 1]), *SpatialScaleX* aurait généralement la même valeur que *InputWidth*.

`SpatialScaleY`

Type : <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b>

Le composant Y (ou hauteur) du facteur d’échelle pour multiplier les coordonnées *ROITensor* par afin de les rendre proportionnées à *InputHeight* et *InputWidth*. Par exemple, si *ROITensor* contient des coordonnées normalisées (valeurs dans la plage [0.. 1]), *SpatialScaleY* aurait généralement la même valeur que *InputHeight*.

`OutOfBoundsInputValue`

Type : <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b>

Valeur à lire à partir de *InputTensor* lorsque les rois sont en dehors des limites de *InputTensor*. Cela peut se produire lorsque les valeurs obtenues après la mise à l’échelle de *ROITensor* par *SpatialScaleX* et *SpatialScaleY* sont supérieures à *InputWidth* et *InputHeight*.

`MinimumSamplesPerOutput`

Type : <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b>

Nombre minimal d’exemples d’entrée à utiliser pour chaque élément de sortie. L’opérateur calcule le nombre d’échantillons d’entrée en procédant de la `ScaledCropSize / OutputSize` sorte, puis le bride à *MinimumSamplesPerOutput* et *MaximumSamplesPerOutput*.

`MaximumSamplesPerOutput`

Type : <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b>

Nombre maximal d’échantillons d’entrée à utiliser pour chaque élément de sortie. L’opérateur calcule le nombre d’échantillons d’entrée en procédant de la `ScaledCropSize / OutputSize` sorte, puis le bride à *MinimumSamplesPerOutput* et *MaximumSamplesPerOutput*.

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputTensor*, *OutputTensor* et *ROITensor* doivent avoir le même *type de données*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 | FLOAT32, FLOAT16 |
| ROITensor | Entrée | 2 à 4 | FLOAT32, FLOAT16 |
| BatchIndicesTensor | Entrée | 1 à 4 | UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |