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
ms.openlocfilehash: 3252389da64b74e07853069c71315b290a2ba6d5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380957"
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

## <a name="remarks"></a>Notes

Une barrière de mémoire garantit que les opérations de mémoire en suspens sont terminées. Les threads sont synchronisés aux barrières GroupSync. Cela peut bloquer un ou des threads si les opérations de mémoire sont en cours.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




