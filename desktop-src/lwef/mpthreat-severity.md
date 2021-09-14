---
title: Énumération MPTHREAT_SEVERITY (MpClient. h)
description: Risque de gravité des menaces.
ms.assetid: 7C50AC74-16CB-4198-ABB2-D6999429F2EA
keywords:
- MPTHREAT_SEVERITY énumération des fonctionnalités d’environnement Windows héritées
- PMPTHREAT_SEVERITY de l’héritage des Windows fonctionnalités d’environnement du pointeur d’énumération
topic_type:
- apiref
api_name:
- MPTHREAT_SEVERITY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eec7bff3b23a89ce8187798d8a69a9968cbc2bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191927"
---
# <a name="mpthreat_severity-enumeration"></a>\_Énumération MPTHREAT Severity

Risque de gravité des menaces.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMPTHREAT_SEVERITY { 
  MP_THREAT_SEVERITY_UNKNOWN   = 0,
  MP_THREAT_SEVERITY_LOW       = 1,
  MP_THREAT_SEVERITY_MODERATE  = 2,
  MP_THREAT_SEVERITY_HIGH      = 4,
  MP_THREAT_SEVERITY_SEVERE    = 5,
  MP_THREAT_SEVERITY_MAXVALUE  = 5
} MPTHREAT_SEVERITY, *PMPTHREAT_SEVERITY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**gravité de la menace de MP \_ \_ \_ inconnue**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**gravité de menace de la MP \_ \_ \_ faible**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**gravité des menaces de MP \_ \_ \_ modéré**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**gravité des menaces de MP \_ \_ \_ élevé**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**gravité des menaces de la MP \_ \_ \_ critique**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**niveau de \_ gravité des menaces MP \_ \_ MaxValue**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





