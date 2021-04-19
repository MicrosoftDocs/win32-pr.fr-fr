---
description: Récupère l’index généré automatiquement de la primitive dans la géométrie à l’intérieur de l’instance de la structure d’accélération de niveau inférieur.
ms.assetid: ''
title: PrimitiveIndex
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrimitiveIndex
api_type:
- NA
ms.openlocfilehash: d6d1e8ba338a3fb567b583b42074210b514ef360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544205"
---
# <a name="primitiveindex-function"></a>PrimitiveIndex fonction)

Récupère l’index généré automatiquement de la primitive dans la géométrie à l’intérieur de l’instance de la structure d’accélération de niveau inférieur.

## <a name="syntax"></a>Syntaxe

```
uint PrimitiveIndex();
```

## <a name="remarks"></a>Notes

Pour **les \_ \_ \_ \_ triangles de type Geometry RAYTRACING D3D12**, il s’agit de l’index de triangle dans l’objet Geometry.

Pour **le \_ \_ type Geometry D3D12 \_ \_ \_ \_ RAYTRACING**, il s’agit de l’index dans le tableau AABB qui définit l’objet Geometry.

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Tout nuanceur de correspondance**](any-hit-shader.md)
* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur d’intersection**](intersection-shader.md)

## <a name="see-also"></a>Voir aussi

* [Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
