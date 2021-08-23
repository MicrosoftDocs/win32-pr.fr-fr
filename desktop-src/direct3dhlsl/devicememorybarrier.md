---
title: DeviceMemoryBarrier fonction)
description: Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire de l’appareil aient été effectués.
ms.assetid: 904ab8f6-4849-4b13-8fac-3967cf66574e
keywords:
- DeviceMemoryBarrier fonction HLSL
topic_type:
- apiref
api_name:
- DeviceMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f3629f7eaf8b3e271ca988b73e1dedab1e428136cc86663b64b838597d1b98c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855259"
---
# <a name="devicememorybarrier-function"></a>DeviceMemoryBarrier fonction)

Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès à la mémoire de l’appareil aient été effectués.

## <a name="syntax"></a>Syntaxe

``` syntax
void DeviceMemoryBarrier(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Pris en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




