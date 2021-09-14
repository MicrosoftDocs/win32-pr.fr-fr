---
title: Structure MPTHREAT_STATS (MpClient. h)
description: Statistiques relatives aux menaces.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_STATS
- PMPTHREAT_STATS des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118246"
---
# <a name="mpthreat_stats-structure"></a>MPTHREAT, \_ structure des statistiques

Statistiques relatives aux menaces.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a>Membres

<dl> <dt>

**ThreatCount**
</dt> <dd>

Type : **uint**

</dd> <dd>

Nombre de menaces détectées.

</dd> <dt>

**SuspiciousThreatCount**
</dt> <dd>

Type : **uint**

</dd> <dd>

Nombre de menaces détectées avec l’analyse du comportement.

</dd> <dt>

**Reserved**
</dt> <dd>

Type : **uint \[ 4 \]**

</dd> <dd>

Champs réservés pour une utilisation ultérieure.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





