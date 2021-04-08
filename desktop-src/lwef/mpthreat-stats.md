---
title: Structure MPTHREAT_STATS (MpClient. h)
description: Statistiques relatives aux menaces.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_STATS
- PMPTHREAT_STATS des fonctionnalités d’environnement Windows héritées du pointeur de structure
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843501"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





