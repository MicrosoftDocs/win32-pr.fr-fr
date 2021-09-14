---
description: Obtient l’emplacement actuel dans la largeur, la hauteur et la profondeur obtenues avec la valeur système [**DispatchRaysDimensions**](dispatchraysdimensions.md) intrinsèque.
title: DispatchRaysIndex
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221596"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex

Obtient l’emplacement actuel dans la largeur, la hauteur et la profondeur obtenues avec la valeur système [**DispatchRaysDimensions**](dispatchraysdimensions.md) intrinsèque.

## <a name="syntax"></a>Syntaxe

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>Notes

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants.

* [**Tout nuanceur de correspondance**](any-hit-shader.md)
* [**Nuanceur pouvant être appelé**](callable-shader.md)
* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur d’intersection**](intersection-shader.md)
* [**Nuanceur manque**](miss-shader.md)
* [**Nuanceur de création de rayon**](ray-generation-shader.md)

## <a name="see-also"></a>Voir aussi

* [Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
