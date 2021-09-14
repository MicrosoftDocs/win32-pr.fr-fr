---
title: GroupMemoryBarrierWithGroupSync fonction)
description: Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès partagés au groupe aient été effectués et que tous les threads du groupe aient atteint cet appel.
ms.assetid: 64dd78e1-c597-4bd0-8a9b-592123178de5
keywords:
- GroupMemoryBarrierWithGroupSync fonction HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07798bb8ad6bd9c4cdfa14bfa57d97818dbd6962
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127297126"
---
# <a name="groupmemorybarrierwithgroupsync-function"></a>GroupMemoryBarrierWithGroupSync fonction)

Bloque l’exécution de tous les threads dans un groupe jusqu’à ce que tous les accès partagés au groupe aient été effectués et que tous les threads du groupe aient atteint cet appel.

## <a name="syntax"></a>Syntaxe

``` syntax
void GroupMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




