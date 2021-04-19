---
description: Matrice pour la transformation de l’espace objet en espace universel.
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: 04f80dde64984010c6e015f6e885565396d3b9c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516175"
---
# <a name="objecttoworld3x4"></a>ObjectToWorld3x4

Matrice pour la transformation de l’espace objet en espace universel. Object-Space fait référence à l’espace de la structure d’accélération de niveau inférieur actuelle.

## <a name="syntax"></a>Syntaxe

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a>Notes

La matrice est une transposition de la matrice **ObjectToWorld4x3** .

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Tout nuanceur de correspondance**](any-hit-shader.md)
* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur d’intersection**](intersection-shader.md)





## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




