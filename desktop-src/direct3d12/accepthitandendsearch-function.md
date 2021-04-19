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
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513938"
---
# <a name="accepthitandendsearch-function"></a>Fonction AcceptHitAndEndSearch

Utilisé dans un [nuanceur de correspondance](any-hit-shader.md) pour valider l’accès actuel, puis arrêter la recherche de plus d’accès pour le rayon. Si un nuanceur d’intersection est en cours d’exécution, son exécution s’arrête.  L’exécution passe au [nuanceur de correspondance le plus proche](closest-hit-shader.md), s’il est activé, avec l’accès le plus proche jusqu’à présent.

## <a name="syntax"></a>Syntaxe

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>Valeur de retour

**void**

## <a name="remarks"></a>Notes

Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :

* [**Nuanceur pouvant être appelé**](callable-shader.md)
* [**Nuanceur de correspondance le plus proche**](closest-hit-shader.md)
* [**Nuanceur manque**](miss-shader.md)
* [**Nuanceur de création de rayon**](ray-generation-shader.md)



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence HLSL Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




