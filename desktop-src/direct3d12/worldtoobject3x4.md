---
description: 'WorldToObject3x4 : matrice de transformation de l’espace universel vers l’espace de l’objet.'
ms.assetid: ''
title: WorldToObject3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject3x4
api_type:
- NA
ms.openlocfilehash: 5818e579076dc94a5d42003aa0af93f012e779a69e4ca78988e5c62b518a2d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631749"
---
# <a name="worldtoobject3x4"></a>WorldToObject3x4

Matrice pour la transformation de l’espace universel à l’espace de l’objet. Object-Space fait référence à l’espace de la structure d’accélération de niveau inférieur actuelle.

## <a name="syntax"></a>Syntaxe

```
void WorldToObject3x4();

```




## <a name="remarks"></a>Notes

La matrice est une transposition de la matrice **WorldToObject4x3** .

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Tout nuanceur de correspondance**](any-hit-shader.md)
* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur d’intersection**](intersection-shader.md)





## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




