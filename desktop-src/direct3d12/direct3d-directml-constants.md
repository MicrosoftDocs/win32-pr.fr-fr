---
title: Constantes DirectML
description: Les constantes suivantes sont déclarées dans `DirectML.h` .
keywords:
- Constantes
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: 5f2d95d0eef67309ef1e5902ed6b968616b38bc081bd259d77418e950e4e028f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989599"
---
# <a name="directml-constants"></a>Constantes DirectML

Les constantes suivantes sont déclarées dans `DirectML.h` .

| Constante | Valeur | Description |
|-|-|-|
| DML_TENSOR_DIMENSION_COUNT_MAX | 5 | Les dizaines de DirectML prennent en charge un maximum de 5 dimensions pour DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0. |
| DML_TENSOR_DIMENSION_COUNT_MAX1 | 8 | Les dizaines de DirectML prennent en charge un maximum de 8 Dimensions pour DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0. |
| DML_TEMPORARY_BUFFER_ALIGNMENT | 256 | Les mémoires tampons temporaires et persistantes doivent avoir une adresse de base qui est alignée sur 256 octets. |
| DML_PERSISTENT_BUFFER_ALIGNMENT | 256 | Les mémoires tampons temporaires et persistantes doivent avoir une adresse de base qui est alignée sur 256 octets. |
| DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT | 16 | Les dizaines de tampons ont une exigence d’alignement d’adresse de base minimale de 16 octets. |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête | DirectML. h |

## <a name="see-also"></a>Voir aussi

* [Référence DirectML](direct3d-directml-reference.md)
* [Référence de base](direct3d-12-core-reference.md)
* [Référence de Direct3D 12](direct3d-12-reference.md)
