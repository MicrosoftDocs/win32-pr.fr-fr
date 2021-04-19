---
description: La structure QUERYTABLE fournit une liste des ordinateurs qui utilisent actuellement Moniteur réseau pour capturer les données réseau.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: QUERYTABLE, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517796"
---
# <a name="querytable-structure"></a>QUERYTABLE, structure

La structure **QUERYTABLE** fournit une liste des ordinateurs qui utilisent actuellement Moniteur réseau pour capturer les données réseau.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a>Membres

<dl> <dt>

**nStationQueries**
</dt> <dd>

En entrée, le nombre maximal d’ordinateurs que vous souhaitez Moniteur réseau renvoyer.

Lors de la sortie, le nombre de structures [STATIONQUERY](stationquery.md) retournées par Moniteur réseau. Chaque structure **STATIONQUERY** représente un ordinateur qui capture actuellement des données.

</dd> <dt>

**StationQuery**
</dt> <dd>

En entrée, tableau de structures [STATIONQUERY](stationquery.md) vides qui contient le nombre d’éléments spécifié dans **nStationQueries**.

Lors de la sortie, il s’agit d’une structure [STATIONQUERY](stationquery.md) remplie pour chaque ordinateur qui capture des données. Le nombre d’éléments remplis est retourné par **nStationQueries**.

</dd> </dl>

## <a name="remarks"></a>Notes

La mémoire pour cette structure et le tableau [STATIONQUERY](stationquery.md) doit être allouée par l’application appelante et libérée une fois que les informations ne sont plus nécessaires.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC::QueryStations](idelaydc-querystations.md)
</dt> <dt>

[IESP::QueryStations](iesp-querystations.md)
</dt> <dt>

[IRTC::QueryStations](irtc-querystations.md)
</dt> <dt>

[IStats::QueryStations](istats-querystations.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




