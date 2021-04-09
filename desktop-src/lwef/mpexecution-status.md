---
title: Énumération MPEXECUTION_STATUS (MpClient. h)
description: État d’exécution de la menace possible.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS énumération des fonctionnalités d’environnement Windows héritées
- PMPEXECUTION_STATUS des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
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
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843369"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





