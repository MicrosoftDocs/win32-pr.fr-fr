---
description: Cette structure contient des données pour le rapport de sollicitation de la mémoire.
ms.assetid: 42cf0922-53cc-48b9-8359-b88583ef5f1c
title: D3DMEMORYPRESSURE, structure (D3d9types. h) pour Microsoft Media Foundation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7400c4822b61a84ab288f0424cfa84e825e69dc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520293"
---
# <a name="d3dmemorypressure-structure-d3d9typesh-for-microsoft-media-foundation"></a>D3DMEMORYPRESSURE, structure (D3d9types. h) pour Microsoft Media Foundation

Contient des données pour le signalement de la sollicitation de la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>Membres

<dl> <dt>

**BytesEvictedFromProcess**
</dt> <dd>

Nombre d’octets qui ont été supprimés par le processus pendant la durée de la requête.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

Nombre total d’octets placés dans des segments de mémoire non optimaux, en raison d’un espace insuffisant dans les segments de mémoire préférés.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

Efficacité globale des allocations de mémoire qui ont été placées dans une mémoire non optimale. La valeur est exprimée sous la forme d’un pourcentage. Par exemple, la valeur 95 indique que les allocations placées dans des segments de mémoire qui ne sont pas préférés sont de 95% efficaces. Ce nombre ne doit pas être considéré comme une mesure exacte.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge | applications de \[ bureau Windows 7 uniquement\]                                                              |
| Serveur minimal pris en charge | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]                                                 |
| En-tête                  | D3d9types. h (inclure d3d9. h) |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures vidéo Direct3D](direct3d-video-structures.md)
</dt> <dt>

[Rapport de sollicitation de la mémoire](memory-pressure-reporting.md)
</dt> </dl>

 

 




