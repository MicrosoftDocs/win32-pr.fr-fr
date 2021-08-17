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
ms.openlocfilehash: 1b40987c76f42d41d74b7cb3d41f35cc20bd5a6ac1414ae9b010cedcfa7ef9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124163"
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
