---
title: Énumération MPTHREAT_DETECTION (MpClient. h)
description: Types de détection de menaces incorrects connus possibles.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION énumération des fonctionnalités d’environnement Windows héritées
- PMPTHREAT_DETECTION des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741005"
---
# <a name="mpthreat_detection-enumeration"></a>\_Énumération MPTHREAT Detection

Types de détection de menaces incorrects connus possibles.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**\_ \_ béton détection des menaces MP \_**
</dt> <dd>

Une menace a été détectée par le biais de signatures concrètes.

</dd> <dt>

<span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_heuristique de \_ détection des menaces MP \_**
</dt> <dd>

Une menace a été détectée par le biais de l’heuristique.

</dd> <dt>

<span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**\_générique de \_ détection des menaces MP \_**
</dt> <dd>

Une menace a été détectée via des signatures génériques.

</dd> <dt>

<span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**détection des menaces de MP \_ \_ \_ suspectes**
</dt> <dd>

Une menace a été détectée via la surveillance du comportement.

</dd> <dt>

<span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**\_FASTPATH de \_ détection des menaces MP \_**
</dt> <dd>

Une menace a été détectée via FastPath.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





