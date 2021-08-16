---
title: AllMemoryBarrier fonction)
description: Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire aient été effectués.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- AllMemoryBarrier fonction HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fc5d22c36d67aa0e8df8352ba8fa6f2d579ddabd4825e6508499420a56bd0ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626749"
---
# <a name="allmemorybarrier-function"></a>AllMemoryBarrier fonction)

Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire aient été effectués.

## <a name="syntax"></a>Syntaxe

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Une barrière de mémoire garantit que les opérations de mémoire en suspens sont terminées. Les threads sont synchronisés aux barrières GroupSync. Cela peut bloquer un ou des threads si les opérations de mémoire sont en cours.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




