---
title: Énumération MPRESOLVED_REASON (MpClient. h)
description: Raisons possibles d’une défaillance de correction en cours de résolution.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- MPRESOLVED_REASON énumération des fonctionnalités d’environnement Windows héritées
- PMPRESOLVED_REASON de l’héritage des Windows fonctionnalités d’environnement du pointeur d’énumération
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a365ef55d9fe2d76e619f3c772cc1df2e6c5e1c8c33721f24dc844d064b33398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975979"
---
# <a name="mpresolved_reason-enumeration"></a>MPRESOLVED \_ Reason, énumération

Raisons possibles d’une défaillance de correction en cours de résolution.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**\_raison MPRESOLVED \_ inconnue**
</dt> <dd>

Dans un état d’erreur.

</dd> <dt>

<span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**\_ \_ analyse complète de la raison MPRESOLVED \_**
</dt> <dd>

Une analyse complète a été effectuée.

</dd> <dt>

<span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**la \_ raison MPRESOLVED \_ a expiré \_**
</dt> <dd>

Suffisamment de temps s’est écoulé. La valeur par défaut est d’une semaine.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





