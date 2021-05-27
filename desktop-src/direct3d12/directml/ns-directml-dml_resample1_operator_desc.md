---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Rééchantillonne les éléments de la source vers le tenseur de destination, en utilisant les facteurs de mise à l’échelle pour calculer la taille du tenseur de destination. Vous pouvez utiliser le mode d’interpolation linéaire ou le voisin le plus proche.
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 3cf5a49f5c92b835646e146b631abd18b4b19e6b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550394"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a>Structure DML_RESAMPLE1_OPERATOR_DESC (directml. h)
Rééchantillonne les éléments de la source vers le tenseur de destination, en utilisant les facteurs de mise à l’échelle pour calculer la taille du tenseur de destination. Vous pouvez utiliser le mode d’interpolation linéaire ou le voisin le plus proche. L’opérateur prend en charge l’interpolation sur plusieurs dimensions, pas seulement 2D. Vous pouvez conserver la même taille spatiale, mais interpoler entre les canaux ou les lots. La relation entre les coordonnées d’entrée et de sortie est la suivante.

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a>Membres

`InputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur contenant les données d’entrée.


`OutputTensor`

Type : **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tenseur dans lequel écrire les données de sortie.


`InterpolationMode`

Type : [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Ce champ détermine le type d’interpolation utilisé pour choisir les pixels de sortie.

- **DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**. Utilise l’algorithme *voisin le plus proche* , qui choisit l’élément d’entrée le plus proche du centre de pixels correspondant pour chaque élément de sortie.

- **DML_INTERPOLATION_MODE_LINEAR**. Utilise l’algorithme *Quadrilinear* , qui calcule l’élément de sortie en appliquant la moyenne pondérée des 2 éléments d’entrée voisins les plus proches par dimension. Étant donné que les 4 dimensions peuvent être rééchantillonnées, la moyenne pondérée est calculée sur un total de 16 éléments d’entrée pour chaque élément de sortie.


`DimensionCount`

Type : [ **uint**](/windows/desktop/winprog/windows-data-types)

Nombre de valeurs dans les tableaux dont les *échelles*, *InputPixelOffsets* et *OutputPixelOffsets* pointent. Cette valeur doit correspondre au nombre de dimensions de *InputTensor* et *OutputTensor*, qui doit être 4.


`Scales`

Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

Échelles à appliquer lors du rééchantillonnage de l’entrée, où Scales > 1 augmente l’image et met à l’échelle < 1 pour réduire l’image de cette dimension. Notez que les échelles n’ont pas besoin d’être exactement `OutputSize / InputSize` . Si l’entrée après la mise à l’échelle est supérieure à la limite de sortie, nous la découperons à la taille de sortie. En revanche, si l’entrée après la mise à l’échelle est plus petite que la limite de sortie, les bords de sortie sont bloqués.


`InputPixelOffsets`

Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

Offsets à appliquer aux pixels d’entrée avant le rééchantillonnage. Lorsque cette valeur est `0` , le coin supérieur gauche du pixel est utilisé à la place de son centre, ce qui n’entraîne généralement pas le résultat attendu. Pour rééchantillonner l’image à l’aide du Centre des pixels et pour avoir le même comportement que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), cette valeur doit être `0.5` .


`OutputPixelOffsets`

Type : \_ \_ taille \_ de champ (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

Offsets à appliquer aux pixels de sortie après le rééchantillonnage. Lorsque cette valeur est `0` , le coin supérieur gauche du pixel est utilisé à la place de son centre, ce qui n’entraîne généralement pas le résultat attendu. Pour rééchantillonner l’image à l’aide du Centre des pixels et pour avoir le même comportement que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), cette valeur doit être `-0.5` .


## <a name="remarks"></a>Remarques
Lorsque les *InputPixelOffsets* sont définis sur 0,5 et que les *OutputPixelOffsets* sont définis sur-0,5, cet opérateur équivaut à [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).

## <a name="availability"></a>Disponibilité
Cet opérateur a été introduit dans `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Contraintes tenseur
*InputTensor* et *OutputTensor* doivent avoir le même *type de données*.

## <a name="tensor-support"></a>Support tenseur
| Tenseur | Type | Nombre de dimensions prises en charge | Types de données pris en charge |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrée | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |