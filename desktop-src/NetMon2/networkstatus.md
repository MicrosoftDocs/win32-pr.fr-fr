---
description: La structure NETWORKSTATUS décrit l’état actuel du NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: NETWORKSTATUS, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530226"
---
# <a name="networkstatus-structure"></a>NETWORKSTATUS, structure

La structure **NETWORKSTATUS** décrit l’état actuel du NPP.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a>Membres

<dl> <dt>

**State**
</dt> <dd>

Indique l’état actuel du NPP.



| Valeur                                                                                                                                                                                                          | Signification                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <dt>**NETWORKSTATUS \_ état \_ void**</dt> </dl>                | Le NPP n’est pas connecté ou est connecté et la capture n’est pas démarrée.<br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <dt>**capture de l' \_ État NETWORKSTATUS \_**</dt> </dl> | Le NPP capture des données.<br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <dt>**État de NETWORKSTATUS \_ \_ suspendu**</dt> </dl>          | Le NPP s’est interrompu lors de la capture des données.<br/>                                     |



 

</dd> <dt>

**Indicateurs**
</dt> <dd>

Indicateurs qui décrivent l’état actuel du NPP.



| Valeur                                                                                                                                                                                                                             | Signification                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <dt>**\_déclencheur d’indicateurs NETWORKSTATUS \_ \_ en attente**</dt> </dl> | Il existe un déclencheur en attente pour le NPP.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Lors de l’utilisation de cette structure, vous devez allouer la mémoire pour la structure avant de pouvoir l’utiliser et libérer la mémoire lorsque la structure n’est plus nécessaire.

La liste Voir aussi en bas de cette rubrique répertorie toutes les méthodes qui utilisent cette structure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC :: QueryStatus](idelaydc-querystatus.md)
</dt> <dt>

[IESP :: QueryStatus](iesp-querystatus.md)
</dt> <dt>

[IRTC :: QueryStatus](irtc-querystatus.md)
</dt> <dt>

[IStats :: QueryStatus](istats-querystatus.md)
</dt> </dl>

 

 




