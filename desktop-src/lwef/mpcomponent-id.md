---
title: Énumération MPCOMPONENT_ID (MpClient. h)
description: Composants possibles pour le gestionnaire de protection contre les programmes malveillants.
ms.assetid: 014B400A-880B-419D-9F50-F3354CE945D9
keywords:
- MPCOMPONENT_ID énumération des fonctionnalités d’environnement Windows héritées
- PMPCOMPONENT_ID des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPCOMPONENT_ID
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196eebc5a3bee4968878c376cd7358724c9c55cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103385"
---
# <a name="mpcomponent_id-enumeration"></a>\_Énumération MPCOMPONENT ID

Composants possibles pour le gestionnaire de protection contre les programmes malveillants.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMPCOMPONENT_ID { 
  MPCOMPONENT_AS_SIGNATURE         = 0,
  MPCOMPONENT_AV_SIGNATURE         = 1,
  MPCOMPONENT_REALTIME_MONITOR     = 2,
  MPCOMPONENT_ONACCESS_PROTECTION  = 3,
  MPCOMPONENT_IOAV_PROTECTION      = 4,
  MPCOMPONENT_BEHAVIOR_MONITOR     = 5,
  MPCOMPONENT_AUTO_SCAN            = 6,
  MPCOMPONENT_AUTO_SIGUPDATE       = 7,
  MPCOMPONENT_IPC                  = 8,
  MPCOMPONENT_NIS                  = 9,
  MPCOMPONENT_ELAM                 = 10,
  MPCOMPONENT_MAXVALUE             = 10
} MPCOMPONENT_ID, *PMPCOMPONENT_ID;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPCOMPONENT_AS_SIGNATURE"></span><span id="mpcomponent_as_signature"></span>**MPCOMPONENT \_ comme \_ signature**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AV_SIGNATURE"></span><span id="mpcomponent_av_signature"></span>**\_signature AV \_ MPCOMPONENT**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_REALTIME_MONITOR"></span><span id="mpcomponent_realtime_monitor"></span>**\_moniteur en temps réel MPCOMPONENT \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_ONACCESS_PROTECTION"></span><span id="mpcomponent_onaccess_protection"></span>**\_protection MPCOMPONENT onaccess \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_IOAV_PROTECTION"></span><span id="mpcomponent_ioav_protection"></span>**\_protection MPCOMPONENT IOAV \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_BEHAVIOR_MONITOR"></span><span id="mpcomponent_behavior_monitor"></span>**\_moniteur de comportement MPCOMPONENT \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AUTO_SCAN"></span><span id="mpcomponent_auto_scan"></span>**\_analyse automatique \_ MPCOMPONENT**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AUTO_SIGUPDATE"></span><span id="mpcomponent_auto_sigupdate"></span>**MPCOMPONENT \_ auto \_ SIGUPDATE**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_IPC"></span><span id="mpcomponent_ipc"></span>**\_IPC MPCOMPONENT**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_NIS"></span><span id="mpcomponent_nis"></span>**MPCOMPONENT \_ NIS**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_ELAM"></span><span id="mpcomponent_elam"></span>**MPCOMPONENT \_ Elam**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_MAXVALUE"></span><span id="mpcomponent_maxvalue"></span>**MPCOMPONENT \_ MaxValue**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





