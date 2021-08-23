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
ms.openlocfilehash: 7671b45dc09c8aca494ad270aa69fc386ef3d7c03d5144fdc3e89b4f657bb07b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975939"
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
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





