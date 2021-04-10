---
title: Structure MPTHREAT_STATS_DATA (MpClient. h)
description: Données de statistiques sur les menaces supplémentaires.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_STATS_DATA
- PMPTHREAT_STATS_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103560"
---
# <a name="mpthreat_stats_data-structure"></a>Structure de données des \_ statistiques de MPTHREAT \_

Données de statistiques sur les menaces supplémentaires.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwThreatCount**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nombre de menaces.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





