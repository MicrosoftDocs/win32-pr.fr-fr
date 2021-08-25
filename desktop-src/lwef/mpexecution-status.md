---
title: Énumération MPEXECUTION_STATUS (MpClient. h)
description: État d’exécution de la menace possible.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS énumération des fonctionnalités d’environnement Windows héritées
- PMPEXECUTION_STATUS de l’héritage des Windows fonctionnalités d’environnement du pointeur d’énumération
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4748b6d97e1b7ee05db8044837b89e2653a14fd1e6f87068a40107cdd9ee60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943909"
---
# <a name="mpexecution_status-enumeration"></a>\_Énumération de l’État MPEXECUTION

État d’exécution de la menace possible.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**État d’exécution du point de gestion \_ \_ \_ inconnu**
</dt> <dd>

L’état d’exécution n’est pas connu.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**État de l’exécution du point de gestion \_ \_ \_ bloqué**
</dt> <dd>

Blocage de l’exécution par mini-filtre.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**État d’exécution du point de gestion \_ \_ \_ autorisé**
</dt> <dd>

Autorisé à s’exécuter par mini-filtre.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**\_État de l’exécution du pack d’exécution \_ \_**
</dt> <dd>

La menace est en cours d’exécution.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**État d’exécution du pack d' \_ exécution \_ \_ non \_ exécuté**
</dt> <dd>

La menace n’est pas en cours d’exécution et n’est disponible qu’à partir du moteur pendant la mise à jour.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





