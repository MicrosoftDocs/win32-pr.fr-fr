---
description: Utilisé dans un nuanceur de correspondance pour valider l’accès actuel, puis arrêter la recherche de plus d’accès pour le rayon.
ms.assetid: ''
title: Fonction AcceptHitAndEndSearch
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 35073145a9b9a4788c6aed3bbae0633f0a9f5b85
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813034"
---
# <a name="accepthitandendsearch-function"></a>Fonction AcceptHitAndEndSearch

Utilisé dans un [nuanceur de correspondance](any-hit-shader.md) pour valider l’accès actuel, puis arrêter la recherche de plus d’accès pour le rayon. Si un nuanceur d’intersection est en cours d’exécution, son exécution s’arrête.  L’exécution passe au [nuanceur de correspondance le plus proche](closest-hit-shader.md), s’il est activé, avec l’accès le plus proche jusqu’à présent.

## <a name="syntax"></a>Syntaxe

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>Valeur de retour

**nullité**

## <a name="remarks"></a>Remarques

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Nuanceur pouvant être appelé**](callable-shader.md)
* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur manque**](miss-shader.md)
* [**Nuanceur de création de rayon**](ray-generation-shader.md)



## <a name="see-also"></a>Voir aussi

* [Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
